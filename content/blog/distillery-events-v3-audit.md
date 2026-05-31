---
title: "Distillery Events: How a Toronto venue group is being eaten by a neighborhood entity it doesn't control"
date: 2026-05-27T22:00:00-05:00
draft: false
tags: ["case study", "entity SEO", "schema", "hospitality", "Toronto"]
categories: ["case studies"]
description: "The brand SERP is being cannibalized by thedistillerydistrict.com. The audit found Google miscategorized Distillery Events as a sub-attribute of the Distillery District neighborhood — and a fabricated 5★/500-review schema block on the homepage that's an active Google manual-action risk."
summary: "The brand SERP is being cannibalized by thedistillerydistrict.com. The audit found Google miscategorized Distillery Events as a sub-attribute of the Distillery District neighborhood — and a fabricated 5★/500-review schema block on the homepage that's an active Google manual-action risk. Full v3.1 marketing engine audit with 22 tabs and projected $233K–$382K 12-month revenue recovery."
cover:
  image: ""
  alt: ""
  caption: ""
ShowToc: true
TocOpen: false
---

## The headline

**Signal Density: 38.3% - Tier: Losing.** Across four commercial categories (corporate, weddings, group dining, event spaces), Distillery Events has zero Map Pack appearances. On the brand's own searches, [thedistillerydistrict.com](https://thedistillerydistrict.com/) outranks them (Map Pack 2 / Top-3 9 / Top-10 15 vs DE's 1 / 7 / 12).

## The thesis

The events business is being treated by Google as a feature of the neighborhood, not as a venue brand. Every symptom in the audit flows from this single ontological error. Schema absence, GBP undersizing, brand SERP cannibalization - all downstream effects.

## The schema discovery (post-publication correction)

The original v3 audit said "zero JSON-LD anywhere." That was wrong. A second LLM running the same audit caught what my crawler missed: the homepage carries a `Restaurant` schema block (wrong type for an events business) with a fabricated `aggregateRating: { "ratingValue": "5", "reviewCount": "500" }`.

Real GBP rating is 3.8 stars on 32 reviews. Yelp is 4.x on 86 reviews. There is no legitimate source for "5/500."

Per [Google's review-snippet guidelines](https://developers.google.com/search/docs/appearance/structured-data/review-snippet), fabricated review schema is a documented manual-action target. The audit's new Priority 0 is: **remove this before doing any other SEO work** - if Google flags it first, every tactical fix downstream is wasted.

## The architectural fix

Three moves, in order:

1. **Schema-level identity declaration.** Organization + LocalBusiness + EventVenue JSON-LD across all key pages, with sameAs arrays linking the parent (distilleryhospitality.com) + four sister restaurant brands + all social handles + GBPs.
2. **GBP "Department of" relationships** on all five family GBPs (DE + El Catrin + Cluny Bistro + Madrina + Pure Spirits).
3. **Reciprocal cross-linking** with explicit entity-language anchor text across the property family.

The unreplicable moat: **no other Toronto event venue has four sister restaurants + four event spaces + two partner galleries + outdoor grounds on one property under one parent organization.** Activation requires roughly one week of dev work plus 1-2 hours of GBP admin.

## Projected revenue impact

| Phase | Window | Recovery range |
|---|---|---|
| Tier-0 foundational | Days 1-30 | $78K - $132K |
| Tier-1 per-venue + geo | Days 31-90 | $80K - $125K incremental |
| Tier-2 hub + AI search | Days 91-180 | $50K - $85K incremental |
| Tier-3 brand SERP + authority | Days 181-365 | $25K - $40K incremental |
| **Cumulative 12-month** | - | **$233K - $382K** |

## What I learned

WebFetch and SiteOne Crawler both missed the schema because they don't reliably scan `<script type="application/ld+json">` blocks. Always raw-fetch HTML and grep for `ld+json` as part of any schema audit going forward.

Independent LLM verification is now part of the methodology. One model running the audit is a sanity check; two models running it independently is a verification.

---

*Full v3.1 marketing engine audit is a 22-tab interactive HTML deliverable (~170 KB). Available on request.*
