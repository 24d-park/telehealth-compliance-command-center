# Research Note — New Jersey (NJ)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-16
- **Verified fields:** 10 / 20  ·  **Needs legal review:** 10 / 20
- **Method:** Primary sources only, read directly in-browser (statute/rule text confirmed verbatim). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; every link deep-links to the specific document)

- **Interstate Medical Licensure Compact Commission — Participating States / Compact State Map**
  - https://imlcc.com/participating-states/
  - _Compact State Map checked 2026-07-16 (46 member jurisdictions; AK joined 2026-06-22). .org domain is no longer official (casino-spam); .com is official._
- **New Jersey P.L.2017 c.117 — Telemedicine/Telehealth Act (N.J.S.A. 45:1-61 et seq.; §§45:1-62, 45:1-63)**
  - https://pub.njleg.state.nj.us/Bills/2016/PL17/117_.PDF
  - _Enacted chapter-law text read 2026-07-16; amended by P.L.2021 c.310_
- **DEA — Diversion Control Division (Telemedicine)**
  - https://www.deadiversion.usdoj.gov/Telemedicine.html
  - _Checked 2026-07-15 (DEA drafting updated telemedicine rules)_
- **New Jersey P.L.2015 c.74 — Prescription Monitoring Program (N.J.S.A. 45:1-45/46)**
  - https://pub.njleg.state.nj.us/Bills/2014/PL15/74_.PDF
  - _Enacted text read 2026-07-16; amended by P.L.2017 c.341 & P.L.2023 c.177 — verify consolidated thresholds_
- **New Jersey P.L.2003 c.280 §34 — Registration of out-of-State pharmacies (N.J.S.A. 45:14-73)**
  - https://pub.njleg.state.nj.us/Bills/2002/PL03/280_.PDF
  - _Enacted chapter-law text read 2026-07-16 (§45:14-73)_
- **U.S. Pharmacopeia — Compounding Standards (USP 795/797)**
  - https://www.usp.org/compounding
  - _Checked 2026-07-15 (federal framework; confirm state adoption)_
- **U.S. FDA — Human Drug Compounding (503A/503B)**
  - https://www.fda.gov/drugs/guidance-compliance-regulatory-information/human-drug-compounding
  - _FDA content current 2026-06-15 (checked 2026-07-15; confirm state overlay)_
- **New Jersey P.L.2003 c.280 — Pharmacy Practice Act (N.J.S.A. 45:14-41/69/70: compounding def + permit + Board standards authority)**
  - https://pub.njleg.state.nj.us/Bills/2002/PL03/280_.PDF
  - _Enacted text read 2026-07-16; approved 2004-01-14. Sterile-specific = N.J.A.C. 13:39 (Imperva-blocked, not verified)_

## Verified requirements — exact citations

| Field | Citation / Source | Deep link |
|---|---|---|
| IMLC compact | Interstate Medical Licensure Compact Commission — Participating States / Compact State Map | https://imlcc.com/participating-states/ |
| In-person exam to establish | New Jersey P.L.2017 c.117 — Telemedicine/Telehealth Act (N.J.S.A. 45:1-61 et seq.; §§45:1-62, 45:1-63) | https://pub.njleg.state.nj.us/Bills/2016/PL17/117_.PDF |
| Informed consent | New Jersey P.L.2017 c.117 — Telemedicine/Telehealth Act (N.J.S.A. 45:1-61 et seq.; §§45:1-62, 45:1-63) | https://pub.njleg.state.nj.us/Bills/2016/PL17/117_.PDF |
| Controlled sub. via telehealth | DEA — Diversion Control Division (Telemedicine) | https://www.deadiversion.usdoj.gov/Telemedicine.html |
| In-person exam before Rx | New Jersey P.L.2017 c.117 — Telemedicine/Telehealth Act (N.J.S.A. 45:1-61 et seq.; §§45:1-62, 45:1-63) | https://pub.njleg.state.nj.us/Bills/2016/PL17/117_.PDF |
| PDMP query mandatory | New Jersey P.L.2015 c.74 — Prescription Monitoring Program (N.J.S.A. 45:1-45/46) | https://pub.njleg.state.nj.us/Bills/2014/PL15/74_.PDF |
| Nonresident pharmacy permit | New Jersey P.L.2003 c.280 §34 — Registration of out-of-State pharmacies (N.J.S.A. 45:14-73) | https://pub.njleg.state.nj.us/Bills/2002/PL03/280_.PDF |
| USP 795/797 standards | U.S. Pharmacopeia — Compounding Standards (USP 795/797) | https://www.usp.org/compounding |
| 503A/503B framework | U.S. FDA — Human Drug Compounding (503A/503B) | https://www.fda.gov/drugs/guidance-compliance-regulatory-information/human-drug-compounding |
| State compounding permit | New Jersey P.L.2003 c.280 — Pharmacy Practice Act (N.J.S.A. 45:14-41/69/70: compounding def + permit + Board standards authority) | https://pub.njleg.state.nj.us/Bills/2002/PL03/280_.PDF |

