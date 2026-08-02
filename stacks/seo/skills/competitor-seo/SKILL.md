---
name: competitor-seo
description: Track competitors' search rankings and content moves, and produce a weekly change report with recommended responses.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [web, files, schedule]
tags: [seo, research, automation]
---

# Competitor SEO Watch

Monitor a list of competitor domains and report what changed.

## Procedure

1. **Load the watchlist.** Read `seo/watchlist.md` from the workspace. Each
   line is `domain — note`. If the file does not exist, ask the user for
   two or three competitor domains and create it.
2. **Check each competitor.** For each domain, search the web for its recent
   content (site: queries, brand-name queries) and fetch its blog or news
   index. Note new pages, changed titles, and topics they are pushing.
3. **Compare against last week.** Read `seo/last-report.md` if present.
   Differences are the story; unchanged rankings are one line, not a table.
4. **Write the report** to `seo/report-<date>.md`:
   - What changed, per competitor, with links.
   - What it means: one or two sentences each, no fluff.
   - Recommended responses, ranked by effort/impact.
5. **Update state.** Overwrite `seo/last-report.md` with this week's
   findings so next week diffs against it.

## Rules

- Never invent rankings or traffic numbers. If a fact can't be sourced from
  a fetched page, mark it "unverified".
- Keep the whole report under 600 words. A report nobody reads is a cron
  job, not a deliverable.
