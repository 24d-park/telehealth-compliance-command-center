# New Hampshire — Telehealth & Pharmacy Compliance Research Notes

**Date:** 2026-07-21
**Fields verified:** 7 (+ 2 federal defaults) → 11 ver / 9 rev. **Honest partial — live hosts fully blocked.**

## SOURCING NOTE (critical)
***ALL live NH state hosts are WAF-403 blocked in this environment:*** gc.nh.gov, www.gencourt.state.nh.us, and oplc.nh.gov all return "Error 403 / Attack ID 20000051" (the SAME WAF signature Iowa's legis.iowa.gov throws). The research subagent returned ZERO fields. **Recovery that worked:** Internet Archive captures of the official gc.nh.gov statute pages, via `web.archive.org/web/2024id_/https://gc.nh.gov/rsa/html/XXX/<chap>/<sec>.htm` (the `id_` raw-capture suffix serves the .gov HTML directly; body via console innerText). Same honest approach as TN/OR Wayback sourcing — disclosed in each SOURCES entry.

## STRUCTURAL KEY
- Telehealth practice standard = **RSA 329:1-d "Telemedicine"** (Board of Medicine). ***NOT the insurance-coverage law RSA 415-J.***
- Controlled Drug Act = RSA 318-B (incl. the PDMP program at 318-B:31–42).
- Pharmacy Act = RSA 318 (pharmacy licensure at 318:37; §318:38 was REPEALED 2023).

## VERIFIED (via Internet Archive captures of official gc.nh.gov)
### RSA 329:1-d (Telemedicine)
- **provider.fullLicense** — (II) "An out-of-state physician providing services by means of telemedicine ... shall be required to be licensed under this chapter" (consultation exception RSA 329:21,II).
- **modality.video / audioOnly / async** — (I) "'Telemedicine' means the use of audio, video, or other electronic media and technologies ... including the use of synchronous or asynchronous interactions." Audio is named in the operative definition → audio-only within the statutory telemedicine def.
- **prescribing.inPersonRx** — (III) Sch II-IV CS via telemedicine allowed after establishing a relationship, BUT "a subsequent in-person exam shall be conducted ... at intervals appropriate ... but not less than annually." A genuine annual in-person requirement for CS telemedicine prescribing.

### RSA 318:37 (Licensure of Pharmacies)
- **pharmacy.nonresident / ecommerce.onlinePharmacy** — (II)(a) "No person shall conduct or operate a mail-order pharmacy located outside of this state by shipping, mailing, or delivering prescription drugs into this state unless such pharmacy is registered in New Hampshire and a permit has been issued by the New Hampshire pharmacy board" (must hold home-state license in good standing; submit CS registrations). (§318:38 repealed 2023 → §318:37 is current.)

## LEFT "NEEDS LEGAL REVIEW" (honest reds — mostly blocked-host)
- **prescribing.pdmp** — the archived merged-chapter capture of RSA 318-B had the PDMP section bodies (318-B:31–38) COLLAPSED; I could see a query-exception rule but NOT the operative "shall query before prescribing" verb. Left red rather than assume a mandate. (NH almost certainly has a mandatory query — but I could not read the verb, so I won't assert it.)
- **relationship.consent** — RSA 329:1-d references consent only narrowly (for record-forwarding, V(c)); no general telehealth informed-consent mandate in the statute (may be in Board rule Med 500, host-blocked).
- **relationship.inPerson** — 329:1-d allows establishing the relationship via telemedicine, BUT RSA 318-B:1 XXVI-a defines "practitioner-patient relationship" as including "an in-person exam" — two conflicting contexts; left red pending clarification.
- **provider.telehealthReg** — no separate registration located (full licensure is the mechanism per 329:1-d II).
- **pharmacy.pic, pharmacy.csDispense, compounding.stateReg** — live in Board of Pharmacy rules (NH Code Ph 700) and RSA 318-B detail — host WAF-blocked and not well-archived.
- **ecommerce.website** — not located.
- **ecommerce.dtc** — RSA 329:1-d's questionnaire bar is OPHTHALMIC-ONLY ("Not determine an ophthalmic prescription solely by use of an online questionnaire"), too narrow to assert as a general DTC ban.

## FOLLOW-UP (NH is the weakest state — needs unblocking)
- Route NH `.gov` fetches through a residential proxy / different egress IP, OR use curl, to reach gc.nh.gov live.
- Priority reads once unblocked: RSA 318-B:31–42 (PDMP mandatory-query verb), NH Code Med 500 (telehealth consent + relationship), Ph 700 (PIC, compounding USP adoption, CS dispensing).
