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
| [Alabama](AL.md) | 19 / 20 | +csDispense (Ala. Code 20-2-58 Sch II written-Rx + Sch III/IV 6mo/5-refill, via Wayback id_ Justia 2006 code) 2026-07-30. Telehealth §34-24-700 + pharmacy AAC 680-X-2. Red: ecommerce.website (absence). NOTE: latent duplicate AL override block (680-X shadowed by telehealth block) |
| [Arkansas](AR.md) | 17 / 20 | UNBLOCKED via Justia/Wayback id_ (AR Telemedicine Act 17-80-402/403/404); §404(d)(1) telehealthReg verified-null + §404(e)(1) consent added 2026-07-29; Rx §405 not archived, ecommerce absences remain |
| [Arizona](AZ.md) | 18 / 20 | +dtc (A.A.C. R4-23-404(F) internet-questionnaire ban, via Wayback pdf.js of Title 4 Ch.23) 2026-07-30. Red: compounding (AZ regulates by ISO class R4-23-670, NOT USP-by-number — verified absence), website |
| [California](CA.md) | 19 / 20 | +telehealthReg (verified-null: B&P 2052 exclusive-licensure + 2290.5(e); 2290.6 not codified) 2026-07-30. +csDispense (HSC 11200). Red: ecommerce.website (genuine null) |
| [Colorado](CO.md) | 17 / 20 | +async/consent/telehealthReg (C.R.S. 12-30-124) earlier; +inPersonRx (12-30-124(6) parity, no in-person rule in 3 CCR 713-1) + csDispense (C.R.S. 18-18-308) 2026-07-29. Red: audioOnly (term absent from Title 12), dtc (no explicit questionnaire bar) — genuine absences |
| [Connecticut](CT.md) | 18 / 20 | +telehealthReg (verified-null: 19a-906(a)(12)(A) title-20 exclusive; out-of-state branch B sunset 6/30/2025 + 19a-906a repealed 6/4/2024; Ch. 368ll not 368a) 2026-07-30. +audioOnly (19a-906(a)). Red: website/dtc genuine absences |
| [District of Columbia](DC.md) | 16 / 20 | +telehealthReg (DC Code 3-1205.01 verified-null) + csDispense (48-903.08). Red: audio-only/async (17 DCMR 4618 real-time only), website, dtc (genuine absences) |
| [Delaware](DE.md) | 18 / 20 | +inPersonRx (24 Del. C. 6004(a)) + csDispense (16 Del. C. 4739) 2026-07-29. NOTE old telemed 1769D repealed 2021, now Ch. 60. Red: pdmp (4798(f) conditional reasonable-belief trigger, not universal), website (genuine absence) |
| [Florida](FL.md) | 17 / 20 | +fullLicense/video/async/csDispense/pic (Fla. Stat. 458.311, 456.47(1), 893.04, 465.018). audioOnly red (def excludes only email/fax, NOT audio-only); consent red (64B8-9.0141 repealed); dtc red (456.47(2)(b) permits no-exam) |
| [Georgia](GA.md) | 15 / 20 | +telehealthReg (Ga. R&R 360-2-.17 out-of-state Telemedicine License, positive requirement) 2026-07-29. Red: modality.async/video + consent genuine absences in Rule 360-3-.07; website not located |
| [Hawaii](HI.md) | 16 / 20 | +nonresident (HRS 461-15(a)(7) out-of-state pharmacy permit; Wayback id_ capitol.hawaii.gov) 2026-07-30. +telehealthReg (HRS 453-1.3(e)) + csDispense (HRS 329-101(b); HAR 16-95 extracted via archive-origin pdf.js). Genuine absences: onlinePharmacy/website (no internet-specific law), consent (eval-only), pdmp (dispenser-report only) |
| [Iowa](IA.md) | 18 / 20 | +telehealthReg (653—13.9(3) verified-null) + audioOnly (13.9(1) excluded) + dtc (13.9(21) questionnaire ban) 2026-07-29; rule renumbered 13.11→13.9. pdmp red (§124.553(5) no-duty), consent already green |
| [Idaho](ID.md) | 19 / 20 | +csDispense + pdmp (Idaho Code 37-2722: (b)-(c) Sch II valid-Rx/no-refill + (f) mandatory 12mo PMP query for opioid/benzo) 2026-07-30. +telehealthReg/consent/audio-only (54-5713/5708/5703 Virtual Care Access Act). Red: ecommerce.website (absence) |
| [Illinois](IL.md) | 17 / 20 |  |
| [Indiana](IN.md) | 17 / 20 | +csDispense (IC 35-48-3-9 Sch II written-Rx/no-refill + III/IV 6mo/5-refill, Wayback id_ Title 35) 2026-07-30. UNBLOCKED via archived OFFICIAL iga.in.gov (Wayback id_); +modality/pdmp/pic/nonresident/online-pharmacy/dtc. Red: audio-only (absent), compounding (856 IAC unreachable — Title 25 has no USP-by-number), website |
| [Kansas](KS.md) | 14 / 20 | +telehealthReg (K.S.A. 40-2,211 verified-null) + audio-only exclusion. consent red (care-coord report only), pdmp voluntary (65-1685(c)). inPersonRx/compounding/website/dtc in K.A.R. — sos.ks.gov CloudFront-403, 68-13-3/4 not in Wayback (held) |
| [Kentucky](KY.md) | 19 / 20 | +compounding (201 KAR 2:076 §3 adopts USP 795/797/800/825 ALL by number — fullest on the board; live LRC) 2026-07-30. +telehealthReg + no-in-person (KRS 311.5975/311.597). Red: ecommerce.dtc (implied-only) |
| [Louisiana](LA.md) | 19 / 20 | +8 fields via OSR-compiled LAC .docx (46:XLV consent/mandatory-PMP, 46:LIII nonresident/CDS/PIC/USP compounding/questionnaire ban); only ecommerce.website red (genuine absence) |
| [Massachusetts](MA.md) | 14 / 20 | +telehealthReg (243 CMR 2.01 verified-null) + nonresident/csDispense (247 CMR 6.02/9.15, via mass.gov /doc PDF); consent/in-person/Rx absent from 243 CMR 2.00 (genuine silence), e-commerce absent from 247 CMR |
| [Maryland](MD.md) | 19 / 20 | +telehealthReg + audio-only-excluded (COMAR 10.32.05); only ecommerce.website red (genuine null) |
| [Maine](ME.md) | 19 / 20 | +inPersonRx (02-373 CMR Ch.11 3(7)) + csDispense (02-392 CMR Ch.19) + pic (02-392 CMR Ch.13 3(1)) 2026-07-29 via official SOS .docx. Red: website (genuine absence). Numbering: telehealth Ch.11(orig Ch.6), PIC Ch.13 |
| [Michigan](MI.md) | 18 / 20 | +telehealthReg + no-in-person (MCL 333.16283/16284, via Wayback); only e-commerce red |
| [Minnesota](MN.md) | 17 / 20 | +inPersonRx (§147.033 subd.2-3 telehealth relationship, no in-person mandate; §147.091 + R.6800 confirm absence) 2026-07-30. +compounding.stateReg (Minn. R. 6800.3300 USP 795/797 by number) 2026-07-29. Red: consent (§147.033 has none; in excluded insurance act §62A.673), dtc (only questionnaire bar §145.713 is ophthalmic-only), website |
| [Missouri](MO.md) | 17 / 20 | +telehealthReg (RSMo 191.1145.3 full-licensure); consent/pdmp/website red (pdmp source anti-bot blocked) |
| [Mississippi](MS.md) | 18 / 20 | +telehealthReg (Rule 5.2 + Code 73-25-34 verified-null) + dtc (Rule 7.1 questionnaire ban) 2026-07-29. Red: pdmp (73-21-127 reporting/registration; mandatory query only for pain-mgmt practices, not universal), website (absence) |
| [Montana](MT.md) | 16 / 20 | +telehealthReg/inPersonRx/csDispense (MCA 37-3-301, 37-7-401; ARM 24.156.813). CORRECTED stale anchors: MCA 37-3-343 repealed, ARM 24.156.809→.813. async/consent red (no telemed def, no explicit consent term) |
| [North Carolina](NC.md) | 17 / 20 | +compounding (21 NCAC 46 .2801 adopts USP <795>+<797> by number; <800> not named — via Wayback id_ of OAH) 2026-07-30. Red: audio-only (insurance/Medicaid-only), inPersonRx (only NC Med Board position statement — non-binding), website. NC OAH server blocks live |
| [North Dakota](ND.md) | 17 / 20 | +telehealthReg/audioOnly(excluded)/csDispense/onlinePharmacy (NDCC 43-17, 19-03.1-22, 43-15-34.1 via pdf.js). consent red (PA-list only), pdmp voluntary (19-03.5-05), website absent |
| [Nebraska](NE.md) | 18 / 20 | +inPersonRx + dtc (172 NAC 88 §009(F) Bd Medicine electronic-Rx H&P standard, via official rules.nebraska.gov API) 2026-07-30. +fullLicense + telehealthReg (38-121 UCA) + pic (38-2833). Red: pdmp (universal reporting + permissive access, no query mandate), website (absence). dtc caveat: H&P-adequacy framing, not literal questionnaire ban |
| [New Hampshire](NH.md) | 17 / 20 | +pdmp (RSA 318-B:41 mandatory opioid query; program moved to RSA 126-A:89-96) + telehealthReg/inPerson/consent (329:1-d, 318:1) + PIC/USP compounding (Ph 704.11/404.01); all via Wayback id_. csDispense/website/dtc red (dtc bar ophthalmic-only) |
| [New Jersey](NJ.md) | 19 / 20 | +telehealthReg (45:1-62.b verified-null), dtc (45:1-62.d questionnaire ban), pic/csDispense/onlinePharmacy (N.J.A.C. 13:39 via Wayback id_ — Imperva bypassed). Red: website (genuine absence) |
| [New Mexico](NM.md) | 17 / 20 | nmonesource.com 403; sourced via NMAC (srca.nm.gov) |
| [Nevada](NV.md) | 16 / 20 |  |
| [New York](NY.md) | 12 / 20 | +ecommerce.website (8 NYCRR 63.6 internet drug-price-list disclosure, resolved a prior contradiction). Structural ceiling: modality/consent/in-person only in excluded insurance-parity PHL 2999-cc. Genuine gaps, not access. |
| [Ohio](OH.md) | 17 / 20 |  |
| [Oklahoma](OK.md) | 18 / 20 | +csDispense (OAC 535:15-3-13 legitimate-purpose+valid-relationship gate) + compounding (535:15-10-61 USP 797/825 by number; 795/800 NOT) 2026-07-30 via Wayback id_ Title 535 pdf.js. +telehealthReg/audioOnly(excluded)/consent (OAC 435:10-7-13). Red: website (absence), dtc (real-time-equipment req, indirect) |
| [Oregon](OR.md) | 15 / 20 | +csDispense (OAR 855-080-0085) + inPersonRx (ORS 677.494(2) expressly permits telemedicine prescribing) 2026-07-29. Genuine absences: audioOnly/consent + pdmp (voluntary per ORS 431A.865(8))/website/dtc |
| [Pennsylvania](PA.md) | 16 / 20 | +telehealthReg (63 P.S. 422.10 verified-null; Act 42 is insurance-title, no registry) + inPersonRx (49 Pa. Code 16.92 CS in-person exam, OTP telehealth carve-out). Red: relationship/consent (Board regs), ecommerce website/dtc |
| [Rhode Island](RI.md) | 18 / 20 | +telehealthReg (RIGL 5-37-2 verified-null) + inPersonRx (216-RICR-40-05-1) + csDispense (RIGL 21-28-3.18) 2026-07-29. Red: consent (0 hits in physician rule), website — genuine absences |
| [South Carolina](SC.md) | 17 / 20 | +audio-only permitted (medium-neutral def 40-47-20(53)); async/consent/website remain |
| [South Dakota](SD.md) | 17 / 20 | +csDispense (SDCL 34-20B-29/37 CS-dispensing registration gate; Sch II no-refill §§70.1-80 repealed SL2016) 2026-07-30. +telehealthReg (SDCL 34-52-2 full-licensure). Red: audio-only (needs store-forward), pdmp (34-20E-11 non-mandatory), website (premises-display) |
| [Tennessee](TN.md) | 14 / 20 | Wayback-sourced statute text; +consent (TCA 63-1-155(b), archived 2021 TN Code) |
| [Texas](TX.md) | 20 / 20 | COMPLETE — Occ. Code 151.056/562.056/562.101/562.1045 (incl. rare real on-website disclosure mandate) |
| [Utah](UT.md) | 17 / 20 | +dtc (26B-4-704(4) questionnaire/email/patient-history ban, reused ut_teleact) 2026-07-30. +telehealthReg (26B-4-704 Title 58 licensure). Red: audio-only (needs A+V), consent (no statute), website |
| [Virginia](VA.md) | 17 / 20 | +dtc (Va. Code 54.1-3303(B) bona-fide-relationship exam req + binding 18VAC85-20-25(A); no literal questionnaire word) 2026-07-30. +telehealthReg (54.1-2901 no registry). Red: consent (only non-binding Guidance 85-12; 18VAC85-20 has no telemed consent rule), audio-only (insurance-only), website |
| [Vermont](VT.md) | 19 / 20 | +nonresident + onlinePharmacy + compounding (VT Bd Pharmacy Rules Pt.16/§13.22 USP 797 — Wayback id_ pdf.js) + csDispense (18 V.S.A. §4215) 2026-07-30. +inPersonRx (18 V.S.A. 9361(b)) 2026-07-29. NOTE: VT adopts USP 797 only (795/800 absent). Remaining red: website absence |
| [Washington](WA.md) | 15 / 20 | +csDispense (WAC 246-945-011) + telehealthReg (RCW 18.71.021 verified-null; only carve-out is out-of-state consultation) 2026-07-29. Remaining reds genuine absences: consent (rule repealed), in-person/inPersonRx (in excluded insurance title RCW 48.43.735), website/dtc |
| [Wisconsin](WI.md) | 19 / 20 | +telehealthReg + no-in-person-Rx (Med 24.04/24.07); only ecommerce.website red (phone line, not website) |
| [West Virginia](WV.md) | 19 / 20 | +compounding (15 CSR 1 §12.3 adopts 2023 USP 797/800 sterile + 795 nonsterile BY NUMBER, via official SOS CSR PDF pdf.js) 2026-07-30. Red: ecommerce.website (absence) |
| [Wyoming](WY.md) | 12 / 20 | +telehealthReg/USP-compounding/csDispense(Ch.10)/PIC(Ch.2) via rules.wyo.gov GetRuleVersionHTML (tokenless). At honest ceiling: no Bd-Medicine telemedicine chapter (modality/consent/inPerson red), PDMP voluntary, no website/dtc mandate |

---
> **DISCLAIMER:** Operational research tool; **not legal advice.** Verify with counsel and the applicable board before acting.
