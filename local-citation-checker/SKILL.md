---
name: local-citation-checker
description: Verify a business's name, address, and phone across directories and listings using a live browser, and flag every inconsistency with fix instructions.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web, browser]
tags: [local, audit]
---

# Local Citation Checker

Find every place the business's NAP is wrong, prove it with what the page actually shows, and say how to fix it.

## Procedure

1. **Set the canonical NAP.** Ask for the exact business name, address, and phone number (and website URL) the owner considers correct. Normalize formatting quirks to compare fairly (St vs Street, +1 prefixes) but track them.
2. **Build the checklist.** Start from the core set — Google Business Profile, Bing Places, Apple Maps (via web), Yelp, Facebook, and the site's own contact page — then add industry and local directories found by searching the business name plus city.
3. **Visit each listing in the browser.** Open each candidate page in the logged-in browser session and read the displayed name, address, phone, website, and hours. If a page will not load, is behind a wall, or shows no listing, record exactly that and move on — do not guess what the listing probably says.
4. **Search for stray listings.** Search the phone number and the address in quotes to surface duplicate or outdated listings (old addresses, misspelled names) the owner forgot about.
5. **Compare against canonical.** For each listing, mark every field as match, formatting-only difference, or true mismatch. Quote the listed value verbatim next to the canonical value.
6. **Write fix instructions.** For each mismatch or duplicate, state where to log in or which claim/suggest-an-edit flow to use. Do not submit edits or claims yourself; the owner does that.
7. **Deliver the report.** Save to `reports/<date>-citations-<slug>.md`: a table of directory, URL, each NAP field's status, and the fix, plus a summary count of clean vs. broken citations. Report the path back.

## Quality bar

- Every status in the table comes from a page the browser actually rendered during this run.
- Unreachable pages are reported as unreachable, never counted as clean or broken.
- Formatting-only differences are listed separately so the owner does not chase harmless variants.
