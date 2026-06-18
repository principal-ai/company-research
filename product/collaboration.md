---
type: product
title: Collaboration on code trails — sharing, feedback, review
description: How trails are shared, commented on, bundled, and reviewed — the collaboration surface around the code-trail primitive.
volatility: slow
as_of: 2026-06
tags: [product, code-trails, collaboration, sharing, review]
---

# Collaboration on code trails

A code trail is built to be **shared and reviewed**, not just authored. The
primitive ([`code-trails.md`](code-trails.md)) and the product framing
([`overview.md`](overview.md)) cover what a trail is; this doc covers the surface
that lets people share trails, leave feedback on them, and review with them. The
*why this raises productivity* argument lives in trails, not in this doc.

## Sharing and publishing

A trail (and a topic) is **local-only until a person publishes it**. Publishing
sends it to **web-ade**, a web viewer where the trail becomes a shareable link a
teammate or reviewer can open without the desktop app. Publishing is a deliberate
human action taken from the app UI — authoring and sharing are separate steps, so
work in progress stays local until someone decides to share it.

## Anchored feedback

Readers leave **notes and comments anchored to a specific place** — a trail
marker, or a span of text inside a markdown doc (via a W3C text-quote anchor of
the exact text). Anchored feedback surfaces as **inline highlights** the next time
the document or trail is opened. Because a comment lands on the exact marker or
line it concerns, feedback is tied to ground truth rather than floating in a
separate thread.

## Topics as shared briefs

A **topic** is a curated bundle of trails on one subject, with a markdown
description that **doubles as a working brief**. The same bundle a person reads to
get oriented is the brief an agent is pointed at — so a topic is both a shared
reading list and a handoff artifact for collaborators, human or agent.

## Review flows

Trails carry review use cases directly:

- **PR / diff walkthroughs** — a trail can walk a reviewer through a change set, marker by marker, instead of a flat diff.
- **Plan annotation and review** — plans and designs can be annotated and reviewed with the same anchored-feedback model before work proceeds.

## Curation is a shared act

The core workflow is a division of labor: an agent **drafts**, one or more humans
**curate and vouch**. Curation — deciding which markers matter and whether the
reasoning is right — is where review and sign-off happen, so collaboration is part
of how a trail is produced, not a step bolted on after.
