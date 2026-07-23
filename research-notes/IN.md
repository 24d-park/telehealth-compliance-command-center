# Research Note — Indiana (IN) — PARTIAL (5 state-specific fields verified 2026-07-22)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date attempted:** 2026-07-20
- **Verified fields:** 5 state-specific / 20 (9 incl. federal defaults)  ·  Status: **PARTIAL** — telehealth core (IC 25-1-9.5 §§7-10) sourced 2026-07-22; pharmacy/PDMP/compounding still open. See "UNBLOCKED (partial)" section below.

## Why Indiana is blocked in this environment

Indiana's official primary-source host, **iga.in.gov** (Indiana Code + Indiana Administrative Code), could
NOT be read this session by either the subagent or the parent verification pass:

1. **iga.in.gov is a JavaScript single-page app (SPA)** that does not hydrate in this browser/proxy stack —
   every statute page renders as an empty shell. Asset paths (main.js, CSS) return the 691-byte index.html
   fallback, and the guessed per-chapter PDF paths (`/pdf-documents/...`) also return the SPA HTML, not a PDF.
2. **api.iga.in.gov** (the backing JSON API) returns `403 "x-api-key not found"` — it requires a free
   registered API key (docs.api.iga.in.gov) that could not be obtained autonomously.
3. **Internet Archive (Wayback)** has 2022-era server-rendered captures for a *sparse* set of Title 25
   chapters, but **the core telehealth chapter IC 25-1-9.5 (Article 1, Chapter 9.5) is NOT archived** —
   Article 1 chapter captures return 404. Confirmed via the Wayback CDX URL-prefix index (no captures).

## What would unblock Indiana (recommended next steps)

1. **Register a free IGA API key** at docs.api.iga.in.gov and fetch structured statute JSON, e.g.
   `https://api.iga.in.gov/2025/code/titles/25/articles/1/chapters/9.5` with the `x-api-key` header.
2. Use a **curl/HTTP-capable environment** (this session's browser could not execute the SPA and had no
   curl) to pull the IGA statute PDFs or API directly.
3. A **browser stack that fully executes JavaScript with a residential proxy** would render iga.in.gov
   statute pages directly (the tool warned it was running without residential proxies).

## Target sections to research once a working path exists

- Telehealth: IC 25-1-9.5 (practice), IC 25-1-9.5-6 (modality), IC 25-1-9.5-8 (CS/opioid prescribing limits)
- Out-of-state telehealth: IC 25-1-9.5 (certification for out-of-state providers)
- PDMP (INSPECT): IC 25-1-9.6 / IC 35-48-7
- Nonresident pharmacy: IC 25-26-17; PIC: IC 25-26-13
- Compounding: 856 IAC 3

**No fabricated citations were entered for Indiana.** Every field is left at its unsourced seed until a
primary source can actually be read.

## Re-attempt 2026-07-21 (confirmed still blocked)

A second dispatch + parent verification pass this session re-confirmed the block with no change:
- iga.in.gov still returns only the un-hydrated React SPA shell on every route — app pages, `/api/`, `/static/` assets, AND `/pdf-documents/...` enrolled-act PDFs.
- Wayback `id_` raw captures of the modern IC pages return the same ~3 KB SPA stub; CDX enumeration found only landing-page shells. Legacy `in.gov/legislative/ic/...` captures are all 2001–2007 (predating IC 25-1-9.5, enacted 2021).
- The HB1514-2021 enrolled-act PDF also returns the shell via both live and Wayback; no `in.gov/pla` PLA statute PDFs are archived.

Per the honesty standard, NO Indiana fields were written this session either. The 4 "verified" fields in the tracker are federal-default layers (DEA/Ryan Haight), not IN-specific sourcing. Indiana remains the ONE jurisdiction of 51 not researched. Unblock requires a JS-rendering (non-headless-detected) browser, a registered IGA API key (docs.api.iga.in.gov), or a residential-proxy/curl fetch. This is the documented follow-up item.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UNBLOCKED (partial) — 2026-07-22

Indiana moved from **0 -> 5 state-specific verified fields** (9/20 sourced incl. federal defaults). The breakthrough was NOT iga.in.gov (still a dead JS SPA — the `/static/js/main.*.js` bundle itself 404s to the 691-byte SPA shell, so React can never hydrate; re-confirmed a 3rd time). Instead: the **official 2024 Indiana Code is reproduced on Justia**, and although Justia is Cloudflare-walled live, its static statute pages ARE archived — read **verbatim via Internet Archive `id_` raw captures** (`https://web.archive.org/web/<ts>id_/https://law.justia.com/codes/indiana/title-25/article-1/chapter-9-5/section-25-1-9-5-N/`). Same honest-mirror method used for TN/OK/NM/HI/NH.

