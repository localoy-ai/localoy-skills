---
name: case-study-writer
description: Turn client results, metrics, and interview notes into a problem-approach-results case study with a pull quote and summary stats, saved as a markdown draft.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [content, clients]
---

# Case Study Writer

Turn raw client results and interview notes into a case study a prospect will finish reading.

## Procedure

1. **Read the source material.** Go through the interview notes, metrics, emails, or project files provided. List the concrete facts: who the client is, what they struggled with, what was done, what changed, over what timeframe. Anything not in the source material does not go in the study.
2. **Verify the context.** Search the web for the client's site and industry basics to describe them accurately (size, market, location). Confirm any external claims — market figures, tool names, dates — before using them.
3. **Find the story.** Pick the single most impressive, defensible result as the spine. A case study proves one thing well; secondary wins go in a short list near the end.
4. **Draft in the standard shape.** Sections: title stating the result ("How X cut lead cost 40% in 90 days" — only if the number is real), client snapshot, The Problem (what it cost them, in their words where possible), The Approach (what was done and why, 3-5 concrete steps), The Results (numbers with timeframes), and a closing quote plus CTA.
5. **Use real quotes only.** Pull quotes verbatim from the interview notes, lightly trimmed for clarity with edits marked. If no usable quote exists, write a placeholder `[QUOTE NEEDED: topic]` and list suggested questions to ask the client.
6. **Add the numbers box.** Summarize 2-4 headline metrics in a stats block near the top. Every number must trace to the source material; note the source next to each in an HTML comment.
7. **Deliver.** Write to `drafts/case-study-<client-slug>.md` and report the path, the headline result, and any placeholders that need client input.

## Quality bar

- Zero invented facts, numbers, or quotes; gaps are flagged, not filled.
- The Problem section makes the reader feel the pain before the fix appears.
- Results include timeframe and baseline, not bare percentages.
- Reads in under five minutes; no paragraph over four sentences.
