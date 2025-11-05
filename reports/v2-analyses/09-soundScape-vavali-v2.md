# SoundScape - Project Viability Analysis (V2)

**Project**: SoundScape
**Authors**: Vedha Avali (vavali), Leha Choppara (lehac), Nathan Lee (nzlee)
**Analysis Date**: 2025-11-02
**Proposal Version**: Round 3

---

## VIABILITY SCORE BREAKDOWN

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| **1. Technical Feasibility** | 2/5 | Massive scope: web + mobile apps, audio processing (SNR, MFCC, perceptual hashing), ML clustering, worker queues, Firebase + PostgreSQL. This is 6-12 month scope compressed into 5 weeks. Audio QC pipeline alone (clipping detection, silence ratio, duplicate detection via embeddings) is week-long subsystem. |
| **2. Crowdsourcing Viability** | 2/5 | Novel acoustic dimension is genuinely differentiated, but value proposition unclear for casual users. Empty map problem (need clips to be useful, need usefulness to attract clips). No evidence of user interest testing. Competing with low-friction alternatives (Instagram stories, TikTok for sharing sounds). |
| **3. Incentive Design** | 2/5 | Task is moderately quick (record 10-30s clip + tags = 2-5 min), but tedious and lacks intrinsic fun. Gamification cited (Octalysis) but badges/leaderboards unlikely to motivate strangers to repeatedly record ambient sounds. Zero budget ($0.00/task) for 150+ submissions. Why would people do this? |
| **4. Scope Appropriateness** | 1/5 | 8 key features, each 1-2 weeks of work: geo-tagged uploads, mood tagging, interactive map, crowd verification, daily challenges, reputation system, similarity clustering, open API. Plus sophisticated audio QC pipeline. This is a funded startup, not a 5-week student project. |
| **5. Recruitment Strategy** | 2/5 | Generic "Penn students, social media campaigns, local volunteers" without specifics. Mentions tourism board partnerships (aspirational). No concrete channel commitments. Target of 100-500 workers unrealistic with zero budget and weak intrinsic motivation. |
| **6. Quality Control** | 3/5 | Most sophisticated QC section of any proposal—perceptual hashing, SNR thresholds, geolocation validation, duplicate detection, trusted listener escalation. However, building this QC pipeline is itself a multi-week project. QC is over-engineered for pilot scale (100 clips). |
| **TOTAL** | **12/30** | **Stop and Pivot** |

---

## EXECUTIVE SUMMARY

SoundScape is a conceptually novel and well-documented crowdsourced audio mapping platform with genuine differentiation (acoustic exploration) and impressive attention to technical detail. However, **the project is fundamentally overscoped by 300-400%** for a 5-week timeline. The team is attempting to build a cross-platform app with professional-grade audio processing, ML-based clustering, sophisticated QC pipelines, and gamified engagement systems—a scope appropriate for a funded 6-month startup sprint, not a student course project. Additionally, **incentive design is critically weak**: the team assumes strangers will repeatedly record and upload ambient sounds for badges and leaderboard positions without any evidence of demand or testing. With zero budget for acquisition and vague recruitment plans, the project faces both a **cold-start problem** and **sustained engagement problem** that gamification alone cannot solve.

---

## DETAILED ASSESSMENT

### 1. Technical Feasibility (2/5)

**Stated Technical Components**:
- Frontend: React + Tailwind (web) AND React Native/Expo (mobile app)
- Backend: Python FastAPI + Node/Express + Firebase Firestore + PostgreSQL warehouse
- Audio processing: Worker queue + Python services using librosa/pydub/ffmpeg for feature extraction
- ML: Scikit-learn + optional PyTorch for clustering/similarity
- External: Mapbox GL, OpenStreetMap, optional MTurk/Prolific adapters
- QC Pipeline: SNR estimation, clipping detection (>10% frames threshold), silence ratio (>80%), perceptual hashing (MFCC/chroma/CLAP embeddings), duplicate detection (cosine similarity >0.95)

