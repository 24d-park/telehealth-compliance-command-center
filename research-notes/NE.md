# Nebraska — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Primary host:** nebraskalegislature.gov (Nebraska Revised Statutes — official Unicameral site; clean, deep-linkable by `?statute=NN-NNNN`, body via console).
**Fields verified:** 8 (+ 2 federal defaults) → 13 ver / 7 rev.

## KEY SCOPE FLAG (read before relying on the telehealth fields)
The **entire Nebraska Telehealth Act (§§71-8501–71-8512) is MEDICAID-FRAMED.** §71-8503(2) defines "Health care practitioner" as **"a Nebraska medicaid-enrolled provider who is licensed, registered, or certified to practice in this state."** §71-8506 is expressly titled *"Medical assistance program; reimbursement; requirements"* and its "in-person shall not be required" clause is scoped "under the medical assistance program." So the Act's consent + modality + no-in-person rules are a Medicaid reimbursement framework, **not** a general practice-standards code. Every NE Telehealth-Act note discloses this. A general-practice telehealth standard, if one exists, would live in Board of Medicine rules (Title 172 NAC), not retrieved this pass.

## VERIFIED (statute text read verbatim)
- **relationship.consent** — §71-8505(1) "shall ensure ... written information is provided"; (2) patient "shall sign a statement ... or give verbal consent." MANDATORY; emergency exception (4). **Amended Laws 2024 LB1215 §38.**
- **modality.video** — §71-8503(3)(a) synchronous electronic exchange; §71-8506(3) "two-way, real-time, interactive communications."
- **modality.async** — §71-8503(3)(b)(ii) store-and-forward.
- **modality.audioOnly** — §71-8503(3)(c): audio-only is telehealth **ONLY** for established-patient behavioral-health or crisis management "as allowed by federal law." EXCLUDED for general medical care.
- **relationship.inPerson** — §71-8506(1) "in-person contact ... shall not be required" (Medicaid-scoped, see flag).
- **pharmacy.nonresident** / **ecommerce.onlinePharmacy** — §71-2407(1) mail service pharmacy outside NE "shall obtain a mail service pharmacy license" before shipping into NE (Mail Service Pharmacy Licensure Act; home-state license + SOS agent + full-time responsible pharmacist).
- **pharmacy.csDispense** — §28-414 Schedule II: no dispensing without an authorized prescription; no refills; 6-month fill limit; EPCS per 21 U.S.C. 801.
- **compounding.stateReg** — §38-2867.01(1): compound "in compliance with the standards of chapters 795 and 797 of The United States Pharmacopeia ... as such chapters existed on January 1, 2023." **USP 795 & 797 adopted BY NUMBER, frozen date; USP 800 NOT by number.** Amended Laws 2023 LB227 §55.

## LEFT "NEEDS LEGAL REVIEW" (honest reds)
- **prescribing.pdmp** — §71-2454: reporting is MANDATORY ("shall be reported ... daily") but prescriber access is PERMISSIVE — "(2)(c) Allow all prescribers or dispensers ... to access the system." No "shall review before prescribing." **VOLUNTARY query → red.**
- **provider.telehealthReg** — no separate out-of-state telehealth registration; full NE licensure is the pathway.
- **prescribing.inPersonRx** — no state CS in-person mandate located (§28-414 / §71-2478 impose none); federal Ryan Haight controls.
- **provider.fullLicense** — left as seed red: the Act's license hook is Medicaid-enrollment-scoped; a clean general-practice full-license telehealth statute was not isolated (Uniform Credentialing Act §38-121 governs licensure generally but not telehealth-specific).
- **ecommerce.website**, **ecommerce.dtc** — no statute located; questionnaire ban + general community-pharmacy PIC likely in Title 172 NAC (not retrieved).

## FOLLOW-UP
- Title 172 NAC (DHHS regulations) for the general community-pharmacy PIC rule, questionnaire/DTC ban, and any Board of Medicine telehealth practice standard (would let fullLicense/dtc/pic go green outside the Medicaid frame).
- Monitor: §71-2454.01 repealed operative 7/1/2026 (LB905); §38-2850 amended operative 7/18/2026 (LB912).


## UPDATE 2026-07-22 (sweep) — +2 fields (13 -> 15/20)

Read verbatim on nebraskalegislature.gov:
- **provider.fullLicense (wired):** Neb. Rev. Stat. §38-121(1)(y) — "No individual shall engage in the following practices unless such individual has obtained a credential under the Uniform Credentialing Act: ... (y) Medicine and surgery." NE regulates at the patient's location, so a NE license is required to treat NE patients via telehealth. [ne_38121]
- **provider.telehealthReg (wired):** Chapter 38 (incl. Telehealth Act definitions) creates NO separate telehealth registration — practice via telehealth uses the same underlying UCA credential. [ne_38121]

Still red (5): prescribing.inPersonRx, prescribing.pdmp (§71-2454 is a dispenser-REPORTING mandate that only "allow[s]" prescriber access — NOT a mandatory query, so left red honestly), pharmacy.pic, ecommerce.website, ecommerce.dtc.
