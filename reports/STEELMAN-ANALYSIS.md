# Steelman Analysis: Round 3 Projects
## NETS 2130 Fall 2025 - Building Up Your Best Ideas

**Purpose**: Present the STRONGEST possible version of each project, identify concrete pathways to success, and provide multiple options for addressing limitations.

**Philosophy**: Every project here has merit. The question isn't "is this viable?" but rather "what's the best path to make this work?"

---

## How to Use This Document

1. **Find your project** in the list below
2. **Read the Strengths** - understand what's working
3. **Review the Limitations** - acknowledge the challenges
4. **Explore the Pathways** - pick the approach that fits your constraints
5. **Choose a Scope** - select MVP, Standard, or Ambitious based on Week 1 results
6. **Execute** - commit to one pathway and scope by end of Week 1

---

# Projects by Theme

## Theme Index

**Data & Social Good** (4 projects):
- [AgriAid](#agriaid---crowdsourced-agricultural-disaster-assessment) - Satellite imagery labeling for humanitarian aid
- [TerraTruth](#terratruth---crowdsourced-environmental-monitoring) - Environmental change tracking
- [MoodMap@Penn](#moodmappenn---campus-emotional-geography) - Mental health awareness mapping
- [StreetEats](#streeteats---food-truck-discovery-platform) - Food access information

**Creative & Content Generation** (2 projects):
- [TripTuner](#triptuner---crowdsourced-travel-itineraries) - Travel recommendation curation
- [SoundScape](#soundscape---crowdsourced-audio-environment-map) - Ambient sound library

**Peer Review & Feedback** (2 projects):
- [PitchPeer](#pitchpeer---startup-pitch-feedback-platform) - Entrepreneurship feedback
- [Urban Explorer](#urban-explorer---campus-event-discovery) - Event discovery and reviews

**Community & Social Coordination** (2 projects):
- [Kinnect](#kinnect---social-fitness-challenges) - Fitness accountability
- [MoodMap@Penn](#moodmappenn---campus-emotional-geography) - (also social good)

---

# Detailed Project Analyses

---

## MoodMap@Penn - Campus Emotional Geography

**Proposal**: `round3/tilian.md`
**Team**: Tilian, Sadia, Julia, Arushi, Liana, Sadia
**Viability Score**: 19/30 (Highest in cohort)

### Summary
A crowdsourced heat map where Penn students pin their current emotional states to campus locations, creating a real-time emotional geography of campus that reveals patterns in mental wellbeing and builds community awareness.

### Dominant Themes
- 🎯 **Prosocial**: Mental health awareness, community building
- 📊 **Creates Dataset**: Temporal-spatial emotional data
- 🤝 **Builds Community**: Shared experience, reducing isolation

### Strengths
1. **Captive Audience**: Penn students are accessible and reachable
2. **Immediate User Value**: See others' emotions, feel less alone, discover support
3. **Low Friction**: 30-second contribution (location + emoji)
4. **Timely Problem**: Mental health is top concern for college students
5. **Simple Tech Stack**: React + Firebase + Mapbox (all well-documented)
6. **Viral Potential**: "I saw my friend's post!" social spreading
7. **Data Value**: Could inform Penn Wellness, counseling services
8. **Privacy-Aware**: Anonymous pins with optional detail
9. **Framework Application**: Explicit Octalysis drives (social influence, unpredictability)
10. **Appropriate Scope**: 8 features, mostly straightforward

### Limitations
1. **Cold-Start Problem**: Empty map has no value, need critical mass (50-100 active users)
2. **Vague Recruitment**: "GroupMe, student orgs" lacks concrete commitments
3. **Privacy Concerns**: Could enable stalking or harassment if not handled carefully
4. **Engagement Drop-Off**: Initial excitement may fade after week 2-3
5. **Data Quality**: Self-reported emotions subjective, could be performative
6. **Moderation Need**: Toxic posts, spam, inappropriate content possible
7. **Platform Fatigue**: "Another app/website to check"
8. **Scope Creep Risk**: Time-decay algorithm, AI insights could distract from core loop

### Pathways Beyond Limitations

#### **Pathway 1: Dorm Floor Pilot** (HIGHEST SUCCESS PROBABILITY)
**Target**: One dorm floor (~40 students) with RA partnership
- **Action**: Contact RAs in team members' dorms THIS WEEK
- **Value Prop to RA**: Mental health engagement tool, floor bonding activity
- **Execution**:
  - Week 1: RA announces in floor GroupMe, mandatory demo at floor meeting
  - Week 2-3: Daily RA reminders, "post your mood before bed" challenge
  - Week 4: Expand to 2-3 more floors if successful
- **Success Metric**: 60% of floor posts at least once, 30% post 3+ times
- **Fixes**: Cold-start (40 people day 1), recruitment (concrete commitment), engagement (RA nudges)

#### **Pathway 2: Class Captive Audience** (HIGH SUCCESS)
**Target**: One large lecture course (100-200 students) with professor partnership
- **Action**: Email 3-5 professors teaching CIS/NETS/PSYC courses THIS WEEK
- **Value Prop**: Extra credit participation, research opportunity for professor
- **Execution**:
  - Week 1: Professor announces, 2 extra credit points for 5+ posts over 3 weeks
  - Weeks 2-4: TAs remind in recitations
  - Week 5: Analyze data for professor's research
- **Success Metric**: 40% of class participates, 10% highly engaged
- **Fixes**: Cold-start (100 people day 1), recruitment (confirmed), incentive (extra credit)

#### **Pathway 3: Event-Based Launch** (MEDIUM SUCCESS)
**Target**: High-traffic campus events (NSO, Spring Fling, Hey Day)
- **Action**: Table at events with QR codes, immediate posting incentive
- **Value Prop**: "See what Penn is feeling RIGHT NOW"
- **Execution**:
  - Week 1: Seed map with team's posts (50+ pins across campus)
  - Week 2: Table at 2-3 events, incentive (enter raffle for $25 gift card per 3 posts)
  - Week 3-4: Viral growth through friend referrals
- **Success Metric**: 200+ users acquired, 30% post more than once
- **Fixes**: Cold-start (seeded), recruitment (direct), engagement (raffle)

#### **Pathway 4: Partnership with Penn Wellness** (LONG-TERM VALUE)
**Target**: Official Penn Wellness endorsement/promotion
- **Action**: Email Penn Wellness with proposal, offer data insights
- **Value Prop**: Anonymous mental health monitoring, intervention opportunities
- **Execution**:
  - Week 0-1: Pitch to Wellness
  - Week 2-3: If approved, promotion via wellness newsletter, counseling center
  - Week 4-5: Share aggregated insights with Wellness
- **Success Metric**: Official endorsement, sustainable user base
- **Fixes**: Legitimacy, recruitment, long-term sustainability

#### **Pathway 5: Gamification Sprint** (ADDRESSES ENGAGEMENT)
**Target**: Maintain engagement after initial excitement
- **Features**:
  - Daily check-in streaks (7-day, 30-day badges)
  - "Mood Forecasting" - predict campus mood for next day, see if you're right
  - "Mood Twins" - anonymously matched with someone feeling the same way
  - Weekly summary - "Your emotional journey this week"
- **Success Metric**: 40% of Week 1 users still active Week 4
- **Fixes**: Engagement drop-off

#### **Pathway 6: Research Study Framing** (IRB-COMPLIANT)
**Target**: Frame as research study with consent
- **Action**: Submit IRB protocol Week 1
- **Value Prop**: "Contribute to Penn mental health research"
- **Execution**:
  - Recruit as research participants (not just app users)
  - Offer Amazon gift cards for sustained participation ($10 for 20 posts)
  - Publish findings, share with participants
- **Success Metric**: 100+ consented participants, publishable data
- **Fixes**: Incentive (payment), legitimacy, user value

#### **Pathway 7: Moderation Automation** (ADDRESSES SAFETY)
**Target**: Prevent toxic content without manual review
- **Simple Approach**:
  - Profanity filter (block posts with banned words)
  - Rate limiting (max 10 posts per user per day)
  - Report button (3 reports = auto-hide until reviewed)
  - Positive-only pins (only allow certain emotion categories)
- **Success Metric**: <5% of posts require manual review
- **Fixes**: Moderation burden, safety concerns

### Fixable for Scope?
**YES** - This is the most viable project in the cohort.

**Critical Success Factor**: Secure ONE concrete partnership (dorm floor OR class) by end of Week 1. Don't build until you have confirmed commitment.

### Recommended Scopes

#### **MVP (Week 1-2)** - Prove Concept
**Build**:
- Simple React map with Mapbox
- Pin creation (location + 5 emoji options + optional text)
- View pins (click to see details)
- Basic profanity filter

**Skip**:
- User accounts (anonymous only)
- Time decay
- Analytics
- AI insights
- Leaderboards

**Goal**: Demo with 40+ users (one dorm floor), 100+ pins

**Success**: If people use it without prompting after Day 3

---

#### **Standard (Week 3-4)** - Add Engagement
**Add to MVP**:
- User accounts (optional, for streaks)
- 7-day check-in streaks
- Pin lifespan (24-48 hour decay)
- Report button

**Skip**:
- AI mood predictions
- Complex analytics
- Mood matching algorithm

**Goal**: 100+ users, 500+ pins, 20% weekly retention

**Success**: If usage is self-sustaining (no team intervention needed)

---

#### **Ambitious (Week 5+)** - Research Value
**Add to Standard**:
- Weekly mood reports (personal insights)
- Aggregated analytics (patterns by location/time)
- "Mood Twins" matching
- Partnership dashboard for Penn Wellness

**Goal**: 200+ users, 1500+ pins, publishable insights

**Success**: If Penn Wellness requests continued access post-course

---

## StreetEats - Food Truck Discovery Platform

**Proposal**: `round3/bradenj.md`
**Team**: Braden, Jason, Via, Dan, Ryan
**Viability Score**: 17/30

### Summary
A real-time platform showing food truck locations, menus, and crowd-sourced reviews, solving the "where are the trucks today?" problem that plagues hungry students and workers in Philadelphia.

### Dominant Themes
- 🍔 **Creates Value**: Solves real user pain (finding food trucks)
- 📊 **Creates Dataset**: Truck locations, menu info, review data
- 💼 **Business Potential**: Could monetize via truck partnerships

### Strengths
1. **Real Problem**: Food trucks are hard to find, students/workers genuinely frustrated
2. **Dual Value**: Users find trucks, trucks get customers
3. **Simple Tech**: MERN stack, straightforward CRUD operations
4. **Geographic Constraint**: Philadelphia-focused keeps scope manageable
5. **Visual Appeal**: Map-based interface is intuitive and demo-friendly
6. **Data Persistence**: Once seeded, info stays valuable (menus don't change daily)
7. **Sophisticated QC**: 7 mechanisms designed (reputation, photo verification, consensus, velocity)
8. **Network Effects**: More users → better data → more users
9. **Clear User Journey**: See map → find truck → leave review (simple loop)
10. **Team Size**: 5 people can divide work (frontend, backend, mobile scout, data seeding)

### Limitations
1. **Cold-Start Nightmare**: Empty map = useless app, who posts first truck?
2. **Chicken-Egg**: Users won't come without trucks, trucks won't engage without users
3. **Truck Partnership Dependency**: "Backup plan" not primary strategy
4. **High-Effort Updates**: Someone must physically scout trucks daily
5. **Geographic Scope**: City-wide is ambitious for 5 weeks
6. **Stale Data Risk**: Truck locations change, stale pins worse than no pins
7. **Competition**: Google Maps, Roaming Hunger, Street Food Philly exist
8. **Incentive Mismatch**: Posting truck locations = 5-10 min for badges
9. **Vague Recruitment**: "Social media" won't work for operational system
10. **Real-Time Challenge**: "Live tracking" needs constant updates

### Pathways Beyond Limitations

#### **Pathway 1: Truck Partnership First** (HIGHEST IMPACT)
**Target**: 5 food truck operators commit to weekly check-ins
- **Action**: Call/visit 20 trucks THIS WEEK, pitch value prop
- **Value Prop**:
  - "Free marketing to Penn/Drexel students"
  - "We'll build your customer base"
  - "Just text us your location each morning (30 seconds)"
- **Execution**:
  - Week 1: Visit trucks during lunch, get phone numbers
  - Week 2-3: Daily text "Where are you today?" to truck owners
  - Week 4-5: Some trucks start texting proactively
- **Success Metric**: 5 trucks give weekly location updates
- **Fixes**: Cold-start (guaranteed data), partnership (confirmed), data freshness (direct source)

#### **Pathway 2: Penn Campus ONLY** (SCOPE REDUCTION)
**Target**: Just Locust Walk + immediate vicinity (5-block radius)
- **Action**: Map the 8-10 trucks that regularly appear near Penn
- **Execution**:
  - Week 1: Team scouts and seeds ALL campus-area trucks
  - Weeks 2-5: Team updates locations Mon/Wed/Fri before lunch
  - Focus recruitment on Penn students only (class GroupMes, r/UPenn)
- **Success Metric**: Every Penn-area truck on map, 100+ Penn student users
- **Fixes**: Scope (manageable), recruitment (captive audience), data completeness

#### **Pathway 3: Static Menu Directory First** (MVP PIVOT)
**Target**: Build comprehensive menu database before location tracking
- **Action**: De-prioritize real-time locations, prioritize menu info
- **Execution**:
  - Week 1-2: Visit every truck, photograph menus, input data
  - Week 3: Launch with "Find trucks by cuisine/price/diet"
  - Week 4-5: Add location crowdsourcing as secondary feature
- **Success Metric**: 30+ trucks with complete menu data
- **Fixes**: Cold-start (team creates value), user value (even without locations)

#### **Pathway 4: Scheduled Routes Database** (DIFFERENT VALUE PROP)
**Target**: Focus on trucks with regular schedules (not real-time)
- **Action**: Research truck Twitter/Instagram for weekly schedules
- **Execution**:
  - Week 1-2: Document weekly patterns ("Hal's Halal: Mon/Wed/Fri at 34th & Walnut 11am-2pm")
  - Week 3-4: Build schedule view ("What's near me TODAY?")
  - Week 5: Add crowdsourced corrections
- **Success Metric**: 20 trucks with documented schedules
- **Fixes**: Data freshness (schedules change slowly), user value (predictive)

#### **Pathway 5: Gamified Scout Network** (INCENTIVE REDESIGN)
**Target**: Create "scouts" who enjoy hunting trucks
- **Action**: Recruit 10-15 "truck spotters" with meaningful incentives
- **Execution**:
  - Leaderboard: Most trucks spotted weekly
  - Prizes: $25 gift card for top spotter each week (invest $100 total)
  - Social recognition: "Scout of the Week" featured in app
  - Make it a game: "Catch 'em all" Pokemon-style
- **Success Metric**: 10 active scouts posting 5+ trucks per week
- **Fixes**: Incentive (fun + recognition + prizes), data freshness (motivated contributors)

#### **Pathway 6: Instagram Integration** (LEVERAGE EXISTING DATA)
**Target**: Aggregate trucks' own social media posts
- **Action**: Follow 50 Philly trucks on Instagram, scrape locations from posts
- **Execution**:
  - Week 1: Build Instagram hashtag monitor (#PhillyFoodTrucks)
  - Week 2-3: Semi-automated: Team checks Instagram daily, adds locations
  - Week 4-5: Users can submit Instagram links to update locations
- **Success Metric**: 30+ trucks tracked via their own posts
- **Fixes**: Data source (trucks post anyway), effort (less manual scouting)

#### **Pathway 7: Class/Org Partnership** (CAPTIVE USERS)
**Target**: One large Penn organization commits to using app
- **Action**: Email Penn Food Truck Coalition, MERT, UA, PODS
- **Value Prop**: "Centralized truck info for your members"
- **Execution**:
  - Week 1: Get 1 org to promote in newsletter
  - Week 2-3: Org members seed initial usage
  - Week 4-5: Org requests features, becomes core user base
- **Success Metric**: 50+ users from partner org
- **Fixes**: Recruitment (concrete), early adoption (guaranteed)

#### **Pathway 8: Review-First, Location-Second** (PHASE APPROACH)
**Target**: Start as Yelp for trucks (static), add locations later
- **Execution**:
  - Phase 1 (Week 1-2): Directory of 40 trucks with reviews only
  - Phase 2 (Week 3-4): Add crowdsourced "Last seen at..."
  - Phase 3 (Week 5): Add real-time updates if Phase 1-2 work
- **Success Metric**: 50+ reviews before adding location tracking
- **Fixes**: User value (immediate), cold-start (team seeds reviews)

### Fixable for Scope?
**YES WITH MAJOR PIVOT** - Change from "real-time tracking" to "scheduled directory + crowdsourced updates"

**Critical Success Factor**: Get 5 truck partnerships OR pivot to Penn-only campus scope by end of Week 1.

### Recommended Scopes

#### **MVP (Week 1-2)** - Penn Campus Directory
**Build**:
- Map with pins for 10-12 Penn-area trucks
- Static info: Menu, hours, typical locations, photos
- Simple text review system (no ratings yet)
- Team updates locations Mon/Wed/Fri manually

**Skip**:
- Real-time tracking
- User-submitted locations
- Photo uploads
- Reputation systems
- Push notifications

**Goal**: Complete info for every Penn-adjacent truck, 50 student users

**Success**: If students check app before leaving for lunch

---

#### **Standard (Week 3-4)** - Add Community Updates
**Add to MVP**:
- Star ratings (1-5)
- "Last seen" crowdsourced updates (users can report current location)
- Photo uploads for menu verification
- Simple reputation (# of accepted updates)

**Skip**:
- Sophisticated reputation algorithms
- Real-time tracking
- Truck owner accounts
- Payment integration

**Goal**: 150+ users, 100+ reviews, 50+ location updates

**Success**: If users report locations without team intervention

---

#### **Ambitious (Week 5+)** - Truck Partnerships
**Add to Standard**:
- Truck owner accounts (can post official locations)
- SMS integration (trucks text location → auto-updates map)
- Push notifications ("Hal's Halal just arrived at your location!")
- Featured truck promotions

**Goal**: 5+ truck partnerships, 300+ users, sustainable model

**Success**: If trucks request continued access post-course

---

## TripTuner - Crowdsourced Travel Itineraries

**Proposal**: `round3/jevinta.md`
**Team**: Jevin, Nikki, Julia, Arushi, Liana, Sadia
**Viability Score**: 18/30

### Summary
A platform where travelers create and vote on day-by-day itineraries for destinations, with the community collectively building the "perfect" travel plan for each city through iterative crowdsourcing.

### Dominant Themes
- ✈️ **Creates Value**: Helps travelers plan better trips
- 📊 **Creates Dataset**: Structured itinerary data
- 🤝 **Builds Community**: Travelers helping travelers

### Strengths
1. **Real Pain Point**: Trip planning is overwhelming, travelers want curated recommendations
2. **Clear Structure**: Day-by-day format makes contributions easy to understand
3. **Iterative Improvement**: Itineraries can evolve based on feedback
4. **Voting Mechanism**: Community validation of quality
5. **Sophisticated QC**: 6 mechanisms including temporal consistency, completeness scoring
6. **Large Team**: 6 people can divide work (frontend, backend, content seeding)
7. **Scalable**: Once built, can add unlimited destinations
8. **Visual Appeal**: Maps, photos, itineraries look great in demos
9. **Clear Aggregation**: Voting + completeness + upvotes formula specified
10. **Existing Demand**: Travel subreddits show people ask for itineraries constantly

### Limitations
1. **FATAL INCENTIVE MISMATCH**: 15-30 min to create itinerary, reward = badges
2. **Backwards Budget**: $75 for voting (easy 30-sec task), $0 for creation (hard 30-min task)
3. **High Friction**: Creating quality itinerary requires research, writing, structuring
4. **Cold-Start**: Why contribute to empty platform?
5. **Reddit Magic Thinking**: "Reddit communities" won't spontaneously create itineraries
6. **Competition**: TripAdvisor, Lonely Planet, travel blogs, ChatGPT all exist
7. **Quality Variance**: Itineraries need deep local knowledge, casual users can't contribute
8. **Scope Creep**: AI summarization, NLP, data visualization are premature
9. **Circular Value**: Need itineraries to attract users, need users to create itineraries
10. **100-200 Worker Target**: Unrealistic without payment

### Pathways Beyond Limitations

#### **Pathway 1: VALIDATION Platform (Not Creation)** ⭐ **HIGHEST VIABILITY**
**Target**: Validate/rank EXISTING itineraries (from blogs, Reddit, ChatGPT)
- **Pivot**: Don't ask people to CREATE (hard), ask people to VALIDATE (easy)
- **Execution**:
  - Week 1: Team scrapes 50 itineraries from travel blogs, Reddit, ChatGPT
  - Week 2: Build voting interface "Is this Paris itinerary good? Vote on each day"
  - Week 3-4: Users vote, comment, improve (5 min per itinerary)
  - Week 5: Aggregate best itineraries
- **Success Metric**: 200 users vote on 50 itineraries, clear winners emerge
- **Fixes**: Incentive (5 min voting vs 30 min creation), cold-start (team seeds), user value (immediately useful)

#### **Pathway 2: Team Creates, Crowd Refines** (HYBRID APPROACH)
**Target**: Team builds 15-20 high-quality seed itineraries
- **Execution**:
  - Week 1-2: Each team member creates 2-3 itineraries (cities they've visited)
  - Week 3: Launch with 15-20 complete itineraries
  - Week 4-5: Crowd submits corrections, alternatives, votes
- **Success Metric**: 100+ users improve team's itineraries
- **Fixes**: Cold-start (immediate value), user task (lighter - editing vs creating)

#### **Pathway 3: Paid Creation ($3-5 per Itinerary)** (BUDGET REALLOCATION)
**Target**: Pay for high-quality itinerary creation
- **Execution**:
  - Reallocate budget: $0 voting, $75 creation = 15-25 paid itineraries
  - Week 1: MTurk pilot (test quality)
  - Week 2-4: Recruit 15-25 creators via r/digitalnomad, travel bloggers
  - Week 5: Free users vote/rank the paid creations
- **Success Metric**: 20 high-quality itineraries, 100+ voters
- **Fixes**: Incentive (payment matches effort), quality (motivated creators)

#### **Pathway 4: Contest/Prize Model** (GAMIFICATION WITH VALUE)
**Target**: Monthly "Best Itinerary" contest with meaningful prize
- **Execution**:
  - Prize: $50 Amazon gift card for top upvoted itinerary per month
  - Promote in travel subreddits: "Win $50 for sharing your best trip"
  - Week 1-3: Contest runs, submissions come in
  - Week 4: Community votes, winner announced
  - Week 5: Repeat with more destinations
- **Success Metric**: 20-30 submissions for $50 prize
- **Fixes**: Incentive (meaningful reward), recruitment (contest creates urgency)

#### **Pathway 5: Penn Student Travel Focus** (CAPTIVE AUDIENCE)
**Target**: Penn students who studied abroad or traveled
- **Execution**:
  - Partner with Penn Abroad office
  - Target: Students who studied in top 10 destinations (Paris, Barcelona, Rome, etc.)
  - Value Prop: "Share your study abroad experience, help future students"
  - Execution: Email past study abroad students with request
- **Success Metric**: 30-40 study abroad students each contribute 1 itinerary
- **Fixes**: Recruitment (specific audience), incentive (help future Quakers, showcase experience)

#### **Pathway 6: Collaborative Itinerary Building** (LOWER FRICTION)
**Target**: Multiple people each add ONE day (not full itinerary)
- **Pivot**: "Add your favorite day in Paris" (2-3 min) vs "Create 7-day Paris itinerary" (30 min)
- **Execution**:
  - Week 1-2: Team creates destination skeletons (city name, basic info)
  - Week 3-4: Users add individual days (much lighter task)
  - Week 5: Aggregate best days into full itineraries
- **Success Metric**: 100+ individual days contributed
- **Fixes**: Friction (2-3 min vs 30 min), easier to start

#### **Pathway 7: Import from Existing Sources** (AGGREGATOR MODEL)
**Target**: Aggregate existing itineraries, add value through ranking/filtering
- **Execution**:
  - Week 1-2: Scrape/manually collect 100+ itineraries from blogs, YouTube (cite sources)
  - Week 3-4: Build filters (budget, pace, interests, season)
  - Week 5: Crowd ranks/votes on aggregated itineraries
- **Success Metric**: 100 itineraries with smart filtering
- **Fixes**: Cold-start (immediate value), legal (cite sources, add transformative value)

#### **Pathway 8: ChatGPT-Generated, Crowd-Validated** (AI + HUMAN)
**Target**: AI generates, humans validate/improve
- **Execution**:
  - Week 1: Generate 50 itineraries using ChatGPT (10 destinations × 5 variations)
  - Week 2-3: Build interface for humans to vote, flag errors, suggest improvements
  - Week 4-5: Humans curate best AI-generated content
- **Success Metric**: 50 AI itineraries → 10 highly-rated human-curated winners
- **Fixes**: Cold-start (instant content), human role (validation not creation)

### Fixable for Scope?
**YES IF YOU PIVOT** - Must change from creation to validation/curation model

**Critical Success Factor**: Test recruitment Week 1. Post in r/travel: "Would you spend 5 minutes voting on Paris itineraries?" If <20% respond positively, PIVOT IMMEDIATELY to team-seeded model.

### Recommended Scopes

#### **MVP (Week 1-2)** - Validation Platform
**Build**:
- Simple voting interface for itineraries
- Upvote/downvote per day, per itinerary
- Comment system for suggestions
- Team seeds 20 itineraries (scraped from blogs + ChatGPT + team's own)

**Skip**:
- User-created itineraries
- AI summarization
- NLP analysis
- Sophisticated aggregation
- User profiles/reputation

**Goal**: 50+ users vote on 20 itineraries, 100+ votes total

**Success**: If votes show clear quality distinctions (some itineraries rated much higher)

---

#### **Standard (Week 3-4)** - Add Light Editing
**Add to MVP**:
- Users can suggest edits to existing days
- "Add an alternative" for specific activities
- Simple reputation (# of accepted suggestions)
- Aggregate "community improved" versions

**Skip**:
- Full itinerary creation
- AI features
- Complex algorithms

**Goal**: 150+ users, 300+ votes, 50+ improvement suggestions

**Success**: If community suggestions demonstrably improve itineraries

---

#### **Ambitious (Week 5+)** - Hybrid Creation
**Add to Standard**:
- Users can create NEW itineraries (now that platform has users)
- Best itinerary contest ($25 prize)
- AI summarization of comments
- Export to PDF/Google Maps

**Goal**: 5-10 user-created itineraries compete with seed itineraries

**Success**: If user-created content matches or exceeds seed quality

---

## Kinnect - Social Fitness Challenges

**Proposal**: `round3/emlo.md`
**Team**: Emily, Carl, others
**Viability Score**: 18/30

### Summary
A social fitness platform where teams compete in step challenges with accountability features, leaderboards, and fitness goal tracking to motivate Penn students to stay active together.

### Dominant Themes
- 🏃 **Prosocial**: Health, fitness, community building
- 🎮 **Gamification**: Competition, leaderboards, achievements
- 🤝 **Social Accountability**: Team-based motivation

### Strengths
1. **BEST INCENTIVE DESIGN IN COHORT** (5/5): Team accountability, social pressure, competition perfectly match task
2. **Strong Intrinsic Motivation**: People actually want to be fit, just need nudge
3. **Clear User Value**: Immediate feedback, compete with friends, track progress
4. **Captive Audience**: Penn students accessible, "friends of friends" recruitment viable
5. **Data Validation**: Fitness APIs provide objective truth (can't fake steps)
6. **Engagement Loop**: Daily check-ins create habit formation
7. **Framework Application**: Sophisticated Octalysis drives (social pressure, accomplishment, scarcity)
8. **Multiple Incentive Layers**: Individual goals + team challenges + leaderboards
9. **Real Problem**: Students struggle with fitness motivation, especially in exam seasons
10. **Viral Potential**: "I need 1 more for my team, join me!" friend recruitment

### Limitations
1. **CATASTROPHIC TECH OVERREACH**: Mobile + 5 APIs + real-time + ML = Impossible in 5 weeks
2. **Mobile Development**: React Native adds 3-4 weeks to ANY timeline
3. **API Integration Complexity**: Strava, Fitbit, Apple Health, Google Fit, Garmin = 5 separate integrations
4. **Real-Time Sync**: Live leaderboards require backend complexity
5. **500+ User Target**: Network effects require scale that won't happen in 5 weeks
6. **Scope Explosion**: 10 features including ML predictions, video workouts, nutrition
7. **Payment Integration**: Stripe for challenges adds complexity
8. **Critical Mass**: Teams of 4-6 means need 40-60 users minimum for 10 teams
9. **Cross-Platform**: Android + iOS doubles development work
10. **Saturated Market**: Strava, Peloton, Nike Run Club all exist

### Pathways Beyond Limitations

#### **Pathway 1: Web-Only Manual Entry** ⭐ **HIGHEST VIABILITY**
**Target**: Eliminate mobile, eliminate APIs, focus on core social dynamics
- **Pivot**: Simple web form where users manually log steps/activities
- **Execution**:
  - Week 1-2: Build basic React app with manual entry form
  - Users log: "Today I walked 8,000 steps" (30-second entry)
  - Simple verification: Honor system + spot checks (photo of fitness app screenshot)
  - Week 3-4: Focus on team challenges, leaderboards, accountability
  - Week 5: Add basic verification (outlier detection)
- **Success Metric**: 40-50 Penn students, 10 teams competing, 70% daily check-in rate
- **Fixes**: Technical feasibility (simple CRUD), timeline (achievable), focus (social dynamics not tech)

#### **Pathway 2: Single Fitness API** (MAJOR DESCOPE)
**Target**: ONE API only (Strava - most popular among runners)
- **Execution**:
  - Week 1: Learn Strava API only
  - Week 2-3: Build web app (NOT mobile) that reads Strava data
  - Non-Strava users: Manual entry option
  - Focus on running/walking only (not 5 different activity types)
- **Success Metric**: 30 users (15 Strava, 15 manual), 5-6 teams
- **Fixes**: API complexity (1 instead of 5), platform (web only), activity type (focused)

#### **Pathway 3: Penn Gyms Challenge** (INSTITUTIONAL PARTNERSHIP)
**Target**: Partner with Pottruck, Hutchinson for official Penn fitness challenge
- **Execution**:
  - Week 1: Email Penn Fitness directors, propose "Penn Fitness Week"
  - Week 2-3: Build simple leaderboard (manual entry of gym visits)
  - Penn Fitness promotes via email, social media
  - Winner team gets free Pottruck guest passes
- **Success Metric**: Penn Fitness partnership, 100+ participants
- **Fixes**: Recruitment (official channel), legitimacy, scale

#### **Pathway 4: CIS/NETS Class Challenge** (CAPTIVE AUDIENCE)
**Target**: Single large class (CIS 1200, NETS 2120) does team fitness challenge
- **Execution**:
  - Week 1: Email professor, propose "Extra credit fitness challenge"
  - Week 2-4: Class forms teams, competes over 3 weeks
  - Extra credit: Participate 12 out of 15 days
  - Website: Simple team leaderboards, manual entry
- **Success Metric**: 80+ students participate, professor agrees
- **Fixes**: Recruitment (captive), scale (100+ users), motivation (extra credit)

#### **Pathway 5: Step Challenge ONLY** (EXTREME SIMPLIFICATION)
**Target**: Just steps (easiest to track), just teams (no individual goals), just leaderboards
- **Execution**:
  - Week 1-2: Web app where users enter daily steps (30 sec/day)
  - Form 6-8 teams of 5-6 people (friends recruit friends)
  - Week 3-4: Daily leaderboard updates (team average steps)
  - Week 5: Winning team gets $50 gift card (split among team)
- **Success Metric**: 40-50 users, 80% check-in rate, clear winner
- **Fixes**: Scope (just steps), tech (simple), incentive (prize + social)

#### **Pathway 6: Existing App Integration** (NO NEW APP)
**Target**: Use existing messaging (GroupMe/Discord) + Google Sheets
- **Execution**:
  - Week 1: Build bot that posts to GroupMe/Discord
  - Users reply with steps: "8000" → bot updates Google Sheet
  - Week 2-4: Bot posts daily leaderboard to chat
  - Zero app downloads needed, users stay in familiar environment
- **Success Metric**: 30-40 users engage via chat, no downloads needed
- **Fixes**: Friction (no app download), familiarity (existing platform)

#### **Pathway 7: Accountability Focus (Not Competition)** (DIFFERENT ANGLE)
**Target**: De-emphasize leaderboards, emphasize team support
- **Execution**:
  - Teams of 4-5 set collective goals
  - Daily team check-ins: "Did you hit your goal today?"
  - Failing = let team down (social pressure, not competitive ranking)
  - No leaderboards, just "is our team on track?"
- **Success Metric**: Higher sustained engagement (Week 1 = Week 5)
- **Fixes**: Engagement (less burnout from competition), focus (support not winning)

#### **Pathway 8: 7-Day Sprint Challenge** (TIME-BOXED)
**Target**: Just 1 week challenge, intense and focused
- **Execution**:
  - Week 1-2: Build minimal platform
  - Week 3: Recruit for Week 4 challenge
  - Week 4: 7-day challenge runs (users more willing to commit to 1 week)
  - Week 5: Repeat with different challenge theme
- **Success Metric**: 60+ users complete 7-day challenge
- **Fixes**: Commitment ask (1 week vs "ongoing"), urgency

### Fixable for Scope?
**YES WITH MANDATORY PIVOT** - Must abandon mobile and API integrations

**Critical Success Factor**: Commit to web-only manual entry by Day 1. Every day spent planning mobile is a wasted day.

### Recommended Scopes

#### **MVP (Week 1-2)** - Web Manual Entry Challenge
**Build**:
- Simple React web form: Log steps daily (text input)
- Team formation (users join teams via code)
- Basic leaderboard (team rankings)
- Admin panel to verify spot checks

**Skip**:
- Mobile app
- ALL fitness APIs
- Automatic sync
- ML predictions
- Payment system
- Video workouts
- Nutrition tracking

**Goal**: 40 users, 8 teams, 70% daily check-in rate

**Success**: If users log steps daily without team intervention

---

#### **Standard (Week 3-4)** - Add Social Features
**Add to MVP**:
- Team chat (simple comments)
- Daily streaks (gamification)
- Photo verification ("Screenshot your step count")
- Basic outlier detection (flag suspicious entries)

**Skip**:
- API integrations
- Mobile
- Complex algorithms
- Payment

**Goal**: 60 users, 12 teams, 80% check-in rate, team bonding visible

**Success**: If teams chat and encourage each other unprompted

---

#### **Ambitious (Week 5+)** - Single API Integration
**Add to Standard**:
- Strava API integration (optional for users)
- Automated outlier detection
- Weekly team reports
- Simple challenge prizes ($25 gift card)

**Goal**: 80+ users, proof that social accountability drives fitness

**Success**: If teams continue challenge after course ends (sustainability)

---

## PitchPeer - Startup Pitch Feedback Platform

**Proposal**: `round3/emkang.md`
**Team**: Emily Kang et al.
**Viability Score**: 14/30

### Summary
A peer feedback platform where entrepreneurs submit startup pitches and receive structured reviews from other founders and potential customers, democratizing access to quality pitch feedback.

### Dominant Themes
- 🚀 **Prosocial**: Helps aspiring entrepreneurs
- 🎓 **Educational**: Learn through giving and receiving feedback
- 🤝 **Community**: Entrepreneurs helping entrepreneurs

### Strengths
1. **Real Problem**: Quality pitch feedback is hard to get without YC/accelerator access
2. **Educational Value**: Reviewing others' pitches teaches pitch skills
3. **Reciprocity Incentive**: "Review 3 to get yours reviewed" could work
4. **Captive Audience**: Penn entrepreneurship ecosystem (Wharton, SEAS, Venture Labs)
5. **Low Barrier to Entry**: Anyone can review pitches (no expertise needed for some feedback)
6. **Data Value**: Could analyze common pitch weaknesses
7. **Clear Structure**: Pitch submission → peer review → ratings (simple loop)
8. **Multiple Feedback Types**: Quick votes + detailed reviews + expert ratings
9. **Potential Partnerships**: Venture Labs, Weiss Tech House, PCI could promote
10. **Long-Term Value**: Successful pitches come back to thank reviewers (feel-good factor)

### Limitations
1. **MASSIVE OVERSCOPE**: 10 features including video, AI QC, matching algorithms, analytics
2. **Video Infrastructure**: Recording, storing, streaming video = enterprise complexity
3. **Two-Sided Marketplace**: Need pitchers AND reviewers simultaneously
4. **AI Quality Assessment**: "AI evaluates feedback quality" is vaporware without implementation
5. **Cold-Start**: Why review pitches on empty platform?
6. **Expertise Gap**: Most students can't give quality startup feedback
7. **Effort Asymmetry**: Writing thoughtful pitch = 2-3 hours, reviewing = 10-20 min
8. **Generic Gamification**: Points/badges don't motivate high-effort tasks
9. **Competition**: Reddit r/startups, Indie Hackers, YC forums all provide free feedback
10. **Vague Recruitment**: "University entrepreneurship communities" = no concrete channels

### Pathways Beyond Limitations

#### **Pathway 1: Text Pitches Only, Voting Focus** ⭐ **HIGHEST VIABILITY**
**Target**: Eliminate video, AI, matching - just text pitches + simple voting
- **Pivot**: 300-word pitch text + yes/no/maybe votes + optional comments
- **Execution**:
  - Week 1-2: Build simple form (text input) + voting interface
  - Week 3: Recruit from Venture Labs, Weiss Tech House
  - Week 4-5: 20-30 pitches, 100+ voters
- **Success Metric**: Clear correlation between votes and actual pitch quality
- **Fixes**: Technical feasibility (simple CRUD), video complexity (eliminated), quick participation

#### **Pathway 2: Venture Labs Course Partnership** (CAPTIVE AUDIENCE)
**Target**: LGST 2050 (New Venture Creation) class
- **Execution**:
  - Week 1: Email Prof. Cohen/Venture Labs, propose as semester project
  - Students must submit pitches, must review 5 peers
  - Week 2-3: Build platform
  - Week 4-5: Class uses for pitch refinement before final presentations
- **Success Metric**: 40-50 students, 40-50 pitches, 200+ reviews
- **Fixes**: Cold-start (captive audience), recruitment (professor assigns), both sides (everyone pitches AND reviews)

#### **Pathway 3: Competition/Showcase Model** (EVENT-BASED)
**Target**: Pitch competition with peer voting determines finalists
- **Execution**:
  - Week 1-2: Build platform
  - Week 3: Announce competition ($100 prize for top-voted pitch)
  - Week 4: Submissions come in (15-25 pitches)
  - Week 5: Community votes, top 3 pitch live at event
- **Success Metric**: 20+ pitch submissions, 100+ voters, legitimate winner
- **Fixes**: Incentive (prize), urgency (deadline), value (showcase opportunity)

#### **Pathway 4: Expert Review Focus** (NOT PEER)
**Target**: Students submit, alumni/mentors review (not peers)
- **Pivot**: Recruit 10-15 alumni/entrepreneurs as reviewers
- **Execution**:
  - Week 1: Recruit reviewers from LinkedIn (Penn alum founders)
  - Week 2-3: Build simple queue system (experts claim pitches to review)
  - Week 4-5: Students get 1-2 expert reviews each
- **Success Metric**: 10 expert reviewers, 30 student pitches, 50+ reviews
- **Fixes**: Quality (experts not peers), incentive for reviewers (give back to Penn)

#### **Pathway 5: Async Video Reviews** (DIFFERENT VALUE)
**Target**: Loom-style video feedback (not pitch videos)
- **Pivot**: Pitches are text, reviewers GIVE feedback via short video
- **Execution**:
  - Students submit text pitches
  - Reviewers record 2-3 min Loom videos giving feedback
  - Personal, higher value than text comments
- **Success Metric**: 20 pitches, 60+ video reviews, positive feedback
- **Fixes**: Video (used for reviews not pitches), personal connection, higher value

#### **Pathway 6: Reddit-Style Upvote System** (SIMPLIFY)
**Target**: Just upvotes/downvotes + comments (no complex features)
- **Execution**:
  - Week 1-2: Build simple upvote system (like Product Hunt)
  - Week 3: Recruit 20-30 pitches from r/startups, Indie Hackers (with permission)
  - Week 4-5: Penn students vote and comment
  - Public leaderboard shows top pitches
- **Success Metric**: Clear ranking emerges, voting reflects quality
- **Fixes**: Simplicity, immediate value (see rankings), easy participation

#### **Pathway 7: Feedback Template System** (STRUCTURE QUALITY)
**Target**: Structured questions lower barrier to quality feedback
- **Execution**:
  - Not free-form "review this pitch"
  - Instead: 10 specific questions (Is problem clear? Is solution viable? Would you use this?)
  - Each question: 1-5 scale + optional comment
  - Week 2-4: Test with 30-40 Penn student pitches
- **Success Metric**: 80% of reviews are substantive (not "good idea!")
- **Fixes**: Review quality (structured), effort (guided), actionability

#### **Pathway 8: Y Combinator Application Review** (SPECIFIC USE CASE)
**Target**: Focus on YC application feedback (very specific format)
- **Execution**:
  - YC applications are 10 questions, standardized format
  - Week 1-2: Build interface for YC app reviews
  - Week 3: Recruit YC applicants (r/ycombinator, Twitter)
  - Week 4-5: Peer review of YC apps before deadline
- **Success Metric**: 15-20 YC apps reviewed, applicants report improvements
- **Fixes**: Focus (one specific format), timing (YC deadlines create urgency), value (high stakes)

### Fixable for Scope?
**YES WITH DRASTIC CUTS** - Must eliminate video, AI, matching, analytics

**Critical Success Factor**: Secure Venture Labs partnership OR plan competition with prize pool by end of Week 1.

### Recommended Scopes

#### **MVP (Week 1-2)** - Text Voting Platform
**Build**:
- Text pitch submission form (300 words max)
- Simple upvote/downvote interface
- Comment system
- Leaderboard (top pitches)

**Skip**:
- Video (anywhere)
- AI quality control
- Matching algorithms
- Expert verification
- User profiles/reputation
- Analytics dashboard

**Goal**: 15 pitches, 30 reviewers, 100+ votes

**Success**: If voting creates clear quality distinctions

---

#### **Standard (Week 3-4)** - Add Structure
**Add to MVP**:
- Structured review questions (10 specific prompts)
- "Review 3 to unlock submission" reciprocity rule
- Simple reputation (# of helpful reviews)
- Filter by category (B2B, B2C, hardware, etc.)

**Skip**:
- Video
- AI
- Complex algorithms

**Goal**: 30 pitches, 60 reviewers, 300+ structured reviews

**Success**: If reviewers report learning from process

---

#### **Ambitious (Week 5+)** - Expert Layer
**Add to Standard**:
- Expert reviewer accounts (alumni, mentors)
- Expert reviews flagged/weighted differently
- Weekly showcase (top 3 pitches featured)
- Optional: Simple pitch competition

**Goal**: 10 experts, 50 pitches, 500+ reviews, successful competition

**Success**: If students report reviews helped improve pitches

---

## Urban Explorer - Campus Event Discovery

**Proposal**: `round3/kyue.md`
**Team**: Kyle Yue et al.
**Viability Score**: 16/30

### Summary
A crowdsourced platform where Penn students discover, post, and review campus events (club meetings, talks, parties, study groups), solving the "I never know what's happening on campus" problem.

### Dominant Themes
- 🎓 **Student Life**: Improves campus experience
- 🤝 **Community**: Connect students with activities
- 📊 **Creates Dataset**: Event data, attendance patterns

### Strengths
1. **Real Problem**: Penn students genuinely struggle to find events beyond their immediate circles
2. **Clear User Value**: Immediate benefit (discover events tonight)
3. **Appropriate Tech Scope** (4/5): Next.js + Prisma + MapBox is manageable
4. **Low Barrier to Entry**: Anyone can post an event (easy contribution)
5. **Geographic Constraint**: Penn campus keeps scope manageable
6. **Visual Appeal**: Map-based discovery is intuitive
7. **Multiple Discovery Modes**: Map view, list view, category filters
8. **Social Proof**: See what's popular (upvotes, attendance counts)
9. **Time Sensitivity**: Events create urgency ("tonight at 7pm!")
10. **Network Effects**: More events → more users → more events

### Limitations
1. **Classic Cold-Start**: Empty map = useless, who posts first event?
2. **Two-Sided Marketplace**: Need event creators AND attendees
3. **Weak Incentives**: Badges/points don't motivate event posting
4. **Vague Recruitment**: "Penn students via social media" = no concrete plan
5. **Circular Value Prop**: Visibility on empty platform = worthless
6. **City-Wide Too Broad**: Philadelphia events too much for 5-week project
7. **Stale Events Risk**: Past events clutter interface if not managed
8. **Competition**: Penn Clubs website, Facebook events, GroupMe already used
9. **Notification System**: Push notifications add complexity
10. **ML Duplicate Detection**: Premature optimization, team hasn't seen if there will be duplicates

### Pathways Beyond Limitations

#### **Pathway 1: Penn Campus ONLY** ⭐ **HIGHEST VIABILITY**
**Target**: Just Penn campus events (not city-wide Philadelphia)
- **Execution**:
  - Week 1: Scrape Penn clubs website, Penn activities calendar → seed 50 events
  - Week 2: Build simple Next.js app with MapBox
  - Week 3-4: Recruit via Penn-specific channels (r/UPenn, Penn Memes, College Houses GroupMes)
  - Focus: Club meetings, talks, study groups only (no parties to avoid liability)
- **Success Metric**: 200+ Penn students, 100+ events, 70% are Penn campus-based
- **Fixes**: Scope (manageable), audience (captive), competition (clubs website is terrible UX)

#### **Pathway 2: Partner with 10 Student Orgs** (COMMITTED CONTENT)
**Target**: Get 10 clubs to commit to posting their events
- **Execution**:
  - Week 1: Email 30 club presidents, get 10 to commit
  - Clubs post weekly events (easy for them, reach new members)
  - Week 2-3: Build platform with club accounts
  - Week 4-5: Clubs promote to their members
- **Success Metric**: 10 club partnerships, 40+ events posted by clubs
- **Fixes**: Cold-start (guaranteed content), recruitment (clubs promote to members)

#### **Pathway 3: Team Seeds 100 Events First** (CONTENT-FIRST)
**Target**: Don't launch until map is full
- **Execution**:
  - Week 1-2: Team manually adds 100 Penn events from various sources
  - Each team member responsible for 15-20 events
  - Week 3: Launch with full map
  - Week 4-5: Users add NEW events and update existing
- **Success Metric**: Launch day has 100 events, users add 30+ more
- **Fixes**: Cold-start (immediate value), first impression (looks active)

#### **Pathway 4: Event Verification Rewards** (INCENTIVE REDESIGN)
**Target**: Pay users to verify events happened ("I was there")
- **Execution**:
  - Users post events (free)
  - Other users verify ("I attended this") + photo proof
  - Verified events get boosted in algorithm
  - Verifiers earn: $0.25 per verification, leaderboard recognition
  - Budget: $50 = 200 verifications
- **Success Metric**: 60% of events get verified, creates quality signal
- **Fixes**: Incentive (payment), quality (verification), engagement (attending events)

#### **Pathway 5: Calendar Integration** (LOWER FRICTION)
**Target**: Make posting events one-click from Google Calendar
- **Execution**:
  - Week 2-3: Build Google Calendar integration
  - Users connect calendar → "Share this event to UrbanExplorer?" one-click
  - Week 4-5: Clubs with shared calendars can bulk-import
- **Success Metric**: 40% of events come via calendar import
- **Fixes**: Friction (one-click vs manual form), adoption (use existing workflow)

#### **Pathway 6: Weekly Digest, Not Real-Time** (DIFFERENT PRODUCT)
**Target**: Curated weekly email, not real-time map
- **Pivot**: Not a platform, a newsletter
- **Execution**:
  - Week 1: Launch newsletter signup, team curates best 20 events weekly
  - Week 2-4: Email list grows, users submit events for inclusion
  - Week 5: Most-clicked events win spot in next week's digest
- **Success Metric**: 300+ email subscribers, 30% open rate
- **Fixes**: Cold-start (team curates), value (filtered not overwhelming), effort (weekly not daily)

#### **Pathway 7: College House Focus** (HYPER-LOCAL)
**Target**: Start with ONE college house (e.g., Rodin, Hill)
- **Execution**:
  - Week 1: Partner with one college house GA/RA
  - All house events on platform (floor meetings, study breaks, etc.)
  - Week 2-3: House residents adopt
  - Week 4-5: Expand to 2nd and 3rd houses if successful
- **Success Metric**: 80% of one house uses platform, 50+ house-specific events
- **Fixes**: Recruitment (RA promotes), critical mass (smaller denominator), value (immediately useful to house)

#### **Pathway 8: Study Group Focus ONLY** (NICHE DOWN)
**Target**: Not all events, just study groups/academic support
- **Execution**:
  - Week 1-2: Build simple study group finder
  - Categories: By class (CIS 1200, MATH 1400, etc.)
  - Week 3: Recruit in large lecture courses
  - Week 4-5: Students post study sessions for upcoming exams
- **Success Metric**: 40+ study groups posted, 150+ students join
- **Fixes**: Focus (specific need), timing (exam season urgency), value (academic improvement)

### Fixable for Scope?
**YES IF PENN-ONLY** - Must eliminate city-wide Philadelphia scope

**Critical Success Factor**: Secure 5-10 student org partnerships by end of Week 1, OR commit to team seeding 100 events Week 1-2.

### Recommended Scopes

#### **MVP (Week 1-2)** - Penn Events Directory
**Build**:
- Simple Next.js event listing (map + list views)
- Event submission form (title, time, location, description)
- Upvote system
- Team seeds 50-100 Penn events

**Skip**:
- City-wide Philly events
- User accounts (anonymous posting OK for MVP)
- Notifications
- ML duplicate detection
- Review system
- Advanced filters

**Goal**: 100 events at launch, 50+ Penn student users

**Success**: If students discover events they didn't know about

---

#### **Standard (Week 3-4)** - Add Social Features
**Add to MVP**:
- User accounts (track your events)
- "I'm going" button (RSVP)
- Simple reviews/ratings (1-5 stars)
- Event categories (academic, social, clubs, arts)

**Skip**:
- Push notifications
- ML algorithms
- Recommendations
- Social sharing

**Goal**: 150+ events, 200+ users, 50+ RSVPs, 30+ reviews

**Success**: If users check platform 2-3 times per week

---

#### **Ambitious (Week 5+)** - Club Partnerships
**Add to Standard**:
- Club accounts (verified badge)
- Bulk event import (Google Calendar)
- Email digest (weekly top events)
- Simple recommendations ("Based on events you attended...")

**Goal**: 10+ club partnerships, 250+ events, 400+ users, sustainable model

**Success**: If clubs request continued access post-course

---

## AgriAid - Crowdsourced Agricultural Disaster Assessment

**Proposal**: `round3/nikkiliu.md`
**Team**: Nikki Liu et al.
**Viability Score**: 15/30

### Summary
Crowdsourced satellite imagery labeling to identify agricultural damage from natural disasters, enabling faster humanitarian aid deployment to affected farming communities in developing countries.

### Dominant Themes
- 🌍 **Prosocial**: Humanitarian aid, disaster relief
- 📊 **Creates Dataset**: Labeled satellite imagery for ML training
- 🔬 **Research Value**: Could contribute to disaster response research

### Strengths
1. **Compelling Mission**: Helping disaster victims is emotionally motivating
2. **Real Impact Potential**: Faster damage assessment = faster aid deployment
3. **Clear Task**: Binary classification (damaged/not damaged) or severity scale (low/medium/high)
4. **Sophisticated QC** (4/5): Cohen's kappa, NDVI validation, consensus voting, expert review
5. **Quantitative Analysis**: Strong metrics (precision, recall, inter-rater reliability)
6. **Novel Approach**: Crowdsourced disaster assessment less common than other applications
7. **Data Availability**: Satellite imagery is publicly accessible (Sentinel-2, Landsat)
8. **Low Skill Barrier**: After brief training, anyone can label damage
9. **Scalable**: Once system works, can apply to any disaster globally
10. **Long-Term Value**: Dataset could train ML models for future disasters

### Limitations
1. **MASSIVE TECHNICAL COMPLEXITY**: Google Earth Engine pipeline = 2-3 weeks alone
2. **4,167 VOLUNTEER HOURS NEEDED**: 50,000 annotations ÷ 12 per hour = 4,167 hours
3. **Unrealistic Recruitment**: "Environmental groups" won't spontaneously label 50,000 images
4. **Expertise Contradiction**: Claims "no expertise needed" but also discusses NDVI, spectral analysis
5. **Partnership Dependency**: Relies on NGO partnerships that take 6+ months to establish
6. **Timeline Mismatch**: "Week 1-8" for 5-week project
7. **Scope Explosion**: 8 features + satellite pipeline + ML validation + forum
8. **Weak Incentive**: Altruism rarely sustains high-volume tedious work
9. **No Budget**: $0 allocated for labeling compensation
10. **Stale Data**: Historical disasters (2017-2023) less emotionally urgent

### Pathways Beyond Limitations

#### **Pathway 1: Use Existing Dataset** ⭐ **HIGHEST VIABILITY**
**Target**: Don't build satellite pipeline, use pre-processed disaster dataset
- **Pivot**: Use xBD dataset (satellite disaster images, already processed)
- **Execution**:
  - Week 1: Download xBD dataset (building damage from disasters)
  - Week 2: Build simple labeling interface (image → damaged yes/no)
  - Week 3-4: Recruit Penn students to label (easier than volunteers)
  - Week 5: Analyze aggregation quality vs. ground truth
- **Success Metric**: 1,000 images labeled with 3-5 annotations each
- **Fixes**: Technical complexity (eliminated), timeline (feasible), focus (labeling not infrastructure)

#### **Pathway 2: 90% Scope Cut** (REALISTIC VOLUME)
**Target**: 10,000 tiles → 1,000 tiles (10% of original plan)
- **Execution**:
  - 1,000 tiles × 3 annotations each = 3,000 labels
  - 3,000 labels ÷ 12 per hour = 250 volunteer hours
  - 250 hours ÷ 5 weeks = 50 hours/week = 10 volunteers doing 1 hour/day
  - Week 1-2: Recruit 10-15 committed volunteers
  - Week 3-5: Volunteers label systematically
- **Success Metric**: 1,000 tiles fully labeled, QC metrics show reliability
- **Fixes**: Volunteer hours (250 vs 4,167), recruitment (10 committed > 100 casual)

#### **Pathway 3: Penn Environmental Courses Partnership** (CAPTIVE AUDIENCE)
**Target**: ENVS/GEOL classes use as educational exercise
- **Execution**:
  - Week 1: Email ENVS profs, propose as class activity
  - Week 2-3: Build interface
  - Week 4-5: Class labels images (extra credit or required)
  - Students learn about disaster assessment + remote sensing
- **Success Metric**: 30-40 students, 1,500 labels, publishable analysis
- **Fixes**: Recruitment (captive), motivation (grades), scale (achievable)

#### **Pathway 4: Paid Labeling (MTurk)** (BUDGET REALLOCATION)
**Target**: Pay for quality labels instead of hoping for volunteers
- **Execution**:
  - Budget: $200 for labeling
  - Pay: $0.10 per image (3-5 labels per image)
  - 1,000 images × 3 labels × $0.10 = $300 (request budget increase)
  - Week 1-2: Build MTurk HIT
  - Week 3-4: Collect labels
  - Week 5: Analyze quality
- **Success Metric**: 1,000 images with 3+ high-quality labels each
- **Fixes**: Incentive (payment), reliability (MTurk workers), timeline (fast)

#### **Pathway 5: Recent Disaster Focus** (URGENCY)
**Target**: Current disaster (2024-2025) creates emotional urgency
- **Execution**:
  - Monitor news for recent agricultural disasters
  - Week 1: Identify recent disaster, acquire satellite imagery
  - Week 2-4: Recruit volunteers with "Help [Country] farmers NOW"
  - Partner with relevant diaspora communities (e.g., Pakistani Students Association if Pakistan flooding)
- **Success Metric**: 500 images labeled for current disaster, urgency drives participation
- **Fixes**: Motivation (urgency), recruitment (community connection), impact (real-time aid)

#### **Pathway 6: AI-Assisted Labeling** (HYBRID APPROACH)
**Target**: AI pre-labels, humans verify/correct
- **Execution**:
  - Week 1-2: Use existing ML model (from xBD paper) to pre-label
  - Week 3-4: Humans verify: "AI thinks this is damaged. Agree? Yes/No/Unsure"
  - Much faster (2-3 seconds per image vs. 5-6 minutes)
  - Week 5: Analyze when humans agree/disagree with AI
- **Success Metric**: 5,000 images verified (10x more volume)
- **Fixes**: Task time (3 sec vs 5 min), volume (achievable), research value (human-AI agreement)

#### **Pathway 7: Binary Classification Only** (SIMPLIFY TASK)
**Target**: Just "damaged" or "not damaged" (not severity levels)
- **Execution**:
  - Eliminate 3-level severity classification
  - Just yes/no: "Is this field damaged?"
  - Faster (2 min per image vs. 5 min)
  - Week 2-4: Volunteers label 2,000+ images
- **Success Metric**: 2,000 images with binary labels, high inter-rater reliability
- **Fixes**: Task complexity (simpler), time (faster), volume (more achievable)

#### **Pathway 8: Gamification with Impact Visualization** (BETTER INCENTIVE)
**Target**: Show real-time impact of labeling work
- **Execution**:
  - Map showing "areas assessed thanks to your work"
  - Counter: "Your labels helped identify aid needs for X farms"
  - Leaderboard: Top labelers this week
  - Weekly update: "This week's labels led to [specific aid deployment]" (if partnered with NGO)
- **Success Metric**: 20+ volunteers continue past Week 2
- **Fixes**: Engagement (visualized impact), motivation (see results), retention

### Fixable for Scope?
**YES WITH 90% SCOPE CUT** - Must use existing dataset and reduce volume 10x

**Critical Success Factor**: Download xBD dataset Week 1, build simple interface Week 2, recruit 10-15 COMMITTED volunteers (not "environmental groups"). Alternative: Secure Penn ENVS course partnership or MTurk budget.

### Recommended Scopes

#### **MVP (Week 1-2)** - Labeling Interface
**Build**:
- Download xBD dataset (building damage)
- Simple React interface: Show image → "Damaged?" → Yes/No buttons
- Store labels in database
- Admin view: Track labeling progress

**Skip**:
- Google Earth Engine pipeline
- Live satellite imagery
- Severity classification (just binary)
- NDVI analysis
- Forum/communication features
- ML validation

**Goal**: 500 images labeled by 10 committed volunteers

**Success**: If volunteers complete 50+ images each

---

#### **Standard (Week 3-4)** - Add Quality Control
**Add to MVP**:
- Gold standard questions (10% of images with known answers)
- Consensus requirement (3 labels per image)
- Simple reputation (accuracy on gold standard)
- Inter-rater reliability calculation (Cohen's kappa)

**Skip**:
- Complex aggregation algorithms
- ML model comparison
- Real-time disaster data

**Goal**: 1,000 images with 3+ labels each, kappa > 0.6

**Success**: If consensus labels match expert labels (on sample)

---

#### **Ambitious (Week 5+)** - Research Publication
**Add to Standard**:
- Compare human labels to ML model predictions
- Analyze when humans outperform AI
- Partnership with disaster response research group
- Publish findings as research paper contribution

**Goal**: Publishable insights on crowdsourced disaster assessment

**Success**: If research demonstrates crowdsourcing viability for this task

---

## TerraTruth - Crowdsourced Environmental Monitoring

**Proposal**: `round3/jlee0902.md`
**Team**: Jenny Lee et al.
**Viability Score**: 15/30

### Summary
A platform where volunteers label satellite imagery to track environmental changes (deforestation, urban sprawl, water pollution) over time, creating transparency for environmental advocacy and corporate accountability.

### Dominant Themes
- 🌍 **Prosocial**: Environmental protection, corporate accountability
- 📊 **Creates Dataset**: Time-series environmental change data
- 🔬 **Research Value**: Could support environmental research/litigation

### Strengths
1. **EXCEPTIONAL QC DESIGN** (5/5): Gold standard, outlier detection, expert review, weighted trust scores, cross-validation
2. **Sophisticated Aggregation**: Weighted consensus formula with confidence intervals
3. **Compelling Mission**: Environmental transparency resonates with many people
4. **Clear Adversary**: Corporate greenwashing creates emotional motivation
5. **Time-Series Value**: Tracking changes over time (not one-time labels)
6. **Multiple Use Cases**: Deforestation, pollution, urban sprawl (versatile)
7. **Framework Application**: Strong Quinn & Benderson decomposition
8. **Data Persistence**: Once labeled, historical imagery stays valuable
9. **Scalable**: Can monitor any region globally
10. **Impact Potential**: Data could support environmental litigation, policy

### Limitations
1. **CATASTROPHIC SCOPE**: 10 features + PostGIS + AI detection + forum = 12+ weeks minimum
2. **NGO Partnership Impossibility**: Partnerships take 6+ months, not 5 weeks
3. **No Captive Audience**: Where will 50-500 volunteers come from?
4. **Expertise Contradiction**: "Satellite imagery interpretation" requires training
5. **Satellite Pipeline Complexity**: PostGIS + geospatial queries = advanced GIS skills
6. **Premature Optimization**: AI anomaly detection before having users
7. **Vague Recruitment**: No specific channels, no test outreach
8. **$0 Budget**: Altruism for tedious work (labeling 1000s of images)
9. **Cold-Start**: Why join platform with no imagery, no community, no impact yet?
10. **Competition**: Zooniverse, Global Forest Watch, satellite.org already exist

### Pathways Beyond Limitations

#### **Pathway 1: Public Satellite Data + Simple Labeling** ⭐ **HIGHEST VIABILITY**
**Target**: Eliminate PostGIS, use simple image comparison
- **Pivot**: Show two satellite images of same location (2015 vs 2024) → "Has forest decreased? Yes/No"
- **Execution**:
  - Week 1: Use Global Forest Watch API for pre-processed imagery
  - Week 2: Build simple image comparison interface
  - Week 3-4: Recruit Penn environmental students to label 500 locations
  - Week 5: Analyze aggregated labels, visualize findings
- **Success Metric**: 500 locations labeled with consensus, clear deforestation trends identified
- **Fixes**: GIS complexity (eliminated), pipeline (use existing APIs), focus (labeling not infrastructure)

#### **Pathway 2: 90% Scope Cut** (REALISTIC TECHNICAL TARGET)
**Target**: Just comparison labeling + consensus voting (skip 7 of 10 features)
- **Features to BUILD**:
  - Image display (before/after)
  - Label submission (changed/not changed)
  - Consensus calculation (majority vote)
- **Features to SKIP**:
  - PostGIS geospatial database
  - AI anomaly detection
  - Time-decay reputation
  - Discussion forum
  - User authentication (anonymous OK)
  - Advanced analytics dashboard
  - Real-time monitoring
- **Success Metric**: 3 features implemented perfectly vs. 10 features half-done
- **Fixes**: Technical feasibility, timeline, focus

#### **Pathway 3: Penn ENVS Course Partnership** (CAPTIVE AUDIENCE)
**Target**: ENVS 1000 (Intro to Environmental Science) class project
- **Execution**:
  - Week 1: Email ENVS profs, propose as semester project
  - Students learn environmental monitoring + satellite imagery interpretation
  - Extra credit or required: Each student labels 50 locations
  - Week 2-3: Build simple interface
  - Week 4-5: Class uses platform, analyze results together
- **Success Metric**: 50 students × 50 labels = 2,500 labels
- **Fixes**: Recruitment (captive), education (part of learning), scale (achievable)

#### **Pathway 4: Focus on ONE Environmental Issue** (NICHE DOWN)
**Target**: Just deforestation in Amazon (not pollution + sprawl + everything)
- **Execution**:
  - Partner with existing Amazon conservation groups
  - Week 1-2: Identify 200 high-risk Amazon locations
  - Week 3-4: Recruit via r/environment, environmental Discord servers
  - Week 5: Publish findings, share with conservation groups
- **Success Metric**: 200 Amazon locations tracked, findings shared with activists
- **Fixes**: Focus (specific, emotionally resonant), recruitment (targeted communities), impact (concrete)

#### **Pathway 5: Use Zooniverse Platform** (INFRASTRUCTURE SHORTCUT)
**Target**: Build on existing Zooniverse platform (not from scratch)
- **Execution**:
  - Week 1: Register project on Zooniverse.org
  - Zooniverse provides: User management, labeling interface, consensus algorithms, volunteer community
  - Week 2-3: Upload imagery, design classification workflow
  - Week 4-5: Zooniverse community labels images
- **Success Metric**: 10,000+ classifications from Zooniverse volunteers
- **Fixes**: Technical complexity (eliminated), recruitment (existing volunteer base), QC (built-in)

#### **Pathway 6: Penn-Only Local Monitoring** (HYPER-LOCAL)
**Target**: Track environmental changes around Philadelphia, not globally
- **Execution**:
  - Week 1-2: Identify 50 Philly-area sites (parks, waterways, construction)
  - Team visits sites monthly, takes photos + drone footage
  - Week 3-4: Build timeline interface showing changes
  - Week 5: Partner with Philly environmental groups
- **Success Metric**: 50 local sites tracked, partnership with Schuylkill River rangers or similar
- **Fixes**: Recruitment (local connection), scope (manageable), verification (can visit sites)

#### **Pathway 7: Corporate Accountability Focus** (SPECIFIC TARGET)
**Target**: Track specific company's environmental claims
- **Execution**:
  - Week 1: Choose 1 company with environmental commitments (e.g., "will reforest X acres")
  - Week 2-3: Get satellite imagery of claimed reforestation sites
  - Week 4-5: Crowd verify: "Is there actually new forest here?"
  - Publish findings as case study
- **Success Metric**: Verifiable findings on 1 company, media attention
- **Fixes**: Focus (concrete), urgency (accountability), impact (specific result)

#### **Pathway 8: AI Pre-Label, Human Verify** (HYBRID)
**Target**: Use existing ML models for initial detection, humans verify
- **Execution**:
  - Week 1-2: Use Global Forest Watch API (has built-in change detection)
  - Week 3-4: Humans verify: "AI detected forest loss here. Correct? Yes/No/Unsure"
  - Much faster than manual labeling
  - Week 5: Analyze when humans catch AI errors
- **Success Metric**: 2,000+ AI detections verified, improving AI accuracy
- **Fixes**: Task speed (verification faster than labeling), volume (more achievable), research value

### Fixable for Scope?
**YES WITH MASSIVE PIVOT** - Must eliminate PostGIS, partnerships, AI detection, and 7 of 10 features

**Critical Success Factor**: Choose ONE pathway (ideally #5 Zooniverse or #3 Penn course) by Day 1. Do not attempt to build full platform from scratch.

### Recommended Scopes

#### **MVP (Week 1-2)** - Simple Comparison Labeling
**Build**:
- Image comparison interface (before/after satellite images)
- Simple form: "Has forest decreased? Yes/No/Unsure"
- Store labels in simple database
- Use Global Forest Watch API for imagery (don't build pipeline)

**Skip**:
- PostGIS
- User authentication
- Geospatial queries
- AI detection
- Forum
- Time-decay reputation
- Real-time monitoring
- Advanced analytics

**Goal**: 500 location comparisons labeled by 10-15 volunteers

**Success**: If consensus labels show clear patterns

---

#### **Standard (Week 3-4)** - Add Basic QC
**Add to MVP**:
- Gold standard questions (pre-labeled examples)
- Consensus requirement (3 labels per location)
- Simple accuracy tracking (% correct on gold standard)
- Majority voting aggregation

**Skip**:
- Complex weighted trust scores
- Advanced statistical validation
- AI integration
- Expert review queue

**Goal**: 1,000 locations with 3+ labels, demonstrated quality

**Success**: If gold standard accuracy > 75%

---

#### **Ambitious (Week 5+)** - Partnership & Impact
**Add to Standard**:
- Partner with 1 environmental organization
- Create public dashboard of findings
- Press release / blog post with results
- Open-source dataset for researchers

**Goal**: Real impact (findings used by environmental advocates)

**Success**: If organization uses your data for campaign/research

---

## SoundScape - Crowdsourced Audio Environment Map

**Proposal**: `round3/vavali.md`
**Team**: Vavali et al.
**Viability Score**: 12/30 (LOWEST IN COHORT)

### Summary
A crowdsourced platform where users record and upload ambient sounds from locations around campus/city, creating an audio map that captures the acoustic character of different places for urban planning, accessibility, and artistic purposes.

### Dominant Themes
- 🎨 **Creative/Artistic**: Audio as art, urban soundscapes
- ♿ **Accessibility**: Helps blind/low-vision users preview locations
- 📊 **Creates Dataset**: Geotagged audio library
- 🏙️ **Urban Planning**: Noise pollution data

### Strengths
1. **Novel Concept**: Audio maps are less common than photo/review maps
2. **Multiple Value Props**: Accessibility, urban planning, art, nostalgia
3. **Emotional Resonance**: Sounds evoke memories, create sense of place
4. **Accessibility Mission**: Helping blind/low-vision users is compelling
5. **Clear Geographic Constraint**: Campus or city-specific keeps scope somewhat bounded
6. **User-Generated Content**: Once contributed, audio stays valuable
7. **Low Barrier to Recording**: Everyone has a smartphone microphone
8. **QC Thinking**: SNR analysis, perceptual hashing show technical sophistication
9. **Multiple Discovery Modes**: Map view, category browse, trending sounds
10. **Long-Term Value**: Historical archive of campus sounds (time capsule aspect)

### Limitations
1. **CATASTROPHIC OVERSCOPE**: 13+ separate week-long projects combined into one
2. **Audio ML Pipeline**: MFCC extraction, clustering, similarity = advanced signal processing
3. **Mobile Development**: iOS + Android adds 3-4 weeks minimum
4. **Storage Costs**: Audio files are large, hosting costs spiral quickly
5. **Sophisticated QC**: SNR, perceptual hashing, ML clustering all complex
6. **Worker Queues**: Background audio processing requires DevOps skills
7. **Zero Validation**: No evidence anyone wants this, no pilot test
8. **Weak Incentives**: Recording sounds for badges/leaderboards unlikely to work
9. **Quality Variance**: Wind noise, handling noise, poor recordings common
10. **Vague Recruitment**: "Social media campaigns" won't yield 300-1000 users
11. **Moderation**: Offensive audio, copyright music, privacy violations
12. **Battery Drain**: Recording audio drains phones, users may resist

### Pathways Beyond Limitations

#### **Pathway 1: Web-Only, Manual Upload** ⭐ **HIGHEST VIABILITY**
**Target**: Eliminate mobile app and ML, focus on simple web upload
- **Pivot**: Users record on their phone, upload via web browser
- **Execution**:
  - Week 1-2: Simple React web form (upload audio file + location + tags)
  - Week 3-4: Build map view with playback (MapBox + HTML5 audio player)
  - No ML clustering, just categories (nature, urban, music, etc.)
  - Week 5: Penn students contribute 50-100 campus sounds
- **Success Metric**: 100 audio clips from 30 users, map demonstrates concept
- **Fixes**: Mobile complexity (eliminated), ML complexity (eliminated), focus (core value prop)

#### **Pathway 2: Penn Campus ONLY** (SCOPE REDUCTION)
**Target**: Just Penn campus, not city-wide
- **Execution**:
  - Week 1: Team records 30 iconic Penn sounds (Locust Walk, Huntsman bell, Pottruck gym, etc.)
  - Week 2-3: Build simple web interface
  - Week 4-5: Recruit Penn students via r/UPenn to add more sounds
  - Focus: Capture Penn's audio character
- **Success Metric**: 100+ Penn campus sounds, coverage of major locations
- **Fixes**: Geographic scope (manageable), audience (captive), value (nostalgic for Penn students)

#### **Pathway 3: Annotation Not Recording** (LOWER FRICTION)
**Target**: Users describe existing sounds, not record new ones
- **Pivot**: Team records 100 sounds, users annotate/tag/describe
- **Execution**:
  - Week 1-2: Team creates audio library
  - Week 3-4: Users listen and add tags, descriptions, emotions
  - Much faster (30 sec to tag vs 5 min to record/upload)
  - Week 5: Build search by mood ("calm sounds," "energetic sounds")
- **Success Metric**: 100 sounds with 5+ annotations each
- **Fixes**: Friction (annotation faster than recording), quality (team controls recording quality)

#### **Pathway 4: Accessibility Focus ONLY** (NICHE DOWN)
**Target**: Just for blind/low-vision users (drop urban planning, art, etc.)
- **Execution**:
  - Partner with Penn Disability Services
  - Week 1-2: Record 50 key campus locations blind students need to navigate
  - Week 3-4: Build accessible interface (screen reader compatible)
  - Week 5: Test with blind students, gather feedback
- **Success Metric**: 5-10 blind Penn students report it's useful
- **Fixes**: Focus (specific user group), value (concrete utility), validation (direct feedback)

#### **Pathway 5: Contest/Art Project** (EVENT-BASED)
**Target**: "Capture Penn's Soundscape" contest with prizes
- **Execution**:
  - Week 1-2: Build simple upload interface
  - Week 3: Launch contest, prizes ($100 total: $50/$30/$20)
  - Categories: Most unique sound, best quality, most iconic Penn sound
  - Week 4: Community votes
  - Week 5: Winners announced at small event
- **Success Metric**: 50+ submissions, clear community engagement
- **Fixes**: Incentive (prizes), urgency (deadline), value (showcase opportunity)

#### **Pathway 6: Collaboration with Music/Audio Students** (PARTNERSHIP)
**Target**: Penn music, audio engineering, DMD students contribute
- **Execution**:
  - Week 1: Email music/DMD professors, propose as extra credit project
  - Students learn field recording techniques
  - Week 2-4: Students contribute high-quality recordings (better than general public)
  - Week 5: Showcase student work
- **Success Metric**: 20-30 audio students contribute, higher quality recordings
- **Fixes**: Recruitment (specific audience), quality (trained recordists), motivation (portfolio building)

#### **Pathway 7: YouTube Audio Compilation** (NO APP NEEDED)
**Target**: Just collect YouTube links to ambient sound videos
- **Execution**:
  - Week 1-2: Build simple interface to submit YouTube links
  - Users find existing ambient sound videos ("10 Hours of Penn Campus Sounds")
  - Week 3-4: Curate map of locations with YouTube links
  - Week 5: Create original compilation video (team edits)
- **Success Metric**: 50 locations with linked ambient videos
- **Fixes**: Effort (finding links easier than recording), legal (linking not hosting), storage (zero)

#### **Pathway 8: Pre-Recorded Sound Library** (DIFFERENT PRODUCT)
**Target**: Not crowdsourced, curated by team
- **Pivot**: Team becomes audio archivists, not platform builders
- **Execution**:
  - Week 1-3: Team records 100 high-quality campus sounds (rent good microphones)
  - Week 4: Build beautiful website showcasing sounds
  - Week 5: Launch as "Penn Soundscape Archive" art project
- **Success Metric**: 100 high-quality sounds, featured on Penn arts blog
- **Fixes**: Quality (professional), scope (team creates), value (artistic merit)

### Fixable for Scope?
**BARELY - Requires 70-80% Scope Cut** - Must eliminate mobile AND ML OR pivot to annotation/curation

**Critical Success Factor**: Decide by Day 1: Are you building technology platform (risky) or creating curated audio archive (safer)? Do not attempt mobile + ML in 5 weeks.

### Recommended Scopes

#### **MVP (Week 1-2)** - Web Upload Only
**Build**:
- Simple React web form (upload audio file + location pin + tags)
- Basic map view (MapBox) with playback (HTML5 audio player)
- Team seeds 30 Penn campus sounds

**Skip**:
- Mobile app
- All ML/audio processing
- SNR analysis
- Perceptual hashing
- Sophisticated QC
- User accounts (anonymous uploads OK)
- Categories/filtering

**Goal**: 50 audio clips from 15 users, demonstrates concept

**Success**: If users say "this is cool, I'd use this"

---

#### **Standard (Week 3-4)** - Add Basic Features
**Add to MVP**:
- User accounts (optional, to track your contributions)
- Simple categories (nature, urban, music, voices, mechanical)
- Tag system (users add descriptive tags)
- Basic moderation (flag for removal button)

**Skip**:
- Mobile app
- ML anything
- Advanced audio processing
- Worker queues

**Goal**: 100 audio clips, 30 users, coverage of major Penn locations

**Success**: If users discover new sounds and locations

---

#### **Ambitious (Week 5+)** - Curation & Art
**Add to Standard**:
- Curated playlists ("Sounds of Locust Walk," "Peaceful Penn Spots")
- Search by mood/emotion tags
- Featured sound of the week
- Partnership with Penn arts/music department

**Goal**: Recognized as legitimate audio art project, sustainable contributions

**Success**: If featured on Penn arts blog or in campus exhibition

---

# Summary: Decision Framework for Students

## Quick Decision Tree

### Step 1: Calculate Your Viability Score
Use the rubric (reports/RUBRIC-PROJECT-VIABILITY.md) to score your project /30.

### Step 2: Check Your Critical Dimensions
- **Technical Feasibility <3/5?** → You must descope or pivot platform
- **Recruitment <3/5?** → You must secure concrete commitments Week 1
- **Incentive Design <3/5?** → You must add payment or reduce task friction

### Step 3: Choose a Pathway
- Review pathways for your project above
- Pick ONE that matches your constraints (time, skills, network, budget)
- Commit to it fully (don't try to combine multiple pathways)

### Step 4: Select Appropriate Scope
- **If you're confident** → Standard Scope
- **If you're unsure** → MVP Scope (you can always add features later)
- **If you're ambitious AND have Week 1 validation** → Ambitious Scope

### Step 5: Execute Week 1 Validation
- **Day 1-3**: Build/prepare what you need to test recruitment
- **Day 4-5**: Actually test (post somewhere, email someone, get responses)
- **Day 6-7**: Decide based on results (continue or pivot)

## Universal Success Principles

### Regardless of which project you choose:

1. **Validate Before Building**: Test recruitment Week 1, not Week 4
2. **Seed Content First**: Don't launch with empty platforms
3. **Focus on Core Loop**: One feature done well > ten features half-done
4. **Budget Correctly**: Pay for hard tasks, gamify easy ones
5. **Be Specific**: "Social media" → "r/UPenn, Locust Walk GroupMe, CIS 1200 Slack"
6. **Have Backup Plan**: What if Reddit doesn't respond? (Answer: MTurk or team seeds)
7. **Cut 50% of Features**: If it hurts, cut 50% more
8. **Make It Penn-Specific**: Captive audiences are your friend

## Final Thoughts

Every project in Round 3 has merit. The question isn't whether your idea is good—it's whether you can execute it in 5 weeks with limited resources.

The teams that will succeed are those who:
- Pick ONE pathway and commit fully
- Validate assumptions Week 1 (not Week 4)
- Make hard cuts early (not when it's too late)
- Focus on core loop (not feature bloat)
- Secure concrete commitments (not vague plans)

**Remember**: A simple, working system with real users beats a complex, elegant platform with fake data every time.

**Your goal**: Prove the crowdsourcing concept works, not build a startup.

---

**Good luck! You've got great ideas. Now execute strategically.**
