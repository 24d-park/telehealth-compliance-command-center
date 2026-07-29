# Research Note — Tennessee (TN)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 13 / 20  (9 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 7 / 20
- **Method:** Primary sources only. The official TN SOS rule PDFs were read via **Internet Archive captures** (see sourcing note below), extracted in-browser with PDF.js. Subagent findings treated as leads and independently re-verified.

## Sources checked (official TN SOS rule PDFs, via Internet Archive)

- **0880-02-.16 — Telemedicine Licensure & Practice** (Board of Medical Examiners, June 2025) — https://web.archive.org/web/20250701141747id_/https://publications.tnsosfiles.com/rules/0880/0880-02.20250617.pdf
- **1140-03 — Pharmacy Standards of Practice** (PIC .14; CS dispensing) (Board of Pharmacy, March 2024) — https://web.archive.org/web/20240528015718id_/https://publications.tnsosfiles.com/rules/1140/1140-03.20240314.pdf
- **1140-07 — Sterile Product Preparation; USP** (Board of Pharmacy, May 2024) — https://web.archive.org/web/20240528015650id_/https://publications.tnsosfiles.com/rules/1140/1140-07.20240501.pdf

## Verified requirements

No practice on a TN patient (in person or remotely) unless licensed by the Board (0880-02-.16);
**TN DISCONTINUED its standalone "telemedicine license"** — Board no longer issues one (notable change);
video/store-and-forward permitted; **audio-only EXCLUDED from telemedicine** ("not an audio only telephone
conversation" — stricter than most states); relationship exists "whether or not there has been an encounter
in person" (no in-person mandate); CS orders require prescriber DEA number (1140-03); PIC record maintained
by Board (1140-03-.14); sterile compounding per "applicable USP standards" (1140-07-.02).

## Fields still "Needs legal review"

relationship.consent, prescribing.inPersonRx, prescribing.pdmp (CSMD, TCA 53-10-310), pharmacy.nonresident
(TCA 63-10-216), ecommerce.* — these live in the **TN CODE (Titles 53 & 63)**, which is genuinely
UNREACHABLE: advance.lexis.com is session-locked and aggregators are banned. The section numbers appear only
**cited within rule authority lines**, not as readable text, so nothing was asserted from them.

## SOURCING NOTE (important)

The live `publications.tnsosfiles.com` host is CloudFront-403 in this environment. The TN fields are sourced
to **Internet Archive captures of the genuine official .gov PDFs** (byte-identical copies) — disclosed in
each SOURCES entry. This is a genuine primary document, not an aggregator. Re-fetch from the live TN SOS host
(or a Lexis session for the Code) when available to refresh dates and unlock the statute-dependent fields.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


---

## Update 2026-07-28 — more-research pass (13 -> 14/20)

**relationship.consent WIRED** — Tenn. Code Ann. § 63-1-155(b) (Telehealth Services — Establishment of Provider-Patient Relationship): "a healthcare provider-patient relationship with respect to telemedicine or telehealth is created by mutual consent and mutual communication, except in an emergency, between the patient and the provider. The consent by the patient may be expressed or implied consent." TN codifies consent as a telehealth relationship-formation element (expressed OR implied) — a genuine sourced consent requirement, weaker than documented-informed-consent states (noted in-field). [src: tn_6301155]

**ACCESS:** read verbatim from the Internet Archive `id_` capture of the official 2021 TN Code (Justia verbatim reproduction) — https://web.archive.org/web/20240805235525id_/https://law.justia.com/codes/tennessee/2021/title-63/chapter-1/part-1/section-63-1-155/ — same archived-mirror route used for IN/AR. Live TN Code hosts (advance.lexis.com, publications.tnsosfiles.com) remain Lexis/CloudFront-blocked. Only the 2021 capture of § 63-1-155 exists; re-verify current consolidated text when a live TN host is reachable.

**Still red (6), confirmed NOT on the Justia archived mirror this pass:**
- prescribing.pdmp (CSMD, TCA § 53-10-310) — Title 53 pharmacy chapters not reproduced on Justia TN mirror
- prescribing.inPersonRx
- pharmacy.nonresident (TCA § 63-10-216) — not archived
- ecommerce.onlinePharmacy / ecommerce.website / ecommerce.dtc

CDX enumeration confirmed Justia's TN captures cover only the Title 63 physician chapters (63-6-209 stale 2015; 63-1-155 telehealth 2021; 63-1-156 overdose-immunity). The pharmacy/CSMD sections need a live TN primary host or a Lexis session. Follow-up: retry live publications.tnsosfiles.com CSMD/1140 rule PDFs via Wayback for the § 53-10-310 mandatory-query verb + TN Board of Pharmacy nonresident (§ 63-10-216).


## UPDATE 2026-07-29 — final-research wave 5, NO CHANGE (stays 14/20) — 2 HIGH-CONFIDENCE LEADS HELD
Subagent lead. Statutory text came ONLY from the LawServer secondary mirror ("current as of 2024"); Justia
(Cloudflare), TN SOS PDF publications.tnsosfiles.com (CloudFront 403), Wayback (not archived), and Justia-live
(Cloudflare) were ALL unreachable this session. Per the tracker's primary-source rule, NOT wired — verify verbatim
from the official LexisNexis-hosted TN Code or TN SOS next session, then green.
### Held leads (ready to wire once primary confirmed)
- **prescribing.pdmp** — Tenn. Code §53-10-310(e)(1): "When prescribing a controlled substance, all healthcare
  practitioners ... shall check the controlled substance database prior to prescribing ... at the beginning of a
  new episode of treatment, prior to the issuance of each new prescription ... for the first ninety (90) days ...
  and ... at least every six (6) months when that prescribed controlled substance remains part of the treatment."
  Triggers (e)(4): all opioids + benzodiazepines. Exceptions (e)(6): hospice; ≤3-day supply no refill; inpatient/
  residential administration. → GREEN once primary-verified. (Would need a new source key, e.g. tn_53_10_310.)
- **pharmacy.nonresident** — Tenn. Code §63-10-210: "A pharmacy that dispenses and mails a prescription into
  Tennessee from another state shall first pay the licensure fee required of a Tennessee pharmacy ...". §63-10-216
  adds out-of-state compounding-pharmacy inspection. → GREEN once primary-verified. (New source key, e.g. tn_63_10_210.)
### Genuine holds
- prescribing.inPersonRx — §63-1-155 imposes same-standard-of-care + a provider-patient relationship "created by
  mutual consent and mutual communication," but NO prior-in-person-exam mandate at the statutory level. Any
  questionnaire/in-person rule would be in BME rule 0880-02-.14/.16 (TN SOS 403 — unread). Red.
- ecommerce.dtc — no explicit questionnaire bar in §63-1-155; likely in BME rules 0880-02-.14/.16 (unreachable). Red.
- ecommerce.onlinePharmacy / ecommerce.website — genuine absences.
