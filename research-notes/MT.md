# Montana — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 11 (+ 2 federal defaults) → 13 ver / 7 rev.

## STRUCTURAL CATCH
***The old standalone telemedicine statutes MCA §§37-3-342 through 37-3-349 are all REPEALED.*** Telehealth is now the single consolidated practice-standards statute **§37-2-305** ("Telehealth services — rulemaking authority"; Title 37 ch. 2 General Provisions Relating to Health Care Practitioners), plus board rulemaking. Practice-standards title (telehealth coverage/parity is Title 33 Insurance, separate). Pharmacy = MCA Title 37 ch. 7 + ARM Title 24.174. MPDR = MCA §37-7-1501 et seq.

## SOURCING
- Statutes: **mca.legmt.gov** (the current MCA host; leg.mt.gov/bills/mca now redirects here). Deep-link `/bills/mca/title_0370/chapter_0020/part_0030/section_0050/0370-0020-0030-0050.html`. Body renders in DOM → innerText. Clean.
- ARM rules: **rules.mt.gov** rule bodies are an **Esper SPA PDF viewer that did NOT render extractable text headless this session**. Workaround used: the rules.mt.gov full-text SEARCH INDEX quotes the operative rule language + gives the definitive deep-link policy URL. Pharmacy rule fields (PIC, compounding) are therefore cited chapter-level, honestly flagged. FOLLOW-UP: open each rule's "View in PDF" download to pin subsection quotes.

## VERIFIED (statute read verbatim on mca.legmt.gov)
- **provider.fullLicense** — §37-2-305(1) ("a person licensed under this title") + §37-3-301(1) (no medicine without MT license).
- **modality.video + audioOnly** — §37-2-305(3)(a): "the use of audio, video, or other telecommunications technology or media, including audio-only communication." Audio-only PERMITTED (narrow carve-out §37-2-305(3)(c): audio-only barred for medical-marijuana debilitating-condition certifications absent a prior in-person relationship).
- **relationship.inPerson** — §37-2-305(1): telehealth OK when "appropriate ... and meets the standard of care"; no general prior-in-person prerequisite.
- **prescribing.pdmp — TARGETED MANDATORY** — §37-7-1515: "A prescriber or an agent of the prescriber shall review a patient's records under the prescription drug registry before the prescriber issues a prescription for an opioid or a benzodiazepine" (verb verified). Six exceptions (hospice, ≤7-day non-refillable, in-facility administration, emergency, chronic-pain reviewed q3mo, registry down). Contrast §37-7-1503 (registration/reporting) which is NOT a query mandate.
- **pharmacy.nonresident** — §37-7-703(1): "Each out-of-state mail order pharmacy must be registered." Amended Ch. 726, L. 2025.
- **pharmacy.pic** — ARM 24.174.805 (change-of-PIC rule presupposes/regulates a PIC per licensed pharmacy). Chapter-level.
- **compounding.stateReg** — ARM 24.174.841 "Sterile Products": directs compliance with "USP Chapter 795 ... and USP Chapter 797." USP 795/797 by number; USP 800 NOT confirmed by number. Chapter-level (index-verified).
- **ecommerce.onlinePharmacy** — subsumed in §37-7-703 (no separate internet-pharmacy permit).

## LEFT "NEEDS LEGAL REVIEW"
- **provider.telehealthReg** — no separate out-of-state telehealth registration; full MT license only.
- **modality.async** — §37-2-305(3)(b) EXCLUDES health-care delivery "by means of facsimile machines or electronic messaging alone." Pure store-and-forward/async by itself is NOT a recognized standalone modality (async only counts in conjunction with other qualifying tech) → left red.
- **relationship.consent** — §37-2-305 has no telehealth-specific "shall obtain consent"; delegated to board rule under §37-2-305(2). No statutory mandate located.
- **prescribing.inPersonRx** — no state CS-before-telehealth in-person mandate; DEA controls.
- **pharmacy.csDispense** — ARM 24.174.14xx "Dangerous Drug Act" subchapter + MCA Title 50 ch. 32 (chapter-level; exact section not isolated behind the SPA viewer).
- **ecommerce.website** — no VIPPS/website-display mandate.
- **ecommerce.dtc** — no express online-questionnaire ban located; MT relies on the §37-2-305 general standard-of-care test → left red rather than infer.

## FOLLOW-UP
- Open ARM 24.174.841, 24.174.805, and 24.174.14xx "View in PDF" downloads to pin subsection-level quotes (would harden PIC/compounding/csDispense from chapter-level). Watch MAR Notice 2025-206 (eff. 12/6/25) amending pharmacy rules.
