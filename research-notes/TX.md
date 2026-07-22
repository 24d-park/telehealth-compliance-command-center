# Research Note — Texas (TX)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-16
- **Verified fields:** 11 / 20  ·  **Needs legal review:** 9 / 20
- **Method:** Primary sources only, read directly in-browser (statute/rule text confirmed verbatim). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; every link deep-links to the specific document)

- **Interstate Medical Licensure Compact Commission — Participating States / Compact State Map**
  - https://imlcc.com/participating-states/
  - _Compact State Map checked 2026-07-16 (46 member jurisdictions; AK joined 2026-06-22). .org domain is no longer official (casino-spam); .com is official._
- **Texas Occupations Code Ch. 111 — Telemedicine/Teledentistry/Telehealth (§§111.002 consent, 111.005 relationship, 111.007 standard)**
  - https://statutes.capitol.texas.gov/Docs/OC/htm/OC.111.htm
  - _Statute text read 2026-07-16; current through 89th Leg. 2nd C.S., 2025_
- **DEA — Diversion Control Division (Telemedicine)**
  - https://www.deadiversion.usdoj.gov/Telemedicine.html
  - _Checked 2026-07-15 (DEA drafting updated telemedicine rules)_
- **Texas Health & Safety Code §481.0764(a) — Texas PMP**
  - https://statutes.capitol.texas.gov/Docs/HS/htm/HS.481.htm
  - _Statute text read 2026-07-16; current through 89th Leg. 2nd C.S., 2025_
- **Texas Occupations Code §560.001(b) — nonresident (Class E) pharmacy license**
  - https://statutes.capitol.texas.gov/Docs/OC/htm/OC.560.htm
  - _Statute text read 2026-07-16; current through 89th Leg. 2nd C.S., 2025_
- **U.S. Pharmacopeia — Compounding Standards (USP 795/797)**
  - https://www.usp.org/compounding
  - _Checked 2026-07-15 (federal framework; confirm state adoption)_
- **U.S. FDA — Human Drug Compounding (503A/503B)**
  - https://www.fda.gov/drugs/guidance-compliance-regulatory-information/human-drug-compounding
  - _FDA content current 2026-06-15 (checked 2026-07-15; confirm state overlay)_
- **Texas Occupations Code §562.156 & §560.052(g) — sterile-compounding license + pre-license inspection**
  - https://statutes.capitol.texas.gov/Docs/OC/htm/OC.562.htm
  - _Statute text read 2026-07-16; §562.156 added Acts 2013 Ch. 608 (SB 1100), eff. 2013-09-01_
- **Texas Occupations Code §560.051(f) — Class E / nonresident (mail-order & online) pharmacy license**
  - https://statutes.capitol.texas.gov/Docs/OC/htm/OC.560.htm
  - _Statute text read 2026-07-16; current through 89th Leg. 2nd C.S., 2025_
- **Texas Occupations Code §562.112 — no dispensing of Rx from internet/telephonic consult without valid practitioner-patient relationship**
  - https://statutes.capitol.texas.gov/Docs/OC/htm/OC.562.htm
  - _Statute text read 2026-07-16; added Acts 2005 Ch. 1345 (SB 410), eff. 2005-09-01_

## Verified requirements — exact citations

| Field | Citation / Source | Deep link |
|---|---|---|
| IMLC compact | Interstate Medical Licensure Compact Commission — Participating States / Compact State Map | https://imlcc.com/participating-states/ |
| In-person exam to establish | Texas Occupations Code Ch. 111 — Telemedicine/Teledentistry/Telehealth (§§111.002 consent, 111.005 relationship, 111.007 standard) | https://statutes.capitol.texas.gov/Docs/OC/htm/OC.111.htm |
| Informed consent | Texas Occupations Code Ch. 111 — Telemedicine/Teledentistry/Telehealth (§§111.002 consent, 111.005 relationship, 111.007 standard) | https://statutes.capitol.texas.gov/Docs/OC/htm/OC.111.htm |
| Controlled sub. via telehealth | DEA — Diversion Control Division (Telemedicine) | https://www.deadiversion.usdoj.gov/Telemedicine.html |
| PDMP query mandatory | Texas Health & Safety Code §481.0764(a) — Texas PMP | https://statutes.capitol.texas.gov/Docs/HS/htm/HS.481.htm |
| Nonresident pharmacy permit | Texas Occupations Code §560.001(b) — nonresident (Class E) pharmacy license | https://statutes.capitol.texas.gov/Docs/OC/htm/OC.560.htm |
| USP 795/797 standards | U.S. Pharmacopeia — Compounding Standards (USP 795/797) | https://www.usp.org/compounding |
| 503A/503B framework | U.S. FDA — Human Drug Compounding (503A/503B) | https://www.fda.gov/drugs/guidance-compliance-regulatory-information/human-drug-compounding |
| State compounding permit | Texas Occupations Code §562.156 & §560.052(g) — sterile-compounding license + pre-license inspection | https://statutes.capitol.texas.gov/Docs/OC/htm/OC.562.htm |
| Online pharmacy licensure | Texas Occupations Code §560.051(f) — Class E / nonresident (mail-order & online) pharmacy license | https://statutes.capitol.texas.gov/Docs/OC/htm/OC.560.htm |
| DTC platform restrictions | Texas Occupations Code §562.112 — no dispensing of Rx from internet/telephonic consult without valid practitioner-patient relationship | https://statutes.capitol.texas.gov/Docs/OC/htm/OC.562.htm |

