# TripTuner - Project Viability Analysis (V2)

**Project**: TripTuner
**Authors**: Jevin Ta (jevinta), Nikki Liu (nikkiliu), Julia Zhuo (juzhuo), Arushi Agarwal (arushiga), Liana Veerasamy (lianav), Sadia Rahman (rsadia)
**Analysis Date**: 2025-11-02
**Proposal Version**: Round 3

---

## VIABILITY SCORE BREAKDOWN

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| **1. Technical Feasibility** | 4/5 | React/Next.js + Firebase stack is well-proven for this use case. Structured submission form, voting interface, and weighted aggregation are straightforward CRUD + basic math. OpenAI API integration adds slight risk but manageable. Loss of 1 point for AI features (summarization, moderation) and potential NLP duplicate detection complexity. |
| **2. Crowdsourcing Viability** | 3/5 | Travel enthusiasts exist and Reddit travel communities are real. However, competing with abundant free alternatives (TripAdvisor, Google Travel, travel blogs). Value proposition of "editable community itineraries" is novel but unvalidated. Cold-start problem: need itineraries to attract users, need users to contribute itineraries. |
| **3. Incentive Design** | 2/5 | Fatal mismatch: asking for CREATION (15-30 min to craft detailed itinerary) but offering BADGES and leaderboard positions. Budget allocates $75 for 250 votes ($0.05/vote) but expects ~50 itineraries for free. Intrinsic motivation ("share travel stories") untested and competing with Instagram, travel blogs where people already share. |
| **4. Scope Appropriateness** | 3/5 | 10 listed features, several are substantial (NLP duplicate detection, AI summarization, visualization dashboard). Core loop (submit → vote → rank) is 2-week build, but AI/NLP features add risk. Achievable if team cuts 3-4 "nice-to-have" features, but proposal treats all as essential. |
| **5. Recruitment Strategy** | 2/5 | Generic "Reddit communities, Penn student forums, Instagram travel accounts" without specific subreddits, accounts, or commitments. No evidence of outreach testing or moderator approval. Backup mentions MTurk but budget only covers voting tasks, not itinerary creation. Target of 100-200 workers unrealistic without payment for creative work. |
| **6. Quality Control** | 4/5 | Strong QC section: 6 mechanisms specified including majority voting (≥5 votes per itinerary), reputation system, outlier detection (budgets 2σ from mean), AI moderation (Perspective API). Appropriate for subjective creative tasks. Could be more specific about consensus thresholds but generally well-thought-out. |
| **TOTAL** | **18/30** | **Needs Major Revision** |

---

## EXECUTIVE SUMMARY

TripTuner is a well-structured travel itinerary crowdsourcing platform with appropriate technical scope and sophisticated quality control mechanisms. However, the project suffers from a **critical incentive design flaw**: it asks strangers to spend 15-30 minutes creating detailed travel itineraries for free, offering only badges and leaderboard recognition in return. The budget allocates funds for low-effort voting tasks ($0.05 per vote) but expects high-effort creative contributions (full itineraries) with no payment. This fundamental mismatch between task difficulty and compensation, combined with vague recruitment strategy and competition from existing travel platforms, puts the project at high risk of failing to attract meaningful participation. The team has three viable paths forward: pay for itinerary creation, dramatically reduce task burden, or plan to seed content themselves.

---

## DETAILED ASSESSMENT

### 1. Technical Feasibility (4/5)

**Strengths**:
- React/Next.js + Node.js/Express + Firebase Firestore is a proven, well-documented stack
- Core CRUD operations (submit itinerary form, display list, voting interface) are standard web development
- Weighted aggregation formula (0.6 votes + 0.2 feedback + 0.2 completeness) is simple arithmetic
- Firebase hosting + Vercel deployment is straightforward and well-supported
- Tag-based filtering and visualization dashboard (D3.js/Chart.js) are moderate complexity but achievable

**Concerns**:
- **OpenAI API integration** for summarization and moderation adds external dependency and cost (though probably <$20 for pilot)
- **NLP duplicate detection** mentioned but not detailed—if using embeddings or semantic similarity, this is non-trivial; if using simple string matching, easier but less effective
- **10 features listed**, several substantial:
  1. Itinerary submission portal (1 week: structured form with validation)
  2. Voting & feedback system (1 week: interface + database + aggregation)
  3. Editable suggestions (1 week: UI for proposing swaps + conflict resolution logic)
  4. Ranking engine (0.5 week: weighted formula implementation)
  5. Tag-based filtering (0.5 week: query logic + UI)
  6. Local tips hub (0.5 week: separate content type + display)
  7. Leaderboard & gamification (0.5 week: points tracking + display)
  8. Visualization dashboard (1 week: data aggregation + D3.js charts)
  9. Duplicate detection (1 week if NLP-based, 0.5 week if simple)
  10. AI summarization (0.5 week: API integration + prompt engineering)

**Total: ~7-8 weeks of work if all features built**

**Realistic Core Loop**: Submit form → voting interface → basic ranking → display results = 2-3 weeks if team is focused

