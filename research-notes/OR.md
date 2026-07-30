# Research Note — Oregon (OR)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 13 / 20  (9 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 7 / 20
- **Method:** Primary sources only. Subagent findings treated as leads and independently re-verified.

## SOURCING NOTE (important)

The official Oregon hosts were **not usable this session**: oregonlegislature.gov serves ORS chapters as
empty HTML shells (the text lives only in per-chapter PDFs whose paths 404'd), and the SOS OARD
(secure.sos.state.or.us/oard) **bot-blocked every request** ("Please Contact Us"). So the ORS/OAR text was
read via the **Open Law Library verbatim reproduction (oregon.public.law)**, which reproduces the official
text and cites the authoritative secure.sos.state.or.us / oregonlegislature.gov source URL on each page.
This is disclosed in every SOURCES entry — the same honest approach used for TN (Internet Archive captures).
A downstream verifier should confirm against the official SOS OARD links when the host is reachable.

## Sources checked

- **ORS 677.494 — Telemedicine; where practice occurs** (eff. June 6 2024) — https://oregon.public.law/statutes/ors_677.494
- **ORS 677.137 / 677.139 — cross-state-lines medicine license** — https://oregon.public.law/statutes/ors_677.139
- **OAR 855-045-0200 — compounding; USP 795/797/800** — https://oregon.public.law/rules/oar_855-045-0200
- **OAR 855-041-1060 — non-resident pharmacies; OR-licensed PIC** — https://oregon.public.law/rules/oar_855-041-1060

## Verified requirements

OR licensure required to treat OR patients (practice "occurs where the patient is physically located,"
ORS 677.494); telemedicine includes synchronous (real-time) and asynchronous modalities; relationship may be
established via telemedicine, provider need not be in-state (no in-person mandate); **a genuine cross-state-
lines medicine license** issued by the Oregon Medical Board (ORS 677.139); compounding drug-outlet
registration + **USP 795/797/800 adopted by rule** (OAR 855-045-0200); non-resident pharmacy registration +
Oregon-licensed PIC (OAR 855-041-1060) — also the licensure basis for mail-order/internet pharmacies.

## IMPORTANT PDMP finding (verify-don't-assume win)

**prescribing.pdmp is left "Needs legal review" because Oregon does NOT mandate a PDMP query.** ORS 431A.877
requires practitioners to **register** with the PDMP, but there is no statutory duty to check it before
prescribing. Registration is compelled; query is not. Verified directly rather than assumed.

## Other fields still "Needs legal review"

- modality.audioOnly — ORS 677.494 defines telemedicine broadly but does not separately name or permit
  audio-only; NOT FOUND as an explicit rule.
- relationship.consent — no telehealth-specific informed-consent statute/rule located in ORS 677 / OAR 847-025.
- prescribing.inPersonRx — no discrete controlled-substance in-person mandate (the closest is the cross-state
  OAR 847-025 internet-only prohibition).
- ecommerce.website — no on-website display mandate located.
- ecommerce.dtc — the only internet-questionnaire prohibition read is in the cross-state-lines OAR 847-025
  preamble; too provider-class-specific to assert as a general rule, so left red.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


---

## Update 2026-07-23 (wave 5) — +1 (13 -> 14 verified); OR at honest ceiling

**pharmacy.csDispense wired** — OAR 855-080-0085(1) (Board of Pharmacy Division 80), read verbatim on oregon.public.law (official OARD host bot-blocked): "the provisions of 21 CFR 1306.01 through 1306.27 and 1304.03(d) shall be complied with by the registrants, practitioners and pharmacists as specified therein in the issuance, preparation, labeling dispensing, recordkeeping and filing of prescriptions for controlled substances." Mandatory "shall." [or_855080]

The other 6 reds are CONFIRMED GENUINE ABSENCES (verbatim-verified where a rule exists), not access failures:
- modality.audioOnly — ORS 677.494(1) defines telemedicine as synchronous/asynchronous "electronic communications" generically; audio-only never named/permitted/addressed.
- relationship.consent — no telehealth consent statute/rule (ORS 677.494 silent; OAR ch.847 div.25 has only records/confidentiality + cross-state limits).
- prescribing.inPersonRx — ORS 677.494(2) permits telemedicine prescribing with NO in-person prerequisite.
- prescribing.pdmp — ORS 431A.877 compels REGISTRATION only ("shall register"); query VOLUNTARY. Re-confirmed verbatim.
- ecommerce.website — no on-website display mandate.
- ecommerce.dtc — OAR ch.847 div.25 is titled "Rules for Licensure to Practice Medicine Across State Lines" and applies solely to out-of-state licensees; no general questionnaire ban.


## UPDATE 2026-07-29 — final-research wave 1, +1 field (14 -> 15/20)
Subagent lead, parent-verified verbatim on oregonlegislature.gov.
- **prescribing.inPersonRx** — ORS 677.494(2): telemedicine may be used "including ... the prescription of
  drugs, to a patient physically located in this state," provider "not required to be physically located in
  this state." Prescribing via telemedicine is EXPRESSLY authorized — no in-person exam mandate. Reused
  existing or_677494 source. (Note: current official text says "physician associate," not "physician
  assistant.")
### Confirmed HOLDS (subagent validated the red calls — no change)
- prescribing.pdmp — decisively NOT a query mandate: ORS 431A.877 is registration-only, and ORS 431A.865(8)
  EXPLICITLY states "Nothing ... requires a practitioner or pharmacist who prescribes or dispenses ... to
  obtain information about a patient from the [PDMP]." Textbook voluntary. Stay red.
- relationship.consent — no telemedicine informed-consent mandate in ORS 677.494 or OAR 847-025. Absence.
- modality.audioOnly — only inferable from "electronic communications," not explicitly named. Hold red.
(provider.telehealthReg was ALREADY green — OR has the ORS 677.139 cross-state-lines license; not re-touched.)

## UPDATE 2026-07-30 — gap-fill wave, NO CHANGE (stays 15/20) — one HELD lead for next session
Subagent lead, parent-reviewed. NOTHING wired (primary source blocked / not a clean null).
- **ecommerce.dtc → HELD LEAD (mirror-only, ready to wire).** OAR **847-025-0000(2)(d)**: a cross-state-lines
  physician "shall refrain from writing prescriptions for medication resulting only from a sale or consultation
  over the Internet" (+ (2)(a) establish physician-patient relationship, (2)(b) objective clinical judgment).
  That IS a genuine internet/DTC-prescribing bar. BUT it was read ONLY on the public.law mirror — the official
  SOS OARD (secure.sos.state.or.us/oard/) is bot-blocked ("Please Contact Us") and the query-string rule URL is
  NOT archived on Wayback (CDX returned zero captures). Per the mirror-only rule, do NOT wire off public.law
  alone. TO WIRE next session: pull OAR 847-025-0000 from the official SOS page (residential egress) OR the
  Oregon Medical Board rules PDF, confirm (2)(d) verbatim + effective date, then green with a new key or_847_025.
  CAVEAT: OAR 847-025 is the "Practice of Medicine Across State Lines" division — scoped to out-of-state
  physicians, not general in-state telemedicine; note that scope when wiring.
  RE-ATTEMPTED 2026-07-30 (parent): SOS OARD is hard-blocked for THIS stack too (viewSingleRule.action →
  "Please Contact Us" wall; ruleVrsnRsn guess failed) and no Wayback capture exists. The official OMB
  "Statement of Philosophy – Telemedicine" (oregon.gov/omb/board/Philosophy, adopted 2012, amended through Apr
  2024) DOES restate the bar — "Treatment based solely on an online questionnaire without individualized review
  and assessment does not constitute an acceptable standard of care" — which corroborates the rule is real, BUT
  a Statement of Philosophy is NON-BINDING GUIDANCE, not a rule/statute, so it does NOT clear the greening bar
  (same rule that rejects guidance-only consent). Still HELD until the binding OAR 847-025-0000(2)(d) text is
  read on a non-blocked authoritative source (residential-egress SOS page, or an official OMB rules PDF).
- **modality.audioOnly → stays RED.** Verified absent within OAR 847-025 (all 7 rules read), but that division
  is cross-state-lines-scoped, so the absence is not a clean general verified-null. OR's general telemedicine
  modality standard, if any, would live elsewhere (ORS 677.495–.535 / a different OMB division) — not yet read.
