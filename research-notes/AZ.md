# Research Note — Arizona (AZ)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 17 / 20  ·  **Needs legal review:** 3 / 20  (richest state to date)
- **Method:** Primary sources only, read directly in-browser on azleg.gov (Arizona Revised Statutes, Titles 32 & 36; body text via console innerText). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; azleg.gov)

- **A.R.S. §36-3601 — Telehealth definitions** — https://www.azleg.gov/ars/36/03601.htm
- **A.R.S. §36-3602 — Delivery of health care through telehealth; requirements; exceptions** — https://www.azleg.gov/ars/36/03602.htm
- **A.R.S. §36-3606 — Interstate telehealth services; registration** — https://www.azleg.gov/ars/36/03606.htm
- **A.R.S. §36-2606 — CSPMP registration/mandatory use** — https://www.azleg.gov/ars/36/02606.htm
- **A.R.S. §32-1929 — Biennial registration of pharmacies** — https://www.azleg.gov/ars/32/01929.htm
- **A.R.S. §32-1961 — Limit on dispensing/compounding/sale (pharmacist in active personal charge)** — https://www.azleg.gov/ars/32/01961.htm
- **A.R.S. §32-1901 — Definitions (pharmacist in charge)** — https://www.azleg.gov/ars/32/01901.htm

## Verified requirements (13 state-sourced + federal-framework inheritance)

Out-of-state provider may treat AZ patients by REGISTERING with the applicable AZ board (§36-3606,
<10-encounter exemption) — a genuine telehealth registration, unlike most states; telehealth def
covers audio/video/store-and-forward (§36-3601), audio-only only when audio-visual not reasonably
available; informed consent required + documented (§36-3602(A)); no in-person exam mandate EXCEPT
Schedule II drugs + federal law (§36-3602(E)); CSPMP 12-month report before opioid/benzo Sch II-IV,
quarterly (§36-2606); biennial registration of any place from/which drugs dispensed incl. out-of-
state & online (§32-1929); pharmacist in active personal charge / PIC (§32-1961(B), §32-1901).

## Fields still "Needs legal review"

- compounding.stateReg, ecommerce.website, ecommerce.dtc — all live in AZ Administrative Code Title 4
  Ch. 23 (Board of Pharmacy R4-23), which was **Cloudflare-blocked ("Just a moment…")** this session.

## Notes / corrections made during verification

- Corrected two bad citations from the research hints: **§32-1863 is NOT the PIC statute** (PIC is
  §32-1901 def + §32-1961(B)), and **§32-1910 is emergency dispensing, not compounding.**
- azleg.gov statute pages show no inline effective/amended date in the body — each source notes this.
- AZ Admin Code (apps.azsos.gov) needs a non-Cloudflare-blocked path to finish the 3 remaining fields.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.
# Research Note — Arizona (AZ)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

## FOLLOW-UP LEAD 2026-07-22 (wave-2 subagent; parent could not re-verify — PDF too large to load this session)

A research subagent extracted the AZ Board of Pharmacy rules (A.A.C. Title 4 Ch. 23) from a Wayback id_ raw capture of the official azsos.gov PDF (web/20201016174410id_/https://apps.azsos.gov/public_services/Title_04/4-23.pdf) and reported:
- **ecommerce.dtc — PROHIBITED** — A.A.C. R4-23-404(F): "A pharmacist shall not dispense a drug from a prescription order if the pharmacist has knowledge, or reasonably should know under the circumstances, that the prescription order was issued on the basis of an internet-based questionnaire or an internet-based consultation without a medical practitioner-patient relationship as defined in R4-23-110." — a genuine questionnaire-only dispensing ban.
- compounding.stateReg — R4-23-670 uses ISO Class 5/7 air-cleanliness standards, NOT USP 795/797/800 by number (subagent found no USP incorporation in the 2020 capture).

STATUS: NOT wired — the 543K-char Title 4 PDF would not finish loading in the parent browser this session for independent re-read. TO VERIFY: load the Wayback PDF via pdf.js and scan pages ~15-45 for "internet-based questionnaire" (R4-23-404(F)); if confirmed verbatim, wire ecommerce.dtc = PROHIBITED. A current (2025) capture also exists for reconfirmation.


## RE-VERIFY ATTEMPT 2026-07-22 — FAILED, ecommerce.dtc stays HELD (red)

Parent tried to independently confirm the R4-23-404(F) questionnaire-ban quote but could NOT:
- Wayback id_ raw capture of the Title 4 PDF (web/20201016174410id_/.../4-23.pdf) would not finish loading/parsing in this browser stack (the ~543K-char doc stalls pdf.js; a raw fetch()->arrayBuffer also dropped the session twice mid-transfer).
- Live apps.azsos.gov AND pharmacy.az.gov are BOTH Cloudflare bot-walled ("Just a moment...").
- No per-section HTM capture exists in Wayback.
STATUS: The subagent's verbatim quote is specific and plausible (R4-23-404(F): pharmacist "shall not dispense ... issued on the basis of an internet-based questionnaire or an internet-based consultation without a medical practitioner-patient relationship"), but per the non-fabrication rule it stays RED until a human/parent reads it verbatim. TO RETRY: a residential-proxy browser (to clear azsos.gov Cloudflare) or a curl-capable environment fetching the Wayback PDF, then pdf.js/pdftotext scan for "internet-based questionnaire".
