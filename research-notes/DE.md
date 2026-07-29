# Delaware — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 12 (+ 2 federal defaults) → 16 ver / 4 rev.

## STRUCTURAL CATCH (critical)
***The old telemedicine statute 24 Del. C. §1769D was REPEALED effective July 1, 2021 (83 Del. Laws c.52, §6).*** The current telehealth PRACTICE-STANDARDS law is **24 Del. C. ch. 60 (§§6001-6005)**. Any tracker still citing §1769D is outdated. NOT the insurance parity law (18 Del. C. §3370/3571R, out of scope). Pharmacy = 24 Del. C. ch. 25 + 24 DE Admin Code 2500. Controlled substances/PMP = 16 Del. C. ch. 47 (incl. §4798 PMP + §§4741-4745 Safe Internet Pharmacy Act).

## SOURCING
delcode.delaware.gov chapter index pages (e.g. /title24/c060/index.html) render the full chapter text — extract via document.body.innerText. regulations.delaware.gov (Admin Code 2500) is JS-rendered but returns full text via innerText (occasionally needs a re-navigate if it loads empty once).

## VERIFIED
- **provider.fullLicense** — §6001(1)/§6002(a): distant-site provider must be "legally allowed to practice in Delaware."
- **provider.telehealthReg — GENUINE PATHWAY** — §6002(c)-(d): a provider licensed in a non-compact state "may only provide telehealth ... if the health-care provider obtains an interstate telehealth registration from the Division of Professional Regulation." (Like VT, one of the few states with a real out-of-state telehealth registration.)
- **modality.video** — §6001(6)/§6004(a)(3) real-time 2-way audio-visual.
- **modality.audioOnly** — §6001(6): permitted ONLY as a broadband-unavailable fallback ("audio-only conversations, if the patient is not able to access the appropriate broadband service"). Conditional.
- **modality.async** — §6001(4)/§6003(b) store-and-forward recognized.
- **relationship.inPerson** — §6003(a): relationship "may be established either in-person or through telehealth"; §6004(a) offers multiple satisfaction routes. No prior in-person.
- **relationship.consent** — §6003(a)(3) MANDATORY: relationship "must include ... informed consent regarding the use of telemedicine technologies."
- **ecommerce.dtc** — §6003(c): "prohibited from issuing prescriptions solely in response to an internet questionnaire, an internet consult, or a telephone consult" + 16 Del. C. §4744(b)(1) (Safe Internet Pharmacy Act) as a second basis.
- **pharmacy.nonresident** — 24 Del. C. §2535: out-of-state pharmacy delivering into DE "must obtain a nonresident pharmacy license from the Board."
- **pharmacy.pic** — §2528(a)(2) + Admin Code 2500 §3.1: one PIC per pharmacy, one pharmacy per PIC.
- **compounding.stateReg** — Admin Code 2500 §10.0: "shall adhere to ... USP Chapters 795 (USP 795) and 797 (USP 797) and any updates" + USP 800 compliance. USP 795/797/800 by number (dynamic "current edition").
- **ecommerce.onlinePharmacy** — 16 Del. C. §§4741-4745 Safe Internet Pharmacy Act: unlicensed internet pharmacy may not dispense to a DE patient (§4744(a)) → effectively requires a Board license.

## LEFT "NEEDS LEGAL REVIEW"
- **prescribing.pdmp** — §4798(f) is CONDITIONAL: prescriber "shall obtain, before writing a prescription for a controlled substance ... WHEN the prescriber has a reasonable belief that the patient may be seeking the controlled substance ... for any reason other than the treatment of an existing medical condition." Not a blanket before-every-Rx mandate → left red (consistent with how conditional PDMPs are treated). (Independently confirmed the "reasonable belief" trigger — the subagent was correct.)
- **prescribing.inPersonRx** — no state CS-before-telehealth in-person mandate; federal DEA/Ryan Haight controls.
- **ecommerce.website** — no VIPPS/license website-display mandate (§4744(b) only requires non-shipping rogue sites to disclaim DE shipping).

## PENDING-LAW FLAG
- **85 Del. Laws c.49** recodifies Pharmacy ch. 25 subchapters IV/V (nonresident §2535, PIC §2528) **effective June 30, 2026** — re-verify those section numbers after that date. §4798 PMP was amended by 85 Del. Laws c.19 (2025).


## UPDATE 2026-07-29 — final-research wave 4, +1 field (16 -> 17/20)
Parent-worked in-browser on delcode.delaware.gov.
- **prescribing.inPersonRx** — 24 Del. C. §6004(a): a telehealth provider must "prior to diagnosis and
  treatment, do at least 1 of the following: (1) Provide an appropriate examination in-person. (2) Require
  another Delaware-licensed health-care provider be present ... (3) Make a diagnosis using audio or visual
  communication. (4) Meet the standard of service required by applicable professional societies ...". In-person
  is ONE of four options — a diagnosis by audio/visual (option 3) satisfies it, so NO mandatory in-person exam
  before prescribing. (§6003(c) separately bars questionnaire-only prescribing — already wired to dtc.) Reused
  de_telehealth (Ch. 60).
### Structural note
- 24 Del. C. §1769D (old Telemedicine section) was REPEALED eff. 7/1/2021 and replaced by 24 Del. C. Chapter 60
  ("Provisions Applicable to Telehealth and Telemedicine", §§6001-6005). All DE telehealth fields cite Ch. 60.
### Still red (pending subagent verification this wave)
- prescribing.pdmp (16 Del. C. §4798 — conditional "reasonable belief" trigger, likely a hold),
  pharmacy.csDispense (16 Del. C. §4739 CS Act), ecommerce.website (likely genuine absence).
