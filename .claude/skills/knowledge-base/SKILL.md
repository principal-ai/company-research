---
name: knowledge-base
description: Guidance for writing and organizing markdown documents in this knowledge-base repo so they stay dependable and work well as a substrate for trails. Use when adding, editing, splitting, or reorganizing docs here — e.g. "add a doc about CompetitorX", "write up our pricing", "where should this fact live", "clean up the market folder", or whenever authoring KB markdown. These are soft conventions, not enforced rules — lean toward them, don't block on them.
---

# Knowledge Base conventions

This repo is a markdown knowledge base: one repo, many folders, each folder a
subject area (e.g. `product/`, `competitors/`, `market/`). The docs here are
the raw material that **trails** thread together to answer real questions — an
investor-question trail walks markers across `product/` and `competitors/` and
the *answer is the path*.

So these docs get read two ways: directly by a person, and indirectly by an
agent assembling a trail. Both readers are better served when a fact is easy to
locate, easy to trust, and easy to point at.

These are **conventions, not gates.** Nothing is linted or enforced yet — we'll
tighten what proves useful as we learn through usage. Lean toward them; never
block work on them.

## The one idea everything follows from

Code is self-verifying: a trail points at `auth.ts:42` and the line is either
there and says what's claimed, or it isn't. A KB fact ("CompetitorX raised
$50M", "our ARR is $4M") is a claim about the *world* — nothing in the file
makes it true, and it goes stale silently when reality moves and the file
doesn't.

So the things worth caring about most here are the things the medium *won't*
catch for you: **where a fact lives, where it came from, and how fresh it is.**
Everything below is a lean in that direction.

## Lean toward these

### One concern per document
Keep a doc about one thing — one investor, one competitor, one feature. A doc
that sprawls across an investor *and* your funnel *and* a pricing aside is hard
to point a trail marker at and hard to keep current. When a doc starts wanting
"and also…", that's the signal to split.

### Give facts a stable handle
Prose reflows — adding a paragraph shifts every line below it, so line numbers
are a bad anchor. Lean on **headings** as the addressable unit: clear,
descriptive `##` sections that a link or a trail marker can target by slug.
Stable section titles are worth more than perfect prose here.

### One home per fact
The classic wiki rot is the same number in three docs, drifting into three
different numbers. Give each fact **one canonical home** and link to it from
everywhere else, rather than restating it. "Our ARR" lives in one place;
`competitors/` and `market/` docs link to that place. If you catch yourself
copying a value, link instead.

### Make links resolve
Cross-references (`[[wikilinks]]` or relative paths) are the graph trails ride
on. A link that points nowhere is worse than no link. When you move or rename a
doc, fix what pointed at it.

### Say where a fact came from, and when
This is the big one, because the file can't vouch for itself. When a claim could
be wrong or could go stale, note its **source** and an **as-of date** — inline
is fine ("ARR $4M *(per Q2 board deck, 2026-05)*"), frontmatter is fine, a
footnote is fine. A trail that can show its sources is the difference between a
pitch that holds up and one that doesn't.

### Know what rots
Some facts are evergreen (your founding story), some are slow (product
architecture), some are perishable (competitor pricing, market size, your own
metrics). It helps to mark the perishable ones — even a date is enough — so a
reader (human or agent) knows to re-check before leaning on them. Don't bother
dating things that don't move.

### Keep facts and spin separable
State the fact plainly; keep positioning and narrative distinguishable from it
(a separate section, a callout, frontmatter — whatever's natural). The same
fact base then feeds the bullish investor trail *and* the honest internal one,
and a trail can pull the fact without dragging the framing along.

### Let the folders be the taxonomy
Folders are the top-level subjects. Put a doc where a reader would look for it
first. When a doc genuinely belongs to two subjects, pick one home and link from
the other (same single-home instinct as facts). A short `README.md` per folder
saying what belongs there keeps the taxonomy legible as it grows.

### Categorize by domain, never by argument
A folder should answer *"what is this a fact about?"* (its neutral subject or
source) — never *"what point does this support?"* A `market/funding/` folder is
fine; a `market/why-we-win/` folder is not, because the grouping itself is a
claim, and claims belong in **trails**, not the filesystem. Same test as keeping
facts and spin separable: if naming a folder requires taking a side, that
structure is a trail wearing a folder costume. Stay flat and let trails impose
the thematic grouping on demand.

### Source-heavy folders: one doc per source, one point per anchor
Some folders (notably `market/`) are mostly **external evidence** — surveys,
reports, incidents. There, the natural unit is **one doc per source/artifact**
(`market/stack-overflow-survey-2025.md`), not one doc per claim. A single source
usually makes several points; give each point its own stable `##` heading so a
trail marker can land on exactly one finding
(`…survey-2025.md#trust-declining`) without the others coming along. The doc is
the source's one canonical home; the **anchors** are the pointable facts. This is
what lets these folders stay flat — anchors give you finer structure than folders
would, so you don't need theme subfolders to organize evidence. Keep each heading
a neutral fact ("46% distrust AI output accuracy"), not a framed argument; the
framing is the trail's job. Put the `as_of` and `sources:` at the doc level (the
artifact's date), and any specific figure gets an inline cite next to its claim.
A source whose points span several themes just lives at the folder root,
uncategorized — trails reach its anchors from anywhere regardless of where the
file sits.

## A light frontmatter starting point (optional)

Not required, not validated — a convenient hook for the source/freshness habit
above. Use it where it helps, skip it where it doesn't:

```markdown
---
title: CompetitorX
volatility: perishable   # evergreen | slow | perishable
as_of: 2026-05-01
sources:
  - Q2 board deck
  - https://competitorx.com/pricing
---
```

We'll learn which fields actually earn their keep and standardize those later,
rather than imposing a schema up front.

## How this pays off in trails

When the docs above hold, an informative trail answering "What's our moat?"
becomes a clean path — one marker per stop, each pointing at a single-home,
sourced, dated fact:

- → `product/architecture.md#data-network-effect`
- → `competitors/competitor-x.md#gaps`
- → `product/roadmap.md#defensibility`

The trail's narration supplies the pitch; each marker traces back to a fact you
can stand behind. That's the whole reason to keep the docs tidy — the cleaner
the KB, the better the trails it can carry.

## Don't

- Don't enforce these as a checklist or block a doc from landing over them.
- Don't add frontmatter fields or structure a doc doesn't need yet.
- Don't restate a fact you could link to.
- Don't invent a source or a date — if you don't know it, say you don't.
