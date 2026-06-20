---
type: product
title: Principal AI / Code Trails — overview
description: What Principal AI is and what a code trail is — the product that makes a codebase's intent clear and grounded.
volatility: slow
as_of: 2026-06
tags: [product, code-trails, overview]
---

# Principal AI / Code Trails

Principal AI builds **Code Trails**: a way to capture, render, and navigate a
codebase's *intent* — the reasoning behind the code — as an artifact pinned to the
code itself. This doc states what the product is; the primitive's detail lives in
[`code-trails.md`](code-trails.md), and the *why it matters* arguments live in
trails, not here.

## What a code trail is

A **code trail** is an ordered walk of **markers**, each pinned to a file and line
range, with the reasoning attached. Read end to end, a trail is a path through the
code that explains a flow, a decision, or an invariant — the answer to a question
*is* the path. The full primitive (markers, views, snippets) is described in
[`code-trails.md`](code-trails.md).

## Two properties

A code trail is **human-curated** and **code-grounded**. An agent drafts it and an
expert shapes and vouches for it; every marker is pinned to `file:line` so it stays
verifiable against source. Each property is detailed in
[`code-trails.md`](code-trails.md).

## What it produces

The output is a codebase's intent made **clear** (read the *why*, not just the
*what*) and **grounded** (each step checks against real source). The
intent is captured as a durable artifact rather than living in prose that drifts.
Each trail is a **mental-model primitive** — a targeted unit of understanding
that, through topics and File City comprehension coverage, aggregates with others
into a maintained, shared mental model of the repo.

## How trails are authored and viewed

- **Authored** — an agent drafts a trail; a human curates it. Trails are posted to a local Principal bridge that persists and broadcasts them.
- **Rendered** — in the **File City** panel, a spatial map of the repository (files as buildings) where each marker highlights its building and opens the matching source slice. See [`file-city.md`](file-city.md).
- **Two flavors** — **investigation** trails (exploratory, laid while figuring something out) and **informative** trails (durable, canonical, shareable).
- **Topics** — curated bundles of related trails on one subject.

## Runtime extension (OTEL)

A trail's markers can bind to OpenTelemetry spans/events, carrying intent (*why*),
code (*where*), and runtime telemetry (*what happened*) on one spine. See
[`otel-trails.md`](otel-trails.md) (not yet written).

## Substrate (OKF / knowledge bases)

Trails ride on **pointable facts** — markdown knowledge organized so each fact has
a stable, addressable anchor. The substrate discipline is described in
[`okf-substrate.md`](okf-substrate.md) (not yet written) and this bundle's
[`OKF.md`](../OKF.md).
