---
type: reference
title: Company thesis — working brief
description: The value thesis for Principal AI / Code Trails — utility primary (efficiency, quality, alignment, incl. OTEL instrumentation + investigation), the compounding data asset as act two — and how it maps onto this bundle's docs + trails.
timestamp: 2026-06-17
volatility: perishable
as_of: 2026-06-17
tags: [thesis, positioning, working-brief, trails]
---

# Company thesis — working brief

> **Status: working brief, not a fact doc.** This captures an in-progress,
> deliberately *opinionated* argument and the plan for splitting it into pointable
> facts + trails. It takes a side, which is why it lives at the root and **not**
> inside `product/`, `market/`, or `competitors/`, where docs stay neutral. The
> `market/` and `competitors/` docs it points at now exist; `product/` docs don't yet.

## 1. The thesis (primary): human-curated, code-grounded intent

**The shift.** As AI agents write more of the code, the bottleneck moves off
*writing* and onto everything around it — and three things are breaking at once:

- **Cost** — the industry moved to per-token pricing and it's contentious
  ([`market/github-copilot-usage-billing-2026.md`](market/github-copilot-usage-billing-2026.md),
  [`cursor-pricing-2025.md`](market/cursor-pricing-2025.md),
  [`claude-code-rate-limits-2025.md`](market/claude-code-rate-limits-2025.md)).
- **Comprehension** — adoption is rising while trust falls and quality erodes
  ([`stack-overflow-survey-2025.md`](market/stack-overflow-survey-2025.md),
  [`gitclear-code-quality-2025.md`](market/gitclear-code-quality-2025.md)).
- **Safety** — unreviewed generation causes real incidents
  ([`replit-db-deletion-2025.md`](market/replit-db-deletion-2025.md),
  [`veracode-genai-security-2025.md`](market/veracode-genai-security-2025.md)).

**The product.** A **code trail** is **human-curated, code-grounded intent** — an
ordered walk of markers, each pinned to file + line, with the reasoning attached.
An agent drafts it cheaply (the commodity step, not gated on human authoring); the
two load-bearing properties are:

- **human-curated** — an expert shapes and vouches for it: which markers matter,
  whether the reasoning is right. This is where *trust* is created.
- **code-grounded** — every marker is pinned to file:line, so the intent is
  *verifiable* against real source and staleness surfaces when the code moves.

The result is a codebase's intent made **legible** (read the *why*, not just the
*what*) and **pointable** (each step checks against ground truth).

**Workflow:** *agents draft it, humans curate it, the code keeps it honest* —
agent = scale, human = judgment & trust, code = currency. (The same
draft→curate division is the RLHF pattern, which is why it reinforces act two.)

**The value — one root, three payoffs.** Everything follows from *intent made
legible and pointable*:

- **Agent efficiency** — a trail is pre-computed, expert-curated context, so an
  agent skips blind exploration: fewer tokens, fewer wrong turns. (Directly
  answers the **cost** pressure.)
- **Software quality** — the "why" stops evaporating at merge; living
  documentation pinned to code, better review and onboarding. (Answers
  **comprehension**.)
- **Intent alignment** — agents act on what you *meant*, not just what you typed;
  the codebase carries its intent forward. (Answers **safety**.)

**One-liner:** *As agents write the code, the scarce thing isn't writing it —
it's intent you can trust: human-curated so it's right, code-grounded so it stays
honest.*

## 2. The OTEL extension — grounding reaches into runtime

The same trail extends past source into *runtime*: bind a trail's markers to the
OpenTelemetry spans/events emitted along that flow, and the trail carries three
layers on one spine — intent (*why*), code (*where*), and telemetry (*what
actually happened*). Two moves fall out:

- **Trails guide instrumentation.** The hard part of OTEL isn't the API, it's
  deciding *what's worth a span*. A trail's markers already are the meaningful
  steps, so they map directly to instrumentation points — an agent proposes the
  spans from the trail, a human curates which ones matter.
- **Investigations ride the trail, not raw code.** With telemetry bound to
  markers, debugging becomes "walk the trail, read the live data at each step,
  localize the anomaly" — skipping the expensive reconstruct-the-flow-from-raw-
  source step that agents otherwise burn tokens re-deriving every time. This is
  the **efficiency** payoff extended from *writing* code into *operating* it, and
  it also hits the **safety** pressure (fast, grounded incident response).

These close into a loop: curate an informative trail → instrument from its
markers → telemetry flows back, bound to the trail → lay an *investigation trail*
that rides it → promote the investigation back into an informative trail. Each
pass sharpens the map — and produces act-two data that's reasoning bound to
*observed behavior*, not just to source.

**Grounding now spans both layers — and each has an enforcement mechanism:**

| Layer | Captures | Grounded by |
| --- | --- | --- |
| Code | *where* (markers) | file:line pins (staleness shows on change) |
| Intent | *why* (reasoning) | human curation (an expert vouches) |
| Telemetry | *what happened* (runtime) | **OTEL contract validation** |

