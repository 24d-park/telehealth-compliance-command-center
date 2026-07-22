# Telehealth Compliance — Research Notes

> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.

Per-state research notes backing the compliance tracker (`../index.html`). Each note records:
sources checked (primary, deep-linked), date checked, exact citations for verified fields,
fields still needing legal review, unclear/open questions, and a pharmacist/attorney review checklist.

## Research standard (applied to every note)
Primary sources only, in priority order: state board of pharmacy → state statutes / administrative
code → state medical board → state telehealth statutes/rules → state PDMP agency; DEA / FDA / HHS /
USP for federal layers. No blogs, vendor pages, or LLM answers. Every clickable source deep-links
to the specific rule/statute section/document — never a homepage or search result.

## Coverage status (regenerated 2026-07-22)
**50 of 51 jurisdictions have state-specific sourced fields. Indiana is now PARTIAL** (5 telehealth
fields sourced 2026-07-22 via the Justia reproduction of the official Indiana Code, read through
Internet Archive `id_` raw captures, because the primary host iga.in.gov is an un-hydratable JS SPA).
"Verified / 20" counts state-specific fields backed by a primary source (federal/USP framework
defaults every state inherits are not counted here). Where a count reads via a note's own tally it
may differ by the ±2 federal defaults; see each note for the exact breakdown.

| State | Verified / 20 | Notes |
|---|---|---|
| [Alaska](AK.md) | 14 / 20 |  |
| [Alabama](AL.md) | 18 / 20 | Telehealth statute §34-24-700 et seq. + pharmacy AAC 680-X-2 (2026-07-21); csDispense/e-commerce red (AAC 680-X-3 SPA won't hydrate) |
| [Arkansas](AR.md) | 15 / 20 | UNBLOCKED 2026-07-22 via Justia/Wayback id_ (AR Telemedicine Act 17-80-402/403/404); Rx section 405 not archived |
| [Arizona](AZ.md) | 17 / 20 |  |
| [California](CA.md) | 18 / 20 | +csDispense (HSC 11200); telehealthReg left red (not exhaustively surveyed); website genuine null |
| [Colorado](CO.md) | 12 / 20 | Telehealth CRS 12-30-108 fields locked in 1,000pp OLLS PDF (won't load); no mirror (Title 12 renumbered 2019) |
| [Connecticut](CT.md) | 16 / 20 |  |
| [District of Columbia](DC.md) | 14 / 20 |  |
| [Delaware](DE.md) | 16 / 20 |  |
| [Florida](FL.md) | 12 / 20 |  |
| [Georgia](GA.md) | 14 / 20 |  |
| [Hawaii](HI.md) | 13 / 20 | capitol.hawaii.gov Cloudflare-blocked; recovered via Wayback id_ + DCCA PDF |
| [Iowa](IA.md) | 15 / 20 |  |
| [Idaho](ID.md) | 14 / 20 |  |
| [Illinois](IL.md) | 17 / 20 |  |
| [Indiana](IN.md) | 9 / 20 | Telehealth core (IC 25-1-9.5 §§7-10) via Justia/Wayback id_ + 4 federal-framework defaults; pharmacy/PDMP/compounding still open |
| [Kansas](KS.md) | 13 / 20 | +audio-only exclusion (K.S.A. 40-2,211); prescribing/compounding in K.A.R. (sos.ks.gov path 404s) |
| [Kentucky](KY.md) | 18 / 20 | +telehealthReg + no-in-person (KRS 311.5975/311.597, parent-reverified); compounding/dtc red |
| [Louisiana](LA.md) | 11 / 20 |  |
| [Massachusetts](MA.md) | 11 / 20 | §5O statute = definition + credentialing only; consent/in-person/Rx/pharmacy in 243/247 CMR (mass.gov 404, not archived) |
| [Maryland](MD.md) | 19 / 20 | +telehealthReg + audio-only-excluded (COMAR 10.32.05); only ecommerce.website red (genuine null) |
| [Maine](ME.md) | 16 / 20 |  |
| [Michigan](MI.md) | 18 / 20 | +telehealthReg + no-in-person (MCL 333.16283/16284, via Wayback); only e-commerce red |
| [Minnesota](MN.md) | 15 / 20 |  |
| [Missouri](MO.md) | 17 / 20 | +telehealthReg (RSMo 191.1145.3 full-licensure); consent/pdmp/website red (pdmp source anti-bot blocked) |
| [Mississippi](MS.md) | 16 / 20 |  |
| [Montana](MT.md) | 13 / 20 |  |
| [North Carolina](NC.md) | 16 / 20 | audio-only/in-person-Rx/compounding red (NC OAH admin-code server blocks; board position statement non-statutory) |
| [North Dakota](ND.md) | 13 / 20 |  |
| [Nebraska](NE.md) | 13 / 20 |  |
| [New Hampshire](NH.md) | 11 / 20 | all live NH hosts WAF-403; recovered via Wayback id_ |
| [New Jersey](NJ.md) | 14 / 20 | Telehealth Act (P.L.2017 c.117) via pdf.js; pharmacy/e-commerce behind Imperva-blocked N.J.A.C. 13:39 |
| [New Mexico](NM.md) | 17 / 20 | nmonesource.com 403; sourced via NMAC (srca.nm.gov) |
| [Nevada](NV.md) | 16 / 20 |  |
| [New York](NY.md) | 11 / 20 | Structural ceiling: no standalone telehealth practice statute (modality/consent only in insurance-parity PHL 2999-cc, excluded). Genuine gaps, not access. |
| [Ohio](OH.md) | 17 / 20 |  |
| [Oklahoma](OK.md) | 13 / 20 | oscn.net Turnstile-blocked; Wayback id_; OAC rules gapped |
| [Oregon](OR.md) | 13 / 20 | Wayback-sourced statute text |
| [Pennsylvania](PA.md) | 14 / 20 |  |
| [Rhode Island](RI.md) | 15 / 20 |  |
| [South Carolina](SC.md) | 17 / 20 | +audio-only permitted (medium-neutral def 40-47-20(53)); async/consent/website remain |
| [South Dakota](SD.md) | 15 / 20 |  |
| [Tennessee](TN.md) | 13 / 20 | Wayback-sourced statute text |
| [Texas](TX.md) | 20 / 20 | COMPLETE — Occ. Code 151.056/562.056/562.101/562.1045 (incl. rare real on-website disclosure mandate) |
| [Utah](UT.md) | 16 / 20 | +telehealthReg (26B-4-704 Title 58 licensure); reds genuine (audio-only needs A+V, no consent statute, DOPL e-commerce) |
| [Virginia](VA.md) | 16 / 20 | +telehealthReg (§54.1-2901 no separate registry); reds are genuine nulls (consent guidance-only, audio-only insurance-only) + 18 VAC rules |
| [Vermont](VT.md) | 14 / 20 |  |
| [Washington](WA.md) | 13 / 20 | Remaining reds largely genuine absences (consent rule repealed, no in-person mandate); csDispense WAC unread |
| [Wisconsin](WI.md) | 19 / 20 | +telehealthReg + no-in-person-Rx (Med 24.04/24.07); only ecommerce.website red (phone line, not website) |
| [West Virginia](WV.md) | 18 / 20 |  |
| [Wyoming](WY.md) | 8 / 20 | honest partial — most specifics in unread Board rules |

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.
