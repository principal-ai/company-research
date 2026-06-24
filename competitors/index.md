---
type: index
title: Competitors
description: One neutral doc per competitor — facts only. Backlog of who to cover; comparison to Principal lives in trails.
---

# Competitors

One **neutral, isolated** doc per competitor — facts about the competitor only.
The Principal-vs-them comparison is a **trail**, never baked into a doc. Author
with the `author-competitor-doc` skill (web-verify, dated `## Updates` log).

A dangling link below = a competitor we *intend* to cover but haven't yet
(OKF "not-yet-written knowledge"). Writing the doc resolves the link.

A competitor with **2+ substantial products** gets a **folder**
(`<slug>/index.md` = the company + product list, one doc per product); a
single-product competitor stays a **flat doc**. See `author-competitor-doc`.

## Has a doc

- [Cursor / Anysphere](cursor/index.md) — *folder*: [editor](cursor/editor.md), [Canvas](cursor/canvas.md), [Graphite](cursor/graphite.md), [Origin](cursor/origin.md).
- [GitHub (Microsoft)](github.md) — the incumbent code platform + Copilot.
- [Entire (Entire Inc.)](entire.md) — ex-GitHub CEO Thomas Dohmke's "platform for humans and agents"; **Checkpoints** binds each commit to the agent session that produced it, stored in git history.
- [GitLab](gitlab.md) — AI-native DevSecOps platform; **Orbit** lifecycle context graph + Duo Agent Platform + agent-scale Git backend.
- [CodeLayer / HumanLayer](humanlayer.md) — agent-orchestration "AI IDE" on Claude Code; structured human-in-the-loop workflows.
- [Linear](linear/index.md) — *folder*: work-tracking surface extending into [Agent](linear/agent.md) + [Diffs](linear/diffs.md); ticket → agent → code → review.
- [Windsurf / Codemaps (Cognition)](windsurf.md) — AI-annotated codebase maps; the closest **File City** analog.
- [Google Code Wiki](google-code-wiki.md) — Gemini-powered living repo documentation + Q&A (public preview).
- [Greptile](greptile.md) — full-codebase AI reviewer on a semantic graph; also a codebase Q&A "expert".
- [OpenAI Codex (Sites)](codex.md) — agent deploys hosted interactive apps at a workspace URL (preview).
- [Plannotator (backnotprop)](plannotator.md) — local, OSS human-in-the-loop **plan + code-diff annotation** layer for AI coding agents; feedback routes back to the agent.
- [Sazabi](sazabi.md) — YC AI-native observability ("Datadog for the AI era"); **logs-only** ingestion ("logs are all you need") with an agent that investigates incidents and opens PRs.

## Competitor candidates — to write

- [ ] [Sourcegraph](sourcegraph.md) — Cody + Code Search (likely a folder).
- [ ] [Swimm](swimm.md) — code documentation pinned to code.
- [ ] [Glean](glean.md) — enterprise "work AI".
- [ ] _(add named tools/companies as they surface in research)_

## Theme: the GitHub-replacement threat

A set of players building **AI-native code platforms** aiming to displace GitHub.
This is a competitive **lens, not a folder** — capture each company as its own
neutral doc; the "who threatens the incumbent, and where Principal fits" argument
is a **trail** that walks them. Players to track:

- **[Cursor / Origin](cursor/origin.md)** — agent-native Git forge (announced).
- **[Entire](entire.md)** — ex-GitHub CEO Thomas Dohmke's "platform for humans and agents"; captures the agent session behind each commit (have doc).
- **Pierre Computer** — AI-native code platform (Jacob Thornton); claims massive repo-creation throughput. *(no doc yet)*
- **Stagewise** — open-source agentic IDE / agent orchestration. *(no doc yet)*
- **Cloudflare (?)** — flagged by us as a possible adjacent player; **unverified** which offering is meant (Pages/Workers/R2 are edge hosting, not a Git forge). Clarify the specific product before writing. *(no doc yet)*
- **[GitHub](github.md)** — the incumbent being measured against.
- **[GitLab](gitlab.md)** — incumbent's AI-native rival; Next-Gen SCM reframes the repo as queryable project intelligence rather than a clone.

