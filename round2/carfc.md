# Crowdsourcing Project Idea: Kinnect

_Replace [Project Title] with a creative name for your project_

## Authors

**Original Author:** Emily Lo, emlo

**Contributor:** Caroline Cummings, carfc

## Problem Statement

Staying consistent with daily fitness is difficult, and traditional fitness apps often fail to provide social accountability or motivation. Many people struggle to maintain healthy habits because they lack a sense of community or clear rewards for their efforts. Kinnect addresses this by turning individual activity into a crowd-powered challenge that motivates users through social engagement and tangible incentives.

## Target Audience

Fitness enthusiasts, casual exercisers, and anyone who wants motivation to stay active daily.

## Description

Kinnect is a crowdsourced fitness platform that transforms individual movement into a global, shared challenge. Users log their daily physical activity — walking, running, stretching, or workouts — which contributes to a live, interactive map showing how communities around the world are staying active. The system gamifies participation through streaks, team challenges, and points redeemable for rewards like fitness gear, class discounts, or charitable donations. By aggregating crowd-contributed activity data, Kinnect motivates consistent exercise, fosters social accountability, and turns personal fitness into a fun, community-driven habit.Kinnect is a crowdsourced fitness platform that transforms individual movement into a global, shared challenge. Users log their daily physical activity — walking, running, stretching, or workouts — which contributes to a live, interactive map showing how communities around the world are staying active. The system gamifies participation through streaks, team challenges, and points redeemable for rewards like fitness gear, class discounts, or charitable donations. By aggregating crowd-contributed activity data, Kinnect motivates consistent exercise, fosters social accountability, and turns personal fitness into a fun, community-driven habit.

## Project Type

_Select the category that best fits your project:_

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [ X ] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 5-8 key features or capabilities of your system. Expand from Round 1:_

1. Map: Visualize daily activity contributions from local communities and worldwide.
2. Daily Activity Logging
3. Streaks 
4. Personal Goals
5. Team and City Challenges
6. Leaderboards 
7. Points and rewards system

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
Social media users, students, family and friends. 

**What will they provide?**
Their fitness data.

**What skills do they need?**
Mobility, ability to use the mobile app. 

**Do skills vary widely? How?**
Yes, professional, club, intramural, recreational activities will be included depending on the level of the user. 

**How will you incentivize participation?**
Competition between people, cities, teams. FOMO. People's desire to workout more and be healthy.

**How much will it cost?**
It will be free for users but there will potentially be in-app purchases for equipment and additional points. 

We will have to pay for data storage. 

**Where will your data come from?**
Users can import fitness data from workouts. 

**How many crowd workers do you need?**
Can start with 10s but ideally 100s.

## Technical Approach

**What are the main steps/components in your system?**

1. User creates account with optional personal fitness goals and connecting account to devices and/or health account.
2. User log daily activity (workouts, steps, etc)
3. Join challenges and teams
4. Earn points
5. Engage with the community

**What parts are done by the crowd vs. automated?**
* Human: Logging activities, joining challenges, verifying achievements.
* Automated: Data aggregation, leaderboard updates, map visualizations, anomaly detection.

**What technologies/tools will you use?**
React Native (mobile app), Firebase/AWS (backend), MongoDB (data storage), Python (data processing), Mapbox API (map visualization), Fitbit/Apple Health APIs (data sync).

**How will you aggregate results from the crowd?**
Weighted aggregation by verified activity type and intensity. Outlier detection filters implausible data.

## Quality Control

**How will you ensure quality of crowd contributions?**

* Verification through synced devices when possible.

* Outlier detection for unrealistic submissions (e.g., 50-mile “walks”).

* Optional peer endorsements for challenges.

* User reputation system for consistent, trustworthy activity logging.

**Specific quality control methods:**
- [ ] Gold standard questions (test questions with known answers)
- [ ] Majority voting across multiple workers
- [ ] Expert review or verification
- [ ] Attention checks or trap questions
- [ X ] Reputation/qualification systems
- [X  ] Statistical outlier detection
- [ X ] Other: [Automated device-based validation]

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
Success Criteria:
* High daily engagement and retention.
* Growth in community participation over time.
* Measurable increase in user activity levels.
* Positive user feedback on motivation and usability.

**What would success look like quantitatively?**
* 100+ active users in first month.
* 70% weekly retention after four weeks.
* 1,000+ activities logged within first two months.
* <5% invalid data submissions.

## Challenges & Mitigation Strategies

_For each challenge, propose a mitigation strategy:_

**Challenge 1:** Maintaining user engagement after initial novelty fades.
**Mitigation:** Introduce rotating challenges, seasonal events, and new reward tiers to sustain motivation.

**Challenge 2:** Ensuring data integrity for self-reported activities.
**Mitigation:** Integrate wearable syncing and anomaly detection; promote social verification.

**Challenge 3:** Building community momentum at small scale.
**Mitigation:** Start with local university or workplace pilots, leveraging social groups to grow organically.


## Prior Work

_Are there similar projects or systems? How is yours different?_

[Describe similar work and what makes your approach unique or improved]

**Specific related projects:**
- Strava: Focuses on performance tracking but lacks global collaborative goals.
- Nike Run Club: Encourages running but emphasizes individual progress, not collective movement.

Kinnect’s Difference:
Unlike existing apps, Kinnect crowdsources global participation data to create real-time collective challenges, blending social motivation, gamified rewards, and community-level insights into one platform.

## Discussion Notes from Round 2

**What did you agree on?**
- Prioritize community engagement over complex fitness metrics.
- Focus on gamified incentives and visualization early on.

**What concerns or pushback emerged?**
- Scalability of backend with real-time map updates.
- Balancing privacy with public leaderboard visibility.

**Why is this idea promising?**
It merges the social power of crowdsourcing with fitness motivation—transforming solitary workouts into collaborative experiences.

**What makes this sustainable and feasible?**
Feasible as a class project under $500 using free-tier cloud tools. Scalable with user growth and partnerships (e.g., local gyms, student orgs).

## Additional Notes

_Any other relevant information, inspirations, or considerations?_

Future directions could include AI-generated personalized challenges, social badges, and integration with charitable organizations to convert collective activity into real-world impact.
