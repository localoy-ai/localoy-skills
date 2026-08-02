---
name: serp-rank-tracker
description: Check where tracked keywords rank for a site each week, log positions to a history file, and report movement with likely causes.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web, schedule]
tags: [seo, reporting, automation]
---

# Serp Rank Tracker

Keep an honest weekly record of where the site ranks and explain what moved.

## Procedure

1. **Load the tracking list.** Read `data/rank-tracker/keywords.md` for the keyword list, target domain, and location context. If it does not exist, ask the user for keywords (10-25 is a good size) and create it.
2. **Check each keyword.** Search each keyword and scan the results for the target domain. Record the position (1-20), the ranking URL, and which competitors sit above it. If the domain is not in the top 20, record "not found" — never estimate a position.
3. **Log the snapshot.** Append this week's positions to `data/rank-tracker/history.md` as a dated row per keyword, so past runs are preserved.
4. **Compute movement.** Compare against the previous snapshot. Classify each keyword as up, down, flat, new, or lost, with the position delta.
5. **Look for causes.** For each keyword that moved 3+ positions, check the obvious suspects: did the ranking URL change, did a new competitor page appear above it, did the site's page change recently (fetch it and note anything visibly different). Label causes as observed or hypothesis — never present a guess as fact.
6. **Flag actions.** For each drop, suggest one concrete response (refresh the page, fix the element that regressed, build a link). For gains near page one, suggest the small push that could cross the line.
7. **Write the report.** Save to `reports/<date>-rank-report-<slug>.md` with a movement table, cause notes, and the action list. Report the path back.

## Cadence

Runs weekly, same weekday each week. Each run repeats the full procedure, appends to the history file, and produces a fresh dated report. If the history file shows a gap (a missed week), note it in the report rather than interpolating positions.

## Quality bar

- Positions come only from searches performed during the run; results can vary by location, so record the same context every week and note it in the report.
- Movement of 1-2 positions is noise — say so instead of inventing a story for it.
