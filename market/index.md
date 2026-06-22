---
type: index
title: Market
description: Market signals, trends, sizing, and external evidence — dated and sourced. What each signal means for us lives in trails.
---

# Market

Market signals, trends, sizing, and external evidence — the world Principal is
being built into. These facts are **perishable**: every doc carries a `source`
and an `as_of`, because nothing in the file makes a market claim true and it
goes stale silently when reality moves.

State the signal plainly. What it *means for Principal's value* is a **trail**
across `market/*` ↔ `product/*`, not an argument inside the doc.

This folder is **flat**: one doc per source/artifact, one finding per `##`
anchor. No theme subfolders — grouping a survey, a security report, and an
incident into "the pressure on AI codegen" is itself an argument, so that lives
in a **trail** that points at these anchors, not in the filesystem.

## Has a doc

External evidence on AI-assisted coding (each doc = one source; cite anchors):

- [`stack-overflow-survey-2025.md`](stack-overflow-survey-2025.md) — AI adoption up, trust down, time lost debugging.
- [`gitclear-code-quality-2025.md`](gitclear-code-quality-2025.md) — code cloning up ~4x, refactoring/reuse down (211M lines).
- [`veracode-genai-security-2025.md`](veracode-genai-security-2025.md) — AI code ~45% insecure-by-choice, 2.74x more vulns than human.
- [`replit-db-deletion-2025.md`](replit-db-deletion-2025.md) — AI agent deleted a production DB during a code freeze (July 2025).
- [`cursor-pricing-2025.md`](cursor-pricing-2025.md) — usage-based pricing shift, backlash, apology + refunds.
- [`github-copilot-usage-billing-2026.md`](github-copilot-usage-billing-2026.md) — all plans to token billing; backlash over credit depletion.
- [`claude-code-rate-limits-2025.md`](claude-code-rate-limits-2025.md) — weekly rate limits, developer backlash, class-action suit.
- [`claude-code-artifacts-2026.md`](claude-code-artifacts-2026.md) — Claude Code ships shareable, live pages from agent sessions (PR walkthroughs, dashboards, timelines).
- [`agentic-loops-discourse-2026.md`](agentic-loops-discourse-2026.md) — industry reframes AI coding as designing/supervising loops (inner/middle/outer); human moves author→reviewer; bottleneck moves to the outer loop.
- [`sdlc-vibe-coding-whitepaper-2026.md`](sdlc-vibe-coding-whitepaper-2026.md) — Google whitepaper: "generation is solved, verification/judgment is the new craft"; Agent = Model + Harness; vibe→agentic spectrum sorted by verification; spec quality is the new bottleneck.
- [`verification-loop-2026.md`](verification-loop-2026.md) — verification-loop *speed* is the binding constraint; PR review time +91% as merges climb; the dominant cost is reconstructing intent, not reading the diff.

## Backlog — signals to capture

- [ ] `market-size.md` — TAM/SAM for the category (sourced, dated).
- [ ] `ai-coding-adoption.md` — adoption trends in AI-assisted development.
- [ ] _(add signals, trends, and evidence as research surfaces them)_
