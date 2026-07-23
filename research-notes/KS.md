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


---

## Update 2026-07-23 (wave 5) — +1 (13 -> 14 verified)

**provider.telehealthReg wired** — K.S.A. 40-2,211(a)(2),(4) (Kansas Telemedicine Act, read verbatim on ksrevisor.gov): a telemedicine "healthcare provider" = a "physician" ("a person licensed to practice medicine and surgery by the state board of healing arts"), licensed PA/APRN, or a person authorized by the Behavioral Sciences Regulatory Board. Providers must already hold their underlying KS license; the Act creates NO separate telehealth registration. VERIFIED-NULL. Eff. Jan. 1, 2019 (L. 2018, ch. 98, §2). [ks_teleact]

Still red:
- relationship.consent — K.S.A. 40-2,212(d) is a conditional care-coordination REPORT ("shall send within three business days a report to such primary care or other treating physician"), NOT a consent-to-treat mandate; 40-2,212(b) allows telemedicine to establish the relationship. GENUINE red.
- prescribing.pdmp — K.S.A. 65-1685(c): "The board is hereby authorized to provide data ... to ... individuals authorized to prescribe" — PERMISSIVE access, no "shall review before prescribing." VOLUNTARY.
- prescribing.inPersonRx + compounding.stateReg — K.A.R. Art.100 (Healing Arts telemedicine prescribing) + Art.68 Art.13 (Board of Pharmacy compounding: 68-13-2/3/4). **BLOCKED: sos.ks.gov/kssos.org CloudFront-403; 68-13-3/4 have NO Wayback captures.** Honestly UNREAD — held, not guessed. FOLLOW-UP: current KS Board of Pharmacy regs PDF (not the stale 2014 book) + Board of Healing Arts Art.100 rulebook PDF; retry Wayback for pubs_kar_Regs.aspx?KAR=68-13-3/68-13-4 at other timestamps.
- ecommerce.website/dtc — same blocked K.A.R.; likely absent but unconfirmed.


---

## Update 2026-07-23 (wave 6) — KS K.A.R. unblock ATTEMPTED, no change (stays 14/20)

Tried to close the two K.A.R.-locked fields (compounding.stateReg = K.A.R. 68-13-3/4 Board of Pharmacy; prescribing.inPersonRx = K.A.R. Art.100 Board of Healing Arts). ALL access routes exhausted this session — documented so the next session doesn't re-walk them:

- **pharmacy.ks.gov** — bot-blocked ("Access Denied", title-level bot detection).
- **sos.ks.gov** (official K.A.R. viewer `pubs_kar_Regs.aspx?KAR=68-13-4`) — CloudFront-403 live; cross-origin fetch from archive.org origin = "Failed to fetch". Guessed compiled-PDF paths (`/publications/kar/2024/68.pdf`, `Article_68-13.pdf`, `Vol_2_Agency_68.pdf`) all fail.
- **Wayback** — "has not archived that URL" for 68-13-4 (confirmed via web.archive.org/web/2id_/). The KAR viewer's query-string URLs are essentially uncaptured; only the 68-13 ARTICLE INDEX and a few unrelated rules (68-21-2) have captures, not 68-13-3/4 or Art.100 bodies.
- **casetext.com** (free KAR reproduction) — now redirects to Westlaw/CoCounsel (paywalled); no readable body.
- **kslegislature.gov** — hosts STATUTES (K.S.A.) only, no K.A.R. administrative regulations.
- **Historical kansas.gov/pharmacy** — CDX shows no pharmacy regs PDFs (only old INK board agendas).

**Honest hold** (access-blocked, NOT a research gap): compounding.stateReg + prescribing.inPersonRx + ecommerce.website/dtc all live in the unreachable K.A.R. Do NOT guess the USP-adoption or telemedicine-prescribing text. FOLLOW-UP to close: obtain a CURRENT KS Board of Pharmacy "Pharmacy Act & Regulations" consolidated PDF (the 2014 book the subagent found is stale) or a current Board of Healing Arts Art.100 rulebook PDF from a direct download link, or retry sos.ks.gov when the CloudFront block lifts / from a residential-proxy session.
