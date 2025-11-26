# Crowdsourcing Project Idea: Urban Explorer

## Authors

**Original Author:** Katherine Yue (kyue)

**Contributor:** James Doh (dohj0109) & Omar Pareja (pareja)

## Problem Statement
[In 2-3 sentences, describe the problem your project will solve. What pain point or challenge are you addressing?]
With city events scattered across multiple platforms, it can be hard for residents to discover what's happening nearby (e.g. open mic nights, volunteer drives, etc). On the other side, many local or spontaneous events go unnoticed because there's a lack of a centralized, up-to-date platform that showcases these events. 


## Target Audience

[Who will use this system? Who will be your crowd workers? Be specific about the types of users and workers involved.]
Not only the residents, but people who are visiting the city, small businesses advertising their events, and others who want to discover or promote nearby happenings.

## Description

[Provide a clear description of your crowdsourcing project in 3-4 sentences. What will the system do? How will it work at a high level?]
This platform is a crowdsourced event discovery app that visualizates what's happening in a city to allow residents to easily find nearby events. With an interactive map for easy viewing, users can post local events, verify existing listings by upvoting or confirming details, and flag outdated ones. Events fade out automatically after they expire. Over time, crowd participation creates a self-sustaining ecosystem of local information that connects residents and visitors across the city.

## Project Type

_Select the category that best fits your project:_

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [X] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 5-8 key features or capabilities of your system. Expand from Round 1:_

1. Interactive Map – shows the events in a user friendly way.
2. Posting Feature – quick workflow that will allow users to quickly upload events.
3. Verification System – users must go through a verification system to verify their identity before they can post or see any postings.
4. Notification System – upcoming events within radius
5. Engagement Leaderboard – badges when you post more events, badges when you attend more events

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
[E.g., MTurk, volunteers, social media users, students, etc.]
Mainly volunteers, there can also be social media users and such.

**What will they provide?**
[E.g., labels, votes, creative content, transcriptions, etc.]
Event listings, improved verification, flags if inappropriate postings.

**What skills do they need?**
[E.g., bilingual, domain expertise, basic internet skills, etc.]
Basic internet skills.

**Do skills vary widely? How?**
[Explain if some workers will be better than others and why]
Some users can be more active with more access to event information. but besides that, some users will be active because they want to attend more things.

**How will you incentivize participation?**
[E.g., payment, gamification, intrinsic motivation, course credit. Be specific about your incentive design.]
Gamification, visibility for smaller businesses, gained social interactions and connections through these events.

**How much will it cost?**
[Provide rough cost estimates: $/task, $/worker, total budget needed]
Hosting / APIs may be about $100, can have some monetary incentive at first (e.g. $10 per event posted) with initial users to get thigns going. Total budget per month can be about $500.

**Where will your data come from?**
[E.g., public datasets, user-generated, scraped data, APIs, etc.]
User-generated, can also have public event listings.

**How many crowd workers do you need?**
[Estimate the scale: 10s, 100s, 1000s?]
Initially hundreds, but will likely need 100s in the future.

## Technical Approach

**What are the main steps/components in your system?**

1. User posts event
2. System saves the event along with its data
3. Shows the event realtime on a map interface

**What parts are done by the crowd vs. automated?**
[Clearly distinguish human tasks from computational tasks]
Human: uploading events
Automated: data aggregation like saving events to db and showing them in realtime

**What technologies/tools will you use?**
[E.g., Python, React, AWS, specific ML libraries, MTurk API, etc.]
Next.js, React Query, Typescript, AWS, Postgres

**How will you aggregate results from the crowd?**
[E.g., majority voting, weighted averaging, expert adjudication, ML filtering, etc.]
Show events on a map using pins, as well as upvotes and flags to see what events are more popular and trustworthy.

## Quality Control

**How will you ensure quality of crowd contributions?**
[Describe your quality control mechanisms in detail]
- Verification of users before usage of app
- Weighted trust scores based on activity and success of users
- Redudant information can be flagged and also crawled through with text similarity
- Events deleted after scheduled time

**Specific quality control methods:**
- [ ] Gold standard questions (test questions with known answers)
- [X] Majority voting across multiple workers
- [X] Expert review or verification
- [ ] Attention checks or trap questions
- [X] Reputation/qualification systems
- [X] Statistical outlier detection
- [ ] Other: [specify]

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
[Describe specific metrics or evaluation criteria]
Based on number of active users as well as user satisfaction surveys.

**What would success look like quantitatively?**
[E.g., "90% accuracy," "100 users in first week," "$X cost per task"]
100+ users in city, > 80% satisfaction, < 10% flagged events.

## Challenges & Mitigation Strategies

_For each challenge, propose a mitigation strategy:_

**Challenge 1:** Maintaining accuracy of events.
**Mitigation:** Identity verification, weighted reputation, duplicate detection.

**Challenge 2:** Sustaining crowd engagement, especially in ways that are not financial.
**Mitigation:** Gamification (badges, leaderboards, recognition), and potentially just minimize the financial output with targeted event posters.

**Challenge 3:** Scaling.
**Mitigation:** Technically-wise, would need to build the databases separately and configure the overall system architecture as such.

## Prior Work

_Are there similar projects or systems? How is yours different?_

[Describe similar work and what makes your approach unique or improved]

**Specific related projects:**
- Eventbrite: mostly paid events and feels too official
- Nextdoor: seems to focus more on neighborhoods, but people might want it for a broader city

## Discussion Notes from Round 2

**What did you agree on?**
[Key points of agreement between partners]
Different features like leaderboard to gain and sustain traction.

**What concerns or pushback emerged?**
[Questions, challenges, or areas of uncertainty discussed]
Fake events / ensuring accuracy of events.

**Why is this idea promising?**
[Explain why you chose to develop this idea over the alternative]
People, especially those who are new to the area, will be interested in finding more about the city as well as the events it has to offer.

**What makes this sustainable and feasible?**
[Specific reasons this can work within course constraints]
Events happen every day, all week, all year, so there will always be something to post about.

## Additional Notes

_Any other relevant information, inspirations, or considerations?_

[Optional: Add any additional context, ideas, or references]
Thank you!
