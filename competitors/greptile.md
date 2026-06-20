---
type: competitor
title: Greptile
description: AI code-review agent that indexes the whole codebase into a semantic graph and reviews each PR against that full context; also answers natural-language questions about a codebase.
volatility: fast
as_of: 2026-06
resource: https://www.greptile.com
sources:
  - "Greptile v4 + new pricing (Mar 5, 2026): https://www.greptile.com/blog/greptile-v4"
  - "Series A — $25M led by Benchmark + v3 (Sep 23, 2025): https://www.greptile.com/blog/series-a"
  - "Anthropic customer story — Claude Agent SDK / Opus 4.5: https://claude.com/customers/greptile"
  - "Company benchmark (82% catch rate): https://www.greptile.com/benchmarks"
note: >
  Facts only — comparison to Principal lives in trails. Benchmarks and engagement
  metrics are the company's own — attributed, not asserted. Most likely to go
  stale: model version (Opus 4.5), pricing, and version cadence. The $180M
  valuation was pre-close reporting; the closed round's valuation is unverified.
---

# Greptile

**Greptile** is an AI code-review agent that indexes an entire codebase and reviews
each pull request against that full context — "catching bugs in the seams between
files, services, and shared dependencies, not just issues visible in the diff." It
also answers natural-language questions about a codebase. Founded by Daksh Gupta
(Y Combinator W24).

## Overview

- **Vendor:** Greptile.
- **Product:** Greptile — current major version **v4** (Mar 5, 2026).
- **Category:** AI code review / codebase Q&A.
- **Funding:** **$25M Series A led by Benchmark** (announced Sep 23, 2025), with
  Cory Levy, YC, and Initialized Capital; an earlier ~$4M seed (Initialized).
  *(Pre-close reporting floated a ~$180M valuation; the closed round's valuation
  is unverified.)*
- **Traction claim:** the company / Anthropic case study cite **2,000+
  organizations** (incl. NVIDIA, Brex, Coinbase) and **1B+ lines reviewed
  monthly**.

## Features

- **Full-codebase PR review** — indexes the repo into a semantic graph and reviews
  each PR with whole-codebase context to catch cross-file / architectural issues.
- **Agentic reviews** — v3+ is built on the **Anthropic Claude Agent SDK**; the
  agent "investigates like a skilled engineer," runs in a loop with tools
  (codebase search, learned rules), and (per the Anthropic case study) runs on
  **Claude Opus 4.5** at ~90% cache hit rates.
- **Codebase Q&A** — the API's `POST /query` answers natural-language questions
  about the repo and returns relevant files/functions/classes.
- **Integrations** — GitHub and GitLab (inline comments, suggestions, NL
  summaries); self-hosting; MCP; API.

## Pricing

v4 introduced base + usage: **$30 / developer / month, including 50 reviews/month,
then $1 per additional review** (the company says <10% of users exceed the
included usage); pre-Series-A startups get 50% off.

## Competitive surface

The Greptile features that fall inside Principal's domain — review, understanding,
context:

- **Whole-codebase PR review** — reviewing changes against full repo context is
  the point of closest overlap with Principal's review surface.
- **Codebase Q&A "expert"** — answering "how does X work" over a repo overlaps
  Principal's understanding domain.

How these compare to Principal is a trail concern, not recorded here.

## Updates

### 2026-03-05 · Release — Greptile v4 + new pricing
v4 is "better than v3 at catching tricky bugs, and also has a far lower false
positive rate." New pricing: $30/dev/mo incl. 50 reviews, then $1 each. Company-
cited engagement gains: addressed comments per PR +74% (0.92→1.60), share of
comments addressed 30%→43%, positive replies +68% (0.31→0.52). Source:
https://www.greptile.com/blog/greptile-v4

### 2025-09-23 · Funding + Release — $25M Series A (Benchmark) + v3
Greptile raised a $25M Series A led by Benchmark and shipped **v3**, a rewrite to
an agentic, multi-hop review architecture on the Claude Agent SDK; the company says
v3 catches 3x more critical bugs than v2. Source: https://www.greptile.com/blog/series-a

### 2026 · Claim — company benchmark
The company reports an **82% bug catch rate** across 50 real-world bugs, vs Bugbot
58% and CodeRabbit 44% (its own methodology). Source: https://www.greptile.com/benchmarks