### Verified from IC 25-1-9.5 (Telehealth Services and Prescriptions)
- **section 7** (Standards; provider-patient relationship; consent; records) -> `relationship.inPerson` (same standard of care as in-person; NO general prior-in-person mandate), `relationship.consent` (7(b)(3) informed consent + 7(b)(6) medical record MANDATORY). [src: in_tele_7]
- **section 8** (Issuance of Rx; controlled-substance conditions) -> `prescribing.inPersonRx` (Rx via telehealth w/o prior in-person if scope/standard met; CS only per 8(b) w/ IC 35-48-3 registration + 21 USC 829/Ryan Haight). **CRITICAL 8(a)(3)(B): NO opioid via telehealth EXCEPT a partial agonist for opioid dependence (e.g. buprenorphine); 8(a)(4) no abortion-inducing drug.** [src: in_tele_8]
- **section 9** (Practitioner outside Indiana; jurisdiction) -> `provider.telehealthReg` + `pharmacy.nonresident` (out-of-state practitioner must file WRITTEN certification to the Indiana Professional Licensing Agency submitting to IN jurisdiction/law before treating IN patients; 10(b): failure to file = Class B infraction per act). [src: in_tele_9]

Enactment: all sections added P.L.78-2016 SEC.2, amended through P.L.109-2022 (sec 7) / P.L.85-2021 (sec 8, 9).

### Still open (honest gaps, 11 fields)
- `provider.fullLicense`; `modality.video/audioOnly/async` — **section 6 "Telehealth" definition section is NOT individually archived on Justia** (chapter index confirms it exists; only sections 7-10 have section-level captures).
- `prescribing.pdmp` — INSPECT (IC 25-1-9.6 / IC 35-48-7), not read.
- `pharmacy.pic` (IC 25-26-13), full pharmacy nonresident PERMIT (IC 25-26-17) — **IC 25-26 is not reproduced on Justia**; section 9 covers only the out-of-state PROVIDER pathway, not the dispensing-pharmacy permit.
- `compounding.stateReg` (856 IAC); `ecommerce.website/dtc/onlinePharmacy`.

### To close the remaining fields
1. **Register a free IGA API key** at docs.api.iga.in.gov -> fetch structured statute JSON for IC 25-26 + the section 6 definition directly.
2. Or find archived captures of IC 25-26 (pharmacy) + 856 IAC (Board of Pharmacy rules) on an un-walled mirror.


---

## Update 2026-07-23 — laggard push (9 -> 10 verified)

**provider.fullLicense wired** — Ind. Code 25-22.5-3-1(a) read verbatim via Internet Archive id_ capture of the FindLaw/Westlaw reproduction: "The minimum requirements for all applicants for an unlimited license to practice medicine or osteopathic medicine in Indiana must include but are not limited to the requirements prescribed by this section." Supported by 25-22.5-1-1.1(a)(4) (services "transmitted through electronic communications" on a regular basis are within the practice of medicine). Capture: https://web.archive.org/web/20180313060437id_/http://codes.findlaw.com/in/title-25-professions-and-occupations/in-code-sect-25-22-5-3-1.html — src in_med_lic. CAVEAT: 2018 capture; the "unlimited license" verb is long-standing but the note flags re-verifying current consolidated text.

**Re-confirmed still blocked (10 reds remain):** iga.in.gov is still a dead JS SPA. A fresh subagent pass checked Justia, FindLaw AND Casetext via Wayback CDX + id_ captures and confirmed the coverage gap is real, not a technique failure:
- IC 25-1-9.5-**6** (Telehealth DEFINITION — needed for modality.video/audioOnly/async) is NOT captured on Justia (only 7-10 are), nor on FindLaw/Casetext.
- IC 25-1-9.6 / IC 35-48-7 (INSPECT PDMP) — zero captures anywhere.
- IC 25-26-13 (PIC), 25-26-17 (nonresident pharmacy), 25-26-18 (mail-order/internet pharmacy) — Article-26 index confirms these chapters EXIST but no section pages are archived on any host.
- 856 IAC (compounding/USP) — only 6 stray pages archived, none on compounding.

**The only clean unblock left: register a free api.iga.in.gov x-api-key** (docs.api.iga.in.gov) and fetch structured statute JSON for IC 25-1-9.5-6, 25-1-9.6, 25-26-13/17/18, and Title 35 ch. 7. The archived-mirror path is exhausted for Indiana.
