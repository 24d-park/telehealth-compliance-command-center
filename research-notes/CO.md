# Research Note — Colorado (CO)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 9 / 20  (5 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 11 / 20
- **Method:** Primary sources only. The official Colorado SOS pharmacy rule PDF was read via in-browser PDF.js. Subagent findings treated as leads and independently re-verified.

## Sources checked (official CO SOS rule PDF)

- **3 CCR 719-1 — State Board of Pharmacy Rules** (Permanent Rule, eff. 12/31/2025, 301 pp.) — https://www.sos.state.co.us/CCR/GenerateRulePdf.do?ruleVersionId=12294&fileName=3%20CCR%20719-1
  - Rule 5.00.15 (nonresident prescription drug outlet registration)
  - Rule 5.00.70 (pharmacist manager — "direct charge")
  - Rule 21.00.00 (compounding)
  - Rule 23.00.00 (PDMP — establishes program, no query mandate in the rule itself)

## Verified requirements (pharmacy-rule level only)

Nonresident prescription drug outlet registration for out-of-state shippers (5.00.15); pharmacy under the
"direct charge of a pharmacist manager" (5.00.70); CS dispensing framework incl. Schedule II handling and
nonresident compounded-CS limits (Rule 21 / 20.00.60); compounding codified in CO's own Rule 21.00.00;
internet pharmacies folded into the prescription-drug-outlet/nonresident framework (no separate class).

## Fields still "Needs legal review" — and WHY (important)

ALL provider (fullLicense, telehealthReg), ALL modality (video/audioOnly/async), relationship.inPerson/consent,
prescribing.inPersonRx, prescribing.pdmp (mandatory query), ecommerce.website/dtc. **REASON: the Colorado
Revised Statutes (CRS Title 12 Art. 240 medical practice, Art. 280 pharmacy; CRS 12-30-115 telehealth;
12-280-403/404 PDMP query mandate) are served as very large PDFs at content.leg.colorado.gov and were NOT read
this session.** The entire provider / telemedicine-practice / prescribing dimension lives in the CRS, not the
Board rules. CO is intentionally pharmacy-rule-only pending a dedicated CRS statute pass.

## Notable finding

Colorado regulates compounding via its **own** Rule 21.00.00 and references "USP/NF: the current edition" as a
compendial standard, but does **NOT adopt USP Chapters <795>/<797> by number** — confirmed by full-text search
of the 301-page rule ("795"/"797" return zero hits). This differs from states like WA/GA that adopt the USP
chapters explicitly.

## Follow-up

Fetch individual CRS article PDFs (or use the leg.colorado.gov statute browser to deep-link specific sections)
to unlock the provider/prescribing dimension and the PDMP mandatory-query mandate (CRS 12-280-403/404).

---

## Update 2026-07-21 — gap-fill pass (9 → 12 verified)

Read CRS Title 12 (2024 OLLS whole-title PDF, 1048pp) via pdf.js on leg.colorado.gov — the per-section CRS is Lexis-hosted/barred, so cite the OLLS title PDF. 3 CCR 719-1 (301pp) read via pdf.js on sos.state.co.us.

Newly verified:
- **prescribing.pdmp — GREEN.** §12-280-404(4)(a) "shall query the program prior to prescribing an opioid" + (a.5) "before prescribing a benzodiazepine" — mandatory-query-with-exceptions (hospital/SNF, cancer, palliative/hospice, post-surgical >14 days, disaster, single dose); technical-failure safe harbor in (4)(c).
- **fullLicense** §12-240-104 (telemedicine within the practice of medicine → full CO license).
- **modality.video** + **relationship.inPerson** §12-30-108 (telehealth standard-of-care parity; relationship "need not involve an in-person encounter" per 3 CCR 719-1 Rule 3.00.21).
- Pharmacy: **nonresident** Rule 2.00/5.00 (Non-Resident Prescription Drug Outlet), **pic** = "pharmacist manager," **onlinePharmacy** subsumed.

Still red (honest): telehealthReg (no separate telemedicine license), modality.audioOnly (§12-30-108 doesn't affirmatively name it; CO telehealth insurance defs are Title 10, EXCLUDED), modality.async, relationship.consent, prescribing.inPersonRx (DEA governs), pharmacy.csDispense, **compounding.stateReg (Rule 21 incorporates "current edition USP/NF" GENERALLY, NOT 795/797/800 by number)**, ecommerce.website, ecommerce.dtc.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — gap-fill attempted, NO change (stays 12/20)

The fillable reds (modality.async, relationship.consent under **CRS §12-30-108**; prescribing.inPersonRx) live only in the **CRS Title 12 OLLS whole-title PDF (~1,000 pp)** at content.leg.colorado.gov, which **would NOT initialize in this browser's PDF.js within the time budget** this session (same large-PDF choke as the NJ Pharmacy Act). No Justia/Wayback mirror exists — CO Title 12 was **renumbered in 2019** and only pre-renumber 2016 captures are archived; the per-section CRS is Lexis-hosted/barred. Left honest-red rather than guess. FOLLOW-UP: a ranged/section fetch of §12-30-108 (telehealth) + §12-280 (pharmacy CS) once the large PDF can be loaded, or a non-Lexis section mirror.
