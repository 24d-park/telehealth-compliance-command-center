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


---

## Update 2026-07-23 (wave 4) — +1 (13 -> 14 verified)

**provider.telehealthReg wired** — HRS §453-1.3(e) (read via Wayback capture of capitol.hawaii.gov, live host Cloudflare-blocked): "A physician-patient relationship may be established via a telehealth interaction; provided that the physician has a license to practice medicine in the State" + §453-1.3(a). Full HI licensure exclusive; no separate telehealth registration. VERIFIED-NULL. [hi_telehealth]

Still red (parent-confirmed honest):
- **relationship.consent** — §453-1.3(b) is a "documented patient evaluation, including history and a discussion of physical symptoms" mandate, NOT an explicit informed-consent clause. Any express consent rule would be in HAR medical-board rules (unread). Red.
- **prescribing.pdmp** — HRS 329: §329-101(b) makes dispenser REPORTING mandatory ("no CS may be dispensed unless ... reported"), but prescriber access §329-104(c) is permissive/discretionary. No "shall query before prescribing." Red (verified-null).
- **pharmacy.nonresident / csDispense / onlinePharmacy / website** — all in HAR Title 16 Ch. 95 (DCCA/PVL PDF, 58pp, archive https://web.archive.org/web/20250705005719id_/https://cca.hawaii.gov/pvl/files/2013/08/HAR-16-95-C_0816.pdf). Subagent located but couldn't extract (archive.org CSP blocked PDF.js). FOLLOW-UP: navigate to a neutral origin FIRST, then fetch that archived PDF (archive.org serves CORS *) + pdf.js.


---

## Update 2026-07-23 (wave 6) — +1 (14 -> 15 verified); HAR 16-95 extracted

**ACCESS WIN — the HAR 16-95 PDF is extractable.** The prior note flagged the 58-page DCCA HAR-16-95 PDF as un-extractable (archive.org CSP blocked pdf.js). Fix: NAVIGATE to the archive.org id_ URL FIRST (so you're on the web.archive.org origin), THEN inject pdf.js + same-origin `fetch()` the ArrayBuffer. Cross-origin fetch of the archived PDF from a neutral page (example.com) fails CORS ("Failed to fetch") — the same-origin trick is the key. Archived PDF: https://web.archive.org/web/20250705005719id_/https://cca.hawaii.gov/pvl/files/2013/08/HAR-16-95-C_0816.pdf (109,351 chars extracted).

**pharmacy.csDispense wired** — Haw. Rev. Stat. §329-101(b) (Electronic Prescription Accountability System, via Wayback capitol.hawaii.gov): "No identified controlled substances may be dispensed unless information relevant to the dispensation of the substance is reported electronically ... to the central repository." Mandatory CS-dispensing condition. Corroborated by HAR §16-95-82 (Valid prescriptions): "A pharmacist may fill and dispense prescriptions provided the prescription is valid. A valid prescription shall be legibly written and contain, at a minimum ..." (date, prescriber signature/name/address, drug+instructions, patient identifiers). [hi_329101]

### Held RED after reading the FULL 58-page HAR 16-95 (genuine absences, NOT access failures):
- **pharmacy.nonresident** + **ecommerce.onlinePharmacy** — HAR 16-95 has NO nonresident-pharmacy or internet/online-pharmacy provision (chapter covers pharmacist/pharmacy licensing, wholesale distributor, practice, records, advertising — no nonresident/internet section). HRS §461-14 is only the general in-state permit ("without first having obtained a permit"). The words "nonresident"/"out-of-state"/"internet"/"website" do not appear in the chapter. Genuine absence.
- **ecommerce.website** — §16-95-103 is "Advertising of controlled substances prohibited," NOT an on-website disclosure mandate. §§16-95-101/102 govern advertising procedures (prescription drugs / related services), no website-display requirement. Red.
- **relationship.consent** — §453-1.3(b) documented-evaluation mandate, not explicit informed consent (unchanged).
- **prescribing.pdmp** — HRS 329 dispenser REPORTING mandatory (§329-101(b)), but prescriber query permissive (§329-104(c)). VOLUNTARY. Red.

HI section list confirms: no nonresident/internet subchapter exists. These reds are its honest ceiling absent new statute.
