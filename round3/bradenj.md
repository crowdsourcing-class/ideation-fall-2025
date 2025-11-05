# Crowdsourcing Project Idea: StreetEats


## Authors


**Original Author:** Braden Johnson (bradenj)


**Round 2 Contributors:** Simon Roling (rolings), Jackson Gold (jgold23)


**Round 3 Contributors:** Braden Johnson (bradenj), Simon Roling (rolings), Jackson Gold (jgold23), Eitan Gotian (egotian), Kieran Chetty (chettyk)


## Problem Statement


Have you ever walked to your favorite food-truck just to be disappointed that it is not there? Finding food trucks can be tough due to inconsistent schedules and locations especially if the owners are not updating live on social media or something similar. Customers need an app that provides real-time crowd source updates on food truck statuses and quality reviews.


## Target Audience


**End Users:** Everyday people looking for a quick meal, food-truck goers or people who live in areas with lots of them (cities), students on campuses.


**Crowd Workers:** Social media users, students, food truck customers, and truck owners/employees.


**Stakeholders:** Food truck owners/operators, local communities, students, and potential advertisers.


## Description


Many people love to eat street food from food trucks. StreetEats allows people to find food trucks in their neighborhood that they may not have known about previously, and find information such as hours, locations, and menus for each truck. Crowdworkers can write reviews and post location and schedule info. Users will have a streamlined platform to find the best open food trucks near them.


## Project Type


_Select the primary category:_


- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [x] Business idea using crowdsourcing
- [ ] Other: [specify]


## Key Features


_List 8-10 key features or capabilities of your system:_


1. Live, crowd updated map of food-truck locations.
2. Menu reviews with images for each truck.
3. Ability to favorite trucks and receive notifications about them.
4. Ability to find food truck hours.
5. Ability to post reviews about new food trucks and place new trucks on the app.
6. Simple check-in to confirm a truck’s presence (photo/geo optional).
7. Reputation system that highlights accurate contributors and trusted owners.
8. Filters (cuisine, price, distance, dietary tags) and map/list views.
9. Owner portal to verify updates and post official announcements.


## Feasibility: Crowd & Resources


**Where will your crowd workers come from?**
Students on campuses, city residents, and truck owners’ customer bases. Recruitment via campus tabling, QR codes at trucks, local forums, and truck-owner partnerships.


**What will they provide?**
Real-time status/location confirmations, hours updates, new truck submissions, menus/photos, and item-level reviews.


**What skills do they need?**
Basic internet skills (using an app), access to food trucks, writing/analysis skills for reviews.


**Do skills vary widely? How?**
The location/schedule updating portion of the crowd sourcing is pretty skill independent-if the user sees/visits an open food truck they can update the app and the same if one is closed. There is some skill with the review portion of the app, cause while a subjective measure, the user would have to write the review.


**How will you incentivize participation?**
The core of the app relies mostly on intrinsic motivation and a small bit of gamification. We will use a reputation score to promote accurate updates and well thought-out reviews. Those with higher reputation can receive titles like verified contributor status and have their reviews highlighted. The intrinsic motivation comes from wanting to provide and see valid updates on food trucks. Likely the user would be going to the food truck either way so making the quick input in the app would become part of the experience and the user will feel like they are giving back to the community. At some point the user will likely use the app for themselves and either find a new food truck to try or avoid accidentally visiting a closed food truck. Truck owners/employees are also intrinsically motivated as this will promote business for their truck and avoid users having a bad experience by coming and it being unexpectedly closed.


**Budget & Cost Analysis:**
- Estimated cost per task: $0.00
- Estimated cost per worker: $0.00
- Number of tasks needed: ~2,000 (could vary on area/food-truck popularity when scaling)
- Total estimated budget: ~$100
- Justification: Leverages volunteer updates and owner participation, food trucks are extremely popular on campus and with students


**Where will your data come from?**
Our data will essentially be entirely user generated. Using the crowd (students, food-truck goers) for most updates and also offering owner-verified updates. We could potentially pull initial data from a service like Google Maps or Yelp to have a base that is then built off of using the crowd updates.


**Scale Requirements:**
- Minimum viable crowd size: ~50 active local contributors
- Target crowd size for full functionality: ~300 steady contributors
- Potential to scale to: 1,000+ contributors across multiple cities


## Technical Architecture


**System Components:**


