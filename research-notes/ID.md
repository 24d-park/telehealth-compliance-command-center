# Idaho — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Primary host:** legislature.idaho.gov/statutesrules/idstat/ (Idaho Statutes — clean, deep-link `/TitleNN/TNNCHNN/SECTNN-NNNN/`; body renders in snapshot, though the page footer is verbose).
**Fields verified:** 10 (+ 2 federal defaults) → 14 ver / 6 rev.

## STRUCTURAL KEY
The former "Idaho Telehealth Access Act" is now the **Idaho Virtual Care Access Act**, Idaho Code Title 54 Ch. 57 (§§54-5701–54-5714), rewritten by **2023 ch. 102**, with §54-5705 amended **2025 ch. 93**. It is a **practice-standards** title (not insurance). Pharmacy rules were deregulated and redesignated to **IDAPA 24.36.01** (from 27.01.01) eff. 7/1/2020, under DOPL/Board of Pharmacy.

## VERIFIED (statute text read verbatim on legislature.idaho.gov)
- **provider.fullLicense** — §54-5713(1) "Prior to delivering health care services via virtual care, a provider must obtain a license from the applicable licensing board" + 6 narrow out-of-state exemptions (1)(a)-(f).
- **modality.video / async** — §54-5703(5) technology-neutral "virtual care" umbrella: "video visits," "e-consults," "e-visits," "remote patient monitoring," "synchronous and asynchronous care delivery modalities."
- **relationship.inPerson** — §54-5705 "A provider-patient relationship may be established by use of virtual care technologies." Amended 2025 ch. 93.
- **prescribing.inPersonRx** — §54-5707(1) prescribing allowed via virtual care with established relationship; CS "shall not be a controlled substance unless prescribed in compliance with 21 U.S.C." — defers to federal Ryan Haight, no separate ID in-person mandate. §54-5706 requires documenting clinical history + symptoms.
- **ecommerce.dtc** — §54-5706 "Treatment based solely on a static online questionnaire does not constitute an acceptable standard of care." ("Static online questionnaire" defined §54-5703(4).)
- **pharmacy.nonresident / pharmacy.pic / ecommerce.onlinePharmacy** — §54-1729: all drug/device outlets "doing business in or into Idaho" must be board-registered; nonresident must be licensed/good-standing at home + "have a person in charge"; Nonresident drug outlet certificate. Amended 2025 ch. 93.
- **compounding.stateReg** — IDAPA 24.36.01.700 (eff. 3-28-23): policies developed "in consideration of the applicable provisions of USP Chapter 795 ... USP Chapter 797 ... Chapter 1075 ... Chapter 1160" — USP chapters cited by number as GUIDANCE, not binding wholesale adoption; **USP <800> absent**. (Read via Internet Archive capture of the official adminrules.idaho.gov PDF; live host under a documented outage.)

## LEFT "NEEDS LEGAL REVIEW" (honest reds)
- **prescribing.pdmp** — §37-2726: dispenser reporting mandatory ("shall be filed with the division electronically") but prescriber database access permissive ("may be made available only to ... A practitioner"). No shall-review-before-prescribing → VOLUNTARY.
- **modality.audioOnly** — §54-5703(5) is technology-neutral but does NOT name audio-only telephone; left red rather than infer permission from silence (consistent with SC/OR treatment).
- **provider.telehealthReg** — §54-5713 provides out-of-state licensure EXEMPTIONS, not a separate registration pathway.
- **relationship.consent** — §54-5708 "informed consent ... shall be obtained as required by any applicable law" — conditional (defers to other law), not a freestanding Ch. 57 mandate.
- **ecommerce.website** — no public website/VIPPS display requirement located (consistent with ID's deregulated approach).

## FOLLOW-UP
- Re-open IDAPA 24.36.01 on the live adminrules.idaho.gov once the outage clears, to re-confirm the compounding "in consideration of" language and check for any hardened PIC/nonresident rule detail.


## UPDATE 2026-07-22 (sweep) — +3 fields (14 -> 17/20)

Read verbatim on legislature.idaho.gov (Idaho Virtual Care Access Act, Title 54 Ch. 57):
- **provider.telehealthReg (wired):** §54-5713(1) — "Prior to delivering health care services via virtual care, a provider must obtain a license from the applicable licensing board," with only narrow out-of-state exemptions (temporary-visitor continuity, facility-credentialed, disaster, pre-visit prep, consult/referral). Full Idaho licensure; no separate telehealth registration. [id_virtualcare]
- **relationship.consent (wired):** §54-5708 — "A patient's informed consent for the use of virtual care shall be obtained as required by any applicable law." [id_virtualcare]
- **modality.audioOnly (wired):** §54-5703(5) — "virtual care" is a technology-neutral umbrella ("synchronous and asynchronous ... telemedicine, telehealth, m-health, e-consults, e-visits, video visits, remote patient monitoring, and similar technologies"); audio-only is not excluded, so permitted at the standard of care. [id_virtualcare]

Still red (3): prescribing.pdmp, pharmacy.csDispense, ecommerce.website.