**Why This Is 2/5 (Very Risky)**:

Each of these is a significant subsystem:

1. **Audio recording and upload** (1 week): Web Audio API for browser recording, React Native for mobile, file validation, format transcoding to mono 16kHz, loudness normalization (EBU-R128)

2. **Geolocation + mapping** (1 week): GPS validation, spoofing detection ("sensor consistency checks"), Mapbox integration with color-coded pins, clustering for dense areas

3. **Audio QC pipeline** (1.5 weeks): SNR calculation from noise floor, clipping detection, silence detection, perceptual hashing for duplicates, worker queue management

4. **Crowd verification system** (1 week): Multi-worker rating interface, weighted majority voting with reputation weighting, consensus thresholds, dispute resolution escalation

5. **Gamification backend** (1 week): User profiles, points/badges/leaderboards, daily challenge system, reputation tracking

6. **ML similarity clustering** (1.5 weeks): Audio feature extraction (MFCCs, chroma), embeddings, clustering algorithm, similarity API endpoint

7. **Open API and analytics** (0.5 week): Data export, aggregation for researchers/planners

**Total: ~7.5 weeks of work for experienced team, 10-15 weeks for students learning these technologies**

**Critical Technical Risks**:
- Audio processing is a specialized domain—team may underestimate difficulty of SNR estimation, perceptual hashing, and format normalization
- Mobile app development adds 3-4 weeks alone and requires platform-specific expertise
- Cross-platform (web + mobile) requires maintaining two codebases or complex shared logic
- Worker queues and async processing introduce operational complexity (monitoring, failure handling)
- PostgreSQL warehouse + Firebase Firestore suggests unclear data architecture (why both?)
- ML clustering is premature optimization—system doesn't need similarity features to validate crowdsourcing concept

**Verdict**: Scope is 3-4x too large for 5 weeks. Team will spend weeks on infrastructure and never reach crowdsourcing validation. Classic "let's build everything" trap.

---

### 2. Crowdsourcing Viability (2/5)

**Strengths**:
- Genuinely novel dimension (sound) that existing mapping platforms don't cover
- Some legitimate use cases: urban planners, sound-sensitive individuals, remote workers seeking ambiance
- Educational/research value: acoustic datasets for environmental science or accessibility research

**Concerns**:

**Cold-start problem**:
- An empty or sparse sound map has no value to end users
- But workers won't contribute without seeing existing value or community
- "Seeding strategy" not mentioned in proposal

**Unclear value proposition for casual users**:
- Who is the target end user? Document states "remote workers, travelers, urban planners, musicians, game designers, those with sensitivity to sounds"—this is 6 different personas with different needs
- What problem does this solve that simpler tools don't? (Instagram/TikTok for sharing sounds, Yelp for café ambiance reviews, Google Maps for crowdedness)
- Why would someone browse a sound map? Novelty, yes, but sustained usage?

**Competing alternatives**:
- Existing sound databases (Freesound, BBC Sound Effects, Soundcities archive) for creative users
- Social media (Instagram stories, TikTok) for casual ambient sharing
- Google Maps' "busy times" feature + reviews mentioning "quiet" or "loud" for practical use

**No evidence of demand**:
- No user interviews mentioned
- No testing of value proposition with potential users
- No proof that people want to explore cities through sound (vs. visuals, reviews, or personal visits)

**Verdict**: Conceptually interesting but no validation that users want this. Novelty doesn't equal utility. High risk of building something impressive but unused.

---

### 3. Incentive Design (2/5)

**Task Analysis**:
- Recording 10-30s ambient clip: 30-60 seconds
- Navigating to upload form, adding tags (mood, environment), confirming location: 1-2 minutes
- Listening to others' clips for verification: 1-2 minutes per clip
- **Total task time: 2-5 minutes per contribution**

