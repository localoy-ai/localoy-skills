---
name: review-responder
description: Draft replies to new customer reviews from a review export or listing URL, matching the business's stored voice; flags genuinely angry reviews for the owner instead of auto-replying.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web, memory]
tags: [local, reputation]
---

# Review Responder

Answer every new review in the owner's own voice, and never let a reply make an angry customer angrier.

## Procedure

1. **Gather the reviews.** Read the provided review export files, or fetch the latest reviews from the listing URL via web search. Note the star rating, reviewer name, and full text of each.
2. **Recall the voice.** Load the stored brand voice and any past reply patterns from memory (sign-off style, whether the owner uses first names, phrases they always or never use). If nothing is stored, read a few of the business's existing replies and store what you learn.
3. **Triage.** Sort reviews into three buckets: positive (4-5 stars), fixable negative (specific complaint, calm tone), and escalate (threats, legal language, accusations of fraud or safety issues, or raw anger). Escalated reviews get no draft reply beyond a holding line; write a short note to the owner explaining what happened and what they should decide first.
4. **Draft positive replies.** Two to three sentences each: thank them by name, echo one specific detail from their review so it reads as human, and invite them back. Vary the openings so replies on the same page do not look templated.
5. **Draft fixable-negative replies.** Acknowledge the specific problem without arguing, state what the business will do or has done (only if the files confirm it -- never promise refunds or policy you cannot verify), and move the conversation offline with a named contact.
6. **Check facts.** Any claim in a reply (hours, policies, "we've fixed this") must come from the provided files. Anything unverifiable gets flagged in the draft with a `[CONFIRM]` marker rather than asserted.
7. **Save and report.** Write all drafts to `drafts/review-replies-<date>.md`, escalations first, and report the path plus counts: replied, escalated, flagged.

## Output

One markdown file at `drafts/review-replies-<date>.md`. Each entry shows the original review, the star rating, the draft reply (or escalation note), and any `[CONFIRM]` flags. Nothing is posted; the owner pastes approved replies themselves.

## Memory

Recalls the brand voice guide, preferred sign-off, and past escalation decisions. After each run, stores any new voice observations and which escalations the owner chose to answer personally, so future triage matches their judgment.
