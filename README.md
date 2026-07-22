# Telehealth & Pharmacy Compliance Command Center

A self-contained, single-file web app that tracks telehealth and pharmacy regulatory
requirements across all 51 US jurisdictions (50 states + DC) along 20 compliance fields
per jurisdiction — provider licensing, modality, patient relationship, prescribing/controlled
substances, pharmacy dispensing, compounding, and e-commerce/online.

**Live app:** open `index.html` in any browser (no build step, no server, works offline).

## What makes it different: provenance over guesses

Every regulatory claim is either backed by a **verbatim primary-source citation** (state statute,
administrative code, or board rule — with the exact section, URL, and read date) **or** it is
honestly marked **"Needs legal review."** A field turns green only when real primary-source text
was read verbatim. "No requirement located" and documented access-blocks stay red rather than being
filled with a plausible guess. This no-fabrication rule is the core design constraint.

> **Not legal advice.** This is an operational research tool. Verify with counsel and the applicable
> board before acting.

## Features

- **50-state map** — per-jurisdiction cards, colour-coded by tracked compliance status.
- **Data table** — all 20 fields × 51 jurisdictions with a derived %-verified column.
- **Compare states** — side-by-side field-by-field.
- **Compliance calendar** — time-sensitive items (sunsets, effective dates).
- **Change log** — the full sourced audit trail of every data change.
- **Ask (grounded)** — a natural-language query box that is **retrieval-only (no LLM, no API key,
  no server)**. It matches a question to the state + topic and returns the exact verified note and
  citation already recorded, or an honest "needs legal review" — it cannot hallucinate because it
  only surfaces what the sourced data contains.

## Structure

- `index.html` — the entire app (HTML + CSS + JS + data, single file).
- `research-notes/` — per-state research notes (`XX.md`) documenting sources checked, exact
  citations, fields still needing review, and access-blocks encountered; plus `README.md` with the
  coverage-status table.

## Data-sourcing method

Primary sources only, in priority order: state board of pharmacy → state statutes / administrative
code → state medical board → state telehealth statutes/rules → state PDMP agency; DEA / FDA / USP
for the federal layers. Where a live host is Cloudflare/Imperva-walled or a non-hydrating JS SPA,
text is recovered from Internet Archive Wayback raw (`id_`) captures or official PDFs (via pdf.js) —
always disclosed in the relevant note. No blogs, vendor pages, or AI-generated answers are ever cited.