**Stated Incentives**:
- Gamified points, badges, and leaderboards
- Recognition as "top Sound Explorer"
- Themed challenges (e.g., "Quietest Spot on Campus Week")
- "Visible impact" (contribution appears on global map)
- "Emotional reward for users who enjoy sharing pieces of their environment"

**Why This Is 2/5 (Mismatch)**:

According to the rubric:
- **Task 2-10 min + tedious**: Need payment or strong intrinsic motivation
- **Task enjoyment**: Recording ambient sounds is not inherently fun for most people (unlike games, social voting, creative expression)
- **Badges/leaderboards work when**: Users are already committed, or task is very quick (<30 sec), or there's strong existing community

**Problems**:
1. **Zero budget** ($0.00/task, $0.50/worker for raffle) for 150+ verified submissions = asking for ~$300-500 of labor for free
2. **Weak intrinsic motivation**: Most people don't enjoy recording ambient sounds as hobby. This isn't like rating hot-or-not (fun) or reviewing restaurants (useful to them). It's data collection work.
3. **No personal utility**: Contributors don't benefit from their own recordings (unlike mood tracking or journaling). All value goes to future users.
4. **Cold community**: Without existing engaged users, leaderboards and badges feel hollow ("I'm #1 of 3 people")

**Comparison to Successful Crowdsourcing**:
- Wikipedia: Contributors get ownership, expertise demonstration, ideological alignment ("free knowledge")
- reCAPTCHA: Task is 2 seconds, blocking access to something users want
- MTurk: Direct payment for tedious work
- Geocaching: Treasure hunt game mechanic makes finding locations intrinsically fun
- SoundScape: Asks for tedious data collection with weak gamification and no payment

**Verdict**: Incentives do not match task difficulty. Gamification cited but not compelling for this use case. Without payment or captive audience, recruitment will fail.

---

### 4. Scope Appropriateness (1/5)

**Feature Count Test**: 8 key features listed, but several are major subsystems:

1. Geo-tagged audio uploads: Recording interface + file handling + GPS tagging + storage = 1 week
2. Mood & environment tagging: UI + database schema + validation = 0.5 week
3. Interactive sound map: Mapbox integration + color-coding + clustering = 1 week
4. Crowd verification & rating: Multi-worker interface + voting logic + aggregation = 1 week
5. Daily sound challenges: Challenge creation system + notifications + tracking = 1 week
6. Gamified reputation system: User profiles + points + badges + leaderboards = 1 week
7. Sound similarity discovery: ML clustering pipeline = 1.5 weeks
8. Open data & API access: Data export + API endpoints + documentation = 0.5 week

**Total: 7.5 weeks**, assuming no bugs, no learning curve, and perfect execution.

**Additional Hidden Scope**:
- Mobile app (mentioned in tech stack): +3-4 weeks
- Audio QC pipeline (detailed in QC section): +1.5 weeks
- Worker queue infrastructure: +0.5 week
- Trusted listener escalation system: +0.5 week

**Actual Total: ~13 weeks of work**

**Two-Week Test**: "Could you build working core loop in 2 weeks?"
- Core loop = record clip → upload with tags → display on map → crowd verification
- Realistically: Week 1 (recording + upload infrastructure), Week 2 (basic map display). Verification, gamification, QC, and ML would all be cut.
- Answer: Barely, and only if mobile app, sophisticated QC, and all gamification are cut.

**Manual Simulation Test**: "Could you manually simulate the system before building it?"
- Yes—team could manually record 20-30 clips, tag them, plot on Google My Maps, and have friends rate them.
- This would test value proposition and feasibility.
- **Proposal does not mention piloting or manual testing**—goes straight to full-stack implementation.

**Must-Have Features Test**: "Can you name exactly 3-4 must-have features?"
- Proposal lists 8 features, none marked as optional.
- Realistic must-haves: (1) Upload audio with location, (2) Display on map, (3) Basic rating/tagging.
- Everything else (gamification, ML clustering, sophisticated QC, challenges) is nice-to-have but treated as essential.

