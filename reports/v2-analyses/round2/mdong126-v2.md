# V2 Viability Analysis: Soundscape

**Project:** Soundscape - Crowdsourced global map of ambient audio environments

**Round:** 2 (DROPPED)

**Author:** Mingni Dong (mdong126), Anika Basu (basua)

---

## Viability Score

### 1. Technical Feasibility: 2/5
**Significant Complexity:**
- Audio recording, upload, and streaming infrastructure
- Audio feature extraction (volume, frequency spectrum, MFCC, chroma)
- ML-based audio similarity clustering
- Interactive map with real-time updates
- Web Audio API + mobile recording
- Audio format transcoding and normalization
- Perceptual hashing for duplicate detection
- SNR calculation and audio quality filtering

**Tech Stack Mentioned:**
- Frontend: React (Next.js), React Native (Expo), Tailwind, Web Audio API
- Backend: Python (FastAPI) or Node (Express), Firebase Functions
- Storage: Firebase Firestore + Cloud Storage + optional PostgreSQL
- Audio/ML: librosa, pydub, ffmpeg, scikit-learn, optional PyTorch/ONNX
- Maps: Mapbox GL JS, Leaflet, OpenStreetMap, Turf.js
- QC: Weighted voting service, Redis queues
- Analytics: PostHog/Mixpanel, Firebase Remote Config
- DevOps: Docker, GitHub Actions, Vercel, Expo EAS, Sentry
- Optional: MTurk/Prolific adapters

**This is absolutely massive:**
- Audio processing pipeline alone = 2-3 weeks
- Mobile + web apps = 2-3 weeks each
- ML similarity/clustering = 2 weeks
- Map integration = 1 week
- QC systems = 1 week

**Total estimated effort:** 10-12 weeks minimum for an experienced team.

### 2. Crowdsourcing Viability: 3/5
**Mixed Prospects:**

**Strengths:**
- Task is relatively quick (10-30 seconds to record)
- Creative/exploratory appeal (sonic tourism)
- Immediate visual feedback (appears on map)
- Potential for intrinsic motivation (sharing your environment)

**Weaknesses:**
- Value proposition is unclear for most users
- "Remote workers finding quiet spaces" - niche audience
- "Travelers exploring cities through sound" - do people actually want this?
- Not obviously useful until you have dense coverage
- Circular dependency: need lots of recordings to be interesting, need to be interesting to get recordings

**Questionable Assumptions:**
- Do people actually care about ambient soundscapes?
- Would you choose a café based on its audio profile?
- Market validation seems absent

### 3. Incentive Design: 3/5
**Gamification-Focused:**
- Points and badges for verified uploads
- Leaderboards by city/category
- "Sound Explorer" titles
- Daily themed challenges ("Quietest Spot on Campus Week")
- Contributions appear on global map (visibility)
- Small digital rewards for challenge winners

**Analysis:**
- Task is quick (30 seconds to record) - gamification can work
- Creative/artistic element adds intrinsic motivation
- Leaderboards provide social motivation
- Map visualization provides immediate feedback

**However:**
- No payment for contributions
- Badges for audio recordings = questionable appeal
- "Digital rewards" is vague
- Requires sustained participation (recordings get stale)

**Verdict:** Better than unpaid high-effort tasks, but weaker than problems people personally care about solving.

### 4. Scope Appropriateness: 1/5
**Wildly Overscoped:**

**8 Major Features:**
1. Geo-tagged audio uploads with automatic location tagging
2. Mood & environment tagging system
3. Interactive sound map with color-coding
4. Crowd verification & rating system
5. Daily sound challenges
6. Gamified reputation system
7. Sound similarity discovery (ML clustering)
8. Open Data & API Access

**Technical Components:**
- Web app
- Mobile app (iOS + Android)
- Audio processing pipeline
- ML similarity engine
- Real-time map visualization
- Gamification infrastructure
- Quality control systems
- API for external developers
- Analytics and A/B testing

**This is a complete product platform, not a course project.**

**Scope Reality Check:**
- Could you build core loop in 2 weeks? NO - audio pipeline + map integration + mobile alone = 3-4 weeks
- Could you manually simulate the system? NO - requires technical audio processing
- Can you name 3-4 must-haves? They list 8 essential features

### 5. Recruitment Strategy: 2/5
**Vague with Unrealistic Scale:**
- "Volunteers, people in the Philly area"
- "At least 300 and max 1000" workers needed
- No specific channels identified
- No captive audience

