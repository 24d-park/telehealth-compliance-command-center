# Research Note — Virginia (VA)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 15 / 20  ·  **Needs legal review:** 5 / 20
- **Method:** Primary sources only, read directly in-browser on law.lis.virginia.gov (Code of Virginia, Titles 54.1 & 38.2). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; Code of Virginia)

- **Va. Code §54.1-3303 — Prescriptions/therapeutic purposes; telemedicine bona fide relationship** — https://law.lis.virginia.gov/vacode/54.1-3303/
- **Va. Code §54.1-2522.1 — Requirements of practitioners (PMP query)** — https://law.lis.virginia.gov/vacode/54.1-2522.1/
- **Va. Code §54.1-3434.1 — Nonresident pharmacies to register (incl. Internet/VIPPS)** — https://law.lis.virginia.gov/vacode/54.1-3434.1/
- **Va. Code §54.1-3434 — Permit to conduct pharmacy (pharmacist-in-charge)** — https://law.lis.virginia.gov/vacode/54.1-3434/
- **Va. Code §54.1-3410.2 — Compounding; USP-NF standards** — https://law.lis.virginia.gov/vacode/54.1-3410.2/

## Verified requirements (11 state-sourced + federal-framework inheritance)

The anchor is **§54.1-3303(B)** — a prescriber may establish a bona fide practitioner-patient
relationship to prescribe Sch II–VI via face-to-face real-time OR store-and-forward telemedicine,
subject to nine conditions, requires active VA licensure (backs fullLicense, modality.video/async,
relationship.inPerson, prescribing.inPersonRx). PMP query when initiating opioids >7 consecutive days
(§54.1-2522.1). Nonresident registration for Sch II-VI shippers; internet pharmacies dispensing >50%
internet-solicited volume need NABP/VIPPS certification (§54.1-3434.1). Pharmacist-in-charge signs
permit application (§54.1-3434). Compounding beyond-use dates per USP-NF (§54.1-3410.2).

## Fields still "Needs legal review"

- relationship.consent — only Board of Medicine Guidance Document 85-12 addresses it; that is
  guidance, NOT binding law, so it was correctly excluded.
- modality.audioOnly — the only statutory treatment (§38.2-3418.16) is an insurance-COVERAGE exclusion
  ("does not include audio-only telephone"), not a clinical practice rule; left red to avoid overreach.
- provider.telehealthReg — no broad standalone registration; §54.1-2901 has only a narrow
  continuity-of-care exemption (existing patient, prior in-person exam within a year, up to one year).
- ecommerce.website, ecommerce.dtc — would live in 18 VAC 110 board rules (not read).

## Notes

- §54.1-2522.1 has a superseding version **effective July 1, 2027** that changes the PMP trigger to a
  benzodiazepine/opiate supply anticipated to last more than 90 consecutive days. Current field cites
  the "effective until July 1, 2027" version (>7-day opioid trigger). Re-check after that date.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — +1 field (15 -> 16/20)

- **provider.telehealthReg (now wired):** Va. Code §54.1-2901 read verbatim — VA has NO broad standalone telehealth registration. The only telemedicine carve-out from full licensure is a narrow out-of-state behavioral-health continuity-of-care exemption (pre-existing patient + in-person exam within the prior year, capped at one year). Full VA license is the pathway (§54.1-3303). Same verified "no separate registration" pattern as OH. [src: va_2901]

Remaining red (4) are genuine nulls / rule-level: relationship.consent (only non-binding Board Guidance 85-12), modality.audioOnly (only insurance-coverage exclusion §38.2-3418.16, excluded per project rule), ecommerce.website/dtc (18 VAC 110 board rules — 18VAC110-20-15 is repealed; internet-pharmacy duties would be elsewhere in 18 VAC 110, not read).
