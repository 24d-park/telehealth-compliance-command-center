# Research Note — North Carolina (NC)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 9 / 20  ·  **Needs legal review:** 11 / 20
- **Method:** Primary sources only, read directly in-browser on ncleg.gov (NC General Statutes, Chapter 90). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; NC General Statutes)

- **N.C. Gen. Stat. §90-18 — Practicing without license; penalties** — https://www.ncleg.gov/EnactedLegislation/Statutes/HTML/BySection/Chapter_90/GS_90-18.html
- **N.C. Gen. Stat. §90-113.74C — CSRS practitioner use (STOP Act)** — https://www.ncleg.gov/EnactedLegislation/Statutes/HTML/BySection/Chapter_90/GS_90-113.74C.html
- **N.C. Gen. Stat. §90-85.21A — Out-of-state operations (nonresident pharmacy)** — https://www.ncleg.gov/EnactedLegislation/Statutes/HTML/BySection/Chapter_90/GS_90-85.21A.html
- **N.C. Gen. Stat. §90-106 — Prescriptions and labeling (CS)** — https://www.ncleg.gov/EnactedLegislation/Statutes/HTML/BySection/Chapter_90/GS_90-106.html
- **N.C. Gen. Stat. §90-85.21 — Pharmacy permit (pharmacist-manager)** — https://www.ncleg.gov/EnactedLegislation/Statutes/HTML/BySection/Chapter_90/GS_90-85.21.html

## Verified requirements (5 state-sourced + federal-framework inheritance)

Full NC license to practice medicine (§90-18); CSRS/PDMP review before initial targeted-CS Rx and
every 3 months (§90-113.74C STOP Act); nonresident pharmacy annual registration (§90-85.21A);
mandatory e-prescribing of targeted CS + copy/refill limits (§90-106); pharmacist-manager on the
pharmacy permit (§90-85.21).

## Fields still "Needs legal review" (this is the correct, honest outcome — see notes)

All modality fields (video/audio/async), relationship.inPerson, relationship.consent,
prescribing.inPersonRx, provider.telehealthReg, compounding.stateReg, and all e-commerce fields.

## Notes / why NC is intentionally thin

- **NC's telehealth practice standards live almost entirely in NC Medical Board POSITION STATEMENTS,
  which are NOT primary law** — they were deliberately excluded per the research standard. NC's
  General Statutes contain no telehealth-specific practice carve-out; general §90-18 licensure applies.
- **The NC Administrative Code host (reports.oah.state.nc.us, Title 21 Ch. 46 Board of Pharmacy rules
  — including USP-compounding adoption) was completely unreachable this session** (ERR_BLOCKED_BY_CLIENT
  / CDP timeout across multiple attempts, both http and https). Rule-only fields were therefore left
  red rather than asserted from an unread rule.
- Compounding: §90-85.3(c) only *defines* "compounding"; the USP 795/797 adoption itself is in 21 NCAC
  46 (unreachable), so compounding.stateReg stays red.
- NC's 9 verified (5 state-sourced + 4 federal-inherited) reflects genuinely sparse codified NC
  telehealth law, not a research gap. Re-run 21 NCAC 46 from an environment that can reach the OAH host.

---

## Update 2026-07-21 — gap-fill pass (9 → 16 verified)

Statutes read verbatim on ncleg.gov; NC Medical Board Position Statement 5.1.4 (Telemedicine) read on ncmedboard.org. **STRUCTURAL: NC has NO comprehensive telehealth statute** — the practice standard is NCMB Position Statement 5.1.4 (adopted 2010, amended Mar 2024). Modality/consent/relationship/DTC fields are therefore BOARD-POLICY-level, flagged as such in the tracker notes (an official Board issuance, but softer than a codified rule).

Newly verified:
- **prescribing.pdmp — GREEN.** STOP Act §90-113.74C: "a practitioner shall review the information in the controlled substances reporting system ... for the 12-month period preceding the initial prescription" + "every subsequent three-month period." Mandatory targeted-CS review.
- Statute: **fullLicense** §90-9.1; **nonresident** §90-85.21A ("shall annually register with the Board"); **csDispense** §90-106(a1) (e-prescribe mandate for targeted CS); **pic** §90-85.21(a) (pharmacist-manager); **onlinePharmacy** subsumed §90-85.21A.
- Board policy (PS 5.1.4): **video** endorsed, **async** permitted, **relationship.inPerson** not required, **consent** documentation "should," **ecommerce.dtc** ban ("treatment based solely on static online questionnaires ... are not acceptable").

Still red: telehealthReg (no registry; §90-18(c)(11) exceptions only), modality.audioOnly (standard-of-care gated), prescribing.inPersonRx (Board policy + federal DEA, no state statute), **compounding.stateReg (21 NCAC 46 — reports.oah.state.nc.us BLOCKED/ERR_BLOCKED_BY_CLIENT this session)**, ecommerce.website. Compounding is the one genuine host-blocked gap — re-run 21 NCAC 46 from an unblocked network.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.