The contract-validation layer is what keeps the telemetry binding from rotting:
it enforces that emitted spans/events conform to a curated contract, so the
runtime layer becomes as *verifiable* as the source layer. It generalizes
"code-grounded" to **grounded at every layer**, and slots into the same shape as
the core concept — agents **draft** instrumentation → humans **curate** the
contract → validation **enforces** it → telemetry conforms → investigations ride
it. (It also underpins dashboards: aggregating metrics over spans/events only
works if they conform to a contract.)

*Open detail to settle when we write this up:* whether validation runs at
**build/CI** ("telemetry contracts tested like code") or at **runtime/collector**
("non-conforming telemetry rejected/flagged live"), or both — it changes how the
capability is described.

## 3. The frontier is moving onto our turf

New competitive signal, and it cuts both ways — validation *and* threat:

- Cursor (Anysphere) bought **Graphite** and is building **Origin**, with its CEO
  framing **code review as the emerging bottleneck** as AI scales
  ([`competitors/cursor/`](competitors/cursor/index.md)). That's our thesis, said
  by a $29B competitor.
- **GitHub** is straining under agent-generated load (outages, traffic re-routed
  to AWS) ([`competitors/github.md`](competitors/github.md)) — evidence the old
  human-paced collaboration layer doesn't fit an agent-written world.

The frontier (editor → review → hosting) is converging on understanding, review,
and intent — i.e. Principal's domain. Whether that's a moat or a race is a
**trail** argument, not a fact here.

## 4. Act two: the compounding data asset (the refinery)

Underneath the utility sits an asset. Because authoring a trail is *already useful
work*, the **expert reasoning over code** it captures falls out as **exhaust** —
a machine-readable reasoning chain / trajectory, the highest-grade fuel for
training coding agents (process supervision, not just input→output). The
reCAPTCHA / Duolingo / Waze / Stack Overflow pattern: valuable labels as a
byproduct of a task with its own payoff.

**Utility is the load-bearing precondition:** no usage → no exhaust → no asset.
So act two depends on act one being real — which is *why* we lead with utility.

**Open question — who buys the refined oil?** Deliberately unresolved; we may
pick more than one:

1. **Moat / train our own** — the trail corpus is proprietary training data. *(Most ambitious, least concrete comps.)*
2. **Powers the product itself** — trails make our answers better for the team that authored them. *(Most product-legible today.)*
3. **Sell the corpus** — the labeled dataset is the asset, sold to labs. *(Most direct proof a market exists.)*

## 5. How it maps to the bundle

Facts stay neutral in docs; the argument above is the **trail**.

```
product/      TO WRITE — the spine head:
  overview.md       What Principal AI / Code Trails is.
  code-trails.md    A trail = ordered markers pinned to file+line + reasoning.
  trail-artifact.md A finished trail is a persisted, machine-readable reasoning
                      chain over code. (Neutral fact — pivot of both acts.)
  otel-trails.md    Trails bind to OTEL; markers→instrumentation; investigations
                      ride the trail (the runtime extension).
  otel-contracts.md Contract validation enforces that telemetry conforms — the
                      runtime grounding leg.

market/       DONE — flat, one doc per source, point-per-anchor. The three
              pressures (cost / comprehension / safety) are a TRAIL grouping over
              these, not folders.

competitors/  DONE for the frontier — cursor/ (folder: editor, graphite, origin)
              + github.md. BACKLOG — swimm, sourcegraph, glean (the "powers the
              product" neighbors), and scale/mercor/surge for act-two story 3.
```

Deliberately absent: no `data-is-oil-thesis.md`, no `monetization.md` — arguments
live in trails, where the same facts carry a cautious internal version and a
bullish investor version without the docs taking a side.

## 6. The trails

**Primary — "Why Code Trails matters" (utility spine):**
1. The pressure → `market/` cost + comprehension + safety anchors
2. The product → `product/code-trails.md`, `product/trail-artifact.md` (intent legible & pointable)
3. The payoffs → efficiency / quality / alignment, each tied back to its pressure
4. The runtime extension → `product/otel-trails.md`, `product/otel-contracts.md` (efficiency reaches into investigation; grounding reaches into telemetry)
5. The frontier confirms it → `competitors/cursor/`, `competitors/github.md`

**Act two — "The compounding data asset" (downstream branch):**
- `product/trail-artifact.md` → reasoning-as-exhaust → the three buyer stories.
  Reuses the spine head; only branches at monetization.

## 7. Comparables, parked for reference

- **Pattern (labels as exhaust):** reCAPTCHA, Duolingo, Waze, Tesla, Stack Overflow.
- **Story 1 (flywheel/moat):** Tesla, Cursor/Anysphere, Midjourney, Google Search.
- **Story 2 (self-serving):** Swimm *(closest product-shape)*, Sourcegraph/Cody, Glean, Stack Overflow for Teams, Guru, Unblocked, Pieces.
- **Story 3 (sell labeled data):** Scale AI, Surge AI, Mercor, Turing, Labelbox, Sama/Appen; Reddit & Stack Overflow data-licensing deals as proof of a buyer.
