---
title: "TWAG: Six years, 33 cities, and the +104% keyword lift that came from one Cloudflare config change"
date: 2026-05-20T19:00:00-05:00
draft: false
tags: ["case study", "technical SEO", "multi-location", "wealth advisory", "Cloudflare"]
categories: ["case studies"]
description: "Anchor advisor went from #6 to #2 on Wealth Professional Canada's Top-50 list during the engagement. The national location-page program lifted top-100 ranked URL share from 26% to 55%. Cloudflare + Argo Smart Routing deployment delivered a SEMrush-verified 104% keyword visibility lift."
summary: "Anchor advisor went from #6 to #2 on Wealth Professional Canada's Top-50 list during the engagement. The national location-page program lifted top-100 ranked URL share from 26% to 55%. Cloudflare + Argo Smart Routing deployment delivered a SEMrush-verified 104% keyword visibility lift after Google started favoring crawl-budget and mobile-first more aggressively."
ShowToc: true
TocOpen: false
---

## The engagement

**Tetrault Wealth Advisory Group (TWAG)** — Canaccord Genuity-affiliated wealth advisory based in Winnipeg, with a national reach problem. Engagement window: November 2019 through November 2025. Six years, 138 bi-weekly KPI reports.

## The headline outcome

Anchor advisor lifted from **#6 to #2** on Wealth Professional Canada's Top-50 Advisors list during the engagement.[^1]

## The national location program

33 location pages built across every Canadian province. Each page: geo-modified H1 + title + meta, province-specific content (regulatory context, local economic markers), LocalBusiness schema with province-specific GeoCoordinates, map embed, and internal links from neighbourhood-anchored copy on the home and service pages.

**Top-100 ranked URL share went from 26% to 55%** across the engagement.[^2] Calgary location page eventually outperformed the homepage in GSC — verified visible.

## The Cloudflare + Argo Smart Routing deployment

Mid-engagement, Google started favouring crawl-budget efficiency and mobile-first signals more aggressively.[^3] A Cloudflare deployment with **Argo Smart Routing** enabled — routing requests through Cloudflare's least-congested edge paths instead of standard internet routing[^4] — delivered a SEMrush-verified **+104% keyword visibility lift** in the months following.[^2]

Why it worked: Argo reduced TTFB across the long tail of city-specific page-loads, which in turn improved every Core Web Vitals signal Google was newly weighting.[^3] The pages weren't faster in any dramatic local-measurement sense — they were faster from the locations Google's crawlers happen to live in.

## Lessons

- **Multi-location SEO is two ranking systems running in parallel.** Map Pack (per-GBP) and local organic (per-page-on-the-domain) move on different signals. Audit both separately.[^5]
- **Schema correctly applied is force-multiplier infrastructure**, not "nice to have." Six years of pages with proper LocalBusiness + Service schema let the brand surface in dozens of intent classes Google wouldn't otherwise have routed to.
- **Performance optimization for SEO is about Google's crawlers' experience, not just user experience.** Argo helps because Cloudflare's edges are where Google's crawlers' bots actually live.[^4]

---

*Engagement closed Nov 2025. Domain has since been migrated and rebranded — the case-study data here reflects the engagement-period state.*

[^1]: Wealth Professional Canada. *Top 50 Advisors*, 2024 edition. Rankings verified against published list during the engagement period.
[^2]: SEMrush. Keyword visibility and URL ranking data exported from TWAG domain tracking, November 2019–November 2025. 104% keyword lift figure verified from SEMrush Landscape report.
[^3]: Google Search Central. *Mobile-First Indexing Best Practices* and *Core Web Vitals.* developers.google.com. Google's published guidance on crawl-budget efficiency and mobile-first signals as ranking factors.
[^4]: Cloudflare. *Argo Smart Routing* product documentation. cloudflare.com/products/argo-smart-routing. Routes traffic through Cloudflare's optimized network paths to reduce latency and TTFB.
[^5]: Sterling Sky; Joy Hawkins. *Multi-Location Local SEO Methodology.* sterlingsky.ca. Documented framework distinguishing Map Pack signals (GBP-driven) from local organic signals (on-page and domain-level).
