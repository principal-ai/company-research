---
okf_version: "0.1"
title: Company Research — OKF bundle
description: Research substrate for Principal AI / Code Trails — product, competitors, market — kept pointable so trails can answer "what is this worth?" at any altitude.
---

# Company Research

A knowledge base whose job is to answer one question at several altitudes:
**what is Principal AI / Code Trails worth?** — at the product level, relative to
competitors, in light of where the market is going, and as an investment.

The docs here are **not** the deliverable. They're the *substrate*. The
deliverable is **trails**: a trail is the answer to a real question, and the
answer *is the path* — an ordered walk of markers, each pinned to one canonical,
sourced fact in these folders. Because every stop anchors to a pointable fact,
the answer carries its own evidence and stays honest as the facts update.

So the whole repo is organized around making each fact **pointable**: one
concept per doc, stable heading anchors, one canonical home, a source and an
as-of date on anything that can rot. That's what lets a trail marker land on
something solid. Conventions live in
[`.claude/skills/knowledge-base/SKILL.md`](.claude/skills/knowledge-base/SKILL.md);
the hard bundle rules (frontmatter, type vocabulary, conformance) live in
[`OKF.md`](OKF.md).

## Two halves of one mechanism

- **OKF** makes facts pointable — the discipline in `knowledge-base` + `OKF.md`.
- **Trails** turn pointable facts into grounded, auditable answers. Facts stay
  **neutral and isolated** in the docs; the comparison, the positioning, the
  "why this is valuable" lives in the trail — so the same fact base can carry an
  honest internal trail *and* a bullish investor trail without the docs taking a
  side.

## Structure

Top level is by **research domain** (the fact-sources). The value arguments are
trails *across* these folders, not folders themselves.

```
company/        Principal AI itself — the founders, founding story, public presence.
                  Facts about the team/company, distinct from the product below.
product/        Principal AI / Code Trails — what it is and how it's designed.
                  Capabilities and design decisions. Facts about our own product.
competitors/    One neutral doc per competitor (+ index.md backlog of who to cover).
market/         Market signals, trends, sizing, external evidence. Heavily dated/sourced.
```

## The trails this substrate is for

Each is a value argument at one altitude, threading markers across the folders:

- **product-value** — walks `product/`: what the thing does and why that matters.
- **competitive-value** — walks `competitors/*` ↔ `product/*`.
- **market-value** — walks `market/*` ↔ `product/*`.
- **investor case** — walks all of the above to make the investment argument.

## Status

- **Folder structure:** stood up; each folder has an `index.md` backlog.
- **Docs:** none yet — corpus is fresh. Backlogs name what's wanted.
- **Authoring:** competitor docs via the `author-competitor-doc` skill;
  market docs follow the same shape (see that skill's siblings note).
