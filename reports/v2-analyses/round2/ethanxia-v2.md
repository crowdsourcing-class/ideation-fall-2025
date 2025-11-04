# V2 Viability Analysis: CrowdScout

**Project:** CrowdScout - TikTok-style platform for crowdsourced sports recruiting

**Round:** 2 (DROPPED)

**Author:** Ethan Xia (ethanxia), Connor Cummings (connorcc)

---

## Viability Score

### 1. Technical Feasibility: 2/5
**Critical Issues:**
- Video hosting and streaming infrastructure (major cost and complexity)
- "For-you" ML recommendation algorithm like TikTok
- Weighted aggregation with credibility scoring
- Real-time video feed with like/dislike system
- ML model to predict "recruitability score"
- Integration with public sports datasets (MaxPreps, NCAA)

**Red Flags:**
- Video platform = complex CDN, storage, encoding, streaming
- Personalized recommendation system = sophisticated ML
- "PyTorch, Spark" mentioned - production ML pipeline is advanced
- Multiple complex systems: video platform + social features + ML ranking

**Reality Check:**
- Video platforms are notoriously difficult to build
- TikTok's algorithm alone is worth billions in R&D
- This is closer to a startup than a course project

### 2. Crowdsourcing Viability: 2/5
**Issues:**
- Two-sided marketplace: need athletes uploading AND scouts/recruiters browsing
- Cold-start problem: platform only valuable with lots of content
- Competing with established platforms (Hudl, MaxPreps, NCSA)
- "At least 10 athletes to continually upload videos" - incredibly low bar suggests lack of realistic planning

**Value Proposition Unclear:**
- Why would athletes use this vs. Hudl (which recruiters already use)?
- Why would scouts trust crowdsourced ratings over their own evaluation?
- General users scrolling through sports highlights - do they care enough to rate accurately?

### 3. Incentive Design: 3/5
**Mixed Approach:**
- Athletes: Exposure and recruitment opportunities (strong intrinsic motivation)
- Scouts: Access to talent (strong intrinsic motivation)
- General users: "Gamification (like TikTok) through leaderboards, points, badges" for scrolling and rating

**Strengths:**
- Athletes and scouts DO have real incentives
- Entertainment value for casual users might work

**Weaknesses:**
- Casual user ratings may not be quality signals recruiters trust
- No payment mentioned for high-quality evaluations
- Risk of popularity contest vs. actual athletic merit

### 4. Scope Appropriateness: 1/5
**Severely Overscoped:**
Core features listed:
1. Video hosting + upload system
2. Like/dislike rating system
3. Skills tagging system
4. Leaderboard dashboard
5. Weighted aggregation algorithm
6. Personalized ML recommendation feed
7. Integration with sports statistics APIs

**Each of these alone is substantial:**
- Video platform with CDN = 3-4 weeks minimum
- Recommendation algorithm = 2-3 weeks
- Credibility-weighted aggregation = 1-2 weeks
- External API integration + data normalization = 1-2 weeks

**Technology stack mentioned:** Python, React, AWS, PyTorch, Spark
- This suggests large-scale data processing and ML training
- Completely unrealistic for 5-week timeline

### 5. Recruitment Strategy: 2/5
**Vague with Some Specifics:**
- "Social media, schools, and sports communities" - generic
- "Student-athletes using the app" - how will you reach them?
- "At least 10 athletes" - absurdly low target that signals no real plan
- "100 users in the first week" as success metric, but no path to achieve it

**Missing:**
- No specific schools or clubs identified
- No partnerships with coaches or athletic departments
- No concrete recruitment channels named
- Competing with established platforms with existing user bases

### 6. Quality Control: 4/5
**Relatively Strong:**
- Verified coaches/scouts given higher weight
- Rater reputation system tracking accuracy over time
- Detection of suspicious rating patterns (coordinated upvoting)
- Blend engagement signals (watch time, completion rate)
- Separate "coach-only" score resistant to gaming
- Statistical outlier detection

**This is actually the strongest part of the proposal** - shows understanding of quality control challenges.

---

## Total Score: 14/30

**Verdict:** STOP AND PIVOT

---

## Why Was It Dropped?

**Speculation based on quality:**

1. **Video Platform Complexity:** Building a video hosting platform alone is a massive undertaking. Storing, encoding, streaming, and serving video at scale requires:
   - CDN infrastructure (expensive)
   - Video encoding pipelines
   - Significant AWS/cloud costs (not "relatively inexpensive")
   - Mobile optimization
   This is startup-level infrastructure, not course project scope.

2. **TikTok-Algorithm Delusion:** The proposal mentions building a "for-you" recommendation algorithm. TikTok's algorithm represents years of ML research and billions in investment. Even a simplified version requires:
   - Large training dataset
   - Feature engineering (watch time, engagement, user preferences)
   - Model training and evaluation infrastructure
   - Real-time inference system
   This is not feasible in 5 weeks.

