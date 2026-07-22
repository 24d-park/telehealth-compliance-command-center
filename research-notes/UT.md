# Research Note — Utah (UT)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 15 / 20  (11 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 5 / 20
- **Method:** Primary sources only, read directly on le.utah.gov (structured statute tables) + adminrules.utah.gov (DOPL R156-17b). Subagent findings treated as leads and independently re-verified.

## Recodification flag

Utah recodified **Title 26 → Title 26B in 2023**, so the Telehealth Act is now **Utah Code 26B-4-704**
(eff. 5/3/2023). Several statute sections currently display a pending **"Effective 7/1/2026"** consolidated
version — dates recorded exactly as shown on the page.

## Sources checked (primary; le.utah.gov + adminrules.utah.gov)

- **26B-4-704 — Scope of telehealth practice** — https://le.utah.gov/xcode/Title26B/Chapter4/26B-4-S704.html
- **58-37f-304 — Controlled Substance Database (mandatory check)** — https://le.utah.gov/xcode/Title58/Chapter37f/58-37f-S304.html
- **58-17b-306 — Class D/nonresident pharmacy** — https://le.utah.gov/xcode/Title58/Chapter17b/58-17b-S306.html
- **DOPL Rule R156-17b** (PIC R156-17b-603; compounding R156-17b-614e) — adminrules.utah.gov

## Verified requirements

Full Title 58 medical license (58-67-301 + 26B-4-704); synchronous video (26B-4-704(1)(g) two-way audio+video);
async store-and-forward (26B-4-704(1)(a)); relationship established "during the patient encounter" — no prior
in-person visit (26B-4-704(2)); no Rx "based solely on ... an online questionnaire ... email ... or a
patient-generated medical history" (26B-4-704(4)); **MANDATORY CSD check** — 58-37f-304(2)(a) prescriber "shall
check the database ... before the first time" prescribing a Schedule II/III opioid; Class D out-of-state
pharmacy licensure (58-17b-306(2)); dispenser CS licensure (58-37f-304(1)(a)); PIC "personally in full and
actual charge" (R156-17b-603); compounding adopts **USP 795/797/800/825** (R156-17b-614e).

## Fields still "Needs legal review"

- **modality.audioOnly** — 26B-4-704 "synchronous interaction" requires two-way audio AND video; audio-only is
  not expressly authorized as a telemedicine modality.
- **relationship.consent** — no dedicated telehealth informed-consent statute (only a credentials-disclosure
  duty).
- provider.telehealthReg (no separate registration; Title 58 license governs), ecommerce.website, ecommerce.dtc.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — +1 field (15 -> 16/20)

- **provider.telehealthReg (now wired):** Utah Code 26B-4-704 authorizes telehealth by a provider holding the applicable Title 58 license (58-67-301 medicine); NO separate telehealth registration or telehealth-only credential exists — full Utah licensure is the pathway. [src: ut_teleact]

Remaining red (4) are genuine: modality.audioOnly (26B-4-704 "synchronous interaction" requires two-way audio AND video — audio-only not authorized), relationship.consent (no dedicated telehealth informed-consent statute, only a credentials-disclosure duty), ecommerce.website/dtc (DOPL rule-level, not located).
