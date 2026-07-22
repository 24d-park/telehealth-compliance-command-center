# Alaska — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 11 (+ 2 federal defaults) → 14 ver / 6 rev.

## SOURCING TECHNIQUE
akleg.gov/basis/statutes.asp is a **single-page app** — the address bar only shows a `#section` hash (e.g. `#08.64.364`), and deep links do NOT auto-scroll on fresh load. **Workaround:** type the section number into the in-page SEARCH box and click Display, then read via document.body.innerText. The `#`-hash is the site's own citation format (no static per-section URL exists).

## STRUCTURAL KEY
Telehealth practice standard = **AS 08.64.364** (State Medical Board, Title 8 Business & Professions). ***Confirmed NOT REPEALED*** (adjacent AS 08.64.365 IS a repealed 1976 emergency-circumstances section — don't confuse them). Pharmacy = AS 08.80 + 12 AAC 52. PDMP = AS 17.30.200 (Title 17). All practice-standards titles — NOT insurance Title 21.

## VERIFIED
- **provider.fullLicense** — AS 08.64.360 (unlicensed practice = class A misdemeanor).
- **modality.video + audioOnly + async** — AS 08.64.364(c): the board may not discipline a licensee for "the evaluation, diagnosis, supervision, or treatment of a person through **audio, video, or data communications** when physically separated from the person" (conditions (c)(1)-(3)). ***All three modalities affirmatively named — the subagent was too conservative marking them NOT FOUND. Read the operative (c) clause, not just the definitions.***
- **relationship.inPerson** — AS 08.64.364(c): treatment "when physically separated" allowed if (1) follow-up care available, (2) records offered to PCP, (3) board regs met. No prior in-person.
- **prescribing.inPersonRx** — AS 08.64.364(c)(2): no Rx "in response to an Internet questionnaire or electronic mail message to a person with whom the physician ... does not have a prior physician-patient relationship" + AS 08.64.363 (7-day opioid limit).
- **ecommerce.dtc** — same AS 08.64.364(c)(2) questionnaire/email ban.
- **pharmacy.nonresident** — AS 08.80.159: out-of-state pharmacy shipping into AK "shall (1) obtain a license under AS 08.80.157; (2) appoint an agent for service of process; (3) authorize inspection." (Registration→licensure conversion eff. ~Nov 2023/Jan 2024.)
- **pharmacy.pic** — AS 08.80.330: "Each pharmacy shall have a pharmacist-in-charge."
- **ecommerce.onlinePharmacy** — AS 08.80.030(b)(17): board licenses "Internet-based pharmacies providing services to residents in the state" (+ 12 AAC 52.020(h)). A distinct internet-pharmacy hook.

## LEFT "NEEDS LEGAL REVIEW"
- **prescribing.pdmp** — AS 17.30.200: "Nothing in this section requires or obligates a dispenser or practitioner to access or check the database before dispensing, prescribing, or administering a medication." VOLUNTARY (registration + reporting mandatory only). Verbatim-confirmed.
- **provider.telehealthReg** — no separate pathway; full AK license only.
- **relationship.consent** — the only "shall obtain written informed consent" is abortion-specific (12 AAC 40.070 / AS 18.16.060); no general telehealth consent mandate.
- **compounding.stateReg** — ***distinctive: AK does NOT adopt USP by number.*** 12 AAC 52.440 incorporates the Board's own "Compounding Practices" pamphlet dated Feb 2008; 12 AAC 52.430 uses "accepted standard of care." Only a general "current USP" reference elsewhere for unit-dose storage.
- **pharmacy.csDispense** — AS 17.30.200(b)/AS 17.30.020 (reporting).
- **ecommerce.website** — not found.

## FOLLOW-UP
- 12 AAC 40.943 adopts the FSMB Model Policy (2014) + AMA Report 7 by reference as telemedicine standards — could add nuance to modality/standard-of-care if the AAC is later extractable.
