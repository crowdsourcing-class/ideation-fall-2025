# Crowdsourcing Project Idea: Urban Explorer

## Authors

**Original Author:** Katherine Yue (kyue)

**Round 2 Contributors:** Katherine Yue (kyue), James Doh (dohj0109), Omar Pareja (pareja)

**Round 3 Contributors:** Katherine Yue (kyue), James Doh (dohj0109), Omar Pareja (pareja), Eric Lee (ericclee), Mario Valek (mvalek)

## Problem Statement

[In 2-3 sentences, describe the problem your project will solve. What pain point or challenge are you addressing?]
With city events scattered across multiple platforms, it can be hard for residents to discover what's happening nearby (e.g. open mic nights, volunteer drives, etc). On the other side, many local or spontaneous events go unnoticed because there's a lack of a centralized, up-to-date platform that showcases these events.


## Target Audience

**End Users:** [Who will use/benefit from the system?]
Not only the residents, but people who are visiting the city, small businesses advertising their events, and others who want to discover or promote nearby happenings.

**Crowd Workers:** [Who will contribute to the crowdsourcing tasks?]
Anyone who is hosting events or those who want to vote on events, as well as volunteers who are ensuring accuracy.

**Stakeholders:** [Who else is affected or interested in this project?]
​​Small businesses, city event coordinators, and local governments interested in improving community engagement.


## Description

[Provide a comprehensive description of your crowdsourcing project. What will the system do? How will it work? What value does it provide?]
Urban Explorer is a crowdsourced event discovery platform that visualizes real-time events and gatherings across the city through an interactive map interface. Users are able to post events, upvote postings, and flag inappropriate events. We want to ensure that contents are fresh through expiration and verification processes.

## Project Type

_Select the primary category:_

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [x] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 8-10 key features or capabilities of your system:_

1. Interactive map - displays all events in a map interface 
2. Posting feature - allows users to upload events  
3. Verification system - ensures users verify their identity before doing anything  
4. Notification system - notifies users of events within a certain radius  
5. Engagement leaderboard - leaderboard for posting or attending events/having popular events  
6. Auto-expiration - removes expired events automatically
7. Flagging system - enables users to report fake events
8. Trust score - weights user input based on their history of accurate events

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
[E.g., MTurk, volunteers, social media users, students, etc. Be very specific about recruitment strategy.]
Primarily volunteers and social media users who want to stay informed or promote local events

**What will they provide?**
[E.g., labels, votes, creative content, transcriptions, etc. Detail the exact contributions.]
Event listings, verification votes, and flags for outdated/inaccurate postings

**What skills do they need?**
[E.g., bilingual, domain expertise, basic internet skills, etc.]
Basic internet and smartphone skills