**Technical Risks**:
- "Editable suggestions" feature is ambiguous—how do conflicting edits get resolved? Requires version control or approval workflow.
- NLP duplicate detection may be premature optimization—manual review or simple title matching may suffice for pilot
- Visualization dashboard is nice-to-have but not essential for validating crowdsourcing concept

**Verdict**: Technically feasible if team descopes to core loop first (submit → vote → rank → display) and treats AI/NLP/visualization as optional enhancements. Current feature list is 2x what's needed for validation but not impossible if rigorously prioritized.

---

### 2. Crowdsourcing Viability (3/5)

**Strengths**:
- Travel planning is a real problem—people do struggle with itinerary design and information overload
- Reddit travel communities (r/travel, r/solotravel) are active and genuine sources of travel enthusiasts
- "Editable, community-curated plans" offers differentiation from static review sites
- Travel content naturally inspires sharing (people like talking about their trips)

**Concerns**:

**Saturated market**:
- TripAdvisor, Google Travel, Lonely Planet, WikiVoyage already aggregate travel info
- Travel blogs and YouTube vlogs provide detailed itineraries for free
- Reddit itself has thousands of travel itinerary posts—why move to a new platform?
- Instagram and TikTok serve as existing channels for travel sharing with better social feedback

**Value proposition unclear**:
- What problem does TripTuner solve that Googling "[destination] itinerary reddit" doesn't?
- "Editable suggestions" feature is mentioned but not central to pitch—this could be unique value but underexplored
- End users (travelers) get existing free content; contributors get badges instead of the Instagram likes/blog traffic they already receive elsewhere

**Cold-start problem**:
- Platform is only useful with diverse itinerary library (need 20-30 per destination to show variety)
- But contributors won't join an empty platform
- Proposal mentions "seeding" ("post calls to action on Reddit") but no concrete seeding plan (will team create initial itineraries?)

**Target audience vague**:
- "Travelers seeking realistic, crowd-curated itineraries" is broad
- Are these budget backpackers? Luxury travelers? Families? Solo travelers?
- Different personas have very different needs (3-day Paris with kids ≠ 3-day Paris solo)

**No validation evidence**:
- No user interviews mentioned
- No testing whether travelers actually want community-editable itineraries vs. reading multiple static examples
- No proof that travel enthusiasts would switch from Reddit/blogs to a new platform

**Verdict**: Viable in theory (people do plan trips and share travel stories), but facing steep competition from established platforms and unclear differentiation. Success depends entirely on either (a) significantly better user experience than alternatives or (b) capturing a specific niche community. Neither is demonstrated in proposal.

---

### 3. Incentive Design (2/5)

**Task Analysis**:

**Primary Task (Itinerary Creation)**:
- Research or recall a past trip
- Structure into day-by-day plan
- Estimate costs for activities, food, accommodation
- Write descriptions for 5-10 activities/locations
- Add tags (budget, duration, themes)
- **Estimated time: 15-30 minutes** (20+ minutes for most people)

**Secondary Task (Voting)**:
- Read an itinerary (2-3 minutes)
- Rate on realism, value, fun (30 seconds)
- Optional: Write feedback comment (1-2 minutes)
- **Estimated time: 3-5 minutes per itinerary**

**Tertiary Task (Editable Suggestions)**:
- Read itinerary, identify improvement
- Propose specific swap or reorder
- **Estimated time: 5-10 minutes**

---

**Stated Incentives**:
- Intrinsic motivation: "share travel stories"
- Social recognition: leaderboards, badges (e.g., "Master Trip Designer")
- Gamification: ranking titles, points system
- Emotional: "helping fellow travelers"

**Budget**: $75-100 total
- $0.05 per vote × 250 votes = $12.50
- $0.50 per worker for ~10 votes = estimated for voters only
- **$0 for itinerary creation**

---

**Why This Is 2/5 (Serious Mismatch)**:

According to the rubric's incentive formula:
```
If (Task Time × Boredom Level) > (Incentive Value), then you have a problem.
```

- **Itinerary creation**: 20 min × moderate boredom (structured data entry, cost research) >> badge value
- Rubric guideline: **"Task > 10 min: MUST pay or have captive audience"**
- Rubric guideline: **"Creative work (30 min): Requires ownership/showcase value OR payment"**

**Problems**:

1. **Budget backwards**: Paying for EASY task (voting) but expecting FREE labor for HARD task (creation)
   - Should be reversed: Pay $2-5 per itinerary, get votes for free or cheap
   - Current budget affords ~15-25 paid itineraries if reallocated

2. **Weak intrinsic motivation**:
   - "Share travel stories" — people already do this on Instagram (with likes), blogs (with traffic), Reddit (with karma)
   - TripTuner offers badges, which have no established social value outside the platform
   - No showcasing value (unlike blog portfolio or Instagram feed)
   - No ownership (unlike personal blog where you control brand and monetization)

3. **Gamification without community**:
   - Badges and leaderboards work when there's an existing community to compete within
   - For new platform, "you're #1 of 5 contributors" feels hollow, not rewarding
   - Reddit karma is valuable because millions of users see it; TripTuner badges have no audience

