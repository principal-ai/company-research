---
type: competitor
title: Cursor Canvas
description: Cursor feature where agents render interactive, React-based visualizations (dashboards, diagrams, charts) as durable artifacts instead of text responses. Shipped in Cursor 3.1.
volatility: fast
as_of: 2026-06
resource: https://cursor.com/blog/canvas
sources:
  - "Canvas announcement — Cursor 3.1 (Apr 15, 2026): https://cursor.com/blog/canvas"
  - "Canvas tool docs (reference): https://cursor.com/docs/agent/tools/canvas"
note: >
  Facts about the Canvas feature only — comparison to Principal lives in trails.
  New feature on a fast-moving product; re-verify specifics before leaning on
  them.
---

# Cursor Canvas

A Cursor feature in which the agent renders **interactive, React-based
visualizations** in place of (or alongside) a text response. Part of the
[Cursor editor](editor.md) by [Anysphere](index.md). Announced **Apr 15, 2026**
and shipped in **Cursor 3.1**.

## Overview

- **Vendor:** Anysphere, Inc.
- **Product:** Canvas (feature of the Cursor agent / Agents Window).
- **Category:** Agent output surface / visual artifact.
- **Released:** Cursor 3.1 (announced 2026-04-15).

## Features

- **Visual output** — agents produce dashboards and custom interfaces built from
  tables, boxes, diagrams, and charts rather than prose.
- **Multi-source data** — a canvas can join data from multiple sources, including
  local debug files, into a single chart.
- **Component library** — first-party UI components plus existing Cursor tools
  (e.g. diffs, to-do lists) embedded in the canvas.
- **Interactivity** — supports custom logic and interactive elements tailored to
  the request.
- **Durable artifacts** — canvases live alongside the terminal, browser, and
  source control in the Agents Window (persist, not one-shot text). Stored for
  reopening later without rerunning the underlying queries.
- **Access** — open from the card in the agent's response, the Command Palette
  ("Open Canvas"), or directly from the Agents Window.
- **Sharing** — shared canvases create **live snapshots** colleagues open via a
  browser link, without rerunning agents or reading chat history.
- **Skills extension** — developers can author skills that teach the agent new
  canvas types (e.g. a Docs Canvas skill for architecture diagrams). A skill
  packages trigger description, layout, data sources/queries, and formatting
  rules for consistent, team-wide output.

Stated use cases: incident-response dashboards (observability data), PR-review
interfaces (logical grouping / prioritization), evaluation analysis for model
testing, and research visualization / hypothesis tracking.

## Pricing & access gating

- **Sharing** requires a **paid plan (Pro, Teams, Enterprise)** and team
  membership; team admins can disable shared canvases via org settings.
- Requires privacy settings that permit data storage — **Legacy Privacy Mode
  blocks it**.

See [`market/cursor-pricing-2025.md`](../../market/cursor-pricing-2025.md) for the
editor's billing model.

## Competitive surface

- **Visual artifacts of a codebase / flow** — agent-generated dashboards,
  diagrams, and durable visual artifacts sitting next to source control overlap
  Principal's visual-comprehension territory (File City, trails).
- **Code review** — PR-review canvases that group and prioritize changes touch
  the same review surface as [Graphite](graphite.md) and Principal.

How these compare to Principal is a trail concern, not recorded here.
