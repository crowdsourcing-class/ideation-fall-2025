# Crowdsourcing Project Idea: Soundscape
## Authors

**Original Author:** Mingni Dong mdong126

**Contributor:** Anika Basu basua
## Problem Statement
Online maps and city guides tell you where to go, but not what it feels like. There’s no good way to explore the soundscapes of citiee, from quiet parks to bustling cafés which could help people choose better workspaces, travel destinations, or relaxation spots.

## Target Audience

Target Users: Remote workers, travelers, urban planners, and people who love discovering new environments (musicians, game designers, etc.). To a more niche crowd, those with sensitivity to sounds.
## Description
SoundScape is a crowdsourced platform that builds an interactive global map of sounds. Users record short ambient audio clips from their surroundings like a park, café, or subwayand upload them with location and mood tags. Other users also listen, rate, and verify these clips to classify areas by their sound environment (ex calm, lively, chaotic). Over time, the system aggregates these contributions into a living, community-driven map that helps people explore cities and spaces through their acoustic atmosphere.

## Project Type

_Select the category that best fits your project:_

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [x ] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 5-8 key features or capabilities of your system. Expand from Round 1:_

1. Geo-tagged Audio Uploads: Users can easily record and upload 10–30 second ambient sound clips with automatic location tagging.
2. Mood & Environment Tagging: Contributors label each sound by mood (e.g., calm, energetic) and environment type (e.g., café, park, street).
3. Interactive Sound Map: A dynamic map visualizes sounds worldwide, color-coded by vibe and noise level for easy exploration.
4. Crowd Verification & Rating: Other users rate or flag clips to ensure quality and consistency, creating consensus-driven classifications.
5. Daily Sound Challenges: Themed prompts (“Record the most peaceful place you find today”) drive engagement and repeat participation.
6. Gamified Reputation System: Contributors earn badges, ranks, and profile stats for accurate or popular uploads, building long-term motivation.
7. Sound Similarity Discovery: Automatic clustering surfaces “related” sounds (e.g., find clips with a similar acoustic profile).
8. Open Data & API Access: Aggregated, anonymized sound data is accessible for researchers, developers, and urban planners.

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
volunteers, people in the Philly area

**What will they provide?**
upload sound clips, labels for the sound clips, ratings of the clips 
**What skills do they need?**
ability to understand english, at least average ability to hear 
**Do skills vary widely? How?**
Some users will have a better ear for distinguishing sound qualities (e.g., background chatter vs. music), making them more accurate taggers and verifiers. Others might be better at recording clear, representative clips due to higher-quality microphones or quieter environments. Additionally, experienced users will develop stronger intuition for consistent labeling and mood classification, while casual participants may focus more on creative or exploratory recordings. Over time, reputation scores and feedback loops will help surface and reward these more skilled contributors.

**How will you incentivize participation?**
SoundScape uses a gamified intrinsic motivation model to encourage sustained participation. Contributors earn points and badges for verified uploads, ratings, and challenge completions. A leaderboard highlights top Sound Explorers by city or category, fostering friendly competition. Each contribution immediately appears on the global sound map creating visible impact and emotional reward for users who enjoy sharing pieces of their environment. Occasional themed challenges (ex Quietest Spot on Campus Week) offer small digital rewards or feature highlights to keep engagement high without monetary payments.

**How much will it cost?**
Because SoundScape relies on voluntary, gamified participation, no direct payments to contributors are required. The main expenses are technical infrastructure and hosting:
Storage & Hosting: $200 (Firebase + Mapbox free tiers with occasional overages)
Web & Mobile App Deployment: $100 (domain, minimal backend hosting)
Marketing & Incentives: $150 (digital rewards, small prizes for top contributors)
Miscellaneous (API usage, analytics tools): ~$50
Total Estimated Budget: ≈ $500 for the pilot phase (covering 300–1,000 contributors).
Cost per worker: $0.50 assuming max 1,000 participants.
Cost per task: Essentially $0, since all participation is volunteer-based and driven by intrinsic and gamified motivation.

**Where will your data come from?**
All data will be user-generated through crowd contributions. Participants record and upload short ambient audio clips via the SoundScape web or mobile app, which automatically tags each submission with time, location, and basic acoustic metadata. Additional contextual data (ex mood labels, environment type) comes from crowd tagging and verification tasks. For baseline geographic information and map visualization, the system will use open-source APIs such as OpenStreetMap or Mapbox. No scraping or proprietary datasets will be required.

**How many crowd workers do you need?**
the more the better but at least 300 and max 1000

## Technical Approach

**What are the main steps/components in your system?**

