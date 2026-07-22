# Research Note — New York (NY)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-16 (re-checked 2026-07-20)
- **Verified fields:** 6 / 20  ·  **Needs legal review:** 14 / 20
- **Method:** Primary sources only, read directly in-browser (statute/rule text confirmed verbatim). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; every link deep-links to the specific document)

- **Interstate Medical Licensure Compact Commission — Participating States / Compact State Map**
  - https://imlcc.com/participating-states/
  - _Compact State Map checked 2026-07-16 (46 member jurisdictions; AK joined 2026-06-22). .org domain is no longer official (casino-spam); .com is official._
- **DEA — Diversion Control Division (Telemedicine)**
  - https://www.deadiversion.usdoj.gov/Telemedicine.html
  - _Checked 2026-07-15 (DEA drafting updated telemedicine rules)_
- **New York Education Law §6808-b — Registration of nonresident establishments (NYSED Office of the Professions, Article 137)**
  - https://www.op.nysed.gov/professions/pharmacist/laws-rules-regulations/article-137
  - _Statutory text read 2026-07-16 via NYSED OP; no inline effective date shown_
- **8 NYCRR §63.6 — Registration and operation of New York establishments (NYSED Office of the Professions, Commissioner's Regulations, Part 63)**
  - https://www.op.nysed.gov/professions/pharmacist/laws-rules-regulations/part-63
  - _Regulatory text read 2026-07-20 via NYSED OP (Part 63 accordion body); no inline effective date shown. Confirms the Internet/website drug-retail-price-list disclosure mandate → `ecommerce.website`._
- **U.S. Pharmacopeia — Compounding Standards (USP 795/797)**
  - https://www.usp.org/compounding
  - _Checked 2026-07-15 (federal framework; confirm state adoption)_
- **U.S. FDA — Human Drug Compounding (503A/503B)**
  - https://www.fda.gov/drugs/guidance-compliance-regulatory-information/human-drug-compounding
  - _FDA content current 2026-06-15 (checked 2026-07-15; confirm state overlay)_

## Verified requirements — exact citations

| Field | Citation / Source | Deep link |
|---|---|---|
| IMLC compact | Interstate Medical Licensure Compact Commission — Participating States / Compact State Map | https://imlcc.com/participating-states/ |
| Controlled sub. via telehealth | DEA — Diversion Control Division (Telemedicine) | https://www.deadiversion.usdoj.gov/Telemedicine.html |
| Nonresident pharmacy permit | New York Education Law §6808-b — Registration of nonresident establishments (NYSED Office of the Professions, Article 137) | https://www.op.nysed.gov/professions/pharmacist/laws-rules-regulations/article-137 |
| USP 795/797 standards | U.S. Pharmacopeia — Compounding Standards (USP 795/797) | https://www.usp.org/compounding |
| 503A/503B framework | U.S. FDA — Human Drug Compounding (503A/503B) | https://www.fda.gov/drugs/guidance-compliance-regulatory-information/human-drug-compounding |

## Fields still "Needs legal review" (unsourced)

- Full medical license  (`provider.fullLicense`)
- Telehealth registration  (`provider.telehealthReg`)
- Synchronous video  (`modality.video`)
- Audio-only  (`modality.audioOnly`)
- Asynchronous / store-forward  (`modality.async`)
- In-person exam to establish  (`relationship.inPerson`)
- Informed consent  (`relationship.consent`)
- In-person exam before Rx  (`prescribing.inPersonRx`)
- PDMP query mandatory  (`prescribing.pdmp`)
- Controlled-sub. dispensing limits  (`pharmacy.csDispense`)
- Pharmacist-in-charge nuance  (`pharmacy.pic`)
- State compounding permit  (`compounding.stateReg`)
- Online pharmacy licensure  (`ecommerce.onlinePharmacy`)
- DTC platform restrictions  (`ecommerce.dtc`)

## Unclear questions / open items

- MAJOR ACCESS GAP (re-confirmed 2026-07-20): nysenate.gov (Cloudflare "Just a moment…"), public.leginfo.state.ny.us (CDP navigate timeout), health.ny.gov + regs.health.ny.gov (403 CloudFront/Forbidden) all STILL unreachable this environment. legislation.nysenate.gov OpenLegislation API responds but requires an API key (email signup — can't self-serve). Only NYSED Office of the Professions (op.nysed.gov: Article 137 statute + Part 63 regulations) is reachable, so verification is limited to the pharmacy-side fields it covers.
- relationship.consent + telehealth practice standards: target is Pub. Health Law Art. 29-G (§2999-cc et seq.) — source blocked, NOT verified.
- PDMP / I-STOP: target is Pub. Health Law §3343-a (PMP Registry consultation) — source blocked, NOT verified.
- prescribing.inPersonRx: NY controlled-substance law + federal Ryan Haight/DEA — no NY primary source retrieved.
- compounding.stateReg + all e-commerce: not retrieved (would be Educ. Law Art. 137 + 8 NYCRR Part 63) — NOT verified.
- Only §6808-b (nonresident establishment registration) confirmed, via NYSED OP.

## Items needing pharmacist / attorney review

- [ ] EVERYTHING except §6808-b — re-run from an environment that can reach nysenate.gov / leginfo
- [ ] §2999-cc telehealth consent + standards
- [ ] §3343-a I-STOP PDMP
- [ ] compounding rules (8 NYCRR Part 63)
- [ ] all e-commerce fields

---

## Update 2026-07-21 — gap-fill pass (6 → 11 verified)

nysenate.gov is Cloudflare-blocked live, but the statute pages ARE recoverable via **Internet Archive id_ captures** (`web.archive.org/web/YYYYid_/https://www.nysenate.gov/legislation/laws/PBH/3343-A`). op.nysed.gov used live for the Education Law / Board rules.

Newly verified this pass:
- **prescribing.pdmp — GREEN (big one).** I-STOP **PHL §3343-a(a)**: "Every practitioner **shall consult** the prescription monitoring program registry **prior to prescribing or dispensing** any controlled substance listed on schedule II, III or IV." Broad mandatory consult before every Sch II-IV Rx — one of the strongest PDMP mandates in the country. (Duty excludes veterinarians + certain dispensing.)
- **fullLicense** Ed. Law §6522; **nonresident** §6808-b (incl. internet pharmacies; NB eff. until 5/22/2026 — stacked version); **csDispense** §6810; **pic** §6808 ("immediate supervision and management of a licensed pharmacist"); **onlinePharmacy** subsumed in §6808-b.

Corrections to earlier hypotheses: nonresident is **§6808-b** (not §6808(6)); **8 NYCRR Part 29 has NO internet/questionnaire ban** (read §§29.1/29.2/29.4 verbatim — general misconduct only).

Still red — and these are GENUINE gaps, not access failures: **New York has NO standalone telehealth practice-standard statute.** Modality (video/audio/async), relationship.inPerson, and consent live only in the **insurance-parity law PHL §2999-cc**, which is EXCLUDED per the project's insurance-vs-practice rule. So provider.telehealthReg (§6526 exemptions only), all modality fields, relationship.inPerson/consent, prescribing.inPersonRx, compounding (no USP-by-number in 8 NYCRR Part 63), ecommerce.website, and ecommerce.dtc remain red. NY will stay ~11/20 until/unless a practice-standard modality source outside the insurance title is identified.

**Lesson banked:** nysenate.gov statute text is reachable via Wayback id_ even though the live site is Cloudflare-blocked — same trick as HI/OK.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — gap-fill attempted, NO change (stays 11/20)

Re-read **8 NYCRR Part 63** live on the reachable op.nysed.gov: it carries NO USP-by-number compounding-standards adoption (only CE / licensing / registration / internship), so **compounding.stateReg stays red**. Confirmed the note's structural conclusion: **New York has no standalone telehealth PRACTICE-standard statute** — modality (video/audio/async), relationship.inPerson, and relationship.consent live only in the insurance-parity law **PHL §2999-cc**, EXCLUDED per the project's insurance-vs-practice rule. provider.telehealthReg (§6526 exemptions only), prescribing.inPersonRx, and ecommerce.website/dtc likewise have no non-insurance practice-standard primary source. **NY's remaining reds are genuine statutory gaps, not access failures** — it will stay ~11/20 unless a practice-standard modality source outside the insurance title is found.
