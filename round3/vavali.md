# Crowdsourcing Project Idea: Soundscape

## Authors

**Original Author:** Mingni Dong/ mdong126


**Round 2 Contributors:** 

**Round 3 Contributors:**  Vedha Avali (vavali), Leha Choppara (lehac), Nathan Lee (nzlee)

## Problem Statement

Online maps and city guides tell you where to go, but not what it feels like. There’s no good way to explore the soundscapes of cities, from quiet parks to bustling cafés which could help people choose better workspaces, travel destinations, or relaxation spots.


## Target Audience

**End Users:** Remote workers, travelers, urban planners, and people who love discovering new environments (musicians, game designers, etc.). To a more niche crowd, those with sensitivity to sounds. 

**Crowd Workers:**  Everyday users with smartphones, students, travelers, commuters.

**Stakeholders:** Urban planners, environmental researchers, tourism boards, accessibility advocates, and local businesses (cafés, co-working spaces, parks) who benefit from acoustic data for design, planning, or promotion.

## Description

SoundScape is a crowdsourced platform that builds an interactive global map of sounds. Users record short ambient audio clips from their surroundings like a park, café, or subway and upload them with location and mood tags. Other users also listen, rate, and verify these clips to classify areas by their sound environment (ex calm, lively, chaotic). There are also challenges that users can partake in to upload their sounds to specific vibes and get badges. Over time, the system aggregates all of these contributions into a living, community-driven map that helps people explore cities and spaces through their acoustic atmosphere.


## Project Type

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [x ] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

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
Recruitment will focus on Penn students, local volunteers in the Philadelphia area, and social media campaigns. Participants will be encouraged to share their soundscapes via the app or website. Partnerships with student organizations and local tourism boards can boost engagement.

**What will they provide?**
They will upload sound clips, labels for the sound clips, ratings of the clips.

**What skills do they need?**
Participating would require the ability to understand english, and at least average ability to hear.


**Do skills vary widely? How?**
Some users will have a better ear for distinguishing sound qualities (e.g., background chatter vs. music), making them more accurate taggers and verifiers. Others might be better at recording clear, representative clips due to higher-quality microphones or quieter environments. Additionally, experienced users will develop stronger intuition for consistent labeling and mood classification, while casual participants may focus more on creative or exploratory recordings. Over time, reputation scores and feedback loops will help surface and reward these more skilled contributors.

**How will you incentivize participation?**
SoundScape uses a gamified intrinsic motivation model to encourage sustained participation. Contributors earn points and badges for verified uploads, ratings, and challenge completions. A leaderboard highlights top Sound Explorers by city or category, fostering friendly competition. Each contribution immediately appears on the global sound map creating visible impact and emotional reward for users who enjoy sharing pieces of their environment. Occasional themed challenges (ex Quietest Spot on Campus Week) offer small digital rewards or feature highlights to keep engagement high without monetary payments.

**Budget & Cost Analysis:**
- Estimated cost per task: $0.0
- Estimated cost per worker: $0.50
- Number of tasks needed: at least 150 verified audio submissions
- Total estimated budget: $500 
- Justification: This budget is realistic within course constraints because SoundScape minimizes financial costs by leveraging intrinsic and gamified motivation rather than paid labor. Infrastructure is lightweight, built on free or low-cost tiers of Firebase and Mapbox—and tasks are small, engaging, and scalable

**Where will your data come from?**
All data will be user-generated through crowd contributions. Participants record and upload short ambient audio clips via the SoundScape web or mobile app, which automatically tags each submission with time, location, and basic acoustic metadata. Additional contextual data (ex mood labels, environment type) comes from crowd tagging and verification tasks. For baseline geographic information and map visualization, the system will use open-source APIs such as OpenStreetMap or Mapbox. No scraping or proprietary datasets will be required.


**Scale Requirements:**
- Minimum viable crowd size: 100 workers
- Target crowd size for full functionality: 500 workers would be most ideal
- Potential to scale to: 1000 workers

## Technical Architecture

**System Components:**

Frontend interfaces: Web app (React/Next.js + Tailwind, Web Audio API) and optional mobile app (React Native/Expo) for recording, tagging, and browsing the sound map.
Backend API: Python FastAPI (or Node/Express) for auth, upload orchestration, QC pipelines, aggregation endpoints, and admin tools.
Data layer: Firebase Firestore (metadata, tags, votes, reputations) + Cloud Storage (audio files); optional PostgreSQL warehouse for analytics.
Audio/ML services: Worker queue + Python services using librosa/pydub/ffmpeg for feature extraction, QC heuristics, duplicate detection, and scikit-learn (optional PyTorch) for clustering/similarity.
External APIs: Mapbox GL / OpenStreetMap for maps & geocoding; optional MTurk/Prolific adapters for burst verification during pilots.

