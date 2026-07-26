---
name: faq-generator
description: Build a customer FAQ page from support questions, reviews, and competitor FAQs — grouped by topic, answered in plain language, saved as publish-ready markdown.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [content, support]
---

# FAQ Generator

Build the FAQ customers actually need, sourced from what they actually ask.

## Procedure

1. **Mine real questions.** Read the support tickets, emails, chat logs, or review exports in the workspace. Extract every distinct question customers have asked, in their own wording. These outrank anything invented.
2. **Fill gaps from outside.** Search the web for the business's public reviews and for 2-3 competitor FAQ pages in the same category. Note questions competitors answer that the collected material missed — shipping, refunds, pricing, compatibility are common blind spots.
3. **Deduplicate and rank.** Merge variants of the same question, keep the phrasing a real customer used, and rank by frequency and purchase impact. Target 12-25 questions; cut anything asked once with no buying relevance.
4. **Group by topic.** Organize into 3-6 sections in the order a new customer meets them: product basics, pricing and billing, ordering and shipping, usage, support and returns. Adjust names to the business.
5. **Write the answers.** Two to four sentences each, direct answer in the first sentence, plain language, no deflection to "contact support" unless genuinely required. Pull specifics (prices, timeframes, policies) only from the source material or the business's own site; mark anything unconfirmed `[CONFIRM: detail]`.
6. **Add structure for reuse.** Precede each section with an anchor-friendly heading and note at the top of the file which questions suit FAQ schema markup for search.
7. **Deliver.** Write to `drafts/faq-<slug>.md` and report the path, the question count per section, and the list of `[CONFIRM]` items needing the owner's sign-off.

## Quality bar

- Every question traces to a real source: support log, review, or a competitor's page — noted in an HTML comment per question.
- Answers commit to specifics; hedge words ("typically," "may vary") appear only where policy genuinely varies.
- No policy, price, or timeframe is stated without a source; unknowns are flagged, not guessed.
- A frustrated customer skimming for one answer finds it inside 20 seconds.
