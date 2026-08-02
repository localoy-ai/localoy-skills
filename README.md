# localoy stacks

The official skill suite for [localoy](https://localoy.fly.dev) — your agents, local first.

**A stack is a role.** Install one and use as much of it as the job needs; you are
not expected to pick skills yourself. Each stack carries a charter — what it owns,
what it refuses — plus the skills that do the work.

```
stacks/<stack>/
  STACK.md                 the charter and the routing table
  sections/
    manifest.json          registry of on-demand bodies
    playbook.md            the hard calls, read when the work is ambiguous
  skills/<skill>/
    SKILL.md               one procedure
```

| Stack | What it runs | Skills |
|---|---|---|
| `seo` | Audits, keywords, rankings, links | 7 |
| `content` | Everything you publish, in one voice | 8 |
| `marketing` | Campaigns, landing pages, email, the numbers | 6 |
| `sales` | Proposals, case studies, client reporting | 5 |
| `local` | Map presence, citations, customer questions | 4 |
| `gtm` | Positioning — **early; read its charter for what it does not cover** | 1 |

## Install

On any machine running the localoy daemon:

```sh
localoy install seo-audit        # loy install seo-audit works too
```

Name-only installs resolve against this repo. **The folder layout is not part of
that contract** — the daemon finds a skill by name at any depth, so the suite can be
regrouped without breaking an install. Any public GitHub repo works the same way:

```sh
localoy install you/your-skills my-skill
```

> Moving from a flat layout: skills used to sit at the repo root. Installing by name
> still works, but a daemon older than this change cannot resolve names inside
> `stacks/`. Upgrade the daemon, or install with an explicit path.

## Skill format

Each skill folder holds a `SKILL.md` — YAML frontmatter plus the markdown procedure
the agent follows:

```markdown
---
name: seo-audit
description: One sentence on what it does and what it produces.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]      # what it needs; granting is the agent's config
output_contract: [no_invented_scores, summary_table]
triggers: [audit my site, check my seo]
stages:                          # optional: each runs as its own verified turn
  - id: crawl
    goal: Fetch the pages and record the status of each.
    produces: work/pages.md
---

# Title

## Procedure
1. ...

## Quality bar
- ...
```

`capabilities` is a declaration, never a grant: what an agent may actually touch is
decided by that agent's own capability set on the daemon.

`output_contract` is the machine-checked half of the quality bar. The daemon reads
the file the skill produced — not the reply describing it — and a breach earns one
correction turn. Rule ids are defined by the daemon, so only published ones work.

`triggers` are the phrases that route a request here, in the user's own words. They
outrank name matching, which keeps a skill reachable when nobody would guess its
name.

`stages`, when present, run as one turn each with their own verification. A stage
must declare `produces`, or there is no way to tell a finished step from a skipped
one.

## Stack format

`STACK.md` carries the charter: what the role owns, what it refuses, and a routing
table mapping what a user says to the skill that answers it. Keep it thin — the
charter is read on every turn. Long-form judgment belongs in `sections/`, which is
read only when the charter says to.

## Contributing

PRs welcome. Keep procedures concrete (numbered steps, explicit outputs, a quality
bar), declare every capability you use, and bump `version` on any content change —
installs are content-addressed and pinned by digest.

Two rules that are easy to miss: a skill lives in exactly one folder, but any number
of stacks may list it by name; and never state a number you did not measure.
