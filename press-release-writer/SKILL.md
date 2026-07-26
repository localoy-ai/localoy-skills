---
name: press-release-writer
description: Draft an AP-style press release from an announcement brief — headline, dateline, lead, quotes, boilerplate, and media contact — ready for distribution as markdown.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [content, pr]
---

# Press Release Writer

Turn an announcement into a press release an editor could run with minimal edits.

## Procedure

1. **Nail the news.** From the brief, identify what is actually new: launch, funding, hire, partnership, milestone, event. If the answer to "why would anyone outside the company care" is unclear, ask before drafting.
2. **Gather the facts.** Collect names with exact titles and spellings, dates, locations, numbers, and product details from the brief and workspace files. Verify company details, spellings, and any market claims via web search. Never invent a statistic or a quote attribution.
3. **Write the headline and subhead.** Headline in title case, under 100 characters, stating the news plainly with an active verb. Optional subhead adds the strongest supporting fact. No exclamation points, no marketing adjectives.
4. **Write the lead.** Dateline format: CITY, State, Month Day, Year —. First paragraph answers who, what, when, where, why in 25-35 words. An editor should be able to run the lead alone as a complete story.
5. **Build the body.** Inverted pyramid: second paragraph expands the what and why with specifics; third carries an executive quote that adds perspective, not restated facts; later paragraphs cover details, availability, and a second quote (customer or partner) if the brief supplies one. Draft quotes for named people and mark them `[FOR APPROVAL]`.
6. **Close in standard form.** Add the "About <Company>" boilerplate (write one from verified facts if none exists), media contact block with placeholders for anything not provided, and end with ###.
7. **Deliver.** Write to `drafts/press-release-<slug>.md` and report the path, the headline, and any items awaiting approval or missing contact details.

## Output

- AP style throughout: numerals per AP rules, no Oxford comma, title case headline, third person only.
- 400-500 words for the release body; one page when printed.
- All facts traceable to the brief or a verified source; approval-pending items listed at the top of the file in an HTML comment.