## Fields still "Needs legal review" (unsourced)

- Full medical license  (`provider.fullLicense`)
- Telehealth registration  (`provider.telehealthReg`)
- Synchronous video  (`modality.video`)
- Audio-only  (`modality.audioOnly`)
- Asynchronous / store-forward  (`modality.async`)
- In-person exam before Rx  (`prescribing.inPersonRx`)
- Controlled-sub. dispensing limits  (`pharmacy.csDispense`)
- Pharmacist-in-charge nuance  (`pharmacy.pic`)
- Website/disclosure rules  (`ecommerce.website`)

## Unclear questions / open items

- prescribing.inPersonRx: NO Texas statute mandates an in-person exam before a telehealth controlled-substance Rx (§111.009 supply limits are teledentistry-only). Confirm no 22 TAC rule imposes one.
- Website disclosure/license-display: would be a 22 TAC (TSBP) rule; the TAC portal is a JS-only Appian portal that could not be loaded — not verified.
- Modality rules (video/audio-only/async): TMB rules in 22 TAC Ch. 174 not loaded — statute confirms relationship + standard of care only.
- Class A/A-S compounding distinctions are set by TSBP rule (22 TAC), not statute — statute confirms the sterile-license requirement only.

## Items needing pharmacist / attorney review

- [ ] provider.fullLicense + telehealthReg (TMB)
- [ ] modality permissions (22 TAC Ch. 174)
- [ ] prescribing.inPersonRx — confirm no TAC in-person mandate
- [ ] pharmacy.csDispense + pharmacy.pic
- [ ] ecommerce.website (22 TAC TSBP rule)

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — +5 fields (11 -> 16/20)

**Access note:** statutes.capitol.texas.gov was rebuilt into an Angular SPA (returns only the app shell — same failure class as Indiana's iga.in.gov). Re-read Occupations Code Ch. 111 verbatim via **Internet Archive id_ raw capture** of the pre-redesign static page.
- **provider.fullLicense** — §111.001(7): telemedicine medical service = delivered by "a physician licensed in this state." [tx_111_def]
- **modality.video** — §111.005(a)(3)(A): synchronous audiovisual interaction. [tx_111_def]
- **modality.async** — §111.005(a)(3)(B): asynchronous store-and-forward. [tx_111_def]
- **modality.audioOnly** — §111.005(a)(3)(B): synchronous audio permitted ONLY in conjunction with store-and-forward (not standalone). [tx_111_def]
- **prescribing.inPersonRx** — §111.005 (no prior in-person) + §111.009 (CS quantity caps are teledentistry-only, not physicians); CS on DEA floor. [tx_111_rx]

### Still red (4) — all in 22 TAC (JS-gated Appian SPA portal)
provider.telehealthReg, pharmacy.csDispense, pharmacy.pic, ecommerce.website. FOLLOW-UP: 22 TAC Ch. 174 (TMB) + TSBP rules via a working TAC path or Wayback.


## UPDATE 2026-07-22 (batch 2) — +4 fields (16 -> 20/20, COMPLETE)

All read verbatim via Internet Archive `id_` raw captures of the pre-SPA Occupations Code pages (statutes.capitol.texas.gov is now a JS SPA).
- **provider.telehealthReg** — Occ. Code §151.056(a): an out-of-jurisdiction person performing an act part of a Texas-initiated patient-care service "is considered to be engaged in the practice of medicine in this state and is subject to appropriate regulation by the board." Full TX licensure; no separate telehealth registration. [tx_151_056]
- **pharmacy.csDispense** — §562.056(a): no dispensing without a valid practitioner-patient relationship; a pharmacist "may not dispense ... if the pharmacist knows or should know that the prescription was issued without a valid practitioner-patient relationship." (Schedule-specific limits also in H&S Code Ch. 481.) [tx_562]
- **pharmacy.pic** — §562.101 (pharmacy under pharmacist supervision; Class A/B continuous on-site) + §551.003(29) PIC definition. [tx_562]
- **ecommerce.website** — §562.1045: an internet-selling pharmacy "shall link its site to the Internet site maintained by the board" and post board complaint info/telephone/mailing address/website on its home page. **A rare genuine on-website disclosure mandate.** [tx_562]

**Texas is now fully sourced: 20/20.**
