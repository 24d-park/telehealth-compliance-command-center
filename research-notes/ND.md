# North Dakota — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 9 (+ 2 federal defaults) → 13 ver / 7 rev.

## SOURCING TECHNIQUE (important for ND)
ndlegis.gov serves the **statute TEXT only inside chapter PDFs** — the `t43c17.html` pages are a table-of-contents ONLY (section links, no body). The PDF deep-link (`t43c17.pdf#nameddest=43-17-44`) opens in Google's PDF viewer iframe, which console can't read. **What worked:** inject pdf.js from cdnjs, `fetch()` the raw PDF ArrayBuffer, extract every page's text layer, stash to `window.__NDTX`. NOTE: the hyphens in section numbers render as U+2011 (non-breaking) so `indexOf('43-17-44')` fails — search by keyword ('telemedicine', 'videoconferencing') instead. Same pdf.js approach handles the NDAC rule PDFs (`ndlegis.gov/information/acdata/pdf/61-02-01.pdf`).

## STRUCTURAL KEY
Telehealth practice standard = **NDCC ch. 43-17** (Physicians; Board of Medicine), modernized by **S.L. 2023 ch. 382**. §43-17-44 = telemedicine standards, §43-17-45 = prescribing, §43-17-02.3 = license/deemed-location. Pharmacy = ch. 43-15 + NDAC Title 61. PDMP = NDCC ch. 19-03.5. (Telehealth INSURANCE parity is separate, NDCC Title 26.1 — not used.)

## VERIFIED (statute PDFs read verbatim via pdf.js)
- **provider.fullLicense** — §43-17-02.3: "The practice of medicine is deemed to occur in the state the patient is located. A practitioner providing medical care to a patient located in this state ... shall possess an active North Dakota license."
- **modality.video + async** — §43-17-44(3): "An examination utilizing secure videoconferencing or store-and-forward technology ... meets this standard."
- **relationship.inPerson** — §43-17-44(3): exam "may be performed entirely through telemedicine, if ... equivalent to an in-person examination." Also requires a "bona fide relationship."
- **prescribing.inPersonRx** — §43-17-45: telemedicine prescribing OK on professional discretion; **opioids via telemedicine ONLY as FDA-approved MAT for opioid use disorder or to hospital/LTC patients**, "may not be prescribed through a telemedicine encounter for any other purpose."
- **ecommerce.dtc** — §43-17-44(3)(a): "An examination or evaluation consisting only of a static online questionnaire or an audio conversation does not meet the standard of care."
- **pharmacy.nonresident** — §43-15-34.1: "Any pharmacy operating outside the state which ships, mails, or delivers ... into North Dakota shall obtain and hold a pharmacy permit."
- **pharmacy.pic** — §43-15-32: pharmacy "must be in charge of a registered pharmacist."
- **compounding.stateReg** — NDAC 61-02-01: "Should be conducted according to USP chapter 795" / "compounded according to USP chapter 797" / hazardous "according to USP chapter 800." All three by number (note the softer "should" verb).

## LEFT "NEEDS LEGAL REVIEW" (honest reds)
- **prescribing.pdmp** — §19-03.5-05 expressly disclaims: "Nothing in this chapter requires a prescriber or dispenser to obtain information about a patient from the central repository prior to prescribing or dispensing a controlled substance." VOLUNTARY. (§43-17-45(2) requires telemedicine CS-prescribers to "participate in" the PDMP — that's registration, not query.)
- **modality.audioOnly** — §43-17-44(3)(a) EXCLUDES it: a standalone "audio conversation ... does not meet the standard of care." One of the clearer audio-only exclusions.
- **relationship.consent** — no express telehealth informed-consent mandate in ch. 43-17. (The "obtain informed consent" clause I found is in the physician-assistant scope-of-practice list §43-17-02.1, NOT telemedicine — checked and rejected.)
- **provider.telehealthReg** — full ND license or IMLC (§43-17-46); no separate telehealth registry.
- **pharmacy.csDispense** — NDAC 61-13 / NDCC 19-03.1 (chapter-level only; section text not extracted).
- **ecommerce.onlinePharmacy** (subsumed in the §43-15-34.1 nonresident permit), **ecommerce.website** (not found).

## FOLLOW-UP
- Extract NDAC 61-13 + NDCC 19-03.1 section text (pdf.js) for pharmacy.csDispense.
- Check NDAC Title 50 (Board of Medicine rules) for any telehealth consent rule that would flip relationship.consent.


---

## Update 2026-07-23 (wave 5) — +4 (13 -> 17 verified)

Prior-session leads RE-CONFIRMED verbatim by parent via pdf.js on ndlegis.gov, plus new CS extraction. URL fixes: PDMP=t19c03-5.pdf, CS Act=t19c03-1.pdf, NDAC CS=61-13-01.pdf.

Newly wired:
- **provider.telehealthReg** — ch.43-17: telemedicine practitioners are "licensees" (43-17-44(2): "A licensee practicing telemedicine shall verify the identity of the patient ... and shall disclose ... the identity and licensure status of any licensee"). Full ND license or IMLC (43-17-46) exclusive; no separate telehealth registry. VERIFIED-NULL. [nd_telemed]
- **modality.audioOnly — EXCLUDED** — 43-17-44(3)(a): "An examination or evaluation consisting only of a static online questionnaire or an audio conversation does not meet the standard of care." [nd_telemed]
- **pharmacy.csDispense** — NDCC 19-03.1-22(1): "no controlled substance in schedule II may be dispensed without the written prescription of a practitioner ... may not be filled more than six months after the date it was written." (19-03.1-22.4 also bars internet dispensing without a valid Rx.) [nd_cs]
- **ecommerce.onlinePharmacy** — 43-15-34.1 out-of-state pharmacy permit subsumes internet/mail-order ("internet"/"website" absent from ch.43-15). [nd_pharmacy]

Still red (confirmed genuine): relationship.consent (the only "consent" in ch.43-17 is the PA scope list 43-17-02.1, NOT telemedicine), prescribing.pdmp (19-03.5-05 disclaims any query duty = VOLUNTARY; note dispenser reporting 19-03.5-02(2) + telemed-prescriber participation 43-17-45(2) ARE separately mandatory), ecommerce.website (no website/disclose language in ch.43-15 or NDAC 61-02-01 — not swept across all of NDAC Title 61).
