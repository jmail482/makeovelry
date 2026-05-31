---
title: "whichkitchenappliance.com: How a URL restructure generated 403s on every ranking page and collapsed a site overnight"
date: 2026-05-28T10:00:00-05:00
draft: false
tags: ["case study", "technical SEO", "403", "ranking collapse", "crawl audit"]
categories: ["case studies"]
description: "A Screaming Frog crawl identified 403 Forbidden errors on every high-ranking /cookers/ content page and 523 blocked images. The collapse wasn't an algorithm update — it was a URL restructure that broke indexed paths."
summary: "A well-performing UK kitchen appliance affiliate blog lost 91% of its top-3 keywords in two weeks. Screaming Frog identified the cause: a content restructure that returned 403 Forbidden on the structural ranking assets and blocked 523 image files simultaneously. The client chose not to implement the rollback."
cover:
  image: ""
  alt: ""
  caption: ""
ShowToc: true
TocOpen: false
---

## The situation

**whichkitchenappliance.com** was a well-performing UK kitchen appliance affiliate blog. At its pre-collapse peak (SEMrush, Nov 24–30, 2021), the site held 68 keywords in the top 3, 157 in the top 10, and 365 in the top 100 — average position 44.39, estimated daily traffic 72.66. Google Analytics confirmed 147,325 en-gb users and 168,276 sessions between April 2021 and January 2022.

On November 28, 2021, organic traffic collapsed sharply. Lisa reached out in February 2022 unable to identify the cause.

## The diagnosis question

The first task was distinguishing between a site-side technical failure and a Google algorithm update. That distinction determines whether the recovery action is within the site owner's control. Jonathan used raw GA data — not third-party approximations — to annotate the traffic graph directly, noting that the drop point did not align with any known algorithm update and warranted a technical investigation first.

## What the crawl found

A Screaming Frog technical crawl of the site identified the cause. Multiple key content pages in the /cookers/ category were returning **403 Forbidden (Client Error) / Non-Indexable**:

- /cookers/electric-cookers-induction-vs-ceramic-cooker-tops/
- /cookers/how-to-buy-a-new-gas-cooker/
- /cookers/range-cooker-guide/
- /cookers/what-is-a-range-cooker/
- /cookers/do-electric-cookers-come-with-plugs/
- /cookers/what-are-the-different-range-cooker-sizes/
- /cookers/does-le-creuset-work-with-induction-hobs/

One additional page (/cookers/do-gas-cookers-need-an-electric-supply/) had been incorrectly canonicalised. These were the structural ranking assets — not low-value or orphaned pages.

A secondary crawl filtered to image files found **523 image URLs in /wp-content/uploads/ also returning 403 Forbidden**. The server was returning HTML error pages instead of image files — Content-Type was text/html — eliminating the site's entire image SEO footprint simultaneously.

## The outcome

| Metric | Pre-collapse (Nov 24–30, 2021) | Post-collapse (Dec 8, 2021) | Change |
|---|---|---|---|
| Top-3 keywords | 68 | 5 | −91% (64 lost) |
| Top-10 keywords | 157 | 56 | −64% (101 lost) |
| Organic visibility | 9.60% | 2.50% | −7.74pp |
| Estimated daily traffic | 72.66 | 24.84 | −66% |

347 keywords declined simultaneously in a two-week window against 14 improving.

## The recommendation — and what happened

Roll back to the prior URL structure to restore indexed paths, then rebuild the architecture correctly from a stable baseline. Lisa chose not to implement the rollback. The engagement concluded at the diagnostic stage.

## What this demonstrates

The methodology — raw GA annotation to rule out an algorithm event before diagnosing a technical cause — is the correct sequencing for any unexplained ranking collapse. Third-party rank trackers provide an approximation. GA provides the real number.

---

*Screaming Frog crawl data, GA export (Apr 2021–Jan 2022), and SEMrush Landscape reports (Nov 24–Dec 8, 2021) on file. Engagement: February 2022.*

