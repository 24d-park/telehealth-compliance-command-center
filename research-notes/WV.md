# West Virginia — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Primary host:** code.wvlegislature.gov (WV Code — clean official host). Statute body sits BELOW a huge chapter-selector `<select>` in the snapshot; extract via console `document.body.innerText` + `indexOf('§30-...')`/`slice`. The a11y snapshot only shows the chapter dropdown, so always read the body through console.
**Fields verified:** 14 (+ 2 federal defaults) → 18 ver / 2 rev. **Richest of this batch.**

## STRUCTURAL KEY
**W. Va. Code §30-1-26 "Telehealth practice" is a BOARD-WIDE cross-cutting statute** applying to ALL Chapter 30 health-care licensing boards (medicine, pharmacy, nursing, etc.). The medicine-specific companion is **§30-3-13a "Telemedicine"** (Board of Medicine/Osteopathic). Both are **practice-standards** titles (Ch. 30 Professions), NOT insurance/reimbursement (Ch. 33). §30-1-26 current version enacted 2025; §30-3-13a carries 2023-era abortifacient/gender-medication prescribing prohibitions.

## VERIFIED (statute text read verbatim)
- **provider.fullLicense** — §30-1-26(c): interstate-telehealth registration "does not authorize a health care professional to practice from a physical location within this state without first obtaining appropriate licensure."
- **provider.telehealthReg** — §30-1-26(a),(b)(2)(B): "Registration" = authorization "for the limited purpose of providing interstate telehealth services"; out-of-state practitioner must be home-state licensed/good-standing AND "Registered as an interstate telehealth practitioner with the appropriate board in West Virginia." Genuine registration pathway; §30-1-26(f) exempts already-WV-licensed practitioners.
- **modality.video / audioOnly / async** — §30-1-26(a) def = "synchronous or asynchronous telecommunications technology **or audio only telephone calls**" (excludes internet questionnaires, e-mail, fax). §30-3-13a: "Audio-only calls or conversations that occur in real time **may be used to establish** the physician-patient relationship" → **audio-only PERMITTED** (video preferred if available). "Store and forward telemedicine" defined (async).
- **relationship.inPerson** — §30-3-13a: relationship "may be established" via telemedicine (no prior in-person to START); BUT §30-1-26(b)(4): established telehealth patient must "visit an in-person health care practitioner within 12 months of using the initial telemedicine service" (suspendable at provider discretion; exempt for acute inpatient, post-op, behavioral/addiction medicine, palliative care).
- **relationship.consent — MANDATORY** — §30-3-13a(d)(6): a physician/podiatrist using telemedicine "shall ... Obtain from the patient appropriate consent for the use of telemedicine technologies."
- **prescribing.inPersonRx** — §30-3-13a(b)(5)/§30-1-26(b)(5): treating SOLELY via telemedicine "may not prescribe ... any controlled substances listed in Schedule II" (nor Sch II pain-relievers for chronic nonmalignant pain) unless established patient/same group practice. Sch II telemedicine Rx barred absent established relationship; no blanket in-person prerequisite for non-Sch-II.
- **prescribing.pdmp — MANDATORY (key result)** — §60A-9-5a(b): "upon initially prescribing or dispensing any Schedule II controlled substance, any opioid or any benzodiazepine to a patient who is not suffering from a terminal illness, and at least annually thereafter ... **shall access** the West Virginia Controlled Substances Monitoring Program Database," documenting results. Verb verified. **Scoped to INITIAL prescribing + at-least-annual, NOT before every fill** — distinct from the mere register/maintain-access duty in §60A-9-5a(a).
- **pharmacy.nonresident** / **ecommerce.onlinePharmacy** — §30-5-24(a) "A mail-order pharmacy which dispenses drugs shall register with the board" (+ §30-5-22 permit/inspection). No standalone VIPPS-style certificate.
- **pharmacy.pic** — §30-5-23(a): pharmacy "under the direction and supervision of a licensed pharmacist ... designated ... pharmacist-in-charge"; may not be PIC at more than one pharmacy (in or out of state).
- **pharmacy.csDispense** — Ch. 60A (Uniform CSA) + §60A-9-5a; §30-5-21 pharmacist responsible for quality/accuracy.
- **ecommerce.dtc** — TWO hooks: (prescriber) §30-3-13a "Treatment, including issuing a prescription, based solely on an online questionnaire, does not constitute an acceptable standard of care"; (dispenser) §30-5-14 pharmacist "may not compound or dispense any prescription order when he or she has knowledge that the prescription was issued by a practitioner without establishing a valid practitioner-patient relationship. An online or telephonic evaluation by questionnaire ... is inadequate."

## LEFT "NEEDS LEGAL REVIEW"
- **compounding.stateReg** — the rule is CSR **15-01** (WV Board of Pharmacy, eff. 7/1/2026) but the official rule is published only as a **FlateDecode-compressed PDF whose body text is NOT machine-extractable** on `apps.sos.wv.gov/adlaw/csr`. Left red rather than assert USP 795/797/800-by-number vs. general "current USP" — requires a manual/OCR PDF read.
- **ecommerce.website** — §30-5-20 is physical **principal-business-location** display only ("conspicuously display his or her board authorization at his or her principal business location"), NOT a website/VIPPS posting mandate.

## FOLLOW-UP
- Resolve compounding.stateReg by OCR-reading CSR 15-01 (readfile.aspx PDF) to nail the USP-by-number vs. general-reference distinction — WV is one field away from a very complete 15.
- Several Board of Pharmacy CSRs (15-01, 15-06, 15-15, 15-19) now carry 7/1/2026 effective dates — re-confirm on next pass.
