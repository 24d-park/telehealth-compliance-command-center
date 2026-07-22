# Wyoming — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 5 (+ 2 federal defaults) → 8 ver / 12 rev. **Honest partial — most specifics delegated to Board rules I couldn't extract.**

## SOURCING TECHNIQUE
***Wyoming serves statutes ONLY as large compressed title PDFs*** (no HTML section deep-links). Read Title 33 (816pp, ~1.56M chars) + Title 35 (954pp) via pdf.js: `fetch()` the PDF, extract every page's text layer, stash to window.__WY. The FlateDecode streams decompress cleanly in-browser. There is NO per-section anchor URL — the citation resolves only to the title PDF. Board rules are on rules.wyo.gov (Board of Medicine = Agency 052; Board of Pharmacy separate) as PDFs behind a viewer — NOT extractable this session.

## STRUCTURAL KEY (why WY is mostly red)
***Wyoming's Medical Practice Act DELEGATES telehealth specifics to Board RULES, not statute.*** W.S. §33-26-202(a)(xix) directs the Board of Medicine to "Adopt rules and regulations for the practice of telemedicine"; W.S. §33-1-303(a)(iv) has every Title-33 board define telemedicine/telehealth "within each promulgated rule." So modality/consent/in-person/DTC live in rules.wyo.gov (Agency 052), and PIC/compounding/PDMP live in Board of Pharmacy rules — none extractable this session. The statute gives only the skeleton.

## VERIFIED (from the Title 33 statute PDF)
- **provider.fullLicense** — W.S. §33-26-301(a): "No person shall practice medicine in this state without a license granted by the board." Since §33-26-102 defines telemedicine AS the practice of medicine, a WY license is required.
- **modality.video** — W.S. §33-26-102(a)(xxix): "'Telemedicine' means the practice of medicine by electronic communication or other means from a physician in a location to a patient in another location, with or without an intervening health care provider." Broad; real-time electronic/video is the core recognized case.
- **pharmacy.nonresident** — W.S. §33-24 (Pharmacy Act): a pharmacy that "ships, mails or delivers, in any manner, controlled substances or prescription drugs or devices into this state ... shall be considered a nonresident pharmacy, shall obtain a license from the board" (+ comply with home-state regulator).
- **ecommerce.onlinePharmacy** — subsumed in the §33-24 nonresident license (no separate internet-pharmacy permit in statute).

## LEFT "NEEDS LEGAL REVIEW" (mostly delegated-to-rule, unread)
- **provider.telehealthReg** — no separate pathway found in statute.
- **modality.audioOnly + modality.async** — the statute def is broad ("electronic communication or other means") but does NOT affirmatively name audio-only or store-and-forward; delegated to Board of Medicine rule. Left red rather than infer permission from silence (ID/ND precedent).
- **relationship.inPerson + relationship.consent + prescribing.inPersonRx** — Board of Medicine rules (Agency 052, Ch. 1 telemedicine), unread.
- **prescribing.pdmp** — ***WY's PDMP is Board-of-Pharmacy-run under Title 33 ch. 24 + Board rules, NOT the Title 35 controlled-substances article*** (searched Title 35, no "drug monitoring program" section). The mandatory-vs-voluntary verb is not readable from statute — left red rather than guess.
- **pharmacy.csDispense + pharmacy.pic + compounding.stateReg (USP) + ecommerce.dtc + ecommerce.website** — all Board of Pharmacy rules, rules.wyo.gov PDFs not extractable this session.

## FOLLOW-UP (WY is the weakest — needs a Board-rules pass)
- Dedicated run on rules.wyo.gov: Board of Medicine Agency 052 Ch. 1 (telemedicine modality/consent/in-person/DTC) + Board of Pharmacy rules (PIC, compounding USP-by-number, PDMP mandatory-query verb, CS dispensing). If the rules.wyo.gov viewer stays unextractable, try the Board's own PDF mirrors (wyomedboard.wyo.gov / pharmacyboard.wyo.gov) or Wayback.
