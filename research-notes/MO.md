# Research Note — Missouri (MO)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 16 / 20  (12 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 4 / 20
- **Method:** Primary sources only. Statutes read directly on revisor.mo.gov (text renders inline); CSR admin rules read from the official SOS PDF (s1.sos.mo.gov) via in-browser PDF.js. Subagent findings treated as leads and independently re-verified.

## Sources checked (primary)

- **Mo. Rev. Stat. §191.1145 — telehealth definitions + full licensure** — https://revisor.mo.gov/main/OneSection.aspx?section=191.1145
- **§191.1146 / §334.108 — relationship + no questionnaire-only Rx** — https://revisor.mo.gov/main/OneSection.aspx?section=334.108
- **§195.600 — statewide PDMP** — https://revisor.mo.gov/main/OneSection.aspx?section=195.600
- **§338.220 — pharmacy permit classes (incl. Class K Internet)** — https://revisor.mo.gov/main/OneSection.aspx?section=338.220
- **20 CSR 2220-2 — Board of Pharmacy rules (PIC, nonresident, compounding)** — https://www.sos.mo.gov/cmsimages/adrules/csr/current/20csr/20c2220-2.pdf

## Verified requirements

Full MO licensure to treat MO patients via telemedicine (§191.1145.3); telehealth includes audiovisual,
**audio-only** (added 2025 S.B. 79), and asynchronous store-and-forward; relationship may be established via
telemedicine (§191.1146); valid relationship + adequate exam required before prescribing, no telephone-only Rx
(§334.108); **explicit DTC prohibition — no Rx "based solely on an internet request or an internet
questionnaire" (§334.108.4)**; nonresident pharmacy license + Class K Internet permit (§338.220, 20 CSR
2220-2.025); PIC (2220-2.090); USP 797 (sterile) + 795 (non-sterile) adopted (2220-2.200/.400).

## IMPORTANT PDMP finding (verify-don't-assume win)

**prescribing.pdmp is left "Needs legal review" because Missouri's PDMP query is VOLUNTARY, not mandatory.**
Missouri was the LAST state in the country to establish a statewide PDMP (2021 S.B. 63). The statute
(§195.600.8) says prescribers "shall be **permitted to** access" dispensation information — access is
authorized but there is **no mandatory-query duty** before prescribing. I verified the exact "shall be
permitted to access" language directly rather than assuming a mandate. Marking this green would have been
a false compliance obligation.

## Other fields still "Needs legal review"

- relationship.consent — only an assistant-physician collaborative-practice rule (20 CSR 2150-2.240) requires
  telehealth consent; there is no general all-provider telehealth informed-consent mandate.
- provider.telehealthReg — only narrow §191.1145.4 exemptions from full licensure; no separate registration.
- ecommerce.website — no on-website display mandate (§338.080 display applies to the physical premises).

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 (wave 2) — +1 field (16 -> 17/20)

- **provider.telehealthReg (wired):** RSMo 191.1145.3 read verbatim on revisor.mo.gov: "In order to treat patients in this state through the use of telemedicine or telehealth, health care providers shall be fully licensed to practice in this state and shall be subject to regulation by their respective professional boards." No separate telehealth registration; §191.1145.4 exempts only informal/emergency/episodic out-of-state consultation. [mo_1911145]

Still red (3): relationship.consent — §191.1146 imposes an interview/exam duty + a questionnaire ban ("A questionnaire completed by the patient ... does not constitute an acceptable medical interview and examination") but has NO standalone informed-consent clause, so left red rather than mislabel an exam duty as consent. prescribing.pdmp — revisor.mo.gov anti-bot ("No FISHING") blocked RSMo 195.700 (statewide PDMP); mandatory-query verb unverified. ecommerce.website — genuine null.
