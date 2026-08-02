---
name: content-repurposer
description: Split one long-form piece (blog post, guide, transcript) into a tweet thread, standalone tweets, LinkedIn posts, and short video hooks, saved as one repurposing pack.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files]
tags: [content, social]
---

# Content Repurposer

Turn one long-form piece into a week of platform-native short content.

## Procedure

1. **Read the source.** Read the full piece from the workspace path the user gives. Note its core argument, the 3-6 strongest standalone ideas, any numbers or examples, and the best one-liners already in the text.
2. **Extract the idea list.** Write each idea as one plain sentence a stranger would understand without the article. Discard ideas that only work with full context. This list drives everything downstream.
3. **Write the tweet thread.** 5-8 tweets. First tweet is a hook that states the payoff or a sharp claim from the piece — no "a thread on X". Each tweet under 280 characters, one idea each, and the last tweet links back to the full piece with a reason to click.
4. **Write standalone tweets.** 4-6 single tweets, each self-contained: a stat with its meaning, a contrarian take, a how-to in one line, a quotable sentence lifted or tightened from the source.
5. **Write LinkedIn posts.** 2-3 posts, 100-200 words each. Open with a one-line hook on its own line, use short paragraphs and white space, end with a question or soft CTA. Rewrite for a professional first-person voice; do not paste tweet copy with more words.
6. **Write video hooks.** 4-6 spoken-word hooks (one or two sentences, under 5 seconds aloud) for short-form video, each paired with a one-line note on what the rest of the clip covers.
7. **Deliver.** Write everything to `drafts/repurpose-<slug>.md` under clear platform headings and report the path plus the counts per format.

## Quality bar

- Every piece stands alone; none says "in this article" or assumes the reader saw the original.
- Only claims and numbers that appear in the source; repurposing adds framing, never facts.
- Hooks differ from each other — no two open with the same structure.
- Voice matches the source author, compressed, not flattened into generic social-speak.
