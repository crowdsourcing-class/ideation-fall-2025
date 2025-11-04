# Crowdsourcing Project Idea: PennPulse

## Authors

**Original Author:** Alex Oh @alexoh

**Contributor:** Shivi Jain @shivij

## Problem Statement

Penn students face significant information overload from dozens of disparate, un-curated event sources like listservs, GroupMe, digital flyers, and club newsletters. This noise makes it difficult to discover timely and relevant opportunities (e.g., guest speakers, networking events, free food). As a result, students miss valuable experiences, and event organizers struggle to reach a broad audience.

## Target Audience

All Penn students who want to find and attend campus events. PennPulse is a community-driven utility, where the act of using the app (to find events) creates the incentive to contribute (by curating), making the crowd and the user base one and the same.

## Description

PennPulse is a centralized, real-time feed of all happenings at Penn. It relies entirely on its users to submit events, curate the feed by upvoting/downvoting, and verify event details (like free food or attendance) with live "check-ins." This community-driven curation filters the noise, allowing any student to instantly see what's actually worth going to on campus right now.

## Project Type

_Select the category that best fits your project:_

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [X ] Other: self sustaining community resource

## Key Features

_List 5-8 key features or capabilities of your system. Expand from Round 1:_

1. Club leaders / approved users can post events with title, description, time, location, and tags
2. People can upvote or downvote once they go to an event
3. There are pictures to record the event and if anyone wants to see what the event will be like
4. Users can filter for tags they are looking for (speaker events, food, etc)
5. Custom notifications based on interests/academics
6. [Feature 6 - optional]
7. [Feature 7 - optional]
8. [Feature 8 - optional]

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
Volunteers are Penn students. The users of the app are the crowd.

**What will they provide?**
Content, event creation, verification, categorization

**What skills do they need?**
Must be a penn student

**Do skills vary widely? How?**
Some users may be more interested in posting their events, others may be more interested in attending opportunities 

**How will you incentivize participation?**
It is pretty self-sustaining. Club leaders are able to reach the widest audience to advertise their opportunities, and students are able to have a “one stop shop” for all things happening on campus.

**How much will it cost?**
[Provide rough cost estimates: $/task, $/worker, total budget needed]
Hopefully $0

**Where will your data come from?**
[E.g., public datasets, user-generated, scraped data, APIs, etc.]
Data will come from users to manually input events, can create a way of automatically inputting events from newsletters etc.

**How many crowd workers do you need?**
[Estimate the scale: 10s, 100s, 1000s?]
Around 100 to start

## Technical Approach

**What are the main steps/components in your system?**

Submission: A user submits an event via a form, which writes to an events table in the database.
Computation (Feed): The app front-end fetches all events and algorithmically ranks them based on a score (e.g., net_votes / (time_since_post + 2)^1.8—a Reddit-style hot ranking).
Crowd Task (Curation): Users upvote/downvote, writing to a votes table. The events table updates its net_votes score.
Crowd Task (Tagging): Users add/confirm tags, writing to a tags table linked to the event.
Computation (Filtering): The database is queried based on user-selected tags (e.g., SELECT * FROM events WHERE 'free_food' = ANY(tags)).
Crowd Task (Verification): Users at the event (location-check optional) tap "Check-In." The system increments a check_in_count.
Computation (Verification): When check_in_count > 5, the system automatically applies a "Verified" badge to that event.


**What parts are done by the crowd vs. automated?**
The crowd will allow for inputting the event as well as the rating, but the automation will come with scam detection and compiling all of the results together. In addition, the custom filtration will be automated. 

**What technologies/tools will you use?**
[E.g., Python, React, AWS, specific ML libraries, MTurk API, etc.]
React, AWS

**How will you aggregate results from the crowd?**
[E.g., majority voting, weighted averaging, expert adjudication, ML filtering, etc.]
Majority voting, qualification system (pennkey login), community flagging

## Quality Control

**How will you ensure quality of crowd contributions?**

[Describe your quality control mechanisms in detail]

**Specific quality control methods:**
- [ ] Gold standard questions (test questions with known answers)
- [X] Majority voting across multiple workers
- [ ] Expert review or verification
- [ ] Attention checks or trap questions
- [X] Reputation/qualification systems
- [X] Statistical outlier detection
- [ ] Other: [specify]

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
If students are able to go to events and find activities and events that they would not be able to find otherwise. 

**What would success look like quantitatively?**
[E.g., "90% accuracy," "100 users in first week," "$X cost per task"]

## Challenges & Mitigation Strategies

_For each challenge, propose a mitigation strategy:_

**Challenge 1:** Low initial adoption.
**Mitigation:** Partner with large orgs (e.g., PEC, AWE, SWE, Wharton Council) to cross-post their events at launch.

**Challenge 2:** Spam or false events.
**Mitigation:**Require Penn email verification, downvote filters, and automatic removal after low trust scores.

**Challenge 3:**Information overlap or duplicate posts.
**Mitigation:** NLP-based similarity detection and automatic merging of near-duplicate events.

## Prior Work

_Are there similar projects or systems? How is yours different?_

[Describe similar work and what makes your approach unique or improved]

**Specific related projects:**
- Penn Clubs:  Great for club discovery but poor for live, day-of events. PennPulse focuses on real-time, social verification.
-Sidechat: Crowdsourced but unstructured — PennPulse adds structure, verification, and filtering.

## Discussion Notes from Round 2

**What did you agree on?**
 Both agreed Penn students already act as a natural crowd.


Keep the app lightweight, with fast event submission and live filtering.


Use reputation-based incentives over monetary ones.


**What concerns or pushback emerged?**
Onboarding enough users early to make the platform self-sustaining.

**Why is this idea promising?**
It leverages existing community behavior because Penn students are already sharing events constantly. PennPulse simply centralizes and rewards it.

**What makes this sustainable and feasible?**
Once active, it’s self-sustaining through mutual benefit, students need events, organizers need attendees.

## Additional Notes

_Any other relevant information, inspirations, or considerations?_

[Optional: Add any additional context, ideas, or references]
