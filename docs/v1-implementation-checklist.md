# V1 Implementation Checklist

Maps every control in `SECURITY.md` to concrete, buildable tasks and suggested tech.
Tech suggestions are **defaults, not mandates** — swap for your stack. The point is that
each security control has a real implementation owner and an acceptance test.

> **V1 hard rule:** no PHI, prescriptions, patient names, or real credentials — anywhere,
> including seed/demo data. Everything below assumes that constraint.

Legend: `[ ]` todo · suggested tech in _italics_.

---

## 0. Foundation / architecture
- [ ] Pick a server framework (this is currently a static single-file HTML demo; V1 needs a
      backend). _Node/Express or Fastify · Python/FastAPI or Django · Go/chi_
- [ ] Database for records, versions, audit, users. _PostgreSQL_ (row-level control, JSONB,
      strong constraints)
- [ ] Object storage for uploads, **outside web root**. _S3-compatible bucket, or a
      non-served disk path_
- [ ] Environment separation: dev / staging / prod, each with its own secrets.
- [ ] Keep the existing dashboard as the read UI; put all writes behind the authenticated API.

## 1. Authenticated users
- [ ] App-native auth with a vetted library — **do not hand-roll**. _Lucia / Auth.js
      (Node) · Django auth · Authlib (FastAPI)_
- [ ] Password hashing with a slow KDF. _argon2id (preferred) or bcrypt_
- [ ] Login throttling + account lockout after N failed attempts.
- [ ] Session cookies: `Secure`, `HttpOnly`, `SameSite=Lax/Strict`; rotate session id on login.
- [ ] Idle timeout + absolute session lifetime.
- [ ] (Post-V1) MFA/TOTP.
- **Acceptance:** unauthenticated request to any data route → 401; brute force → lockout.

## 2. Role-based access control (Admin / Compliance / PIC / Read-only)
- [ ] `roles` + `user_roles` tables; role required on every mutating route **server-side**.
- [ ] Deny-by-default middleware — routes opt *in* to a required role.
- [ ] PIC scoping: additional site/dimension ownership check beyond role.
- [ ] Per-object authorization for documents (not just "is logged in").
- [ ] UI hides controls by role **and** the server enforces it (UI hiding is not security).
- **Acceptance:** Read-only POST/PUT/DELETE → 403; PIC editing another site → 403.

## 3. No patient data in V1
- [ ] Schema contains **no** PHI fields (no patient name/DOB/Rx/MRN columns).
- [ ] Input validation rejects free-text that matches PHI patterns where feasible.
- [ ] Seed/demo data is 100% synthetic; a check/script asserts no real credential formats.
- **Acceptance:** schema review shows no PHI columns; demo data scan is clean.

## 4. Encrypted transport (HTTPS/TLS)
- [ ] TLS terminated at proxy/load balancer. _Caddy (auto-HTTPS) · nginx + Let's Encrypt_
- [ ] HTTP → HTTPS redirect; **HSTS** header (`max-age`, `includeSubDomains`).
- [ ] Modern TLS only (1.2+); secure ciphers.
- [ ] Security headers: `Content-Security-Policy`, `X-Content-Type-Options: nosniff`,
      `Referrer-Policy`, `X-Frame-Options`/frame-ancestors.
- **Acceptance:** plain HTTP redirects; SSL Labs / testssl.sh grade A; headers present.

## 5. Attachment / file-upload restrictions
- [ ] Type allow-list (PDF, PNG, JPG) enforced by **magic-byte/content sniff**, not extension.
      _file-type (Node) · python-magic_
- [ ] Max size + max count per request; reject over-limit with 413.
- [ ] Sanitize/normalize filenames; generate storage keys server-side (never trust client name).
- [ ] Store outside web root; serve via authenticated route with forced download + non-executable
      content-type.
- [ ] Malware scan on upload where available. _ClamAV_
- [ ] Strip/deny active content (no SVG-as-image, no HTML).
- **Acceptance:** uploading `.html`/`.svg`/renamed `.exe` is rejected; stored files can't execute.

## 6. Audit log for edits / status changes
- [ ] `audit_log` table: actor_id, action, entity, entity_id, old_value, new_value, timestamp, ip.
- [ ] Write on: requirement edit, status change, upload, delete, permission change, login events.
- [ ] **Append-only**: no UPDATE/DELETE grant for the app role; separate retention.
- [ ] Read view for Admin + Read-only auditor; no user can edit it.
- **Acceptance:** every status change produces an immutable log row with old→new.

## 7. Rate limiting on search / chat endpoints
- [ ] Per-user + per-IP limits with burst + sustained windows. _token bucket · Redis-backed
      (rate-limiter-flexible / slowapi / nginx limit_req)_
- [ ] Stricter limits + per-user quota on any chat/LLM endpoint (cost control).
- [ ] Return `429` with `Retry-After`; log abusers.
- **Acceptance:** exceeding the limit returns 429; chat quota caps per-user spend.

## 8. Input validation
- [ ] Server-side schema validation on every endpoint. _zod / Joi (Node) · Pydantic (FastAPI)
      · DRF serializers (Django)_
- [ ] Allow-lists for enums (status, role, dimension); length + format caps on all strings.
- [ ] Parameterized queries / ORM everywhere — no string-built SQL.
- [ ] Output encoding on render; sanitize any user HTML. _DOMPurify if rich text is ever allowed_
- **Acceptance:** injection payloads are rejected/escaped; malformed enum → 400.

## 9. Secrets in .env
- [ ] All secrets from env vars; `.env` git-ignored; commit only `.env.example` with placeholders.
- [ ] Validate required env vars at boot (fail fast if missing).
- [ ] Secret scanning in CI. _gitleaks / trufflehog_
- [ ] Scrub secrets from logs and error output.
- [ ] Plan rotation; (prod) consider a manager. _AWS Secrets Manager · Vault · Doppler_
- **Acceptance:** repo contains no real secret; app refuses to boot without required vars.

## 10. Source history — never silently overwrite a requirement
- [ ] `requirements` + `requirement_versions` (or event-sourced) — edits INSERT a new version.
- [ ] Each version stores: value, source citation, source URL, source date, editor, timestamp.
- [ ] "Current" is a pointer to the latest version; history is viewable + diff-able.
- [ ] No destructive UPDATE of a requirement's substance; revert = new version.
- [ ] Surface history in the state modal (extends the existing provenance UI).
- **Acceptance:** editing a requirement preserves the prior version with its source intact.

---

## Cross-cutting
- [ ] Dependency scanning in CI. _npm audit / pip-audit · Dependabot_
- [ ] Automated tests for authz (the highest-value security tests: role × route matrix).
- [ ] Structured logging (no secrets/PHI) + basic alerting on auth failures / 429 spikes.
- [ ] Backups of DB + object storage; test restore.
- [ ] Pre-launch: run the acceptance tests above as a release gate.

## Suggested build order
1. Backend skeleton + Postgres + `.env` loading + fail-fast config **(0, 9)**
2. Auth + sessions **(1)**
3. RBAC middleware + deny-by-default **(2)**
4. Requirements + **source history** + audit log **(10, 6)**
5. Input validation across all routes **(8)**
6. File uploads with restrictions **(5)**
7. TLS + security headers at the edge **(4)**
8. Rate limiting on search/chat **(7)**
9. No-PHI schema review + demo-data scan **(3)** — verify before any demo
10. CI scanning, authz tests, backups **(cross-cutting)**
