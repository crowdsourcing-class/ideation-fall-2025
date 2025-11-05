# Crowdsourcing Project Idea: TrashTag Tracker

## Authors

**Original Author:** Jun Hyun Park (andrewpp)

**Contributor:** Eric Lee

## Problem Statement

Urban and campus areas accumulate litter in places not regularly monitored by sanitation services. Volunteers want to help clean up but lack accessible information about where trash is most severe or whether cleanup has already happened. This system aims to crowdsource accurate reporting and verification of litter hotspots to guide meaningful cleanup action.

## Target Audience

Primary users include college students, local residents, environmentally active social media users, and volunteer organizations. Crowd workers will be anyone with a smartphone who is willing to report or verify trash conditions in their community.

## Description

TrashTag Tracker is a crowd-powered platform where users submit photos and locations of trash hotspots and where other users confirm or dispute those reports over time. These crowd contributions generate a live “Cleanup Map” that highlights high-priority zones needing volunteer attention. Once cleanup occurs, users upload proof and the platform updates hotspot status after verification. This fosters community collaboration and keeps environmental progress transparent.

## Project Type

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [x] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

1. Photo and GPS-based trash hotspot submission
2. Verification workflow for confirming trash presence and cleanup
3. Live cleanup map showing hotspot severity and recency
4. Gamification (badges, streaks, leaderboard) to motivate participation
5. Duplicate image and location detection

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**  
Volunteers from the campus community, social media outreach, environmental clubs.

**What will they provide?**  
Images, geolocation tags, trash category labels, verification votes.

**What skills do they need?**  
Basic smartphone and internet use; no specialized expertise required.

**Do skills vary widely? How?**  
Some users will be more familiar with environmental sorting (e.g., recyclables), but majority voting mitigates differences.

**How will you incentivize participation?**  
Gamification: badges for cleanup, leaderboards, positive social impact, potential partnerships with campus orgs for rewards.

**How much will it cost?**  
Estimated under **\$500** total using free hosting tiers; potentially ~$50–100 for initial outreach incentives or small paid validation tasks.

**Where will your data come from?**  
Entirely user-generated uploads (photos + GPS).

**How many crowd workers do you need?**  
Around **100–300** active contributors to effectively cover a campus-sized region.

## Technical Approach

**What are the main steps/components in your system?**
1. User submits photo + geolocation + trash category.
2. System stores and clusters reports into hotspots.
3. Other users verify presence or mark duplicates.
4. After cleanup report, multiple users confirm status change.
5. Map UI updates severity and completion indicators.

**What parts are done by the crowd vs. automated?**
- **Crowd:** Labeling, verification, submitting cleanup evidence.
- **Automation:** Spatial clustering, duplicate detection, ranking hotspots by severity.

**What technologies/tools will you use?**
React or mobile web frontend, Firebase/Supabase backend, basic computer vision APIs for duplicate detection, Mapbox/OpenStreetMap for visualization.

**How will you aggregate results from the crowd?**
Weighted majority voting based on trust scores and report recency.

## Quality Control

**How will you ensure quality of crowd contributions?**
Redundant validation for all submissions, reporting history scoring per user, automated flagging of suspicious or inconsistent uploads.

**Specific quality control methods:**
- [ ] Gold standard questions (test questions with known answers)
- [x] Majority voting across multiple workers
- [x] Expert review or verification (optional through moderators)
- [x] Attention checks or trap questions (simple validation rules)
- [x] Reputation/qualification systems
- [x] Statistical outlier detection
- [ ] Other: [specify]

## Evaluation & Success Metrics

**How will you know if your project succeeds?**  
High engagement and accurate monitoring of hotspots that lead to real cleanup outcomes.

**What would success look like quantitatively?**
- 100+ unique hotspot submissions
- 80%+ verified cleanup confirmations
- 90% accuracy in duplicate/trash detection vs. ground truth
- 100+ active contributors within first 4 weeks

## Challenges & Mitigation Strategies

**Challenge 1:** Fake or low-quality submissions  
**Mitigation:** Reputation scoring + multiple independent confirmations

**Challenge 2:** Lack of sustained user engagement  
**Mitigation:** Gamification and real-time progress visualization

**Challenge 3:** Privacy/geolocation concerns  
**Mitigation:** Blur tool for sensitive images; location rounding options

## Prior Work

No prior similar projects.

## Discussion Notes from Round 2

**What did you agree on?**  
Focus on microtasks and verifying both the presence and removal of trash.

**What concerns or pushback emerged?**  
Ensuring that enough users consistently verify hotspots rather than only submitting them.

**Why is this idea promising?**  
Low barrier to entry, high social/environmental value, and strong intrinsic motivation from participants.

**What makes this sustainable and feasible?**  
Relies on volunteers and free-tier services, small geographic scope initially, easy to scale as interest grows.

## Additional Notes
