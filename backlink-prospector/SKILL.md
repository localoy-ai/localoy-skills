---
name: backlink-prospector
description: Find realistic backlink prospects for a business — local press, suppliers, directories, guest posts — with a tailored outreach angle for each.
version: 0.1.0
publisher: localoy
license: MIT
capabilities: [files, web]
tags: [seo, outreach]
---

# Backlink Prospector

Build a short list of link prospects a small business could plausibly land, not a dump of DA-90 domains that will never reply.

## Procedure

1. **Profile the business.** Ask for the site URL, service area, and anything linkable they already have (events, sponsorships, data, notable staff, suppliers, memberships). Fetch the site to confirm.
2. **Search local press.** Look for local news sites, city blogs, and chamber-of-commerce pages that cover businesses like this one. For each, verify the outlet actually links out to businesses in its articles before listing it.
3. **Check supplier and partner links.** List the business's suppliers, vendors, franchises, or associations from the user's answers. Search each one's site for a "partners", "stockists", "members", or "find a dealer" page and record whether a listing with a link is realistic.
4. **Find relevant directories.** Search for niche and local directories in the industry and area. Skip generic spam directories; keep ones that real competitors appear in (verify by checking a competitor listing).
5. **Identify guest-post hosts.** Search for local or industry blogs that publish outside contributors. Confirm by finding at least one published guest piece on the site before including it.
6. **Write outreach angles.** For every prospect, write one specific angle: what the business offers them (a story, data, a sponsorship, a reciprocal listing) and who to contact if a contact page exists.
7. **Deliver the list.** Save to `reports/<date>-backlink-prospects-<slug>.md`: a table of prospect, type, URL, evidence it links out, angle, and effort level. Report the path back.

## Quality bar

- Every prospect was verified by loading its site; dead or parked domains are excluded.
- No fabricated metrics — do not quote domain authority or traffic figures you did not look up.
- Angles are specific to the prospect; if the best angle is "ask nicely", the prospect probably does not belong on the list.
