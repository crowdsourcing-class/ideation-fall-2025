# Urban Explorer - Project Viability Analysis (V2)

**Project**: Urban Explorer - Crowdsourced event discovery platform with interactive map
**Authors**: Katherine Yue (kyue), James Doh (dohj0109), Omar Pareja (pareja), Eric Lee (ericclee), Mario Valek (mvalek)
**Analysis Date**: 2025-11-02
**Analyst**: NETS 2130 Course Staff

---

## VIABILITY SCORE BREAKDOWN

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| **1. Technical Feasibility** | 3/5 | React Native frontend, Node.js backend, PostgreSQL database with map integration. Moderate complexity with one new technology (maps), but achievable CRUD app. Some confusion (React Native vs. Next.js). |
| **2. Crowdsourcing Viability** | 2/5 | Two-sided marketplace (need event posters AND attendees). No captive audience identified. Value proposition unclear until critical mass reached. Classic cold-start problem. |
| **3. Incentive Design** | 2/5 | Leaderboards and badges for posting events (low-effort task = appropriate gamification), but incentives don't address cold-start. Small businesses gain "visibility" on empty platform = circular. |
| **4. Scope Appropriateness** | 4/5 | 8 features with reasonable core loop. Interactive map, posting, verification, notifications. Some feature creep (trust scores, ML duplicate detection) but mostly constrained. |
| **5. Recruitment Strategy** | 2/5 | Vague: "volunteers and social media users." No specific channels named. Made-up 1:10 poster:attendee ratio. Plan to pay for initial posts ($1 each) acknowledges cold-start but underestimates scale needed. |
| **6. Quality Control** | 3/5 | Basic mechanisms: majority voting (3 users for verification), expert review (10-15%), reputation/trust scores, statistical outlier detection. Reasonable but some vagueness ("trusted users" selection unclear). |

**TOTAL SCORE: 16/30**

**Category**: **NEEDS MAJOR REVISION** (15-19 range)

---

## EXECUTIVE SUMMARY

Urban Explorer is a crowdsourced event discovery platform addressing a real user need: centralized local event information. The technical architecture is appropriate for a 5-week timeline, and the team demonstrates modern full-stack competency. However, the project suffers from classic two-sided marketplace challenges: weak cold-start strategy, circular value proposition (need events to attract users, need users to attract event posts), and underestimated acquisition costs. The incentive design relies on network effects that won't exist during the MVP phase. With strategic pivots—particularly seeding content proactively and focusing on a dense geographic area—this could become viable.

---

## DETAILED ASSESSMENT

### 1. Technical Feasibility: 3/5 - Challenging but Doable

**What they're building:**
- Frontend: React Native (line 99) OR Next.js (line 127)—inconsistency suggests planning confusion
- Backend: Node.js + Express
- Database: PostgreSQL
- Map integration: Interactive map interface (likely Mapbox or Google Maps)
- Features: Event posting, verification system, notifications, leaderboards, auto-expiration, flagging, trust scores
- ML: "Text similarity detection for duplicate events" (line 130)

**Why this scores 3/5:**

**Strengths:**
- Standard CRUD operations (create event, read events, update verification, delete expired)
- Team lists specific, modern tools: TanStack Query, Prisma ORM (line 103)—shows technical competence
- Workflow (lines 108-116) is clear and reasonable: post → validate → persist → fetch → infinite scroll
- No mobile-specific features that require native code (notifications can be web-based)
- Map integration is "one new technology"—fits rubric's definition of "moderate complexity"

**Concerns:**
- **React Native vs. Next.js confusion**: Line 99 says React Native, line 127 says Next.js. These are different frameworks (mobile vs. web). Suggests team hasn't aligned on architecture.
- **ML duplicate detection**: "Text similarity detection" (line 130) is non-trivial. Simple Levenshtein distance is doable; embedding-based similarity requires ML pipeline. Scope creep risk.
- **Notification system**: "Notifies users of events within a certain radius" (line 51)—requires background jobs, geospatial queries, and push notification setup. 2-3 days of work if not using existing service.
- **Trust score system**: "Weights user input based on history" (line 55)—requires tracking reputation, updating scores, and integrating into ranking algorithm. Not difficult but time-consuming.

**Two-week test:**
Could they build core loop (post event → display on map → users upvote) in 2 weeks?
- **Yes**, if Next.js/React (web app) and cutting notifications + trust scores + ML.
- **No**, if React Native (mobile) or keeping all features.