1. Frontend web interface (React) with map and list views
2. Backend API (Node.js/Express on AWS)
3. Database (PostgreSQL on AWS RDS)
4. External APIs (Google Maps)


**Detailed Workflow:**


_Step-by-step description of how the system works:_


1. User reports: "Truck X is open in Ludlow until 3:30" or checks-in to confirm.
2. System performs sanity checks (geo proximity to past locations, duplicate detection).
3. Multiple crowd workers independently confirm/deny, owners can verify officially.
4. Aggregation applies weighted majority voting (reputation, owner weight).
5. Database updates truck status, map and list views refresh in near real time.
6. Users who favorited the truck receive notifications, reviews/photos attach to the truck page.


**Human vs. Automated Tasks:**
Report/confirm truck presence: Human, Requires on-the-ground observation
Owner verification, Human (owner), Provides authority
Aggregation weighting: Automated Consistent, fast, unbiased combination




**Technologies & Tools:**
Frontend: React
Backend: Node.js/Express, REST API
Database: PostgreSQL (RDS)
Crowdsourcing Platform: Native app flows, optional MTurk for initial seeding
Hosting: AWS


**Aggregation Method:**
Weighted majority voting with time sensitivity and contributor reputation. Conflicting requests will wait before updating. Owner-verified updates receive higher weight and will be published. Confidence scores determine whether to publish immediately or await additional votes.


## Quality Control


**Quality Control Strategy:**
We will use owner-verified updates as close to the “gold-standard”. For other user updates, we will utilize the users reputation score combined with other similar updates coming in to verify before publishing (i.e. developing a confidence score before updating the status). If we receive conflicting updates this will have a negative impact on the confidence score. Time will also need to be considered in the quality control as we will want our updates to be live.


**Specific QC Mechanisms:**
- [x] Gold standard questions
 - _Details: We will use owner-verified updates as the gold standard. If their our know truck hours, we will use this as our base and then change based on updates._
- [x] Majority voting across multiple workers
 - _Details: Reputation and time-weighted updates from the crowd. Will need to achieve certain confidence score (goes down with conflicting updates/with time)._
- [x] Expert review or verification
 - _Details: Owner-verified updates will carry significant weight and potentially even override._
- [x] Attention checks or trap questions
 - _Details: Occasional on-page checks (verifying truck color/signage and menu)._
- [x] Reputation/qualification systems
 - _Details: Users will have a reputation score that goes up as they make accurate updates over time. For the review portion, while a subjective feature, users can upvote reviews they think are good contributing to the score._
- [x] Statistical outlier detection
 - _Details: Flag users making updates at unlikely times based on typical schedules like a breakfast truck open at 10 pm or a menu addition without verification._
- [x] Redundancy and agreement metrics
 - _Details: This will tie in with the confidence score, if a truck is receiving similar updates from multiple users (agreement) then it will lead to a higher confidence score and update in our app._


**Handling Low-Quality Work:**
This is where we utilize the confidence score for updating itself. If a truck is receiving conflicting updates then we will wait to publish. If a user is consistently making incorrect updates or random wrong posts, they’re reputation will go down. This could lead to lost privileges like inability to review or attempt to update the status/menu for a truck.


## Evaluation & Success Metrics


**Primary Success Metrics:**
1. Number of Trucks: 25
2. Number of Verified Users: 100
3. Number of Verified Truck Partnerships: 3


**Evaluation Methodology:**
We will collect the number of trucks, the number of users, and the number of total reports (user inputs). We will also evaluate the success rates of each user.


**Baseline Comparisons:**
- Compare against Yelp/google maps
- [How will you measure improvement over baseline?]: # of realtime updates on food trucks in UCITY.


**Success Criteria:**
- Minimum viable success: 1 Trucks and 10 users
- Target success: 25 trucks and 100 users
- Stretch success: All trucks in Ucity and 1000 users




- 
## Challenges & Mitigation Strategies


**Challenge 1:** Initial growth and cold-start on Penn’s campus/University City
**Why it's a risk:** Without early data, the app feels empty and untrustworthy.
**Mitigation strategy:** Campus tabling, QR codes at trucks.
**Backup plan:** partner with 10–20 truck owners to seed data.


**Challenge 2:** Sustaining contributor engagement
**Why it's a risk:** Drop-off reduces data freshness and coverage.
**Mitigation strategy:** Visible reputation, badges, leaderboards, weekly highlights, personalized notifications.
**Backup plan:** Use some sort of raffle for free food to keep people engaged… sponsored by trucks we partner with.


