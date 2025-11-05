# V2 Viability Analysis: TerraTruth (Round 2 - DROPPED)

## Project Summary
**TerraTruth** - A web platform connecting NGOs with volunteers to analyze satellite imagery for humanitarian/environmental monitoring

**Authors:** Alexander Mehta (amehta26), Brandon Yan (bdonyan)

---

## Viability Score Assessment

### 1. Technical Feasibility: 2/5
**Score: Very Risky**
- Satellite imagery processing and GIS data handling
- PostGIS database extension for geographic coordinates
- Complex data pipeline: image serving, annotation, aggregation
- Partner data portal with API/export functionality
- Progressive training module with gold standards
- **Red flags:** GIS/geospatial is explicitly listed in rubric as very risky
- Even without ML, satellite image handling is complex specialty domain

### 2. Crowdsourcing Viability: 2/5
**Score: Weak Value**
- Depends on partnerships with NGOs (Amnesty, Greenpeace, Doctors Without Borders) that don't exist yet
- "If you build it, they will come" for volunteer analysts
- Value is entirely altruistic (no personal benefit)
- Competes with existing volunteer platforms (Zooniverse, Amnesty Decoders)
- Requires passionate volunteers willing to do tedious image analysis

### 3. Incentive Design: 3/5
**Score: Acceptable**
- Intrinsic motivation (contributing to humanitarian causes)
- Gamification: badges, leaderboards, "leveling up"
- Impact visibility dashboard showing how data was used
- Community forum for engagement
- Task time: Likely 5-15 minutes per image depending on complexity
- **Decent match for motivated volunteers**, but no fallback if altruism doesn't work

### 4. Scope Appropriateness: 1/5
**Score: Fantasy**
- 7 major features including mission-based system, reputation engine, weighted aggregation, impact dashboard, sensitive content filtering, progressive training, AND partner data portal
- Building a full non-profit platform infrastructure in 5 weeks
- Requires partnerships that take months to establish
- GIS data pipeline alone is 3-4 weeks
- This is a startup/organization, not a class project

### 5. Recruitment Strategy: 1/5
**Score: Magic Thinking**
- "Recruited through partner non-profits" - which don't exist yet
- "University groups, social media campaigns"
- "Online volunteer portals" - which ones? How?
- Needs 100s of active workers (states "100-300 active monthly volunteers within first year")
- No evidence of testing recruitment or securing any commitments
- Classic "build the platform and hope partners/volunteers appear"

### 6. Quality Control: 5/5
**Score: Multi-layered**
- Gold standard images with known answers
- Weighted aggregation by user accuracy scores
- Progressive training (users must pass before contributing to live data)
- Reputation system with skill levels (Recruit, Analyst, Expert)
- Statistical outlier detection
- Multiple workers per image (n=3-5)
- **Ironically, this is the BEST QC design of any dropped project**

**TOTAL SCORE: 14/30**

---

## Verdict: STOP AND PIVOT

This falls in the 10-14 range: "Project is not feasible as described. Needs complete rethink."

---

## Why Was It Dropped?

**Likely reasons:**

1. **Partnership dependency** - Entire project requires NGO partnerships that take months to secure
2. **Geospatial/GIS complexity** - Rubric explicitly flags this as a red flag for 5-week projects
3. **Massive overscoping** - Building a permanent platform infrastructure for multiple organizations
4. **No path to first user** - Needs both NGO partners AND volunteer analysts, neither are secured
5. **Too ambitious** - This is a non-profit organization/startup, not a class project
6. **Cost uncertainty** - States "free imagery via non-profit agreements" but these don't exist

**Evidence from proposal:**
- "Permanent, scalable platform that serves multiple organizations"
- Technical stack includes PostGIS (specialized GIS database)
- Success metric: "At least 3 partner non-profits publicly citing data" within first year
- Challenge #1 acknowledges imagery sourcing is a major problem
- "Start by focusing on publicly available data to BUILD THE PLATFORM and USER BASE. Use this demonstrated capability... to THEN secure formal partnerships"
  - This is a multi-year roadmap, not a 5-week project

