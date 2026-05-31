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

**Overall Digital Health Score: 38/100.**

Five total pages. Zero schema markup anywhere. Homepage loading in approximately 5 seconds.

From the Langley address: 11 keywords tracked, zero organic traffic. Best position: #18 for "windshield replacement langley" (150 searches/month) — on the **/about/ page**, not the /services/ page. Three keywords appearing as thumbnail results only (near-zero click value).

From the South Surrey address: complete blackout. Zero organic rankings. Zero Map Pack rankings. Zero AI Overview appearances. "Auto glass repair surrey" — not in the top 30. A physical shop at 1706 152 Street that Google did not know existed.

## Four critical failures

**1. HTTP/HTTPS dual indexing.** Rank Tracker confirmed both `http://sologlass.ca/` and `https://sologlass.ca/` were indexed as separate pages, splitting all ranking signals between them. The footer logo linked to the HTTP version. Per Google's canonical documentation, this dilutes every ranking signal the site had earned.

**2. Dev server links in footer.** Every page on the site carried footer Quick Links — "Services", "About", "FAQs", "Contact" — all pointing to `dev3.boost-digital.ca` instead of `sologlass.ca`. The /services/ page additionally carried an image hosted on `ejw.f33.mytemp.website`, a temporary build server. Google's crawler followed these links on every crawl, routing crawl equity away from the production site.

**3. Wrong page ranking for all service keywords.** The /about/ page ranked for 11 keywords. The /services/ page ranked for one. Google chose /about/ because it contained more Langley-relevant text than the services page. No proper location pages existed to give Google a correct target.

**4. Every title tag and image alt text said "Langley."** Five pages, all titled for Langley only. Every image alt described a service "in Langley." Zero Surrey, South Surrey, or White Rock signals existed anywhere on the site — for a business whose second location was one block from the White Rock border.

## The competitive context

NOVUS Glass South Surrey holds ICBC Tier 1 Top Performer status — listed first on ICBC's official repair locator, with a dedicated /south-surrey/ page whose title explicitly says "(WHITE ROCK)." Speedy Glass has a physical White Rock address and a dedicated /white-rock/ URL. Braymar Glass (formerly Broco Glass) has operated in South Surrey/White Rock for 25+ years with dedicated location content.

Solo Glass's South Surrey location at 1706 152 Street is physically closer to most White Rock residents than NOVUS at 2546 King George Blvd. The proximity advantage existed. The content to claim it did not.

The keyword difficulty data confirmed the opportunity: all 11 tracked keywords showed green difficulty ratings (10–23 range). These were not hard keywords to rank for. The structural damage was the only barrier.

## The 24-step roadmap

The audit delivered a sequenced 3/6/12-month roadmap where each phase depended on the prior:

**Phase 1 — 3 months:** Force HTTPS canonical sitewide. Fix dev server links (5 footer links + 1 image URL). Diagnose and resolve 5-second homepage load. Build /langley/ and /south-surrey/ dedicated location pages with LocalBusiness + AutoRepair JSON-LD schema. Build /white-rock/ service area page. Fix all page titles and image alt text sitewide. Add FAQPage schema to existing 13 FAQs. Configure GBP profiles to location pages. Launch Surrey review generation program.

**Phase 2 — 6 months:** Dedicated service pages (/windshield-repair/, /windshield-replacement/, /mobile-service/). ICBC claims landing page (a content type no competitor in White Rock/South Surrey owned). ADAS calibration investigation. Service area pages for adjacent communities. Blog launch.

**Phase 3 — 12 months:** Content hub (15–20 interlinked pages around ICBC + BC auto glass). YouTube video content. GEO optimization and llms.txt for AI search citation. Expanded service area coverage. Sustained review velocity (target: 350+ combined reviews).

## What this demonstrates

Auto glass in BC is an insurance-paid category. ICBC covers windshield repair and replacement directly — customer cost is limited to their deductible. The conversion bottleneck is not price or persuasion. It is visibility. Every person searching "windshield repair near me" in South Surrey who didn't find Solo Glass was revenue going to NOVUS, Speedy, or Braymar by default.

The audit's sequencing principle: you cannot build location pages until canonical is resolved. You cannot target White Rock until location architecture exists. The 24 items were not a list — they were a dependency chain. Executing them out of order wastes work.

---

*Excalibur V2 audit, April 25, 2026. Data: SEO PowerSuite Rank Tracker v8.50.18 (geo-located from both business addresses). ICBC tier data: ICBC Glass Repair Program Guide, Oct 2024. Evidence protocol: VERIFIED / SITE CRAWL / AUTH SOURCE / NEEDS VALIDATION / CALCULATED — tagged per finding.*