4. **Comparison to successful crowdsourced content**:
   - Wikipedia: Contributors get expertise demonstration, ideological alignment ("free knowledge"), reputation in scholarly community
   - Stack Overflow: Contributors get professional reputation, recruitment exposure, problem-solving satisfaction
   - YouTube: Creators get ad revenue, subscriber base, potential career
   - TripTuner: Contributors get... a "Master Trip Designer" badge on a platform their friends don't use

5. **Task-reward mismatch examples**:
   | Platform | Task | Time | Reward | Match? |
   |----------|------|------|--------|--------|
   | Hot or Not | Click rating | 5 sec | Fun, curiosity | ✅ Great |
   | reCAPTCHA | Solve challenge | 10 sec | Access to site | ✅ Perfect |
   | MTurk | Data entry | 2 min | $0.10 | ✅ Fair |
   | Wikipedia | Write article | 30 min | Reputation, altruism | ✅ Good (for motivated users) |
   | TripTuner | Write itinerary | 20 min | Badge | ❌ **Massive mismatch** |

**Comparison to V1 Feedback**: V1 identified this as "fatal flaw." Round 3 did not address it—incentive design is unchanged.

---

**Viable Alternatives**:

The team has **three paths to fix this**:

**Path 1: Pay for Creation**
- Reallocate budget: $3-5 per itinerary
- $75-100 budget → 15-25 quality itineraries (enough for 3-5 destinations)
- Get votes organically (easier task, students might do for fun) or pay $0.05/vote as planned
- This matches task difficulty to compensation

**Path 2: Reduce Task Burden**
- Don't ask for full itineraries; ask for single activity recommendations
- "What's your favorite thing to do in [city]?" = 2-minute task
- Aggregate 20-30 single recommendations into crowdsourced "best activities" list
- Much lighter lift → gamification becomes viable
- Could still build to full itineraries later if traction proves out

**Path 3: Team Seeds Content**
- Accept that team + friends will create initial 10-20 itineraries
- Use crowdsourcing for voting/ranking/refinement only
- Treat creation as "content curation by team," crowdsourcing as "validation by users"
- Honest about scope but still demonstrates aggregation principles

**Verdict**: Current incentive design is fatally flawed for 100-200 unpaid itinerary contributors. Team must choose one of the three alternatives above or accept that participation will be minimal (<20 itineraries from friends/teammates).

---

### 4. Scope Appropriateness (3/5)

**Feature Count**: 10 features listed (see Technical Feasibility section for breakdown)

**Core Loop Test**: "Could you build working demo of CORE loop in 2 weeks?"
- Core loop = Submit itinerary → Others vote → See ranked results
- Week 1: Submission form with validation + database
- Week 2: Voting interface + basic aggregation + results display
- Answer: **Yes, if nothing else is built**

**Manual Simulation Test**: "Could you manually simulate before building?"
- Yes—team could create 10 itineraries in Google Docs, share with 20 friends to vote/comment, aggregate results in spreadsheet
- This would test value proposition before writing code
- **Proposal does not mention piloting or manual testing**—goes straight to platform development

**Must-Have Features Test**: "Can you name exactly 3-4 must-have features?"
- Proposal lists 10 features, none explicitly marked as optional
- Realistic must-haves:
  1. ✅ Submission portal
  2. ✅ Voting system
  3. ✅ Ranking display
  4. ✅ Basic filtering (by destination/theme)

- Nice-to-have (should be cut):
  1. ❌ Editable suggestions (complex conflict resolution)
  2. ❌ AI summarization (premature optimization)
  3. ❌ Duplicate detection via NLP (manual review sufficient for pilot)
  4. ❌ Visualization dashboard (analytics not needed for validation)
  5. ❌ Open API integration (mentioned under tech stack but not core)
  6. ❌ Local tips hub (separate feature; distracts from itineraries)

**Scope Comparison to Similar Projects**:
- V1 mentioned "Fun Facts" (NETS 2130 past project) as inspiration
- Fun Facts likely had simpler scope: submit fact → vote → rank
- TripTuner adds structured itinerary form, budget tracking, editable suggestions, AI features—significantly more complex than inspiration

**Timeline Provided**:
- Week 1-2: Design UI, set up Firebase and database
- Week 3-4: Develop submission form and voting system
- Week 5-6: Pilot launch with 3 destinations; collect votes and feedback
- Week 7-8: Analyze data, refine ranking algorithm, add visualizations

**Assessment of Timeline**:
- Weeks 1-2: Reasonable for basic setup
- Weeks 3-4: Tight for both submission AND voting systems with validation
- Weeks 5-6: "Pilot launch" assumes working platform by week 5—risky if weeks 3-4 have delays
- Weeks 7-8: Probably outside course timeline (most course projects are 5-6 weeks)
- No buffer for recruitment challenges or technical blockers

**Verdict**: Achievable if team ruthlessly prioritizes core loop and cuts 4-5 "nice-to-have" features. Current scope is 1.5-2x what's needed for validation. Risk of feature creep is high because team hasn't identified must-haves vs. nice-to-haves.

---

### 5. Recruitment Strategy (2/5)

**Stated Strategy**:
- Reddit communities (r/travel, r/solotravel)
- Penn student forums
- Instagram travel accounts
- Volunteer networks

**Scale Requirements**:
- Minimum: 100 workers
- Target: 200 workers for 5 destinations
- Scalable to: >1,000 users via social media promotion