## Fields still "Needs legal review" (unsourced)

- Full medical license  (`provider.fullLicense`)
- Telehealth registration  (`provider.telehealthReg`)
- Synchronous video  (`modality.video`)
- Audio-only  (`modality.audioOnly`)
- Asynchronous / store-forward  (`modality.async`)
- Controlled-sub. dispensing limits  (`pharmacy.csDispense`)
- Pharmacist-in-charge nuance  (`pharmacy.pic`)
- Online pharmacy licensure  (`ecommerce.onlinePharmacy`)
- Website/disclosure rules  (`ecommerce.website`)
- DTC platform restrictions  (`ecommerce.dtc`)

## Unclear questions / open items

- NJPMP query thresholds: verified 2015 enacted text (P.L.2015 c.74), but amended by P.L.2017 c.341 and P.L.2023 c.177 — confirm CURRENT triggers against consolidated N.J.S.A. text before relying operationally.
- prescribing.inPersonRx (Sch. II): statute references implementing regulation 'as provided by regulation' (N.J.A.C. Title 13) — exact admin-code detail NOT read.
- Sterile-compounding-specific rules: N.J.A.C. 13:39 — njconsumeraffairs.gov is Imperva-blocked, could NOT be verified.
- E-commerce (online pharmacy / website / DTC): NO internet-specific language in the Pharmacy Practice Act; N.J.A.C. 13:39 blocked — all three left Needs legal review.

## Items needing pharmacist / attorney review

- [ ] NJPMP current thresholds vs consolidated N.J.S.A. (post-2017/2023 amendments)
- [ ] prescribing.inPersonRx implementing rule (N.J.A.C. 13)
- [ ] sterile-compounding rules (N.J.A.C. 13:39 — access blocked)
- [ ] all e-commerce fields
- [ ] provider.fullLicense + telehealthReg
- [ ] modality permissions
- [ ] pharmacy.csDispense + pharmacy.pic

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — 4 more fields verified (10 -> 14 / 20)

Read verbatim via pdf.js on the enacted P.L.2017 c.117 (Telemedicine/Telehealth Act) at pub.njleg.state.nj.us:
- **provider.fullLicense** — N.J.S.A. 45:1-62.b(1): provider must be validly licensed/certified/registered under Title 45 to provide services in NJ. [nj_45_1_62]
- **modality.video** — §45:1-62.c(1): "Telemedicine services shall be provided using interactive, real-time, two-way communication technologies." [nj_45_1_62]
- **modality.async** — §45:1-62.c(2): asynchronous store-and-forward expressly permitted. [nj_45_1_62]
- **modality.audioOnly** — §45:1-61 def: telemedicine "does not include the use, in isolation, of audio-only telephone" (etc.); §45:1-62.c(2) allows interactive audio only combined with store-and-forward (no video) if the in-person standard of care is met after records review. Audio-only alone is NOT telemedicine. [nj_45_1_62]

### Still red (6) — all behind the Imperva block
provider.telehealthReg, pharmacy.csDispense, pharmacy.pic, ecommerce.onlinePharmacy/website/dtc. The NJ Pharmacy Practice Act PDF is too large for pdf.js to fully parse and the sterile/PIC/e-commerce specifics live in **N.J.A.C. 13:39**, which is Imperva-blocked (njconsumeraffairs.gov). Left honest-red. FOLLOW-UP: N.J.A.C. 13:39 via an un-walled mirror or Wayback.
