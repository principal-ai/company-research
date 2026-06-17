---
name: author-competitor-doc
description: Author or update a neutral, OKF-conformant competitor doc in this company-research KB (competitors/<slug>.md, type competitor) — web-verify the facts, capture features and the competitive surface, and keep a dated Updates log. Use when the user says "make a competitor doc", "add <competitor>", "research <competitor> for the KB", "write up <competitor>", "log an update on <competitor>", or invokes /author-competitor-doc. Facts only — the Principal-vs-them comparison belongs in a trail (author-informative-trail), never in the doc. NOT for the competitors index backlog and NOT for our own product docs.
---

# Author Competitor Doc

Author (or update) a single competitor doc in this knowledge base. Competitor
docs are **neutral and in isolation** — facts about the competitor only. The
comparison to Principal lives in a **trail**, never in the doc.

This pairs with the general `knowledge-base` conventions. The competitor doc is
the facts; a comparison trail is the answer that walks them.

## When to fire

- "make a competitor doc for X" / "add X" / "write up X for the KB"
- "research X (competitor) and capture it"
- "log an update on X" / "X just shipped Y — add it"
- explicit `/author-competitor-doc`

Don't fire when:

- The user wants the **comparison** (Principal vs. X) — that's a trail; use
  `author-informative-trail`.
- The user wants to edit the **competitors backlog list** — that's
  `competitors/index.md` (edit directly).
- The user wants one of **our** capabilities documented — that's a
  `type: product` doc under `product/`.

## Prerequisites

- This company-research repo (competitor docs live under `competitors/`).
- Web access — competitor facts must be **verified, not recalled**. Search first.

## Process

1. **Verify with the web.** Search for the vendor, product name + version, launch
   date, funding, traction claims, and current features. Prefer primary sources
   (vendor site/docs, press releases) and capture URLs + dates. Do not assert
   from memory — the whole value is dated, sourced facts.
2. **Pick the slug + path, and the shape.** Default to a flat
   `competitors/<slug>.md` (lowercase-kebab, e.g. `github.md`). If the competitor
   has **2+ substantial products** that move independently, use the **folder
   shape** instead (see "One doc vs. a folder" below). Either resolves the
   dangling link the `index.md` backlog has for it.
3. **Fill the template** (below) with neutral facts only.
4. **Competitive surface.** Flag *which* of the competitor's features fall in
   Principal's domain (collaboration, understanding, context). Flag the overlap;
   do **not** compare. End with the "comparison lives in a trail" line.
5. **Seed the Updates log** with what you just found (dated, newest first).
6. **Update `competitors/index.md`.** Move the entry from "Competitor
   candidates" to "Has a doc" with a live link.
7. **Offer the comparison trail.** The Principal-vs-X comparison is a separate
   artifact — route to `author-informative-trail`, threading this doc's
   "Competitive surface" against the relevant `product/*` docs.

To **log an update** on an existing doc: append a dated entry to `## Updates`
(newest first), and if it changes a core fact, fold it into the relevant section
above and bump `as_of`. Never edit past Updates entries.

## One doc vs. a folder (multi-product competitors)

Same discipline as the rest of the KB: **anchors before folders.** Default to one
flat doc per competitor, with each product a `##` section. Promote to a folder
**only when a single doc strains** — i.e. the competitor has 2+ substantial
products with their own features, pricing, and release cadence (e.g. Cursor →
editor + Graphite + Origin; Sourcegraph → Cody + Code Search).

Do **not** group competitors by the *threat* they pose (e.g. a
`github-replacers/` folder) — that grouping is an argument, so it's a **trail**,
not a folder. Categorize by entity only.

Folder shape:

```
competitors/<slug>/
  index.md      type: competitor — the COMPANY: overview, funding, strategy,
                  + a "Products (this folder)" list linking each product doc.
  <product>.md  type: competitor — ONE product: its own Overview / Features /
                  Competitive surface / Updates. Links back to index.md.
```

Rules for the folder shape:

- **Split entity from offerings.** Company-level facts (funding, positioning,
  strategy) live in `index.md`; product-level facts live in the product docs. One
  concern per doc still holds.
- **One home per fact.** A cross-product fact (e.g. a company-wide pricing change,
  or a market signal) lives in its one canonical home and is **linked**, not
  restated — including links out to `market/*` where the fact is a market signal.