**Verdict**: Doable if they clarify the stack (web-first) and descope ML + notifications. Current ambiguity risks wasting Week 1 debating architecture.

---

### 2. Crowdsourcing Viability: 2/5 - Weak Value Proposition

**Their model:**
- **Posters**: Local event organizers, small businesses, individuals hosting gatherings
- **Attendees**: Residents, visitors looking for things to do
- **Value**: Centralized discovery of local events

**The cold-start death spiral:**

**Problem 1: Two-sided marketplace**
- Need events to attract users (why install an app with 3 events?)
- Need users to attract event posts (why post to a platform with 10 users?)
- Rubric explicitly warns: "Two-sided marketplace (need both sides simultaneously)" is a red flag

**Problem 2: Weak immediate value**
- Compare to competitors:
  - **Eventbrite**: Thousands of events, ticketing system, established trust
  - **Nextdoor**: Existing social network, diverse content (not just events)
  - **Facebook Events**: 2 billion users, integrated social graph
- Urban Explorer Day 1: 0 events, 0 users, no ticketing, no social features
- User value: Zero until critical mass (50-100 events in their area)

**Problem 3: No captive audience**
- "Volunteers and social media users" (line 61)—completely vague
- Not "my dorm building (300 people)" or "Penn clubs I'm in"
- Not "my fraternity uses this for parties" (built-in audience)

**Problem 4: Made-up ratio**
- "100 users, 10 workers (assuming 1:10 ratio of posters & attendees)" (line 91)
- Where does 1:10 come from? Social platforms typically see 1:100 or worse (1% rule: 90% lurkers, 9% contributors, 1% creators)
- If ratio is actually 1:50, need 500 initial users to get 10 posters—impossible to bootstrap

**Mitigation they mention:**
- "At first, it will come from paid sources (people who search for event postings)" (line 88)
- Budget: "$1 for each post" × "50-100 initial posts" = $50-100
- This helps but underestimates scale:
  - 50 events city-wide = useless (user in North Philly sees 2 events)
  - Need geographic density: 50 events in 1-mile radius = useful

**Challenge 2 (Cold Start) mitigation:**
- "Scrape and import event data from public APIs (Facebook Events, Meetup, city government calendars)" (line 202-203)
- **Critical flaw**: Facebook Events API shut down in 2018. Can't scrape without violating ToS.
- Meetup API requires partnership.
- City calendars: doable but limited (official events only, not "open mic at coffee shop")

**Rubric scoring:**
- Score 5: "Captive audience—your class, dorm, club"—they don't have this
- Score 2: "Weak value—benefits require scale OR unclear to users"—matches exactly

**Verdict**: Classic two-sided marketplace death spiral. Without seeding strategy or captive audience, very high risk of empty platform.

---

### 3. Incentive Design: 2/5 - Mismatch

**Task analysis:**

**For event posters:**
- **Time**: 2-5 minutes (fill form: title, description, location, date/time)
- **Effort**: Low to moderate
- **Boredom**: Low (self-interested, promoting own event)

**For verifiers/voters:**
- **Time**: 30 seconds (upvote or flag)
- **Effort**: Very low
- **Boredom**: Low (browsing events is discovery task)

**Incentives offered:**

**For posters:**
1. **Visibility**: "Small businesses can gain visibility through this platform" (line 77)
   - Problem: Visibility on platform with 10 users = worthless
   - Circular incentive (need users to get visibility, need posts to get users)
2. **Leaderboards/badges**: For having "popular events" (line 52)
   - Problem: No community yet, leaderboard of 3 people is demotivating
3. **Freemium model**: "Promoted events or analytics dashboards for businesses incur fee" (line 263)
   - Problem: Won't pay to promote on empty platform

**For verifiers/attendees:**
1. **Discovery value**: Finding events to attend
   - Problem: Only valuable if events exist (cold-start)
2. **Gamification**: Badges for posting or verifying (line 77)
   - Appropriate for low-effort task, but no intrinsic motivation

**Rubric assessment:**
- Posting (2-5 min) + gamification = "Score 4: Good match"
- BUT incentive value is zero until network effects exist
- Should be Score 2: "Mismatch—high effort (for posters in empty network) → badges only"

**What's missing:**

1. **No organic reason for first 100 posters**:
   - Why post to Urban Explorer vs. Facebook/Instagram?
   - Facebook: Friends see it (existing audience)
   - Instagram: Followers see it (existing audience)
   - Urban Explorer: Strangers might see it (no audience)