**Backup**: "Use MTurk for initial pilot votes"

---

**Why This Is 2/5 (Vague Hope)**:

**Specificity Test** (from rubric): "Can you NAME the exact groups/places?"
- ❌ r/travel and r/solotravel named, but no evidence of:
  - Reading subreddit rules (many ban promotional posts)
  - Getting moderator approval
  - Testing user interest with sample post
- ❌ "Penn student forums" not specified (which forums? GroupMe? Piazza? Facebook groups?)
- ❌ "Instagram travel accounts" not specified (whose accounts? influencers you'll partner with? or hoping for viral discovery?)
- ❌ "Volunteer networks" completely vague

**Testing**: "Have you TESTED recruitment?"
- ❌ No evidence of posting anywhere
- ❌ No user interviews to gauge interest
- ❌ No outreach to travel communities to see if they'd participate

**Cold-Start Planning**: "Can you seed it yourself?"
- 🟡 Backup mentions MTurk, which is good
- ❌ But MTurk budget only covers voting ($12.50 for 250 votes), not itinerary creation
- ❌ No mention of team creating seed itineraries themselves

**Realistic Reddit Strategy**:
- r/travel has 5.3M members but STRICT rules against self-promotion
- Posting "Check out my new travel planning site!" will likely get removed/banned
- More viable: "I'm a Penn student researching travel planning—would you fill out this itinerary form for my class project?" (framed as research, not product promotion)
- Even then, expect 0.01-0.1% engagement (5-50 people from 5M members, if post is well-received)
- Organic Reddit posts take time to gain traction; may not happen within 5-week window

**Penn Students**:
- More accessible but are Penn students your target users?
- Most Penn students probably haven't traveled enough to create detailed destination itineraries
- Could work for "Spring Break 2025" or "Study Abroad Advice" itineraries if narrowly focused

**Backup Plan Assessment**:
- MTurk is smart backup for voting tasks
- But doesn't solve creation problem (MTurk workers will create low-quality itineraries for $0.05—need to pay $2-5 for quality)
- If entire budget goes to MTurk itinerary creation: $75 ÷ $3 = 25 itineraries (viable but leaves no budget for voting)

**Concrete Strategy Missing**:
- ✅ Good: "Reddit communities" named specifically
- ❌ Bad: No evidence of testing, moderator approval, or community buy-in
- ❌ Bad: No plan for recruiting first 10 contributors (friends? teammates? classmates?)
- ❌ Bad: No forcing function (course requirement, research study participation, partnership with travel club)

**Comparison to Strong Recruitment** (rubric 5/5 example):
- Weak: "Reddit communities, social media campaigns" (TripTuner's approach)
- Strong: "r/travel moderators approved my post (screenshot attached), Penn Travel Club agreed to promote to 150 members, team will create 10 seed itineraries"

**Verdict**: Recruitment is better than "users will find us" magical thinking (has specific channels named), but still vague and untested. No evidence of community access, no commitments secured, no proof of demand. Will likely struggle to recruit 100-200 unpaid itinerary creators.

---

### 6. Quality Control (4/5)

**Strengths**:
This is the strongest section of the proposal—team has thought systematically about QC.

**Mechanisms Specified**:
1. ✅ **Majority voting**: ≥5 votes per itinerary required for publication
2. ✅ **Expert review (optional)**: Top entries spot-checked by experienced travelers
3. ✅ **Reputation system**: Points and badges build trust over time; high-reputation users' votes weighted more heavily
4. ✅ **Statistical outlier detection**: Budgets 2 standard deviations from mean get flagged
5. ✅ **AI moderation**: Perspective API filters spam and offensive text
6. ✅ **Redundancy**: Multiple voters per itinerary ensure consensus

**Aggregation Formula**:
```
Score = 0.6 × votes + 0.2 × feedback_sentiment + 0.2 × completeness
```
- Reasonable weighting prioritizing crowd votes
- Feedback sentiment requires NLP (OpenAI API likely) but doable
- Completeness is objective (do all required fields have data?)

**Handling Low-Quality Work**:
- Flagged itineraries temporarily hidden for review
- Repeat low-quality contributors lose visibility points
- Appropriate progressive consequences

**Appropriate for Task Type**:
- QC for subjective creative tasks (itineraries) is hard—no "gold standard"
- Relying on consensus + reputation is correct approach
- Statistical outlier detection (budget anomalies) is smart catch for fake/joke entries

---

**Why Not 5/5**:

**Missing Specifics**:
1. **Consensus threshold**: What % agreement needed to publish? (e.g., "4 of 5 voters must rate ≥3 stars")
2. **Feedback sentiment**: How is this quantified? (OpenAI sentiment score? Count of positive/negative words?)
3. **Completeness definition**: What fields are required? (budget + 3 activities? budget + full day-by-day?)
4. **Expert review logistics**: Who are the "experienced travelers"? How are they recruited? Is this manual or automated?
5. **Outlier handling**: What happens to flagged entries? (Manual review? Auto-reject? Re-task for verification?)

**Potential Overengineering**:
- For pilot with 20-50 itineraries, manual team review might be faster/simpler than building full automated QC
- AI moderation (Perspective API) is nice-to-have but may be overkill for small pilot (can manually moderate 50 itineraries)
- Reputation system requires multiple contributions per user to work—won't be effective until later stages

**Risk of Spam Not Addressed**:
- What stops someone from submitting 20 joke itineraries? (Rate limiting by IP? Account verification?)
- What if coordinated group of friends upvotes each other's itineraries? (Graph analysis to detect voting rings? Not mentioned.)

**Recommendations**:
- Specify consensus thresholds and completeness requirements
- Start with manual review for first 30-50 itineraries, add automation only if scaling beyond course scope
- Add basic rate limiting (max 5 submissions per user per day)

**Verdict**: Strong QC foundation with 6 mechanisms and clear aggregation formula. Loses 1 point for missing operational specifics and potential overengineering for pilot scale. Overall, this is the most polished aspect of the proposal.

---

## RISK ANALYSIS

### Top 3 Risks & Mitigations

#### Risk 1: Zero Itinerary Contributions Due to Weak Incentives (Critical, ~85% probability)
**Impact**: Team builds functional platform but fails to recruit itinerary creators. Demo shows working voting/ranking system but only 5-10 itineraries (created by team members/friends). Crowdsourcing validation fails because the hard part (creation) wasn't adequately incentivized.

**Why It's Critical**:
- 20-30 minutes is too long for unpaid task with weak intrinsic motivation
- Badges have no value outside platform (not like Reddit karma with established social currency)
- Travelers already share on Instagram/blogs where they get likes/traffic
- Cold-start problem: empty platform doesn't attract contributors

**Mitigation Options**:

**Option A: Reallocate Budget to Pay for Creation** (Recommended)
- Change budget: $75-100 for itinerary creation, votes are free/cheap
- Pay $3-5 per quality itinerary on MTurk/Prolific
- Set clear quality bar (must include budget, 5+ activities, realistic timing)
- $75 → 15-25 itineraries covering 3-5 destinations
- Use peer review from course classmates for voting (free labor)
- **This is the most straightforward fix**

**Option B: Dramatically Reduce Task Burden**
- Pivot from "full itinerary" to "single activity recommendation"
- New task: "What's the best thing you did in [city]?" (2-minute response)
- Collect 20-30 single activities per destination
- Aggregate into "crowd-favorite activities" list
- Much lighter task (2 min vs. 20 min) → gamification becomes viable
- Still demonstrates aggregation and ranking principles
- **This validates core crowdsourcing concept with lighter lift**

**Option C: Team Seeds All Content**
- Accept that team (6 members) will create all initial itineraries
- 6 people × 3 itineraries each = 18 itineraries (enough for demo)
- Use crowdsourcing only for voting and feedback refinement
- Frame project as "content created by team, validated by crowd"
- Reduces scope but still demonstrates aggregation/QC
- **This is most honest about what's achievable**

**Option D: Narrow to Captive Audience**
- Partner with specific Penn course or club
- Example: "NETS 2130 students create itineraries for class credit"
- Example: "Penn Travel Club members contribute in exchange for featured placement"
- Requires securing partnership THIS WEEK
- **This solves recruitment but requires immediate action**

**Backup**: If no mitigation chosen and recruitment fails (likely), team should:
- Pivot to voting/ranking existing itineraries (scrape TripAdvisor, travel blogs, Reddit posts)
- Test whether crowd ranking improves upon algorithmic ranking (upvotes, recency)
- This salvages the aggregation concept without requiring creation

**Consequence if Unaddressed**: Week 4-5 panic when team realizes nobody is contributing. Demo shows 8-12 itineraries (mostly team + close friends). Platform works technically but crowdsourcing validation is weak. Grade: B/B- for technical execution but insufficient crowd participation.

---

#### Risk 2: Reddit Recruitment Fails or Gets Banned (High, ~70% probability)
**Impact**: Team posts to r/travel or r/solotravel but gets removed by moderators for self-promotion, or post gets buried and receives minimal engagement. No organic contributor pipeline materializes.

**Why It's High Risk**:
- Most subreddits have strict rules against promotional posts
- Even "research project" framing gets mixed reception (users are tired of surveys)
- Reddit posts need immediate engagement (first hour) to gain visibility—can't guarantee this
- Timing matters (posting during US overnight hours gets less traction)

**Mitigation**:

**Test Reddit Receptivity NOW**:
- Post simple question this week: "Would you be interested in a community-curated travel itinerary platform?"
- Gauge response before investing in full platform build
- If response is tepid (<50 upvotes, <20 comments), Reddit may not be viable channel
- **This is critical early validation**

**Get Moderator Approval**:
- Message r/travel and r/solotravel mods explaining project (student research, nonprofit, helping community)
- Ask permission to post; some mods will allow educational/research projects
- If mods say no, pivot to other channels immediately

**Diversify Recruitment Channels**:
- Don't rely solely on Reddit
- Penn-specific: NETS 2130 classmates, study abroad returnees, Penn Travel Club
- Facebook: Travel groups, study abroad groups, budget travel communities
- Discord: Travel planning servers, digital nomad communities
- **Have 3-4 channels, not just Reddit**

**Seed Content First**:
- Don't launch with empty platform
- Team creates 10-15 seed itineraries BEFORE public recruitment
- When users arrive, they see populated platform and are more likely to contribute
- **This solves cold-start problem**

**Backup**: If Reddit fails, reallocate to MTurk ($75 for 15-25 paid itineraries) and get voting from Penn students (easier ask than creation).

---

#### Risk 3: Scope Creep Delays Core Loop, Insufficient Testing Time (Medium, ~60% probability)
**Impact**: Team spends weeks 1-4 building all 10 features (AI summarization, NLP duplicate detection, visualization dashboard, editable suggestions). Working MVP doesn't exist until week 5, leaving no time for user testing and iteration. Demo shows feature-rich platform with minimal actual usage data.

**Why It's Medium Risk**:
- Proposal lists 10 features without prioritization
- "AI summarization," "duplicate detection," and "visualization dashboard" are technical rabbit holes
- Team may feel pressure to deliver everything promised in proposal
- Feedback cycles (test → learn → iterate) require time, which gets compressed if build takes 4 weeks

**Mitigation**:

**Ruthless Prioritization Week 1**:
- Meet as team and force-rank all 10 features
- Identify "Must-Have for Demo" (3-4 features) vs. "Nice-to-Have" (cut these)
- **Must-Haves**: Submit form, voting interface, ranking display, basic filtering
- **Nice-to-Haves**: AI summarization, NLP duplicates, viz dashboard, editable suggestions, local tips hub

**Build Horizontal Slice First**:
- Week 1-2: End-to-end core loop (submit → store → display → vote → rank)
- Week 3: Soft launch with 5-10 seed itineraries; test with 20-30 voters
- Week 4: Analyze feedback; add 1-2 most-requested features
- Week 5: Final data collection and polish
- **This ensures working system by week 3, leaving time to pivot**

**Manual Processes Are OK**:
- AI summarization? Team manually writes 2-sentence summary for each itinerary (10 min per itinerary × 20 itineraries = 3 hours)
- NLP duplicate detection? Team manually reviews submissions (5 min per review)
- Visualization dashboard? Generate charts in Google Sheets and screenshot for demo
- **Don't automate what can be done manually for pilot scale**

**Set Weekly Milestones**:
- Week 1: Working submission form (can create and store itinerary)
- Week 2: Working voting (can display itinerary and collect votes)
- Week 3: Working ranking (can compute scores and display sorted list)
- Week 4: Minimum viable QC (outlier detection or AI moderation, pick one)
- **If any milestone slips, cut a feature immediately**

**Backup**: If scope proves too large, pivot to simpler version:
- "Vote on existing travel itineraries" (team curates 20 itineraries from blogs/Reddit, crowd ranks them)
- This still demonstrates voting aggregation and QC without requiring creation
- Reduces scope by 40-50%

---

## DECISION GUIDANCE

### Verdict: WEAK GO / NEEDS REVISION (Score: 18/30)

**Overall Assessment**: TripTuner is a technically sound project with strong quality control design and achievable core functionality, but **fatally flawed incentive design** creates high risk of recruitment failure. The team is asking for 15-30 minutes of creative work (itinerary creation) while offering only badges and leaderboard positions—a massive mismatch that will prevent reaching target scale of 100-200 contributors. Technical scope is appropriate if features are prioritized, but proposal treats all 10 features as essential without identifying must-haves. Recruitment strategy names specific channels (Reddit) but lacks testing, moderator approval, or backup plans. **The project can succeed if the team immediately addresses the incentive problem** through one of three paths: pay for creation, reduce task burden, or plan to seed content themselves.

---

### Critical Change Required

**Before proceeding, the team MUST choose one of these paths**:

### Path 1: Pay for Creation (Strongly Recommended)
**Reallocate budget to match task difficulty**:
- **Budget change**: $75-100 for itinerary creation, $0-25 for voting
- **MTurk/Prolific**: Pay $3-5 per quality itinerary (must meet requirements: budget included, 5+ activities, realistic timing, 150+ words)
- **Expected output**: 15-25 itineraries covering 3-5 destinations
- **Voting**: Free (Penn students, course classmates) or cheap ($0.05/vote for final validation)
- **Why this works**: Matches task difficulty to compensation; realistic for 5-week timeline
- **Trade-off**: Less emphasis on organic community, more emphasis on aggregation/QC algorithms

**Implementation**:
- Week 1: Build submission form
- Week 2: Post 10-15 HIT tasks on MTurk; collect and review
- Week 3: Build voting interface; recruit Penn students to vote
- Week 4-5: Analyze aggregation results; validate QC mechanisms

---

### Path 2: Reduce Task Burden (Recommended Alternative)
**Pivot from creation to curation**:
- **Change task**: Don't ask for full itineraries; ask for single activity recommendations
- **New prompt**: "What's the best thing you did in [city]? (Include cost, time needed, and why you recommend it)"
- **Task time**: 2-5 minutes instead of 20-30 minutes
- **Aggregate**: 20-30 activities per city → "crowd-favorite activities" ranked list
- **Why this works**: Lighter task makes gamification viable; still demonstrates aggregation
- **Trade-off**: Simpler output (activity list, not full itinerary), but proves core concept

**Implementation**:
- Week 1: Build simple activity submission form
- Week 2: Recruit 50-100 Penn students/Reddit users to submit favorite activities
- Week 3: Build voting/ranking interface
- Week 4-5: Aggregate and analyze; test if crowd ranking beats individual opinions

---

### Path 3: Team Seeds Content (Honest Scoping)
**Accept that creation won't be crowdsourced**:
- **Team role**: 6 members × 3-4 itineraries each = 18-24 itineraries
- **Crowd role**: Voting, feedback, and ranking refinement
- **Frame project**: "Content curated by team, validated and ranked by crowd"
- **Why this works**: Removes incentive problem; still demonstrates aggregation, QC, and voting mechanisms
- **Trade-off**: Doesn't validate crowdsourced creation, but proves aggregation works

**Implementation**:
- Week 1: Team researches and writes 18-24 itineraries for 3-5 destinations
- Week 2: Build voting and ranking interface
- Week 3-4: Recruit 80-120 voters (Penn students, friends, Reddit)
- Week 5: Analyze voting patterns; test weighted aggregation formula

---

**If none of these paths are chosen**, the project will likely fail to recruit meaningful participation and demonstrate minimal crowdsourcing validation.

---

### Predicted Outcomes

#### Scenario A: Team Pays for Creation (Path 1) — 30% probability if changes made
- **Week 1-2**: Build platform; post MTurk tasks
- **Week 3**: Collect 15-25 quality itineraries; build voting system
- **Week 4**: Recruit 80-120 Penn students to vote on itineraries
- **Week 5**: Analyze aggregation results; demonstrate QC effectiveness
- **Grade**: B+ to A- range—strong technical execution, validated aggregation and QC, slightly weaker on organic crowdsourcing
- **Learning**: Paid crowdsourcing works for creative tasks when budget aligns with effort

#### Scenario B: Team Reduces Task Burden (Path 2) — 25% probability if changes made
- **Week 1**: Build simple activity submission form
- **Week 2-3**: Recruit 60-100 contributors; collect 150-250 activity recommendations
- **Week 4**: Build ranking interface; aggregate and analyze
- **Week 5**: Demo crowd-curated activity lists for 3-5 cities
- **Grade**: A-/B+ range—strong crowdsourcing validation with lighter task, good engagement
- **Learning**: Task scope directly impacts participation; smaller asks get better response

#### Scenario C: Team Seeds Content (Path 3) — 20% probability if changes made
- **Week 1**: Team writes 18-24 itineraries
- **Week 2-3**: Build voting system; recruit 100-150 voters
- **Week 4-5**: Collect 500+ votes; validate aggregation formula
- **Grade**: B+ range—strong technical work, demonstrates aggregation/QC, but limited crowdsourced creation
- **Learning**: Sometimes hybrid approach (team creates, crowd validates) is pragmatic path

#### Scenario D: Team Proceeds As Planned (No Changes) — 60% probability without intervention
- **Week 1-3**: Build platform with most/all 10 features
- **Week 4**: Realize Reddit posts aren't generating contributions; panic recruitment
- **Week 5**: Demo with 8-15 itineraries (team + close friends); working voting system but minimal data
- **Grade**: B-/C+ range—technically competent but failed crowdsourcing validation
- **Learning**: Incentive design matters more than technical sophistication

#### Scenario E: Team Scope Creeps, Doesn't Finish — 15% probability
- **Week 1-4**: Build AI summarization, NLP duplicates, visualization dashboard, editable suggestions
- **Week 5**: Core voting system not fully working; rushed demo with incomplete features
- **Grade**: C+ range—overambitious scope prevented completion
- **Learning**: Prioritization and scope management are critical skills

---

## COMPARISON TO V1 ANALYSIS

### What Changed from Round 2 to Round 3?

**Improvements**:
- ✅ Expanded team from 2 to 6 members (Jevin, Nikki, Julia, Arushi, Liana, Sadia)
- ✅ Added steel-man discussion comparing TripTuner (Idea A) to CrowdBudget (Idea B)
- ✅ Clarified aggregation formula with specific weights (0.6 votes + 0.2 feedback + 0.2 completeness)
- ✅ Expanded QC section to 6 mechanisms with more specifics (2σ outlier threshold, Perspective API)
- ✅ Added "Handling Low-Quality Work" subsection
- ✅ Specified budget breakdown ($0.05/vote, $0.50/worker)

**Unresolved Issues from V1**:
- ❌ **Incentive design remains fatally flawed** (V1: "asking for CREATION but offering BADGES")
- ❌ Recruitment strategy still vague (Reddit mentioned but no testing or moderator approval)
- ❌ No evidence of demand validation or user testing
- ❌ 10 features listed without prioritization (V1 suggested cutting to 3-4 must-haves)
- ❌ No discussion of seeding strategy or cold-start problem

**Regression**:
- ⚠️ Budget now explicitly allocates $75-100 for VOTING but $0 for creation—making the incentive mismatch even more explicit
- V1 suggested "pivot to paid contributions ($3-5 per itinerary)"—Round 3 did the opposite

### V1 vs V2 Scoring Comparison

| Dimension | V1 Score (Implied) | V2 Score | Change | Notes |
|-----------|-------------------|----------|--------|-------|
| Technical Feasibility | ~4/5 | 4/5 | → | Still appropriately scoped if features prioritized |
| Crowdsourcing Viability | ~3/5 | 3/5 | → | Travel sharing is real but competition and cold-start unaddressed |
| Incentive Design | ~2/5 | 2/5 | → | **Critical flaw remains unfixed; budget allocation makes it worse** |
| Scope Appropriateness | ~3/5 | 3/5 | → | 10 features still too many but core loop achievable |
| Recruitment Strategy | ~2/5 | 2/5 | → | Reddit named but still no testing or commitments |
| Quality Control | ~3.5/5 | 4/5 | ↑ | Improved with more specifics (2σ threshold, Perspective API) |
| **TOTAL** | **~17-18/30** | **18/30** | → | **Minimal improvement; core issues unaddressed** |

### V1 Verdict vs V2 Verdict

**V1 Verdict**: "WEAK GO"

**V2 Verdict**: "WEAK GO / NEEDS REVISION"

**Status**: Essentially unchanged. Round 3 improved documentation (especially QC section) but did not address the fundamental incentive design problem that V1 identified as the "fatal flaw."

---

### Key Takeaway

**The team improved the DOCUMENTATION but not the DESIGN.** Adding a sixth team member, expanding the QC section, and specifying the aggregation formula are all positive, but **none of these changes address why strangers would spend 20 minutes creating itineraries for badges**.

**What V1 Analysis Predicted**: "Build platform weeks 1-3, realize week 4 Reddit doesn't care, MTurk week 4-5, demo with 25-30 itineraries (8 team + 10 MTurk + 5 friends)."

**Current V2 Assessment**: This prediction remains accurate. The team has a larger group (6 people instead of 2), which helps with development velocity but doesn't solve the recruitment/incentive problem.

---

### Comparison to V1 Recommendations

**V1 Recommended**: "Three Paths Forward: (1) Pivot to paid contributions ($3-5 per itinerary, 15-25 total), (2) Reduce task burden (single activity recs vs. full itineraries), (3) Accept seeding it yourselves (team creates 10-15 each)"

**V2 Actual Changes**: ❌ None of these paths were chosen. Budget was explicitly allocated to voting ($75 for 250 votes) rather than creation.

**Result**: The most critical feedback from V1 was ignored. Team focused on adding documentation and team members rather than fixing the core design flaw.

---

### Why the Score Barely Changed

**V1**: ~17-18/30
**V2**: 18/30

The score improved slightly (+1 point) due to:
- Better QC specificity (+0.5 in Dimension 6)
- Larger team reducing technical risk (+0.5 spread across dimensions)

But the score couldn't improve meaningfully because:
- **The fatal incentive flaw remains** (Dimension 3: still 2/5)
- **Recruitment is still vague** (Dimension 5: still 2/5)
- **Scope is still unclear** (Dimension 4: still 3/5)

**Documentation improved, execution plan did not.**

---

## RECOMMENDATION

**This project can still succeed, but requires immediate decision on incentive strategy.** The team has done good work on QC design and technical architecture, but **must immediately address the creation incentive problem** before investing time in platform development.

**Required Actions for Week 1** (if team proceeds):

### Decision Point 1: Choose Path (Required by end of Week 1)
- [ ] **Path 1**: Reallocate budget to pay $3-5 per itinerary (15-25 paid contributions)
- [ ] **Path 2**: Pivot to single activity recommendations (lighter task, 2-5 min)
- [ ] **Path 3**: Team creates all itineraries; crowdsource voting only

**Team must commit to ONE path. Proceeding without choosing will result in participation failure.**

### Decision Point 2: Test Recruitment (Required by end of Week 1)
- [ ] Post interest check to r/travel or r/solotravel: "Would you use a community-curated travel itinerary platform?"
- [ ] Message subreddit moderators for approval to post research project
- [ ] If Reddit test fails or mods deny, pivot to Penn-only recruitment (classmates, study abroad students)

### Decision Point 3: Prioritize Features (Required by end of Week 1)
- [ ] Force-rank all 10 features
- [ ] Identify 3-4 "Must-Have for Demo"
- [ ] Cut or defer 6-7 "Nice-to-Have" features
- [ ] Commit to building horizontal slice (submit → vote → rank) by end of Week 2

---

**If these decisions are not made by end of Week 1**, the team will follow the predicted Scenario D trajectory: build a feature-rich platform with minimal user participation, resulting in B-/C+ grade for technical work but failed crowdsourcing validation.

**If team addresses incentive problem and descopes features**, the project has good potential (B+ to A- range) because the core concept (crowd-ranked travel content) is sound and the technical architecture is appropriate.

**The difference between success and failure is not technical—it's operational**: Will the team prioritize solving the incentive and recruitment problems over building all proposed features?

---

**Analysis by**: Claude Sonnet (NETS 2130 Project Evaluation)
**Viability Score**: 18/30 (Needs Major Revision)
**Recommendation**: Proceed only if incentive problem solved; otherwise pivot or descope significantly
