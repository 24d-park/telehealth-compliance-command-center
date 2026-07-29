# Maine — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 12 (+ 2 federal defaults) → 16 ver / 4 rev.

## STRUCTURAL KEY (source selection matters)
- **Telehealth PRACTICE STANDARDS = 02-373 CMR Ch. 11** "Joint Rule Regarding Telehealth Standards of Practice" (Board of Licensure in Medicine + Osteopathic 02-383 + Nursing 02-380). Originally Ch. 6 (eff. Dec 10 2016), **renumbered Ch. 11, amended 7/24/2022.** Statutory authority 32 M.R.S. §3269.
- ***DO NOT use 24-A §4316 for practice standards*** — that is the INSURANCE-coverage law and only supplies a cross-referenced definition.

## SOURCING TECHNIQUE (reusable)
The Board rule is published only as a **.docx** at maine.gov/sos/sites/.../inline-files/373c011%20-%20JUL%202025.docx (the old `/sos/cec/rules/` URL scheme is dead). Navigating to it triggers a download, not a render. **Extraction that worked:** in browser console, `fetch()` the .docx → it's a ZIP (PK\x03\x04) → scan local file headers for `word/document.xml` → inflate with `new DecompressionStream('deflate-raw')` → strip XML tags → full rule text (~25k chars). Store to `window.__X` and regex it. This is the go-to for any Maine Board .docx rule.

## VERIFIED
### Telehealth rule 02-373 CMR Ch. 11 (read verbatim from document.xml)
- **provider.fullLicense** — §3(2)(A) "Physicians, physician assistants and advanced practice registered nurses who use telehealth ... of a patient located in Maine shall hold an active Maine license or shall hold an active registration in Maine to provide interstate consultative telemedicine services."
- **modality.video** — §2(11) "Synchronous encounter" = real-time interactive audio OR video.
- **modality.audioOnly** — §2(12) "telehealth includes the use of audio-only technology" (when appropriate + standard of care). PERMITTED.
- **modality.async** — §2(1) "Asynchronous encounter" + §2(10) "Store and forward transfer."
- **relationship.inPerson** — relationship begins "whether or not there has been an in-person encounter"; telehealth OK "if the standard of care does not require an in-person encounter."
- **relationship.consent** — §10 MANDATORY: "A licensee who uses telehealth ... shall ensure that the patient provides appropriate informed consent ... and that such informed consent is timely documented in the patient's telehealth record."
- **ecommerce.dtc** — §21: prescribing based solely on a "static questionnaire ... (in contrast to an adaptive, interactive and responsive online interview) is prohibited."

### Statutes (legislature.maine.gov)
- **provider.telehealthReg** — 32 M.R.S. §3300-D: "The board may register a physician to practice medicine in this State through interstate telehealth" — CONSULTATIVE services only, biennial. Amended PL 2021 c.293.
- **prescribing.pdmp — MANDATORY (verified verb)** — 22 M.R.S. §7253(1): "upon initial prescription of a benzodiazepine or an opioid medication ... and every 90 days ... a prescriber shall check prescription monitoring information." (Corrects the task hint §7248, which only establishes the program.)
- **pharmacy.nonresident / ecommerce.onlinePharmacy** — 32 M.R.S. §13751 license classification "B. Mail order prescription pharmacy" (amended PL 2025 c.136) + 02-392 CMR Ch. 11 mail-order registration.
- **compounding.stateReg** — 02-392 CMR incorporates USP <795>/<797> BY NUMBER by reference, but pinned to the OLDER **USP 36-NF 31 (2013-14)** edition; <800> not found. (Subagent read of the pharmacy CMR; chapter-level — flagged as fixing an old edition.)

## LEFT "NEEDS LEGAL REVIEW"
- **prescribing.inPersonRx** — no separate ME CS-before-telehealth in-person statute; §7 + §21 leave prescribing to professional discretion + standard of care; DEA federal rules apply.
- **pharmacy.pic + pharmacy.csDispense** — "pharmacist in charge" is a defined, operative role throughout 02-392 CMR (Ch. 13/19/22/23) but the exact PIC-designation subsection + granular CS-dispensing verbs were not isolated (subagent hit iteration cap). Chapter-level only → left red rather than assert a section-level verb.
- **ecommerce.website** — mail-order registration requires disclosing the web address TO THE BOARD (02-392 CMR Ch. 11), but that is not a public-display mandate.

## FOLLOW-UP
- Pin the 02-392 CMR PIC-designation subsection + CS-dispensing sections (unzip the pharmacy .docx the same way) to convert pharmacy.pic/csDispense from red to green.


## UPDATE 2026-07-29 — final-research wave 4, +3 fields (16 -> 19/20)
Subagent lead, parent-verified: telehealth statute subchapter confirmed on legislature.maine.gov (Title 32
Ch. 48 Subch. 4 TELEHEALTH SERVICES, §3300-AA); Board rules read via the official ME SOS .docx.
- **prescribing.inPersonRx** — 02-373 CMR Ch. 11 §3(7): in-person clinical interview + physical exam is the
  general rule but "may not be in-person if the technology utilized ... is sufficient to establish an informed
  diagnosis as though [it] had been performed in-person." No absolute mandate; static questionnaire insufficient.
  Reused me_teterule.
- **pharmacy.csDispense** — 02-392 CMR Ch. 19 §2: Sch II written Rx must comply w/ MDEA "Requirements for
  Written Prescriptions of Schedule II Drugs" (incorporated); no CS pre-printing; 90-day fill limit; e-CS per
  21 CFR 1300/1304/1306. New source me_392.
- **pharmacy.pic** — 02-392 CMR Ch. 13 §3(1): "No retail pharmacy may operate without a pharmacist in charge."
  New source me_392.
### Confirmed HOLD
- ecommerce.website — no on-website disclosure mandate in the Board rules (full Ch. 1-38 searched). Genuine
  absence. Numbering corrections logged: telehealth rule is Ch. 11 (orig. Ch. 6); PIC is Ch. 13 (not Ch. 18/19,
  Ch. 18 repealed); §3300-G is conversion-therapy, NOT telehealth (that's §§3300-AA..EE).