**Detailed Workflow:**

1. User records and uploads a short ambient clip.  
2. System extracts metadata (volume, frequency, etc.) and tags location.  
3. Crowd rates and labels clip by mood and environment.  
4. Weighted voting combines tags into consensus labels.  
5. Map updates with verified clip and aggregated mood profile.  
6. Gamification updates user profile and leaderboards. 

**Human vs. Automated Tasks:**

| Task | Performed By | Why? |
|------|--------------|------|
| Recording & Uploading | Human | Contributors capture short ambient audio clips from their surroundings. |
| Tagging & Labeling | Human | Users describe each clip by mood (e.g., calm, energetic), environment type (e.g., street, café, park), and perceived noise level.|
| Verification & Rating | Human | Crowd members listen to others’ clips, confirm or dispute tags, and rate audio quality. |
| Creative Participation | Human | Users engage in themed challenges and explore the sound map, driving ongoing contributions. |
|Metadata Extraction | Automated | System analyzes volume, duration, and frequency spectrum for each clip. |
|Geo-Tagging & Mapping| Automated | Automatically assigns GPS coordinates and visualizes clips on an interactive map.|
|Aggregation & Quality Control:| Automated | Weighted majority voting integrates multiple crowd labels while prioritizing high-reputation contributors. |
|Audio Similarity & Clustering | Automated |  Algorithms group related sounds and detect duplicates or corrupted submissions. |


**Technologies & Tools:**
- Frontend: React + Tailwind CSS, Web Audio API
- Backend: Python FastAPI (or Node/Express)
- Database: Firebase Firestore, PostgreSQL
- ML/AI: Scikit-learn
- Crowdsourcing Platform: MTurk
- Hosting: AWS
- Other: Worker queue + Python services using librosa/pydub/ffmpeg for feature extraction

**Aggregation Method:**
Weighted Majority Voting: For each tag (mood, environment, noise level), compute a reliability-weighted vote
ML-Assisted QC (filter, not final arbiter): Audio heuristics/embeddings flag outliers (too silent, clipped, duplicates) and suggest priors; humans still decide.
Dispute Resolution / Expert Adjudication: If disagreement persists after N reviews, route to a small “trusted listener” pool (top-reputation users) for tie-break.

## Quality Control

**Quality Control Strategy:**
Pre-Submission Guardrails (likely going to be automated)
Device + Audio sanity: enforce 10–30s duration; reject files with clipping >10% frames, silence ratio >80%, or SNR < 5dB (estimate SNR via noise floor from lowest-energy percentile).
Format normalization: transcode to mono, 16kHz; loudness normalized (EBU-R128 target).
Geo validation: GPS must be within 30m of device reading; detect spoofing via sensor consistency (GPS jitter, step counter, IP geolocation); deny uploads from VPN/tor if flagged multiple times.
Duplicate detection: perceptual hashes/embeddings (e.g., MFCC/chroma/CLAP) with cosine similarity >0.95 ⇒ near-duplicate; keep the earliest or highest-quality copy.
Abuse: per-device rate limits (e.g., ≤10 uploads/day), CAPTCHAs after bursts, shadow-ban if anomaly score spikes.
Expert/Trusted Listener Escalations:
Top-rep users (90th percentile accuracy + tenure) resolve ties and edge cases.
Two-man rule for contested items: require agreement of 2 trusted listeners or 1 trusted + staff.

**Specific QC Mechanisms:**
- [ ] Gold standard questions (test questions with known answers)
- [x ] Majority voting across multiple workers
  - _Details: Each clip rated by 3–5 users; consensus required for publication.  
- [x ] Expert review or verification
  - _Details: High-reputation users verify edge cases.  
- [ ] Attention checks or trap questions
  - _Details: [What types? How often? Consequences?]_
- [x ] Reputation/qualification systems
  - _Details: Accuracy-based weighting over time.  
- [x ] Statistical outlier detection
  - _Details: Low SNR or duplicate sounds are flagged for removal.  
- [ ] Redundancy and agreement metrics
  - _Details: [How much redundancy? What agreement threshold?]_
- [ ] Other: [specify]
  - _Details: [Explain custom QC approaches]_

