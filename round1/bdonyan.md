# Crowdsourcing Project Idea: [Project Title]

## Author
Brandon Yan, bdonyan

## Problem Statement
Penn students waste time guessing dining hall, gym, printing, and cafe wait times. Official queues are not published or are stale. A lightweight, crowdsourced reporting system can provide fresh, location-level wait times students can actually use to plan their day.

## Core Concept
**One-line pitch:** Real-time, crowdsourced wait times for popular campus locations with simple QC and robust aggregation.

**Target users:** Penn students deciding where/when to go (dining, gyms, cafes, printers).

**The crowd:** On-site students recruited via QR posters, Discords, GBMs, and social posts; small weekly raffle for participation.

**The task:** Submit current wait in minutes + a quick line photo; optionally a headcount. The form captures GPS and timestamp automatically.

## Key Features
1. One-tap report: wait minutes + quick photo
2. Auto-GPS/time checks to verify you’re there and it’s recent
3. Live map showing current wait + a simple confidence badge

## Feasibility Check
**Data source:** User-submitted reports from students on site; seed with team spot checks in first week.

**Budget reality:** <$500: $200 gift-card raffle, $50 posters, $0 hosting (GitHub Pages + Firebase/Sheets).

**Crowd size needed:** Dozens of contributors per week; a few hundred reports total for good coverage.

**Quality control approach:** Get ~3 reports per location per 15 minutes, reject stale/outsider photos (time/GPS), and down-weight reports that disagree with gold checks.

## Technical Approach
**Human tasks:** Enter wait minutes and take a quick photo on-site.

**Automated tasks:** Capture GPS/time, reject stale/duplicate photos, compute the final wait, update the map.

**Aggregation method:** Time-decayed, trust-weighted median of all valid reports in the last ~20 minutes.

## Prior Work
**Similar projects:** Google “Popular Times” / Waze crowd signals — ours focuses on specific campus spots with photo+GPS verification.

**Lessons from past course projects:** Keep tasks tiny, use redundancy, show a simple dashboard early, recruit with QR posters.

## Why This Could Work
Tasks take ~30 seconds, are easy to verify (photo + GPS), and a small crowd can cover key locations quickly. The tech is simple (static site + Firebase/Sheets), costs are low, and a raffle keeps participation steady.