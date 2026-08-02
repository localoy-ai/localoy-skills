# SEO playbook — the hard calls

Read this when the request is open-ended, when work spans several skills, or when
findings disagree about what matters. A single narrow ask does not need it.

## Prioritising findings

Rank by what it costs to ignore, not by how easy it is to fix. The order that
holds almost always:

1. **Pages that cannot be indexed at all.** A `noindex` on a money page, a robots
   rule blocking a section, a 404 in the sitemap. Nothing else matters while a page
   is invisible.
2. **Pages indexed under the wrong identity.** Missing or duplicate titles, a
   canonical pointing somewhere else, two URLs serving the same content. The page
   is visible but competing with itself.
3. **Pages that are fine but unfound.** Orphans, anything more than two clicks from
   the homepage, sections with no internal links in.
4. **Everything else.** Heading structure, markup, image attributes. Real, worth
   doing, never the reason traffic fell.

If a fix is one line and sits in bucket 4, still put it in bucket 4. Effort is a
tiebreaker inside a bucket, never a promotion between them.

## Reading a ranking change

Before explaining a drop, establish it happened. `serp-rank-tracker` first, always.

Then work down, and stop at the first that explains the size of the move:

- **Did the page change?** Compare against what you last recorded. A rewrite,
  a template change, a lost internal link.
- **Did the site change?** A migration, a redirect chain, a new robots rule.
- **Did the SERP change?** New competitors, a new feature block, the intent shifting
  under the query. `competitor-seo` answers this.
- **Did nothing change?** Then say so. "I could not find a cause" is a real finding
  and better than the plausible story that sends them rewriting a page for nothing.

Never attribute a move to an algorithm update you have not verified. It is the
easiest unfalsifiable answer in this field and it teaches them nothing.

## Sequencing multi-skill work

For "sort out our SEO" with no further steer:

1. `seo-audit` — learn the actual state. Everything downstream depends on it.
2. `keyword-research` — only once you know what the site is already about. Research
   first and you will target words the site cannot plausibly rank for.
3. `on-page-optimizer` on the pages where the audit and the keyword set overlap.
   That intersection is where the fastest movement lives.
4. `serp-rank-tracker` to set the baseline you will be judged against. Do this
   before the fixes land, not after — a baseline recorded afterwards proves nothing.
5. `competitor-seo` and `backlink-prospector` last. Both are slow, and both are
   easier to aim once the site's own house is in order.

Do not run all seven because you were asked a broad question. Three well-sequenced
skills with a clear finding beat seven reports nobody reads.

## When findings disagree

Two rules settle most conflicts:

- **Observation beats inference.** What you fetched outranks what you concluded.
- **The narrower claim wins.** "This page's title is 92 characters" survives; "the
  site has a titles problem" does not, unless you counted.

If two findings genuinely conflict and you cannot resolve them, report both and say
which you would act on first. Do not average them into a claim neither supports.
