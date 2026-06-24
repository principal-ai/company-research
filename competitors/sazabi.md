---
type: competitor
title: Sazabi
description: YC AI-native observability platform ("Datadog for the AI era") — logs-only ingestion (stdout/stderr) with a chat/agent interface that investigates incidents, instruments code, and opens PRs.
volatility: fast
as_of: 2026-06
resource: https://www.ycombinator.com/companies/sazabi
sources:
  - "Launch YC: Sazabi — Datadog for the AI Era: https://www.ycombinator.com/launches/QdT-sazabi-datadog-for-the-ai-era"
  - "YC company page: https://www.ycombinator.com/companies/sazabi"
  - "Founder — Sherwood Callaway (LinkedIn): https://www.linkedin.com/in/sherwoodcallaway/"
note: >
  Facts only — comparison to Principal lives in trails. Early-stage (closed alpha,
  YC Spring 2026); traction figures are company-reported and the "logs are all you
  need" scope claims are the company's. Most likely to go stale: alpha/GA status
  and the traction numbers.
---

# Sazabi

**Sazabi** is an AI-native observability platform positioned as **"Datadog for the
AI era"** — "what Datadog would look like if it were built in 2026 instead of
2010." Founded by **Sherwood Callaway** (two-time YC founder who started the
infrastructure/observability teams at Brex), with a nine-person team including
three Brex alumni and two former observability founders. YC **Spring 2026** batch;
**closed alpha** as of June 2026.

## Overview

- **Vendor:** Sazabi.
- **Category:** AI-native observability / monitoring.
- **Status:** closed alpha (June 2026).

## "Logs Are All You Need"

Sazabi's foundational claim is that it does **not require metrics or traces** —
users send only **logs (stdout and stderr)**. From log data alone, the company says
it can answer complex queries, perform aggregations, profile endpoints, and trace
requests through an entire system. The approach is to ingest everything and let an
agent make sense of it.

## AI-era features

- **Chat-based UX** instead of dashboards; **Slack** as a primary entry point.
- **Agent-driven instrumentation** — "zero code or config changes."
- **Autonomous alerts** that carry full context and "never misfire."
- **CLI for coding agents** — gives coding agents visibility into observability data.
- An **AI agent** that "memorizes your codebase, architecture, traffic patterns, and
  past incidents," runs background investigations, and opens PRs.

## Traction (company-reported)

In one month of closed alpha: **35 teams** onboarded, **8,000 background
investigations**, **2,000 issues** detected, **2 TB** of logs ingested, **200 PRs**
opened.

## Competitive surface

The Sazabi capabilities inside Principal's domain — understanding, runtime context:

- **An agent reasoning over runtime telemetry to investigate incidents** overlaps
  Principal's runtime / OTEL direction (investigations over trail-bound telemetry).
- **The ingest-everything model ("logs are all you need")** is the opposite of
  binding telemetry to curated intent; the contrast is a trail concern, not recorded
  here.

## Updates

### 2026-06-24 · Doc created
Captured from the YC launch ("Datadog for the AI Era") and YC company page: logs-only
ingestion, chat/agent UX, agent-driven instrumentation, founder Sherwood Callaway
(ex-Brex, two-time YC), nine-person team, closed-alpha traction. Sources:
https://www.ycombinator.com/launches/QdT-sazabi-datadog-for-the-ai-era ·
https://www.ycombinator.com/companies/sazabi