**Missing:**
- Which Philadelphia communities?
- How to recruit 300-1000 people?
- Why would they participate?
- No Penn-specific strategy despite being at Penn

**Mentions recruitment strategy but provides no concrete plan.**

### 6. Quality Control: 4/5
**Impressively Detailed:**

**Pre-Submission Guardrails:**
- Duration enforcement (10-30s)
- Clipping detection (>10% rejected)
- Silence ratio checks (>80% rejected)
- SNR threshold (< 5dB rejected)
- Format normalization (mono, 16kHz, loudness normalized)
- GPS validation (30m accuracy)
- Sensor consistency checks
- Duplicate detection via perceptual hashing
- Rate limiting and CAPTCHA

**Post-Submission:**
- Weighted majority voting
- Gold standard test clips
- Attention checks
- Reputation system (90th percentile = trusted listeners)
- Expert escalation for disputes
- Statistical outlier detection

**This is actually excellent** - shows deep understanding of audio QC challenges. However, it's also extremely complex to implement.

---

## Total Score: 15/30

**Verdict:** NEEDS MAJOR REVISION / STOP AND PIVOT

---

## Why Was It Dropped?

**Speculation based on quality:**

1. **Massive Technical Overscope:**
   - Building web + mobile apps for audio recording alone = 3-4 weeks
   - Audio processing pipeline (normalization, feature extraction, duplicate detection) = 2 weeks
   - ML-based similarity clustering = 2 weeks
   - Interactive map visualization = 1 week
   - Gamification infrastructure = 1 week
   - **Total: 9-10 weeks minimum, before any features**

2. **Unclear Market Demand:**
   - The proposal never convincingly demonstrates WHO wants this and WHY
   - "Remote workers finding quiet spaces" - wouldn't they just go to the same café they already know?
   - "Travelers exploring through sound" - is this a real use case?
   - "Urban planners" - would they rely on crowdsourced audio?
   - Feels like a solution looking for a problem

3. **Mobile Requirement:**
   - Geolocation + audio recording essentially requires mobile app
   - React Native development adds 2-3 weeks
   - Testing on iOS + Android adds complexity
   - Could do web-only but loses core value proposition (location accuracy)

4. **Network Effects Required:**
   - Platform only useful with dense coverage of locations
   - Need hundreds of recordings per city to be valuable
   - Early users get almost no value
   - Recruitment plan to get 300-1000 users is completely absent

5. **Sustainability Question:**
   - Recordings get stale (café soundscape changes)
   - Requires ongoing contributions forever
   - Gamification may not sustain long-term engagement
   - No business model or funding source

6. **Quality Control Complexity:**
   - The QC system is sophisticated and well-thought-out
   - However, it's also extremely complex to implement
   - Audio validation requires significant technical work
   - Weighted reputation systems need user base to calibrate

---

## Was This the Right Decision?

**YES - Correct to drop, though high-quality proposal**

**Arguments for dropping:**
- 15/30 score = "Needs Major Revision" / borderline "Stop and Pivot"
- Technical scope is 2x what's feasible in 5 weeks
- Mobile development requirement (for location accuracy)
- No evidence of market demand or user research
- Requires 300-1000 users with no recruitment plan
- Complex audio processing pipeline

**However, this is a WELL-THOUGHT-OUT proposal:**
- Quality control mechanisms are excellent
- Technical architecture is detailed and appropriate
- Team clearly understands the domain
- Features are well-justified

**What would have happened:**
- Week 1-2: Build basic web audio recording + upload
- Week 3: Realize mobile is needed for accurate geolocation
- Week 4: Panic about scope, cut most features
- Week 5: Have basic prototype with 10 test recordings
- Result: Technically impressive demo but no real users or validation

**This is a project that could work as:**
- A startup with 6-12 months and funding
- A master's thesis project
- A well-resourced capstone with full semester
- **Not** a 5-week course project

---

## Hidden Gem Potential?

**YES - Strong concept with excellent planning, but needs 80% descope**

**The Core Insight is Interesting:**
- Soundscapes DO affect productivity, mood, and experience
- Audio is an underexplored dimension of place
- Crowdsourcing could capture ephemeral atmospheric data
- Creative/artistic angle is appealing

**This team clearly has strong skills:**
- Technical sophistication (audio processing knowledge)
- Thoughtful quality control design
- Comprehensive feature planning
- Understanding of gamification and motivation

**How It Could Have Worked:**

### Pivot: "Penn Campus Soundmap"

**Radical descope to Penn-only, web-only MVP:**

