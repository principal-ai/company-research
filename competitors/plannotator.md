---
type: competitor
title: Plannotator (backnotprop)
description: A local, browser-based plan-review and code-diff annotation layer for AI coding agents — annotate, send structured feedback back to the agent, and share with a team.
volatility: fast
as_of: 2026-06
resource: https://plannotator.ai/
sources:
  - "Plannotator site — 'Plan and code review for your agents' / 'Shape what gets built. Own what ships.', features + integrations (2026-06): https://plannotator.ai/"
  - "GitHub backnotprop/plannotator — dual MIT/Apache-2.0, v0.21.0 (2026-06-19), 117 releases, 729 commits, ~6.4k stars: https://github.com/backnotprop/plannotator"
  - "Product Hunt — maker Michael (@backnotprop); initial launch 2025-12-29, expanded 2026-04-29; 'Annotate, review, and share Claude Code plans. (Plugin/Hook)': https://www.producthunt.com/products/plannotator"
  - "Plannotator docs — OpenCode + other agent integration guides (2026-06): https://plannotator.ai/docs/guides/opencode/"
note: >
  Facts about the product only — comparison to Principal lives in trails, not
  here. NOT a HumanLayer product (a prior assumption); built by Michael
  (@backnotprop) + OSS contributors. Fast-moving: 117 releases by 2026-06 and the
  license recently moved from BSL to MIT/Apache — re-verify the OSS terms, the
  current version, and the state of the commercial "Workspaces" offering (beta /
  waitlist at room.plannotator.ai) before leaning on any of them.
---

# Plannotator (backnotprop)

**Plannotator** is a local, browser-based review surface that sits around AI
coding agents: it lets a human annotate an agent's **proposed plan** before
execution and review the agent's **uncommitted code diff** before commit, sending
structured feedback back to the agent. It is open source, built by **Michael
(`@backnotprop`)** with a community of contributors.

## Overview

- **Vendor / author:** Michael (`@backnotprop`) + open-source contributors. Independent project — **not** affiliated with HumanLayer.
- **Product:** **Plannotator** — a plan-review and code-diff annotation layer for coding agents. Initial Product Hunt launch **2025-12-29** (Claude Code plugin/hook); expanded launch **2026-04-29**. Taglines: *"Plan and code review for your agents"* and *"Shape what gets built. Own what ships."*
- **Category:** Human-in-the-loop review/annotation layer for AI coding agents.
- **License / state:** Dual **MIT or Apache-2.0** (recently transitioned from a Business Source License). Core plugin is GA, free, open source — `github.com/backnotprop/plannotator`, **v0.21.0 (2026-06-19)**, 117 releases, ~6.4k stars; actively maintained. The OSS code is what ships.
- **Commercial:** **Workspaces** — a paid team/live-collaboration offering, in **beta / waitlist** (`room.plannotator.ai`).
- **Install:** `curl -fsSL https://plannotator.ai/install.sh | bash`.

## Features

- **Plan review** — intercept an agent's proposed plan; annotate inline, mark deletions, suggest replacements, and send structured feedback back to the agent before it executes.
- **Code review** — PR-style diff viewer for the agent's uncommitted code, with line-level annotations and feedback that flows back into the agent loop.
- **Local-first / privacy** — runs entirely in the browser with no network calls; plans never leave the machine by default. Small plans encode in the URL hash; larger shared plans use end-to-end AES-256-GCM encryption.
- **Sharing & history** — encrypted share-by-URL, version history with plan diffs; **Workspaces** adds team live collaboration (beta).
- **Agents supported** — Claude Code, Codex, Copilot CLI, Gemini CLI, OpenCode, Kiro CLI, Droid, Amp, Pi.
- **Integrations** — VS Code, Obsidian, Bear, GitHub, GitLab.

## Competitive surface

The Plannotator features that fall inside Principal's domain — collaboration,
understanding, context — i.e. where the two products touch:

- **Human-in-the-loop plan/code review** — a human curates and annotates agent output (plan + diff) before it lands; overlaps Principal's human-in-the-loop, human-curated stance and its trail-based PR/diff review.
- **Line-level diff annotation** — PR-style diff walkthrough with inline annotations, in the same "guided review of agent changes" shape Principal targets.
- **Annotation sharing + team workspaces** — share-by-URL and team collaboration over the annotated artifact touch Principal's collaboration surface.
- **Feedback loop back to the agent** — structured annotations routed back to the coding agent, in Principal's context/feedback territory.

How these compare to Principal's features is a trail concern, recorded there, not
here.

## Updates

Running log of what we learn as it happens — releases, funding, pricing, notable
news. Newest first. Facts only; implications go in trails. When an update changes
a core fact above, fold it into the relevant section and bump `as_of`.

### 2026-06-20 · Review — initial doc
First capture. Verified: independent OSS project by Michael (`@backnotprop`), **not** HumanLayer. Dual MIT/Apache-2.0 (moved from BSL), **v0.21.0 (2026-06-19)**, 117 releases, ~6.4k stars, actively maintained — OSS plugin is what ships. Plan-review + code-diff annotation for agents (Claude Code, Codex, Copilot CLI, Gemini CLI, OpenCode, Kiro CLI, Droid, Amp, Pi); local-first, E2E-encrypted sharing. Commercial **Workspaces** in beta/waitlist (`room.plannotator.ai`). Launches: 2025-12-29 (initial), 2026-04-29 (expanded). Sources: https://plannotator.ai/ · https://github.com/backnotprop/plannotator · https://www.producthunt.com/products/plannotator
