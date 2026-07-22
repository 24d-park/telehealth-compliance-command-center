# Vermont — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 12 (+ 2 federal defaults) → 14 ver / 6 rev. **The richest telehealth-registration state so far.**

## SOURCING TECHNIQUE
legislature.vermont.gov `/statutes/section/TITLE/CHAP/SECTION` (zero-padded, e.g. `/18/219/09361`). Huge nav menu dominates the snapshot — **extract via `document.body.innerText` and regex for keywords** ('shall query', 'audio-only telephone', 'telehealth registration'). Reliable. NOTE: the OPR / Board of Pharmacy admin-rules site (sos.vermont.gov / CloudFront) returned 403 this session — rule-level pharmacy fields could NOT be reached.

## STRUCTURAL KEY (title discipline is critical here)
- **Telehealth practice standards = 18 V.S.A. Ch. 219** (§9361 telemedicine, §9362 audio-only) + **26 V.S.A. Ch. 56** (§§3052-3061 telehealth licensure/registration) + **26 V.S.A. §1354** (Board of Medical Practice conduct) + **18 V.S.A. Ch. 84A** (VPMS).
- ***INSURANCE (do NOT use for practice standards): 8 V.S.A. §§4098a, 4098b, 4100k.*** §§9361-9362 borrow definitions from 8 V.S.A. §4098a, but the operative practice rules live in Title 18/26.

## VERIFIED (statute text read verbatim)
- **provider.fullLicense** — 18 V.S.A. §9361(b): "a health care provider licensed in this State may prescribe, dispense, or administer drugs ... after having performed an appropriate examination of the patient in person, through telemedicine, or by the use of instrumentation."
- **provider.telehealthReg — GENUINE DUAL PATHWAY (rare)** — 26 V.S.A. §3053(a): an out-of-state provider not otherwise VT-licensed "shall obtain a **telehealth license or telehealth registration** from the Office or the Board." §3054: telehealth license ≈ ≤20 unique VT patients over a 2-yr term (fee 75% of renewal); telehealth registration ≈ ≤120 consecutive days, ≤10 unique patients. Added 2021 No. 107 (Adj. Sess.), **eff. July 1, 2023.**
- **modality.video** — 18 V.S.A. §9361 (defs incorporate 8 V.S.A. §4098a): real-time audiovisual recognized.
- **modality.audioOnly** — 18 V.S.A. §9362(b)(1): "a health care provider may deliver health care services to a patient using **audio-only telephone** if the patient elects to receive the services in this manner and it is clinically appropriate to do so." PERMITTED.
- **modality.async** — 18 V.S.A. §9361: "store-and-forward" defined + recognized (patient right-to-refuse; originating-site consent).
- **relationship.inPerson** — 18 V.S.A. §9361(b): exam "in person, through telemedicine, or by the use of instrumentation" — telemedicine exam suffices.
- **relationship.consent** — 18 V.S.A. §9361(c)(1): "shall obtain and document a patient's oral or written informed consent for the use of telemedicine technology prior to delivering services." MANDATORY.
- **prescribing.pdmp — TARGETED MANDATORY (verb verified)** — 18 V.S.A. §4289(c): "health care providers **shall query** the VPMS ... in the following circumstances: (1) at least annually for patients ... receiving ongoing treatment with an opioid Schedule II, III, or IV controlled substance; (2) when starting a patient on a Schedule II, III, or IV ... for nonpalliative long-term pain therapy of 90 days or more; (3) the first time the provider prescribes an opioid Schedule II, III, or IV ... to treat chronic pain; and (4) prior to writing a re[placement Rx]." A real mandate, but scoped — NOT before every prescription. Registration separately mandatory §4289(b).
- **ecommerce.dtc** — 26 V.S.A. §1354(a)(33)(B): "an electronic, online, or telephonic evaluation by questionnaire is inadequate for the initial evaluation of the patient" (narrow exceptions in (C)).
- **pharmacy.pic** — 26 V.S.A. §2062(b)(3) & §2061(e): license application must identify a "pharmacist ... who shall be the pharmacist in charge of the drug outlet"; retail/institutional "shall be managed by licensed pharmacists."

## LEFT "NEEDS LEGAL REVIEW" (honest reds)
- **prescribing.inPersonRx** — no VT telehealth-specific CS-before-in-person statute; §9361(b) holds prescribing to "the same standards ... as ... traditional settings." DEA federal rules apply.
- **pharmacy.nonresident + ecommerce.onlinePharmacy + compounding.stateReg** — 26 V.S.A. §2061 creates the drug-outlet registration and a "Compounding" license CLASSIFICATION, but the Board "shall establish by rule" (§2061(d)) the nonresident/mail-order criteria + USP-by-number adoption. Those rules live in the **OPR Board of Pharmacy admin rules**, which returned CloudFront-403 this session. Left red rather than assert unread rules.
- **ecommerce.website** — not found in statute.

## FOLLOW-UP
- Retry the OPR / sos.vermont.gov Board of Pharmacy rules (different egress or Wayback) for nonresident/mail-order license, online-pharmacy permit, and USP compounding-by-number → would flip 3 reds green.
- Re-read §§9361-9362 final text for the 2025 No. 11 (eff. 9/1/2025) amendments to confirm no substantive telehealth change.
