---
type: market-signal
title: Claude Code Artifacts — shareable pages from agent sessions (2026)
description: Anthropic ships Artifacts in Claude Code — live, interactive web pages published from a session (PR walkthroughs, dashboards, investigation timelines) shared on a private claude.ai URL.
timestamp: 2026-06-19
volatility: perishable
as_of: 2026-06-19
tags: [ai-coding, agent-output, collaboration, review]
sources:
  - https://code.claude.com/docs/en/artifacts
---

# Claude Code Artifacts — shareable pages from agent sessions (2026)

One aspect per heading.

## The release
Anthropic added **Artifacts** to Claude Code (in beta): the agent publishes a
live, interactive web page from a session to a private URL on claude.ai. The
page opens in a browser and updates in place as the session continues. Claude
writes an HTML or Markdown file in the project, then publishes it (asking
permission before publishing a new artifact).

## What it's for
The documented use cases are squarely about making agent output legible and
shareable rather than read line-by-line in a terminal:
- Walk a reviewer through a pull request with **annotated, color-coded diffs**.
- Render a **dashboard** from data the session already pulled.
- Lay out implementation/design **options side by side** to compare.
- Keep an **investigation timeline / work-in-progress checklist** that fills in
  while a long task runs.
- Send a teammate a **link** instead of pasting terminal output into Slack.

## How sharing works
A new artifact is private to its author; the author shares it from the page
header to specific people or to everyone in the organization. Sharing stops at
the org boundary — viewers must be signed in to claude.ai in the same org, and
there is no public/external sharing. Artifacts are **viewable, not co-edited**:
the author remains the only writer; viewers see each published version.

## Constraints
Each artifact is one self-contained static page under a strict CSP: no external
requests, no backend (cannot store form input, authenticate viewers, or call an
API at view time), single page only (in-page anchors, not routes). Source file
must be `.html`, `.htm`, or `.md`; rendered page ≤16 MiB. Styled pages are more
output-token-intensive than the equivalent terminal text.

## Availability
Beta. Requires a **Team or Enterprise** plan, sign-in to claude.ai via `/login`
(API key / gateway / cloud-provider credentials cannot publish), and the
**Anthropic API** provider (not Bedrock, Vertex, or Microsoft Foundry). Blocked
under CMEK, HIPAA, or Zero Data Retention org policies. Content is stored on
Anthropic-operated infrastructure, visible only to authenticated org members;
admins control enablement, retention, and audit logging.

## Why it's a signal
A first-party agent vendor is now treating "how do humans see, share, and sign
off on what the agent did" as a product surface — annotated PR walkthroughs,
dashboards, and investigation timelines. That demand is the category Principal
is built into.

*Where Principal stands:* the validation is
real, but the **design of the Artifact limits exactly the shareability and
composability that trails are built for**. An Artifact is a *static snapshot* — a
self-contained single page under a strict CSP (no external requests, no backend,
no routes), so it can't link into other artifacts, bind to live source as code
moves, or carry runtime/telemetry; it's a frozen render of one session, not a
composable unit. Its sharing is *org-bounded and read-only* — private to the
author, viewable (not co-edited), and walled at the organization boundary with no
external sharing. Trails are the opposite on both axes: **code-grounded** (each
marker pinned to file:line, so it stays honest as code changes and can carry
runtime/OTEL), and **composable + curated** (markers compose, trails bundle into
topics, and a human curates and vouches for them across teams). The fuller
product comparison lives in a **trail**; the takeaway here is that the Artifact
validates the demand while showing the ceiling of a snapshot-shaped answer to it.
