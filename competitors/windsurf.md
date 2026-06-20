---
type: competitor
title: Windsurf / Codemaps (Cognition)
description: Cognition's AI IDE (formerly Codeium, now relaunching as Devin Desktop) and its Codemaps feature — AI-annotated structured maps of a codebase for human+AI comprehension.
volatility: fast
as_of: 2026-06
resource: https://cognition.ai/blog/codemaps
sources:
  - "Windsurf Codemaps announcement (Nov 4, 2025): https://cognition.ai/blog/codemaps"
  - "Codemaps feature docs: https://docs.windsurf.com/windsurf/codemaps"
  - "Cognition acquires Windsurf (~$250M, Jul 14, 2025): https://techcrunch.com/2025/07/14/cognition-maker-of-the-ai-coding-agent-devin-acquires-windsurf/"
  - "Windsurf → Devin Desktop rebrand (Jun 2026): https://docs.devin.ai/desktop/devin-desktop-faq"
note: >
  Facts only — comparison to Principal lives in trails. Codemaps is the feature of
  interest (closest File City analog); the editor around it is mid-rebrand
  (Windsurf → Devin Desktop), so product naming and plan gating are the most
  likely to go stale. Per-plan availability of Codemaps was not stated and is
  unverified.
---

# Windsurf / Codemaps (Cognition)

**Windsurf** is the AI-native IDE (a VS Code fork, formerly **Codeium**) owned by
**Cognition** (the team behind **Devin**), which acquired it in July 2025.
**Codemaps** is a Windsurf feature that generates AI-annotated structured maps of
a codebase. As of June 2026 the editor is relaunching as **Devin Desktop**.

## Overview

- **Vendor:** Cognition (Windsurf / Devin).
- **Product:** Windsurf IDE + **Codemaps** feature (announced Nov 4, 2025).
- **Category:** AI IDE; Codemaps is a codebase-comprehension / code-map surface.

## Features (Codemaps)

- **AI-annotated structured maps** — "first-of-its-kind AI-annotated structured
  maps of your code": a navigable map whose nodes are code locations, with
  **trace guides** that explain relationships and execution paths between code
  elements; clicking a node jumps to the file/line.
- **Fast vs Smart generation** — "You can choose a **Fast** (SWE-1.5) or **Smart**
  (Sonnet 4.5) model to generate your Codemap" — Cognition's own SWE-1.5 for speed
  or Anthropic's Claude Sonnet 4.5 for deeper analysis.
- **Invocation** — open via the maps icon or **Cmd+Shift+C** in Windsurf; generate
  from a task prompt or from automatic suggestions / navigation history.
- **Into the agent** — reference a codemap inside **Cascade** conversations via
  `@{codemap}` to inject the map as agent context.
- **Shareable** — "These artifacts are sharable today across teams for learning
  and discussion." Codemaps "respects ZDR" (Zero Data Retention).
- **Related:** **DeepWiki** (Windsurf) provides symbol-level documentation;
  Codemaps map how components execute and relate.

## Pricing

No Codemaps-specific tier or price was stated in the announcement; per-plan
availability is unverified.

## Competitive surface

The Codemaps features that fall inside Principal's domain — understanding,
collaboration, context:

- **AI codebase maps with per-node explanations** — turning a codebase into a
  navigable, annotated map for comprehension is the **closest analog to File
  City** in this set.
- **Shareable map artifacts for team learning** — overlaps Principal's
  collaboration/curation surface.

How these compare to Principal is a trail concern, not recorded here.

## Updates

### 2026-06 · News — Windsurf rebrands to Devin Desktop
Cognition relaunched the Windsurf editor as **Devin Desktop** (June 2026), shifting
the default surface toward an agent command center while keeping the IDE. Source:
https://docs.devin.ai/desktop/devin-desktop-faq

### 2025-11-04 · Release — Codemaps
Cognition announced **Windsurf Codemaps**: AI-annotated structured maps of a
codebase with trace guides, Fast (SWE-1.5) / Smart (Sonnet 4.5) generation,
`@{codemap}` reference into Cascade, and shareable artifacts. Source:
https://cognition.ai/blog/codemaps

### 2025-07 · Acquisition — Cognition acquires Windsurf
Cognition (maker of Devin) acquired Windsurf (the remaining Codeium product, brand,
and team), reported at ~$250M, after Google separately hired Windsurf's CEO and
licensed tech. Source: https://techcrunch.com/2025/07/14/cognition-maker-of-the-ai-coding-agent-devin-acquires-windsurf/
