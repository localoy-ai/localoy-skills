---
name: gbp-post-writer
description: Write Google Business Profile posts (updates, offers, events) from a business brief or promo details, formatted to GBP limits, saved as ready-to-paste drafts.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [local, content]
---

# GBP Post Writer

Turn a promo, event, or plain business update into Google Business Profile posts that fit the platform and get clicks.

## Procedure

1. **Read the brief.** Open the provided files (offer details, event info, business notes). Note the business name, category, location, and what the post should accomplish. If no brief exists, ask for the offer or update in one line before writing anything.
2. **Pick the post type.** Map the request to a GBP type: Update (general news), Offer (has a deal, coupon code, or end date), or Event (has a date, time, and title). The type decides which fields you must fill.
3. **Check the facts.** Confirm hours, dates, prices, and addresses against the provided files. If a claim is missing (for example "voted best in town"), verify it with a web search or drop it. Never invent numbers or awards.
4. **Write the post.** Body of 150-300 characters for Updates, front-loading the point in the first 80 characters since GBP truncates previews. Offers get title, start/end dates, coupon code, and terms. Events get title, date, and time. One clear call to action per post, matched to a GBP button (Call now, Book, Order online, Learn more).
5. **Write two variants.** Same facts, different angle: one leading with the benefit, one leading with urgency or novelty. Label them A and B.
6. **Add an image note.** One line describing the photo to attach (subject, orientation, no text overlays that GBP will crop at 4:3).
7. **Save and report.** Write everything to `drafts/gbp-<slug>.md` and report the path back with a one-line summary of each variant.

## Output

A single markdown file at `drafts/gbp-<slug>.md` containing: post type, variant A, variant B, CTA button choice, offer/event fields if applicable, and the image note. Each variant is ready to paste into GBP with no editing.

## Voice

Plain and local. Write like the owner talking to a neighbor, not a brand talking to a market. No hashtags (GBP ignores them), no emoji walls, no phone numbers in the body (Google may flag them).
