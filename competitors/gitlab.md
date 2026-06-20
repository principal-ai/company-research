---
type: competitor
title: GitLab
description: AI-native DevSecOps platform whose agentic layer (Duo Agent Platform) and lifecycle context graph (Orbit) reason over a unified map of code, work items, pipelines, and production signals.
volatility: slow
as_of: 2026-06
resource: https://about.gitlab.com/
sources:
  - "GitLab Transcend announcements — 'Built for the agentic engineering era' (Jun 10, 2026): https://about.gitlab.com/blog/gitlab-transcend-announcements/"
  - "GitLab Announces New Capabilities to Give Enterprises Speed and Control at Agentic Scale — press release (Jun 10, 2026): https://ir.gitlab.com/news/news-details/2026/GitLab-Announces-New-Capabilities-to-Give-Enterprises-Speed-and-Control-at-Agentic-Scale/default.aspx"
  - "GitLab Duo Agent Platform general availability (Jan 15, 2026): https://ir.gitlab.com/news/news-details/2026/GitLab-Announces-the-General-Availability-of-GitLab-Duo-Agent-Platform/default.aspx"
note: >
  Facts about GitLab only — comparison to Principal lives in trails, not here.
  Most likely to go stale: beta→GA status of Orbit, Next-Gen SCM, and Governance
  for Agents (all pre-GA as of Jun 2026), and the performance claims (vendor
  internal-testing numbers, not independently verified). The relevant surface for
  us is the context/comprehension layer (Orbit), not the full DevSecOps platform.
---

# GitLab

**GitLab** (NASDAQ: GTLB) is an AI-native DevSecOps platform spanning source code
management, CI/CD, security, and project planning. At **GitLab Transcend** (June
10, 2026) it repositioned the platform around agentic software delivery — adding a
lifecycle **context graph** (Orbit), an agent-scale **Git backend**, and agent
governance on top of its existing **Duo Agent Platform**.

## Overview

- **Vendor:** GitLab Inc. (public; NASDAQ: GTLB).
- **Platform:** GitLab DevSecOps platform, available on GitLab.com, Self-Managed,
  and Dedicated deployments.
- **Anchor release:** GitLab Transcend, **2026-06-10** — "Built for the agentic
  engineering era."
- **Category:** AI-native DevSecOps platform / agentic software delivery.
- **Traction claim:** the company says Duo Agent Platform weekly active users
  grew **10x** since its January 2026 GA, and that its code review ranked in the
  top five on the Martian Offline Benchmark.

## Features

The capabilities introduced or highlighted at Transcend 2026 (statuses as of Jun
2026):

