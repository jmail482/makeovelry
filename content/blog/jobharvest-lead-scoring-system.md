---
title: "JobHarvest: A scoring and filtering system for SEO job leads — built because most job boards waste your time"
date: 2026-05-29T13:30:00-05:00
draft: false
tags: ["case study", "automation", "job search", "lead scoring", "Python"]
categories: ["case studies"]
description: "JobHarvest is a job lead filtering and scoring system built to eliminate the 75%-match-or-reject threshold problem in SEO job searching. It filters for role fit, flags EU/non-remote locations, removes junior roles, and scores remaining leads against a documented skills profile — all without generating filler leads."
summary: "Senior SEO job searching without a filter system produces noise: junior roles, EU-only listings, mismatched titles, and remote-listed roles that turn out to be location-specific. JobHarvest applies a 75% match threshold minimum, removes filler, and scores leads against a documented profile. Methodology documented in HOW_SCORING_WORKS.md (688 lines). Top leads identified include Webrunner Media Senior SEO Lead, CareForMix Digital Marketing Specialist, and GCOM Support SEO Specialist."
cover:
  image: ""
  alt: ""
  caption: ""
ShowToc: true
TocOpen: false
---

## The problem with raw job boards

Senior SEO job searching against raw job board output produces predictable noise: junior roles labelled as "specialist," EU-only listings appearing in Canadian remote searches, titles like "Digital Marketing Coordinator" mixed with "SEO Lead," and roles that require skills stacks (paid social, programmatic, CRO) that don't match a Local SEO / Technical SEO specialist profile.

Running this noise through a manual review process costs time and produces frustration, not leads. The solution is a filter-first system.

## The scoring methodology

JobHarvest applies a documented scoring methodology (HOW_SCORING_WORKS.md, 688 lines at `C:\Users\jfnfi\Documents\AI\Projects\job-scraper\how this works\`) before any lead reaches review.

**Hard exclusions applied before scoring:**
- EU and non-Canadian international locations (even when listed as remote)
- German location listings
- Junior-level roles (Coordinator, Assistant, Entry Level by title or JD signal)
- Roles requiring primary expertise outside the documented skills profile

**Match threshold:** 75% minimum. Below 75%, the lead is excluded without review — not flagged for manual consideration.

**Scoring inputs:**
- Role title alignment to target titles: SEO Specialist / SEO Lead / SEO Manager / Digital Marketing Specialist
- Location: remote Canada or Winnipeg on-site preferred; other on-site excluded
- Skills overlap against documented profile (Local SEO, Technical SEO, GBP, WordPress, Google Ads, Meta Ads)
- Seniority signal from JD language and required years of experience

**Resume sources used for matching:** Resume.txt, resume data sheet.txt, old stuff i could beef my resume up with.txt. Not Jonathan_Nishikawa_Resume.docx — the one-page format obscures experience depth that the scoring system needs to assess.

## Top leads identified

The system produced actionable leads at or above the 75% threshold:

- **Webrunner Media — Senior SEO Lead** — strong title match, Canadian remote, agency context aligned to service profile
- **CareForMix — Digital Marketing Specialist** — healthcare sector, remote Canada, skills overlap confirmed
- **GCOM Support — SEO Specialist** — technical SEO emphasis, confirmed Canadian, role scope aligned

Each lead above threshold goes to manual review for cover letter development and application. Each lead below threshold is logged but not reviewed.

## What the system does not do

JobHarvest does not auto-apply. It does not send emails. It does not generate cover letters. It produces a filtered, scored lead list and stops there. Human judgment handles everything past the scoring output.

The system also does not claim outcome data. No conversion-to-interview rate is documented. No offer data exists. The system's value is in the front-of-funnel: eliminating noise and surfacing leads worth manual time.

---

*HOW_SCORING_WORKS.md: 688 lines. Path: C:\Users\jfnfi\Documents\AI\Projects\job-scraper\how this works\. Match threshold: 75%. Target roles: SEO Specialist, SEO Lead, SEO Manager, Digital Marketing Specialist. Target locations: remote Canada, Winnipeg on-site.*
