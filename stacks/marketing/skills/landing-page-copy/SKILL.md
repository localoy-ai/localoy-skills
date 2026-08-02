---
name: landing-page-copy
description: Write conversion-focused landing page copy from a product brief — hero, benefits, social proof, objection handling, and CTAs — delivered as structured markdown by section.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [content, conversion]
---

# Landing Page Copy

Turn a product brief into landing page copy that moves a visitor from curious to converted.

## Procedure

1. **Absorb the brief.** Read the product brief and any brand or customer research in the workspace. Identify the one visitor this page is for, the one action they should take, and the one problem the product solves. If the brief lacks these, ask before writing.
2. **Research the market.** Search the web for 2-3 competitor landing pages in the same category. Note the claims they all make so you can avoid sounding identical, and the objections their FAQs reveal.
3. **Write the hero.** Headline under 10 words stating the outcome the customer gets, not the product category. Subheadline explains how in one sentence. Primary CTA button copy is a verb phrase describing what happens next ("Get my free audit"), never "Submit."
4. **Write the benefits section.** Three to five benefits, each a bold outcome statement followed by one or two sentences of mechanism. Lead with benefit, support with feature. No feature lists without a "so that."
5. **Handle proof and objections.** Draft slots for testimonials, logos, and numbers with guidance on what to place there — never fabricate quotes, customers, or statistics. Add a short objection-handling block (price, effort, trust) phrased as the visitor thinks it.
6. **Close the page.** Repeat the CTA with a risk-reducer (guarantee, free trial, no-card note — only ones the brief confirms). Add a three-question FAQ if it removes friction.
7. **Deliver.** Write sections in page order with HTML-comment section labels to `drafts/landing-<slug>.md` and report the path plus the headline and CTA you chose.

## Quality bar

- Every claim is either from the brief, verified by search, or clearly marked `[NEEDS SOURCE]`.
- A stranger could read the hero alone and know what the product is, who it is for, and what to do next.
- No hype vocabulary; specificity does the persuading.
