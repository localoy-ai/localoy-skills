---
name: blog-post-writer
description: Draft a publish-ready blog post from rough notes, an outline, or a topic — researched, structured, and written in the company voice.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [content, writing]
---

# Blog Post Writer

Turn the user's input — rough notes, an outline, a bare topic — into a
publish-ready blog post.

## Procedure

1. **Understand the brief.** Identify the topic, the intended reader, and the
   goal of the post (educate, announce, persuade). If the input names none of
   these, infer conservatively from context rather than asking.
2. **Research.** Use web search to verify claims and gather two or three
   supporting facts or examples. Never invent statistics; if a claim cannot
   be sourced, soften it or drop it.
3. **Outline.** Title, hook, three to five sections, conclusion with one
   clear call to action.
4. **Draft.** Write the full post in markdown. Short paragraphs. Concrete
   examples over abstractions. No filler phrases.
5. **Save.** Write the finished draft to `drafts/<slug>.md` in the workspace,
   where `<slug>` is the kebab-cased title. Report the path back.

## Voice

- Plain, direct sentences. Confidence without hype.
- Avoid: "in today's fast-paced world", "unlock", "leverage", "delve".
- Prefer specifics ("cut prompt cost 6×") over vague claims ("dramatically
  faster").
