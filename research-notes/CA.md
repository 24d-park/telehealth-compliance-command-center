# Research Note — California (CA)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-16
- **Verified fields:** 10 / 20  ·  **Needs legal review:** 10 / 20
- **Method:** Primary sources only, read directly in-browser (statute/rule text confirmed verbatim). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; every link deep-links to the specific document)

- **Interstate Medical Licensure Compact Commission — Participating States / Compact State Map**
  - https://imlcc.com/participating-states/
  - _Compact State Map checked 2026-07-16 (46 member jurisdictions; AK joined 2026-06-22). .org domain is no longer official (casino-spam); .com is official._
- **California B&P Code §2290.5(b) — telehealth consent**
  - https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?sectionNum=2290.5.&lawCode=BPC
  - _Statute text read 2026-07-15_
- **DEA — Diversion Control Division (Telemedicine)**
  - https://www.deadiversion.usdoj.gov/Telemedicine.html
  - _Checked 2026-07-15 (DEA drafting updated telemedicine rules)_
- **California Health & Safety Code §11165.4(a) — CURES/PDMP**
  - https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?sectionNum=11165.4.&lawCode=HSC
  - _Statute text read 2026-07-15_
- **California B&P Code §4112(b) — nonresident pharmacy**
  - https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?sectionNum=4112.&lawCode=BPC
  - _Statute text read 2026-07-15 (Amended Stats. 2025, Ch. 196)_
- **U.S. Pharmacopeia — Compounding Standards (USP 795/797)**
  - https://www.usp.org/compounding
  - _Checked 2026-07-15 (federal framework; confirm state adoption)_
- **U.S. FDA — Human Drug Compounding (503A/503B)**
  - https://www.fda.gov/drugs/guidance-compliance-regulatory-information/human-drug-compounding
  - _FDA content current 2026-06-15 (checked 2026-07-15; confirm state overlay)_
- **California B&P Code §4127 — sterile compounding pharmacy license**
  - https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=BPC&sectionNum=4127.
  - _Statute text read 2026-07-16; Amended Stats. 2016, Ch. 484 (SB 1193), eff. 2017-01-01_
- **California B&P Code §4067 — internet dispensing of dangerous drugs**
  - https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=BPC&sectionNum=4067.
  - _Statute text read 2026-07-16; Amended Stats. 2025, Ch. 196 (AB 1503), eff. 2026-01-01_
- **California B&P Code §2242.1 — no internet prescribing without prior exam (Medical Board of CA)**
  - https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=BPC&sectionNum=2242.1.
  - _Statute text read 2026-07-16; Amended Stats. 2015, Ch. 719 (SB 643), eff. 2016-01-01_

## Verified requirements — exact citations

| Field | Citation / Source | Deep link |
|---|---|---|
| IMLC compact | Interstate Medical Licensure Compact Commission — Participating States / Compact State Map | https://imlcc.com/participating-states/ |
| Informed consent | California B&P Code §2290.5(b) — telehealth consent | https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?sectionNum=2290.5.&lawCode=BPC |
| Controlled sub. via telehealth | DEA — Diversion Control Division (Telemedicine) | https://www.deadiversion.usdoj.gov/Telemedicine.html |
| PDMP query mandatory | California Health & Safety Code §11165.4(a) — CURES/PDMP | https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?sectionNum=11165.4.&lawCode=HSC |
| Nonresident pharmacy permit | California B&P Code §4112(b) — nonresident pharmacy | https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?sectionNum=4112.&lawCode=BPC |
| USP 795/797 standards | U.S. Pharmacopeia — Compounding Standards (USP 795/797) | https://www.usp.org/compounding |
| 503A/503B framework | U.S. FDA — Human Drug Compounding (503A/503B) | https://www.fda.gov/drugs/guidance-compliance-regulatory-information/human-drug-compounding |
| State compounding permit | California B&P Code §4127 — sterile compounding pharmacy license | https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=BPC&sectionNum=4127. |
| Online pharmacy licensure | California B&P Code §4067 — internet dispensing of dangerous drugs | https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=BPC&sectionNum=4067. |
| DTC platform restrictions | California B&P Code §2242.1 — no internet prescribing without prior exam (Medical Board of CA) | https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=BPC&sectionNum=2242.1. |