2. **No attendee hook beyond events**:
   - Nextdoor works because it has local news, recommendations, marketplace, etc.
   - Urban Explorer is ONLY events—if no events, no reason to open app

3. **Underestimated paid acquisition**:
   - $1 per event post × 50 events = $50
   - But 50 events city-wide is sparse
   - Need 500 events for density (1 per 0.1 sq mi in Philadelphia) = $500
   - Budget says "$500/month" but doesn't allocate to acquisition

**Verdict**: Incentives appropriate for the task mechanics but ignore cold-start economics. Network effects can't bootstrap without external catalyst.

---

### 4. Scope Appropriateness: 4/5 - Slight Stretch

**Features listed (lines 48-55):**
1. Interactive map
2. Posting feature
3. Verification system
4. Notification system
5. Engagement leaderboard
6. Auto-expiration
7. Flagging system
8. Trust score

**Core loop:**
- User posts event → persists to DB → appears on map → other users upvote/flag → event ranked by score

**Assessment:**

**Must-haves (achievable):**
1. Interactive map: Use Mapbox/Google Maps SDK (2-3 days)
2. Posting: Form + validation (1-2 days)
3. Display: Fetch events, render on map (1-2 days)
4. Voting: Upvote/downvote buttons + counter (1 day)

**Should-haves (adds complexity):**
5. Verification system: Require 3 users to verify (line 147)—adds workflow state machine (2-3 days)
6. Auto-expiration: Cron job to delete old events (1 day)
7. Flagging: Reporting system + moderation queue (2-3 days)

**Could-haves (feature creep):**
8. Trust score: Track user history, weight votes (3-4 days)
9. Leaderboard: Query + display rankings (1-2 days)
10. Notifications: Push or email for nearby events (3-4 days)
11. ML duplicate detection: Text similarity (mentioned line 130, not in feature list) (3-5 days)

**Total estimation:**
- Must-haves: 5-8 days
- Should-haves: 5-7 days
- Could-haves: 7-11 days
- **Total: 17-26 person-days**

With 5-person team × 5 weeks × ~4 days/week effective = 100 person-days, this is **20-25% of budget**. Very reasonable.

**Two-week test**: Yes, could demo core loop in 2 weeks.

**Feature count test**: Core is 3-4 features (map, post, display, vote). They list 8. Slightly over but not egregious.

**Why not 5/5:**
- Notification system is underestimated (push notifications require infrastructure)
- Trust score + verification state machine adds complexity beyond CRUD
- ML duplicate detection (if implemented) is scope creep

**Verdict**: Well-scoped compared to other projects. Main risk is feature creep, not overambition.

---

### 5. Recruitment Strategy: 2/5 - Vague Hope

**Their plan (line 61-62):**
"Primarily volunteers and social media users who want to stay informed or promote local events"

**Specificity test:**

1. **Can you NAME the exact groups/places?**
   - No. "Social media users" but not "Penn Class of 2025 Facebook group" or "r/philadelphia"
   - "Volunteers" but who? From where?

2. **Have you TESTED recruitment?**
   - No evidence of posting anywhere
   - No test event submissions

3. **Do you need >50 people to start?**
   - Yes. Empty map is useless. 100 users minimum (line 91).

4. **Can you seed it yourself?**
   - Partially. They mention paying for initial posts ($1/event × 50 = $50).
   - But 50 events city-wide insufficient for density.

**Challenge 2 mitigation (lines 199-205):**
- **Scrape data from Facebook Events, Meetup**:
  - Facebook Events API shut down 2018—cannot scrape without ToS violation
  - Meetup requires partnership (takes months)
- **Partner with local organizations**:
  - "University clubs, libraries, community centers" (line 203)
  - Good idea but no specifics (which clubs? have they contacted them?)
- **Targeted launch in small area (university campus)**:
  - **Best strategy in the document**—Penn campus is dense, reachable, measurable
  - But not emphasized as primary plan

**Backup plan (lines 205-206):**
"Gamified onboarding—new users vote/verify events before posting"
- Clever (teaches system, builds QC data)
- But requires events to already exist (chicken-egg)

**Rubric scoring:**
- Score 5: "My dorm's GroupMe (200 people), already talked to RA"
- Score 3: "Reddit communities, social media, MTurk"
- Score 2: "Social media campaigns, word of mouth"

They're between 2-3. Generic "social media" without named channels = Score 2.

