# New Mexico — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 13 (+ 2 federal defaults) → 17 ver / 3 rev.

## SOURCING NOTE (important)
The NM **statute** host `nmonesource.com` (NMSA 1978 + NMAC) was **HTTP-403 blocked all session** — statute text could not be independently read. All NM fields are therefore sourced to the official **NM Administrative Code (NMAC)** at `srca.nm.gov` (NM Commission of Public Records), which is itself a primary legal source. Statutory cites (§61-6, §61-11, §30-31) appear only **as referenced within the retrieved rules**, not as independently opened statute pages. NMAC pages render via console `document.body.innerText`; note the whitespace-collapse trick can miss hits — use raw `innerText` + `indexOf`/`substring`, NOT `.replace(/\s+/g,' ')`, because subsection bodies contain wide gaps that a collapsed slice can skip.

## VERIFIED (NMAC rule text read verbatim)
### NM Medical Board (Title 16 Chapter 10)
- **provider.fullLicense** — 16.10.2.8(B) "Medical: An unrestricted license to practice medicine and surgery." Eff. 7/7/2023.
- **provider.telehealthReg** — 16.10.2.8(C) + **16.10.2.11 dedicated "Telemedicine" limited license** "that allows a physician located outside New Mexico to practice medicine on patients located in New Mexico" (same docs as expedited license; no interview unless discrepancy). A genuine out-of-state telehealth licensure pathway. Eff. 7/7/2023.
- **modality.video** — 16.10.8.8(L)(6) "face-to-face telehealth encounter online, using standard videoconferencing technology, where a medical history and informed consent are obtained and a medical record generated."
- **relationship.inPerson** — 16.10.8.8(L)(6)(b) physical exam "waived when a physical examination would not normally be part of a typical physical face-to-face encounter."
- **relationship.consent** — 16.10.8.8(L)(6) "medical history and informed consent are obtained" (condition of the practice-legitimacy exception; verb "obtained").
- **prescribing.inPersonRx** + **ecommerce.dtc (prescriber side)** — 16.10.8.8(L): prescribing "based solely on an on-line questionnaire" without an established physician-patient relationship is unprofessional conduct.
- **prescribing.pdmp — MANDATORY (key result)** — 16.10.14.8(C): "Before a practitioner prescribes or dispenses for the first time, a controlled substance in schedule II, III, IV or V ... for a period greater than four days, or if there is a gap ... for 30 days or more, the practitioner **shall review** a prescription monitoring report ... for the preceding 12 months"; (D) review "a minimum of once every three months during the continuous use." **This prescriber-review mandate lives in the MEDICAL BOARD rule — NOT in 16.19.29 NMAC (which is a dispenser REPORTING rule: "shall submit/report within one business day").** Do not confuse the two.

### NM Board of Pharmacy (Title 16 Chapter 19)
- **pharmacy.nonresident** — 16.19.6.24 "No nonresident pharmacy shall ship, mail or deliver prescription drugs to a patient in this state unless licensed by the board" (+ DEA/board CS registration). Last amended 10/10/2023.
- **pharmacy.pic** — 16.19.6.9 NM-licensed PIC per §61-11-15; failure = violation of §61-11-20(A)(1).
- **pharmacy.csDispense** — 16.19.20 (eff. 6/26/2018) CS registration/monitoring, DEA form 222, inventory/disposition records, per §30-31-11.
- **compounding.stateReg** — 16.19.30 (nonsterile, eff. 9/15/2006): cites **USP <795> BY NUMBER** ("the current chapter of USP <795>") + general "USP/NF." **USP <797>/<800> NOT adopted by number** (sterile licensed separately in 16.19.12 fee category).
- **ecommerce.dtc (dispenser side)** — 16.19.4.8: unprofessional to dispense "if the pharmacist has knowledge ... that the prescription was issued on the basis of an internet-based questionnaire or an internet-based consultation without a valid practitioner-patient relationship."
- **ecommerce.onlinePharmacy** — 16.19.6.24 nonresident framework (no separate internet-pharmacy certificate).

## LEFT "NEEDS LEGAL REVIEW"
- **modality.audioOnly** + **modality.async** — 16.10.8.8(L)(6) authorizes only "videoconferencing technology"; neither audio-only nor store-and-forward is named in the practice-standards rule. NOT FOUND (may exist in NM insurance/reimbursement titles, a different context).
- **ecommerce.website** — no mandatory public website/VIPPS display located.

## FOLLOW-UP
- If nmonesource.com becomes reachable (or via authenticated access), independently open NMSA 1978 §61-6 (Medical Practice Act), §61-11 (Pharmacy Act), §30-31-24 (PMP statute) to confirm the statutory backing behind these rules and to check for an audio-only/store-and-forward statutory authorization.
