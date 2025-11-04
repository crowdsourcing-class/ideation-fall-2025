# V2 Analysis: WeTrack

## Project Overview
**Author:** Arriella Mafuta (arriella)
**One-line pitch:** A social accountability platform where students crowd-verify each other's progress toward shared goals.

## Quick Viability Score: 20/30

### Score Breakdown (Estimated from Round 1)
- **Problem-Solution Fit (7/10):** Real student need for accountability and peer motivation. Common pain point.
- **Crowdsourcing Fit (6/10):** Peer verification is crowdsourcing, but within small closed groups (4-6 members), limiting crowd diversity. More social app than true crowdsourcing.
- **Technical Feasibility (7/10):** Reasonable tech approach (Firebase/Convex, Replit). Budget under $100. Simple verification mechanics.

### Strengths
1. **Clear Target Market:** University students with well-defined use cases (studying, exercising, habit building)
2. **Natural Incentives:** Peer pressure and social motivation are powerful, no payment needed
3. **Simple Task Design:** Daily check-ins + quick validation prompts are low-friction
4. **Engagement Hooks:** Streaks, leaderboards, reactions create stickiness
5. **Self-Organizing:** Small groups (4-6) form naturally through existing social circles

### Weaknesses
1. **Not True Crowdsourcing:** Closed friendship circles aren't "crowds" - limited to small trusted groups
2. **Scalability Issues:** Each group is isolated; no cross-group aggregation or emergent insights
3. **Verification Quality:** Friends may fake validations to help each other; two confirmations from buddies isn't robust QC
4. **Crowded Market Space:** Habitica, Strava, Fitbit, BeReal - many competitors already exist
5. **Free-Rider Problem:** What happens when one person stops participating? Group dynamics collapse

### Critical Flaws
- **Small Group Dynamics:** The "crowd" is just 4-6 friends, not diverse anonymous workers
- **No Aggregation Value:** Unlike true crowdsourcing, validations don't create dataset or emergent knowledge
- **Trust vs. Truth:** Peer verification in friendship circles may prioritize support over accuracy
- **Group Dependence:** App only works if ALL members stay engaged; fragile social contract

## Why Was This Dropped?

**Most Likely Reasons:**
1. **Not Crowdsourcing:** More of a social/accountability app than a crowdsourcing project
2. **Limited Technical Challenge:** Simple CRUD app with basic validation - doesn't showcase course concepts
3. **Crowded Market:** Too many existing solutions (Habitica, Strava challenges, accountability apps)
4. **No Aggregation Insight:** Doesn't produce interesting data or emergent crowd wisdom
5. **Group Formation Problem:** Cold start requires pre-existing friend groups

## Was This the Right Decision?

**Verdict: CORRECT DECISION**

**Why This Was Rightly Dropped:**
- **Fundamentally not crowdsourcing:** The core mechanism (peer verification within small friend groups) doesn't leverage crowd diversity, scale, or anonymity
- **No aggregation value:** Unlike true crowdsourcing projects, this doesn't aggregate inputs to create emergent insights
- **Wrong course fit:** Better suited for a social app development course or behavioral psychology study
- **Limited technical depth:** Straightforward social app without crowdsourcing complexity

**What It Gets Right (But Still Shouldn't Progress):**
- Strong understanding of incentive design (intrinsic motivation)
- Clear problem-solution fit
- Realistic technical scope
- Good engagement mechanisms

**The Core Issue:**
WeTrack is a well-designed social accountability app, but it's not a crowdsourcing project. The "crowd" is just your 5 friends. True crowdsourcing requires:
- Large, diverse groups of contributors
- Aggregation mechanisms that produce emergent value
- Quality control across anonymous/semi-anonymous workers
- Data or insights that emerge from crowd inputs

WeTrack has none of these. It's 5 people checking each other's homework - not a crowd solving a problem through collective intelligence.

## Comparison to Progressed Projects

Projects like **alexoh (Campus Event Feed)** also use peer curation, but:
- Open to entire student body (true crowd scale)
- Aggregates inputs to surface popular events (emergent ranking)
- Anonymous voting creates honest signals
- Produces useful dataset (campus event popularity over time)

WeTrack lacks these crowdsourcing fundamentals.

## Lessons for Future Selection

- **Small groups != crowds:** Friend circles don't provide the diversity and scale needed for crowdsourcing
- **Verify course fit first:** Good app ideas may not be good crowdsourcing projects
- **Aggregation is key:** Crowdsourcing should produce emergent value beyond individual contributions
- **Social apps vs. crowdsourcing:** Just because multiple people interact doesn't make it crowdsourcing

## Alternative Framing (If Student Wanted to Pivot)

To make this a true crowdsourcing project:
- **Community Habit Challenge:** 100s of students tracking habits, with cross-verification by strangers
- **Aggregate Insights:** Surface which habits work best for which goals (crowd generates dataset)
- **Pattern Discovery:** Find correlation between verification methods and actual habit success
- **Public Leaderboard:** Open to all students, not closed friend groups

But as proposed, WeTrack is not a crowdsourcing project - correct decision to drop.