**Critical insight:**
Backup plan (campus launch) should be PRIMARY plan. Penn campus has:
- Geographic density (can saturate 1 sq mi)
- Captive audience (40,000 students)
- Existing events (club meetings, talks, parties)

Starting city-wide is death sentence. Starting Penn-only could work.

**Verdict**: Vague recruitment strategy without concrete channels or commitments. Campus focus mentioned but buried as backup.

---

### 6. Quality Control: 3/5 - Basic

**Mechanisms listed (lines 147-158):**

1. **Majority voting (3 independent users for verification)**:
   - Event unverified until 2+ users upvote (line 147-148)
   - Tie → pending state
   - Reasonable approach

2. **Expert review (10-15% of events weekly)**:
   - "Trusted users" review conflicting votes (line 149-150)
   - Questions: How are "trusted users" selected? Initial bootstrap?

3. **Reputation/trust score**:
   - Increases with confirmed posts, decreases with flagged posts (line 153)
   - High-trust users get "auto-verification priority" and "moderation abilities" (line 153)
   - Good feedback loop

4. **Statistical outlier detection**:
   - Flags unusual posting frequency, duplicate content, geographic inconsistency (line 155)
   - "Temporarily suspended for manual review" (line 156)
   - Smart spam prevention

**What's missing:**

1. **Gold standard**: No mention of test events with known answers
2. **Agreement thresholds**: "2+ users upvote" but what if 2 upvote, 2 flag? Tie-breaking rule unclear
3. **Expert selection**: "Trusted users" based on trust score, but initial trust score = neutral (line 153). Who reviews first 100 events?
4. **Redundancy for verification**: 3 users minimum (line 147), but optimal redundancy not specified

**Handling low-quality work (line 163):**
"Flagged or low-confidence events are re-evaluated by trusted users. Repeated offenders lose posting privileges or reputation points."
- Reasonable approach
- Concern: "Repeated offenders"—how many strikes? Permanent ban or temporary?

**Assessment:**

**Strengths:**
- Multi-layered approach (voting + expert + reputation + outliers)
- Automation for obvious spam (frequency, duplicates)
- Gamification aligns with QC (trust score = status)

**Weaknesses:**
- No gold standard for calibration
- Vague expert selection (initial "trusted users" bootstrapping unclear)
- Verification threshold not precisely specified (what % agreement needed?)

**Rubric scoring:**
- Score 5: "Multi-layered—gold standard + redundancy + statistical filtering + review"
- Score 4: "Thoughtful—2-3 mechanisms with specific thresholds/numbers"
- Score 3: "Basic—redundancy/voting + one other mechanism"

They have 4 mechanisms (voting, expert, reputation, outliers) but lack specificity on thresholds and bootstrapping. Score 3-4. Calling it **3** because missing gold standard and vague on details.

**Verdict**: Reasonable QC framework but needs more specificity. Not a project-killer but room for improvement.

---

## RISK ANALYSIS

### Risk 1: Cold-Start Death Spiral (Likelihood: Very High, Impact: Critical)

**Why critical:**
Without events, users don't install. Without users, event posters don't post. Platform stays empty permanently.

**Warning signs:**
- No captive audience identified (not "my 20 club members will seed")
- Paid acquisition budget ($50-100) insufficient for density
- Reliance on "word of mouth" and "social media campaigns"
- Two-sided marketplace dynamics ignored

**Mitigation:**
1. **Week 0 action**: Change scope from city-wide to **Penn campus only**
   - Achievable density (500 events on 1-mile radius)
   - Reachable audience (40k students)
   - Measurable success (10% penetration = 4,000 installs)
2. **Week 1 action**: Team manually curates 50 Penn events for launch
   - Club meetings, office hours, parties, lectures
   - Costs $0, takes 10 hours (2 hours/person)
3. **Week 2 action**: Partner with 5 Penn clubs for guaranteed posts
   - "We'll feature your events"—give them moderation privileges
   - Locks in content supply
4. **Pivot trigger**: If <100 installs Week 3, pivot to curation model (team updates events daily)

---

### Risk 2: Technical Architecture Confusion Delays Start (Likelihood: Moderate, Impact: Moderate)

**Why concerning:**
Document says React Native (line 99) and Next.js (line 127). These are incompatible choices (mobile vs. web framework). Suggests team hasn't aligned on stack, risks wasting Week 1 debating.