**Handling Low-Quality Work:**
Automatic Rejection: Audio clips that fail automated checks (e.g., too silent, clipped, duplicates, or privacy violations) are immediately rejected with feedback explaining the issue.
Re-Tasking: Low-confidence clips (e.g., <70% consensus or high entropy in labels) are re-queued for additional verification by new contributors until agreement reaches a confidence threshold.
Worker Penalties: Contributors who repeatedly submit poor-quality recordings or fail gold-standard checks will see their reputation score decrease, reducing their weighting in aggregation and limiting future task access.
Progressive Feedback: Instead of harsh penalties alone, low-performing users receive constructive feedback or micro-tutorials to improve future contributions.
Escalation: Recurrent abuse (spam uploads or falsified locations) triggers automated suspension and manual admin review.


## Evaluation & Success Metrics

**Primary Success Metrics:**

Engagement Rate: ≥70% of new users contribute at least one clip or verification.
Data Quality: ≥90% agreement across mood tags per clip.
Geographic Coverage: ≥100 verified clips across 20 Philadelphia locations in pilot.

**Evaluation Methodology:**

Measure upload frequency, retention, and inter-rater agreement. Conduct user satisfaction surveys and analyze participation patterns over time.


**Baseline Comparisons:**
- Compare to existing ambient sound datasets (e.g., Soundcities) to show higher diversity and coverage.  
- Improvement over the baseline will be measured using both **quantitative metrics** (coverage, quality, engagement) and **qualitative evaluations** (user satisfaction and usefulness).  

**Success Criteria:**
- Minimum viable success: 100 verified clips and ≥60% engagement.
- Target success: 500 verified clips, ≥90% tag consensus.
- Stretch success:1,000 verified clips across multiple cities.

## Challenges & Mitigation Strategies

**Challenge 1:** Low user retention after initial curiosity fades
- **Why it's a risk:** A drop in participation would lead to fewer uploads, reduced verification activity, and lower data diversity, undermining the core value of the SoundScape map and preventing the system from reaching critical mass.
**Mitigation:** Introduce ongoing engagement loops, daily themed sound quests,leaderboards, and seasonal badges for top contributors. Provide instant visual feedback when a user’s clip appears on the live map to reinforce contribution–impact connection.
-**Backup plan:** If engagement still drops, launch community events or competitions (Sound of the Week, campus sound hunts) and partner with local organizations to promote participation. 

**Challenge 2:**Poor or inconsistent audio quality (background noise, silence, duplicates)
- **Why it's a risk:** Low-quality or redundant recordings reduce the reliability of sound data, making tags inaccurate and map visualizations misleading. Excessive noise, silence, or duplicates can also frustrate users and damage trust in the platform’s credibility.
- **Mitigation strategy:** Integrate automated audio validation tools (silence detection, clipping checks, and duplicate identification via audio fingerprinting). Provide real-time feedback during recording (too noisy, too short) and short tutorials on how to capture clean, representative sounds. Use crowd verification rounds to flag unclear clips and down-weight poor contributors in future tasks.
- **Backup plan:** If quality issues persist, manually review a sample of submissions each week and re-task flagged clips to trusted contributors for replacement. In severe cases, restrict upload privileges for consistently low-performing users or switch to verified trusted recorders tiers with higher reliability scores.

**Challenge 3:** Inconsistent tagging  
- **Why it's a risk:** Subjective perception of sound mood.  
- **Mitigation strategy:** Weighted majority voting and calibration tasks.  
- **Backup plan:** Machine-learning-based clustering to auto-suggest likely tags.  

## Prior Work & Related Projects

**Similar Existing Systems:**

1. **Wheelmap.org**
   - Description: A global, crowdsourced map where volunteers mark and rate places by wheelchair accessibility, using a simple green/yellow/red traffic-light system; built on OpenStreetMap and available on web and mobile.
   - Similarities: Relies on volunteer geo-tagged contributions; uses consensus and simple categorical labels to make place-based information useful to specific user groups; demonstrates how open mapping plus lightweight gamification can scale.
   - Differences: Focuses on physical accessibility attributes rather than acoustic environments; uses visual traffic-light ratings rather than audio clips, mood tags, or audio-quality QC; SoundScape adds audio processing, verification workflows for sound labels, and exploratory features like similarity clustering.
   - Citation/Link: Wheelmap.org

