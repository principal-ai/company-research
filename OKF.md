---
type: reference
title: OKF rules for this bundle
description: The hard conformance rules, target frontmatter, and type vocabulary for the company-research OKF bundle.
volatility: slow
as_of: 2026-06-16
sources:
  - https://github.com/GoogleCloudPlatform/knowledge-catalog/blob/main/okf/SPEC.md
---

# OKF rules for this bundle

This repo is a conformant **OKF** (Open Knowledge Format) bundle — markdown +
YAML frontmatter, one concept per file, hierarchical folders — with a few richer
extensions (freshness, sources) carried as legal OKF extension keys. Soft
authoring guidance lives in the `knowledge-base` skill; this file is the **hard
shape**: what frontmatter to write and what "conformant" means.

## Target frontmatter (per concept doc)

```yaml
---
# --- OKF ---
type: <concept-kind>          # REQUIRED by OKF, non-empty
title: <human title>          # recommended
description: <one sentence>   # recommended
timestamp: <ISO-8601>         # recommended — when the DOC last changed
tags: [<short>, <strings>]    # recommended, optional
# --- our extensions (OKF tolerates unknown keys) ---
volatility: evergreen|slow|perishable
as_of: <ISO date>             # when the CLAIM was last true/verified (≠ timestamp)
sources:
  - <citation or URL>
---
```

Two fields are easy to conflate: **`timestamp`** is OKF's "doc last modified";
**`as_of`** is our "the claim was true as of." Keep both — they answer different
questions. In this bundle, where most facts are claims about the world (a
competitor's funding, a market size, an investor's thesis), `as_of` is the one
that matters most: it tells a trail whether the fact is still safe to lean on.

## Type vocabulary

Pick a short, self-explanatory `type`. Working set for this bundle:

`product` · `competitor` · `market-signal` · `investor` · `reference`

Extend freely — OKF types are not registered centrally. Keep one type per doc.

## Conformance bar (the only hard rules)

- [ ] Every non-reserved `.md` has parseable frontmatter with a non-empty `type`.
- [ ] Reserved files use reserved names: `index.md` (directory listing),
      `log.md` (change history). `README.md` is **not** an OKF reserved name.
- [ ] Root `index.md` declares `okf_version: "0.1"`.

Everything else is soft guidance — don't reject a doc over a missing optional
field or a broken link. A broken link is **not-yet-written knowledge**, which in
a fresh bundle like this is the normal state.

## Conventions carried over from sister bundles

- **Neutral isolation.** Domain docs (competitor, market-signal, investor) state
  facts only. Comparison, positioning, and "why this is valuable" live in
  **trails**, never baked into a doc.
- **Append-only Updates log.** Entity docs that track a moving target keep an
  `## Updates` section (newest first). The body is current truth (rewrite to stay
  accurate, bump `as_of`); the log is a dated journal (never edit past entries).
