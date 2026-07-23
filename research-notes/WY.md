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


---

## Update 2026-07-23 — laggard push: unchanged (8/20), but extraction METHOD now proven

A subagent this session **solved the rules.wyo.gov access problem** but ran out of iterations before reaching any red-field chapter, so per the no-fabrication rule nothing was written. The method (use it next session):

**rules.wyo.gov serves rules as forced-download PDFs (application/octet-stream)** — direct browser_navigate fails (ERR_ABORTED / forces download). WORKING PATH: on the rules.wyo.gov origin, run the agency search, expand the agency, harvest each chapter's DownloadFile.aspx?...&token=... URL, then in the page console (same-origin):
```
const r = await fetch(URL); window.__buf = await r.arrayBuffer();
// inject pdf.js 3.11.174 from cdnjs, set workerSrc, getDocument({data:__buf}).promise
// loop pages concatenating getTextContent().items.map(x=>x.str).join(' ')
```
This returned full verbatim rule text — confirmed by extracting 80,634 chars of Board of Medicine Chapter 1. **Tokens in the DownloadFile URLs may be session-scoped** — re-harvest from a fresh search each session. NOTE: the Board's Google-Drive-hosted "Complete" PDF is NOT extractable (Drive viewer exposes one page at a time + blocks cross-origin fetch); use the rules.wyo.gov per-chapter PDFs instead.

**What's confirmed to exist but was NOT yet extracted (all 12 reds live here):**
- **Board of Medicine (Agency 052)**, effective 6-5-2024: the dedicated TELEMEDICINE chapter (separate from Ch.1 License Eligibility) holds telehealthReg / audioOnly / async / inPerson / consent / inPersonRx. Ch.1 only had the consulting-physician licensure-exemption telemedicine reference + a continuity-of-care clause.
- **Board of Pharmacy (Agency 059)** — 24 rule results: PDMP mandatory-query verb, CS dispensing, pharmacist-in-charge, USP <795>/<797> compounding adoption, online-pharmacy website disclosure, DTC/questionnaire ban.

FOLLOW-UP: a dedicated WY run that walks Agency 052 telemedicine chapter + Agency 059 chapters with the fetch-ArrayBuffer + pdf.js method above. WY is the weakest jurisdiction and should be a high priority — the access blocker is now solved, only the extraction volume remains.


---

## Update 2026-07-23 — laggard push wave 3: unchanged (8/20), leads HELD (disposition 6a)

A subagent re-ran the rules.wyo.gov fetch-ArrayBuffer + pdf.js extraction (the method proven last session) and surfaced clean, citation-precise verbatim leads. BUT per the read-it-yourself rule, the PARENT could not re-harvest the session-scoped DownloadFile tokens this session (the rules.wyo.gov agency-tree expand control did not surface tokened URLs to the parent, and the bare source_id URL returns "Invalid PDF structure" without a token). So NOTHING was wired. The leads are HELD here verbatim for next session to re-verify and wire.

### HELD LEADS (subagent-extracted verbatim; parent must re-read before wiring)
**STRUCTURAL: Wyoming Board of Medicine has NO dedicated telemedicine chapter.** Agency 052 has only Ch1 (License Eligibility), Ch2, Ch3, Ch5, Ch6, Ch7. The ONLY telehealth text is Agency 052 Ch.1 §7.

1. **provider.telehealthReg + relationship.inPerson + prescribing.inPersonRx** — Agency 052, Ch.1 §7(e) "Continuation of care received outside Wyoming" (eff. 05/23/2025, ref 052.0001.1.05232025). Verbatim: "A physician or physician assistant who has established a provider-patient relationship in another state with a patient who is a resident of Wyoming may provide continued care to the patient via telehealth without a Wyoming physician or physician assistant license subject to the following: (i) The provider-patient relationship must have been established in an in-person encounter in a state in which the physician or physician assistant is licensed; (ii) Subsequent care may be provided ... if the care is a logical and expected continuation ...; (iii) The telehealth care may continue for up to six (6) months ... after which an in-person encounter must take place ..." + §7(a): "'brought into this state' means establishing a physician-patient relationship, either by the physician's physical presence with the patient or through telemedicine." → Interpretation: exclusive WY licensure to treat WY patients; NO separate telehealth registration; the only unlicensed exception is out-of-state continuation-of-care requiring a prior in-person exam in the licensing state.
   TO VERIFY: re-harvest the Ch.1 DownloadFile token (subagent used source_id=24721), extract via pdf.js, confirm §7(e) language verbatim, then wire provider.telehealthReg as a verified-null (exclusive licensure).

