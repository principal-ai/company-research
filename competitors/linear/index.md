---
type: competitor
title: Linear
description: Work-tracking / project-management platform for software teams, now extending from issues into AI agents and code review — positioning itself as the surface where software development happens end to end.
volatility: slow
as_of: 2026-06
resource: https://linear.app
sources:
  - "Introducing Linear Agent — public beta (Mar 24, 2026): https://linear.app/changelog/2026-03-24-introducing-linear-agent"
  - "Linear Diffs — launched May 28, 2026: https://linear.app/changelog/2026-05-27-linear-diffs"
  - "Series C — $82M at ~$1.25B led by Accel (2025): https://linear.app/now/building-our-way"
  - "Reported ~$100M ARR / ~$1.3B valuation: https://getlatka.com/companies/linear.app"
note: >
  Company-level facts only — comparison to Principal lives in trails. Per-product
  facts live in the product docs in this folder. Most likely to go stale:
  Agent/Code Intelligence availability and its usage-based pricing (announced as
  "beyond a certain threshold"), and funding/valuation figures (reported by
  third parties) — re-check before leaning on them.
---

# Linear

**Linear** is a work-tracking and project-management platform for software teams
(issues, projects, roadmaps, cycles). Through 2025–2026 it has extended beyond
tracking into **AI agents** (Linear Agent) and **code review** (Diffs),
positioning itself as the surface through which software development happens —
from a production issue, to a ticket, to an agent doing the work, to review and
ship — without leaving Linear.

## Overview

- **Vendor:** Linear (Linear Orbit, Inc.).
- **Category:** software work-tracking / project management, extending into agent
  orchestration and code review.
- **Funding:** the company reports **~$134M raised** across 4 rounds; most recent
  was an **$82M Series C at a ~$1.25B valuation** (2025), led by **Accel** with
  Sequoia and 01A. *(figures reported by the company and third parties.)*
- **Traction claim:** third parties report **~$100M ARR**; Linear cites customers
  including OpenAI, Scale AI, Perplexity, Vercel, Mercury, Ramp, and Cash App.
- **Strategy (stated):** make the **issue/ticket the unit of work** and let teams
  assign that work to **agents**, then **review and ship** the resulting code from
  inside Linear — closing the loop from production signal → triage → agent → PR →
  review. The Series C (2025) priced in this agentic pivot, which the March 2026
  Agent announcement formalized.

## Products (this folder)

- [`agent.md`](agent.md) — **Linear Agent**: AI grounded in the workspace; turns
  discussions into issues, synthesizes context, and (via Code Intelligence) takes
  code-aware tasks. Public beta, Mar 2026.
- [`diffs.md`](diffs.md) — **Linear Diffs**: review PRs inside Linear with
  structural diffing and (beta) guided, semantic-order walkthroughs; syncs to
  GitHub. Launched May 2026.

## Competitive surface

Linear's move from **tracking** into **agent-driven work** and **code review**
pushes it into Principal's domain — code understanding, review, and team context —
from the *work-management* side rather than the editor side. The **guided
reviews** (semantic-order PR walkthroughs) and the **ticket → agent → code →
review** loop are the points of closest overlap. How they compare is a **trail**
concern, not recorded here.

## Updates

### 2026-05 · Release — Linear Diffs (code review in Linear)
Linear shipped **Diffs** (launched May 28, 2026): review PRs from any issue inside
Linear with unified/split structural diffs, a Reviews inbox, and a beta **guided
reviews** mode that walks reviewers through large PRs in semantic order; iterate
with a background coding agent and sync back to GitHub. See [`diffs.md`](diffs.md).
Source: https://linear.app/changelog/2026-05-27-linear-diffs

### 2026-03 · Release — Linear Agent (public beta)
Linear introduced **Linear Agent**, an AI grounded in the workspace that
synthesizes context, makes recommendations, and takes action across roadmaps,
issues, and code, with **Code Intelligence** (code-aware tasks) announced as
coming to Business/Enterprise. See [`agent.md`](agent.md).
Source: https://linear.app/changelog/2026-03-24-introducing-linear-agent

### 2025 · Funding — Series C ($82M at ~$1.25B)
Linear raised an $82M Series C led by Accel at a ~$1.25B valuation; the round
followed the launch of "Linear for Agents." Source: https://linear.app/now/building-our-way
