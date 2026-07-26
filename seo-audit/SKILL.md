---
name: seo-audit
description: Crawl a site's key pages and audit titles, metas, headings, internal links, and speed flags, producing a prioritized fix list saved to reports/.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [seo, audit]
---

# Seo Audit

Find the technical and on-page problems holding a site back, ranked by impact and effort.

## Procedure

1. **Scope the crawl.** Ask for the site URL if not given. Fetch the homepage and sitemap.xml (or /sitemap_index.xml). Build a page list capped at the 30 most important URLs: homepage, service pages, top blog posts, contact.
2. **Fetch each page.** Request every URL in the list. Record HTTP status, redirect chains, and any page that fails to load. Do not guess at content for pages you could not fetch.
3. **Check on-page elements.** For each page, extract the title tag, meta description, H1, and heading structure. Flag missing or duplicate titles, titles over 60 characters, missing metas, multiple H1s, and headings that skip levels.
4. **Map internal links.** From the fetched HTML, list internal links per page. Flag orphan pages (in the sitemap but never linked), broken internal links (404s), and important pages more than two clicks from the homepage.
5. **Note speed and markup flags.** From the HTML alone, flag oversized inline scripts, images without width/height or lazy loading, missing canonical tags, and missing structured data on pages that should have it (LocalBusiness, Article).
6. **Prioritize.** Sort every finding into three buckets: fix this week (broken links, missing titles, noindex mistakes), fix this month (weak metas, heading issues), and backlog (nice-to-have markup). Base severity only on what you observed.
7. **Write the report.** Save to `reports/<date>-seo-audit-<domain>.md` with a summary table, per-page findings, and the prioritized fix list. Report the file path back.

## Quality bar

- Every finding cites the exact URL and the observed value (e.g. the actual title text and its length).
- No invented scores or estimated traffic numbers; if a check needs a tool you do not have, say so instead of approximating.
- The fix list is actionable by a non-specialist: each item says what to change and to what.
