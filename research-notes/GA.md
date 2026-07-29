# Research Note — Georgia (GA)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 14 / 20  ·  **Needs legal review:** 6 / 20
- **Method:** Primary sources only. Read directly in-browser on rules.sos.ga.gov (official GA Secretary of State administrative code) and dph.georgia.gov (PDMP agency). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; official GA .gov)

- **Ga. Comp. R. & Regs. r. 360-3-.07 — Practice Through Electronic or Other Such Means** (Composite Medical Board)
  - https://rules.sos.ga.gov/gac/360-3-.07 — latest version eff. Sept. 28, 2020 (current through R&R filed June 30, 2026)
- **Georgia PDMP** (Dept. of Public Health, implementing O.C.G.A. §16-13-63.1 / HB 249 of 2017)
  - https://dph.georgia.gov/pdmp — mandatory check eff. July 1, 2018
- **Ga. Comp. R. & Regs. r. 480-6-.02 — Nonresident Pharmacy Permit** (Board of Pharmacy)
  - https://rules.sos.ga.gov/gac/480-6-.02 — operative provision eff. April 1, 2015
- **Ga. Comp. R. & Regs. r. 480-6-.01 — Pharmacy Licenses (direct-charge pharmacist)** (Board of Pharmacy)
  - https://rules.sos.ga.gov/gac/480-6-.01 — last amended eff. Aug. 13, 2024
- **Ga. Comp. R. & Regs. r. 480-11-.02 — Compounded Drug Preparations (USP 795/797)** (Board of Pharmacy)
  - https://rules.sos.ga.gov/gac/480-11-.02

## Verified requirements (10 state-sourced + federal-framework inheritance)

Full GA license for telemedicine (360-3-.07(a)(1) "Georgia licensed practitioners"); audio-only/
telephonic care permitted in an established relationship (360-3-.07(b)); no strict in-person-first
mandate but annual in-person effort required (360-3-.07(a)(3),(8)); CS-for-pain via telemedicine
restricted (360-3-.07(c)); PDMP check before Sch II opiates/cocaine-derivatives/benzos (DPH/HB 249);
nonresident pharmacy permit for out-of-state shippers incl. internet (480-6-.02, O.C.G.A. §26-4-114.1);
CS dispensing per O.C.G.A. T.16 Ch.13 & T.26 Ch.4 (480-11-.02(1)(a)); pharmacist in direct charge
(480-6-.01(2)); USP 795/797 compounding adopted by rule (480-11-.02).

## Fields still "Needs legal review"

- modality.video, modality.async — the telemedicine rule contemplates but does not cleanly define/
  require video, and does not expressly address store-and-forward.
- relationship.consent — disclosure duties exist (360-3-.07(a)(6)-(7)) but no "informed consent for
  telehealth" mandate; provider.telehealthReg; ecommerce.website, ecommerce.dtc.

## Notes / IMPORTANT SOURCING CAVEAT

- **Georgia O.C.G.A. statute text was NOT reachable from a permitted primary host this session:**
  legis.ga.gov has no working statute deep-links (its viewer only searches bills); the statute
  hyperlinks on rules.sos.ga.gov redirect to public.fastcase.com (a prohibited commercial aggregator);
  and LexisNexis's official Georgia Code (advance.lexis.com) needs a paid session. GA fields are
  therefore sourced to the official SOS administrative code (rules.sos.ga.gov) and the DPH PDMP agency
  page — both genuine .gov primary sources — NOT to unread O.C.G.A. text. Statute numbers (e.g.
  §26-4-114.1, §16-13-63.1) appear only where the readable rule/agency page itself cited them.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-29 — final-research wave 1, +1 field (14 -> 15/20)
Subagent lead, parent-verified verbatim on rules.sos.ga.gov.
- **provider.telehealthReg** — POSITIVE requirement (NOT verified-null). Ga. Comp. R. & Regs. r. 360-2-.17
  ("Requirements for Telemedicine Licensure", eff. Jan. 24, 2021): GA issues a distinct "Telemedicine License"
  to an out-of-state physician who holds "a full and unrestricted license to practice medicine in another
  state" (subd. 1); "limited to the practice of telemedicine and shall not be used to practice medicine
  physically in this state" (subd. 2). A genuine out-of-state telehealth licensure pathway like NV/OR/NM/FL.
  New source ga_360217. Authority O.C.G.A. 33-24-56.4, 43-34-31.1.
### Confirmed HOLDS (genuine absences in Rule 360-3-.07 — no change)
- modality.async — no store-and-forward/asynchronous definition in the telemedicine rule.
- relationship.consent — Rule 360-3-.07 contains NO express informed-consent clause (only disclosure/records
  duties in (6)-(7)). A general Chapter 360-14 "Informed Consent" exists but is not telemedicine-specific.
- modality.video — technology-neutral functional-equivalence (360-3-.07(a)(3)(d)), no express video mandate.
- ecommerce.website — genuine absence.
