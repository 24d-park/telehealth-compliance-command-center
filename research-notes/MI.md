# Research Note — Michigan (MI)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 16 / 20  ·  **Needs legal review:** 4 / 20
- **Method:** Primary sources only, read directly in-browser on legislature.mi.gov (statute body extracted via console innerText; the https:// form works, http:// is blocked). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; every link deep-links to the specific section)

- **MCL §333.16294 — Unlawful conduct; felony** — https://www.legislature.mi.gov/Laws/MCL?objectName=mcl-333-16294 (Eff. Apr 1, 1994)
- **MCL §333.16283 — Telehealth definitions** — https://www.legislature.mi.gov/Laws/MCL?objectName=mcl-333-16283 (Add. 2016 Act 359)
- **MCL §333.16284 — Telehealth service; consent required** — https://www.legislature.mi.gov/Laws/MCL?objectName=mcl-333-16284 (Add. 2016 Act 359)
- **MCL §333.16285 — Telehealth prescribing** — https://www.legislature.mi.gov/Laws/MCL?objectName=mcl-333-16285 (Am. 2017 Act 22)
- **MCL §500.3476 — Telemedicine services; definitions** (Insurance Code) — https://www.legislature.mi.gov/Laws/MCL?objectName=mcl-500-3476 (Am. 2024 Act 51/52)
- **MCL §333.7303a — CS prescribing; bona fide relationship + MAPS query** — https://www.legislature.mi.gov/Laws/MCL?objectName=mcl-333-7303a (Am. 2019 Act 43)
- **MCL §333.17748 — Pharmacy license required; PIC** — https://www.legislature.mi.gov/Laws/MCL?objectName=mcl-333-17748 (Am. 2020 Act 142)
- **MCL §333.17748a — Sterile compounding; accreditation/USP** — https://www.legislature.mi.gov/Laws/MCL?objectName=mcl-333-17748a (Am. 2015 Act 133)

## Verified requirements (11 state-sourced + federal-framework inheritance)

Full MI license required (§16294 felony + §500.3476(1) licensed-where-patient-located); telehealth
modality — audio, video, and store-and-forward all permitted per §500.3476(2); **telehealth consent
is a GENUINE statutory mandate** (§16284: "shall not provide a telehealth service without directly
or indirectly obtaining consent for treatment," sole exception DOC inmates); MAPS query before CS
exceeding a 3-day supply (§7303a); nonresident pharmacy must be MI-licensed and PIC required, max 3
pharmacies (§17748); sterile-compounding accreditation or USP-standards compliance (§17748a).

## Fields still "Needs legal review"

- provider.telehealthReg — no separate telehealth registry; full licensure instead.
- relationship.inPerson — §16285/§7303a require a bona-fide relationship for CS but impose no prior
  in-person exam; no general in-person-to-establish mandate located.
- ecommerce.website, ecommerce.dtc — live in Board admin rules (R 338.x), not retrieved.

## Notes

- MI modality definitions sit in the INSURANCE code (§500.3476), cross-referenced by the Public
  Health Code telehealth section §16283(c) — flagged in the field notes.
- Board of Pharmacy admin rules (ars.apps.lara.state.mi.us, R 338.x) not accessed; rule-only fields
  (website/DTC, specific USP-chapter-by-number) left red.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.
# Research Note — Michigan (MI)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

## UPDATE 2026-07-22 (wave 2) — +2 fields (16 -> 18/20)

Both read verbatim via Internet Archive id_ capture of legislature.mi.gov (live site returned a cert error in this browser).
- **provider.telehealthReg (wired):** MCL 333.16283(a),(d) — telehealth service is delivered by a "health professional" = "an individual who is engaging in the practice of a health profession" under existing MI licensure; Act 359 of 2016 (§§16283-16288) creates NO separate telehealth registration. [mi_16283]
- **relationship.inPerson (wired):** MCL 333.16284 — "Except as otherwise provided in this section, a health professional shall not provide a telehealth service without directly or indirectly obtaining consent for treatment." Conditions telehealth ONLY on consent; no prior in-person exam mandate. [mi_16284]

Still red (2): ecommerce.website, ecommerce.dtc (Board of Pharmacy admin rules, not located).