1. **Hyperlocal Focus:**
   - Penn campus only (not global)
   - Target: Penn students exploring study spots
   - 50-100 locations maximum (Van Pelt, Pottruck, cafés, quads)
   - Can seed data yourself by walking around campus

2. **Web-Only (No Mobile App):**
   - Record audio via browser (Web Audio API)
   - Manual location selection from dropdown (no GPS)
   - "Where are you? [Van Pelt L2, Huntsman Hall, Hill College House]"
   - Eliminates 3 weeks of mobile development

3. **No ML Initially:**
   - Simple tagging only ("Quiet", "Moderate", "Loud", "Social", "Focused")
   - Crowd consensus via voting
   - Basic statistics (average rating, # submissions)
   - Add audio similarity later if time permits

4. **Simplified Audio Processing:**
   - Just volume level detection (loud vs. quiet)
   - No frequency analysis, no ML clustering
   - Basic format conversion (existing libraries)
   - Focus on usability, not sophistication

5. **Concrete Recruitment:**
   - Promote in Penn Course Review, Canvas announcements
   - Partner with student gov or residential programs
   - "Find your perfect study spot on campus"
   - Offer small prize for most contributions

6. **Minimal Features (3-4 only):**
   - MUST HAVE: Audio upload, location tag, search/browse map
   - SHOULD HAVE: Volume level display, crowd voting
   - COULD HAVE: Daily challenges, badges
   - WON'T HAVE: Mobile app, ML clustering, API, analytics

**This version could score 22-24/30:**
- Feasibility: 4/5 (web-only, simpler processing)
- Viability: 4/5 (Penn students need study spots)
- Incentives: 3/5 (useful + mild gamification)
- Scope: 5/5 (achievable in 5 weeks)
- Recruitment: 4/5 (Penn channels identified)
- QC: 3/5 (simpler validation)

**Alternative Pivot: "Daily Soundscape Challenge"**

Focus on the creative/artistic angle, not utility:

1. **Daily Theme:** "Capture the most peaceful sound today"
2. **Gallery Format:** Display submissions with play button
3. **Community Voting:** Upvote favorite soundscapes
4. **Winner Showcase:** Daily winner gets featured
5. **No Map:** Just chronological gallery with tags
6. **Instagram-Style:** Social, shareable, creative

---

## Key Lessons

### What Killed This Project:
1. **Mobile Requirement:** Geo-located audio essentially requires mobile app (3-4 weeks alone)
2. **Global Ambition:** "Global map" vs. starting hyperlocal
3. **ML Complexity:** Audio similarity clustering is advanced and unnecessary for MVP
4. **Feature Creep:** 8 major features when 3-4 would suffice
5. **Unclear Market:** No evidence people want this (cool concept ≠ real demand)
6. **Scale Requirements:** Need 300-1000 users for value, but no recruitment plan

### What Could Have Saved It:
1. **Hyperlocal Start:** Penn campus only, not global
2. **Web-Only:** Avoid mobile development complexity
3. **Manual Location:** Dropdown selection, not GPS
4. **No ML Initially:** Simple tagging and voting
5. **Utilize Problem:** "Find study spots" vs. abstract soundscape exploration
6. **Seed Data:** Team records 30-50 locations themselves
7. **Ruthless Descope:** 3 features, not 8

---

## Summary

Soundscape is one of the most technically sophisticated and well-planned proposals in the dropped set. The quality control section alone demonstrates significant expertise. However, it suffers from massive overscope and unclear market demand.

With a 15/30 score, it falls into "Needs Major Revision" territory. The gap between the proposed system and what's feasible in 5 weeks is enormous.

**Was it right to drop?** Yes. This is a 6-12 month startup project, not a 5-week course project. The mobile requirement alone disqualifies it.

**Hidden gem potential: HIGH.** This team clearly has strong technical skills and thoughtfulness. With an 80% descope (Penn-only, web-only, no ML, 3 features), this could have been a B+/A- project.

**The fatal flaw:** Trying to build a production-ready platform (web + mobile + ML + gamification + analytics) instead of a working prototype that proves one core concept.

**Bottom Line:** Excellent planning and technical understanding, but completely unrealistic scope. Needed to pick ONE aspect (web audio map OR mobile geo-tagged recording OR ML similarity OR gamification) and build only that. Instead, tried to build everything.

**Instructional Value:** This is a great example of how good engineers can overscope by underestimating integration complexity. Each component seems manageable in isolation, but together they compound. A valuable lesson in ruthless prioritization.
