---
type: competitor
title: GitHub (Microsoft)
description: The incumbent code-hosting, collaboration, and DevOps platform, plus the Copilot AI suite — the baseline AI-native challengers are measured against.
volatility: slow
as_of: 2026-06
resource: https://github.com
sources:
  - "Octoverse 2025 — 180M+ developers, activity metrics: https://github.blog/news-insights/octoverse/octoverse-a-new-developer-joins-github-every-second-as-ai-leads-typescript-to-1/"
  - "Copilot 4.7M paid subscribers (Jan 2026): https://www.getpanto.ai/blog/github-copilot-statistics"
  - "Reliability strain under AI-agent load; Microsoft routing to AWS (Jun 2026): https://www.theregister.com/software/2026/06/12/github-outages-persist-as-ai-coding-drives-traffic-surge/"
note: >
  Facts only — comparison to Principal lives in trails. Most volatile facts: the
  reliability/outage situation and the Azure/AWS routing response are moving weekly
  (mid-2026); re-verify before leaning on them.
---

# GitHub (Microsoft)

The dominant Git-based code-hosting, collaboration, and DevOps platform, a
subsidiary of **Microsoft** (acquired 2018 for $7.5B). The incumbent that the
new AI-native code platforms position themselves against.

## Overview

- **Vendor:** GitHub, Inc., a subsidiary of Microsoft.
- **Category:** code hosting / collaboration / DevOps platform (Git forge) + AI suite.

## Scale (per Octoverse 2025)

- **180M+ developers** — one new developer joined roughly every second (~36M added).
- **230 new repositories per minute.**
- **43.2M pull requests merged per month** (up 23% YoY).
- **~1B commits pushed in 2025** (up ~25% YoY).

## Copilot

- **20M cumulative users** (July 2025); **4.7M paid subscribers** (Jan 2026, ~75% YoY growth).
- Adopted by **90% of Fortune 100**; the company says 80% of new GitHub developers use Copilot in their first week.

## Products

- **Repositories & collaboration** — hosting, pull requests, issues; the system of record.
- **Actions** — CI/CD.
- **Copilot** — AI coding assistant suite.
- **Codespaces** — cloud development environments.
- **Stacked PRs** — launched to help teams break large agent-generated submissions into reviewable increments.

## Reliability under AI-agent load

A distinct fact cluster (mid-2026): autonomous coding agents shifted GitHub's
traffic profile faster than its capacity planning assumed.

- **Agent-opened PRs surged** from ~4M (Sep 2025) to 17M+ (Mar 2026) — ~325% in six months.
- Reported **~275M AI-agent commits per week.**
- **Nine outages in May 2026**; June availability reported below the 99.9% enterprise SLA.
- Microsoft confirmed (2026-06-16) it is **routing GitHub traffic through AWS**, with an Azure cutover planned July 2026; GitHub pivoted messaging to "Availability First."

## Competitive surface

The GitHub capabilities that fall inside Principal's domain — collaboration,
understanding, context:

- **Copilot** — AI code generation and chat over a repo.
- **Pull requests / review** — the collaboration and review surface.
- **Repository as system of record** — the canonical home of a team's code and history.

How these compare to Principal is a trail concern, recorded there, not here.

## Updates

### 2026-06-16 · News — Microsoft routes GitHub traffic to AWS
After sustained AI-agent-driven load and May outages, Microsoft confirmed routing some GitHub traffic through AWS while migrating components to Azure (cutover planned July 2026). Source: https://www.theregister.com/software/2026/06/12/github-outages-persist-as-ai-coding-drives-traffic-surge/

### 2026-01 · Claim — Copilot 4.7M paid subscribers
GitHub reported 4.7M paid Copilot subscribers, up ~75% YoY. Source: https://www.getpanto.ai/blog/github-copilot-statistics

### 2025 · Claim — Octoverse: 180M+ developers
Annual Octoverse reported 180M+ developers and record activity. Source: https://github.blog/news-insights/octoverse/octoverse-a-new-developer-joins-github-every-second-as-ai-leads-typescript-to-1/