- **Each product doc is independently pointable** so a trail marker can target
  `competitors/<slug>/<product>.md#<feature>` precisely.
- Move the whole folder's entry into `index.md` "Has a doc" with the company link
  plus inline links to each product doc.

## The template

```markdown
---
type: competitor
title: <Product> (<Vendor>)
description: <one neutral sentence — what it is and its category>
volatility: slow
as_of: <YYYY-MM>                     # when these facts were last verified
resource: <primary product URL>      # OKF: the underlying asset this doc is about
sources:
  - "<verified fact> (<date>): <URL>"
  - "<funding/traction source>: <URL or citation>"
  - Internal <source name> (<date or "undated">)
note: >
  Facts about the product only — comparison to Principal lives in trails, not
  here. <Name the claim most likely to go stale and what to re-check.>
---

# <Product> (<Vendor>)

<1–2 neutral sentences: who makes it and its category.>

## Overview

- **Vendor:** <company>.
- **Product:** <name + version>, launched <YYYY-MM-DD> (<short positioning quote>).
- **Category:** <category>.
- **Funding:** <total / last round + lead + year, if known>.
- **Traction claim:** <attributed metric — "the company says…">.

## Features

- **<Feature>** — <factual description>.
- **<Integrations>** — <what it connects to>.
- **<Models / platform / enterprise>** — <if relevant>.

## Competitive surface

The <Product> features that fall inside Principal's domain — collaboration,
understanding, context — i.e. where the two products touch:

- **<their feature>** — <neutral note on scope>.

How these compare to Principal's features is a trail concern, recorded there, not
here.

## Updates

Running log of what we learn as it happens — releases, funding, pricing, notable
news. Newest first. Facts only; implications go in trails. When an update changes
a core fact above, fold it into the relevant section and bump `as_of`.

### <YYYY-MM-DD> · <Release | Funding | Pricing | News | Claim | Review> — <headline>
<1–2 factual sentences.> Source: <URL>
```

## The two tenses (the load-bearing discipline)

A competitor doc has two parts with different rules:

| | Body (Overview / Features / Surface) | Updates log |
| --- | --- | --- |
| Tense | **current truth** — synthesized present state | **dated journal** — append-only |
| Edit rule | rewrite to stay accurate | never edit past entries; only append |
| On a material change | update the section **and** bump `as_of` | add a dated entry |

The log says *when you learned it*; the body says *what's true now*. A glance at
the newest Update vs. `as_of` tells you how fresh the synthesis is.

## Quality bar

- **Neutral isolation.** Every section is facts about the competitor; zero
  Principal comparison. "Competitive surface" flags overlap without arguing it.
- **Verified, dated, sourced.** No claim without a source; `as_of` reflects the
  last verification; `resource` points at the product.
- **Attributed claims.** Funding/traction are "the company says…", not asserted.
- **Comparison goes to a trail.** If you're writing "Principal does X better,"
  stop — that belongs in a comparison trail, not here.

## Checklist

- [ ] Facts web-verified; sources + dates captured.
- [ ] `type: competitor`, `as_of`, `resource`, `sources`, `note` all set.
- [ ] Body is neutral; no Principal comparison anywhere.
- [ ] Competitive surface flags overlap, ends with the trail-pointer line.
- [ ] Updates seeded (newest first).
- [ ] `index.md` entry moved to "Has a doc" with a live link.

## References

- General doc conventions: the `knowledge-base` skill.
- Bundle rules (frontmatter, types, conformance): `OKF.md`.
- The comparison artifact: `author-informative-trail` (thread this doc's
  Competitive surface vs. `product/*`).
- Backlog of competitors to write: `competitors/index.md`.

## Sibling skills (same shape, when you need them)

This skill is the template for two siblings you'll likely want as the bundle
grows — same web-verify + dated `## Updates` + neutral-facts discipline, just a
different `type` and folder:

- **author-investor-doc** → `investors/<slug>.md`, `type: investor` — who they
  are and what they value; the *case to them* is a trail.
- **author-market-signal-doc** → `market/<slug>.md`, `type: market-signal` —
  a dated, sourced market fact or trend; what it *means for us* is a trail.
