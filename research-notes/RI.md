# Rhode Island — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 11 (+ 2 federal defaults) → 15 ver / 5 rev.

## TITLE DISCIPLINE (the RI trap)
***RIGL Title 27 ch. 81 ("Telemedicine Coverage Act") is an INSURANCE title — do NOT source practice standards from it.*** The telehealth PRACTICE standards live in the RICR rule **216-RICR-40-05-1** "Licensure and Discipline of Physicians" (Dept of Health / Board of Medical Licensure & Discipline), eff. 4/24/2022. (Caveat: the rule §1.2(A)(25) borrows the "Telemedicine" DEFINITION from RIGL §27-81-3 by cross-reference — the def originates in the insurance title but is operative for practice via the DOH rule.) Pharmacy = RIGL Title 5 ch. 5-19.1 + rule 216-RICR-40-15-1. PDMP = RIGL Title 21 ch. 21-28.

## SOURCING TECHNIQUE
RICR rules are served ONLY as PDFs inside a JS viewer. **Read via pdf.js against the official RI SOS S3 PDFs** (navigate directly to `risos-apa-production-public.s3.amazonaws.com/DOH/REG_NNNNN...pdf` so the fetch is same-origin — a file:// origin gets CORS-blocked). REG_12738 = telemedicine rule (28pp); REG_13410 = pharmacy rule (128pp). The S3 PDF URLs are linked from each rules.sos.ri.gov/regulations/Part/... page.

## VERIFIED
- **provider.fullLicense** — RIGL §5-37-2 (RI medical license issued by Director of Health; out-of-state needs RI license, only narrow §5-37-16.2 exceptions).
- **modality.video + audioOnly** — 216-RICR-40-05-1 §1.2(A)(25): "real time, two (2) way synchronous audio, video, telephone-audio-only communications or ... store-and-forward." Audio-only expressly named → PERMITTED.
- **modality.async** — recognized in the def (store-and-forward) BUT §1.5.9(H)(2): "Asynchronous evaluation ... without contemporaneous real-time, interactive exchange ... is not appropriate." Recognized-but-restricted.
- **relationship.inPerson** — §1.5.9(H)(2): same standards as face-to-face; no prior in-person exam required.
- **prescribing.pdmp — TARGETED MANDATORY** — RIGL §21-28-3.32(m): "The prescription-monitoring program shall be reviewed prior to starting any opioid" + at-least-q3mo review for continuous opioid therapy ≥3 months. ***IMPORTANT: the subagent wrongly called this VOLUNTARY — it saw only the stale "[Effective until January 1, 2023]" header block and missed subsection (m). Always scroll the FULL statute page on RI (multiple effective-date versions are stacked on one page).***
- **pharmacy.nonresident** — RIGL §5-19.1-11(a): out-of-state pharmacy that ships into RI "shall be licensed by the department."
- **pharmacy.pic** — 216-RICR-40-15-1: PIC = pharmacist "personally in full and actual charge of such pharmacy and personnel."
- **compounding.stateReg** — 216-RICR-40-15-1 §1.2: incorporates USP 795 (2023), 797 (2023), 800 (2020) BY NUMBER and FIXED edition ("not including any further editions or amendments"); also 659 (2021), 825 (2024).
- **ecommerce.dtc** — §1.5.9(H)(2): "treatment, including issuing a prescription, based solely on an online questionnaire without an appropriate evaluation does not constitute an acceptable standard of care."
- **ecommerce.onlinePharmacy** — subsumed in the §5-19.1-11 nonresident license (no separate internet-pharmacy category).

## LEFT "NEEDS LEGAL REVIEW"
- **provider.telehealthReg** — no separate pathway; §5-37-16.2 has narrow licensure EXCEPTIONS (federal/military, air-ambulance, ≤7-day consult) only.
- **relationship.consent** — NO telehealth consent mandate in the practice rule 216-RICR-40-05-1; a consent/notice duty exists only in the INSURANCE title RIGL 27-81, so left red for a practice-standards consent mandate.
- **prescribing.inPersonRx** — no state CS in-person mandate; DEA controls.
- **pharmacy.csDispense** — RIGL §21-28-3.18 general Rx content/recordkeeping (not isolated to a single verb).
- **ecommerce.website** — physical in-pharmacy posting required, but no website/VIPPS display mandate.

## FOLLOW-UP
- Confirm the current (post-Jan-2023) §21-28-3.32 successor version if the legislature renumbered it; the mandatory-review verb (m) should carry forward.
