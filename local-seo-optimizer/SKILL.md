---
name: local-seo-optimizer
description: Audit and improve a business's local pack presence — NAP consistency, location pages, review velocity, and local keyword targeting, with a prioritized plan.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [seo, local]
---

# Local SEO Optimizer

Get a local business more visible in the map pack and local results, using checks you can verify.

## Procedure

1. **Establish the canonical NAP.** Ask for the exact business name, address, and phone number the owner wants everywhere, plus service area and primary categories. This is the reference for every later check.
2. **Check the website's local signals.** Fetch the site. Verify the NAP appears in the footer or contact page and matches the canonical version character-for-character. Check for LocalBusiness structured data, an embedded map, and city/region terms in the title tags of key pages.
3. **Review the Google Business Profile.** Search for the business by name and by "<service> <city>". Note whether the profile appears, its categories, and how its listed NAP compares to canonical. Record what you actually see in results; if you cannot view the profile, say so.
4. **Audit location and service pages.** For each service area or location, check whether a dedicated page exists with unique copy, the local keyword in the title and H1, and the NAP or service-area statement. Flag thin duplicated location pages — they hurt more than help.
5. **Assess review velocity.** From listings visible in search results, note the review count and recency you can observe. Propose a realistic review-request routine (who asks, when, via what link) rather than a target number pulled from nowhere.
6. **Map local keywords.** Build a short list of "<service> <city>" and "near me"-intent terms, check who ranks for each, and assign each to a page from step 4.
7. **Write the plan.** Save to `reports/<date>-local-seo-<slug>.md`: findings per area (NAP, site, profile, pages, reviews), then a prioritized plan ordered by impact. Report the path back.

## Quality bar

- NAP mismatches are quoted exactly (both versions) so the fix is unambiguous.
- No invented review counts, ranking positions, or "local SEO scores" — every number in the report was observed during the run.