**Challenge 3:** Maintaining accuracy against noisy/conflicting reports
- **Why it's a risk:** Misinformation erodes trust.
- **Mitigation strategy:** weighted voting, owner weighting, flagging bad users
- **Backup plan:** Local moderators, owner overrides.


**Challenge 4:** Data sparsity in low-density areas
- **Why it's a risk:** Infrequent updates lead to stale statuses.
- **Mitigation strategy:** Partner with local community groups to raise awareness.
- **Backup plan:** targeted advertising to these communities.


## Prior Work & Related Projects


**Similar Existing Systems:**


1. **Yelp**
  - Description: Reviews and business listings for restaurants.
  - Similarities: Reviews, photos, basic hours, maps.
  - Differences: Not truck-specific, slower updates for pop-ups and mobile vendors.
  - Citation/Link: https://www.yelp.com/


2. **Google Maps business profiles**
  - Description: Maps + business info with community edits.
  - Similarities: Community updates, hours, photos, maps.
  - Differences: Limited real-time truck coverage and reliability for mobile vendors.
  - Citation/Link: https://www.google.com/maps


3. **Social media (Instagram/Twitter) posts**
  - Description: Owners announce specials and locations.
  - Similarities: Timely updates from owners.
  - Differences: Scattered, hard to aggregate/search, no structured reliability.
  - Citation/Link: https://www.instagram.com/


**Lessons from Past Course Projects:**
The main flaw we saw with last year's projects was unrealistic scope: Some projects did not have a robust enough dataset to provide the service that they wanted to, we fix this by allowing humans to continuously make the platform better by leaving reviews and other information.


## Ethical Considerations


**Potential Ethical Issues:**
- Privacy concerns with location and live updates
- Misuse via false reports or harassment of owners
- Review bombing of food trucks


**Mitigation Strategies:**
- Anonymize contributor data
- Issues 2 and 3 will rely on strong moderation within the app


**IRB Considerations:**
We likely will not need an internal review board.


## Business Viability (Optional)


_If your project has business potential, consider:_


**Revenue Model:**
Local ads and partnerships with truck, premium owner features and verifications. Affiliate deals with delivery partners.


**Market Size:**
Major and minor cities with active truck scenes, there are tens of thousands of potential users and thousands of active trucks.


**Competitive Advantage:**
Real-time, crowd-verified data specialized for trucks, easy and definitive user reliability rating, notifications tuned to mobility.


**Sustainability:**
Low initial costs, community-driven incentives, no financial barrier. 
## Steel-Man Discussion (Round 3)


**Idea A Steel-Man (StreetEats):**
Area-by-area rollout (focusing on Penn’s campus/University City first), owner partnerships at launch, reputation-weighted voting, live map updates, notifications on favorite food trucks, and an owner portal.


**Idea B Steel-Man (City Sidewalk Idea):**
Low costs, community-driven to help others would entice users to sign up, appealing to the octalysis framework.


**Why We Chose This Idea:**
StreetEats has clearer stakeholder incentives (owners + hungry users), daily repeat use cases, and a data schema on the simpler side. It’s feasible with student-scale resources and sustainable via community momentum.


**What We Agreed On:**
Start with one neighborhood (Penn/University City), prioritize quick-confirm actions, owner verification will be a valuable source.
**What Concerns Emerged:**
Getting initial Golden Standard data without owners, maintaining freshness off-hours (needing users to visit to get live updates), false positives at large events.


**Key Insights from Round 3 Discussion:**
User reputation weighting handles most conflicts. Owner partnerships at launch dramatically reduce perceived risk and accelerate trust and user verifiability. Getting initial data and user base will be initial bottle neck but discussed potential solutions to this as outlined above. After that, ensuring user engagement will be the next issue but we will utilize the reputation score and the intrinsic value of seeing the schedule and menu updates as reasons to return to StreetEats.


## Implementation Timeline (Optional)


_If you were to build this, what would the timeline look like?_


**Week 1-2:** [Phase 1 tasks]
**Week 3-4:** [Phase 2 tasks]
**Week 5-6:** [Phase 3 tasks]
**Week 7-8:** [Phase 4 tasks]


## Additional Notes


_Any other relevant information, inspirations, or considerations?_


[Optional: Add any additional context, ideas, or references]


## References & Inspiration


_Include any references, papers, articles, or sources that inspired or informed this project idea:_




