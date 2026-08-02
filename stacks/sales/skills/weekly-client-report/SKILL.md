---
name: weekly-client-report
description: Assemble the week's completed work, metrics, and next steps from workspace files into a client-ready weekly report, then send it on the connected channel once every number is verified.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web, schedule, messaging]
tags: [clients, reporting, automation]
---

# Weekly Client Report

Turn a week of scattered work into one short report the client actually reads, and get it to them on time.

## Procedure

1. **Collect the week's material.** Read this week's files in the workspace: task logs, published drafts, prior reports in `reports/`, and any metrics exports the tools dropped in. List what shipped, what moved, and what stalled.
2. **Pull the numbers.** Take metrics only from the provided exports or by checking live sources on the web (review counts, published posts, ranking checks). Every number in the report must trace to a file or a page read this run. If a metric is missing, write "not available this week" -- never estimate.
3. **Lead with wins.** Open the report with two or three concrete outcomes in plain language ("Google rating up from 4.3 to 4.5", "3 posts published, offer post got the most clicks"). Clients skim; the first five lines carry the report.
4. **Show the numbers honestly.** A short metrics table with this week, last week, and the delta. Flat or down numbers stay in; a one-line explanation beats a hidden decline the client finds themselves.
5. **State next steps.** Three to five items for the coming week, each starting with a verb, each traceable to the plan or to something this week surfaced. Note anything you need from the client as its own line.
6. **Save, verify, then send.** Write the report to `reports/weekly/<date>-<client>.md`. Re-read it once against the source files: every claim checked, anything uncertain either removed or explicitly marked as unconfirmed and left out of the sent version. Only then send it to the client on the connected channel; if any core metric could not be verified, hold the send and message the account owner instead, flagging what is missing.
7. **Report the path.** Reply with the file path and whether the report was sent or held.

## Cadence

Runs weekly on a scheduled trigger, default Friday afternoon so the client starts their week with it or ends the week informed -- set the day to match the client's contract. Each run reads the previous report so "last week" columns and carried-over next steps stay consistent.

## Output

One file at `reports/weekly/<date>-<client>.md`: wins, metrics table with deltas, next steps, asks of the client. Under a page. The same text is what gets sent -- no separate summary that can drift from the report.
