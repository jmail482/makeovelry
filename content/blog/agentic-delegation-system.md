---
title: "Building an 8-layer agentic delegation system: orchestration, routing, and cost discipline across a multi-LLM stack"
date: 2026-05-29T11:30:00-05:00
draft: false
tags: ["case study", "AI infrastructure", "agentic systems", "multi-LLM", "automation"]
categories: ["case studies"]
description: "A completed agentic orchestration framework defining 8 delegation layers, 7 workflow types, a free-first routing matrix, and an inbox/outbox handoff protocol for multi-agent AI task execution — built as a standalone operating system for AI-assisted marketing work."
summary: "The Agentic Org Chart and Workflow System defines how AI tasks are structured, routed, and executed across a multi-provider stack (Witsy, Ollama, OpenRouter, Cerebras, Groq, Google, xAI). The framework separates strategy from execution, writer from critic, and establishes cost discipline rules that reserve premium model tokens for synthesis and QA — not bulk processing."
cover:
  image: ""
  alt: ""
  caption: ""
ShowToc: true
TocOpen: false
---

## The problem this solves

Running multiple AI models across multiple providers without a routing framework produces predictable outcomes: premium model tokens burned on low-value tasks, no separation between the agent doing the work and the agent checking it, no cost discipline, no status tracking between agents, and no systematic way to hand off work from one model to the next.

This framework solves all of it.

## The 8-layer hierarchy

Each layer has a defined ownership scope, specific inputs, and specific outputs. Nothing crosses layers informally.

**Layer 0 — Principal.** Human decision owner. All escalations terminate here.

**Layer 1 — Executive Orchestrators.** Set goals, define scope, assign workflows, approve escalations, accept final output on high-stakes tasks.

**Layer 2 — Delegation Managers / Routers.** Choose model and service. Decide cheapest viable route vs premium strategist. Choose Witsy vs Ollama vs paid API. Enforce cost and latency rules. Trigger escalations.

**Layer 3 — Researchers / Extractors.** Pull source data. Scrape or retrieve task inputs. Gather files, URLs, SERP data, GBP profile data. Normalize into structured payloads for downstream layers.

**Layer 4 — Scorers / Classifiers.** First-pass issue scoring, clustering, categorization, priority assignment, evidence labeling.

**Layer 5 — Writers / Generators.** Create drafts. Produce reports. Generate structured outputs. Synthesize artifacts.

**Layer 6 — Critics / QA.** Challenge the draft. Verify fit against requirements. Check for coherence, omissions, weak reasoning, formatting errors. The critic is always a separate model from the writer — never self-review.

**Layer 7 — Publishers / Executors.** Save files. Update dashboards. Push outputs to storage. Hand off to implementation channels.

**Layer 8 — Monitors / Reporters.** Track status. Normalize metrics. Produce executive reporting. Maintain workflow state.

## Free-first routing logic

The default execution rule: use the cheapest viable route. Escalate to paid or premium models only when the task genuinely requires it.

| Task type | Default route | Escalate when | Final escalation |
|---|---|---|---|
| Bulk extraction | Cheapest reliable worker | Extraction quality weak | Strategist verifies sample |
| Classification/scoring | Cheap structured worker | Ambiguity high | Strategist cluster review |
| Strategic brief | Premium strategist | High-stakes scope | Executive QA |
| Draft writing | Strong generator | Quality weak | Premium rewrite or critique |
| QA/critique | Separate critic model | Risk high | Executive orchestrator |
| Local/profile research | Witsy/local + cheap worker | Data quality unclear | Strategist local review |
| Local/private drafting | Ollama peer | Quality insufficient | Witsy/premium route |

The routing matrix enforces one discipline above all: **do not burn premium tokens on bulk first-pass tasks.** Cheap workers handle extraction and scoring. Premium models handle synthesis, executive QA, and genuinely hard reasoning. Writers and critics are never the same model.

## The Witsy substrate

Witsy (local service, port 8090) functions as the primary delegation hub — routing tasks across an engine inventory spanning OpenRouter, Mistral, Google Gemini, Groq, Cerebras, OpenAI, Anthropic, DeepSeek, xAI, and Ollama. The hub executes HTTP POST / JSON and SSE streaming.

Ollama operates as a peer local inference layer, not a subordinate Witsy dependency. Recommended use cases: local low-cost summarization, quick reasoning or coding helpers, preprocessing, private draft generation, and overflow work when central routes are constrained.

## Inbox/outbox protocol

Cross-agent handoff uses a structured message schema with defined status states:

```json
{
  "task_id": "uuid-or-timestamp",
  "agent_from": "source-agent",
  "agent_to": "target-agent",
  "instruction": "detailed task",
  "model": "preferred-model",
  "timeout_sec": 180,
  "priority": "normal"
}
```

Status states: received → running → complete → error → escalation needed. Every step produces a trackable status. No silent failures.

## 7 workflow types

Each workflow is a defined chain from orchestrator to publisher. The chains are templates — not ad hoc decisions made per task.

**Article generation:** SERP/top-10 extractor → factor matrix scorer → brief writer → article drafter → critic/SEO QA → publisher. Inputs: target keyword, market, scope. Outputs: factor matrix, content brief, draft, QA pass, publish-ready artifact.

**GBP / local optimization:** Local research extractor → profile auditor → landing-page matcher → review/proof strategist → critic/QA → implementer/tracker. Inputs: profile URL, landing pages, location targets, competitor set. Outputs: issue matrix, alignment actions, proof/review plan, implementation queue.

**400-site audit:** Bulk extractor → first-pass classifier → issue clusterer → strategist summarizer → critic/QA → report generator. Core rule: do not use premium models on every site first. Cheap workers handle first-pass classification. Premium models touch only cluster summaries and executive output.

**Marketing plan generation:** Baseline aggregator → package-fit scorer → roadmap drafter → critic/QA → dashboard initializer. Outputs: recommended package, milestone roadmap, KPI plan, first implementation queue.

Additional workflow templates: image generation, video generation, dashboard/reporting — each with defined chains, inputs, outputs, and routing rules.

## Cost discipline principles

Every workflow operates under the same financial rules:

- Default to free-first
- Use local/Ollama where it is genuinely useful, not as a fallback after premium models are exhausted
- Reserve premium models for synthesis, executive QA, and genuinely hard reasoning
- Keep writer and critic separate to reduce wasted premium spend on self-review
- Do not burn premium tokens on bulk first-pass tasks

The framework is a standalone completed product — separate from any niche or client implementation. Niche implementations (dental market research, local SEO for specific clients) run under the framework's umbrella but are not merged into it. The boundary rule: the framework defines the operating system. Subprojects are applications running on it.

---

*Agentic Org Chart and Workflow System — standalone completed product documentation. Multi-LLM stack: Witsy (port 8090), Ollama local peer, OpenRouter, Cerebras, Groq, Google Gemini, xAI, DeepSeek, Mistral, Anthropic.*
