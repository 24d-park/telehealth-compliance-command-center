# Research Note — Louisiana (LA) — statute-only (board rules not machine-readable)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 10 / 20  (6 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 10 / 20
- **Method:** Primary sources only, read directly in-browser on legis.la.gov (LA Revised Statutes via Law.aspx?d=ID dynamic pages; body via console). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; legis.la.gov)

- **La. R.S. 40:1223.4 — Telehealth practice standards** (out-of-state registration, audio-only, in-person, CS) — https://legis.la.gov/Legis/Law.aspx?d=964869
- **La. R.S. 40:1223.3 — Telehealth definitions** (synchronous, async store-and-forward) — https://legis.la.gov/Legis/Law.aspx?d=964868
- **La. R.S. 40:1007 — PMP access** (voluntary "may access") — https://legis.la.gov/Legis/Law.aspx?d=409422

## Verified requirements (R.S. 40:1223.x, Acts 2023 No. 322, eff. Jan. 1 2024)

Out-of-state telehealth-provider licensing/registration framework (B)(3); synchronous video + asynchronous
store-and-forward defined (§1223.3); audio-only permitted if standard of care met (B)(7); no prior in-person
exam required for a telehealth encounter (B)(5); **CS via telehealth requires a prior in-person exam** except
in a LA-licensed DEA-registered facility per R.S. 37:1271.1 (B)(6).

## IMPORTANT PDMP finding (verify-don't-assume win)

**prescribing.pdmp left "Needs legal review" — LA's PMP query is VOLUNTARY.** R.S. 40:1007(E): prescribers
"may access" the PMP. The only "shall review" in the section is the BOARD reviewing data for enforcement —
NOT a prescriber pre-prescribing query mandate. Verified the exact verbs directly rather than assume.

## Also notable

The former standalone LA telemedicine-license statute (R.S. 37:1276.1) was **REPEALED** by Acts 2023 No. 322;
telehealth is now governed by the R.S. 40:1223.x framework plus board rules.

## Fields still "Needs legal review" (not reached / not machine-readable)

- provider.fullLicense — La. R.S. Title 37 Ch. 15 medicine licensure section not individually read.
- relationship.consent — likely in the LSBME telemedicine rule LAC 46:XLV.7501 et seq., but that rule PDF
  rendered in a Chrome viewer with **no extractable text layer** this session.
- pharmacy.nonresident, pharmacy.csDispense, pharmacy.pic, compounding.stateReg, ecommerce.onlinePharmacy/
  website/dtc — LA Board of Pharmacy rules (LAC 46:LIII) and Title 37 Ch. 14 pharmacy statutes not reached.

## Follow-up to unblock

Retrieve the LSBME telemedicine rule (LAC 46:XLV.7501 et seq.) and pharmacy.la.gov / LAC 46:LIII rule PDFs
via a PDF-text-capable method (PDF.js worked for other states' PDFs; the LSBME storyblok PDF specifically
lacked a text layer — try the Office of State Register compiled LAC or an OCR pass).

---

## Update 2026-07-21 — gap-fill pass (10 → 11 verified)

Statutes read verbatim on legis.la.gov. **STRUCTURAL CATCH:** LA's telehealth practice standard is NOT R.S. 37:1271 (which merely defers to it) and NOT the insurance title — it's the **Louisiana Telehealth Access Act, R.S. 40:1223.1 et seq.** (Title 40 Public Health), amended Acts 2023 No. 322 eff. 1/1/2024.

Newly verified:
- **fullLicense** §37:1271; **provider.telehealthReg** §40:1223.4(B)(3) (out-of-state provider with "unrestricted and unencumbered license in good standing" — a genuine pathway); **modality.video** §1223.3(5)-(6); **modality.audioOnly** §1223.4(B)(7) ("may use interactive audio without ... video if ... able to meet [standard of care]" — conditional); **modality.async** §1223.3(1); **relationship.inPerson** §1223.4(B)(5) (no prior in-person, must arrange referral); **prescribing.inPersonRx** §1223.4(B)(6)+§37:1271.1 (CS needs in-person history/exam unless DEA-registered facility).

PDMP finding: **prescribing.pdmp LEFT RED** — R.S. 40:1007 verb is "may access" (voluntary at statute level). Per the banked lesson, a Board-rule mandate might exist, but the LA Board sites were 404 (mid-redesign) this session, so it could NOT be confirmed — left red rather than assume.

Still red (LAC Title 46 Board of Pharmacy site 404 this session): relationship.consent, pharmacy.nonresident, pharmacy.csDispense, pharmacy.pic, compounding.stateReg, ecommerce.onlinePharmacy, ecommerce.website, ecommerce.dtc. FOLLOW-UP: LAC Title 46 Part LIII via doa.la.gov/doa/osr (Office of State Register) once the Board redesign settles.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.
