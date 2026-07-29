# Research Note — Mississippi (MS)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 16 / 20  (12 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 4 / 20
- **Method:** Primary sources only. Subagent findings treated as leads and independently re-verified.

## Sources checked (official .gov)

- **Miss. Admin. Code Part 2635, Ch. 5 — Practice of Telemedicine** (msbml.ms.gov HTML reproduction, "as last
  amended February 2026") — https://www.msbml.ms.gov/mississippi-administrative-code
- **Part 2635, Ch. 7 — Internet Prescribing** — same host
- **MS Board of Pharmacy regs Title 30 Part 3001** (Art. VII PIC, XVIII CS, XXXI compounding, XLIII PMP) +
  Miss. Code §73-21-106 — PDFs on mbp.ms.gov (read via PDF.js)

## Verified requirements

Full MS license to practice any form of telemedicine (Part 2635 Ch. 5 Rule 5.2); real-time interactive video
(5.1(F)/5.5); **audio-only PERMITTED "where medically appropriate"** (5.5 — note MS allows audio-only, unlike
TN/MD/IA); store-and-forward permitted but may enhance not replace real-time (5.5); valid relationship required,
"a simple questionnaire without an appropriate exam is in violation" (5.4-5.5); informed consent (5.3); no Rx
"based solely on answers to a set of questions" (Ch. 7); nonresident pharmacy permit (§73-21-106); PIC (Art.
VII); **compounding adopts USP 795/797/800 by number** (Art. XXXI); CS dispensing (Art. XVIII).

## PMP nuance (verify-don't-assume)

**prescribing.pdmp left "Needs legal review."** MS has NO blanket prescriber-side mandatory query — §73-21-127
prescriber access is "may access" (voluntary). The only mandatory "shall review the PMP" is **pharmacist-side**
(Art. XLIII), narrow: before dispensing a Schedule II opiate to a new customer or where no opioid Rx filled
there within 6 months. That's recorded under pharmacy.csDispense, not misattributed to the prescriber field.

## Fields still "Needs legal review"

prescribing.pdmp (prescriber voluntary), provider.telehealthReg (full license, no separate registration),
ecommerce.website, ecommerce.dtc.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-29 — final-research wave 4, +2 fields (16 -> 18/20)
Subagent lead, parent-verified: Rule 5.2 + Rule 7.1 verbatim on msbml.ms.gov; §73-25-34 via Wayback id_ of Justia.
- **provider.telehealthReg** — VERIFIED-NULL. Miss. Admin. Code Pt. 2635 Ch. 5 Rule 5.2: "only providers
  holding a valid Mississippi license are allowed to practice any form of telemedicine ... in Mississippi";
  Miss. Code §73-25-34(2): "no person shall engage in the practice of medicine across state lines (telemedicine)
  ... unless he has first obtained a license." Full MS licensure is the exclusive pathway; no separate registry.
  Reused ms_2635_5.
- **ecommerce.dtc** — Pt. 2635 Ch. 7 Rule 7.1 (Internet Prescribing): prescribing "based solely on answers to a
  set of questions ... fails to meet an acceptable standard of care." Reused ms_2635_7.
### Confirmed HOLDS
- prescribing.pdmp — §73-21-127 is dispenser-reporting + PMP user-registration + permissive access; the ONLY
  mandatory review duty is scoped to registered pain-management practices, NOT a universal prescriber query.
  Stays red.
- ecommerce.website — no on-website disclosure mandate. Genuine absence.