**Verdict**: Massively overscoped. This is a product roadmap for a funded startup's first 6 months, not a 5-week class project. Team needs to cut 70% of features immediately.

---

### 5. Recruitment Strategy (2/5)

**Stated Strategy**:
- Penn students
- Local volunteers in Philadelphia area
- Social media campaigns
- Partnerships with student organizations
- Local tourism boards

**Scale Requirements**:
- Minimum: 100 workers
- Target: 500 workers
- Potential: 1,000 workers

**Why This Is 2/5 (Vague Hope)**:

**Specificity Test**: "Can you NAME the exact groups/places?"
- ❌ No specific Penn student orgs named
- ❌ No specific social media channels or accounts
- ❌ "Local tourism boards" is completely aspirational—securing tourism board partnership takes months
- ❌ "Social media campaigns" without budget or influencer access is magical thinking

**Testing**: "Have you TESTED recruitment?"
- ❌ No evidence of posting anywhere
- ❌ No user interviews or interest validation
- ❌ No proof-of-concept with friends

**Cold-Start**: "Do you need >50 people to start?"
- ✅ Yes—empty sound map has no value, so you need critical mass before launching publicly
- ❌ No seeding strategy described (will team create initial clips?)

**Backup Plan**:
- Mentions "optional MTurk/Prolific adapters" but budget is $500 total
- At $1-2 per recording task, this affords 250-500 recordings—potentially viable but would consume entire budget
- Would still need verification tasks, which would also need payment

