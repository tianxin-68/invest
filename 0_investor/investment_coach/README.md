# Investment Coach Run Log

This directory stores immutable, date-partitioned runtime records for the ChatGPT Scheduled Task **投资教练**.

## Current write path

`0_investor/investment_coach/YYYY-MM-DD.md`

## Boundary

- `../investment_coach.md` is a legacy historical archive and should be treated as read-only.
- New runs must not rewrite the whole legacy archive just to append one entry.
- External articles remain `Evidence / Candidate`; they do not become Investment Source without Owner judgment and later Reality Review.
- One date corresponds to at most one Scheduled run record; if the date file already exists, read that small file and deduplicate by article title / source URL before writing.
- Gmail delivery and GitHub persistence are independent outcomes; failure of one does not imply failure or rollback of the other.
