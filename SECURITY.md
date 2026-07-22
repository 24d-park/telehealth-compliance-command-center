# Security & Access

Security and access-control model for the Telehealth & Pharmacy Compliance Command Center.

This document explains **why** each control exists — not just that it's required. As the tool
grows from a single-file demo into a system that may hold **licenses, inspection documents,
and internal compliance notes**, the threat model changes: the data becomes something a
regulator, a competitor, or an attacker would care about, and something the organization is
legally accountable for keeping accurate and auditable.

> **Scope note — V1 has NO patient data.** No PHI, prescriptions, patient names, or real
> credentials appear in the demo or V1. This is a deliberate scoping decision (see below),
> not a temporary gap. It keeps V1 out of HIPAA scope while the security foundation is built.

---

## Data classification (what we're protecting)

| Class | Examples | Sensitivity |
|-------|----------|-------------|
| Public | Statute citations, public board rules | Low |
| Internal | Compliance notes, interpretations, gap analyses | Medium |
| Confidential | Uploaded licenses, inspection reports, permit PDFs | High |
| **Excluded in V1** | PHI, prescriptions, patient names, real credentials | **Not stored** |

The controls below are sized to the highest class the system actually holds
(Confidential) — never to the least.

---

## Controls and why each one matters

### 1. Authenticated users
**What:** No anonymous access. Every request is tied to a known identity via login.

**Why it matters:** The moment the tool holds internal compliance notes or license
documents, "who saw / changed this?" becomes a question you must be able to answer.
Anonymous access makes that impossible and makes every other control (audit log, RBAC,
rate limiting per user) meaningless. Authentication is the anchor the rest of the model
hangs off — without a verified identity there is nothing to authorize, log, or rate-limit.

### 2. Role-based access control (Admin / Compliance / PIC / Read-only)
**What:** Permissions are granted by role, following least privilege — users get the
minimum access their job needs.

| Role | Typical rights |
|------|----------------|
| **Admin** | Manage users/roles, system config, everything below |
| **Compliance** | Create/edit requirements, change status, upload documents, source data |
| **PIC** (Pharmacist-in-Charge) | Edit pharmacy-scoped fields, upload permits/inspections for their location(s) |
| **Read-only** | View dashboard, export, read audit trail — no writes |

**Why it matters:** Not everyone who needs to *see* compliance status should be able to
*change* a regulatory requirement or delete an inspection document. A read-only auditor,
a PIC responsible for one site, and a compliance lead have very different needs and very
different blast radii if their account is compromised. RBAC contains the damage of a stolen
credential and prevents accidental edits by people who were only meant to look. It also maps
cleanly to real accountability: a status change by "Compliance" means something different
from one by "Admin."

### 3. No patient data in V1
**What:** The system stores no PHI, prescriptions, patient names, or real credentials in V1
or the demo. Compliance data is *about rules and the organization's own credentials*, not
about patients.

**Why it matters:** PHI triggers HIPAA — with breach-notification duties, BAAs, and
substantially heavier security/audit obligations. Keeping patients entirely out of scope in
V1 means a demo or early deployment can't leak PHI (there is none), dramatically shrinks the
attack surface, and lets us build and prove the security foundation before taking on
regulated health data. It's cheaper and safer to add PHI *later, deliberately* than to walk
it back after a leak. This is a scoping decision, enforced by input validation (below), not
an oversight.

### 4. Encrypted transport (HTTPS/TLS)
**What:** All traffic served over HTTPS; HTTP redirects to HTTPS; HSTS enabled.

**Why it matters:** Licenses, inspection documents, and login credentials travel between
browser and server. Without TLS, anyone on the network path (public Wi-Fi, a compromised
router, a corporate proxy) can read session cookies and documents in transit or tamper with
them. TLS gives confidentiality and integrity on the wire and is the baseline expectation for
any system holding confidential business documents. HSTS prevents downgrade attacks that try
to force plaintext.

### 5. Attachment / file-upload restrictions
**What:** Allow-list of file types (e.g. PDF, PNG, JPG), enforced size caps, content-type
verification (validate the real bytes, not just the extension), filename sanitization,
malware scanning where available, and storage outside the web root / served via authenticated,
non-executable paths.

**Why it matters:** File upload is one of the most-exploited features on the web. If a user
can upload an `.html`, `.svg`, or disguised executable and have it served back, that's stored
XSS or remote code execution. Oversized files enable denial-of-service. A PDF that's really a
script, or a filename like `../../etc/passwd`, is a path-traversal or injection vector.
Because this tool's whole point is holding uploaded licenses and inspection PDFs, the upload
path is a primary attack surface and must be locked down, not trusted.

### 6. Audit log for edits / status changes
**What:** An append-only record of who changed what, when, and (ideally) old→new values —
covering requirement edits, status changes, uploads, deletions, and permission changes.

**Why it matters:** This is a *compliance* tool — its output is used to make decisions
regulators may later scrutinize. "This state was marked Compliant on this date, by this
person, citing this source" must be reconstructable. An audit log:
- Provides accountability (ties every change to an identity)
- Enables incident investigation (what did a compromised account touch?)
- Is often itself a regulatory expectation for systems of record
- Deters careless or malicious edits because they're not anonymous

The log must be append-only and protected from the same users who generate it — an audit
trail an ordinary user can edit is not an audit trail.

