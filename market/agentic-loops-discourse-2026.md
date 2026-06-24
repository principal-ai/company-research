---
type: market-signal
title: "The loop" — agentic coding reframed as designing & supervising loops (2026)
description: Across independent voices (Willison, Dex Horthy/HumanLayer, IT Revolution, Anthropic), 2026 discourse reframes AI coding as designing and supervising loops — inner/middle/outer — with the human moving from author to loop-designer and reviewer, and the bottleneck moving to the outer loop.
timestamp: 2026-06-19
volatility: perishable
as_of: 2026-06-19
tags: [ai-coding, agentic, discourse, human-in-the-loop, orchestration]
sources:
  - "Entry-point reference — Dex Horthy (@dexhorthy) post (2026): https://x.com/dexhorthy/status/2067973141289414862"
  - "Simon Willison — 'Designing agentic loops' (2025-09-30): https://simonw.substack.com/p/designing-agentic-loops"
  - "IT Revolution — Leah Brown, 'The Three Developer Loops' (2025-10-20): https://itrevolution.com/articles/the-three-developer-loops-a-new-framework-for-ai-assisted-coding/"
  - "Dex Horthy — 'The Outer Loop' newsletter: https://theouterloop.substack.com/"
  - "LinearB / Dev Interrupted — Dex Horthy on RPI + the Ralph loop (2026-02-17): https://linearb.io/blog/dex-horthy-humanlayer-rpi-methodology-ralph-loop"
  - "Anthropic — 2026 Agentic Coding Trends Report: https://resources.anthropic.com/2026-agentic-coding-trends-report"
  - "DevOps.com — 'The Great Decoupling: Scaling the Outer Loop for the Agentic Era': https://devops.com/the-great-decoupling-scaling-the-outer-loop-for-the-agentic-era/"
  - "Armin Ronacher — 'The Coming Loop' (2026-06-23): https://lucumr.pocoo.org/2026/6/23/the-coming-loop/"
---

# "The loop" — agentic coding reframed as designing & supervising loops (2026)

A **discourse signal**, not a single artifact: through 2025–2026 multiple independent
voices converged on the same frame — agentic coding is no longer about *writing code*,
it's about *designing and supervising loops* (an agent running tools toward a goal,
verifying, and iterating). The vocabulary — "inner/outer loop," "loop engineering,"
"the Ralph loop," "design the loop" — recurs across practitioners, vendors, and
first-party AI labs. This doc captures that convergence and the facts behind it. One
finding per heading. The entry-point reference for this research was a Dex Horthy
(`@dexhorthy`) post; its literal text could not be retrieved (X returns HTTP 402), so
the claims below are anchored on citable sources, not the tweet.

