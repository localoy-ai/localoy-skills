---
name: meta-description-writer
description: Write click-worthy title tags and meta descriptions for a list of URLs, within pixel/character limits, delivered as a before/after table.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [seo, content]
---

# Meta Description Writer

Write titles and metas that earn the click and survive truncation.

## Procedure

1. **Take the URL list.** Ask for the URLs (pasted or in a file under the workspace) and each page's target keyword if known. Cap a single run at 25 URLs; suggest batching beyond that.
2. **Fetch every page.** Load each URL and record the current title and meta description. Read enough of the page to know what it actually offers — the meta must describe the real page, not a wish.
3. **Check the SERP context.** For pages with a known keyword, glance at the ranking results to see what phrasing and promises competitors lead with, so the new snippet can differ usefully.
4. **Write titles.** One per page: target keyword near the front, under 60 characters (about 580px), brand suffix only if it fits, no bait the page cannot pay off. Vary constructions across the batch — do not stamp the same template on every page.
5. **Write meta descriptions.** One per page: 140-155 characters, active voice, one concrete specific from the page (an offer, a differentiator, a location), and a soft call to action. Include the keyword once if it fits naturally; Google bolds it, but never force it.
6. **Verify lengths.** Count characters for every title and meta. Anything over limit gets rewritten, not annotated.
7. **Deliver.** Save to `reports/<date>-metas-<slug>.md`: a table of URL, current title/meta, new title/meta, and character counts, plus a one-line note where the rewrite depends on a page fix. Report the path back.

## Quality bar

- Every new snippet is true to the fetched page — no invented offers, prices, or claims.
- Lengths are counted, not eyeballed; the table shows the numbers.
- No two pages in the batch share a title or meta.
