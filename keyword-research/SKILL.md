---
name: keyword-research
description: Turn seed terms into a keyword map with intent buckets, difficulty judgments, content gaps, and a target page per keyword, saved as a report.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [seo, research]
---

# Keyword Research

Build a keyword map a small business can actually execute: real terms, honest difficulty, one target page each.

## Procedure

1. **Collect inputs.** Ask for the business type, location (if local), seed keywords, and the site URL. Fetch the site's main pages so you know what content already exists.
2. **Expand the seeds.** For each seed, search the web for the term and note autocomplete-style variants, "people also ask" phrasings, and how competitors title their ranking pages. Build a candidate list of 30-60 keywords from what you actually observe in results.
3. **Bucket by intent.** Label each keyword transactional (hire/buy), commercial (compare/best), informational (how/what), or local (near me / city-modified). Drop keywords whose results show the searcher wants something this business does not offer.
4. **Judge difficulty from the SERP.** For each keyword worth keeping, look at who ranks: national brands and directories mean hard; small local sites and thin pages mean winnable. Record the judgment as easy/medium/hard with a one-line reason. Never assign numeric difficulty scores you did not measure.
5. **Find content gaps.** Compare the keyword list against the site's existing pages. Mark each keyword as covered by an existing page, needs an upgrade to an existing page, or needs a new page.
6. **Assign target pages.** Give every kept keyword exactly one target URL (existing or proposed, with a suggested slug). Group keywords that one page can serve together.
7. **Write the map.** Save to `reports/<date>-keyword-map-<slug>.md`: a table of keyword, intent, difficulty, target page, and status, followed by the top 5 pages to create or upgrade first. Report the path back.

## Output

- One markdown table as the map, sorted by intent then difficulty.
- A short "start here" section: the five actions with the best effort-to-reward ratio, each justified by an observed SERP fact.
