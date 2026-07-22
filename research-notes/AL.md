# Research Note — Alabama (AL) — pharmacy-rules-only (telehealth statute unreadable)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 8 / 20  (4 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 12 / 20
- **Method:** Primary sources only. Subagent findings treated as leads and independently re-verified.

## SOURCING NOTE (why AL is thin — honest outcome)

The official **Alabama statute host (alison.legislature.state.al.us) is a JavaScript-gated SPA that renders
ZERO statutory text** — I confirmed directly that the page DOM contains only navigation chrome, no code text.
So Alabama's **2022 telehealth act (§34-24-701 et seq.) is UNREADABLE** from a primary source this session.
Compounding the problem, Alabama's Board of Medical Examiners telehealth rules were **REPEALED** (540-X-15
Telehealth on 12/23/2015; 540-X-16 Practice Across State Lines on 10/15/2022) and folded into that statute —
so the administrative code no longer carries the operative telehealth practice standards. **Per the
non-fabrication rule, I did NOT cite Justia or any aggregator** for the blocked statute, and left all
telehealth fields red.

## Sources checked & VERIFIED (official Alabama Administrative Code — admincode.legislature.state.al.us)

- **680-X-2-.07 — Mail Order Prescriptions / nonresident registration** — pharmacy.nonresident
- **680-X-2-.12 — Supervising Pharmacist (PIC)** — pharmacy.pic
- **680-X-2-.43 — Requirements for Compounding (adopts USP-NF by reference)** — compounding.stateReg
- **680-X-2-.33 — Internet Pharmacies** — ecommerce.onlinePharmacy

Verified requirements: no nonresident pharmacy may ship/mail/deliver into AL "unless registered by the
Alabama State Board of Pharmacy" (680-X-2-.07); every pharmacy "under direct supervision and control of a
registered Pharmacist ... designated the supervising pharmacist" (680-X-2-.12); compounding "shall comply
with all applicable and current regulations of USP-NF" (680-X-2-.43); internet dispensing requires a
"reasonable effort" to confirm a legitimate purpose + valid patient-practitioner relationship (680-X-2-.33).

## Fields "Needs legal review" (all telehealth — statute unreadable)

provider.fullLicense, provider.telehealthReg, modality.video/audioOnly/async, relationship.inPerson/consent,
prescribing.inPersonRx, prescribing.pdmp (§20-2-210 mandatory-query verb unreadable), ecommerce.dtc,
ecommerce.website.

## Follow-up to unblock

Read §34-24-701 et seq. (telehealth act) and §20-2-210 (PDMP) via a JS-executing browser with a residential
proxy, or a curl-capable environment — the alison.legislature.state.al.us SPA needs JS execution to hydrate.
Do NOT re-dispatch AL to a browser-only subagent for the statutes; it will fail the same way.

---

## Update 2026-07-21 — gap-fill pass (8 → 18 verified)

The alison.legislature.state.al.us SPA DID hydrate this session (DOM extraction worked after all), so the telehealth statute was read verbatim. **STRUCTURAL CATCH:** governing law is Title 34 ch. 24 **Article 12** (§§34-24-700 to 707, Act 2022-302, eff. 7/11/2022) — SUPERSEDED the repealed BME rule chapter 540-X-15. (The subagent's "Article 11" was wrong.)

Verified verbatim this pass:
- **fullLicense** §34-24-702(a) — full AL license required to treat AL patients via telehealth.
- **telehealthReg** — NONE; §702(b) is an *exemption* for irregular/infrequent out-of-state MDs (<10 days OR <10 patients/yr), not a registry.
- **modality.video / audioOnly** §701(13): "SYNCHRONOUS ... via audio/visual technologies, **audio only technologies**, or other means" — audio-only PERMITTED (and allowed for CS if synchronous, §704(b)(1)a).
- **modality.async** §701(1) — permitted for telehealth generally, NOT for CS.
- **relationship.inPerson** §703(d) — "may be formed without a prior in-person examination" BUT >4 telehealth visits/12 mo same unresolved condition → physician "shall ... See the patient in person."
- **relationship.consent** §703(e)(4) — MANDATORY, documented.
- **prescribing.inPersonRx** §704(b) — CS Rx needs synchronous audio/AV + "at least one in-person encounter with the patient within the preceding 12 months."
- **prescribing.pdmp — GREEN via Board rule.** Statute §20-2-214(a)(2) is voluntary ("no requirement or obligation ... However, the ... boards may impose ... by rule"), but BME rule **540-X-4-.09** imposes a dose-tiered mandate: >30 MME/day "shall review ... at least two (2) times per year"; >90 MME/day "shall query ... every time a prescription ... is written."
- **pharmacy.nonresident** §34-23-30 + AAC 680-X-2-.07(2); **pic** 680-X-2-.12; **compounding** 680-X-2-.43 (current USP-NF by reference, NOT 795/797/800 by number); **onlinePharmacy** 680-X-2-.33.

Still red (honest): pharmacy.csDispense (680-X-3 chapter-level), ecommerce.website, ecommerce.dtc (implied by relationship/legitimate-purpose standard; no verbatim questionnaire ban).

**Lesson banked:** alison.legislature.state.al.us DOES hydrate in this browser stack — read via DOM extraction (document.body.innerText) after navigate; earlier "needs residential proxy" note was overly pessimistic.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — gap-fill attempted, NO change (stays 18/20)

Target was pharmacy.csDispense (AAC 680-X-3 controlled-substance dispensing). **admincode.legislature.state.al.us did NOT hydrate this session** — fetch returns only "You need to enable JavaScript to run this app" and navigate timed out with an empty DOM. NOTE: the 680-X-2 pharmacy rules DID hydrate in the 2026-07-21 session, so this is an intermittent SPA-hydration issue, not a permanent block. ecommerce.website/dtc remain genuine gaps (no verbatim on-website-display or questionnaire-ban rule located; dtc is implied only by the relationship/legitimate-purpose standard). Left honest-red. FOLLOW-UP: retry AAC 680-X-3 via navigate when the SPA hydrates.
