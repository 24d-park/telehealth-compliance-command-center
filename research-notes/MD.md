# Research Note — Maryland (MD)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 17 / 20  (13 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 3 / 20
- **Method:** Primary sources only, read directly in-browser on mgaleg.maryland.gov (Code) and regs.maryland.gov (COMAR, Open Law Library). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary)

- **COMAR 10.32.05 — Telehealth** (Board of Physicians; amended eff. Sept 15 2025, .06C Jan 19 2026) — https://regs.maryland.gov/us/md/exec/comar/10.32.05
- **Md. Health-General §21-2A-04.2 — PDMP mandatory query** — https://mgaleg.maryland.gov/mgawebsite/Laws/StatuteText?article=ghg&section=21-2A-04.2
- **Md. Health Occ. §12-403 — Pharmacy permit; pharmacist supervision (PIC)** — https://mgaleg.maryland.gov/mgawebsite/Laws/StatuteText?article=gho&section=12-403
- **COMAR 10.34.37 — Nonresident pharmacy permit** — https://regs.maryland.gov/us/md/exec/comar/10.34.37
- **COMAR 10.34.19 — Sterile Pharmaceutical Compounding (USP 795/797)** — https://regs.maryland.gov/us/md/exec/comar/10.34.19

## Verified requirements

Full MD license to treat MD-located patients (10.32.05.03A); synchronous + asynchronous telehealth
(10.32.05.02B); sync/async clinical evaluation, no general in-person mandate (10.32.05.05A); informed
consent required (10.32.05.04A); no Sch II opiate for pain via telehealth without facility/emergency/prior
in-person assessment (10.32.05.06C); **explicit DTC prohibition — "may not treat or prescribe based solely
on a static online questionnaire" (10.32.05.06B)**; PDMP request ≥4mo data before opioid/benzo course since
2018, re-query q90d (HG §21-2A-04.2); pharmacist supervision/PIC (HO §12-403(c)); nonresident permit
(HO §12-403 + COMAR 10.34.37); **USP 795 + 797 explicitly incorporated by reference (COMAR 10.34.19.02)**.

## Fields still "Needs legal review"

- provider.telehealthReg — no separate out-of-state telehealth registration (standard MD licensure applies).
- modality.audioOnly — **EXCLUDED from the Board of Physicians telehealth practice definition**
  (10.32.05.02B: "does not include ... audio-only calls"). NOTE the nuance: audio-only IS recognized for
  Medicaid COVERAGE under Health-General §15-141.2 — two different legal contexts. Left red on the practice
  side to avoid conflating coverage with practice authority.
- ecommerce.website — no on-website display mandate located (label toll-free disclosure only).

## Notable

- MD is currently one of the richest profiles (17/20), with an explicit DTC questionnaire-only prohibition
  and explicit USP 795/797 incorporation — both often absent elsewhere.
- Currency: COMAR 10.32.05 was substantially amended effective Sept 15, 2025, with .06C further amended
  Jan 19, 2026 — treated as the current controlling text.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — +2 fields (17 -> 19/20)

- **provider.telehealthReg (wired):** COMAR 10.32.05.03A — a telehealth practitioner "shall be licensed when providing telehealth services to a patient located in the State" (only HO §14-302 exception). No separate out-of-state telehealth registration; standard MD licensure is the pathway. [md_1032_05]
- **modality.audioOnly (wired) — EXCLUDED:** COMAR 10.32.05.02B(2)(c) read verbatim — "Telehealth" "does not include the provision of health care services solely through: (i) Audio-only calls; (ii) E-mail messages; or (iii) Facsimile transmissions." (Audio-only is separately recognized only for Medicaid COVERAGE under HG §15-141.2 — different legal context.) [md_1032_05]

Only red left (1): ecommerce.website — no on-website license-display mandate located (label toll-free disclosure only). Genuine null.
