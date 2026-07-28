# District of Columbia — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 12 (+ 2 federal defaults) → 14 ver / 6 rev.

## STRUCTURAL KEY
Telehealth practice standard = **17 DCMR §4618** (DC Board of Medicine, eff. 12/22/2017, confirmed NOT repealed). Licensing statute = DC Code Title 3 ch. 12 (Health Occupations). Pharmacy = **22-B DCMR ch. 19** (Board of Pharmacy). PDMP = **DC Code §48-853.03c** (Title 48 ch. 8G). Controlled substances = DC Code Title 48 ch. 9. All practice-standards — NOT the DC insurance/Medicaid telehealth titles (audio-only lives only there).

## SOURCING TECHNIQUE
- DC Code (code.dccouncil.gov) is clean HTML with true per-section deep-links.
- ***DCMR sections are served as .doc downloads*** with no per-section permalink — fetch the .doc and extract text in-browser; cite the chapter RuleList page (dcregs.dc.gov/Common/DCMR/RuleList.aspx?ChapterNum=17-46 / 22-B19) with the section number.

## VERIFIED
- **provider.fullLicense** — 17 DCMR §4618.1: "In order to practice telemedicine for a patient located within the District of Columbia, a license to practice medicine in the District of Columbia is required."
- **modality.video** — §4618.4: physician "may use real-time telemedicine" to establish the relationship + evaluate.
- **relationship.inPerson** — §4618.4: no prior in-person interaction required; real-time telemedicine may establish the relationship.
- **relationship.consent** — §4618.2(a) MANDATORY: standard of care includes "Obtaining and documenting patient consent, except when providing interpretive services."
- **prescribing.inPersonRx** — §4618.3: "A physician shall perform a patient evaluation ... before providing treatment or prescribing medication." No separate CS in-person mandate (DEA governs).
- **prescribing.pdmp — TARGETED MANDATORY** — DC Code §48-853.03c(a)(1): "shall query the ... database before initiating a new course of treatment ... that includes prescribing an opioid or benzodiazepine for more than 7 consecutive days, and every 90 days thereafter." 5 exceptions in (c). Added D.C. Law 23-251 (2021).
- **pharmacy.nonresident** — 22-B DCMR §1903: nonresident pharmacies shipping into DC "shall ... be registered by the Department" (Certificate of Registration before shipping; biennial). Eff. 4/1/2022.
- **pharmacy.pic** — §1920: pharmacy "shall be managed by a pharmacist" (PIC), one pharmacy at a time.
- **compounding.stateReg** — §1907: non-sterile per "current published edition of USP General Chapter 795, 800"; sterile per "USP General Chapter 797, 800." USP 795/797/800 BY NUMBER (+ rolling "current edition"). Eff. 4/1/2022.
- **ecommerce.onlinePharmacy** — §1903: no distinct internet-pharmacy permit; online/mail-order captured by the nonresident registration.

## LEFT "NEEDS LEGAL REVIEW"
- **provider.telehealthReg** — no telehealth registry; the only cross-border route is the *adjoining-state* in-person exemption (DC Code §3-1205.02(a)(4), amended 7/19/2024 D.C. Law 25-191) — not a telehealth registration.
- **modality.audioOnly + modality.async** — 17 DCMR §4618 authorizes only "real-time"; audio-only appears solely in DC insurance/Medicaid titles (excluded); async recognized only as narrow "interpretive services" (§4618.5), not a general modality.
- **pharmacy.csDispense** — DC Code §48-903.01 et seq. + 22-B DCMR §1910 (chapter-level).
- **ecommerce.website** — physical in-pharmacy posting only (§1901.3), no website mandate.
- **ecommerce.dtc** — no standalone online-questionnaire ban; the §4618.3 evaluation requirement functionally precludes questionnaire-only prescribing but isn't an explicit DTC rule.


---

## Update 2026-07-28 — low-coverage push (14 -> 16/20), parent-verified

- **provider.telehealthReg WIRED (verified-null)** — D.C. Code § 3-1205.01(a)(1) ("A license issued pursuant to this chapter is required to practice ... medicine ... pharmacy ... in the District, except as otherwise provided") + 17 DCMR § 4618.1 (DC license required for telemedicine). Only cross-border route is the adjoining-state in-person exemption § 3-1205.02(a)(4), NOT a telehealth credential. No separate DC telehealth registry. [new src dc_hora_120501]
- **pharmacy.csDispense WIRED** — D.C. Code § 48-903.08: Schedule II written-Rx + no refill; III/IV 6-month/5-refill limit. Enacted Aug. 5, 1981, D.C. Law 4-29. [new src dc_48_903_08]

### Still red (4) — genuine absences (17 DCMR §§ 4618/4612 read in full)
- modality.audioOnly + modality.async — § 4618 authorizes only real-time; async only as narrow "interpretive services" (store-and-forward imaging). Audio-only appears only in DC insurance/Medicaid titles (excluded).
- ecommerce.website — no on-website display mandate in the medicine chapter.
- ecommerce.dtc — general § 4618.3 evaluation-before-prescribing duty but NO explicit online-questionnaire ban.

SOURCING: DC Code = clean HTML deep-links (code.dccouncil.gov); DCMR = binary .doc downloads fetched same-origin via the RuleList page. All parent-verified verbatim.