### 7. Rate limiting on search / query endpoints
**What:** Per-user and per-IP request caps on expensive or abusable endpoints (search, and any
future server-side query/AI endpoint), with sensible burst + sustained limits and clear 429
responses.

**Why it matters:** Search endpoints are expensive (DB queries) and abusable. Without limits: a
single client can exhaust resources and deny service to everyone, and an attacker can brute-force
or scrape the entire dataset. Rate limiting keeps the system available and bounds both the resource
and data-exfiltration blast radius of a misbehaving or hostile client.

**Applies to the Ask box only if it is upgraded server-side.** The current "Ask (grounded)"
feature (see §11) runs entirely client-side with no endpoint and no LLM, so there is nothing to
rate-limit or run up cost against today. If it is ever upgraded to a server-side RAG proxy, this
control (and the secrets control in §9) becomes mandatory for that endpoint — a chat endpoint that
calls a paid API is a classic cost-exhaustion and scraping target.

### 8. Input validation
**What:** Validate and sanitize *all* input server-side — types, lengths, formats, allowed
values — using allow-lists over deny-lists. Parameterized queries for the database; output
encoding for anything rendered.

**Why it matters:** Unvalidated input is the root of the most damaging classes of bug:
SQL injection, cross-site scripting, and the kind of malformed data that corrupts a system
of record. It's also how the "no patient data in V1" rule is *enforced* rather than merely
hoped for — validation can reject fields that look like PHI. Server-side is non-negotiable:
client-side checks are a UX nicety an attacker simply skips.

### 9. Secrets in .env (never in code or the repo)
**What:** API keys, DB credentials, signing secrets, and tokens live in environment
variables / a secrets manager — loaded from `.env`, which is git-ignored. Only a
`.env.example` with placeholder keys is committed.

**Why it matters:** Secrets committed to a repo are one of the most common real-world
breaches — they leak via forks, clones, CI logs, and public mirrors, and they persist in git
history even after "deletion." Keeping secrets out of code means a leaked repo doesn't equal a
leaked database, secrets can be rotated without a code change, and each environment
(dev/staging/prod) can hold different values. **The demo uses only placeholder/dummy values —
no real credentials.**

### 10. Source history — never silently overwrite a requirement
**What:** Regulatory requirements are versioned. Editing a requirement creates a new version;
prior versions (with their source, citation, and timestamp) are retained and viewable.
Nothing is destructively overwritten.

**Why it matters:** This is the heart of the tool's integrity guarantee. A compliance decision
made last quarter was made against the rule *as it read then*. If someone silently overwrites
that requirement, you lose the ability to answer "what did we rely on, and was it correct at
the time?" — which is exactly what an audit or a dispute demands. Versioning also protects
against a bad edit (you can see and revert it), preserves the provenance chain the whole
dashboard is built on, and makes regulatory *change* visible over time rather than erasing it.
Combined with the audit log (who/when) and the provenance model (which source), source history
completes the "trustworthy record" promise.

### 11. Grounded "Ask" box — client-side retrieval, no key, no endpoint
**What:** The natural-language "Ask (grounded)" feature is **retrieval-only**: it runs entirely in
the browser, uses **no language model, no API key, and no server endpoint**. It maps a question to a
state + topic and returns the exact verified note + primary-source citation already in the page's
data, or an honest "needs legal review" for unsourced fields.

**Why it matters (security-positive by design):**
- **No secret to leak.** There is no API key in the client code, so there is nothing for a viewer
  to lift from DevTools on the public GitHub Pages build — the failure mode that ruled out the
  client-side-LLM option is structurally impossible here.
- **No abusable endpoint.** With no server call, there is no paid API to run up, no request to
  rate-limit, and no server-side injection surface reachable through the box.
- **Cannot fabricate.** It can only surface data already vetted under the provenance rule, so it
  cannot invent a citation or a compliance answer — consistent with the no-fabrication guarantee.

**If upgraded later (Option B RAG):** phrasing could be improved by sending the *retrieved records*
to an LLM behind a serverless proxy. In that design the key lives in the server environment (never
client-side, per §9) and the endpoint is rate-limited (per §7); the grounding still prevents
hallucination because the model is constrained to the retrieved records.

---

## Demo / non-production data rule

The demo and V1 contain **no PHI, no prescriptions, no patient names, and no real
credentials**. All example licenses, documents, and secrets are synthetic placeholders. This
keeps the demo safe to share, out of HIPAA scope, and impossible to turn into a real-world
data leak.

---

## How the controls reinforce each other

No single control is sufficient; they compose into defense in depth:

- **Authentication** establishes identity → **RBAC** limits what that identity can do →
  **audit log** records what it did → **source history** preserves what it changed.
- **Input validation** + **file restrictions** guard the write paths;
  **rate limiting** guards the read/compute paths.
- **TLS** protects data in transit; **secrets in .env** protect the keys to data at rest.
- **No patient data in V1** shrinks the stakes while the foundation is proven.

A gap in any one weakens the others — e.g. RBAC without an audit log means you can limit
damage but not investigate it; an audit log without source history tells you *that* a rule
changed but not *what it was before*.

---

## Out of scope for V1 (deliberate, revisit later)

- PHI / patient-facing data and the HIPAA controls that come with it
- SSO / SAML / SCIM enterprise identity (start with app-native auth)
- Field-level encryption at rest beyond disk/volume encryption
- Multi-tenant isolation (single-org V1)

These are noted so they're *chosen*, not forgotten — each can be added when the need is real.
