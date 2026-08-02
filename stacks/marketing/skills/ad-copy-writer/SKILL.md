---
name: ad-copy-writer
description: Turn an offer brief into Google and Meta ad variants -- headlines, descriptions, primary text -- built around 3 distinct angles and sized to each platform's character limits.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [ads, content]
---

# Ad Copy Writer

Write ad copy a small business can paste straight into Google or Meta, with real variants to test rather than five rewordings of one idea.

## Procedure

1. **Read the offer brief.** Open the provided files: the offer, the audience, the landing page URL, and any past ad results. Identify the one concrete thing being sold and the one action the ad asks for. If the offer is vague ("get more customers"), stop and ask for the specific offer.
2. **Check the landing page.** Fetch the landing page URL. The ad must promise only what the page delivers -- same offer, same price, same wording for key terms. Note the exact phrases the page uses so the ad-to-page scent holds.
3. **Verify every claim.** Prices, discounts, "since 1998", "rated 4.8" -- each must appear in the brief files or be confirmed on the business's own pages via web search. Unverifiable claims are cut, not softened.
4. **Pick three angles.** Choose three genuinely different persuasion routes from: price/deal, speed/convenience, social proof, problem-agitation, local identity, guarantee/risk-reversal. Name each angle in the output so the test result teaches something.
5. **Write Google Ads copy.** Per angle: 5 headlines at 30 characters max and 3 descriptions at 90 characters max, counted, with at least one headline carrying the keyword and one carrying the offer. Note which headlines should be pinned.
6. **Write Meta copy.** Per angle: primary text (one short version under 125 characters, one longer version), a 40-character headline, and a 30-character link description. Front-load the hook before the "See more" fold.
7. **Save and report.** Write everything to `drafts/ads-<slug>.md` with a short testing note (which angle to run first and what a win would look like), and report the path.

## Output

One file at `drafts/ads-<slug>.md`, organized by angle, then by platform. Every line shows its character count. Ends with the testing note and a list of any claims that were cut for lack of verification, so the owner can supply proof and reinstate them.

## Voice

Concrete over clever. Numbers, place names, and specifics beat adjectives. No exclamation stacking, no "!" in Google headlines more than once per angle, and nothing the landing page cannot back up.
