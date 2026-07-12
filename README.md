# Outside Money in the 2026 Maine U.S. Senate Race

A standalone, single-page ledger of independent expenditures and outside money reported around
Graham Platner's 2026 Maine U.S. Senate candidacy (October 2025 – July 8, 2026).

**Live page:** https://daguilar0123.github.io/graham-platner-campaign-finance/

This repository is **"The Money"** — one of two repos in a single project. It is kept
deliberately separate from its editorial sibling so it can be cited on its own: **it draws no
conclusions** about any candidate, committee, or donor. Its companion, **"The Record,"**
documents the case as a whole from a declared standpoint:

- Sibling repo: https://github.com/Daguilar0123/graham-platner-the-record
- The full project overview, architecture, and design rules live there — see that repo's
  [ARCHITECTURE.md](https://github.com/Daguilar0123/graham-platner-the-record/blob/main/ARCHITECTURE.md).
  The two sites are stitched together by an identical `projnav` strip and absolute cross-links.

## What it contains

- Every FEC Schedule E independent expenditure filed supporting or opposing the candidate (FEC
  candidate ID `S6ME00373`), each row linked to the filing image on docquery.fec.gov.
- Deduped totals (F24 24-hour notices double-filed on later F3X periodic reports counted once):
  **$11,077,173 opposing / $323,426 supporting**.
- Reported money flows not visible in FEC IE data (501(c)(4) donations into the filing super
  PAC), with press citations.
- Press aggregates broader than itemized IE data, labeled as such.
- A share hub with downloadable social graphics, and cross-site navigation to The Record.

## Sources & method

Pulled July 9, 2026 from the FEC API
(`api.open.fec.gov/v1/schedules/schedule_e/?candidate_id=S6ME00373`) and verified against
docquery filing images. Note: the API's `candidate_search` text parameter returns unrelated
records for this name; the candidate ID is required. Press-reported figures are cited inline.
Figures reflect filings available on the compile date; later amendments may change totals.

## Tech

Single-file static HTML/CSS/JS, no build, served by GitHub Pages. See
[CLAUDE.md](CLAUDE.md) for the rules an AI agent working in this repo must follow.

© 2026 Daniel Ismael Aguilar · https://grownfromconcrete.org
