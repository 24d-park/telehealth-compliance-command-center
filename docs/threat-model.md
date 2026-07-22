# Threat Model

STRIDE-based threat model for the Telehealth & Pharmacy Compliance Command Center.
Read alongside `SECURITY.md` (which explains *why* each control exists). This document
maps **assets → threats → mitigations** so the controls are justified by concrete risks,
not habit.

> **V1 scope:** no PHI, prescriptions, patient names, or real credentials. The system of
> record is *regulatory rules + the organization's own credentials/documents*.

---

## 1. Assets (what an attacker wants, or what we must not lose)

| # | Asset | Why it's valuable | Class |
|---|-------|-------------------|-------|
| A1 | Uploaded licenses, permits, inspection PDFs | Confidential business docs; integrity + confidentiality critical | Confidential |
| A2 | Internal compliance notes / interpretations | Reveal legal posture, gaps, strategy | Internal |
| A3 | Requirement records + **source history** | The system of record; decisions depend on it being accurate & tamper-evident | Internal |
| A4 | Audit log | Proof of who did what; must be tamper-evident | Internal |
| A5 | User accounts, roles, sessions | Foothold; role escalation = broad access | Confidential |
| A6 | Secrets (DB creds, API keys, signing keys) | Keys to everything else | Confidential |
| A7 | Availability of the service | Compliance work is time-sensitive (deadlines) | — |

---

## 2. Trust boundaries

- **Browser ↔ Server** — untrusted network; all input crosses here. → TLS, input validation.
- **App ↔ Database** — parameterized access only; app enforces RBAC before the DB sees a query.
- **App ↔ File storage** — uploads stored outside web root, served via authenticated,
  non-executable paths.
- **App ↔ External APIs (search/chat/LLM)** — outbound; secrets involved; abusable/expensive.
- **User ↔ User (role boundary)** — Read-only must not reach Compliance/Admin capabilities.

---

## 3. STRIDE analysis

### Spoofing (pretending to be someone else)
| Threat | Mitigation |
|--------|-----------|
| Stolen/guessed credentials | Strong password policy, account lockout/throttling on login, MFA (post-V1), short session lifetimes |
| Session hijacking | `Secure` + `HttpOnly` + `SameSite` cookies, TLS/HSTS, session rotation on login, idle+absolute timeout |
| Anonymous access to data | Authentication required on every route; deny-by-default |

### Tampering (unauthorized modification)
| Threat | Mitigation |
|--------|-----------|
| Silent overwrite of a requirement | **Source history / versioning** — edits create new versions, prior versions retained |
| Editing/deleting the audit log | Append-only store; audit writes not exposed to app users; separate credentials/retention |
| Malicious file replacing a real document | Versioned document storage; integrity hash on upload; RBAC on replace/delete |
| SQL injection altering data | Parameterized queries / ORM; input validation |
| Request tampering in transit | TLS + integrity from HTTPS |

### Repudiation (denying an action)
| Threat | Mitigation |
|--------|-----------|
| "I didn't change that status" | **Audit log** binds every edit/status change/upload to an authenticated identity + timestamp + old→new |
| Untraceable deletions | Soft-delete + audit entry; hard-delete restricted to Admin and logged |

### Information disclosure (leaks)
| Threat | Mitigation |
|--------|-----------|
| Documents read in transit | TLS/HSTS |
| Direct-object access (guessing a doc URL) | Authorization check per object (not just authentication); unguessable IDs; docs served through app, not static |
| Secrets leaked via repo/logs | Secrets in `.env` (git-ignored); scrub secrets from logs; `.env.example` only |
| Verbose error messages | Generic errors to client; details to server logs only |
| Data scraping | Rate limiting; pagination caps; authz on bulk/export |
| **Accidental PHI ingestion** | Input validation rejects patient-data-shaped fields; no PHI schema exists in V1 |

### Denial of Service (availability)
| Threat | Mitigation |
|--------|-----------|
| Flooding search/chat endpoints | **Rate limiting** (per-user + per-IP), burst + sustained caps, 429s |
| Oversized/many file uploads | Size caps, count caps, type allow-list |
| Expensive LLM/chat abuse (cost DoS) | Rate limit + per-user quotas on chat endpoints |
| Resource-heavy queries | Query timeouts, pagination, indexed columns |

### Elevation of privilege (gaining rights you shouldn't have)
| Threat | Mitigation |
|--------|-----------|
| Read-only performs writes | Server-side RBAC checks on every mutating route (never trust the UI) |
| PIC edits another site's / another dimension's data | Scope checks (site/dimension ownership) in addition to role |
| Horizontal access (user A reads user B's docs) | Per-object authorization |
| Forced browsing to admin routes | Deny-by-default; role required server-side, not hidden-in-UI-only |

---

## 4. Attacker personas (who, realistically)

- **External unauthenticated attacker** — scans, injection, credential stuffing, upload abuse.
  Countered by: auth, validation, rate limiting, file restrictions, TLS.
- **Malicious/careless insider (low role)** — tries to edit rules, exfiltrate docs, or cover
  tracks. Countered by: RBAC, audit log, source history, per-object authz.
- **Compromised account** — legitimate creds, hostile use. Countered by: least privilege
  (limits blast radius), audit log (detects/scopes), MFA (post-V1).
- **Curious/abusive automated client** — scrapes or runs up API cost. Countered by: rate
  limiting + quotas.

---

## 5. Residual risk / accepted for V1

| Risk | Status |
|------|--------|
| No MFA in V1 | Accepted; mitigated by lockout + short sessions; add MFA next |
| App-native auth (no SSO) | Accepted for single-org V1 |
| No field-level encryption at rest | Accepted; rely on disk/volume encryption + access control |
| Single-tenant (no hard multi-tenant isolation) | Accepted for V1 |

Each is a *decision*, revisited when scope (or a customer) demands it.

---

## 6. Mapping back to SECURITY.md controls

| Control | Primary STRIDE categories addressed |
|---------|-------------------------------------|
| Authenticated users | Spoofing, Info disclosure, Elevation |
| RBAC (Admin/Compliance/PIC/Read-only) | Elevation, Tampering, Info disclosure |
| No patient data in V1 | Info disclosure (shrinks stakes) |
| HTTPS/TLS | Info disclosure, Tampering, Spoofing |
| Attachment restrictions | Tampering, DoS, Elevation (RCE) |
| Audit log | Repudiation, Tampering (detection) |
| Rate limiting | DoS, Info disclosure (scraping) |
| Input validation | Tampering, Info disclosure, Elevation |
| Secrets in .env | Info disclosure |
| Source history | Tampering, Repudiation |