**Comparison to Concrete Strategy** (from rubric 5/5 example):
- Bad: "Social media campaigns, word of mouth" (SoundScape's approach)
- Good: "My dorm's GroupMe (200 people), already talked to RA"

**Verdict**: Recruitment is generic and untested. No concrete channel access, no partnerships secured, no proof of demand. Will likely fail to recruit 100+ unpaid workers.

---

### 6. Quality Control (3/5)

**Strengths**:
This is the most impressive section of the proposal. Team has thought deeply about audio-specific QC challenges:

- **Pre-submission guardrails**: Duration enforcement (10-30s), clipping detection (>10% frames rejected), silence detection (>80% silence rejected), SNR thresholds (>5dB)
- **Format normalization**: Transcode to mono 16kHz, loudness normalization (EBU-R128)
- **Geo validation**: GPS within 30m of device reading, spoofing detection via sensor consistency, IP geolocation cross-check
- **Duplicate detection**: Perceptual hashing with MFCC/chroma/CLAP embeddings, cosine similarity >0.95 threshold
- **Abuse prevention**: Rate limits (≤10 uploads/day), CAPTCHAs after bursts, shadow-banning for anomalies
- **Redundancy**: 3-5 workers per clip for verification
- **Reputation weighting**: High-accuracy users' votes weighted more heavily
- **Expert escalation**: Top-reputation users resolve ties and edge cases

**Concerns**:

1. **QC is itself a multi-week project**: Building SNR estimation, perceptual hashing, and duplicate detection pipeline is 1-2 weeks of work. For 100-clip pilot, this is massive over-engineering.

2. **Premature optimization**: System doesn't need sophisticated audio analysis for initial validation. Simple checks (file size, duration, format) plus manual review would suffice for pilot.

3. **Trust in automation**: Proposal assumes audio ML works reliably, but these systems have edge cases (e.g., MFCC embeddings may not catch similar-but-not-duplicate recordings)

4. **Human QC logistics**: 3-5 workers per clip × 150 clips = 450-750 verification tasks. At 2 min each, that's 15-25 hours of work. Where do these verifiers come from? (Same recruitment problem as primary contributions.)

5. **Expert listener pool**: "Top-reputation users" assumes system already has established users with track records. How do you bootstrap this in week 1?

**Recommendations**:
- For pilot: Use simple automated checks (duration, file size) + manual team review for first 50 clips
- Add crowd verification only after proving people will upload clips
- Build sophisticated QC pipeline only if project scales beyond course

**Verdict**: QC strategy is impressively detailed but over-engineered for pilot scale. Team should spend less time designing QC and more time validating that anyone will contribute at all.

---

## RISK ANALYSIS

### Top 3 Risks & Mitigations

#### Risk 1: Scope Explosion Prevents Completion (Critical, ~90% probability)
**Impact**: Team spends all 5 weeks building infrastructure (audio processing, mobile app, worker queues, ML clustering) and never reaches crowdsourcing validation stage. Demo shows impressive technical work but no real user contributions or data.

**Why it's likely**: Proposal describes 13+ weeks of engineering work. Team will hit technical blockers (audio processing is harder than expected, mobile development takes longer, etc.) and run out of time.

**Mitigation**:
- **Cut 70% of scope immediately**:
  - ❌ Mobile app → Web only
  - ❌ Sophisticated QC pipeline → Manual review + basic duration checks
  - ❌ ML clustering → Manual tagging
  - ❌ Worker queues → Synchronous processing
  - ❌ Daily challenges system → Manual admin posts
  - ❌ Reputation/leaderboard backend → Simple CSV tracking
  - ❌ Open API → Manual data export if needed

- **Build horizontal slice**: Record → upload → display on map → manual verification. This is 2 weeks. Add features only if time permits.

- **Manual simulation first**: Before writing any code, team should manually test value proposition:
  - Record 20-30 clips yourselves around campus
  - Plot on Google My Maps with mood tags
  - Show to 10-15 potential users and ask: "Would you explore this? Would you contribute?"
  - If answer is lukewarm, pivot before investing in platform

**Backup**: If team insists on keeping scope, treat this as technical portfolio project (not crowdsourcing validation) and grade accordingly. Acknowledge in proposal that focus is on platform engineering, not crowd participation.

**Consequence if unaddressed**: Week 5 demo shows polished but empty platform with 10-15 team-recorded clips. Grade: B-/C+ for technical ambition but failed crowdsourcing validation.

---

#### Risk 2: Zero Participation Despite Platform Completion (Critical, ~80% probability)
**Impact**: Even if team builds working platform, nobody contributes because (a) recruitment is vague, (b) incentives are weak, (c) value proposition is unclear.

**Why it's likely**: $0 budget for contributions, no concrete recruitment channels, no tested demand, tedious task with weak gamification. Even successful gamified crowdsourcing (Foldit, Zooniverse) has strong intrinsic motivation (science contribution, puzzle-solving). SoundScape asks for data collection labor with unclear personal or social benefit.

**Mitigation**:

**Option A: Add budget**:
- Allocate $200-300 of $500 budget to paying for initial contributions
- MTurk/Prolific: $1-2 per recording + tags = 100-150 paid recordings
- Use remaining $200 for hosting and raffle incentives for organic users
- Seed platform with paid data to demonstrate value, then see if organic users follow

**Option B: Find captive audience**:
- NETS 2130 class requirement (60 students × 3 recordings each = 180 clips)
- Psychology research participant pool (offer 0.5 credits per 5 contributions)
- Partner with specific course (Architecture, Urban Planning, Music) where acoustic data is relevant to coursework

**Option C: Radically simplify task**:
- Instead of recording+tagging+location, just "vote on these pre-recorded clips: is this sound calming or energizing?"
- Pre-record 100 clips yourselves, crowdsource the tagging/rating only
- This reduces task time from 2-5 min to 15-30 seconds, making gamification viable

**Option D: Pivot to annotation instead of creation**:
- Use existing sound databases (Freesound.org has 500k+ sounds)
- Crowdsource mood/environment tagging of existing clips
- Build the map with existing data, crowdsource the metadata
- Much lighter task (listen + tag = 30 sec) and solves cold-start problem

**Backup**: If no mitigation chosen, accept that team will recruit 20-30 participants (mostly friends) and demo will be proof-of-concept, not validated crowdsourcing system.

---

#### Risk 3: Audio Processing Technical Debt Blocks Progress (High, ~70% probability)
**Impact**: Team underestimates difficulty of audio processing, gets stuck debugging SNR calculations or perceptual hashing, loses 1-2 weeks, falls behind on core features.

**Why it's likely**: Audio signal processing is specialized domain. Tasks like "estimate SNR via noise floor from lowest-energy percentile" or "compute MFCC embeddings for duplicate detection" sound simple but have edge cases, require library expertise (librosa/pydub), and need parameter tuning. Team may not have audio engineering experience.

**Mitigation**:

**Simplify audio processing**:
- Accept uploads in standard formats (MP3, M4A) without transcoding
- Basic validation: file size 100KB-5MB, duration 10-30s (read from file metadata)
- No SNR calculation, no clipping detection, no normalization—just store and serve files
- Manual review by team for quality (listen to first 50 submissions yourself)

**Defer duplicate detection**:
- For 100-clip pilot, duplicates unlikely to be major problem
- If needed, use simpler hash (MD5 of file content) to catch exact duplicates
- Perceptual hashing via embeddings is research-grade—overkill for course project

**Use existing services**:
- Consider Cloudinary or similar media management service that handles audio validation/processing automatically
- More expensive but saves weeks of custom development

**Backup**: If audio processing becomes blocker, pivot to text-based version: users describe sounds in words ("busy coffee shop, moderate chatter") instead of uploading recordings. Test crowdsourcing mechanics without audio complexity.

---

## DECISION GUIDANCE

### Verdict: STOP AND PIVOT (Score: 12/30)

**Overall Assessment**: SoundScape is **not feasible as described** for a 5-week course project. The scope is 3-4x too large (13+ weeks of development), the incentive design is critically weak (unpaid tedious work with weak gamification), and the recruitment strategy is vague and untested. This is a well-researched idea with genuine novelty, but the team is attempting to build a funded startup in 5 weeks rather than validating a crowdsourcing concept.

---

### Critical Changes Required

**The team must choose ONE of these paths**:

### Path 1: Radical Descoping (Recommended)
**Make this a 2-week technical core + 3-week validation project**:

**KEEP**:
- Web-only upload form (no mobile)
- Basic Mapbox display with pins
- Simple tagging (mood + environment dropdowns)
- Manual team review of submissions

**CUT**:
- Mobile app
- Audio QC pipeline (SNR, perceptual hashing, etc.)
- ML clustering
- Worker queues
- Sophisticated gamification (keep simple points only)
- Daily challenges system
- Open API
- Trusted listener escalation

**Focus validation effort on**:
- Can we get 50-100 people to submit clips?
- Does anyone actually explore the map?
- Is the data useful or interesting?

**Budget**: Allocate $200-300 for paid pilot contributions via MTurk to seed platform

**Target**: 80-120 total recordings, 30-50 organic contributors, clear patterns on map

**Grade potential**: B+ to A- if validation succeeds, B- if participation is weak

---

### Path 2: Pivot to Annotation (Recommended Alternative)
**Change from creation to curation**:

- Use existing sound libraries (Freesound, BBC Sound Effects)
- Pre-load 100-200 ambient clips (cafés, parks, streets, etc.)
- Crowdsource mood + environment tagging of existing clips
- Build the map with existing audio, crowd provides metadata

**Advantages**:
- Solves cold-start problem (map is pre-populated)
- Much lighter task (listen 15s + tag = 30-45 seconds)
- Gamification more viable for quick tasks
- Removes audio processing complexity
- Still validates crowdsourcing aggregation and quality control

**Changes needed**:
- Week 1: Source and organize 100-200 clips
- Week 2-3: Build tagging interface and map display
- Week 4-5: Recruit taggers and aggregate results

**Target**: 500-1000 tags from 80-120 workers

**Grade potential**: A-/B+ if well-executed

---

### Path 3: Treat as Technical Project (Not Recommended)
**Accept this is platform engineering, not crowdsourcing validation**:

- Acknowledge in proposal that focus is on technical infrastructure
- Build impressive audio processing pipeline and mapping system
- Accept that participation will be minimal (team + friends only)
- Evaluate on technical merit rather than crowd engagement

**Consequence**: Grade will reflect limited crowdsourcing validation (C+/B- range) even if technical work is strong.

---

### Predicted Outcomes

#### Scenario A: Team Radically Descopes (30% probability)
- **Week 1-2**: Build simple web upload + map display
- **Week 3**: Soft launch with paid MTurk seed data (50-80 clips)
- **Week 4**: Targeted promotion to Penn students; 30-50 organic contributions
- **Week 5**: Demo with 100-130 total clips, meaningful patterns visible
- **Grade**: B+ to A- range—demonstrates pragmatic scope management and crowdsourcing validation
- **Learning**: Sometimes simple, working systems beat complex, incomplete ones

#### Scenario B: Team Pivots to Annotation (20% probability)
- **Week 1**: Source existing clips, organize by location
- **Week 2-3**: Build tagging interface and aggregation
- **Week 4-5**: Recruit 80-120 taggers, collect 500-1000 tags
- **Grade**: A-/B+ range—validates crowdsourcing principles with lighter task
- **Learning**: Annotation tasks are more viable than creation tasks for volunteer crowds

#### Scenario C: Team Reduces Scope But Not Enough (40% probability)
- Cuts mobile app and some QC, but keeps too many features
- Weeks 1-3 spent on infrastructure
- Week 4 realization that recruitment is failing
- Week 5 demo with 20-30 clips (mostly team members)
- **Grade**: B-/C+ range—technical competence but weak crowdsourcing demonstration

#### Scenario D: Team Proceeds As Planned (10% probability)
- Attempts full scope
- Gets bogged down in audio processing or mobile development
- Week 5 demo shows partial platform with no user data
- **Grade**: C+/C range—overambitious scope prevented completion

---

## COMPARISON TO V1 ANALYSIS

### What Changed from Round 2 to Round 3?

**Improvements**:
- ✅ Added Nathan Lee as Round 3 contributor (team growth)
- ✅ Massively expanded QC section with specific audio processing thresholds (SNR >5dB, clipping >10%, silence >80%)
- ✅ Added detailed aggregation method (weighted majority voting with reputation weights)
- ✅ Expanded ethical considerations with concrete mitigation strategies
- ✅ Added steel-man discussion comparing to alternative idea (Where2Go)
- ✅ Clarified use cases and end-user personas

**Unresolved Issues from V1**:
- ❌ Scope remains massively overambitious (V1: "3-4x too large", V2: still 13+ weeks of work)
- ❌ Recruitment strategy still vague ("social media campaigns" without specifics)
- ❌ Incentive design unchanged (still $0 budget, still assumes badges will work)
- ❌ No pilot testing or validation of value proposition
- ❌ Mobile app still included despite V1 warning about adding 3-4 weeks

**New Concerns Introduced**:
- ⚠️ Even more ambitious QC pipeline added (perceptual hashing, CLAP embeddings, trusted listener escalation)
- ⚠️ PostgreSQL warehouse added to tech stack (on top of Firebase Firestore—why both?)
- ⚠️ Optional PyTorch mentioned (additional complexity)

### V1 vs V2 Scoring Comparison

| Dimension | V1 Score | V2 Score | Change | Notes |
|-----------|----------|----------|--------|-------|
| Technical Feasibility | 2/5 | 2/5 | → | Scope remains critically overambitious; added more complexity |
| Crowdsourcing Viability | 3/5 | 2/5 | ↓ | Use cases clarified but still no validation; cold-start unaddressed |
| Incentive Design | 2/5 | 2/5 | → | No improvement; still $0 budget with weak motivation |
| Scope Appropriateness | 1/5 | 1/5 | → | **Still massively overscoped; added features not cut** |
| Recruitment Strategy | 2/5 | 2/5 | → | Still vague; "social media campaigns" without specifics |
| Quality Control | 3/5 | 3/5 | → | More detailed but over-engineered for pilot scale |
| **TOTAL** | **13/30** | **12/30** | ↓ | **Slight decline; added complexity without addressing core issues** |

### V1 Verdict vs V2 Verdict

**V1 Verdict**: "WEAK GO - Needs Scope Reduction"

**V2 Verdict**: "STOP AND PIVOT"

**Why the downgrade?**: V1 analysis gave benefit of doubt that team might descope during refinement. Round 3 proposal instead added more complexity (PostgreSQL warehouse, enhanced QC pipeline, PyTorch) without cutting any major features. Team has not internalized scope problem. At 12/30, this crosses threshold from "needs revision" to "not feasible"—requires fundamental pivot, not just trimming.

---

### Key Takeaway

**The team is confusing "thorough documentation" with "feasible execution."** Round 3 added impressive technical detail (QC thresholds, aggregation formulas, ethical frameworks) but did not address the operational reality that this project is too large and lacks validated demand.

**What V1 Analysis Predicted**: "Weeks 1-2 infrastructure setup, week 3 realize audio processing harder than expected, week 4 no users, recruit friends, week 5 polish demo. Show functional map with 25-40 clips mostly around campus."

**Current V2 Assessment**: This prediction remains accurate. Despite enhanced documentation, the project trajectory has not changed because **the fundamental scope and incentive problems remain unresolved**.

---

### Comparison to V1 Critical Change Request

**V1 Requested**: "Cut scope by 70% immediately. Simple web form (not mobile) to upload MP3 + location + tags. MapBox showing pins. Manual QC by team (not ML). 30-50 clips around campus."

**V2 Actual Changes**: Added PostgreSQL warehouse, expanded QC pipeline with more audio signal processing, kept mobile app, added more ML features (PyTorch).

**Result**: Team moved in the opposite direction—added complexity instead of simplifying.

---

## RECOMMENDATION

**This project cannot succeed as currently described.** The team must make a fundamental choice:

### Option 1: Accept Scope Reality
- Cut mobile app, ML pipeline, sophisticated QC, and gamification backend
- Build simple web upload + map in 2 weeks
- Allocate $250 to seed with paid MTurk data
- Focus validation on: Can we demonstrate geographic mood patterns from crowd-tagged sounds?
- **Grade potential**: B+ to A- if executed well

### Option 2: Pivot to Annotation
- Use existing sound databases
- Crowdsource tagging/mood classification only
- Lighter task → better engagement
- Solves cold-start problem
- **Grade potential**: A-/B+ if validation succeeds

### Option 3: Treat as Technical Showcase
- Acknowledge this is platform engineering project
- Accept minimal crowd participation
- Evaluate on technical sophistication
- **Grade potential**: C+/B- (weak crowdsourcing demonstration)

**Do not proceed with current scope.** It will result in an impressive but incomplete technical demo with no crowdsourcing validation.

---

**If team insists on current scope despite analysis**, instructor should require:
1. Milestone 1 (Week 2): Working upload + display (no QC, no mobile, no ML)
2. Milestone 2 (Week 3): 30 real user contributions or pivot required
3. Weekly scope reviews with TA to enforce descoping

**Otherwise, this project will consume 5 weeks and produce a beautiful failure.**

---

**Analysis by**: Claude Sonnet (NETS 2130 Project Evaluation)
**Viability Score**: 12/30 (Stop and Pivot)
**Recommendation**: Fundamental redesign required; do not proceed with current plan