1. User records and uploads a 10–30 second ambient audio clip through the SoundScape app, which automatically tags the location and timestamp.
2. System extracts metadata (e.g., volume level, frequency spectrum) and stores the clip in the database with basic acoustic features.
3. Crowd tags and rates the clip by mood (e.g., calm, lively), environment (e.g., park, café), and clarity.
4. System aggregates tags using weighted majority voting, factoring in each contributor’s reliability score.
5. Map visualization updates in real time to display the new, verified sound on the global “sound map.”
6. Gamification and feedback loop: users earn points, badges, and visibility on leaderboards, motivating continued participation.
   
**What parts are done by the crowd vs. automated?**
Crowd (Human) Tasks:
Recording & Uploading: Contributors capture short ambient audio clips from their surroundings.
Tagging & Labeling: Users describe each clip by mood (e.g., calm, energetic), environment type (e.g., street, café, park), and perceived noise level.
Verification & Rating: Crowd members listen to others’ clips, confirm or dispute tags, and rate audio quality.
Creative Participation: Users engage in themed challenges and explore the sound map, driving ongoing contributions.
Automated (Computational) Tasks:
Metadata Extraction: System analyzes volume, duration, and frequency spectrum for each clip.
Geo-Tagging & Mapping: Automatically assigns GPS coordinates and visualizes clips on an interactive map.
Aggregation & Quality Control: Weighted majority voting integrates multiple crowd labels while prioritizing high-reputation contributors.
Audio Similarity & Clustering: Algorithms group related sounds and detect duplicates or corrupted submissions.


**What technologies/tools will you use?**
Frontend: React (Next.js) for web, React Native (Expo) for mobile; Tailwind CSS; Web Audio API for in-browser recording & playback.
Maps/Geo: Mapbox GL JS (or Leaflet) + OpenStreetMap tiles; Turf.js for geospatial ops.
Backend & APIs: Python (FastAPI) or Node (Express) for REST endpoints; Firebase Auth for auth; Firebase Cloud Functions for lightweight serverless tasks.
Storage & DB: Firebase Firestore (metadata, tags, votes), Firebase/Google Cloud Storage (audio files), optional PostgreSQL for analytics snapshots.
Audio/ML: librosa, pydub, ffmpeg for feature extraction/formatting; scikit-learn for clustering/similarity; optional PyTorch/ONNX for embeddings; Chromaprint/MinHash for duplicate detection.
QC & Aggregation: Weighted majority voting service (custom Python), Redis for job queues/rate limiting.
Analytics & Growth: PostHog or Mixpanel for funnels/retention; Firebase Remote Config for A/B of challenges/badges.
DevOps: Docker, GitHub Actions CI/CD, Vercel (web) + Expo EAS (mobile), Sentry for monitoring.
Optional marketplace integration: MTurk/Prolific adapters for burst verification tasks (if needed for pilots).



**How will you aggregate results from the crowd?**
Weighted Majority Voting: For each tag (mood, environment, noise level), compute a reliability-weighted vote
ML-Assisted QC (filter, not final arbiter): Audio heuristics/embeddings flag outliers (too silent, clipped, duplicates) and suggest priors; humans still decide.
Dispute Resolution / Expert Adjudication: If disagreement persists after N reviews, route to a small “trusted listener” pool (top-reputation users) for tie-break.


## Quality Control

**How will you ensure quality of crowd contributions?**
Pre-Submission Guardrails (likely going to be automated)
Device + Audio sanity: enforce 10–30s duration; reject files with clipping >10% frames, silence ratio >80%, or SNR < 5dB (estimate SNR via noise floor from lowest-energy percentile).
Format normalization: transcode to mono, 16kHz; loudness normalized (EBU-R128 target).
Geo validation: GPS must be within 30m of device reading; detect spoofing via sensor consistency (GPS jitter, step counter, IP geolocation); deny uploads from VPN/tor if flagged multiple times.
Duplicate detection: perceptual hashes/embeddings (e.g., MFCC/chroma/CLAP) with cosine similarity >0.95 ⇒ near-duplicate; keep the earliest or highest-quality copy.
Abuse: per-device rate limits (e.g., ≤10 uploads/day), CAPTCHAs after bursts, shadow-ban if anomaly score spikes.
Expert/Trusted Listener Escalations:
Top-rep users (90th percentile accuracy + tenure) resolve ties and edge cases.
Two-man rule for contested items: require agreement of 2 trusted listeners or 1 trusted + staff.

