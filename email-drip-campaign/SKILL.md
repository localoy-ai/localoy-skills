---
name: email-drip-campaign
description: Design a 5-7 email nurture sequence from a lead magnet or offer brief -- send timing, subject lines, and full body copy for each email, saved as one ready-to-load draft file.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [email, conversion]
---

# Email Drip Campaign

Build a complete nurture sequence -- timing, subjects, full copy -- that moves a new lead from download to purchase without sounding like a sequence.

## Procedure

1. **Read the source material.** Open the provided files: the lead magnet, the offer, audience notes, and any existing emails. Establish what the lead just received, what the business ultimately sells, and the gap between the two the sequence must bridge.
2. **Verify the offer details.** Prices, guarantees, booking links, and deadlines come from the files or the business's live pages (check via web). Anything unconfirmed is marked `[CONFIRM]` in the draft rather than asserted.
3. **Map the arc.** Plan 5-7 emails, each with one job: deliver and set expectations (day 0), quick win from the lead magnet (day 1-2), problem and stakes (day 3-4), proof or story (day 5-6), the offer (day 7-8), objection handling (day 9-10), last call if the offer expires. Adjust count and spacing to the sales cycle in the brief.
4. **Write subjects and preview text.** Two subject line options per email, under 50 characters, plus preview text that extends the subject instead of repeating it. Curiosity is fine; bait that the body does not pay off is not.
5. **Write the bodies.** 100-250 words each, one idea per email, one link per email, plain-text feel over designed blocks. First-person from the owner. Each email must stand alone for readers who skipped the previous one.
6. **Tighten the sequence.** Read the seven emails in a row. Cut repeated phrases, vary openings, and confirm the offer email asks plainly for the sale. Check that every link target exists.
7. **Save and report.** Write the sequence to `drafts/drip-<slug>.md` and report the path with the email count and total span in days.

## Output

One file at `drafts/drip-<slug>.md`. A timing table up top (email number, day, job, subject A), then each email in full: both subject options, preview text, body, link target. Ready to paste into any email tool, with `[CONFIRM]` markers listed at the end for the owner to resolve before loading.

## Voice

Warm, specific, unhurried. The reader gave an email address, not permission to be shouted at. Short sentences, real details from the brief, and no urgency that is not literally true.
