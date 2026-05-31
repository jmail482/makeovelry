---
title: "Excalibur: Building a 14-module marketing audit engine that runs on multiple LLMs and delivers 22-tab interactive HTML"
date: 2026-05-29T12:00:00-05:00
draft: false
tags: ["case study", "AI infrastructure", "marketing engine", "audit system", "Excalibur"]
categories: ["case studies"]
description: "Excalibur is a multi-LLM marketing audit system that evolved from a single-analyst diagnostic into a 14-module business growth intelligence framework delivering interactive HTML audit reports. Live deployments: Sologlass.ca (Excalibur V2, April 2026) and Distillery Events (Excalibur V3.1, May 2026)."
summary: "The Excalibur Marketing Engine was built iteratively to solve a specific problem: producing comprehensive, evidence-tagged marketing audits at a scale and speed no single analyst could achieve manually. By V3.1, the system produced a 22-tab interactive HTML deliverable covering 14 modules — from brand SERP to schema to revenue projection — with independent LLM verification built into the methodology."
cover:
  image: ""
  alt: ""
  caption: ""
ShowToc: true
TocOpen: false
---

## What Excalibur is

Excalibur is a structured multi-LLM marketing audit framework. It assigns specific analytical modules to specific models, enforces an evidence-tagging protocol across all outputs, and produces a structured deliverable — currently a 22-tab interactive HTML report — that a client, advisor, or prospective client can navigate without the analyst being present.

The system is not a single prompt. It is a multi-stage pipeline with defined modules, a routing logic, and a QA layer where a second independent model verifies the primary audit's findings.

## How it evolved

**V2 — Sologlass.ca (April 25, 2026).** The first documented production deployment. A 14-module Business Growth Intelligence Report covering an ICBC-certified BC auto glass shop. Delivered as a tabbed interactive HTML with six core sections: Executive Summary, Page-Level Audit, Rankings Data, Competitive Matrix, SWOT, and Roadmap. Evidence protocol: every finding tagged as VERIFIED / SITE CRAWL / AUTH SOURCE / NEEDS VALIDATION / CALCULATED. Data inputs: SEO PowerSuite Rank Tracker v8.50.18[^1] geo-located from both business addresses, direct site crawl.

**V3.1 — Distillery Events (May 2026).** The Distillery Events audit introduced a finding that changed the methodology permanently. The primary LLM audit reported "zero JSON-LD anywhere." A second independent LLM running the same audit caught what the primary crawler missed: the homepage carried a Restaurant schema block (wrong type for an events business) with a fabricated aggregateRating — 5 stars / 500 reviews — against a real GBP rating of 3.8 stars on 32 reviews.

Per Google's review-snippet guidelines, fabricated review schema is a documented manual-action target.[^2] This became Priority 0 in the V3.1 audit.

**The methodology change locked in at V3.1:** independent LLM verification is now a required step in every Excalibur audit. WebFetch and site crawlers don't reliably scan `<script type="application/ld+json">` blocks — raw HTML fetch and grep for ld+json is now part of every schema audit.

## The 14-module framework

- M0: Business context and competitive tier classification
- M1: Technical SEO (crawl, canonical, HTTP/HTTPS, dev artifacts)
- M2: On-page signals (title tags, H1s, meta, geo-targeting)
- M3: Schema and structured data (LocalBusiness, AutoRepair, FAQPage, Organization, etc.)
- M4: Page speed and Core Web Vitals[^3]
- M5: Content depth and topical authority
- M6: Local Pack mechanics (GBP completeness, service area, category)
- M7: Review velocity and recency analysis
- M8: Competitive matrix (dedicated page structure, franchise vs independent)
- M9: Citation consistency and NAP audit
- M10: SWOT with evidence tagging
- M11: Keyword architecture by tier (core buyer, adjacent, comparison/review)
- M12: Revenue projection and conversion funnel modelling
- M13: Phased roadmap with dependency sequencing

Each finding is tagged to its evidence source. Claims without a source get a NEEDS VALIDATION tag — not a fabricated figure.

## The deliverable format

Single-file interactive HTML. Tabbed navigation. Designed for delivery to a client who may forward it to a business partner, accountant, or advisor. No login required. No external dependencies beyond a browser.

## What the system can't claim

Two live deployments are documented. Neither client has been tracked through full implementation of the audit roadmap. Revenue projections in both reports are modelled estimates based on documented search volumes, stated conversion benchmarks from named industry sources, and procedure/service margin data from verified price guides — not realized outcomes.

---

[^1]: SEO PowerSuite. *Rank Tracker v8.50.18.* link-assistant.com. Geo-located rank tracking configured from both Solo Glass business addresses (Langley and South Surrey) for the April 2026 audit.
[^2]: Google Search Central. *Review Snippets Structured Data.* developers.google.com/search/docs/appearance/structured-data/review-snippet.
[^3]: Google Search Central. *Core Web Vitals.* developers.google.com/search/docs/appearance/core-web-vitals. Defines LCP, INP, and CLS as ranking signals used in Google's page experience assessment.