**Specific quality control methods:**
- [x] Gold standard questions (test questions with known answers)
- [ x] Majority voting across multiple workers
- [ x] Expert review or verification
- [x ] Attention checks or trap questions
- [ x] Reputation/qualification systems
- [x ] Statistical outlier detection
- [x ] Other: [specify]

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
User Engagement & Retention:
≥70% of users return to contribute or rate clips within one week of their first session.
Average of ≥3 uploads or verifications per active user.
Data Volume & Coverage:
At least 100 verified audio clips across ≥20 distinct locations in Philadelphia.
Balanced representation across environment types (ex indoor/outdoor, quiet/loud).
Quality & Accuracy:
≥90% agreement between crowd consensus and gold-standard labels on evaluation clips.
<5% of published sounds flagged as low quality or mislabeled after audit.
Crowd Health Metrics:
Stable median reputation score (±10%) after 2 weeks, indicates consistent labeling behavior.
Fewer than 5% of contributors flagged for spam or inattentive work.
System Performance & Usability:
Audio upload success rate ≥95%.
Median label verification time ≤48 hours.
Post-survey satisfaction score ≥4.0/5 on ease of use and enjoyment.

**What would success look like quantitatively?**
User Growth: 80+ active contributors in the first month, 500 total registered users by the end of the pilot.
Engagement: ≥70% 1-week retention; average of 3+ uploads or verifications per user.
Data Collection: 500+ verified audio clips across at least 20 unique locations by the end.
Label Accuracy: ≥90% agreement between crowd consensus and gold-standard tags.
Quality Control Efficiency: <5% of clips flagged as low-quality or mislabeled.
Cost Efficiency: <$0.50 per active worker and <$500 total pilot budget.
System Reliability: ≥95% successful upload rate and median verification turnaround under 48 hours.

## Challenges & Mitigation Strategies

_For each challenge, propose a mitigation strategy:_

**Challenge 1:** Low user retention after initial curiosity fades
**Mitigation:** Introduce ongoing engagement loops, daily themed sound quests,leaderboards, and seasonal badges for top contributors. Provide instant visual feedback when a user’s clip appears on the live map to reinforce contribution–impact connection.

**Challenge 2:** Poor or inconsistent audio quality (background noise, silence, duplicates)
**Mitigation:** Implement automatic audio validation (silence, clipping, and duplicate detection) before submission, followed by community verification and down-ranking of low-quality clips. Offer short in-app tutorials and tips for good recordings to improve data quality over time.

**Challenge 3:** Labeling inconsistency or careless tagging
**Mitigation:** Use gold-standard sound clips, attention checks, and weighted majority voting to detect unreliable workers. Maintain a dynamic reputation system where accurate contributors earn higher influence and access to special challenges, while low-accuracy users are prompted for refresher training.

## Prior Work

_Are there similar projects or systems? How is yours different?_

[Describe similar work and what makes your approach unique or improved]

**Specific related projects:**
- [Related Project 1]:Wheelmap.org A crowdsourced map that collects accessibility information for wheelchair users. Like SoundScape, it leverages volunteer contributions to enrich environmental data. However, Wheelmap focuses on visual and structural accessibility, while SoundScape captures the acoustic atmosphere of environments and that influences comfort, productivity, and mental well-being.
- [Related Project 2]:Soundcities An early web project that archived urban sound recordings from around the world. While it shares SoundScape’s focus on ambient audio, it lacks real-time crowd participation, gamification, and quality control. SoundScape modernizes this idea by adding interactive maps, crowd verification, reputation-weighted aggregation, and daily challenges, transforming static sound archives into a living, continuously updated community platform.

## Discussion Notes from Round 2

**What did you agree on?**
We agreed that SoundScape’s focus on audio-based environmental mapping is both unique and achievable within the course scope. We liked the idea of combining creativity (recording sounds) with data collection and verification, as it naturally aligns with crowdsourcing principles like aggregation and intrinsic motivation. We also agreed to emphasize gamified participation—leaderboards, challenges, and badges—as the key to retention.

**What concerns or pushback emerged?**
There was concern about data quality (ex noisy or irrelevant recordings) and privacy issues (capturing speech or private spaces). Worries about maintaining consistent participation once novelty wears off. These concerns led us to refine the design with automated audio filters, attention checks, and recurring themed challenges to sustain engagement while enforcing ethical guidelines.

**Why is this idea promising?**
SoundScape turns everyday environments into data points for collective exploration, something novel, accessible, and socially meaningful. It encourages both creativity and contribution, providing immediate feedback and a visual outcome (a living map). It also uses strong drives from Octalysis (social, accomplishment, epic meaning, etc.) Compared to other concepts, it has clear crowdsourcing value, strong intrinsic motivation loops, and potential for real-world relevance beyond the course!

**What makes this sustainable and feasible?**
Technically, the system can run on low-cost, existing infrastructure keeping the total budget under $500. The work relies on voluntary, low-friction participation rather than paid tasks, and most components (tagging, verification) can scale through crowd consensus. Sustainability comes from the platform’s self-reinforcing loop: users contribute → see impact → gain recognition → stay engaged. This makes SoundScape both feasible for the course timeline and viable for long-term continuation.

## Additional Notes

_Any other relevant information, inspirations, or considerations?_

[Optional: Add any additional context, ideas, or references]
