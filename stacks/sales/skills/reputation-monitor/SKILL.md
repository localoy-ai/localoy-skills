---
name: reputation-monitor
description: Weekly sweep of review sites and web mentions for a business; compares against last week's baseline file and messages the owner only when ratings drop or negatives spike.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web, schedule, messaging]
tags: [reputation, automation]
---

# Reputation Monitor

Watch the business's reviews and mentions every week, stay quiet when things are normal, and raise a clear alarm when they are not.

## Procedure

1. **Load the baseline.** Read the previous snapshot from `reports/reputation/` (latest file). It holds last week's average rating, review counts per site, and known negative reviews. On the first run there is no baseline; build one and say so instead of alerting.
2. **Sweep the sources.** For each site listed in the config file (Google, Yelp, Facebook, industry sites), fetch the current rating and recent reviews via web search. Also search the business name plus city for new press or forum mentions.
3. **Record exact numbers.** Log only what the pages actually show: rating to one decimal, total review count, and the text of any new review at 3 stars or below. If a site cannot be reached this week, record "unavailable" rather than reusing or guessing a number.
4. **Compare against baseline.** Flag: average rating down 0.1 or more on any site, two or more new negative reviews in the week, any 1-star review, or a negative mention outside review sites. Everything else is routine.
5. **Write the snapshot.** Save the full picture to `reports/reputation/<date>.md`: per-site numbers, deltas from last week, new reviews quoted, flags raised.
6. **Message only what is confirmed.** If flags were raised, send the owner a short alert on the connected channel: what dropped, by how much, and a link to the snapshot. Send it only after every number in it has been read directly from the source this run; anything uncertain (an unreachable site, an ambiguous mention) is marked "needs a look" in the report, not stated as fact in the message. If nothing was flagged, send nothing, or a one-line "all quiet" if the config asks for it.
7. **Report the path.** Reply with the snapshot path and whether an alert went out.

## Cadence

Runs once a week on a scheduled trigger (default Monday morning, before the owner's workday). Each run reads the prior week's snapshot as its baseline, so the schedule should not be paused for more than a week or deltas lose meaning. A mid-week manual run is fine; it compares against the most recent snapshot, whatever its date.

## Output

Weekly file at `reports/reputation/<date>.md` plus, when warranted, one short alert message. The report is the record; the message is only the summons to read it.
