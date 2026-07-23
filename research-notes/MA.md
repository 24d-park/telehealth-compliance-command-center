# Research Note — Massachusetts (MA)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 11 / 20  (7 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 9 / 20
- **Method:** Primary sources only, read directly in-browser on malegislature.gov (M.G.L.). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; malegislature.gov)

- **M.G.L. c.112 §5O — Telehealth (physician practice + definition)** — https://malegislature.gov/Laws/GeneralLaws/PartI/TitleXVI/Chapter112/Section5O
- **M.G.L. c.94C §24A — PMP (MassPAT) mandatory query** — https://malegislature.gov/Laws/GeneralLaws/PartI/TitleXV/Chapter94C/Section24A
- **M.G.L. c.112 §39H — Complex non-sterile compounding; manager of record; USP** — https://malegislature.gov/Laws/GeneralLaws/PartI/TitleXVI/Chapter112/Section39H

## Verified requirements

Telehealth by a board-licensed physician (§5O + §2); telehealth defined broadly to include interactive
audio-video, audio-only telephone, remote patient monitoring, online adaptive interviews, synchronous +
asynchronous (§5O(a)); MassPAT query required each time a Schedule II/III narcotic OR a benzodiazepine is
prescribed (c.94C §24A); separate complex non-sterile compounding license + adherence to "the most current
standards established by USP, all chapters" (§39H, robust post-NECC framework); manager of record for
compounding pharmacies (§39H(b)).

## Fields still "Needs legal review" — and WHY (important)

provider.telehealthReg, relationship.inPerson, relationship.consent, prescribing.inPersonRx,
pharmacy.nonresident, pharmacy.csDispense, ecommerce.* — all almost certainly resolve in **247 CMR**
(Board of Pharmacy) / **243 CMR** (Board of Medicine), which were **UNREACHABLE this session**: every
mass.gov CMR deep-link returned 404 and the site's internal search is JS-gated. No CMR text was read, so
nothing was asserted from it.

## Corrections made during verification

- **The common belief that M.G.L. c.112 §172 is a telehealth-consent statute is WRONG.** §172 is
  allied-mental-health/human-services confidentiality. The operative MA telehealth statute is **§5O**, which
  contains **no informed-consent clause** — consent likely sits in 243 CMR (unread), so relationship.consent
  is left red rather than mis-cited.
- §36A is wholesale drug business, NOT nonresident retail pharmacy licensure.

## Follow-up

A working mass.gov CMR path (or the Board's "Regulations and Laws" landing page) would unlock consent,
in-person, nonresident-pharmacy, PIC (general), and e-commerce fields.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — gap-fill attempted, NO change (stays 11/20)

Re-read **M.G.L. c.112 §5O** verbatim on malegislature.gov in full: it contains ONLY (a) the telehealth definition (already sourced) and (b) proxy credentialing/privileging — there is **NO informed-consent, in-person, or prescribing clause in the statute itself.** Those fields (relationship.consent, relationship.inPerson, prescribing.inPersonRx) plus pharmacy nonresident/csDispense/pic and e-commerce live in **243 CMR 2.00** (Board of Medicine) / **247 CMR** (Board of Pharmacy).

**Access:** mass.gov CMR deep-links 404 live; the only archived 243 CMR 2.00 capture on Wayback (2025 emergency reg, 6pp) covers just §§2.01–2.02 licensing — NOT the telemedicine §2.07 subsection. Left honest-red. FOLLOW-UP: a working 243 CMR 2.07 / 247 CMR path (the Board's "Regulations & Laws" landing page, or a non-404 mass.gov doc-id / its Wayback id_ capture).


---

## Update 2026-07-23 — laggard push wave 2 (11 -> 14 verified)

Accessed 243/247 CMR via the mass.gov Trial Court Law Library /doc PDF endpoints (the HTML deep-links still 404, but `https://www.mass.gov/doc/<slug>/download` serves the reg as a PDF — read via pdf.js). All quotes parent-verified verbatim.

Newly wired:
- **provider.telehealthReg** — 243 CMR 2.01: "Telemedicine means the provision of services to a patient by a physician from a distance by electronic communication..." + 2.01(4)(b) makes telemedicine part of the practice of medicine (requires MA license under M.G.L. c.112). NO separate telemedicine registration exists in 243 CMR 2.00 (full 54-page text searched: 0 hits for registration/distant-site/in-person). VERIFIED-NULL. [ma_243cmr2]
- **pharmacy.nonresident** — 247 CMR 6.02(4): "A pharmacy located outside of Massachusetts may not dispense or ship any controlled substance into Massachusetts unless it holds a non-resident Drug Store Pharmacy license." [ma_247cmr6]
- **pharmacy.csDispense** — 247 CMR 6.02(1) (Drug Store license required to dispense any CS) + 9.15(2) (pharmacist may not fill absent legitimate medical purpose + valid patient-practitioner relationship + authenticity + c.94C 19(a) compliance). Eff. 12-6-24. [ma_247cmr9]

**IMPORTANT — the high-value telemedicine practice standards DO NOT EXIST in the current 243 CMR 2.00 (Aug 9 2019 version).** The subagent verified this by full-text search of all 54 pages (0 hits for in-person / distant-site / online questionnaire / physician-patient relationship), not by a load failure. So relationship.inPerson, relationship.consent, prescribing.inPersonRx stay red as GENUINE SILENCE, not access failures. Likewise 247 CMR has NO internet/online-pharmacy chapter and NO website-disclosure or questionnaire rule (0 hits) — ecommerce.onlinePharmacy/website/dtc stay red as genuine absences.

Still red (6): relationship.inPerson, relationship.consent, prescribing.inPersonRx (243 CMR silent — would need 105 CMR 700 CS regs or a later telemedicine amendment); ecommerce.onlinePharmacy/website/dtc (247 CMR has no such provision). FOLLOW-UP: 105 CMR 700 (controlled substances) + 247 CMR 11 (CS Act registration) via the same /doc PDF path for any prescribing.inPersonRx rule.
