# Research Note — Kentucky (KY)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 16 / 20  (12 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 4 / 20
- **Method:** Primary sources only. KRS served as PDFs on apps.legislature.ky.gov, read via in-browser PDF.js. Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; apps.legislature.ky.gov)

- **KRS 311.550(17) / 311.560 — telehealth definition + license required** — statute.aspx?id=48883
- **KRS 311.5975 — telehealth informed-consent duty** — statute.aspx?id=30539
- **KRS 218A.172 — mandatory KASPER query + exam before initial Sch II Rx** — statute.aspx?id=57302
- **KRS 315.0351 — out-of-state pharmacy permit, PIC, VIPPS website display** — statute.aspx?id=53707

## Verified requirements

Full KY license (KRS 311.560); telehealth = "interactive audio, video, or other electronic media" — covers
video/audio-only/async (KRS 311.550(17)); **informed consent required** — physician "shall ensure ...
informed consent ... is obtained before services are provided" (KRS 311.5975(1)(a)); nonresident/out-of-state
pharmacy permit + KY-licensed compliance pharmacist (KRS 315.0351).

## KASPER (verify-don't-assume win — confirmed MANDATORY)

**prescribing.pdmp and prescribing.inPersonRx are both verified from KRS 218A.172(1):** before the INITIAL
prescribing/dispensing of any Schedule II controlled substance, a practitioner "shall (a) Obtain a medical
history and conduct a physical or mental health examination ... and (b) Query the electronic monitoring
system established in KRS 218A.202 [KASPER]" (12-month lookback). I read the exact "shall ... Query" verb
rather than assuming — KY's KASPER is a genuine mandatory-query regime (as expected, but verified).

## Notable — a rare on-website display mandate

**ecommerce.website is verified (rare — only VA and KY so far).** KRS 315.0351(1): an out-of-state pharmacy
dispensing >25% of volume from Internet-solicited orders "shall receive and display in every medium in which
it advertises itself a seal of approval for the National Association of Boards of Pharmacy certifying that it
is a Verified Internet Pharmacy Practice Site (VIPPS)."

## Fields still "Needs legal review"

provider.telehealthReg, relationship.inPerson, compounding.stateReg, ecommerce.dtc — these live in the KY
Administrative Regulations (201 KAR 9 medical board / 201 KAR 2 pharmacy), which were NOT read this session
(the research subagent ran out of iterations before opening the KAR pages). Left red rather than assert
unread rule content. **Follow-up:** open 201 KAR 9:250 (telehealth) and 201 KAR 2:076 (compounding) to close
these four.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## FOLLOW-UP LEADS 2026-07-22 (wave-2 subagent, NOT yet parent-verified — do not wire until confirmed)

A research subagent retrieved these via KY statute-PDF stream decompression (apps.legislature.ky.gov). They are plausible but were NOT independently re-read by the parent this session, so they remain RED pending verification:
- **provider.telehealthReg** — KRS 311.5975 (id=30539): "A treating physician who provides or facilitates the use of telehealth shall ensure: (a) That the informed consent of the patient ... is obtained before services are provided through telehealth; and (b) That the confidentiality of the patient's medical information is maintained ...". Implies full-licensure ("treating physician"), no separate registration.
- **relationship.inPerson** — KRS 311.597(1)(e) (id=52966): bars questionnaire-only evaluation ("an electronic, on-line, or telephonic evaluation by questionnaire is inadequate for the initial evaluation") but does NOT mandate a prior in-person exam.
- compounding.stateReg (201 KAR 2:076 / 2:370) — subagent could NOT retrieve (KAR PDF endpoints 404/HTML-wrapper); USP adoption unverified.
TO VERIFY: re-open KRS 311.5975 + 311.597 PDFs (DecompressionStream on the FlateDecode stream) or their Wayback id_ captures, confirm text, then wire telehealthReg + relationship.inPerson.


## RE-VERIFIED 2026-07-22 — +2 fields wired (16 -> 18/20)

Parent independently re-read both KY statute PDFs via pdf.js on apps.legislature.ky.gov (confirming the wave-2 subagent lead above):
- **provider.telehealthReg (WIRED):** KRS 311.5975(1) verbatim — a "treating physician who provides or facilitates the use of telehealth" practices under KY licensure; no separate telehealth registration. [ky_3115975]
- **relationship.inPerson (WIRED):** KRS 311.597(1)(e) verbatim — proper relationship requires identity verification + documented diagnosis + current medical record; "an electronic, on-line, or telephonic evaluation by questionnaire is inadequate for the initial evaluation ... or for any follow-up evaluation"; NO prior in-person exam mandated. [ky_311597]

Still red (2): compounding.stateReg (201 KAR 2:076 / 2:370 — KAR PDF endpoints returned 404/HTML-wrapper, unreachable), ecommerce.dtc.
