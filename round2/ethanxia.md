# Crowdsourcing Project Idea: CrowdScout

## Authors

**Original Author:** Ethan Xia (ethanxia)

**Contributor:** Connor Cummings (connorcc)

## Problem Statement

Sports recruiting is a tedious and difficult process, one which is not accessible to everyone and can dramatically change the lives of prospective athletes in the future. Additionally, underrated players may be drastically overlooked and never get the chance to actually be seen by a scout or recruiter. We are addressing the challenge of developing 

## Target Audience

The target audience will be sports recruiters and non-professional athletes looking to be scouted/recruited. The crowd workers will be general users of the app, who scroll through their "sports feed" and upvote/downvote based on how they perceive the highlight. 

## Description

CrowdScout is a crowdsourcing platform where athletes upload highlight videos and performance data. The crowd (fans, coaches, scouts, and general users) can rate highlights through a like/dislike system and comment on their performances. Using aggregated ratings and engagement metrics and a "for-you" like algorithm, the system ranks and recommends promising players to recruiters. 

## Project Type

_Select the category that best fits your project:_

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [x] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 5-8 key features or capabilities of your system. Expand from Round 1:_

1. Video Rating System - a like/dislike system used to rank videos 
2. Skills Tags - Sport specific tagging to clarify the highlights (defense, soccer, etc.)
3. Crowd Consensus Dashboard / Leaderboard - We can see trending highlights / top athletes to look out for
4. Athlete Video Uploads - Users can upload their own highlights and generate content of their top plays
5. Weighted aggregation - Prioritize ratings from verified coaches / experts (so that critics/fans can also judge for themselves)
6. Personalized recommendations for videos and athletes using ML models
7. [Feature 7 - optional]
8. [Feature 8 - optional]

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
General users, sports enthusiasts, college coaches, professional scouts, student-athletes using the app. Specifically, this will be beneficial for athletes who do not have the resources to go through a typical recruiting/scouting process. This can be promoted through social media, schools, and sports communities. 

**What will they provide?**
Ratings, likes/dislikes, comments, and qualitative feedback on performance videos. 

**What skills do they need?**
Basic internet skills and scrolling skills. Verified coaches and scouts need coaching skills to identify potential recruits. 

**Do skills vary widely? How?**
Yes, skills can vary from player to player and also coach to coach / scout to scout. Fans and general users of the app can provide subjective impressions while coaches offer more technical insight. The system can weigh their input accordingly. 

**How will you incentivize participation?**
Gamification (like TikTok) through leaderboards, points, badges, followers, likes. Recognition for top contributors and social media features like sharing top-rated athletes. Additionally, recommending 'Athlete's on the Rise' to scouts. 

**How much will it cost?**
Usage is free but content moderation is the biggest cost. Paid pilot on MTurk could be some relatively inexpensive per-video cost. 

**Where will your data come from?**
User-generated data through individual athlete uploads, supplemented with public sports datasets such as MaxPreps or NCAA data to correlate with how their current live season stats are. 

**How many crowd workers do you need?**
At least 10 athletes to continually upload videos (but the more users the better). 

## Technical Approach

**What are the main steps/components in your system?**

1. Step 1: User uploads videos and fills out tags (sport, position)
2. Step 2: Crowd rates and comments on videos in app feed
3. Step 3: System aggregates ratings using weighted averages based on rater credibility
4. Step 4: Model analyzes athlete performance and predicts a potential score for recruitability
5. Step 5: Recruiters browse the app/dashboard to see top ranked/filtered athletes. 

**What parts are done by the crowd vs. automated?**
The crowd rates, comments, flags low-quality videos. The algorithm, aggregation, and suggestions are all automated. 

**What technologies/tools will you use?**
Python, React, AWS or some database, PyTorch, Spark. 

**How will you aggregate results from the crowd?**
Weighted averaging combining crowd consensus, coach ratings, and engagement metrics. 

## Quality Control

**How will you ensure quality of crowd contributions?**

[Describe your quality control mechanisms in detail]

**Specific quality control methods:**
- [ ] Gold standard questions (test questions with known answers)
- [x] Majority voting across multiple workers
- [x] Expert review or verification
- [x] Attention checks or trap questions
- [x] Reputation/qualification systems
- [x] Statistical outlier detection
- [ ] Other: [specify]

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
By measuring engagement, data quality, and user activity. 

**What would success look like quantitatively?**
"100 users in the first week,' '10,000 uploads in the first month,' '20% increase in visibility for low-profile athletes'

Challenges & Mitigation Strategies
Challenge 1: Low-quality or biased ratings from casual users
 Mitigation: Implement a rater reputation system that weights scores more heavily from verified coaches/scouts and from users whose past ratings correlate with eventual “success” signals (e.g. other experienced users agreed, video got sustained engagement). Add light moderation: flag videos with unusually polarized ratings for expert review. Provide simple rating rubrics (“athleticism,” “skill,” “game impact”) to reduce noise.
Challenge 2: Cold start and adoption (not enough videos or raters early on)
 Mitigation: Seed the platform with sample highlight clips from public/online HS games or open datasets, and run short campaigns with school teams/clubs to upload at least one clip per player. Add in-app incentives (badges, “Top Scout of the Week,” “Rising Athlete” section) to get early users to rate more than they upload. If needed, run a small MTurk/Prolific batch to bootstrap initial ratings so the feed looks “alive.”
Challenge 3: Gaming the system / coordinated upvoting by friends
 Mitigation: Detect suspicious rating patterns (many upvotes in a short time from linked accounts/IPs), cap the influence of new accounts, and blend engagement signals (watch time, completion, diversity of raters) into the final score. Reserve a “coach-only” or “verified scout” score that cannot be inflated by friends and show it separately in the recruiter dashboard.


## Prior Work

**Specific related projects:**
- Hudl.com: A video analysis website for recruiters to check out athlete highlights. CrowdScout is different because this is more crowd focused, rather than specifically recruiter focused. Everyone, including fans, athletes, and recruiters, can use the app. Also, instead of posting videos to a specific profile, videos are pushed to a centralized "feed," similar to a social media app.

Discussion Notes from Round 2
What did you agree on?
 We agreed that CrowdScout could be a genuinely useful tool for surfacing overlooked talent, especially high school athletes who don’t have access to traditional showcases or club pipelines. The exposure piece — getting more eyes on lesser-known athletes — is the core value.
What concerns or pushback emerged?
 Main concerns were around quality and scale: how to ensure that the ratings are trustworthy and not just popularity contests, and how to get enough users so that “crowd” signals actually mean something. There was also a question about adoption — the system becomes more valuable only when lots of people participate.
Why is this idea promising?
 It’s promising because we’ve seen the pain points in HS recruiting firsthand: it’s expensive, time-consuming, and often depends on being in the right place at the right time. A centralized, crowd-amplified feed lowers the barrier for athletes who can’t travel or pay for elite camps. It also gives recruiters a faster way to find “interesting” players without watching hours of video.
What makes this sustainable and feasible?
 Once the platform is built, most of the data collection (uploads, ratings, comments) is done by users. The ranking/aggregation layer can be iterated on without heavy manual work. For the course, we can prototype with synthetic or sample videos and a small crowd to validate the rating → ranking → recommendation loop.

