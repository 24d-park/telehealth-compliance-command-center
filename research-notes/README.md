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

## Coverage status (regenerated 2026-07-23)
**All 51 jurisdictions have state-specific sourced fields.** Indiana (now 10/20) has fullLicense +
telehealth core (IC 25-1-9.5 §§7-10) via the FindLaw/Justia reproductions read through Internet
Archive `id_` raw captures, because the primary host iga.in.gov is an un-hydratable JS SPA; its
pharmacy chapters (IC 25-26) and the §6 modality definition are not reproduced on any reachable
archive and need a registered api.iga.in.gov key to close.
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
| [Colorado](CO.md) | 15 / 20 | +async/consent/telehealthReg (C.R.S. 12-30-124 via OLLS Title 12 HTML; SECTION CORRECTED from mis-cited 12-30-108). audioOnly/inPersonRx/csDispense/e-commerce red (in 3 CCR 713 Board rules, unread) |
| [Connecticut](CT.md) | 16 / 20 |  |
| [District of Columbia](DC.md) | 14 / 20 |  |
| [Delaware](DE.md) | 16 / 20 |  |
| [Florida](FL.md) | 17 / 20 | +fullLicense/video/async/csDispense/pic (Fla. Stat. 458.311, 456.47(1), 893.04, 465.018). audioOnly red (def excludes only email/fax, NOT audio-only); consent red (64B8-9.0141 repealed); dtc red (456.47(2)(b) permits no-exam) |
| [Georgia](GA.md) | 14 / 20 |  |
| [Hawaii](HI.md) | 15 / 20 | +telehealthReg (HRS 453-1.3(e)) + csDispense (HRS 329-101(b); HAR 16-95 extracted via archive-origin pdf.js). Genuine absences: nonresident/onlinePharmacy/website (not in HAR 16-95), consent (eval-only), pdmp (dispenser-report only) |
| [Iowa](IA.md) | 15 / 20 |  |
| [Idaho](ID.md) | 17 / 20 | +telehealthReg/consent/audio-only (Idaho Code 54-5713/5708/5703, Virtual Care Access Act) |
| [Illinois](IL.md) | 17 / 20 |  |
| [Indiana](IN.md) | 10 / 20 | +fullLicense (IC 25-22.5-3-1 via FindLaw/Wayback id_); IC 25-26 pharmacy + §6 modality def unreachable on any archive — needs api.iga.in.gov key |
| [Kansas](KS.md) | 14 / 20 | +telehealthReg (K.S.A. 40-2,211 verified-null) + audio-only exclusion. consent red (care-coord report only), pdmp voluntary (65-1685(c)). inPersonRx/compounding/website/dtc in K.A.R. — sos.ks.gov CloudFront-403, 68-13-3/4 not in Wayback (held) |
| [Kentucky](KY.md) | 18 / 20 | +telehealthReg + no-in-person (KRS 311.5975/311.597, parent-reverified); compounding/dtc red |
| [Louisiana](LA.md) | 19 / 20 | +8 fields via OSR-compiled LAC .docx (46:XLV consent/mandatory-PMP, 46:LIII nonresident/CDS/PIC/USP compounding/questionnaire ban); only ecommerce.website red (genuine absence) |
| [Massachusetts](MA.md) | 14 / 20 | +telehealthReg (243 CMR 2.01 verified-null) + nonresident/csDispense (247 CMR 6.02/9.15, via mass.gov /doc PDF); consent/in-person/Rx absent from 243 CMR 2.00 (genuine silence), e-commerce absent from 247 CMR |
| [Maryland](MD.md) | 19 / 20 | +telehealthReg + audio-only-excluded (COMAR 10.32.05); only ecommerce.website red (genuine null) |
| [Maine](ME.md) | 16 / 20 |  |
| [Michigan](MI.md) | 18 / 20 | +telehealthReg + no-in-person (MCL 333.16283/16284, via Wayback); only e-commerce red |
| [Minnesota](MN.md) | 15 / 20 |  |
| [Missouri](MO.md) | 17 / 20 | +telehealthReg (RSMo 191.1145.3 full-licensure); consent/pdmp/website red (pdmp source anti-bot blocked) |
| [Mississippi](MS.md) | 16 / 20 |  |
| [Montana](MT.md) | 16 / 20 | +telehealthReg/inPersonRx/csDispense (MCA 37-3-301, 37-7-401; ARM 24.156.813). CORRECTED stale anchors: MCA 37-3-343 repealed, ARM 24.156.809→.813. async/consent red (no telemed def, no explicit consent term) |
| [North Carolina](NC.md) | 16 / 20 | audio-only/in-person-Rx/compounding red (NC OAH admin-code server blocks; board position statement non-statutory) |
| [North Dakota](ND.md) | 17 / 20 | +telehealthReg/audioOnly(excluded)/csDispense/onlinePharmacy (NDCC 43-17, 19-03.1-22, 43-15-34.1 via pdf.js). consent red (PA-list only), pdmp voluntary (19-03.5-05), website absent |
| [Nebraska](NE.md) | 15 / 20 | +fullLicense + telehealthReg (Neb. Rev. Stat. 38-121 UCA); pdmp red (dispenser-report only, no mandatory query) |
| [New Hampshire](NH.md) | 17 / 20 | +pdmp (RSA 318-B:41 mandatory opioid query; program moved to RSA 126-A:89-96) + telehealthReg/inPerson/consent (329:1-d, 318:1) + PIC/USP compounding (Ph 704.11/404.01); all via Wayback id_. csDispense/website/dtc red (dtc bar ophthalmic-only) |
| [New Jersey](NJ.md) | 14 / 20 | Telehealth Act (P.L.2017 c.117) via pdf.js; pharmacy/e-commerce behind Imperva-blocked N.J.A.C. 13:39 |
| [New Mexico](NM.md) | 17 / 20 | nmonesource.com 403; sourced via NMAC (srca.nm.gov) |
| [Nevada](NV.md) | 16 / 20 |  |
| [New York](NY.md) | 12 / 20 | +ecommerce.website (8 NYCRR 63.6 internet drug-price-list disclosure, resolved a prior contradiction). Structural ceiling: modality/consent/in-person only in excluded insurance-parity PHL 2999-cc. Genuine gaps, not access. |
| [Ohio](OH.md) | 17 / 20 |  |
| [Oklahoma](OK.md) | 16 / 20 | +telehealthReg/audioOnly(excluded)/consent (OAC 435:10-7-13 via Wayback MDRULES PDF; oscn.net Turnstile-blocked). csDispense/compounding red (USP 797-sterile only, 795 not by-number); dtc indirect |
| [Oregon](OR.md) | 14 / 20 | +csDispense (OAR 855-080-0085 via oregon.public.law; OR hosts blocked). At honest ceiling: audioOnly/consent/inPersonRx/pdmp(voluntary)/website/dtc all genuine absences |
| [Pennsylvania](PA.md) | 14 / 20 |  |
| [Rhode Island](RI.md) | 15 / 20 |  |
| [South Carolina](SC.md) | 17 / 20 | +audio-only permitted (medium-neutral def 40-47-20(53)); async/consent/website remain |
| [South Dakota](SD.md) | 16 / 20 | +telehealthReg (SDCL 34-52-2 full-licensure); audio-only/pdmp red (audio needs store-forward; 34-20E-11 non-mandatory) |
| [Tennessee](TN.md) | 13 / 20 | Wayback-sourced statute text |
| [Texas](TX.md) | 20 / 20 | COMPLETE — Occ. Code 151.056/562.056/562.101/562.1045 (incl. rare real on-website disclosure mandate) |
| [Utah](UT.md) | 16 / 20 | +telehealthReg (26B-4-704 Title 58 licensure); reds genuine (audio-only needs A+V, no consent statute, DOPL e-commerce) |
| [Virginia](VA.md) | 16 / 20 | +telehealthReg (§54.1-2901 no separate registry); reds are genuine nulls (consent guidance-only, audio-only insurance-only) + 18 VAC rules |
| [Vermont](VT.md) | 14 / 20 |  |
| [Washington](WA.md) | 14 / 20 | +csDispense (WAC 246-945-011 CS-validity gate per RCW 69.50.308). Remaining 6 reds all genuine absences: telehealthReg (no registry), consent (rule repealed), in-person/inPersonRx (no mandate), website/dtc (not located) |
| [Wisconsin](WI.md) | 19 / 20 | +telehealthReg + no-in-person-Rx (Med 24.04/24.07); only ecommerce.website red (phone line, not website) |
| [West Virginia](WV.md) | 18 / 20 |  |
| [Wyoming](WY.md) | 12 / 20 | +telehealthReg/USP-compounding/csDispense(Ch.10)/PIC(Ch.2) via rules.wyo.gov GetRuleVersionHTML (tokenless). At honest ceiling: no Bd-Medicine telemedicine chapter (modality/consent/inPerson red), PDMP voluntary, no website/dtc mandate |

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.
