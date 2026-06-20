---
type: competitor
title: OpenAI Codex (Sites)
description: OpenAI's Codex agent and its Sites feature — the agent creates, deploys, and hosts interactive web apps (dashboards, planners, review workspaces) at a workspace URL instead of returning text.
volatility: fast
as_of: 2026-06
resource: https://developers.openai.com/codex/sites
sources:
  - "Codex for every role — Sites preview (Jun 2, 2026): https://openai.com/index/codex-for-every-role-tool-workflow/"
  - "Codex Sites docs: https://developers.openai.com/codex/sites"
note: >
  Facts only — comparison to Principal lives in trails. Sites is in preview and is
  the feature of interest (agent-output-artifact shape); the broader Codex agent is
  out of scope here. Most likely to go stale: preview/plan gating (Business/
  Enterprise only today) and exact pricing (not published). Keep distinct from
  ChatGPT Canvas (a separate text/code editing surface).
---

# OpenAI Codex (Sites)

**Codex** is OpenAI's coding agent. **Sites** is a Codex feature, announced
**June 2, 2026**, that lets the agent "create, save, deploy, and inspect websites,
web apps, and games hosted by OpenAI" — turning a prompt into a hosted, shareable
interactive app (dashboards, planners, review workspaces, project boards) instead
of a text answer. It is **distinct from ChatGPT Canvas** (a separate in-chat
text/code editing surface).

## Overview

- **Vendor:** OpenAI.
- **Product:** Codex **Sites** — **preview** (announced Jun 2, 2026).
- **Category:** agent-output artifact / hosted interactive app surface.
- **Traction claim:** OpenAI reports **5M+ weekly Codex users**, with
  non-developers ~20% and growing 3x faster than developers.

## Features

- **Agent-built hosted apps** — invoke with the **@Sites** plugin to turn a prompt
  (or compatible existing project) into a hosted site: dashboards, planners,
  review workspaces, project boards, lightweight tools.
- **Validate → save → deploy** — Codex validates the build, saves a reviewable
  candidate (linked to a Git commit), then deploys; "Every Sites deployment URL is
  a production deployment."
- **Hosting / backend** — projects build **Cloudflare Worker-compatible output as
  ES modules**, hosted by OpenAI, with **D1** (relational) and **R2** (object
  storage) bindings for persistent state.
- **Access control** — workspace-authenticated identity ("Sign in" with the
  workspace account); access modes are owner/admin-only, workspace-wide, or a
  custom audience.

## Pricing

In preview for **ChatGPT Business and Enterprise** workspaces ("with more plans
rolling out later"); Enterprise admins enable it via **RBAC**. No standalone price
for Sites was published.

## Competitive surface

The Sites features that fall inside Principal's domain — collaboration, sharing of
work artifacts:

- **Agent-rendered interactive apps/dashboards shared by URL** — making agent
  output a durable, shareable artifact overlaps the agent-output-artifact shape
  Principal addresses (alongside Cursor Canvas and Claude Artifacts).

How these compare to Principal is a trail concern, not recorded here.

## Updates

### 2026-06-02 · Release — Codex Sites (preview)
OpenAI announced **Sites** at its "Intelligence at Work" event: the Codex agent
creates, deploys, and hosts interactive web apps at a workspace URL, via the
@Sites plugin, on Cloudflare-Worker ES modules with D1/R2 storage; preview on
ChatGPT Business/Enterprise. Same announcement cited 5M weekly Codex users,
role-specific plugins, and Annotations. Sources:
https://openai.com/index/codex-for-every-role-tool-workflow/ ·
https://developers.openai.com/codex/sites
