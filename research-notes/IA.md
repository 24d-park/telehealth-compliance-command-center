# Research Note — Iowa (IA)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 15 / 20  (11 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 5 / 20
- **Method:** Primary sources only. Subagent findings treated as leads and independently re-verified.

## SOURCING NOTE

legis.iowa.gov (the Iowa Code and the codified Iowa Administrative Code) was fully **WAF-blocked** this
session ("Web Page Blocked," Attack ID 20000051). So the rules were read from the official **Adopted-and-Filed
rulemaking documents on rules.iowa.gov** (ARC 9115C, 9337C, 9338C), which reproduce the exact adopted rule
text and effective dates — a valid primary state source, disclosed in every SOURCES entry.

**Structural change flagged:** a 2024–25 reorganization under Executive Order 10 moved the Board of Medicine
telemedicine rule to **653—13.9** (was 13.11, eff. May 21 2025) and the pharmacy rules to **DIAL [481]
Chapters 550/551/552** (was 657 IAC, eff. July 16 2025). The old citations are superseded.

## Sources checked (rules.iowa.gov)

- **653—13.9 — Standards of practice: telemedicine** — https://rules.iowa.gov/Notice/Details/9115C
- **481—Ch. 552 (practice; 552.22 compounding) + Ch. 551 (nonresident/PIC)** — https://rules.iowa.gov/Notice/Details/9338C

## Verified requirements

Full IA medical license (13.9(3)); telemedicine covers real-time interactive + asynchronous store-and-forward
(13.9(1)); no prior in-person visit required if standard of care allows (13.9(7)-(8)); **MANDATORY informed
consent**, timely documented (13.9(10)); no prescribing on an Internet questionnaire alone (13.9(8),(21));
nonresident pharmacy license + PIC (Ch. 551); compounding adopts **USP 795 (2023) / 797 (2023) / 800**
(552.22).

## Fields still "Needs legal review"

- **modality.audioOnly — EXCLUDED.** 13.9(1): "Telemedicine shall not include the provision of medical
  services only through an audio-only telephone..." (like TN/MD/OK). Red on the practice side.
- **prescribing.pdmp — voluntary.** The reachable rule (481 Ch. 556) is registration/reporting only
  ("access... available only to registered users"; "may authorize" delegates) with no "shall review before
  prescribing" verb — consistent with Iowa's historically voluntary PMP. (Underlying Iowa Code 124.552–.558
  couldn't be read — legis.iowa.gov WAF-blocked. Flag for re-check.)
- provider.telehealthReg (no separate registration), ecommerce.website, ecommerce.dtc.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.
