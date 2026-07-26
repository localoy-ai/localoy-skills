---
name: proposal-writer
description: Draft a client service proposal from discovery-call notes -- scope, timeline, pricing table, terms -- reusing the firm's past proposal language and rates recalled from memory.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web, memory]
tags: [clients, sales]
---

# Proposal Writer

Turn discovery notes into a proposal that sounds like the firm, prices like the firm, and is ready to send after one read-through.

## Procedure

1. **Read the discovery notes.** Open the provided files: call notes, the prospect's ask, budget signals, and any RFP. List what the client said they want, what they actually need if those differ, and every constraint mentioned (deadline, budget ceiling, decision makers).
2. **Recall the firm's precedent.** Load from memory: past proposal language, standard service descriptions, current rates, payment terms, and which past clauses won or lost deals. Reuse proven wording instead of rewriting the firm's boilerplate each time. If no precedent is stored, ask for one past proposal to seed it.
3. **Research the prospect.** Read the prospect's website and public listings on the web so the proposal names their actual situation (current rating, site state, visible gaps) rather than generic pain points. Cite only what you can see.
4. **Define the scope.** Write deliverables as countable items ("4 GBP posts per month", "reply to all reviews within 2 business days"), each mapped to a line in the notes. Add an explicit out-of-scope list for the ambiguous items -- that list prevents the scope creep that kills small-agency margins.
5. **Build timeline and pricing.** A phase table with start and duration per phase, and a pricing table using the firm's stored rates. Never invent a rate: if a service has no stored price and none in the files, mark it `[RATE NEEDED]` for the owner. Include payment schedule and what happens on late payment, from stored terms.
6. **Assemble and tighten.** Order: one-paragraph summary of their situation, scope, timeline, pricing, terms, next step with a validity date. Cut anything the prospect did not ask about. Check that every number traces to notes, memory, or the prospect's own pages.
7. **Save, store, report.** Write to `drafts/proposal-<client>.md`, store any new language or rates back to memory, and report the path plus open `[RATE NEEDED]` items.

## Output

One file at `drafts/proposal-<client>.md`, structured for direct conversion to PDF: summary, scope with out-of-scope list, phase timeline, pricing table, terms, and a single clear next step. All placeholders listed at the top so nothing unfinished slips out the door.

## Memory

Recalls the firm's service descriptions, rates, terms, and past proposal outcomes; stores updates after each proposal, including which options the client accepted. Over time the firm's best wording becomes the default and pricing stays consistent across prospects.
