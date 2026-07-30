# Research Note — Connecticut (CT)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 16 / 20  (12 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 4 / 20
- **Method:** Primary sources only, read directly in-browser on cga.ct.gov (official CT General Statutes; full chapter text renders inline). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; cga.ct.gov)

- **§19a-906 — Telehealth services** (Ch. 368ll; modality, consent, CS limits) — https://www.cga.ct.gov/current/pub/chap_368ll.htm
- **§20-9(d) — practice of medicine incl. electronic/interstate** (Ch. 370) — https://www.cga.ct.gov/current/pub/chap_370.htm
- **§21a-254(j) — CPMRS mandatory review** (Ch. 420b) — https://www.cga.ct.gov/current/pub/chap_420b.htm
- **§20-594 / §20-627 / §20-633b — pharmacy** (Ch. 400j) — https://www.cga.ct.gov/current/pub/chap_400j.htm

## Verified requirements

Full CT license incl. electronic/interstate service to CT patients (§20-9(d)); telehealth via real-time
interactive two-way tech + asynchronous store-and-forward (§19a-906(a), excludes only fax/text/email); no
prior in-person visit required (§19a-906(b)(1)); **MANDATORY consent** — inform of methods/limitations and
"obtain the patient's consent," documented (§19a-906(b)(2),(e)); **CS-via-telehealth restriction** — no
Schedule I/II/III except non-opioid II/III for psych/SUD per Ryan Haight (§19a-906(c)); **MANDATORY PMP
review** before >72-hour CS supply, q90d recurring (§21a-254(j)(9)); nonresident pharmacy registration
(§20-627); managing pharmacist (§20-594/§20-597); **USP 797/800/825 adopted by statute** (§20-633b).

## Notable / time-sensitive

- **provider.telehealthReg left RED — the out-of-state telehealth-provider registration is SUNSETTING/EXPIRED
  on its face.** §19a-906(k)-(l) applies "on or before June 30, 2025," and the earlier §19a-906a out-of-state
  authorization mechanism was **repealed effective June 4, 2024** (P.A. 24-110). Rather than record an
  expired COVID-era pathway as a live registration, left it red. Flag for re-check if CT re-enacts.
- **modality.audioOnly left RED (honest correction).** The current §19a-906 does NOT name audio-only — the
  research hint that it does was not borne out by the actual text. CT's audio-only allowances live in
  insurance-COVERAGE public acts, a different legal context, so it's red on the practice side.

## Fields still "Needs legal review"

provider.telehealthReg (sunset/repealed), modality.audioOnly (not in §19a-906), ecommerce.website,
ecommerce.dtc (no statute located).

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-29 — final-research wave 3, +1 field (16 -> 17/20)
Parent-worked in-browser on cga.ct.gov (chapter 368a).
- **modality.audioOnly** — Conn. Gen. Stat. §19a-906(a): the telehealth definition provides "Telehealth does
  not include the use of facsimile, audio-only telephone, texting or electronic mail." Audio-only telephone is
  EXCLUDED from telehealth (cannot be the sole modality). Reused ct_19a906.
### Held
- provider.telehealthReg — §20-9(d) requires full CT licensure to treat CT patients via electronic
  communications, but the §19a-906(a) "telehealth provider" enumeration (all CT-licensed provider types, which
  would establish the verified-null / no-separate-registry) sits in the 2026 Supplement that did not load
  cleanly this session. Left RED rather than overreach — re-verify from the 2026 Supplement next session.
- ecommerce.website / ecommerce.dtc — genuine absences (no CT on-website-display or questionnaire-ban statute
  located).


## UPDATE 2026-07-30 — gap-fill wave, +1 field (17 -> 18/20) — closes a prior HELD lead
Subagent lead, parent-verified verbatim on cga.ct.gov. Prior session HELD this red because it looked for §19a-906
in Chapter 368a and the 2026 Supplement wouldn't load; the CORRECT location is **Chapter 368ll** (Miscellaneous
Provisions), and it loads fine.
- **provider.telehealthReg -> WIRED (VERIFIED-NULL), reusing key ct_19a906.** Conn. Gen. Stat. §19a-906(a)(12):
  a "Telehealth provider" means (A) "any health care provider licensed pursuant to title 20 and any pharmacist
  licensed by the Department of Consumer Protection pursuant to title 20 ..." The only out-of-state pathway, branch
  (B), was time-limited "on or before June 30, 2025" (now EXPIRED), and the separate §19a-906a out-of-state-order
  pathway is "repealed, effective June 4, 2024." So as of 2026 only title-20 CT-licensed providers qualify —
  licensure is EXCLUSIVE. This exceeds the prior §20-9(d) "license required" hold basis (which alone would have
  been overreach): the enumeration + the sunset/repeal together prove exclusivity. No new source key.
### Still red (2): ecommerce.website, ecommerce.dtc (genuine absences).