**Do skills vary widely? How?**
[Explain variance in worker abilities and how you'll account for it]
Some users may have access to exclusive or insider event information (like small business owners or event organizers), while others participate casually to find things to do

**How will you incentivize participation?**
[Detailed incentive design. Consider multiple incentive types and their effectiveness.]
For daily users, there would be leaderboards and badges (gamification) the more the best and the more their events are upvoted. Furthermore, small businesses can gain visibility through this platform, and larger city organizations can foster more community involvement through this.

**Budget & Cost Analysis:**
- Estimated cost per task: for initial paid event postings, ~$1 for each post – with more people, this cost will no longer be necessary.
- Estimated cost per worker: ~$15, as the work isn’t constant and tied to how many event posts.
- Number of tasks needed: ~50-100 initial posts.
- Total estimated budget: ~$500 / month
- Justification: Besides cost for tasks and workers, which are mainly early-user incentives, this would cover hosting database servers and API services.

**Where will your data come from?**
[E.g., public datasets, user-generated, scraped data, APIs. Include specific sources.]
At first, it will come from paid sources (people who search for event postings and such), but later on it will become user-generated submissions, scraped public listings, and potentially other avenues with event aggregators (e.g. ticketmaster).

**Scale Requirements:**
- Minimum viable crowd size: 100 users, 10 workers (assuming 1:10 ratio of posters & attendees)
- Target crowd size for full functionality: 500+, even better if 1000+
- Potential to scale to: 1000s, if not tens of thousands

## Technical Architecture

**System Components:**

1. Frontend: react native
2. Backend: node.js
3. Database: postgresql
4. Libraries: tanstack query, prisma orm
5. Infra: AWS (RDS, EC2)

**Detailed Workflow:**

_Step-by-step description of how the system works:_

1. User posts an event
2. Both client/server side form validation
3. Data gets persisted to DB
4. User goes to the events page
5. Makes a query to fetch a list of events
6. User keeps scrolling
7. Keep making more request to receive more events (infinite scroll)

**Human vs. Automated Tasks:**

| Task | Performed By | Why? |
|------|--------------|------|
| [Posting Events] | Human | [Requires human knowledge of real events] |
| [Verifying Events] | Human | [Human judgment ensures trustworthiness] |
| [Displaying map data] | Automated | [Computation-heavy and dynamic] |
| [Event expiration] | Automated | [Ensures data freshness without manual input] |

**Technologies & Tools:**
- Frontend: Next.js, React Query, TypeScript
- Backend: Node.js, Express
- Database: PostgreSQL
- ML/AI: Text similarity detection for duplicate events
- Crowdsourcing Platform: Custom web app
- Hosting: AWS / Vercel

**Aggregation Method:**
[Describe in detail how you will combine multiple crowd contributions. E.g., majority voting, weighted averaging, expectation-maximization, expert adjudication, ML-based filtering, etc.]
Combining upvotes, verification scores, as well as potentially volunteers’ trust scores, events are ranked by a score that weighs all these different factors. We could also implement ML-based filtering to both recommend certain events, as well as flag any suspicious ones (e.g. text similarity). Events that are flagged or noted to be duplicated are then deprioritized.

## Quality Control

**Quality Control Strategy:**
[Comprehensive description of your QC approach and why it's appropriate for your project]

**Specific QC Mechanisms:**
- [ ] Gold standard questions (test questions with known answers)
 - _Details: [How many? How distributed? What happens if workers fail?]_
- [X] Majority voting across multiple workers
 - _Details:_ Each event submission must be confirmed by at least 3 independent users before being marked as “verified” (though it could be visible at first, just unverified). If two or more users upvote the same event and no one flags it, it passes verification. In the case of a tie (equal votes and flags), the event remains in an unverified / pending state until additional input is received.  
- [X] Expert review or verification
 - _Details:_ A small group of trusted users, who are selected based on prior contribution quality and verified identity, will review approximately 10% - 15% of total events weekly. These experts focus on events with conflicting votes, repeated flags, or unusually high engagement to ensure fairness and consistency.  
- [ ] Attention checks or trap questions
 - _Details: [What types? How often? Consequences?]_
- [X] Reputation/qualification systems
 - _Details:_ Each user begins with a neutral trust score that increases as their posts are confirmed or upvoted and decreases when their events are flagged or removed. Users who maintain a high trust score gain perks such as auto-verification priority and moderation abilities, as well as visibility on leaderboards and with badges. This system incentivizes accurate participation and builds a self-regulating community.  
- [X] Statistical outlier detection
 - _Details:_ Automated scripts flag anomalies such as users posting an unusually high number of events per day, duplicate content, or geographically inconsistent listings. Outlier detection uses metrics like posting frequency, location variance, and similarity scores to identify possible spam or automated behavior. Flagged accounts or posts are temporarily suspended for manual review.  
- [ ] Redundancy and agreement metrics
 - _Details: [How much redundancy? What agreement threshold?]_
- [ ] Other: [specify]
 - _Details: [Explain custom QC approaches]_

**Handling Low-Quality Work:**
[What happens when quality issues are detected? Rejection? Re-tasking? Worker penalties?]
Flagged or low-confidence events are re-evaluated by trusted users. Repeated offenders lose posting privileges or reputation points.

## Evaluation & Success Metrics

**Primary Success Metrics:**

1. User engagement rate – measured by posts and verifications per week.
2. Event accuracy – % of verified vs. flagged events (target: < 10% flagged).
3. User satisfaction – survey rating >= 80%.

**Evaluation Methodology:**

[Describe how you will evaluate your project. What experiments will you run? What data will you collect? How will you analyze it?]
Collect analytics on app engagement, flag frequency, and trust score distribution. Conduct occasional surveys to assess satisfaction and user experience.

**Baseline Comparisons:**
- [What baseline will you compare against?]
- [How will you measure improvement over baseline?]
Compare to Eventbrite and Nextdoor in terms of event freshness, accuracy, and engagement. Measure improvement through retention and daily active user growth.

**Success Criteria:**
- Minimum viable success: 100 weekly active users
- Target success: 500 weekly active users with <10% flagged events 
- Stretch success: 1000+ active users per city

## Challenges & Mitigation Strategies

**Challenge 1:** Data Quality and Spam Events
- **Why it's a risk:** Malicious users or businesses could post fake events, duplicate listings, or spam, which would degrade user trust and make the platform unreliable. Without quality control, the map becomes useless.
- **Mitigation strategy:** Implement a multi-layered verification system:
Automated filtering for obvious spam keywords.
User flagging system to allow the community to report suspicious posts
Trust Score for users, where accurate event postings increase a user's score, giving their future posts higher visibility.
Captcha or phone verification for new accounts to deter bots
- **Backup plan:** If automated systems fail, appoint a small team of volunteer moderators from the most trusted users (those with high reputation scores) to manually review flagged content.

**Challenge 2:**  The Cold Start Problem 
- **Why it's a risk:** A new event platform is useless if it's empty. Without a critical mass of events and users at launch, new users will see no value, leave, and never return, preventing the platform from growing.
- **Mitigation strategy:** Proactively seed the platform with data before public launch:
Scrape and import event data from public APIs (Facebook Events, Meetup, or city government calendars) to create an initial base of content.
Partner with local organizations (university clubs, libraries, community centers) to encourage them to be early adopters and post their events.
Run a targeted launch campaign in a small, dense geographic area (a university campus) to achieve density quickly.
- **Backup plan:** If organic growth is too slow, use gamified onboarding process that requires new users to vote on or verify a few existing events before they can post, simultaneously building the community and teaching them the platform

**Challenge 3:** User Privacy and Safety
- **Why it's a risk:** Displaying event locations on a public map raises safety concerns. Users might be wary of sharing their location or attending events posted by strangers, limiting participation.
- **Mitigation strategy:** Build privacy and safety into the core design:
Allow event creators to show only an approximate neighbourhood or venue name instead of a precise pin. 
Implement a badge system to distinguish between "Public," "Club/Group," and "Private" events.
Prominently display community guidelines and safety tips for attending events. 
- **Backup plan:** For high-risk or frequently flagged event categories, implement a mandatory host verification process (e.g., linking a social media profile) before such events can be published.

**Challenge 4:** Sustaining Long-Term Engagement  
- **Why it's a risk:** Users might download the app, use it once, and forget about it. Without recurring engagement, the crowd stagnates, events become outdated, and the platform dies.
- **Mitigation strategy:** Use proven engagement loops and incentives:
Push notifications for new events in a user's area of interest or from hosts they follow.
Use gamification, e.g. an "Explorer Level" or badge system that rewards users for posting events, verifying listings, and attending gatherings. 
- **Backup plan:** If natural engagement drops, introduce periodic challenges or themes with small, tangible rewards for participation to re-ignite activity.


## Prior Work & Related Projects

**Similar Existing Systems:**

1. **Eventbrite**  
   - Description: Centralized platform for paid and official events.  
   - Similarities: Event listings and user submissions.  
   - Differences: Urban Explorer focuses on spontaneous, local, and free events.  

2. **Nextdoor**  
   - Description: Neighborhood-focused social platform.  
   - Similarities: Community interaction and local engagement.  
   - Differences: Urban Explorer offers real-time event mapping and gamification.  

**Lessons from Past Course Projects:**
[What did you learn from reviewing past NETS 2130 projects? What will you do differently?]
Past projects often struggled with sustained engagement. We plan to address this through strong incentive design (badges, leaderboards) and real-time feedback loops.

## Ethical Considerations

**Potential Ethical Issues:**
- Privacy concerns from event location sharing  
- Fair treatment and moderation of user content  
- Risk of misinformation or spam events  

**Mitigation Strategies:**
- Limit location accuracy to approximate radius  
- Clear reporting and moderation system  
- Enforce community guidelines and user accountability 

**IRB Considerations:**
[Will this project require IRB approval? Why or why not?]
Unlikely to require IRB approval since no sensitive personal data or experimental manipulation is involved.

## Business Viability (Optional)

_If your project has business potential, consider:_

**Revenue Model:**
[How could this make money?]
Freemium model: base access is free, while promoted events or analytics dashboards for businesses incur a fee.

**Market Size:**
[Who would pay for this? How many potential customers?]
Local event organizers, small businesses, and city tourism boards. High potential across mid-to-large cities.

**Competitive Advantage:**
[Why would people choose your solution?]
Real-time map interface, community-driven validation, and gamified participation create a unique, sustainable edge.

**Sustainability:**
[Can this continue after the course ends?]
Once the user base reaches critical mass, the system becomes self-sustaining through user participation and business incentives.

## Steel-Man Discussion (Round 3)

**Idea A Steel-Man:**
[How the group built up the first idea to its strongest possible form]
Focused on hyperlocal event posting verified by residents for trust and immediacy

**Idea B Steel-Man:**
[How the group built up the second idea to its strongest possible form]
Proposed gamified city exploration, but lacked strong verification and sustainability

**Why We Chose This Idea:**
[Explain why this idea (after steel-manning) was the most convincing. Focus on feasibility, sustainability, and realistic implementation.]
It balances practicality and engagement—real-world value for users, feasible technical design, and natural scalability

**What We Agreed On:**
[Key points of consensus among all four group members]
Interactive map, reputation-based trust system, and gamified engagement features

**What Concerns Emerged:**
[Remaining questions, challenges, or areas needing more thought]
Ensuring event authenticity and continuous user engagement post-launch

**Key Insights from Round 3 Discussion:**
[What did you learn from the group discussion that improved the idea?]
Combining verification systems with gamification yields both quality control and sustained participation

## Implementation Timeline (Optional)

_If you were to build this, what would the timeline look like?_

**Week 1-2:** Ideation, wireframes, and technical setup (Next.js, database schema)  
**Week 3-4:** Implement core posting and event map features  
**Week 5-6:** Add verification, trust score, and gamification systems  
**Week 7-8:** Launch MVP and evaluate with small user group

## Additional Notes

_Any other relevant information, inspirations, or considerations?_

[Optional: Add any additional context, ideas, or references]

## References & Inspiration

_Include any references, papers, articles, or sources that inspired or informed this project idea:_

1. [Reference 1]
2. [Reference 2]
3. [Reference 3]