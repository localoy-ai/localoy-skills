---
name: video-script-writer
description: Script short-form or explainer videos from a topic or brief — timed hook, spoken beats, b-roll and on-screen text notes, and CTA — formatted as a two-column markdown script.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [content, video]
---

# Video Script Writer

Turn a topic into a shootable script with every second accounted for.

## Procedure

1. **Scope the video.** From the brief, fix the format (short-form under 60 seconds, or explainer 2-5 minutes), platform, audience, and the single takeaway the viewer should leave with. Ask if the length or goal is unspecified; a 30-second script and a 3-minute script are different jobs.
2. **Verify the substance.** Search the web to confirm any facts, numbers, or product claims the script will state aloud. Spoken claims are hard to retract; anything unverified gets cut or reworded as opinion.
3. **Write the hook first.** First 3 seconds, one or two spoken sentences that name the viewer's problem or make a specific claim. Write three hook options; recommend one. No "hey guys" or intros — the hook is the first frame.
4. **Outline the beats.** 3-5 beats for short-form, 5-8 for explainers. Each beat is one idea that earns the next second of watching. Order for retention: strongest material early, payoff before the CTA, no saving the best for last.
5. **Script both columns.** For each beat write the spoken words (conversational, contractions, sentences under 15 words) and the visual column: b-roll direction, on-screen text, and cut notes. Mark rough timestamps per beat so total runtime hits the target at roughly 140 spoken words per minute.
6. **Land the CTA.** One ask, stated in five seconds or less, tied to the video's takeaway. For short-form, also write the caption and 3-5 hashtags.
7. **Deliver.** Write to `drafts/video-script-<slug>.md` as a two-column table (AUDIO | VISUAL) with timestamps, hooks at top, and report the path, runtime, and recommended hook.

## Output

- Every spoken line is written to be said aloud — read it mentally at pace; rewrite anything that trips.
- Timestamps sum to the target length within 10%.
- Visual column gives a shooter enough to film without asking questions.
- No facts in the script that step 2 did not verify.
