# Oklahoma — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 12 (+ 2 federal defaults) → 13 ver / 7 rev. (4 OAC rule-level fields gapped.)

## SOURCING TECHNIQUE
***oscn.net (the courts' statute host) is Cloudflare-Turnstile blocked live.*** Recovered statute text via Internet Archive `id_` raw captures of the official OSCN pages: `web.archive.org/web/YYYYid_/https://www.oscn.net/applications/oscn/DeliverDocument.asp?CiteID=NNNNNN`. Section→CiteID mapping came from archived 2022/2023 OSCN Title 59 + Title 63 indexes. ***OAC Title 435 (Medical Board) + Title 535 (Board of Pharmacy) admin rules could NOT be reached*** — rules.ok.gov is a JS SPA with negligible archive; sos.ok.gov eDMS OAC PDFs not located. FOLLOW-UP: okmedicalboard.org has archived rules PDFs (OAC 435:10 telemedicine) that DO load via Wayback — a dedicated rules pass would close the 4 gaps (audio-only, consent, compounding-USP, DTC).

## STRUCTURAL KEY
Telehealth practice standard = **59 O.S. §478.1** (Board of Medical Licensure & Supervision; NOT repealed, amended HB 2686 emerg. eff. 5/15/2023), Title 59 (Professions) — not insurance. Pharmacy = **59 O.S. §353 et seq.** (Pharmacy Act). PMP = **63 O.S. §2-309D** (Anti-Drug Diversion Act, OSBNDD).

## VERIFIED (statute read verbatim via Internet Archive)
- **provider.fullLicense** — §478.1(A)(1): relationship via telemedicine requires the physician "Holds a license to practice medicine in this state."
- **modality.video** — §478.1(A)(2)-(3): modality-neutral encounter requirements (identity/location confirmation, credentials).
- **modality.async** — §478.1(D): "A physician-patient relationship shall not be created solely based on the receipt of patient health information" (store-and-forward recognized but insufficient alone).
- **relationship.inPerson** — §478.1(A): relationship "may be established ... through telemedicine" (no prior in-person).
- **prescribing.inPersonRx** — §478.1(C): telemedicine "shall not be used to establish a valid physician-patient relationship for the purpose of prescribing opiates, synthetic opiates, semisynthetic opiates, benzodiazepine or carisoprodol," except opioid antagonists/partial agonists (63 O.S. 1-2506.1/.2) or Sch III/IV/V FDA-approved MAT/detox. A genuine CS-via-telehealth restriction.
- **prescribing.pdmp — TARGETED MANDATORY** — 63 O.S. §2-309D(G)(2)(a): "Prior to prescribing or authorizing for refill, if one hundred eighty (180) days have elapsed prior to the previous access and check, of opiates ... benzodiazepine or carisoprodol to a patient of record, registrants ... shall be required to access the information in the central repository." ***Verb verified. Threshold is 180 days since last check — NOT a "3-day supply" threshold.*** Hospice/nursing-facility exceptions. Amended SB 1151 (2022).
- **pharmacy.nonresident** — §353.18(A)(1): license required whether the sale "occurs in this state, or ... out of state and the [drug] is to be delivered ... to patients or customers in this state" + §353.18(A)(3)(b) "Non-resident pharmacies."
- **pharmacy.pic** — §353.18(A)(2)(c): "under the management and control of a licensed pharmacist or pharmacist-in-charge who shall be licensed as a pharmacist in Oklahoma"; PIC def §353.1(33).
- **ecommerce.onlinePharmacy** — §353.18(A)(1): expressly "including, but not limited to, Internet, website or online pharmacies" must procure a Board license. Explicit hook.

## LEFT "NEEDS LEGAL REVIEW"
- **provider.telehealthReg** — no separate pathway; full in-state licensure.
- **modality.audioOnly** — §478.1 modality-neutral, doesn't distinguish audio-only; any limit would be in OAC 435 ch. 10 (unread).
- **relationship.consent** — §478.1(B) requires HIPAA-compliant secure comms but no consent verb; likely in OAC 435 (unread).
- **pharmacy.csDispense** — 63 O.S. ch. 2 art. 3 + §2-309 e-prescribe mandate + OAC 535 (chapter-level).
- **compounding.stateReg** — OAC 535 (unread); statutory hook only = §353.18(A)(4) sterile-compounding permit "by rule."
- **ecommerce.website** — not located.
- **ecommerce.dtc** — no express online-questionnaire ban in statute; likely OAC 435 (unread).

## FOLLOW-UP
- Dedicated OAC pass via okmedicalboard.org archived rule PDFs (OAC 435:10 telemedicine — audio-only/consent/DTC) + Board of Pharmacy OAC 535 (compounding USP-by-number, CS dispensing).


---

## Update 2026-07-23 (wave 4) — +3 (13 -> 16 verified)

Read via Wayback id_ of the OK Allopathic Board MDRULES PDF (`https://web.archive.org/web/20220121201000id_/https://www.okmedicalboard.org/download/457/MDRULES_08.2021.pdf`) + pdf.js. oscn.net/rules.ok.gov Turnstile-blocked. All parent-verified verbatim.

- **provider.telehealthReg** — OAC 435:10-7-13(a): "Physicians treating patients in Oklahoma through telemedicine must be fully licensed to practice medicine in Oklahoma." Exclusive licensure, no separate registration. VERIFIED-NULL. Eff. 9-12-14. [ok_mdrules]
- **modality.audioOnly — EXCLUDED** — the telemedicine definition "is not a consultation provided by telephone or facsimile machine ... This definition excludes phone or Internet contact"; (b)(3)(A): "Audio and video equipment must permit interactive, real-time communications." Real-time audio AND video required. [ok_mdrules]
- **relationship.consent** — OAC 435:10-7-13(b)(1): a telemedicine encounter must include "the documentation of a history, a physical exam, the ordering of any diagnostic tests, making a diagnosis and initiating a treatment plan with appropriate discussion and informed consent." [ok_mdrules]

Still red (honest holds):
- **compounding.stateReg** — OK Board of Pharmacy 2022 law-book: USP <797> adopted by number for STERILE (OAC 535:15-10-54), but "795" returns NO match — non-sterile compounding rules are self-contained, not a 795-by-number adoption. Held rather than green a partial. A newer 2023 red-marked Chapter 15 PDF may differ (not parsed).
- **pharmacy.csDispense** — operative "shall ... legitimate medical purpose"/"shall not dispense ... without a valid preexisting relationship" language found in the concatenated law-book, but a clean standalone OAC 535 section cite couldn't be pinned. Held.
- **ecommerce.website** — no on-website disclosure mandate (verified-absent). **ecommerce.dtc** — no standalone "online questionnaire" ban; the prohibition is achieved indirectly via the real-time-equipment/face-to-face requirement. Red.