2. **Soundcities**
   - Description:  SoundCities is one of the earliest online “sound maps” , an open database of urban sound recordings collected from cities worldwide, originally launched by artist Stanza. It allows users to listen to ambient clips tied to specific geographic locations.
   - Similarities: Like SoundScape, it connects audio recordings to geospatial data, enabling users to explore the acoustic character of different places. Both aim to create a sensory representation of the world through sound.
   - Differences: SoundScape goes beyond archival listening by introducing active crowdsourcing, gamified participation (Octalysis framework), automated quality control, and real-time verification. It transforms a static art archive into a dynamic, social, and continuously updated platform where users contribute, rate, and explore collaboratively.
   - Citation/Link: http://www.soundcities.com

3. **Google Maps**
   - Description: A global mapping platform with community contributions (reviews, photos, Q&A) via the Local Guides program, which awards points and badges for published contributions.
   - Similarities: Uses large-scale user contributions and lightweight incentives to enrich place understanding; demonstrates viable patterns for contribution loops, profiles, and moderation at scale.
   - Differences: Focus is on navigation and business attributes, not acoustic mood; audio is not a primary data type and recent product changes indicate a deprioritization of certain social features; SoundScape’s core unit is short ambient clips with mood/noise labels, verified via consensus and audio QC.
   - Citation/Link: https://www.google.com/maps

**Lessons from Past Course Projects:**
We learned that low participation after launch is definitely an issue that makes it hard to collect data. Technical polish alone really isn’t enough. To address this, SoundScape focuses on intrinsic gamified engagement (from the Octalysis framework). Many projects also lacked clear differentiation from existing platforms. Ours does as no other platform has the same exact features.

## Ethical Considerations

**Potential Ethical Issues:**

- Issue 1: Privacy concerns with user data: Users are uploading geo-tagged audio clips, which may inadvertently capture sensitive or private information. These recordings may contain background conversations or identifiable sounds.

- Issue 2: Fair compensation for crowd workers: As the project relies on crowdsourcing, there may be concerns about compensating workers fairly, especially since the model is primarily based on intrinsic motivation rather than financial incentives.

- Issue 3: Potential for misuse or harmful content: Users might upload offensive, inappropriate, or harmful audio clips, potentially leading to legal or reputational issues for the platform.

**Mitigation Strategies:**
- Privacy concerns with user data: Implement privacy measures by anonymizing the audio files, ensuring no personally identifiable information (PII) is collected with the clips. Provide clear privacy policies and user consent mechanisms before uploads. Additionally, introduce content moderation systems to detect and reject sensitive or private content automatically (e.g., background conversations).

-Fair compensation for crowd workers: Focus on intrinsic motivators such as gamification, badges, and recognition, which help build a sustainable and rewarding community. If necessary, explore small, non-monetary incentives such as feature highlights or community recognition for top contributors, rather than direct financial compensation.

- Potential for misuse or harmful content: Establish community guidelines that prohibit the uploading of inappropriate content. Use a combination of automated systems (e.g., audio quality detection, inappropriate content flags) and human moderators (e.g., trusted listeners) to review and address harmful content. If violations persist, use automated penalties such as suspension or banning.

**IRB Considerations:**
This project may not require IRB approval, as it primarily involves crowdsourcing public domain content (ambient sounds), and users are not providing sensitive personal data. However, if any of the recordings inadvertently capture private or sensitive information, or if the platform collects any identifiable data (e.g., voice recognition or exact locations), the project may need to undergo IRB review to ensure compliance with ethical standards regarding data privacy. Additionally, participants will be made aware of their rights and the terms of participation through clear consent forms.




## Business Viability (Optional)

_If your project has business potential, consider:_

**Revenue Model:**
SoundScape could generate revenue through a freemium data and analytics model. The core sound map remains free for the public, while premium access is offered to urban planners, environmental researchers, wellness apps, and real estate developers seeking noise and mood analytics. Potential revenue streams include API subscriptions, licensing aggregated acoustic datasets, and partnerships with travel or mindfulness platforms that integrate “sound-based exploration” features.

**Market Size:**
The global smart city analytics and environmental data markets are rapidly growing. Potential customers include thousands of city governments, academic research groups, and startups focused on spatial intelligence, tourism, or wellness. Even niche adoption, such as campus sound mapping or city-level pilots, could attract hundreds of institutional users interested in acoustic data for design and accessibility planning.


**Competitive Advantage:**

Unlike other mapping platforms that emphasize visual, textual, or navigational information, SoundScape offers a novel sensory layer sound. Its crowdsourcing model creates real-time, diverse coverage at low cost, while gamified participation ensures continuous data collection. This blend of creativity, data richness, and emotional connection gives SoundScape a unique value proposition compared to static archives or corporate mapping tools.

