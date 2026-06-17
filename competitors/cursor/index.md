---
type: competitor
title: Cursor / Anysphere
description: AI-native developer-tools company building an end-to-end "AI software factory" — editor, code review, and a Git hosting platform.
volatility: slow
as_of: 2026-06
resource: https://cursor.com
sources:
  - "Anysphere raised $2.3B at a $29.3B valuation (Nov 2025): https://www.infoworld.com/article/4110558/cursor-owner-anysphere-agrees-to-buy-graphite-code-review-tool.html"
  - "Cursor acquires Graphite (Dec 2025): https://finance.yahoo.com/news/exclusive-cursor-acquires-code-review-153008616.html"
  - "Origin agent-native Git platform (announced): https://vff.ai/article/2026/05/21/cursor-sees-opening-as-github-flounders"
note: >
  Company-level facts only — comparison to Principal lives in trails. Per-product
  facts live in the product docs in this folder. Most likely to go stale: Origin's
  status (announced, not GA) and funding/valuation — re-check before leaning on them.
---

# Cursor / Anysphere

**Anysphere, Inc.** is the company behind **Cursor**, an AI-native code editor.
Following its 2025 funding and the Graphite acquisition, it is assembling an
end-to-end "AI software factory" spanning code authoring, review, and hosting.

## Overview

- **Vendor:** Anysphere, Inc.
- **Category:** AI-native developer tooling (editor + review + code hosting).
- **Funding:** the company raised **$2.3B in Nov 2025 at a $29.3B valuation**.
- **Strategy (stated):** own the full loop — *write* in the Cursor editor → *run*
  agents in parallel → *review* with Graphite-style workflows → *host and merge*
  on Origin. CEO Michael Truell has framed code **review** as the emerging
  bottleneck as AI is deployed across engineering teams.

## Products (this folder)

- [`editor.md`](editor.md) — the AI-native code editor (a VS Code fork).
- [`graphite.md`](graphite.md) — AI code review / stacked PRs (acquired Dec 2025).
- [`origin.md`](origin.md) — agent-native, Git-compatible hosting platform; a
  direct GitHub challenger (announced, targeting fall 2026).

## Competitive surface

Cursor's move from editor into **review** (Graphite) and **hosting +
collaboration** (Origin) pushes it directly into Principal's domain — code
understanding, review, and team context. The review-as-bottleneck framing
overlaps Principal's own thesis. How they compare is a **trail** concern.

## Updates

### 2026-06 · News — Origin positioned against GitHub
Cursor's Origin (agent-native Git forge) gained attention as GitHub faced
reliability strain under AI-agent load. Status: announced, not GA. Source: https://vff.ai/article/2026/05/21/cursor-sees-opening-as-github-flounders

### 2025-12 · Acquisition — Cursor acquires Graphite
Anysphere acquired code-review startup Graphite to add AI review and stacked PRs
to the Cursor stack. Source: https://finance.yahoo.com/news/exclusive-cursor-acquires-code-review-153008616.html

### 2025-11 · Funding — $2.3B at $29.3B valuation
Anysphere raised $2.3B. Source: https://www.infoworld.com/article/4110558/cursor-owner-anysphere-agrees-to-buy-graphite-code-review-tool.html
