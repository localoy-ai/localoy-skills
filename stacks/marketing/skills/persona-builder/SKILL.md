---
name: persona-builder
description: Build 2-4 evidence-based buyer personas from customer notes, reviews, and analytics exports; stores them in memory and updates them as new facts arrive instead of rebuilding from scratch.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web, memory]
tags: [research, strategy]
---

# Persona Builder

Turn what customers actually said and did into personas grounded in evidence, and keep them current as new evidence lands.

## Procedure

1. **Recall existing personas.** Load any personas already stored in memory, with the evidence each was built on. If they exist, this run is an update: the goal is to confirm, adjust, or retire, not to start over.
2. **Read the raw material.** Go through the provided files: customer notes, review exports, support messages, and analytics exports. Pull direct quotes, repeated complaints, stated reasons for buying, and demographic signals the data actually contains.
3. **Fill gaps from public sources.** Where the files are thin, read the business's public reviews on the web for customer language. Use only what real customers wrote; industry "typical customer" articles are background, never evidence.
4. **Cluster into 2-4 personas.** Group by motivation and situation, not demographics alone -- two people of different ages hiring for the same job belong to one persona. Each persona needs at least three independent pieces of evidence; a pattern seen once is noted as a hypothesis, not a persona.
5. **Write each persona.** Name, one-line situation, what triggers the purchase, top two objections, where they found the business, and three verbatim quotes with sources. Numbers (percentages, average spend) appear only if the analytics files support them.
6. **Reconcile with memory.** Note what changed since last run: new evidence that strengthened a persona, contradictions that weakened one, hypotheses promoted or dropped. Store the updated personas and their evidence trail in memory.
7. **Save and report.** Write the full set to `reports/personas-<date>.md` with a changelog section, and report the path plus a one-line summary per persona.

## Output

One file at `reports/personas-<date>.md`: each persona on its own page-length section with its evidence cited, a hypotheses list for weak patterns, and a changelog against the previous version. Other skills (ad copy, drip campaigns) can take this file as input directly.

## Memory

Stores each persona with its supporting quotes and sources, plus open hypotheses awaiting evidence. On later runs it recalls all of this, so a single new review can update a persona without re-reading the whole corpus, and retired personas stay retired with the reason recorded.