**Sustainability:**
Yes, SoundScape is designed to be sustainable beyond the course because it relies on intrinsically motivated participation and low-cost infrastructure rather than paid labor. The system’s gamified feedback loops (leaderboards, badges, and community recognition) encourage ongoing contributions without continuous oversight. Hosting costs remain minimal through Firebase and Mapbox free tiers, and the open-source codebase allows future students or volunteers to maintain and expand it. Long-term sustainability could come from university partnerships, research collaborations, or integration with wellness, tourism, or urban planning organizations interested in real-time acoustic data. This mix of community engagement and institutional relevance ensures the platform can persist and evolve after the class concludes.

## Steel-Man Discussion (Round 3)

**Idea A Steel-Man:**
We strengthened **SoundScape** into a robust, multi-layered crowdsourcing platform that not only collects ambient sounds but also integrates social participation, gamification, and automated quality control. The strongest version of the idea includes mood and environment tagging, daily challenges, and a reputation-based verification system that ensures reliable data while keeping contributors engaged. The project also incorporates machine learning for clustering and detecting duplicate or low-quality audio. We framed SoundScape as a “living sound map” that grows richer over time, bridging creativity, exploration, and research. Its appeal lies in how it transforms ordinary urban environments into community data and provides tangible value for users, researchers, and urban planners alike.

**Idea B Steel-Man:**
The **Where2Go** concept was developed into a crowdsourced, real-time bathroom locator app that helps users find accessible, clean, and safe restrooms in public areas—especially useful on large campuses or in cities. In its strongest version, Where2Go crowdsources restroom data from users who submit and rate bathrooms based on cleanliness, accessibility, safety, and amenities. It incorporates live updates, filters (e.g., gender-neutral, wheelchair accessible), and an incentive system where contributors earn badges for verified reviews. The system also includes a report/verification mechanism to keep listings accurate and up to date. This version of the idea emphasized social good, inclusivity, and practical utility for everyday users such as travelers, students, and families.


**Why We Chose This Idea:**
We selected **SoundScape** because it was more **original**, **ethically straightforward**, and **achievable within the course timeline**. Unlike *WhereToGo*, which overlaps heavily with existing apps like Google Maps or Yelp, SoundScape introduces a novel sensory dimension—sound—as the medium of exploration. It’s inherently creative, socially engaging, and scalable without high moderation or legal risks. From a crowdsourcing perspective, it clearly aligns with principles of aggregation, redundancy, and intrinsic motivation. SoundScape also fits the course constraints better, with a feasible $500 budget and a simple prototype path (record → verify → map visualization).

**What We Agreed On:**
We agreed that SoundScape’s emotional and sensory appeal makes it uniquely engaging. It provides immediate visual and auditory feedback for contributions, creating a clear contribution–impact loop that motivates repeat participation. The idea also has strong long-term potential beyond the course, serving academic, creative, and civic purposes.

**What Concerns Emerged:**
Our main concerns centered on privacy (e.g., accidental voice capture), uneven data coverage across locations, and the possibility of engagement decline after novelty fades. There were also discussions about ensuring consistent labeling quality and preventing background noise from skewing results.


**Key Insights from Round 3 Discussion:**
[What did you learn from the group discussion that improved the idea?]
During the Round 3 discussion, we realized that SoundScape’s success depends as much on user emotion and experience as on data quality. Feedback emphasized the need to make participation feel personally meaningful and immediately rewarding, not just functional. This led us to strengthen our Octalysis-based design, adding more social recognition features (leaderboards, “Sound of the Week”) and daily challenges to boost engagement.
We also learned the importance of clear data ethics and privacy safeguards—for example, automatically detecting and filtering speech or private recordings to ensure responsible collection. Finally, peers encouraged us to define specific use cases (like urban planning or stress-free travel) to make the project’s real-world impact more concrete. These insights made SoundScape more focused, socially engaging, and ethically sound.


## Implementation Timeline (Optional)

**Week 1–2:** Prototype design, basic map integration, and upload interface.  
**Week 3–4:** Implement tagging, rating, and basic QC pipeline.  
**Week 5–6:** Add gamification (badges, leaderboards) and aggregation logic.  
**Week 7–8:** Conduct pilot in Philadelphia with students, analyze data, and refine UX.

## Additional Notes

## References & Inspiration


1. [Wheelmap.org](https://wheelmap.org)  
2. [Soundcities](http://www.soundcities.com)  
3. [NoiseTube](http://noisetube.net)  
4. Octalysis Framework – Yu-kai Chou (for gamification design)