**Warning signs:**
- React Native = mobile app (requires App Store deployment, mobile-specific APIs)
- Next.js = web framework (server-side rendering, web-first)
- Cannot be both simultaneously

**Mitigation:**
1. **Immediate decision (before Week 1)**: Choose **Next.js web app**
   - Rationale: No App Store approval delay, easier deployment, desktop + mobile web
   - Sacrifice: Not a "real app" (web wrapper feels less native)
2. **Rule out React Native**:
   - Rubric explicitly warns: "Mobile app development (add 3-4 weeks to timeline)"
   - 5-week project cannot afford mobile complexity

**Impact if not addressed:**
- Week 1 wasted on "should we do mobile or web" debate
- Week 2 discovers mobile deployment complexity
- Week 3-4 scramble to rebuild as web app
- Week 5 demo incomplete app

---

### Risk 3: Notification System Underestimated (Likelihood: Moderate, Impact: Moderate)

**Why concerning:**
Feature 4: "Notification system—notifies users of events within certain radius" (line 51). Sounds simple but requires:
- Background job scheduler (cron or task queue)
- Geospatial queries (find events within X miles of user location)
- Push notification service (Firebase, OneSignal, or AWS SNS)
- User preferences (opt-in/out, notification frequency)

**Effort estimate:** 3-5 days of work, debugging across devices.

**Mitigation:**
1. **MVP version**: Email notifications only (simpler than push)
   - Send daily digest of events near user's saved location
   - Use SendGrid/Mailgun (free tier sufficient)
2. **Defer push notifications**: Mark as "stretch goal" if time allows
3. **Alternative**: No proactive notifications—users check app when bored (Instagram model)

---

## DECISION GUIDANCE

### Verdict: **WEAK GO / MONITOR CLOSELY** (Score: 16/30)

Per rubric guidance for 15-19 range: "Needs major revision. Project has multiple serious issues."

Sits on boundary with 20-24 ("Weak GO"). With targeted changes below, could elevate to viable.

**Critical changes required:**

### 1. Geographic Scope: City-Wide → Penn Campus Only (Non-Negotiable)

**Why:**
- Cannot achieve event density city-wide with limited resources
- Penn campus = captive audience, achievable critical mass
- 40,000 students, 1-mile radius = high density

**How:**
- Launch target: 100 events in 1-mile radius of campus
- Marketing: Posters in Huntsman, clubs email list, class announcements
- Seed events: Team manually adds 50 verified events (club meetings, lectures, office hours)

**Success metric:**
- 500 installs Week 3 (1% of students)
- 10% of those post events (50 posters)
- 50 posters × 2 events each = 100 events

---

### 2. Technical Architecture: Commit to Next.js Web App (Week 0)

**Why:**
- React Native adds 3-4 weeks (App Store approval, mobile debugging)
- Next.js = web-first, mobile-responsive, fast deployment

**How:**
- Use Next.js + React + Mapbox GL JS
- Mobile users access via browser (responsive design)
- Deploy on Vercel (free tier, instant deploys)

**Sacrifice:**
- Not a "native app" (no App Store presence, less "professional")
- Acceptable for MVP, can port to mobile later if successful

---

### 3. Incentive Redesign: Seed Content Proactively (Week 1-2 Priority)

**Why:**
- Gamification doesn't solve cold-start
- Small businesses won't pay for visibility on empty platform
- Must provide value from Day 1

**How:**
1. **Week 1: Team seeds 50 events**
   - 2 hours/person scraping Penn websites (clubs, departments, athletics)
   - Manually create posts (team = verified posters)
2. **Week 2: Partner with 10 clubs**
   - Offer "featured club" status
   - Give club leaders moderation privileges (status incentive)
   - Each club posts 5 events = 50 more events
3. **Week 3: Open to public**
   - 100 events live, platform looks active
   - Users see immediate value (events to attend)

**Budget reallocation:**
- $500/month → $0 paid acquisition, $100 hosting, $400 club partnership incentives (pizza for meetings?)

---

### 4. Descope: Cut Notifications + ML Duplicate Detection (Week 2 Decision)

**Why:**
- Notifications = 3-5 days work, not core to MVP
- ML duplicate detection = 3-5 days, rare problem in small dataset

**How:**
- Mark both as "Phase 2" features
- Focus Week 3-4 on polish (map UX, posting flow, verification speed)

**Sacrifice:**
- Users don't get proactive event alerts (must open app to discover)
- Duplicate events possible (but can flag manually during MVP)

---

### Predicted Outcomes

