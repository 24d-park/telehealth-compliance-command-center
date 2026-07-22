# Research Note — Pennsylvania (PA)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 14 / 20  ·  **Needs legal review:** 6 / 20
- **Method:** Primary sources only, read directly in-browser on palegis.us (unconsolidated statutes) and pacodeandbulletin.gov (49 Pa. Code); text confirmed verbatim. Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; every link deep-links to the specific document)

- **Medical Practice Act of 1985 §10 (63 P.S. §422.10) — Unauthorized practice** (State Board of Medicine)
  - https://www.palegis.us/statutes/unconsolidated/law-information/view-statute?txtType=HTM&SessYr=1985&ActNum=0112.&SessInd=0
- **Act 42 of 2024 — Telemedicine (40 Pa.C.S. Ch. 91; INSURANCE title)** (PA General Assembly)
  - https://www.palegis.us/statutes/unconsolidated/law-information/view-statute?txtType=HTM&SessYr=2024&ActNum=0042.&SessInd=0 — Approved July 3, 2024, eff. in 90 days
- **ABC-MAP Act §8 (Act 191 of 2014; 35 P.S. §872.1 et seq.) — prescriber PDMP query** (PA Dept. of Health / ABC-MAP)
  - https://www.palegis.us/statutes/unconsolidated/law-information/view-statute?txtType=HTM&SessYr=2014&ActNum=0191.&SessInd=0 — §8(a) amended Nov. 2, 2016, No.124
- **Pharmacy Act §4.1 (63 P.S. §390-4.1) — Nonresident Pharmacies** (State Board of Pharmacy)
  - https://www.palegis.us/statutes/unconsolidated/law-information/view-statute?txtType=HTM&SessYr=1961&ActNum=0699.&SessInd=0 — §4.1 added Oct. 7, 2015, No.43
- **49 Pa. Code §27.11 — Pharmacy permit and pharmacist manager** (State Board of Pharmacy)
  - https://www.pacodeandbulletin.gov/Display/pacode?file=/secure/pacode/data/049/chapter27/s27.11.html — amended June 27, 2025, eff. June 28, 2025, 55 Pa.B. 4335
- **49 Pa. Code §27.18 — Standards of practice (CS dispensing)** (State Board of Pharmacy)
  - https://www.pacodeandbulletin.gov/Display/pacode?file=/secure/pacode/data/049/chapter27/s27.18.html
- **49 Pa. Code §27.601 — Compounding of preparations (FDCA §503A + USP)** (State Board of Pharmacy)
  - https://www.pacodeandbulletin.gov/Display/pacode?file=/secure/pacode/data/049/chapter27/s27.601.html — adopted June 21, 2019, eff. June 22, 2019, 49 Pa.B. 3210

## Verified requirements (10 state-sourced + federal-framework inheritance)

PA medical license required to practice (Med Practice Act §10); synchronous / audio-only /
asynchronous telemedicine defined (40 Pa.C.S. §4802, Act 42 of 2024 — **coverage/definition
statute in the Insurance title, NOT a practice-standards act; flagged as such**); ABC-MAP PDMP
query mandatory for first CS, on suspicion, and each opioid/benzo (ABC-MAP §8(a)); nonresident
pharmacy biennial registration (Pharmacy Act §4.1); Sch II must be written + DEA number
(49 Pa. Code §27.18); pharmacist-manager/PIC (49 Pa. Code §27.11); USP compounding chapters +
FDCA §503A adopted by rule (49 Pa. Code §27.601).

## Fields still "Needs legal review" (unsourced)

- Telehealth registration (`provider.telehealthReg`) — Act 42 creates no provider telehealth registry.
- In-person exam to establish (`relationship.inPerson`), Informed consent (`relationship.consent`),
  In-person exam before Rx (`prescribing.inPersonRx`) — these most likely live in State Board of
  Medicine standards-of-practice regs (49 Pa. Code Ch. 16/25), which could not be fully opened.
  Left red; no requirement asserted without reading the actual rule.
- Website/disclosure rules (`ecommerce.website`) — no on-website display mandate located (§4.1(b)
  requires the toll-free number on the drug LABEL, not the website).
- DTC platform restrictions (`ecommerce.dtc`) — no questionnaire-only prohibition located in statute.

## Notes / open items

- palegis.us renders statutes inside an IFRAME; read via `window.frames[0].document.body.textContent`.
  The section link list is a TOC — take the LAST occurrence of a heading to reach the body text.
- Act 42 of 2024 is the newest PA telemedicine law but it is an INSURANCE-title coverage statute;
  clinical practice standards for telehealth are NOT in Act 42. Follow-up pass on 49 Pa. Code Ch.
  16/25 (Board of Medicine) is needed for the relationship/prescribing fields.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.