## Fields still "Needs legal review" (unsourced)

- Full medical license  (`provider.fullLicense`)
- Telehealth registration  (`provider.telehealthReg`)
- Synchronous video  (`modality.video`)
- Audio-only  (`modality.audioOnly`)
- Asynchronous / store-forward  (`modality.async`)
- In-person exam to establish  (`relationship.inPerson`)
- In-person exam before Rx  (`prescribing.inPersonRx`)
- Controlled-sub. dispensing limits  (`pharmacy.csDispense`)
- Pharmacist-in-charge nuance  (`pharmacy.pic`)
- Website/disclosure rules  (`ecommerce.website`)

## Unclear questions / open items

- Website disclosure/license-display for online drug sales: no CA statute located (may live in 16 CCR regulations — not verified).
- Modality rules (video/audio-only/async) not yet sourced — check Medical Board of California telehealth guidance + 16 CCR.
- In-person exam before controlled-substance Rx: federal DEA floor applies; CA-specific overlay not yet sourced.
- Pharmacist-in-charge (PIC) and controlled-sub dispensing limits: not yet sourced (16 CCR / Board of Pharmacy).

## Items needing pharmacist / attorney review

- [ ] provider.fullLicense scope (Medical Board of California)
- [ ] modality permissions (all three)
- [ ] relationship.inPerson establishment rule
- [ ] prescribing.inPersonRx CA overlay
- [ ] pharmacy.csDispense + pharmacy.pic
- [ ] ecommerce.website disclosure

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — 7 more fields verified (10 -> 17 / 20)

All read verbatim in-browser on leginfo.legislature.ca.gov (clean, un-walled):
- **provider.fullLicense** — B&P §2052(a): practicing/diagnosing/treating/prescribing without a valid unrevoked certificate is a public offense; full CA license required. [ca_2052]
- **modality.video / audioOnly / async** — B&P §2290.5(a): "telehealth" includes BOTH synchronous interactions and asynchronous store-and-forward; modality-neutral, no video mandate, no statutory audio-only ban. [ca_2290_5]
- **relationship.inPerson** — B&P §2290.5(c) + §2242(a): no prior in-person visit required; the "appropriate prior examination" may be met via telehealth. [ca_2290_5]
- **prescribing.inPersonRx** — B&P §2242(a): prescribing without an appropriate prior exam is unprofessional conduct, but the exam can be achieved via telehealth incl. questionnaire if standard of care met; CS remain on the DEA federal floor. [ca_2242_exam]
- **pharmacy.pic** — B&P §4113: every pharmacy must designate a board-approved PIC responsible for all-law compliance; no license issues/renews without one. [ca_4113]

### Still red (3) — mostly genuine nulls, not gaps
- provider.telehealthReg — CA has NO separate telehealth registration/telehealth-only credential (full §2052 license is the pathway); effectively a null.
- pharmacy.csDispense — CS partial-fill/labeling detail lives in 16 CCR Board rules, not read.
- ecommerce.website — no public on-website license-display statute located (may be in 16 CCR).


## UPDATE 2026-07-22 (batch 2) — +1 field (18 -> 19... 18/20 wired this pass)

- **pharmacy.csDispense** — Cal. Health & Safety Code §11200 read verbatim on leginfo: no CS Rx dispensed/refilled >6 months after date (a); Schedule III/IV capped at 5 refills / 120-day supply (b); Schedule II may not be refilled (c). [ca_11200]

Still red: provider.telehealthReg — CA practices telehealth under an existing license (B&P §2290.5) and no separate telehealth registration was located, BUT the research pass did not exhaustively survey the entire Business & Professions Code, so this is left red rather than asserted as a verified null. ecommerce.website — no on-website display statute located (genuine null).