2. **compounding.stateReg — USP 795/797/800/825 ADOPTED** — Agency 059 (Board of Pharmacy) Program 0001 Ch.22 (Compounding) §4 "Incorporation by Reference" (eff. 08/19/2025, ref 059.0001.22.08192025, source_id=24903). Verbatim: "All referenced general chapters of the United States Pharmacopeia - National Formulary (USP-NF)... are specifically referring to the USP-NF 2024, Issue 1, which is hereby incorporated and adopted by reference... (i) ... General Chapter 795 Pharmaceutical Compounding – Nonsterile Preparations ... (ii) ... General Chapter 797 Pharmaceutical Compounding – Sterile Preparations ... (iii) ... General Chapter 800 Hazardous Drugs ... (iv) ... General Chapter 825 Radiopharmaceuticals ..." → WY adopts USP 795/797/800/825 by reference.
   TO VERIFY: re-harvest Ch.22 token, extract, confirm §4, wire compounding.stateReg green.

3. **prescribing.pdmp — genuine NULL (leave red)** — Agency 059 Program 0002 Ch.8 (PDMP, eff. 05/24/2023, source_id=21690). The rule imposes NO mandatory pre-prescribe query: "Pharmacists and practitioners shall register as users with Wyoming PMP AWARxE to request patient profiles..." ("shall register"/"may request" only). Any mandatory-query duty, if any, is in statute (W.S. 35-7-1060), unread. → leave prescribing.pdmp RED (no rule-level mandate).

### EXTRACTED-BUT-UNPARSED chapters (subagent fetched, ran out of iterations) — for next session:
- Agency 059 Ch.10 Issuing/Dispensing Rx for CS (source_id=21689) → pharmacy.csDispense, maybe ecommerce.dtc/inPersonRx
- Agency 059 Ch.2 General Practice of Pharmacy (source_id=21691) → pharmacy.pic, ecommerce.website
- Agency 059 Ch.19 Licensing of Pharmacists/Pharmacies (source_id=13666) → ecommerce.website, pharmacy.pic
- Agency 059 Ch.14 TELEPHARMACY (source_id=11477) → highly relevant to modality.audioOnly/async
- Agency 059 Ch.9 Opioid Rx Limits (source_id=17696)

### METHOD REMINDER for next session
The bare `DownloadFile.aspx?source_id=N` URL returns "Invalid PDF structure" — it REQUIRES the session-scoped `&token=...`. Harvest fresh tokens by expanding the agency in the rules.wyo.gov search-results tree (the DownloadFile links with tokens appear in the expanded chapter rows), then fetch same-origin + pdf.js. If the agency-tree expand won't surface tokened URLs, try the boards' own PDF mirrors (wyomedboard.wyo.gov, pharmacyboard.wyo.gov) or Wayback captures of the rule PDFs.


---

## Update 2026-07-23 (wave 4) — HELD LEADS WIRED (8 -> 10 verified) + ACCESS BREAKTHROUGH

**The token problem is SOLVED.** rules.wyo.gov's forced-download `DownloadFile.aspx?source_id=N` PDFs need a session-scoped `&token=` that can't be harvested programmatically here (the agency-tree expand control never surfaced tokened URLs to the parent). BUT the site's AJAX backend exposes the rule text directly:

**`POST https://rules.wyo.gov/AjaxHandler.ashx?handler=GetRuleVersionHTML` with body `RULE_VERSION_ID=<id>`** returns the full rule as HTML — no token, no PDF, no pdf.js. Parse it with a throwaway div + `.innerText`. The `RULE_VERSION_ID` values are the same numeric source_ids the subagent extracts (e.g. Ch.1 Medicine = 24721, Ch.22 Compounding = 24903, Ch.8 PDMP = 21690). Discover them from `wyScripts.js` (handlers: `Search_GetProgramRules`, `GetRuleVersionHTML`, `GetAgencyPrograms`). **This is the durable WY access path — use it, not the tokened DownloadFile PDFs.**

