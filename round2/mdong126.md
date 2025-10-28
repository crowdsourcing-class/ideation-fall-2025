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
[Clearly distinguish human tasks from computational tasks]

**What technologies/tools will you use?**
[E.g., Python, React, AWS, specific ML libraries, MTurk API, etc.]

**How will you aggregate results from the crowd?**
[E.g., majority voting, weighted averaging, expert adjudication, ML filtering, etc.]

## Quality Control

**How will you ensure quality of crowd contributions?**

[Describe your quality control mechanisms in detail]

**Specific quality control methods:**
- [ ] Gold standard questions (test questions with known answers)
- [ ] Majority voting across multiple workers
- [ ] Expert review or verification
- [ ] Attention checks or trap questions
- [ ] Reputation/qualification systems
- [ ] Statistical outlier detection
- [ ] Other: [specify]

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
[Describe specific metrics or evaluation criteria]

**What would success look like quantitatively?**
[E.g., "90% accuracy," "100 users in first week," "$X cost per task"]

## Challenges & Mitigation Strategies

_For each challenge, propose a mitigation strategy:_

**Challenge 1:** [Describe challenge]
**Mitigation:** [How will you address it?]

**Challenge 2:** [Describe challenge]
**Mitigation:** [How will you address it?]

**Challenge 3:** [Describe challenge]
**Mitigation:** [How will you address it?]

## Prior Work

_Are there similar projects or systems? How is yours different?_

[Describe similar work and what makes your approach unique or improved]

**Specific related projects:**
- [Related Project 1]: [How it relates and how you differ]
- [Related Project 2]: [How it relates and how you differ]

## Discussion Notes from Round 2

**What did you agree on?**
[Key points of agreement between partners]

**What concerns or pushback emerged?**
[Questions, challenges, or areas of uncertainty discussed]

**Why is this idea promising?**
[Explain why you chose to develop this idea over the alternative]

**What makes this sustainable and feasible?**
[Specific reasons this can work within course constraints]

## Additional Notes

_Any other relevant information, inspirations, or considerations?_

[Optional: Add any additional context, ideas, or references]