**If no changes made (current plan):**
- **Week 1-2**: Build tech (map, posting, voting)—works well
- **Week 3**: Launch city-wide, post in r/philadelphia (ignored)
- **Week 4**: Panic, recruit friends to post events
- **Week 5**: Demo with 20 events (mostly team + friends)
- **Demo**: Slick UI, empty map
- **Grade**: B+ for technical execution, C for crowdsourcing, B overall
- **Feedback**: "Impressive interface, but you didn't solve the cold-start problem"

**If critical changes made (Penn-only, seed content, web app):**
- **Week 1**: Commit to Next.js, seed 50 events
- **Week 2**: Partner with 10 clubs, add 50 more events (100 total)
- **Week 3**: Launch at Penn, post in class GroupChats + club emails
- **Week 4**: 300 installs, 30 organic event posts (clubs using it)
- **Week 5**: 500 installs, 150 events, active voting
- **Demo**: Working platform with real user data, clear density
- **Grade**: A- for realistic scoping + execution
- **Feedback**: "Great example of solving cold-start with geographic focus"

**If partial changes made (Penn focus but no seeding):**
- **Week 1-2**: Build tech
- **Week 3**: Launch Penn-only, 0 events (waiting for organic posts)
- **Week 4**: 50 installs, 10 posts (underwhelming)
- **Week 5**: Team scrambles to add events manually
- **Demo**: ~30 events, lukewarm reception
- **Grade**: B for execution, feedback on weak growth strategy

---

## COMPARISON TO V1 ANALYSIS

### What V1 Got Right:
- Identified cold-start death spiral as main issue
- Called out vague recruitment ("post on Reddit = not a strategy")
- Noted technical inconsistency (React Native vs. Next.js confusion)
- Recognized premature optimization (5 QC mechanisms before users exist)
- Predicted outcome: slick platform, sparse data

### What V2 Adds:

**Structured rubric framework:**
- V1 gave subjective ratings ("C+ crowdsourcing")
- V2 provides dimension-by-dimension 1-5 scores with justification

**Quantified cold-start economics:**
- V1 mentioned chicken-egg problem conceptually
- V2 calculates: 1:10 ratio likely wrong (actually 1:100), 50 events insufficient for density, need 500 for saturation

**Technical feasibility deep-dive:**
- V1 noted React Native risk
- V2 breaks down feature effort (notifications = 3-5 days, trust score = 3-4 days), estimates 17-26 person-days total

**Actionable mitigation with Week-by-Week plan:**
- V1 said "seed content proactively"
- V2 specifies: Team adds 50 events Week 1, partners with 10 clubs Week 2, 100 events for launch Week 3

**Three outcome scenarios:**
- V1 gave single prediction
- V2 shows no-change, full-pivot, partial-pivot with likely grades for each

### Key Agreement:
Both analyses identify **cold-start problem** as fatal flaw and recommend **Penn campus focus** + **content seeding**. V2 provides implementation roadmap.

### Where V2 Differs:
- **More optimistic on scope**: V1 rated scope harshly, V2 gives 4/5 (team planned reasonably)
- **More specific on recruitment**: V2 calculates what "100 events" actually requires (50 manual + 50 partnership)
- **Technical stack decision**: V2 demands Week 0 commitment to Next.js, not debating during execution

---

## CONCLUSION

Urban Explorer addresses a real user pain point (fragmented event information) with an appropriate technical architecture for a 5-week timeline. The team demonstrates full-stack competency and modern tooling knowledge. However, the project suffers from classic two-sided marketplace dynamics: weak cold-start strategy, circular incentives (visibility on empty platform), and unrealistic city-wide scope.

**The core concept is sound**: Crowdsourced event discovery has value. **The execution plan has gaps**: Underestimated cold-start, vague recruitment, city-wide overreach.

**Recommended path forward:**
1. **Scope geographically**: Penn campus only (not Philadelphia)
2. **Seed content proactively**: Team + club partnerships create 100 initial events
3. **Commit to web app (Next.js)**: Avoid mobile complexity
4. **Descope**: Cut notifications + ML duplicate detection

With these changes, Urban Explorer could become an **A-level project** demonstrating successful cold-start strategy for two-sided marketplace. Without them, likely a **B-level demo** with strong UI but weak adoption.

**Final Score: 16/30 - Needs Major Revision**

*With targeted pivots (Penn-only, content seeding), could reach 21-23/30 (Weak GO with managed risks).*
