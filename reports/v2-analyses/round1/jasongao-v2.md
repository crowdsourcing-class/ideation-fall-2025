# V2 Analysis: AccessWatch

## Project Overview
**Author:** Jason Gao (jasongao)
**One-line pitch:** A lightweight platform where residents report, verify and map accessibility issues with geotagged photos, producing a live, open data layer cities and campuses can act on.

## Quick Viability Score: 23/30

### Score Breakdown (Estimated from Round 1)
- **Problem-Solution Fit (7/10):** Addresses real accessibility gaps in cities like Philadelphia with incomplete 311 reporting. Clear problem with tangible impact.
- **Crowdsourcing Fit (8/10):** Excellent crowdsourcing design - reporting, verification, resolution tracking. Multi-stage workflow with redundancy. Strong verification ledger concept.
- **Technical Feasibility (8/10):** Well-scoped tech stack (Supabase, Firebase, Mapbox free tiers). Realistic budget of $20-40. Clear automation plan (geo-validation, duplicate clustering).

### Strengths
1. **Sophisticated Quality Control:** Two-tier verification system (2+ independent confirmations or 1 + public data match) shows deep understanding of crowdsourcing principles
2. **Clear Value Proposition:** Produces actionable open data (GeoJSON/CSV exports) that cities/campuses can actually use
3. **Realistic Scope:** Focuses on Penn campus + 1-2 neighborhoods for pilot (100-200 users, 300-600 reports)
4. **Strong Prior Work Analysis:** References Project Sidewalk (UW) and understands differentiation (fresh verification vs. historical labeling)
5. **Thoughtful Incentive Design:** Streak counters and "impact counters" inspired by successful past projects

### Weaknesses
1. **Cold Start Problem:** Needs critical mass before valuable; maps look empty without ~300+ reports
2. **Photo Verification Complexity:** EXIF data can be stripped/faked; geo-validation within 20-30m isn't foolproof
3. **Maintenance Burden:** Reports need ongoing updates as issues get fixed - requires sustained engagement
4. **Limited Immediate Reward:** Contributors see impact slowly as cities respond (unlike instant gratification apps)

## Why Was This Dropped?

**Most Likely Reasons:**
1. **Geographic Scope Concerns:** Single-campus focus may feel too narrow for course-wide interest
2. **Government/Institutional Dependencies:** Value depends on city/facilities teams actually using the data
3. **Competition with Established Systems:** 311 apps already exist; incremental improvement may not excite reviewers
4. **Long Feedback Loop:** Takes weeks/months to see real-world fixes, making engagement harder to sustain
5. **Technical Ambition:** Geo-clustering, DBSCAN, duplicate detection - may have seemed too complex for semester scope

## Was This the Right Decision?

**Verdict: QUESTIONABLE - Potential Hidden Gem**

**Arguments for Dropping:**
- Very ambitious technical scope (geospatial validation, duplicate clustering, 311 integration)
- Requires institutional buy-in to demonstrate real impact
- Long time horizon to show value (city response times)
- Crowded space (SeeClickFix, 311 apps, Wheelmap.org)

**Arguments Against Dropping:**
- **Exceptionally well-designed:** Shows mastery of crowdsourcing principles (verification, redundancy, quality control)
- **Clearly scoped MVP:** Pilot on Penn campus is realistic for semester timeline
- **Real social impact:** Accessibility is important and underserved
- **Strong technical plan:** Free-tier infrastructure, realistic budget
- **Differentiates from prior work:** Focus on verification and fix-tracking vs. just labeling

**Hidden Gem Potential:** HIGH

This is one of the strongest dropped projects. The proposal demonstrates sophisticated understanding of:
- Quality control mechanisms
- Aggregation strategies
- Incentive design
- Technical feasibility

The project was likely dropped due to perceived scope/complexity concerns and the long feedback loop to demonstrate impact. However, a focused Penn campus pilot (curb ramps, blocked sidewalks around buildings) could have shown meaningful results within one semester.

**What Could Have Saved It:**
- Emphasize quick wins (campus-only focus, 30-day pilot metrics)
- Partner with Penn Disability Services for immediate institutional user
- Demo with synthetic data showing the interface value
- Focus on verification gamification rather than city response

## Lessons for Future Selection

This case highlights a tension in project selection:
- **Technical sophistication** can be mistaken for over-ambition
- **Long-term impact projects** disadvantaged vs. instant-gratification apps
- **Civic tech** needs clearer path to institutional validation within semester constraints
- **Well-scoped pilots** may still get penalized if bigger vision feels too large

The irony: This project better understands crowdsourcing principles than many that progressed, but may have been penalized for being *too* thoughtful about real-world deployment.