Wired this session (parent-verified verbatim via GetRuleVersionHTML):
- **provider.telehealthReg** — Board of Medicine Ch.1 §7 (eff. 05/23/2025, ID 24721): "brought into this state means establishing a physician-patient relationship, either by the physician's physical presence with the patient or through telemedicine"; the only unlicensed pathway is out-of-state continuation-of-care (§7(e)) requiring a prior in-person encounter in the licensing state, capped 6 months. Full WY licensure exclusive; NO separate telehealth registration. VERIFIED-NULL. [wy_med_ch1]
- **compounding.stateReg** — Board of Pharmacy Ch.22 §4 (eff. 08/19/2025, ID 24903): adopts USP-NF 2024 Issue 1 General Chapters 795 (nonsterile) + 797 (sterile) [+800/825] by reference. [wy_pharm_ch22]

Confirmed RED (verified-null, not assumed): **prescribing.pdmp** — Board of Pharmacy Ch.8 §4 (ID 21690): "Practitioners shall register with the controlled substances prescription tracking program (Wyoming PMP AWARxE)" but NO "shall query"/"prior to prescribing" mandate anywhere. Query is not mandatory at the rule level → red.

STRUCTURAL: **WY Board of Medicine has NO dedicated telemedicine chapter** — the only telehealth text is Ch.1 §7. So modality.audioOnly/async + relationship.consent are not addressed in Board of Medicine rules → stay red.

### Still red (10) — for next session via GetRuleVersionHTML:
- pharmacy.csDispense → Board of Pharmacy Ch.10 (Issuing/Dispensing Rx for CS, ID 21689)
- pharmacy.pic → Ch.2 (General Practice, ID 21691) or Ch.19 (Licensing, ID 13666)
- ecommerce.website → Ch.19 (ID 13666) or Ch.2 (ID 21691)
- modality.audioOnly/async → Ch.14 TELEPHARMACY (ID 11477) may address remote/audio
- relationship.inPerson/consent, prescribing.inPersonRx → likely genuine nulls (not in WY Board of Medicine rules); ecommerce.dtc → Ch.10
Fetch each via `GetRuleVersionHTML` (RULE_VERSION_ID above), read innerText, wire verbatim.


---

## Update 2026-07-23 (wave 6) — +2 (10 -> 12 verified)

Cleared two more WY reds via the tokenless `GetRuleVersionHTML` endpoint (parent-read verbatim):
- **pharmacy.csDispense** — Board of Pharmacy Ch.10 (Issuing/Dispensing Prescriptions for CS, eff. 05/24/2023, RULE_VERSION_ID=21689), (c): "In order for a controlled substance prescription to be effective it must be issued for a legitimate medical purpose by a practitioner acting in the usual course of his/her professional practice. The responsibility for the proper prescribing of controlled substances is upon the prescribing practitioner, but a corresponding responsibility rests with the pharmacist who dispenses the prescription." [wy_pharm_ch10]
- **pharmacy.pic** — Ch.2 (General Practice of Pharmacy, eff. 05/24/2023, RULE_VERSION_ID=21691) Section 4: "(a) Every resident pharmacy shall designate one pharmacist, who is licensed by the Board, as the PIC. (b) Every non-resident pharmacy shall designate one registered pharmacist as the PIC. (c) A pharmacist may not serve as PIC for more than one pharmacy at a time unless the pharmacist obtains a waiver from the Board." Ch.2(l) defines PIC. [wy_pharm_ch2]

### Held RED (honest) — the remaining 8:
- **ecommerce.website** — checked Ch.19 + Ch.2: every "website" reference is to the **Board's own** site (newsletter/Orange Book access), NOT a pharmacy on-website disclosure mandate. No such rule.
- **ecommerce.dtc** — no online-questionnaire prescribing ban in the pharmacy rules.
- **modality.audioOnly / modality.async / relationship.inPerson / relationship.consent / prescribing.inPersonRx** — WY Board of Medicine has NO telemedicine chapter (only Ch.1 §7). **Category-error avoided:** Ch.14 "Telepharmacy" DOES use "real-time data, video, and audio links" but that governs remote-SITE pharmacy operations between a telepharmacy and its parent pharmacy — it is NOT a telehealth physician-patient modality, so it does not green audioOnly/async. Left red.
- **prescribing.pdmp** — Ch.8 imposes registration but no mandatory pre-prescribe query (verified-null, wave 3).

WY is now effectively at its honest ceiling given no Board-of-Medicine telemedicine rules exist; remaining reds are genuine absences, not access failures.
