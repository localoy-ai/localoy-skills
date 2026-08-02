---
name: on-page-optimizer
description: Rewrite one page's title, meta description, headings, and body sections against a target keyword, keeping natural language and no stuffing.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [seo, content]
---

# On Page Optimizer

Take one page and one target keyword and produce a rewrite that ranks better without reading like it was written for a robot.

## Procedure

1. **Gather the pair.** Ask for the page URL and the target keyword (plus 1-3 secondary keywords if the user has them). Fetch the live page and extract the current title, meta, headings, and body copy.
2. **Study the SERP.** Search the target keyword and read the top-ranking pages. Note the searcher intent they serve, the subtopics they all cover, and any subtopic the current page misses. Base gap claims only on pages you actually read.
3. **Rewrite the title and meta.** Draft a title under 60 characters with the keyword near the front and a real reason to click, and a meta description of 140-155 characters that matches intent. Provide the current version alongside each rewrite.
4. **Restructure the headings.** Propose one H1 containing the keyword naturally, then an H2/H3 outline covering the intent and the gaps found in step 2. Keep headings descriptive, not keyword-repeated.
5. **Rewrite body sections.** For each section that changes, write the new copy in the site's existing voice. Use the keyword and close variants where they read naturally; if a sentence only exists to hold a keyword, cut it. Preserve facts from the original — do not invent claims, stats, or testimonials.
6. **Add internal link suggestions.** From pages you fetched or the user named, suggest 2-4 internal links with anchor text into and out of this page.
7. **Write the deliverable.** Save to `reports/<date>-onpage-<slug>.md` with before/after for title, meta, and headings, the rewritten sections, and a short rationale per change. Report the path back.

## Quality bar

- Keyword density is never a goal; if the copy reads worse with the keyword, leave it out and say so.
- Every "competitors cover X" claim names the URL where you saw it.
- Nothing fabricated: no made-up reviews, numbers, or credentials in the rewritten copy.
