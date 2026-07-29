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
| [Alaska](AK.md) | 18 / 20 | +telehealthReg (AS 08.64.170 verified-null), csDispense (17.30.020), compounding (12 AAC 52.440 Board pamphlet not USP), pdmp CORRECTED to MANDATORY (17.30.200(k)(4)). Red: consent (FSMB by-ref only), website (repealed 1996) |
| [Alabama](AL.md) | 18 / 20 | Telehealth statute §34-24-700 et seq. + pharmacy AAC 680-X-2 (2026-07-21); csDispense/e-commerce red (AAC 680-X-3 SPA won't hydrate) |
| [Arkansas](AR.md) | 17 / 20 | UNBLOCKED via Justia/Wayback id_ (AR Telemedicine Act 17-80-402/403/404); §404(d)(1) telehealthReg verified-null + §404(e)(1) consent added 2026-07-29; Rx §405 not archived, ecommerce absences remain |
| [Arizona](AZ.md) | 17 / 20 |  |
| [California](CA.md) | 18 / 20 | +csDispense (HSC 11200); telehealthReg left red (not exhaustively surveyed); website genuine null |
| [Colorado](CO.md) | 17 / 20 | +async/consent/telehealthReg (C.R.S. 12-30-124) earlier; +inPersonRx (12-30-124(6) parity, no in-person rule in 3 CCR 713-1) + csDispense (C.R.S. 18-18-308) 2026-07-29. Red: audioOnly (term absent from Title 12), dtc (no explicit questionnaire bar) — genuine absences |
| [Connecticut](CT.md) | 17 / 20 | +audioOnly (Conn. Gen. Stat. 19a-906(a) excludes audio-only telephone) 2026-07-29. Held: telehealthReg (verified-null basis in 2026 Supplement, didn't load); website/dtc genuine absences |
| [District of Columbia](DC.md) | 16 / 20 | +telehealthReg (DC Code 3-1205.01 verified-null) + csDispense (48-903.08). Red: audio-only/async (17 DCMR 4618 real-time only), website, dtc (genuine absences) |
| [Delaware](DE.md) | 18 / 20 | +inPersonRx (24 Del. C. 6004(a)) + csDispense (16 Del. C. 4739) 2026-07-29. NOTE old telemed 1769D repealed 2021, now Ch. 60. Red: pdmp (4798(f) conditional reasonable-belief trigger, not universal), website (genuine absence) |
| [Florida](FL.md) | 17 / 20 | +fullLicense/video/async/csDispense/pic (Fla. Stat. 458.311, 456.47(1), 893.04, 465.018). audioOnly red (def excludes only email/fax, NOT audio-only); consent red (64B8-9.0141 repealed); dtc red (456.47(2)(b) permits no-exam) |
| [Georgia](GA.md) | 15 / 20 | +telehealthReg (Ga. R&R 360-2-.17 out-of-state Telemedicine License, positive requirement) 2026-07-29. Red: modality.async/video + consent genuine absences in Rule 360-3-.07; website not located |
| [Hawaii](HI.md) | 15 / 20 | +telehealthReg (HRS 453-1.3(e)) + csDispense (HRS 329-101(b); HAR 16-95 extracted via archive-origin pdf.js). Genuine absences: nonresident/onlinePharmacy/website (not in HAR 16-95), consent (eval-only), pdmp (dispenser-report only) |
| [Iowa](IA.md) | 18 / 20 | +telehealthReg (653—13.9(3) verified-null) + audioOnly (13.9(1) excluded) + dtc (13.9(21) questionnaire ban) 2026-07-29; rule renumbered 13.11→13.9. pdmp red (§124.553(5) no-duty), consent already green |
| [Idaho](ID.md) | 17 / 20 | +telehealthReg/consent/audio-only (Idaho Code 54-5713/5708/5703, Virtual Care Access Act) |
| [Illinois](IL.md) | 17 / 20 |  |
| [Indiana](IN.md) | 16 / 20 | UNBLOCKED via archived OFFICIAL iga.in.gov/ic/2022/Title_25.html (Wayback id_); +modality video/async, INSPECT pdmp (25-26-24-19k), pic, nonresident, online-pharmacy, dtc. Red: audio-only (absent), csDispense (IC 35-48), 856 IAC compounding (still blocked), website |
| [Kansas](KS.md) | 14 / 20 | +telehealthReg (K.S.A. 40-2,211 verified-null) + audio-only exclusion. consent red (care-coord report only), pdmp voluntary (65-1685(c)). inPersonRx/compounding/website/dtc in K.A.R. — sos.ks.gov CloudFront-403, 68-13-3/4 not in Wayback (held) |
| [Kentucky](KY.md) | 18 / 20 | +telehealthReg + no-in-person (KRS 311.5975/311.597, parent-reverified); compounding/dtc red |
| [Louisiana](LA.md) | 19 / 20 | +8 fields via OSR-compiled LAC .docx (46:XLV consent/mandatory-PMP, 46:LIII nonresident/CDS/PIC/USP compounding/questionnaire ban); only ecommerce.website red (genuine absence) |
| [Massachusetts](MA.md) | 14 / 20 | +telehealthReg (243 CMR 2.01 verified-null) + nonresident/csDispense (247 CMR 6.02/9.15, via mass.gov /doc PDF); consent/in-person/Rx absent from 243 CMR 2.00 (genuine silence), e-commerce absent from 247 CMR |
| [Maryland](MD.md) | 19 / 20 | +telehealthReg + audio-only-excluded (COMAR 10.32.05); only ecommerce.website red (genuine null) |
| [Maine](ME.md) | 19 / 20 | +inPersonRx (02-373 CMR Ch.11 3(7)) + csDispense (02-392 CMR Ch.19) + pic (02-392 CMR Ch.13 3(1)) 2026-07-29 via official SOS .docx. Red: website (genuine absence). Numbering: telehealth Ch.11(orig Ch.6), PIC Ch.13 |
| [Michigan](MI.md) | 18 / 20 | +telehealthReg + no-in-person (MCL 333.16283/16284, via Wayback); only e-commerce red |
| [Minnesota](MN.md) | 16 / 20 | +compounding.stateReg (Minn. R. 6800.3300 USP 795/797 by number) 2026-07-29. Red: consent (§147.033 has none; in excluded insurance act §62A.673), inPersonRx, website/dtc |
| [Missouri](MO.md) | 17 / 20 | +telehealthReg (RSMo 191.1145.3 full-licensure); consent/pdmp/website red (pdmp source anti-bot blocked) |
| [Mississippi](MS.md) | 18 / 20 | +telehealthReg (Rule 5.2 + Code 73-25-34 verified-null) + dtc (Rule 7.1 questionnaire ban) 2026-07-29. Red: pdmp (73-21-127 reporting/registration; mandatory query only for pain-mgmt practices, not universal), website (absence) |
| [Montana](MT.md) | 16 / 20 | +telehealthReg/inPersonRx/csDispense (MCA 37-3-301, 37-7-401; ARM 24.156.813). CORRECTED stale anchors: MCA 37-3-343 repealed, ARM 24.156.809→.813. async/consent red (no telemed def, no explicit consent term) |
| [North Carolina](NC.md) | 16 / 20 | audio-only/in-person-Rx/compounding red (NC OAH admin-code server blocks; board position statement non-statutory) |
| [North Dakota](ND.md) | 17 / 20 | +telehealthReg/audioOnly(excluded)/csDispense/onlinePharmacy (NDCC 43-17, 19-03.1-22, 43-15-34.1 via pdf.js). consent red (PA-list only), pdmp voluntary (19-03.5-05), website absent |
| [Nebraska](NE.md) | 16 / 20 | +fullLicense + telehealthReg (Neb. Rev. Stat. 38-121 UCA); +pic (38-2833) 2026-07-29. Red: pdmp (universal reporting + permissive access, no query mandate), inPersonRx (Medicaid-scoped waiver), dtc (likely 172 NAC, unreached) |
| [New Hampshire](NH.md) | 17 / 20 | +pdmp (RSA 318-B:41 mandatory opioid query; program moved to RSA 126-A:89-96) + telehealthReg/inPerson/consent (329:1-d, 318:1) + PIC/USP compounding (Ph 704.11/404.01); all via Wayback id_. csDispense/website/dtc red (dtc bar ophthalmic-only) |
| [New Jersey](NJ.md) | 19 / 20 | +telehealthReg (45:1-62.b verified-null), dtc (45:1-62.d questionnaire ban), pic/csDispense/onlinePharmacy (N.J.A.C. 13:39 via Wayback id_ — Imperva bypassed). Red: website (genuine absence) |
| [New Mexico](NM.md) | 17 / 20 | nmonesource.com 403; sourced via NMAC (srca.nm.gov) |
| [Nevada](NV.md) | 16 / 20 |  |
| [New York](NY.md) | 12 / 20 | +ecommerce.website (8 NYCRR 63.6 internet drug-price-list disclosure, resolved a prior contradiction). Structural ceiling: modality/consent/in-person only in excluded insurance-parity PHL 2999-cc. Genuine gaps, not access. |
| [Ohio](OH.md) | 17 / 20 |  |
| [Oklahoma](OK.md) | 16 / 20 | +telehealthReg/audioOnly(excluded)/consent (OAC 435:10-7-13 via Wayback MDRULES PDF; oscn.net Turnstile-blocked). csDispense/compounding red (USP 797-sterile only, 795 not by-number); dtc indirect |
| [Oregon](OR.md) | 15 / 20 | +csDispense (OAR 855-080-0085) + inPersonRx (ORS 677.494(2) expressly permits telemedicine prescribing) 2026-07-29. Genuine absences: audioOnly/consent + pdmp (voluntary per ORS 431A.865(8))/website/dtc |
| [Pennsylvania](PA.md) | 16 / 20 | +telehealthReg (63 P.S. 422.10 verified-null; Act 42 is insurance-title, no registry) + inPersonRx (49 Pa. Code 16.92 CS in-person exam, OTP telehealth carve-out). Red: relationship/consent (Board regs), ecommerce website/dtc |
| [Rhode Island](RI.md) | 18 / 20 | +telehealthReg (RIGL 5-37-2 verified-null) + inPersonRx (216-RICR-40-05-1) + csDispense (RIGL 21-28-3.18) 2026-07-29. Red: consent (0 hits in physician rule), website — genuine absences |
| [South Carolina](SC.md) | 17 / 20 | +audio-only permitted (medium-neutral def 40-47-20(53)); async/consent/website remain |
| [South Dakota](SD.md) | 16 / 20 | +telehealthReg (SDCL 34-52-2 full-licensure); audio-only/pdmp red (audio needs store-forward; 34-20E-11 non-mandatory) |
| [Tennessee](TN.md) | 14 / 20 | Wayback-sourced statute text; +consent (TCA 63-1-155(b), archived 2021 TN Code) |
| [Texas](TX.md) | 20 / 20 | COMPLETE — Occ. Code 151.056/562.056/562.101/562.1045 (incl. rare real on-website disclosure mandate) |
| [Utah](UT.md) | 16 / 20 | +telehealthReg (26B-4-704 Title 58 licensure); reds genuine (audio-only needs A+V, no consent statute, DOPL e-commerce) |
| [Virginia](VA.md) | 16 / 20 | +telehealthReg (§54.1-2901 no separate registry); reds are genuine nulls (consent guidance-only, audio-only insurance-only) + 18 VAC rules |
| [Vermont](VT.md) | 15 / 20 | +inPersonRx (18 V.S.A. 9361(b) telemedicine exam is an explicit alternative) 2026-07-29. Held: nonresident/csDispense/compounding (VT OPR pharmacy rules CloudFront-blocked); website absence |
| [Washington](WA.md) | 15 / 20 | +csDispense (WAC 246-945-011) + telehealthReg (RCW 18.71.021 verified-null; only carve-out is out-of-state consultation) 2026-07-29. Remaining reds genuine absences: consent (rule repealed), in-person/inPersonRx (in excluded insurance title RCW 48.43.735), website/dtc |
| [Wisconsin](WI.md) | 19 / 20 | +telehealthReg + no-in-person-Rx (Med 24.04/24.07); only ecommerce.website red (phone line, not website) |
| [West Virginia](WV.md) | 18 / 20 |  |
| [Wyoming](WY.md) | 12 / 20 | +telehealthReg/USP-compounding/csDispense(Ch.10)/PIC(Ch.2) via rules.wyo.gov GetRuleVersionHTML (tokenless). At honest ceiling: no Bd-Medicine telemedicine chapter (modality/consent/inPerson red), PDMP voluntary, no website/dtc mandate |

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.
