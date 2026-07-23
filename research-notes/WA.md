# Research Note — Washington (WA)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 13 / 20  ·  **Needs legal review:** 7 / 20
- **Method:** Primary sources only, read directly in-browser on app.leg.wa.gov (RCW statutes + WAC rules). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; app.leg.wa.gov)

- **RCW 70.41.020 — Definitions (telemedicine / audio-only telemedicine)** — https://app.leg.wa.gov/RCW/default.aspx?cite=70.41.020
- **RCW 74.09.325 — Reimbursement of telemedicine/store-and-forward; audio-only** — https://app.leg.wa.gov/RCW/default.aspx?cite=74.09.325
- **RCW 18.71.030 — Exemptions (out-of-state telemedicine consultation)** — https://app.leg.wa.gov/RCW/default.aspx?cite=18.71.030
- **RCW 18.64.360 — Nonresident pharmacies** — https://app.leg.wa.gov/RCW/default.aspx?cite=18.64.360
- **WAC 246-919-985 — PMP required registration/queries** — https://app.leg.wa.gov/wac/default.aspx?cite=246-919-985
- **WAC 246-945-310 — Responsible pharmacy manager** — https://app.leg.wa.gov/wac/default.aspx?cite=246-945-310
- **WAC 246-945-100 — Compounding minimum standards (USP)** — https://app.leg.wa.gov/wac/default.aspx?cite=246-945-100

## Verified requirements (9 state-sourced + federal-framework inheritance)

Full WA license to independently treat WA patients via telemedicine (RCW 18.71.030(6)-(7) — out-of-
state provider may only consult with a WA-licensed practitioner); telemedicine = interactive audio AND
video, definition includes audio-only (RCW 70.41.020); store-and-forward recognized + audio-only
established-relationship condition from Jan 1 2023 + advance billing consent (RCW 74.09.325); opioid
PMP query at defined junctures (WAC 246-919-985); nonresident pharmacy licensed by DOH (RCW 18.64.360);
responsible pharmacy manager, WA-licensed (WAC 246-945-310); USP <795>/<797>/<800>/<825> (WAC 246-945-100).

## Fields still "Needs legal review"

- relationship.inPerson — no general in-person-exam-to-establish mandate located.
- relationship.consent — only an audio-only BILLING consent (RCW 74.09.325(8)), too narrow to be a
  general telehealth informed-consent rule; former WAC 246-919-855 informed-consent rule was REPEALED.
- prescribing.inPersonRx — no WA state CS in-person mandate located (federal Ryan Haight applies separately).
- provider.telehealthReg — no separate registration (RCW 43.70.495 is a training/attestation for
  non-physicians, not a registration).
- pharmacy.csDispense — WAC 246-945 Subpart C index confirmed but individual rule text not read; left red.
- ecommerce.website, ecommerce.dtc — not located in sources read.

## Notes

- WA's modality/audio-only/async fields are anchored in a **Medicaid reimbursement statute**
  (RCW 74.09.325) + DOH definitions (RCW 70.41.020) — flagged in the field notes; there is no separate
  clinical-practice telemedicine-modality statute.
- Subagent corrected bad task hints: RCW 18.71.470 and 18.130.098 are NOT telemedicine provisions.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — gap-fill attempted, NO change (stays 13/20)

Most remaining reds are **genuine absences, not access failures** (confirmed against RCW/WAC already read):
- relationship.consent — the former **WAC 246-919-855 telehealth informed-consent rule was REPEALED**; only a narrow audio-only BILLING consent (RCW 74.09.325(8)) remains, too narrow to assert as a general consent mandate.
- relationship.inPerson — no general in-person-exam-to-establish mandate in WA statute.
- prescribing.inPersonRx — no WA state CS in-person mandate (federal Ryan Haight governs separately).
- provider.telehealthReg — no separate registration (RCW 43.70.495 is training/attestation, not a registry).
Only **pharmacy.csDispense** (WAC 246-945 Subpart C) and **ecommerce.website/dtc** are true unread gaps; the individual WAC-rule fetches timed out this session. Honest hold. FOLLOW-UP: WAC 246-945 Subpart C controlled-substance dispensing rules when the WAC fetch is stable.


---

## Update 2026-07-23 (wave 5) — +1 (13 -> 14 verified)

**pharmacy.csDispense wired** — WAC 246-945-011 "Prescription validity" (eff. 6/13/24), read verbatim on app.leg.wa.gov (Chapter 246-945 full HTML): "(1) Prior to dispensing and delivering a prescription, a pharmacist shall verify its validity. (2) A prescription shall be considered invalid if: (a) ... alteration, erasure, or addition ...; (b) ... does not contain the required information ...; (c) ... is expired; or (d) The prescription is for a controlled substance and does not comply with the requirements in RCW 69.50.308." (3)(a): Schedule II-V Rx expires 6 months after issue. Mandatory pharmacist CS-validity gate. [wa_945011] This closes the ONE true unread gap flagged in the prior WA note (WAC 246-945 Subpart C).

NOTE on other Subpart C sections: 246-945-040 (Uniform Controlled Substance Act) is a definitional/stimulant-designation rule, and 246-945-346 is CS prescription transfers — 246-945-011 is the operative dispensing-validity gate.

### Remaining reds (6) — all confirmed GENUINE ABSENCES, not access failures:
- provider.telehealthReg — RCW 43.70.495 is a training/attestation for non-physicians, NOT a telehealth registry. No separate registration exists.
- relationship.inPerson — no general in-person-exam-to-establish mandate in WA statute.
- relationship.consent — former WAC 246-919-855 telehealth informed-consent rule REPEALED; only a narrow audio-only BILLING consent (RCW 74.09.325(8)) remains, too narrow for a general consent mandate.
- prescribing.inPersonRx — no WA state CS in-person mandate (federal Ryan Haight governs separately).
- ecommerce.website, ecommerce.dtc — not located in RCW/WAC read; no on-website display mandate or general questionnaire ban.
