# localoy skills

The official skill suite for [localoy](https://localoy.fly.dev) — your agents, local first.

**One folder = one skill.** Every folder at the root of this repo is an
installable skill, named by its folder.

## Install

On any machine running the localoy daemon:

```sh
localoy install seo-audit        # loy install seo-audit works too
```

Name-only installs resolve against this repo (`localoy-ai/localoy-skills`,
folder = name). Any public GitHub repo works the same way:

```sh
localoy install you/your-skills my-skill
```

## Skill format

Each skill folder contains a `SKILL.md` — YAML frontmatter plus the markdown
procedure the agent follows:

```markdown
---
name: seo-audit
description: One sentence on what it does and what it produces.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]   # what the skill needs; granting is the agent's config
tags: [seo, audit]
---

# Title

## Procedure
1. ...
```

Supporting files (templates, scripts) may sit beside `SKILL.md`. A skill is
capped at 64 MB — skills are text plus small scripts, not software.

`capabilities` is a declaration, never a grant: what an agent may actually
touch is decided by that agent's own capability set on the daemon.

## Contributing

PRs welcome. Keep procedures concrete (numbered steps, explicit outputs, a
quality bar), declare every capability you use, and bump `version` on any
content change — installs are content-addressed and pinned by digest.
