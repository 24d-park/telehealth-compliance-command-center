# Research Note — Wisconsin (WI)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 17 / 20  (13 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 3 / 20
- **Method:** Primary sources only, read directly in-browser on docs.legis.wisconsin.gov (official statutes + admin code). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; docs.legis.wisconsin.gov)

- **Wis. Admin. Code Med 24 — Telemedicine** (license .04, relationship .03, consent .07(1)(c), DTC ban .07(2)) — https://docs.legis.wisconsin.gov/code/admin_code/med/24
- **Wis. Stat. §440.01(1) — Telehealth definitions** — https://docs.legis.wisconsin.gov/statutes/statutes/440/i/01
- **Wis. Stat. §961.385(2)(cs) — ePDMP mandatory review** — https://docs.legis.wisconsin.gov/statutes/statutes/961/iii/385
- **Wis. Stat. §450.065 — out-of-state pharmacy license** — https://docs.legis.wisconsin.gov/statutes/statutes/450/065
- **Wis. Stat. §450.09 — managing pharmacist** — https://docs.legis.wisconsin.gov/statutes/statutes/450/09
- **Wis. Admin. Code Phar 15.02 — compounding (USP)** — https://docs.legis.wisconsin.gov/code/admin_code/phar/15

## Verified requirements

Full WI medical license to treat WI patients via telemedicine (Med 24.04); relationship may be established
through telemedicine (Med 24.03); informed consent required (Med 24.07(1)(c) → §448.30 + Med 18); telehealth
defined to cover audio/video/data + asynchronous (§440.01(1)); **mandatory ePDMP review before prescribing**
(§961.385(2)(cs)); out-of-state pharmacy license (§450.065); managing pharmacist (§450.09); DTC
questionnaire-only prescribing prohibited (Med 24.07(2)); **USP 795/797/800/825 incorporated by reference**
(Phar 15.02, eff. 10-1-25).

## Notable / time-sensitive

- **The mandatory PDMP-review requirement has a statutory SUNSET: it "does not apply after April 1, 2030"
  (§961.385(2)(cs)).** Flagged so the tracker can re-check before that date.
- Phar 15 was repealed-and-recreated effective 10-1-25 (CR 24-092) — current USP chapters official as of
  Nov 1, 2023.

## Fields still "Needs legal review"

- provider.telehealthReg — no separate out-of-state telehealth registration; full licensure is the mechanism.
- prescribing.inPersonRx — no controlled-substance-specific in-person exam mandate located.
- ecommerce.website — no on-website license/disclosure requirement (§450.065(5) requires a phone line, not
  a website display).

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — +2 fields (17 -> 19/20)

- **provider.telehealthReg (wired):** Wis. Admin. Code Med 24.04 read verbatim — "A physician who uses telemedicine in the diagnosis and treatment of a patient located in this state shall be licensed to practice medicine and surgery by the medical examining board." No separate telehealth registration; full WI licensure is the mechanism. [wi_med24]
- **prescribing.inPersonRx (wired):** Med 24.07(1) — website/internet treatment (incl. issuing a prescription) requires licensure + name/contact disclosure + informed consent (§448.30) + "a documented patient evaluation ... a medical history and ... an examination or evaluation, or both, and diagnostic tests." The evaluation may be conducted via telemedicine — NO prior in-person-exam mandate; controlled substances remain on the federal DEA floor. [wi_med24]

Only red left (1): ecommerce.website — §450.065(5) requires a phone line, not a website display. Genuine null.
