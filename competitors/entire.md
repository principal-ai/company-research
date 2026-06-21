---
type: competitor
title: Entire (Entire Inc.)
description: Developer platform for humans and agents from former GitHub CEO Thomas Dohmke; its first tool, Checkpoints, captures the agent session behind every git commit directly in git history.
volatility: medium
as_of: 2026-06
resource: https://entire.io/
sources:
  - "Entire launch — 'Developer platform for humans and agents'; Checkpoints concept (entire.io home, as of 2026-06): https://entire.io/"
  - "Entire announcement — $60M seed, investors, Checkpoints CLI (Feb 10, 2026): https://entire.io/news/former-github-ceo-thomas-dohmke-raises-60-million-seed-round"
  - "Former GitHub CEO raises record $60M dev tool seed at $300M valuation (TechCrunch, Feb 10, 2026): https://techcrunch.com/2026/02/10/former-github-ceo-raises-record-60m-dev-tool-seed-round-at-300m-valuation/"
  - "Entire launches with $60M to build AI-focused code management platform (SiliconANGLE, Feb 10, 2026): https://siliconangle.com/2026/02/10/entire-launches-60m-build-ai-focused-code-management-platform/"
note: >
  Facts about Entire only — comparison to Principal lives in trails, not here.
  Most likely to go stale: this is an early-stage company (launched Feb 2026) —
  Checkpoints is the only shipped piece; the "semantic layer" and the review/
  approve/deploy developer interface are roadmap, not product. The relevant
  surface for us is the comprehension/provenance angle ("the decisions behind the
  code"), which Entire captures automatically from agent sessions rather than via
  human curation.
---

# Entire (Entire Inc.)

**Entire** is a developer platform founded by **Thomas Dohmke**, GitHub's CEO for
four years until August 2025. It positions itself as a **"developer platform for
humans and agents"** and launched publicly on **February 10, 2026** with a $60M
seed round. Its thesis: Git tracks the code change but not *how* it was produced,
so in an agent-driven workflow the reasoning behind each change is lost.

## Overview

- **Vendor:** Entire Inc. (private; founded by Thomas Dohmke, ex-GitHub CEO).
- **Product:** Entire developer platform — launched **2026-02-10**; tagline
  *"Developer platform for humans and agents"* / *"Every commit tells a story. Now
  you can read it."*
- **Category:** AI-native code management / agent-provenance platform; framed as a
  next-generation developer platform (a GitHub-adjacent play by GitHub's former CEO).
- **Funding:** **$60M seed at a ~$300M valuation** — described by lead investor
  Felicis as the largest-ever seed round for a developer-tools startup. Lead:
  **Felicis**; participation from **Madrona, M12 (Microsoft), Basis Set, 20VC,
  Cherry Ventures, Picus Capital, Global Founders Capital**. Angels include
  **Gergely Orosz** (The Pragmatic Engineer), **Theo Browne** (T3 Chat), **Olivier
  Pomel** (Datadog CEO), **Garry Tan** (Y Combinator CEO), and **Jerry Yang**
  (AME Cloud / ex-Yahoo).
- **Traction claim:** the company says it is growing the team from ~15 to ~30
  people; Checkpoints shipped as open source at launch. (No usage metrics
  published as of Jun 2026.)

## Features

- **Checkpoints** *(open-source CLI; shipped at launch)* — automatically captures
  the **agent session behind each git commit**: the prompts, reasoning, decisions,
  and metadata such as token usage and which tools the agent used. Each commit is
  paired with the session that produced it as a **checkpoint stored directly in
  git history** — **no hosted service, no external database**. Positioned to stop
  agents "making the same mistakes" by giving them "the full history of how your
  codebase was built. Not just the code, but the decisions behind it."
- **Agent/tool support** — captures from **Claude Code, Gemini CLI, OpenCode,
  Cursor, GitHub Copilot CLI, and FactoryAI**, with "more integrations coming soon."
- **Semantic layer** *(roadmap)* — a layer to make the captured agent data easier
  for AI agents to consume.
- **Developer interface** *(roadmap)* — a UI for reviewing, approving, and
  deploying "hundreds of changes" a day.

## Competitive surface

The Entire features that fall inside Principal's domain — understanding, context,
collaboration — i.e. where the two products touch:

- **Checkpoints (the "decisions behind the code")** — capturing the *why* behind a
  change and binding it to specific commits is the same "intent attached to code"
  territory Principal's trails occupy; Entire derives it **automatically from agent
  sessions** (provenance capture) rather than from human curation.
- **"Platform for humans and agents" framing** — a shared surface where humans and
  agents collaborate on and learn from a codebase's history overlaps Principal's
  collaboration-primitive positioning.
- **Roadmap review/approve interface** — a human surface for reviewing and
  approving large volumes of agent changes overlaps Principal's agent-collaboration
  and review surface.

How these compare to Principal's features is a trail concern, recorded there, not
here.

## Updates

Running log of what we learn as it happens — releases, funding, pricing, notable
news. Newest first. Facts only; implications go in trails. When an update changes
a core fact above, fold it into the relevant section and bump `as_of`.

### 2026-02-10 · Funding + Release — Entire launches with $60M seed and open-source Checkpoints
Ex-GitHub CEO **Thomas Dohmke** launched **Entire** with a **$60M seed at a ~$300M
valuation** (lead: Felicis; with Madrona, M12, Basis Set, 20VC, Cherry Ventures,
Picus Capital, Global Founders Capital; angels incl. Gergely Orosz, Theo Browne,
Olivier Pomel, Garry Tan, Jerry Yang) — called the largest-ever dev-tool seed by
its lead. First product is **Checkpoints**, an open-source CLI that records the
agent session (prompts, reasoning, token use) behind each git commit, stored in
git history; supports Claude Code, Gemini CLI, OpenCode, Cursor, Copilot CLI, and
FactoryAI. Sources: https://entire.io/news/former-github-ceo-thomas-dohmke-raises-60-million-seed-round ·
https://techcrunch.com/2026/02/10/former-github-ceo-raises-record-60m-dev-tool-seed-round-at-300m-valuation/ ·
https://siliconangle.com/2026/02/10/entire-launches-60m-build-ai-focused-code-management-platform/