## "The loop" is now the shared frame
Independent voices describe agentic coding in the same terms. Simon Willison: *"LLM
agents are something that runs tools in a loop to achieve a goal. The art of using
them well is to carefully design the tools and loop"* (2025-09-30). Anthropic's 2026
report frames the year as the shift from single assistants to *"coordinated agent
teams that can run autonomously for hours or days — while engineers move from writing
code to orchestrating the systems that write it."* Dex Horthy (HumanLayer) runs a
newsletter literally named **"The Outer Loop"** ("AI Agents, Human in the Loop,
maybe-agi"). The framing is not one author's coinage — it has become the default lens.

## The inner / middle / outer loop taxonomy
IT Revolution's "Three Developer Loops" (Leah Brown, 2025-10-20) names three nested
timeframes, each governed by the same prevent → detect → correct discipline:
- **Inner loop (seconds–minutes)** — moment-to-moment work with the agent; the
  traditional compile-test-debug cycle compresses into a *"request-output-verify"*
  cycle that can turn in seconds.
- **Middle loop (hours–days)** — context management *across* sessions, addressing how
  agents *"go into a closet and forget everything"* when a session ends.
- **Outer loop (weeks–months)** — strategic architecture and long-term system design;
  preserving API integrity and modular boundaries as implementations accelerate.
The article stresses that human judgment stays load-bearing across all three — knowing
when to intervene, spotting agent confusion, choosing fix-forward vs. revert.

## "Loop engineering" became a named skill
Willison's core claim is that *"a critical new skill to develop is designing agentic
loops"* — the human's job shifts from execution to system design: tool selection,
credential scoping (tightly-limited creds, budget caps), and picking problems with
clear success criteria where trial-and-error is the expected path. The "loop
engineering" label has since spread across practitioner writing (playbooks, guides),
and tooling now ships native loop primitives — e.g. Claude Code's `/goal`, a loop that
runs across turns until a written condition is true (reported v2.1.139, 2026-05-11).
Dex Horthy's **"Ralph loop"** (reset-context-and-rerun) is cited as a cheap, durable
pattern (~$10–11/hr of Sonnet across servers for a multi-hour run).

## Structured loops keep a human curating reasoning before code
Horthy's **RPI (Research → Plan → Implement)** methodology — later rebuilt as
**QRSPI** — forces agents to generate *intermediate design artifacts* (100–200-line
markdown "design discussions") that a human reviews *before* a line of code is planned.
His stated principle: *"you cannot outsource the thinking,"* the human stays *"in the
driver's seat"* for architecture while agents handle execution and tests. He also
reports a **"Dumb Zone"** — model recall degrades in the middle ~40–60% of a large
context window — drawn from analysis of ~100,000 developer sessions, arguing for small
tasks and *frequent context resets/compaction* over complex multi-agent orchestration.

## The human role moves from author to supervisor/orchestrator
Anthropic's 2026 report quantifies the gap: developers use AI in *roughly 60%* of their
work but report being able to *"fully delegate" only 0–20%* of tasks — AI is a constant
collaborator, but effective use still needs setup, prompting, *active supervision,
validation, and human judgment*, especially for high-stakes work. Anthropic's framing:
*"the goal isn't to remove humans from the loop — it's to make human expertise count
where it matters most."* Across sources the recurring claim is the same: when the unit
of work becomes an *outcome* rather than a *suggestion*, the human moves from author to
reviewer/orchestrator.

## The bottleneck moved to the outer loop
A "velocity paradox" / "great decoupling" recurs: the inner loop now runs at the speed
of thought, but the outer loop — PR review, security scans, compliance, architectural
sign-off — is still *pre-agentic* and human-paced, so it becomes the binding constraint
(DevOps.com). AI can emit thousands of lines in seconds; the governance to ship them
safely still takes days. The discourse's practical conclusion: leverage now lives in
the *outer* loop — review, context, and orchestration — not in faster code generation.

## A skeptical voice: looping is fine for throwaway work, dangerous for *lasting* code
Armin Ronacher's **"The Coming Loop"** (2026-06-23) accepts the same two-loop frame —
*"There is already an agent loop inside every coding agent… The other loop is the
harness level loop: the loop outside the agent loop"* — but lands on a warning, not a
celebration. He's comfortable letting loops run on transformation-shaped, impermanent
work (porting, performance exploration, security scanning, research) where trial-and-
error is the point and nothing has to last. What *"does not yet sit well"* with him is
using the same looping method to write **lasting code**, because today's models produce
defensive, badly-invarianted code — Karpathy's line that they are *"mortally terrified
of exceptions"* — patching bad states locally instead of making them impossible. His
metaphor is the sharpest practitioner statement yet of comprehension debt: *"moving from
software as a deterministic machine to software as an organism… We treat it, we monitor
it, we stabilize it, but we do not necessarily comprehend it."* And the part he calls
most uncomfortable: *"opting out of this fully machine-driven future may not be an
option"* — competitive speed and security pressure force participation even for the
reluctant, so the live question becomes not *whether* we loop but how we avoid
abdicating judgment.

## Why it's a signal
The whole industry — practitioners, a $-billion vendor category, and the first-party
labs — is independently relocating the hard problem of AI coding *off* writing code and
*onto* the loop around it: designing it, supervising it, keeping a human curating
reasoning before implementation, and carrying context across sessions (the "middle
loop"). That surface — human-in-the-loop curation, durable context that survives a
session reset, and review/orchestration of agent work — is exactly the domain Principal
is built into.

*Where Principal stands:* we track this discourse
closely and see **code trails as a compatible primitive** for the loop it describes —
human-curated, code-grounded intent is what a supervised loop needs to stay honest. But
we **do not subscribe to the over-automation** the loudest version of this conversation
implies. Human oversight in code development is **more valuable than the space is
currently crediting it** — pushing humans further out of the loop in the name of
autonomy risks **comprehension debt**: code that ships faster than anyone understands
it — what Ronacher calls software becoming an *organism* we monitor but no longer
comprehend (see finding above). That debt is already measurable, not hypothetical — falling trust and time lost to
debugging ([`stack-overflow-survey-2025.md`](stack-overflow-survey-2025.md)), declining
reuse and rising duplication ([`gitclear-code-quality-2025.md`](gitclear-code-quality-2025.md))
— and it cashes out as **serious incidents** ([`replit-db-deletion-2025.md`](replit-db-deletion-2025.md))
at a time when **software security is an increasing concern**
([`veracode-genai-security-2025.md`](veracode-genai-security-2025.md)). Our bet is that
the durable winner of the "loop" era is not maximal autonomy but the *best human-in-the-loop*:
the outer/middle loop, made fast and trustworthy, beats a faster inner loop that no one
can vouch for.

How Principal's primitives map onto specific inner/middle/outer-loop needs — the full
product argument — is a **trail** across `market/*` ↔ `product/*`, developed there
rather than here. See also
[`claude-code-artifacts-2026.md`](claude-code-artifacts-2026.md) (first-party agent
output becoming a review surface) and the HumanLayer competitor doc
([`../competitors/humanlayer.md`](../competitors/humanlayer.md)) — the same Dex
Horthy / "outer loop" work, captured as a competitor's product.
