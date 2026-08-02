---
name: newsletter-writer
description: Draft a complete email newsletter issue from recent company updates, product news, and curated links — subject lines, sections, and CTA included, saved as markdown.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [email, content]
---

# Newsletter Writer

Turn recent updates and a few links into a newsletter issue people actually read.

## Procedure

1. **Gather material.** Read the updates, announcements, and links the user provides, plus any past issues in the workspace to match structure and voice. Ask for the audience and goal (retention, sales, engagement) if unclear.
2. **Verify and enrich.** Open each curated link and confirm it says what the user thinks it says; summarize it in your own words. If the issue needs an industry item, search the web for one recent, reputable source and cite it. Never invent statistics.
3. **Pick the lead.** Choose the single most valuable item for the reader and make it the opening story. Everything else is supporting material.
4. **Draft the issue.** Structure: greeting (one or two sentences, no throat-clearing), lead story, 2-4 short secondary items with subheads, curated links section with one-line takes, single primary CTA, sign-off. Keep total reading time under four minutes.
5. **Write subject lines.** Provide three subject line options under 50 characters plus a preview-text line under 90 characters for each. No clickbait; the subject must be true to the content.
6. **Tighten.** Cut every sentence that does not inform or move the reader to act. Read the draft aloud mentally; anything that sounds like corporate filler goes.
7. **Deliver.** Write to `drafts/newsletter-<date>.md` with subject options at the top, and report the path plus which subject line you recommend and why.

## Voice

- Write like one person emailing another: contractions, second person, short paragraphs.
- One idea per paragraph, two to three sentences max.
- Links get honest one-line descriptions, not "check this out."
- Enthusiasm is fine; superlatives without evidence are not.