### Sub-lens: social / open-source collaboration, reinvented for agents

A distinct fight *within* the GitHub-replacement theme — not "rebuild the forge"
but **rebuild the social and open-source-collaboration layer** (profiles, sharing,
community, the "why" behind code) for a world where humans and agents work the same
codebase. This space is **actively contested and freshly funded** as of 2026, and
GitHub's own former CEO is on both sides of it. Capturing that it exists; the
players, as facts:

- **[Cursor](cursor/index.md)** — moving into the social layer directly: **public
  profiles + claimable handles** (lifetime token stats, activity heatmaps, agent
  runtimes; launched Jun 4, 2026), layered on top of its **Origin** forge play
  (have doc).
- **[Entire](entire.md)** — Thomas Dohmke's "platform for humans and agents";
  binds intent/agent provenance to commits (have doc).
- **Tangled** — European, **decentralized** "next generation of social coding and
  collaboration" on Bluesky's AT Protocol; self-hostable "knots", developer-
  sovereignty pitch; $4.5M seed (byFounders; Bain Capital Crypto, Antler). Notable:
  **Dohmke is an angel here too**, alongside Tailscale's Avery Pennarun and Mårten
  Mickos. *(no doc yet)*
- **[GitHub](github.md)** — the incumbent whose social layer (profiles, stars, PRs,
  discussions) is the thing being reimagined for the agent era.

Principal's stake here — that a *collaboration primitive* could provide a better
social-coding interface than GitHub — is an argument, so it lives in a **trail**,
not in this index.

## Theme: code comprehension & documentation surfaces

The vertical **Principal's File City + trails sit in**: turning a codebase (or an
agent's work on it) into navigable, annotated, shareable visual/doc artifacts
instead of walls of text. A competitive **lens, not a folder** — track each player
as its own neutral doc; the Principal comparison is a **trail**. Three sub-shapes:

**(a) Agent-output artifacts** — a session's *output* rendered as a shareable
interactive page/dashboard:
- **[Cursor Canvas](cursor/canvas.md)** — agent-rendered React dashboards/diagrams (have doc).
- **Claude Code Artifacts** — shareable interactive pages from a session. *(market signal: [claude-code-artifacts-2026](../market/claude-code-artifacts-2026.md))*
- **[OpenAI Codex Sites](codex.md)** — agent deploys hosted interactive apps/dashboards at a workspace URL; preview (have doc).

**(b) Codebase maps / living docs** — the *codebase itself* turned into annotated,
navigable maps — the shape **closest to File City**:
- **[Windsurf Codemaps (Cognition)](windsurf.md)** — AI-annotated maps: code locations + trace guides; Fast/Smart generation. **Most direct File City analog** (have doc).
- **[Google Code Wiki](google-code-wiki.md)** — Gemini-powered living repo docs + diagrams + Q&A; public preview (have doc).
- **[GitLab Orbit](gitlab.md)** — lifecycle context graph mapping code + work items + pipelines + production signals into one live queryable graph; public beta (have doc).
- **Swimm** — documentation pinned to code (already a candidate above).
- **Sourcegraph** — code search / navigation (already a candidate above).

**(c) Guided code/PR walkthroughs** — *walking a human through changes* in semantic
order (overlaps Principal's trail-based PR review):
- **[Greptile](greptile.md)** — codebase-aware reviewer on a semantic code graph; also a "how does X work" codebase expert (have doc).
- **[Linear Diffs](linear/diffs.md)** — Guided Reviews group related changes into explained, semantic-order sections; shipped May 28, 2026 (have doc).
- **[Plannotator](plannotator.md)** — local OSS plan-review + PR-style diff annotation layer; human annotates the agent's plan/diff and feedback routes back to the agent (have doc).

Watch this vertical: it's where a snapshot artifact (shape a), a code-grounded map
(shape b), and a guided walkthrough (shape c) converge — and Principal's bet is
that the *code-grounded, composable, human-curated* map/trail wins. Comparison
lives in a trail.
