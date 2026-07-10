# Outside Money in the 2026 Maine U.S. Senate Race

A standalone, single-page ledger of independent expenditures and outside money
reported around Graham Platner's 2026 Maine U.S. Senate candidacy
(October 2025 – July 8, 2026).

**Live page:** https://daguilar0123.github.io/platner-campaign-money/

## What it contains
- Every FEC Schedule E independent expenditure filed supporting or opposing
  the candidate (FEC candidate ID `S6ME00373`), each row linked to the actual
  filing image on docquery.fec.gov
- Deduped totals (F24 24-hour notices double-filed on later F3X periodic
  reports counted once): **$11,077,173 opposing / $323,426 supporting**
- Reported money flows not visible in FEC IE data (501(c)(4) donations into
  the filing super PAC), with press citations
- Press aggregates that are broader than itemized IE data, labeled as such

## Sources & method
Pulled July 9, 2026 from the FEC API
(`api.open.fec.gov/v1/schedules/schedule_e/?candidate_id=S6ME00373`) and
verified against docquery filing images. Note: the API's
`candidate_search` text parameter returns unrelated records for this name;
the candidate ID is required. Press-reported figures are cited inline.
Figures reflect filings available on the compile date; later amendments may
change totals.

This repository is a campaign-finance record only. It draws no conclusions
about any candidate, committee, or donor.
