---
name: analytics-summarizer
description: Turn exported analytics CSVs (GA4, Search Console, etc.) into a plain-English monthly summary — what moved, why it likely moved, and what to do next.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, shell]
tags: [reporting, analytics]
---

# Analytics Summarizer

Turn a folder of CSV exports into one page a business owner will actually read.

## Procedure

1. **Locate the exports.** Ask where the CSVs live in the workspace (e.g. `data/analytics/`). List the files, open the header row of each, and identify what each export contains: source, date range, dimensions, metrics.
2. **Validate before analyzing.** Check date ranges overlap sensibly, spot duplicate rows, and note gaps or sampling notices. If two files disagree on the same metric, report the discrepancy instead of averaging it away.
3. **Compute the movements.** Use shell tools (awk, python if available) to compare this period against the prior period in the data: sessions, top landing pages, top queries, conversions or goal events — whatever the exports actually contain. Compute percentage changes only where both periods exist.
4. **Rank what mattered.** Pick the 3-6 changes large enough to care about, in absolute terms as well as percentages (a 300% jump on 4 visits is not a headline). Ignore noise-level wiggle and say that you did.
5. **Explain, carefully.** For each headline change, look inside the data for the cause: which page, which query, which channel drove it. Label every explanation as shown by the data or plausible guess — never present a guess as a finding.
6. **Recommend actions.** For each finding, one concrete next step tied to it (update the fading page, build on the rising query, fix the page with collapsing conversions).
7. **Write the summary.** Save to `reports/<date>-analytics-summary-<slug>.md`: a three-sentence top line in plain English, the movements table, explanations, and the action list. Report the path back.

## Output

- Written for a non-analyst: no unexplained jargon, every metric introduced in one clause.
- Every number in the summary is traceable to a named CSV and computed during the run — nothing estimated or remembered.
- If the exports cannot answer a question (no conversion data, missing months), the summary says so plainly and lists what export to add next month.
