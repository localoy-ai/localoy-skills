---
name: brand-voice-guide
description: Distill a brand voice guide -- tone, vocabulary, sentence patterns, do/don't examples -- from a business's existing copy files, and store it in memory so every other skill writes in that voice.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, memory]
tags: [brand, strategy]
---

# Brand Voice Guide

Read everything the business has already written, find the voice that is actually there, and pin it down so all future copy sounds like them.

## Procedure

1. **Collect the corpus.** Read the provided files: website copy, past emails, social posts, review replies, brochures. Note which pieces the owner flagged as "sounds like us" versus "an old agency wrote that" -- weight accordingly. If the corpus is under a few hundred words, say the guide will be provisional and mark it as such.
2. **Extract the patterns.** Work from evidence, not vibes: average sentence length, first person singular or plural, contractions or not, how they open and close, humor style, formality shifts between channels, and how they talk about price and competitors.
3. **Build the vocabulary lists.** Words and phrases they use repeatedly (keep), words they never use (avoid), and industry jargon they translate versus use straight. Include their names for their own products and services exactly as spelled in the corpus.
4. **Write do/don't pairs.** For five common situations (announcing news, handling a complaint, making an offer, talking about the team, asking for a review), write one "do" example in the voice and one "don't" example showing the generic-marketing version to avoid. The don'ts teach faster than the rules.
5. **Define the tone boundaries.** One short paragraph: what this voice is (for example, dry, direct, neighborly) and the two or three failure modes closest to it (stiff, salesy, jokey) so a writer knows which line not to cross.
6. **Review against the corpus.** Rewrite one real paragraph from the corpus using only the guide, and compare. If it drifts, tighten the guide until the rewrite is indistinguishable.
7. **Save, store, report.** Write the guide to `reports/brand-voice.md`, store the distilled voice profile in memory for other skills to recall, and report the path.

## Output

One file at `reports/brand-voice.md`: voice summary paragraph, pattern rules, keep/avoid vocabulary, five do/don't pairs, and tone boundaries. Short enough that a freelancer reads it in five minutes; specific enough that two writers using it produce matching copy.

## Memory

Stores the voice profile -- rules, vocabulary, and the do/don't pairs -- under the business's name. Skills like review-responder, gbp-post-writer, and proposal-writer recall it before writing. When the owner corrects a draft elsewhere, that correction should be added here so the stored voice, not just the file, stays current.
