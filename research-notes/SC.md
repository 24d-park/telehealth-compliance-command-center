# Research Note — South Carolina (SC)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 15 / 20  (11 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 5 / 20
- **Method:** Primary sources only, read directly in-browser on scstatehouse.gov (SC Code of Laws; chapter pages render full section text inline). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; scstatehouse.gov)

- **§40-47-37 — SC Telemedicine Act** (licensure, evaluation standard, CS limits) — https://www.scstatehouse.gov/code/t40c047.php
- **§40-47-20(53) — telemedicine definition** — same chapter
- **§40-47-113(C) — questionnaire-only prescribing is unprofessional** — same chapter
- **§44-53-1645 — PMP mandatory review (Schedule II)** — https://www.scstatehouse.gov/code/t44c053.php
- **§40-43-83 / §40-43-86 — nonresident pharmacy permit, PIC, compounding** — https://www.scstatehouse.gov/code/t40c043.php

## Verified requirements

Full SC medical license to treat SC patients via telemedicine (§40-47-37(A)(4)); telemedicine defined
technology-neutrally (§40-47-20(53)); appropriate evaluation "which need not be done in person" (no
categorical in-person mandate); **Schedule II-narcotic and Schedule III-narcotic prescriptions not permitted
via telemedicine** except four enumerated cases (§40-47-37(C)(7)(b)); **mandatory PMP review before Schedule
II prescribing** — "shall review ... before" (§44-53-1645, verb verified); questionnaire-only prescribing
"is unprofessional" (§40-47-113(C)); nonresident/mail-order pharmacy permit (§40-43-83); PIC (§40-43-86);
compounding standard via Board inspection forms/USP-NF compendia.

## Fields still "Needs legal review"

- provider.telehealthReg — no separate registration (full licensure + a Bureau of Drug Control CS
  registration only if prescribing controlled substances).
- modality.audioOnly, modality.async — the technology-neutral definition neither names nor excludes them
  (NOT FOUND as explicit rules).
- relationship.consent — §40-47-37 requires identity/location verification + credential disclosure, but no
  express informed-consent-for-telehealth clause.
- ecommerce.website — §40-43-83(F) requires the permit be displayed in the physical premises, not a website.

## Notable

- compounding.stateReg is verified but framed carefully: SC references Board inspection forms + USP-NF
  compendia rather than adopting USP 795/797 **by number** — a real state standard, not a by-chapter USP
  adoption like WA/MD/OR.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — +1 field (15 -> 16/20)

- **provider.telehealthReg (now wired):** S.C. Code §40-47-37(A)(4) read verbatim on scstatehouse.gov: a telemedicine licensee must "be licensed to practice medicine in this State" (an out-of-state physician need not reside in SC but must hold a valid, current SC medical license). NO separate telehealth registration exists (only an added SC Bureau of Drug Control CS registration if prescribing controlled substances). [src: sc_4047_37]

Remaining red (4) are genuine: modality.audioOnly/async (technology-neutral definition neither names nor excludes them), relationship.consent (no express telehealth informed-consent clause), ecommerce.website (§40-43-83(F) requires permit display in the PHYSICAL premises, not a website).


## UPDATE 2026-07-22 (batch 2) — +1 field (16 -> 17/20)

- **modality.audioOnly** — S.C. Code §40-47-20(53) read verbatim: telemedicine defined medium-neutrally ("electronic communications, information technology, or other means") and NOT excluding audio-only; §40-47-37 imposes a standard-of-care duty but no video-only requirement. Audio-only permitted where the standard of care is met. [sc_4047_37]

Still red: modality.async (chapter has no store-and-forward provision — NOT FOUND), relationship.consent (no informed-consent clause in Ch. 47 — genuine null), ecommerce.website.