---

## Was This the Right Decision?

**ABSOLUTELY YES - This was correctly dropped.**

**Reasoning:**
- Scores only 14/30, placing it firmly in "Stop and Pivot" territory
- The rubric states for 10-14: "Project is not feasible as described. Needs complete rethink."
- Two critical dimensions score only 1/5 (Scope, Recruitment) - these are structural impossibilities
- Even the strongest dimension (QC: 5/5) can't save a project with no viable path to launch
- The team explicitly describes this as a "permanent platform" and has a "first year" roadmap

**What makes this especially unfeasible:**
1. GIS/satellite is explicitly a red flag in the rubric
2. Partnership-dependent when no partnerships exist
3. Chicken-egg: need platform to attract partners, need partners to justify building platform
4. Competes with established platforms (Zooniverse, Amnesty Decoders) without differentiation

**The team even KNOWS it's a long-term project:**
- Their mitigation for Challenge #1 is: "BUILD THE PLATFORM first, THEN secure partnerships later"
- This is backwards for a class project - you need users/partners FIRST to validate, then build

---

## Hidden Gem Potential?

**LOW - This is a startup idea, not a class project, and unlikely to succeed even as a startup**

**Why NOT a hidden gem:**

1. **Market already served:**
   - Zooniverse exists and works well for citizen science
   - Amnesty Decoders already did satellite analysis (and was discontinued)
   - If Amnesty couldn't sustain it internally, a student project certainly can't

2. **Structural impossibility:**
   - Requires long-term partnerships that take months to establish
   - NGOs need reliability and trust - won't partner with unproven student project
   - Satellite imagery licensing is complex and expensive
   - Even "free" public data (Sentinel, Landsat) requires specialized expertise to use

3. **Execution wouldn't fix it:**
   - This isn't a problem of bad execution or unclear vision
   - The vision is TOO clear and TOO ambitious
   - It's fundamentally mismatched to the constraints (5 weeks, student project, limited resources)

**What MIGHT have made it viable (but still very weak):**

1. **Extreme descoping to proof-of-concept:**
   - Analyze ONE specific crisis with ONE specific task
   - Use 10 pre-downloaded images (no pipeline)
   - Manual task distribution (no fancy system)
   - Build simple annotation interface only
   - Recruit 20 friends to test
   - Prove the concept, don't build the platform

2. **Partner-first approach:**
   - Actually secure commitment from ONE NGO or professor BEFORE building
   - Have them provide data and validation
   - Build only what they specifically need
   - Turns it from speculation into a commissioned tool

3. **Pivot away from satellite:**
   - Same concept (volunteers analyzing images for humanitarian orgs)
   - But use accessible imagery: photos from news sites, social media
   - Example: "Identify flood damage from Instagram posts during disasters"
   - Eliminates GIS complexity entirely

**Even with these changes:** Would still score maybe 18-20/30 (Needs Major Revision / Weak GO)

**Fundamental issue:** The team fell in love with a VISION (permanent humanitarian platform) rather than a PROJECT (prove a concept in 5 weeks). Their proposal reads like a grant application or startup pitch deck, not a class project plan.

**Best evidence this was wrong for the class:**
- They describe it as different from existing projects because it's a "permanent, scalable platform"
- Success metrics include "within the first year"
- Their challenges section assumes months-long partnership development

**The irony:** This is actually the most thoughtfully designed project of the dropped ones (excellent QC, clear vision, well-researched prior work). But thoughtful design doesn't make an impossible project possible. They designed a Ferrari when they needed to build a bicycle.

**Bottom line:** Not a hidden gem - it's a miscategorization. This is a valid startup idea or graduate thesis, not a crowdsourcing class project. The right decision was to drop it or force a complete pivot to something achievable in 5 weeks.
