---
title: "autocomplete_multiplex.py: Routing keyword research across three API backends with automatic failover and credit tracking"
date: 2026-05-29T13:00:00-05:00
draft: false
tags: ["case study", "Python", "keyword research", "automation", "API", "CDCP"]
categories: ["case studies"]
description: "A Python keyword research multiplexer that routes different AI agents to different API backends — Serper, ScrapFly, and direct Google Autocomplete — with automatic failover, per-backend credit tracking, and usage logging. Built to support large-scale CDCP dental keyword research."
summary: "autocomplete_multiplex.py was built to solve a practical problem: running keyword autocomplete queries at scale across a multi-agent AI infrastructure where different agents have different API access, credit pools are finite and backend-specific, and no single backend is reliable enough to run the full workload alone. The solution is a routing layer that matches agent to backend by policy, tracks spend per backend, logs usage, and fails over automatically."
cover:
  image: ""
  alt: ""
  caption: ""
ShowToc: true
TocOpen: false
---

## The problem

Keyword autocomplete research at scale requires running hundreds of seed queries against Google's suggestion endpoint. Running all queries through a single API backend creates three failure modes: credit exhaustion, rate limiting, and single-point-of-failure for a critical research step.

The project context: a large-scale CDCP dental keyword research project requiring autocomplete data across multiple query clusters simultaneously, with different AI agents executing different portions of the workload.

## The routing architecture

The multiplexer routes each incoming query to a backend based on which agent is making the request:

| Agent | Primary Backend | Fallback |
|---|---|---|
| Claude / Opus | Serper | ScrapFly |
| Haiku | ScrapFly | Direct Google |
| G1 (Zeus File Bridge) | Direct Google | ScrapFly |
| G3 / Qwen | ScrapFly | Direct Google |

The routing logic is policy-driven, not dynamic. Each agent has a defined primary and a defined fallback. The multiplexer checks credit availability on the primary backend before routing; if the primary is exhausted or unavailable, the request goes to the fallback automatically without any intervention required.

## Credit tracking

Each backend maintains a separate credit pool. The multiplexer tracks:

- Requests sent per backend per session
- Estimated credits consumed per request (by backend pricing model)
- Running total against configured per-backend limits
- Alert threshold before exhaustion (configurable)

Usage is logged per-request to a structured output file in `/outputs/` with timestamp, agent, backend used, query, and credit cost. Aggregate usage summary writes at session end.

## Backend characteristics

**Serper** — paid API, highest reliability, cleanest JSON response, rate limits apply per API key. Primary for Claude/Opus because Claude-originated research tasks are typically the highest-priority and most complex.

**ScrapFly** — paid scraping proxy, higher latency than Serper, better suited for volume tasks where per-request cost matters more than speed. Primary for Haiku and G3/Qwen volume workloads.

**Direct Google Autocomplete** — zero cost, no API key required (endpoint confirmed working), latency variable, subject to rate limiting from Google's side if request volume is high. Primary for G1 (Zeus) which runs against the infrastructure at high frequency and where per-request cost is the binding constraint.

## Output structure

Outputs go to `Auto Suggest Scraper V2/engine/` and `outputs/`. Each file contains:
- Seed query
- Backend used
- Timestamp
- Raw autocomplete suggestions returned
- Normalized suggestion list

The output format is compatible with downstream keyword clustering and intent classification pipelines.

## What this enables

The multiplexer enables the Zeus multi-agent infrastructure to run parallel keyword research workloads without manual backend selection per agent, without credit exhaustion stopping a full workload mid-run, and without logging gaps that would make usage audits impossible.

For the CDCP dental keyword project: different agents could run different query clusters simultaneously — G1 running neighbourhood + service combinations against Direct Google, Claude running high-priority procedure keywords against Serper — with the multiplexer handling routing, tracking, and failover transparently.

---

*Built May 2026. Output location: C:\Users\jfnfi\Documents\AI\Projects\Auto Suggest Scraper V2\. Backends: Serper API, ScrapFly, Direct Google Autocomplete endpoint. Agent routing: Claude/Opus, Haiku, G1, G3, Qwen.*