3. **Competing with Hudl:** The proposal acknowledges Hudl but doesn't adequately address why athletes would switch. Hudl:
   - Is already established with coaches/recruiters
   - Has professional video analysis tools
   - Is used by thousands of schools
   CrowdScout offers "crowd ratings" but doesn't explain why that's better than professional scout evaluation.

4. **Two-Sided Market with No Traction Plan:** Need athletes, scouts, AND casual raters all at once. "At least 10 athletes" is an absurdly low bar that suggests:
   - No real user research
   - No understanding of network effects needed
   - No partnerships with schools or athletic programs

5. **Cost Underestimation:** "Paid pilot on MTurk could be some relatively inexpensive per-video cost" + "Usage is free but content moderation is the biggest cost"
   - Video storage alone could cost hundreds per month at scale
   - AWS costs for ML inference
   - CDN bandwidth costs
   - This blows through any reasonable course budget

---

## Was This the Right Decision?

**YES - Correct to drop.**

**Clear warning signs:**
- 14/30 score = "Stop and Pivot" territory
- The technical complexity alone (video platform + ML) disqualifies this
- No evidence of partnerships or committed athlete users
- Competing directly with well-funded, established platforms
- Cost structure would exceed course budget by 10x

**What would have happened:**
- Week 1-2: Realize video hosting is too expensive/complex
- Week 3: Try to pivot to simpler version (links to YouTube?)
- Week 4: Can't get athletes to upload content
- Week 5: Have a broken prototype with 5 test videos
- Result: Incomplete system, no users, budget exceeded

---

## Hidden Gem Potential?

**YES - Strong underlying concept with fatal execution**

**The Core Insight is Excellent:**
- Recruiting IS opaque and inaccessible for many athletes
- Crowdsourced discovery COULD surface overlooked talent
- Social/entertaining format COULD drive engagement
- Problem is real and impactful

**Why It Could Have Succeeded with Different Approach:**

### Pivot: "Penn IM Sports Highlights"

**Radically Simplified Version:**

1. **No Video Hosting:**
   - Users submit YouTube/Instagram links (no storage costs)
   - Platform just aggregates and ranks links
   - OR: focus on Penn intramural sports (can film in person)

2. **No ML Recommendation Algorithm:**
   - Simple chronological or vote-based sorting
   - Manual curation of "Top 10 Weekly Highlights"
   - Aggregate view counts and engagement from source platforms

3. **Hyperlocal Focus:**
   - Penn intramural/club sports only
   - Target: College athletes trying to make club teams
   - Partner with Penn Athletics or Pottruck Gym
   - 50-100 Penn students as captive audience

4. **Simple Rating System:**
   - Just upvote/downvote (no complex weighting initially)
   - Focus on discovery, not sophisticated ranking
   - Let view counts do heavy lifting

5. **Manual "Scout" Feature:**
   - Penn club team captains = "scouts"
   - They get access to contact info of highly-voted athletes
   - Platform just facilitates discovery, not algorithmic matching

**This version could score 20-22/30:**
- Tech feasibility: 4/5 (simple CRUD + link aggregation)
- Viability: 3/5 (Penn IM sports = specific community)
- Incentives: 4/5 (club team recruitment is real motivation)
- Scope: 4/5 (achievable in 5 weeks)
- Recruitment: 3/5 (specific Penn communities)
- QC: 3/5 (simpler system, less critical)

---

## Key Lessons

### What Killed This Project:
1. **Video Platform Hubris:** Underestimated complexity and cost of video infrastructure by orders of magnitude
2. **Algorithm Fantasy:** Thinking a "TikTok-style algorithm" is buildable in 5 weeks
3. **Wrong Competition:** Competing with Hudl, a well-funded sports tech company
4. **No Wedge:** No clear reason for first users to switch from existing solutions

### What Could Have Saved It:
1. **Radical Descope:** Links instead of hosted videos, simple voting instead of ML
2. **Hyperlocal Start:** Penn-only, IM sports, club team recruitment
3. **Avoid Mature Markets:** Don't compete with Hudl; serve an underserved niche
4. **Partner for Distribution:** Work with Penn Athletics or Pottruck Gym for built-in audience

---

## Summary

CrowdScout had a genuinely compelling core idea - democratizing sports recruiting through crowdsourced evaluation. The problem is real, the market is large, and the social/entertainment angle could drive engagement.

However, the execution plan was completely infeasible. Building a video platform with TikTok-style recommendations is a multi-million dollar, multi-year endeavor. The team fundamentally misunderstood the technical complexity and cost structure.

**The right decision was to drop it** given the proposed approach. A 14/30 score signals fatal flaws in technical feasibility and scope.

**Hidden gem potential: HIGH.** With a 90% descope focused on:
- Link aggregation instead of video hosting
- Simple voting instead of ML algorithms
- Penn-specific niche (IM sports) instead of all recruiting
- Partner with Penn Athletics for distribution

...this could have been a strong B+/A- project. The idea itself is good; the execution plan was a fantasy.

**Bottom Line:** Great problem, fatal overengineering. Needed to build a "MVP" (minimum viable product), not a "TikTok for recruiting."
