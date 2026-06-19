---
type: competitor
title: CodeLayer (HumanLayer)
description: A commercial agent-orchestration "AI IDE" built on Claude Code, with structured human-in-the-loop workflows for shipping across the SDLC.
volatility: fast
as_of: 2026-06
resource: https://www.humanlayer.com
sources:
  - "HumanLayer site — CodeLayer / 'Token Smarter, not Harder', product + features (2026-06): https://www.humanlayer.com/"
  - "HumanLayer.dev — 'Close your editor forever', CodeLayer positioning (2026-06): https://www.humanlayer.dev/"
  - "YC F24 profile — founder Dexter Horthy, origin as human-in-the-loop API/SDK: https://www.ycombinator.com/companies/humanlayer"
  - "Crunchbase / Tracxn — founded 2023 Chicago, ~$500K seed (2024): https://www.crunchbase.com/organization/humanlayer"
  - "GetLatka — ~$660K revenue 2025, 6-person team (attributed): https://getlatka.com/companies/humanlayer.dev"
note: >
  Facts only — comparison to Principal lives in trails. This is a fast-moving,
  recently-repositioned product: HumanLayer pivoted from a human-in-the-loop
  agent API (YC F24) to the CodeLayer IDE. Most volatile claims: the exact launch
  framing/GA status of CodeLayer (0.1.0, public beta), pricing, and traction.
  Could not confirm a discrete dated press release for the 2026-06 humanlayer.com
  relaunch beyond the site itself — re-verify before leaning on a "launch date."
---

# CodeLayer (HumanLayer)

**HumanLayer** is a Chicago startup (YC F24) founded by **Dexter Horthy**. Its
current flagship is **CodeLayer**, an "AI IDE" for orchestrating AI coding
agents — built on **Claude Code** and shipped with structured, human-in-the-loop
workflows. The company originally launched as a human-in-the-loop API/SDK for AI
agents and has since repositioned around the IDE.

## Overview

- **Vendor:** HumanLayer, Inc. — founded 2023, Chicago; YC F24 batch. Founder/CEO **Dexter Horthy** (`dexhorthy`).
- **Product:** **CodeLayer** — an AI IDE for orchestrating coding agents, built on Claude Code. Taglines: *"Token Smarter, not Harder"* (humanlayer.com) and *"Close your editor forever"* (humanlayer.dev). Self-described "post-IDE IDE" / "Superhuman for Claude Code."
- **Category:** AI IDE / multi-agent coding orchestration.
- **Funding:** ~$500K seed, 2024 (Crunchbase/Tracxn); reported small/bootstrapped team (~6 people). No public Series A as of 2026-06.
- **Traction claim:** The company says everyone "from YC startups to the Fortune 500" uses it; GetLatka reports ~$660K revenue in 2025; the company has cited ~100% MoM MRR growth and paid pilots with publicly-traded teams. (All attributed.)
- **Origin:** Launched (YC F24) as an **API/SDK for human-in-the-loop AI agents** — routing agent approvals/escalations to humans via Slack/email — before repositioning around CodeLayer.

## Features

- **CodeLayer IDE** — desktop IDE to run and orchestrate AI coding agents; keyboard-first, command-palette navigation. Versioned as `codelayer` 0.1.0 (public/beta).
- **QRSPI workflow** — a six-phase structured process (**Q**uestions → **R**esearch → **D**esign → **S**tructure → **P**lan → **I**mplement) with verification checkpoints before implementation.
- **Comment-driven design reviews** — real-time human + AI collaboration on design documents, with inline feedback fed back into agent work.
- **Task management & workspaces** — groups agent sessions, artifacts, and git worktrees in shared, multi-repo team workspaces; artifact versioning/sharing across tasks.
- **Multi-agent orchestration ("MULTICLAUD")** — a local daemon runs many agent sessions in parallel on a laptop; cloud daemons handle long-running work.
- **BYOK** — bring your own model subscriptions (Claude, Codex, others); no per-token HumanLayer billing.
- **Cross-platform** — web, desktop, and mobile with a unified experience.
- **Context Engineering** — methodology coined by Horthy (April 2025); published as "advanced context engineering for coding agents" (ACE-FCA).

## Pricing

- **Starter** — free; up to 3 team members, 200 sessions/month.
- **Pro** — $100/user/month; unlimited tasks/sessions, multi-repo workspaces, remote daemons.
- **Enterprise** — custom; SSO/SAML, audit logs, on-prem options.

## Competitive surface

The CodeLayer features that fall inside Principal's domain — collaboration,
understanding, context — i.e. where the two products touch:

- **Comment-driven design reviews** — real-time human + AI collaboration on design docs, with feedback threaded into agent work (collaboration / human-in-the-loop curation overlap).
- **QRSPI structured workflows & "Context Engineering"** — codifying how understanding and context are assembled before an agent implements (understanding + context overlap).
- **Task workspaces / multi-agent orchestration** — agent-generated work grouped with artifacts and worktrees in shared team spaces (collaboration overlap; adjacent to our "human-curated, code-grounded" framing).
- **Built on Claude Code** — same underlying agent substrate.

How these compare to Principal's features is a trail concern, recorded there, not
here.

## Updates

Running log of what we learn as it happens — releases, funding, pricing, notable
news. Newest first. Facts only; implications go in trails. When an update changes
a core fact above, fold it into the relevant section and bump `as_of`.

### 2026-06-17 · News — humanlayer.com relaunched around CodeLayer
Observed humanlayer.com positioned as the CodeLayer "AI IDE" ("Token Smarter, not Harder"; "Close your editor forever" on humanlayer.dev), with Starter/Pro/Enterprise pricing and the QRSPI workflow front-and-center. Could not confirm a discrete dated press release for a "launch today" beyond the site itself; CodeLayer is at 0.1.0 (public/beta). Re-verify GA/launch framing. Source: https://www.humanlayer.com/ , https://www.humanlayer.dev/

### 2025 · Claim — traction & methodology
Company/third-party figures: ~$660K revenue in 2025 (GetLatka), ~100% MoM MRR growth cited, "Context Engineering" coined April 2025. Attributed, not independently verified. Source: https://getlatka.com/companies/humanlayer.dev

### 2024 · Funding — ~$500K seed
Raised ~$500K seed (Crunchbase/Tracxn). Founded 2023, Chicago; YC F24. Source: https://www.crunchbase.com/organization/humanlayer
