---
type: product
title: Code trails — the primitive
description: A code trail is an ordered set of markers pinned to file+line with reasoning; human-curated, code-grounded, and persisted as a machine-readable artifact.
volatility: slow
as_of: 2026-06
tags: [product, code-trails, primitive]
---

# Code trails — the primitive

A **code trail** is the core artifact: an ordered set of **markers** plus one or
more **views** over them. Markers carry the content (what the code does and why);
views carry the structure (how the steps are laid out and connected). The
product-level framing is in [`overview.md`](overview.md); this doc describes the
primitive and its design properties. The arguments for *why* these properties are
valuable live in trails, not here.

## Markers pin reasoning to source

Each marker has a `sourcePath` and a line range (`file:line`), a description that
carries the reasoning, and an optional source snippet. A marker is one unit of
intent — a decision, a branch, a handler, an invariant — anchored to the exact
place in the code it describes.

## Human-curated

An agent produces the first draft — so capture is cheap and scalable, not gated on
a human authoring documentation by hand — and an expert then shapes the draft and
vouches for it: which markers matter, whether the reasoning is right, what to cut.
The curation step is where a trail becomes trusted rather than merely generated.

## Code-grounded

Every marker is pinned to `file:line`, so the intent is verifiable against real
source rather than asserted in prose. When the code moves, the pin lets staleness
surface instead of silently rotting.

## A trail is pre-computed, curated context

Because a trail is an ordered, expert-curated walk of the relevant code with the
reasoning attached, it can be consumed directly as context — an agent or a person
reads the path instead of re-deriving the flow from raw source.

## A trail is a persisted, machine-readable reasoning artifact

A finished trail persists as a structured, machine-readable record that binds
reasoning to specific code — markers, views, and descriptions in a defined schema.
The artifact is the unit that is stored, shared, versioned, and re-rendered.

## Living documentation

Because the *why* is pinned to code rather than living in separate prose that
drifts, it persists past merge and surfaces staleness when the code changes —
documentation that stays attached to the thing it documents.

## Views and rendering

A trail separates content (markers) from layout (views) so the same markers can
drive different renderers. v1 ships a **sequence** view — lanes by participant or
subsystem, ordered edges between markers — rendered in the **File City** panel
described in [`file-city.md`](file-city.md).
