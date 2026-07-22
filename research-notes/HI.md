# Hawaii — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 10 (+ 2 federal defaults) → 13 ver / 7 rev.

## SOURCING TECHNIQUE
***capitol.hawaii.gov is Cloudflare-blocked*** (direct + console-fetch; even some Wayback captures archived the block page). **Workaround:** individual-section Internet Archive `id_` raw captures of the official HRS pages (`web.archive.org/web/YYYYid_/https://www.capitol.hawaii.gov/hrscurrent/...`). HAR 16-95 (Board of Pharmacy rules) read via pdf.js on the official DCCA PDF at cca.hawaii.gov.

## STRUCTURAL KEY
Practice standard = **HRS §453-1.3** "Practice of telehealth" (Hawaii Medical Board). ***NOT the insurance law HRS 431:10A-116.3, and NOT §453-1.3(h) which is a behavioral-health REIMBURSEMENT parity provision.*** Pharmacy = HRS ch. 461 + HAR Title 16 ch. 95. PDMP/controlled substances = HRS ch. 329. ***FLAG: §453-1.3 subsections (c), (h), (j) carry a repeal-and-reenactment date of 12/31/2025 (L 2023 c.107) — re-verify (c)/(j) after that date.***

## VERIFIED
- **provider.fullLicense** — §453-1.3(e): relationship "may be established via a telehealth interaction; provided that the physician has a license to practice medicine in the State."
- **modality.video** — §453-1.3(j): "real-time video conferencing-based communication."
- **modality.async** — §453-1.3(j): "store and forward technologies" + "secure asynchronous information exchange."
- **relationship.inPerson** — §453-1.3(e): relationship "may be established via a telehealth interaction" (no prior in-person for general care). Opioid/cannabis exception in (c).
- **prescribing.inPersonRx** — §453-1.3(c): for opiates "a physician-patient relationship shall only be established after an in-person consultation between the prescribing physician and the patient." A genuine opioid in-person requirement (non-opioid CS may use a telehealth-established relationship).
- **ecommerce.dtc** — §453-1.3(c): "Issuing a prescription based solely on an online questionnaire is not treatment ... and does not constitute an acceptable standard of care."
- **pharmacy.pic** — §461-9: "A registered pharmacist shall be in personal and immediate charge of the pharmacy and personnel."
- **compounding.stateReg** — HAR §16-95-110(a)(17): compounding per "chapters 795 (nonsterile preparations) and 797 (sterile preparations) of the United States Pharmacopeia National Formulary, as amended." USP 795/797 BY NUMBER; ***USP 800 NOT referenced.*** Eff. 8/15/2016.

## LEFT "NEEDS LEGAL REVIEW"
- **modality.audioOnly** — ***EXCLUDED:*** §453-1.3(j): "standard telephone contacts, facsimile transmissions, or e-mail text, in combination or alone, do not constitute telehealth services." (Audio-only appears only in the (h) behavioral-health REIMBURSEMENT provision — insurance context, not a practice standard.) Coded red.
- **prescribing.pdmp** — HRS §329-101 mandates reporting/registration; §329-104(c) disclosure to registrants "at the discretion of the administrator." No shall-query-before-prescribing → VOLUNTARY.
- **provider.telehealthReg** — full HI licensure required; no separate pathway.
- **relationship.consent** — no express "shall obtain informed consent" in §453-1.3 (requires documented evaluation + records availability, but not a consent "shall").
- **pharmacy.nonresident + ecommerce.onlinePharmacy** — ***genuine absence:*** HRS ch. 461 has NO separate nonresident/mail-order or internet-pharmacy license category ("internet"/"online" appear nowhere in HAR 16-95); the general pharmacy permit §461-14 applies to any pharmacy operating "within the State."
- **pharmacy.csDispense** — HRS §329-38 (general Rx content rules).
- **ecommerce.website** — not found.

## FOLLOW-UP
- Re-verify §453-1.3(c)/(j) after the 12/31/2025 repeal/reenact date to confirm the DTC ban + modality definition survive unchanged.