- **GitLab Orbit** *(public beta)* — a **lifecycle context graph** that
  continuously maps code, work items, pipelines, deployments, and production
  signals into a single live, queryable graph, so agents reason from first-party
  context instead of fragmented signals. The company says agents on Orbit
  responded up to **11x faster**, used up to **4.5x** better cost-effectiveness,
  and produced up to **45x fewer hallucinations** in internal testing, and cites a
  Compare the Market result of "70% accuracy for inline review placement vs. 58%
  for a RAG approach." Press materials describe Orbit as also running as a
  standalone data product with open APIs for third-party agents and tools.
  Orbit ships as two parts — **Orbit Local** (a CLI that parses a repo into a
  local DuckDB code graph, offline) and **Orbit Remote** (Knowledge-Graph-as-a-
  Service indexing a whole GitLab instance into managed ClickHouse). Its source
  is **public but not open source**: the repo
  ([gitlab-org/orbit/knowledge-graph](https://gitlab.com/gitlab-org/orbit/knowledge-graph),
  GitHub mirror gitlabhq/orbit-knowledge-graph) is under the **GitLab Enterprise
  Edition (EE) License** — source-available/proprietary, not an OSI license — and
  accepts community contributions.
- **Next-Generation Source Code Management** *(private beta)* — a rebuilt Git
  backend for agent-scale concurrency that replaces clone-based access with
  structured API access to project intelligence while keeping Git-protocol
  compatibility. Claimed: up to **2x fewer tokens**, **50x faster** wall-clock
  per task, and **1,000x less** network traffic.
- **GitLab Duo Agent Platform** *(GA since Jan 15, 2026)* — orchestration layer
  where agents pick up scoped issues, open merge requests, run reviews, and
  resolve feedback across the lifecycle. Includes agentic chat, foundational
  agents (e.g. Planner, Security Analyst), custom agents via an AI catalog, and
  foundational agentic flows. Integrates **external agents** including Anthropic's
  Claude Code and OpenAI's Codex CLI, and supports the **Model Context Protocol
  (MCP)** for reaching external data and tools without leaving GitLab.
- **Governance for Agents** *(private beta)* — identity, policy, audit, and
  approval framework giving real-time visibility into agent actions, inputs,
  reasoning, and anomalies.
- **Agents for Security** *(GA, GitLab Ultimate)* — automated scanning, triage,
  and vulnerability resolution paced to agent-speed code generation.
- **Pricing / packaging** — **GitLab Flex**, a single annual commitment reshaped
  monthly across seats and AI usage, subsuming usage-based **GitLab Credits**
  (Premium/Ultimate subscribers received $12/$24 in monthly credits under the
  earlier model).

## Competitive surface

The GitLab capabilities that fall inside Principal's domain — understanding,
context, collaboration:

- **GitLab Orbit (lifecycle context graph)** — turning a codebase plus its work
  items, pipelines, and runtime signals into a single navigable, queryable map
  for both agents and engineers overlaps Principal's File City / context
  territory; it is the closest piece to Principal's comprehension surface.
- **Next-Gen SCM as structured project intelligence** — exposing a repo as
  queryable project intelligence rather than a clone touches the same "codebase as
  navigable structure" idea, from the platform/infrastructure side.
- **Duo agentic flows + external agents (Claude Code, Codex CLI) + MCP** — driving
  code work through agents and orchestrating human review of their output overlaps
  Principal's agent-collaboration and review surface.

How these compare to Principal's features is a trail concern, recorded there, not
here.

## Updates

Running log of what we learn as it happens — releases, funding, pricing, notable
news. Newest first. Facts only; implications go in trails.

### 2026-06-20 · Claim — Orbit is source-available (EE License), not open source
The Orbit context graph has a public, active repo
([gitlab-org/orbit/knowledge-graph](https://gitlab.com/gitlab-org/orbit/knowledge-graph);
GitHub mirror gitlabhq/orbit-knowledge-graph; ~2.9k commits, 75+ contributors)
covering both Orbit Local (offline CLI → local DuckDB code graph) and Orbit Remote
(KG-as-a-Service). Its README states the license is the **GitLab Enterprise
Edition (EE) License** — source-available/proprietary, **not** an OSI open-source
license. Sources: https://gitlab.com/gitlab-org/orbit/knowledge-graph ·
https://github.com/gitlabhq/orbit-knowledge-graph · https://docs.gitlab.com/orbit/

### 2026-06-10 · Release — GitLab Transcend: "Built for the agentic engineering era"
GitLab announced **Orbit** (lifecycle context graph, public beta), **Next-Gen
Source Code Management** (agent-scale Git backend, private beta), **Governance for
Agents** (private beta), GA of **Agents for Security**, and **GitLab Flex**
packaging — repositioning the DevSecOps platform around agent-driven delivery. A
community hackathon ran June 10–24, 2026 to build on Orbit.
Source: https://about.gitlab.com/blog/gitlab-transcend-announcements/

### 2026-01-15 · Release — GitLab Duo Agent Platform GA
GitLab made the **Duo Agent Platform** generally available across GitLab.com,
Self-Managed, and Dedicated: agentic chat, foundational + custom agents, agentic
flows, external-agent integration (Claude Code, Codex CLI), and MCP support;
introduced GitLab Credits as usage currency.
Source: https://ir.gitlab.com/news/news-details/2026/GitLab-Announces-the-General-Availability-of-GitLab-Duo-Agent-Platform/default.aspx
