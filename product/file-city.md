---
type: product
title: File City — the visualization layer
description: File City is Principal's spatial layout of the repository where each file is a building; the 2D map is the primary, most-useful view, it renders trail markers, conveys comprehension coverage, and visualizes repo activity live and historic for collaboration.
volatility: slow
as_of: 2026-06
tags: [product, code-trails, visualization, file-city]
---

# File City — the visualization layer

**File City** is Principal's spatial view of a repository: the codebase is laid
out as a city and each file is a **building**. The primary, most-useful form is
the **2D map** of that layout; a 3D scene exists but is more of a novelty than
the working view. It is the panel that renders code trails and, more broadly,
the surface on which repo state is made visible. The trail primitive lives in
[`code-trails.md`](code-trails.md); this doc describes the visualization layer
itself. The *why it matters* arguments live in trails, not here.

## Buildings are files

The repository's structure is mapped to a city: files are buildings, and their
arrangement reflects the codebase's layout. This gives the repo a stable spatial
shape a person can hold in mind and return to, rather than a flat file tree. The
**2D layout** is the view that does the work; the 3D rendering is a novelty on
top of the same map.

## It renders trails

File City is the renderer for code trails. A trail separates content (markers)
from layout (views); File City takes those markers and draws them on the map.
Clicking a marker **highlights its building** and opens the matching
**source slice** in a drawer. The same markers can drive different views (e.g.
the v1 sequence view); see [`code-trails.md`](code-trails.md).

## It conveys comprehension coverage

Beyond a single trail, File City is used to show **comprehension coverage** —
which parts of the repository are understood, documented, and trail-covered
versus which are not. Reading the city tells you where intent has been captured
and where the blank spots are — a maintained mental model of the repo, at the
scale of the whole codebase rather than one file at a time.

## It visualizes activity — live and historic

File City visualizes **activity across the repo**, both **live** (what is being
worked on or changed now) and **historic** (how activity has moved through the
codebase over time). Mapping activity onto the spatial layout makes patterns of
work legible at a glance.

## For collaboration

The coverage and activity views serve **collaboration**: a team shares one
spatial picture of what is understood and where work is happening, so aligning
on, reviewing, and signing off on what agents are doing to the codebase happens
against a common view rather than scattered terminal output. How this compares
to other ways of presenting agent output is a **trail** concern, not this doc's.

## Demonstrated publicly

File City is shown on real codebases via **File City tours** — short public
walkthroughs published on Principal's tour page. See
[`../company/file-city-tours.md`](../company/file-city-tours.md).
