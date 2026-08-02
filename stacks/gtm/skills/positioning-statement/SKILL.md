---
name: positioning-statement
description: |
  Produces a positioning statement — who it is for, what category it competes in,
  what it does better, and the proof — plus the messaging that follows from it.
  Use when asked "what do we say we are", "position this", "why would anyone pick
  us", or "our messaging is all over the place".
version: 0.1.0
publisher: localoy
license: MIT
tier: 2
capabilities: [files, web]
output_contract: [no_invented_scores, summary_table]
inputs:
  - id: what-the-business-sells
    why: you cannot position a company you cannot describe in one sentence
  - id: who-buys-it-today
    why: positioning aimed at the wrong buyer is worse than none, because it is confidently wrong
  - id: who-they-consider-instead
    why: a category claim is only meaningful against the alternatives a buyer actually weighs
escalation:
  decide: [wording, structure, which proof points lead]
  flag: [the category you claim, the competitor set you compare against]
  park: [publishing this anywhere public]
triggers:
  - position this
  - what do we say we are
  - why would anyone pick us
  - our messaging is inconsistent
produces: reports/{date}-positioning-{slug}.md
---
<!-- Generated from SKILL.md.tmpl — do not edit. Regenerate: scripts/gen-skills.sh -->

# Positioning statement

Decide what this business is, for whom, against what — and say it in language a
buyer would recognise as being about them.

## What you need first

- **What the business sells** — you cannot position a company you cannot describe in one sentence
- **Who buys it today** — positioning aimed at the wrong buyer is worse than none, because it is confidently wrong
- **Who they consider instead** — a category claim is only meaningful against the alternatives a buyer actually weighs

Check what you already know from this workspace and the conversation. Ask for everything still missing in a SINGLE message, then wait.

If no answer comes, do not guess your way through. Produce whatever is genuinely useful without the missing facts, state at the top which ones you lacked, and say what would change once you have them.

## What you decide, and what you do not

**Decide yourself** — wording, structure and which proof points lead. Act; do not ask and do not flag.

**Decide and flag** — the category you claim and the competitor set you compare against. Proceed on a named assumption and put it at the top of the output.

**Stop and wait** — publishing this anywhere public. Never resolve one of these by assumption, however long the wait.

## How you work

**Say only what you observed.** Every claim in the output traces to something you
actually read, fetched or were told. If you did not check it, do not assert it.

**Report what you could not do.** A page that would not load, a source you could
not reach, a step you skipped — these go in the output. Dropping them silently
turns partial work into work that looks complete, which is worse than work that
looks partial.

**Name your assumptions.** If you had to assume something to proceed, put it at
the top of what you produce, in one line. An assumption stated is corrected in
seconds; an assumption buried becomes a fact nobody checked.

**Finish or say you did not.** Do not pad to length, and do not present a first
pass as a final one.

## Before you start

Establish what you need before producing anything. A confident answer about a
business you have not described is the most expensive kind of wrong: it reads as
authoritative and nobody catches it until it is in front of a customer.

## Sources

**Cite what you used.** Name the URL, document or statement behind each finding,
inline, where the finding is. A sources list at the bottom that nothing points to
is decoration.

**Prefer what you fetched to what you recall.** When they disagree, the fetch
wins and you say so. When you could not fetch, say that instead of filling the
gap from memory.

**Do not launder a guess through a citation.** Linking a plausible source next to
an unverified claim is worse than the bare claim, because it borrows credibility
the claim did not earn.

## Procedure

1. **Write the one-sentence description.** From what you were told, not from the
   website's own copy. If the sentence needs an "and" to hold together, the
   business may be doing two things; say so rather than smoothing it over.
2. **Name the buyer precisely.** Not a demographic — a situation. "Agencies with
   3-15 staff who bill retainers and have no in-house SEO" beats "small
   businesses". If you cannot get past a demographic, say what you would need to.
3. **Establish the alternative set.** What the buyer does *instead*, which
   includes doing nothing and doing it manually. Fetch each competitor's own
   positioning line; quote it, do not paraphrase.
4. **Choose the category.** The frame the buyer already has, not one you invented.
   A category nobody searches for is a positioning statement nobody can act on.
   State which category you chose and which you rejected.
5. **Find the difference that survives a sceptic.** Something a competitor would
   struggle to claim tomorrow. Features rarely survive; structural facts,
   constraints and access usually do.
6. **Prove it.** Each claim gets one piece of evidence — a number you were given,
   a fact about how it works, a quote. A claim you cannot evidence gets cut, not
   softened.
7. **Write the statement.** For [buyer] who [situation], [name] is a [category]
   that [difference], because [proof]. Then three message variants: one line, one
   paragraph, one page.
8. **Write the report.** Save to the path in `produces`, with the summary table
   first, then the statement, the variants, the alternative set, and a list of
   what you could not verify.

## Quality bar

- The statement names one buyer, one category and one difference. Two of any of
  them means the positioning is not decided yet — say that instead of shipping
  both.
- Every competitor line is quoted from that competitor's own page, with the URL.
- The difference is falsifiable. "Better support" is not; "the only one that runs
  on your machine with your logins" is.
- Nothing describes the buyer in words the buyer would not use about themselves.
- What you could not verify is listed, not omitted.

## The output contract

These are checked against the file you write, not the reply you send. A failure earns one correction turn.

- Never state a score, rating or grade you did not measure. Report the values you actually observed instead — they are more useful and they are true.
- Open with a summary table — a row per page, item or finding — so the shape of the result is readable before the detail.
