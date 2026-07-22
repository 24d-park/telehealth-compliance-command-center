# Research Note — Kansas (KS)

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

- **Date checked:** 2026-07-20
- **Verified fields:** 12 / 20  (8 state-sourced + 4 federal-framework inherited)  ·  **Needs legal review:** 8 / 20
- **Method:** Primary sources only, read directly on ksrevisor.gov (official KS statutes; body via console). Subagent findings treated as leads and independently re-verified.

## Sources checked (primary; ksrevisor.gov)

- **Kansas Telemedicine Act K.S.A. 40-2,211** (definitions) — https://www.ksrevisor.gov/statutes/chapters/ch40/040_002_0211.html
- **K.S.A. 40-2,212** (relationship, standards) — https://www.ksrevisor.gov/statutes/chapters/ch40/040_002_0212.html
- **Pharmacy Act K.S.A. 65-1643** (registration; CS; PIC) — https://www.ksrevisor.gov/statutes/chapters/ch65/065_016_0043.html

## Verified requirements

Full state licensure for telemedicine providers (40-2,211(a)); telemedicine = "real-time two-way interactive
audio, visual, or audio-visual ... secure video conferencing or store-and-forward technology" (video + async);
relationship may be established via telemedicine — no prior in-person visit (40-2,212(b)); nonresident pharmacy
registration (65-1626(uu) + 65-1643(a)); CS dispensing controls (65-1643(j),(k)); pharmacist-in-charge
(65-1626 + 65-1643(a)).

## Fields still "Needs legal review"

- **modality.audioOnly — EXCLUDED.** 40-2,211(a) excludes telemedicine "that consists solely of a telephone
  voice-only conversation, email or facsimile."
- **prescribing.pdmp — voluntary.** K-TRACS: dispenser *reporting* is mandatory (65-1683 "shall submit"), but
  prescriber *access* is permissive — 65-1685(c) "the board ... is hereby authorized to provide data" to
  prescribers. No "shall review before prescribing" verb in statute.
- **relationship.consent** — only a conditional care-coordination *report* (40-2,212(d)), not a blanket
  consent-to-treat mandate.
- **prescribing.inPersonRx, compounding.stateReg** — live in the K.A.R. (Board of Healing Arts Art. 100 /
  Board of Pharmacy Art. 68), and **the K.A.R. host sos.ks.gov returned CloudFront 403 all session**, so those
  regulation-only fields are red rather than guessed.
- provider.telehealthReg (no separate registration), ecommerce.website, ecommerce.dtc.

## Follow-up to unblock

Retry the K.A.R. host (sos.ks.gov) for Art. 68 (compounding/USP) and Art. 100 (telemedicine prescribing) when
reachable.

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.


## UPDATE 2026-07-22 — +1 field (12 -> 13/20)

- **modality.audioOnly — EXCLUDED (now wired).** K.S.A. 40-2,211(a)(5): telemedicine "does not include communication ... that consist[s] solely of a telephone voice-only conversation, email or facsimile transmission." Audio-only cannot be the sole modality. Reused existing `ks_teleact` source (same statute section), read verbatim on ksrevisor.gov.

### Still red (7) — honest
- prescribing.inPersonRx + compounding.stateReg — K.A.R. (Board of Healing Arts Art. 100 / Board of Pharmacy Art. 68). sos.ks.gov is reachable this session but the K.A.R. deep-link path 404s and cross-origin fetch is blocked; individual reg text not read.
- relationship.consent — 40-2,212(d) is only a conditional care-coordination *report*, not a consent-to-treat mandate (genuine, not access).
- prescribing.pdmp — K-TRACS prescriber access is permissive (65-1685(c) "authorized to provide"), no "shall review before prescribing" (genuine).
- provider.telehealthReg (no separate registry), ecommerce.website, ecommerce.dtc.
FOLLOW-UP: K.A.R. Art. 68 (compounding) + Art. 100 (telemedicine prescribing) via a working sos.ks.gov path or Wayback.
