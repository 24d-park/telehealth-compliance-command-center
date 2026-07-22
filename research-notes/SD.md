# South Dakota — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 12 (+ 2 federal defaults) → 15 ver / 5 rev.

## SOURCING TECHNIQUE
sdlegislature.gov `/Statutes/NN-NN-N` pages render the statute text via JavaScript — the accessibility snapshot shows only section links + Source line. **Extract via `document.body.innerText`** in console (the rendered DOM has the full text). Clean, reliable, one section per URL. Admin Rules (ARSD) at `/Rules/Administrative/`.

## STRUCTURAL KEY
Telehealth practice standard = **SDCL ch. 34-52** (SL 2019 ch 156, amended through SL 2021 ch 158). Pharmacy = SDCL ch. 36-11 + ARSD Art. 20:51. Controlled substances = ch. 34-20B. PDMP = ch. 34-20E. (SD telehealth INSURANCE = SDCL Title 58 §58-17F, separate — not used.)

## VERIFIED (statute text read verbatim)
- **provider.fullLicense** — §34-52-2: "Any health care professional treating a patient in the state through telehealth shall be: (1) Fully licensed to practice in the state" (or employed by a listed SD-licensed facility).
- **modality.video** — §34-52-1(5): "Telehealth" includes "interactive audio-video"; §34-52-5 requires real-time audio-visual where a face-to-face would otherwise be required.
- **modality.async** — §34-52-1(4) "store-and-forward technology" (asynchronous), included in the §34-52-1(5) definition.
- **relationship.inPerson** — §34-52-3 + §34-52-5: relationship establishable via telehealth; face-to-face exam only "if a face-to-face encounter would otherwise be required." No blanket in-person prerequisite.
- **relationship.consent** — §34-52-3: "Any health care professional who utilizes telehealth **shall ensure** that a proper health provider-patient relationship is established and includes: ... (3) Obtaining appropriate consent for treatment from a requesting patient after disclosure regarding the delivery models and treatment methods or limitations." MANDATORY (this is the operative telehealth-consent duty; §34-52-7 additionally cross-references applicable informed-consent law).
- **prescribing.inPersonRx + ecommerce.dtc** — §34-52-6: "Without a proper provider-patient relationship, a health care professional using telehealth may not prescribe a controlled drug or substance ... solely in response to an internet questionnaire or consult, including any encounter via telephone."
- **pharmacy.nonresident** — §36-11-19.3: "Any nonresident pharmacy shall be licensed before conducting business in this state" (home-state good standing + names PIC + inspection report).
- **pharmacy.pic** — §36-11-32: license issues only with a pharmacist-in-charge (owner-pharmacist or affidavit delegating "complete responsibility ... to a pharmacist-in-charge").
- **compounding.stateReg** — ARSD 20:51:31:32: compounding/repackaging must comply with USP-NF (Feb 1 2024) chapters **797/795/800/825** by number (50 SDR 138 eff. 6/2/2024; amended 52 SDR 27 eff. 9/15/2025). *(Subagent read; chapter-level.)*
- **ecommerce.onlinePharmacy** — §§36-11-19.2–19.9: no separate "internet pharmacy" permit ('internet' does not appear in ch. 36-11); subsumed in nonresident/resident license.

## LEFT "NEEDS LEGAL REVIEW" (honest reds)
- **prescribing.pdmp** — §34-20E-11 expressly disclaims: "Nothing in this chapter requires a prescriber or dispenser to obtain information about a patient from the central repository prior to prescribing or dispensing a controlled substance." VOLUNTARY. Only registration (§34-20E-2.1) + reporting (§34-20E-3, ≤24h) are mandatory. (Identical disclaimer language to ND §19-03.5-05 — likely a shared model act.)
- **modality.audioOnly** — §34-52-1(5) enumerates "interactive audio WITH store and forward," NOT audio-only telephone; §34-52-6 treats a telephone encounter as insufficient for a CS-prescribing relationship. Not a recognized standalone modality → red.
- **provider.telehealthReg** — full SD licensure is the pathway; no separate telehealth registry.
- **pharmacy.csDispense** — SDCL ch. 34-20B + §34-20B-29 registration (chapter-level).
- **ecommerce.website** — §36-11-36 requires the physical license be posted IN the pharmacy (premises display), not a website/VIPPS mandate.

## FOLLOW-UP
- Independently open ARSD 20:51:31:32 to lock the compounding cite at subsection level (currently subagent-read).
