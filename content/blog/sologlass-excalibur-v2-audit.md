---
title: "Sologlass.ca: A 4.9-star ICBC-certified auto glass shop invisible to every search — and 24 steps to fix it"
date: 2026-05-29T10:00:00-05:00
draft: false
tags: ["case study", "technical SEO", "local SEO", "ICBC", "Excalibur", "auto glass"]
categories: ["case studies"]
description: "Solo Glass had a 4.9-star Google rating, 149+ reviews, two locations, and ICBC certification. From their South Surrey address, they ranked for zero keywords — organic, Map Pack, and AI Overviews all blank. The Excalibur V2 engine diagnosed why."
summary: "A two-location BC auto glass shop with exemplary real-world credentials produced an overall digital health score of 38/100. The audit found the /about/ page ranking for 11 service keywords, footer links pointing to a development server on every page, HTTP and HTTPS indexed as separate pages, and zero digital presence from the Surrey location. A 24-step roadmap sequenced the fix."
cover:
  image: ""
  alt: ""
  caption: ""
ShowToc: true
TocOpen: false
---

## The business

Solo Glass is an ICBC-certified, ITA government-certified auto glass shop operating two locations in BC: Langley (#104 – 22575 Fraser Hwy) and South Surrey (1706 152 Street). Their Google rating: 4.9 stars across 149+ reviews. They offer a lifetime warranty on workmanship, mobile service, and proprietary GlassHealer resin. Family-owned against national franchise competitors NOVUS (Mondofix) and Speedy Glass (Belron).

**The real-world business was strong. The website was preventing Google from understanding any of it.**

*Excalibur V2 audit generated April 25, 2026. Data: SEO PowerSuite Rank Tracker v8.50.18 geo-located from both business addresses. Overall Digital Health Score: 38/100.*

## What the audit found

Five total pages. Zero schema markup anywhere. Homepage loading in approximately 5 seconds — estimated 35% conversion loss before a visitor sees content, based on a documented 7% conversion reduction per second of load delay.[^1]

From the Langley address: 11 keywords tracked, zero organic traffic. Best position: #18 for "windshield replacement langley" (150 searches/month, CPC $6.84[^2]) — on the /about/ page, not the /services/ page. Three keywords appearing as thumbnail results only (near-zero click value). Click-through rates at position 18 approach 0%.[^3]

From the South Surrey address: complete blackout. Zero organic rankings. Zero Map Pack rankings. Zero AI Overview appearances. "Auto glass repair surrey" — not in the top 30. A physical shop at 1706 152 Street that Google did not know existed.

## Four critical failures

**1. HTTP/HTTPS dual indexing.** Rank Tracker confirmed both `http://sologlass.ca/` and `https://sologlass.ca/` were indexed as separate pages, splitting all ranking signals between them. Per Google's canonical documentation, duplicate URL indexing dilutes ranking signals across both versions.[^4]

**2. Dev server links in footer.** Every page carried footer Quick Links — "Services", "About", "FAQs", "Contact" — all pointing to `dev3.boost-digital.ca` instead of `sologlass.ca`. The /services/ page additionally carried an image hosted on `ejw.f33.mytemp.website`. Google's crawler followed these links on every crawl, routing crawl equity away from the production site.

**3. Wrong page ranking for all service keywords.** The /about/ page ranked for 11 keywords. The /services/ page ranked for one. No proper location pages existed. Per Moz local ranking factors research, a location page with consistent NAP and schema is foundational to local visibility.[^5]

**4. Every title tag and image alt text said "Langley."** Five pages, all titled for Langley only. Every image alt described a service "in Langley." Per Google's Images documentation, alt text carries geographic relevance signals.[^6] Zero Surrey, South Surrey, or White Rock signals existed anywhere on the site — for a business whose second location was one block from the White Rock border.

## The competitive context

NOVUS Glass South Surrey holds ICBC Tier 1 Top Performer status — listed first on ICBC's official repair locator per the ICBC Glass Repair Program Guide.[^7] Tier 1 requires a 35%+ windshield repair ratio and delivers a 2% NAGS part rebate, $75/repair claim, and faster payment cycles.[^7] NOVUS's dedicated /south-surrey/ page explicitly targets "(WHITE ROCK)" in the title. Speedy Glass has a physical White Rock address. Braymar Glass (formerly Broco Glass) has operated in South Surrey/White Rock for 25+ years.[^8]

Solo Glass's South Surrey location at 1706 152 Street is physically closer to most White Rock residents than NOVUS at 2546 King George Blvd. The proximity advantage existed. The content to claim it did not.

All 11 tracked keywords showed green difficulty ratings (10–23 range) — low difficulty that proper page structure would rank for. The structural damage was the only barrier.

## The 24-step roadmap

Sequenced by dependency — canonical must be resolved before location pages can work:

**Phase 1 — 3 months:** Force HTTPS canonical sitewide (301 redirect HTTP to HTTPS; fix footer logo link). Fix dev server links (5 footer links + 1 image URL). Diagnose and resolve 5-second homepage load. Build /langley/ and /south-surrey/ dedicated location pages with LocalBusiness + AutoRepair JSON-LD schema. Build /white-rock/ service area page. Fix all page titles and image alt text sitewide. Add FAQPage schema to existing 13 FAQs (zero content creation required — answers already exist). Configure GBP profiles to location pages with non-overlapping service areas. Launch Surrey review generation program (target: 15+ Surrey reviews within 90 days).

**Phase 2 — 6 months:** Dedicated service pages (/windshield-repair/, /windshield-replacement/, /mobile-service/). ICBC claims landing page (no competitor in White Rock/South Surrey owned this content type). ADAS calibration investigation (both NOVUS and Speedy Glass featured ADAS; Sologlass had zero mention). Service area pages for adjacent communities. Blog launch.

**Phase 3 — 12 months:** Content hub (15–20 interlinked pages around ICBC and BC auto glass). YouTube video content. GEO optimization and llms.txt for AI search citation. Expanded service area coverage. Sustained review velocity — target: 350+ combined reviews across both GBPs.

## What this demonstrates

Auto glass in BC is an insurance-paid category. ICBC covers windshield repair and replacement directly — customer cost is limited to their deductible.[^7] The conversion bottleneck is not price or persuasion. It is visibility. The 24 items were not a list — they were a dependency chain. Executing them out of order wastes work.

---

[^1]: SteerPoint. *Why Website Speed Is More Important Than Ever in 2025.* 2025. Documents 7% conversion reduction per additional second of page load time.
[^2]: SEO PowerSuite Rank Tracker v8.50.18. CPC and ranking data geo-located from Langley business address, April 2026.
[^3]: Advanced Web Ranking. *Organic CTR Study*, 2024–2025. Position 18 produces near-zero click-through rates under standard organic CTR distribution curves.
[^4]: Google Search Central. *Consolidate Duplicate URLs.* developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls.
[^5]: Moz. *Local Search Ranking Factors*, 2025. Location page with consistent NAP and LocalBusiness schema documented as a foundational local signal.
[^6]: Google Search Central. *Google Images Best Practices.* developers.google.com/search/docs/appearance/google-images.
[^7]: ICBC. *Glass Repair Program Guide (CSP51).* Effective October 1, 2024. partners.icbc.com.
[^8]: Peace Arch News. *South Surrey Auto Glass Repair Shop Responds to ICBC Changes*, 2023.
