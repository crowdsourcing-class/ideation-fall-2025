# Crowdsourcing Project Idea: StreetEats

_Replace [Project Title] with a creative name for your project_

## Authors

**Original Author:**Braden Johnson (bradenj)

**Contributor:** Simon Roling, rolings, Jackson Gold, jgold23

## Problem Statement

Have you ever walked to your favorite food-truck just to be disappointed that it is not there? Finding food trucks can be tough due to inconsistent schedules and locations especially if the owners are not updating live on social media or something similar. Customers need an app that provides real-time crowd source updates on food truck statuses and quality reviews.

## Target Audience

Everyday people looking for a quick meal are the audience, food truck workers, and people who like certain food trucks and want to promote them can be workers.


## Description

Many people love to eat street food from food trucks. StreetEats allows people to find food trucks in their neighborhood that they may not have known about previously, and find information such as hours, locations, and menus for each truck. Crowdworkers can write reviews and post location and schedule info. Users will have a streamlined platform to find the best open food trucks near them.

## Project Type

_Select the category that best fits your project:_

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [X] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 5-8 key features or capabilities of your system. Expand from Round 1:_
1. Live, crowd updated map of food-truck locations.
2. Menu reviews with images for each truck. 
3. Ability to favorite trucks and receive notifications about them.
4. Ability to find food truck hours.
5. Ability to post reviews about new food trucks and place new trucks on the app.
6. [Feature 6 - optional]
7. [Feature 7 - optional]
8. [Feature 8 - optional]

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
Social media users, students on campuses, people who use food trucks a lot/in cities or areas with lots of food trucks

**What will they provide?**
Updates on food truck locations and schedules (live updates on if a food truck is at “normal spot” at certain time or at a specific location), menu descriptions, reviews on items

**What skills do they need?**
Basic internet skills (using an app), access to food trucks, writing/analysis skills for reviews

**Do skills vary widely? How?**
The location/schedule updating portion of the crowd sourcing is pretty skill independent-if the user sees/visits an open food truck they can update the app and the same if one is closed. There is some skill with the review portion of the app, cause while a subjective measure, the user would have to write the review.

**How will you incentivize participation?**
The core of the app relies mostly on intrinsic motivation and a small bit of gamification. We will use a reputation score to promote accurate updates and well thought-out reviews. Those with higher reputation can receive titles like verified contributor status and have their reviews highlighted. The intrinsic motivation comes from wanting to provide and see valid updates on food trucks. Likely the user would be going to the food truck either way so making the quick input in the app would become part of the experience and the user will feel like they are giving back to the community. At some point the user will likely use the app for themselves and either find a new food truck to try or avoid accidentally visiting a closed food truck. Truck owners/employees are also intrinsically motivated as this will promote business for their truck and avoid users having a bad experience by coming and it being unexpectedly closed.

**How much will it cost?**
[Provide rough cost estimates: $/task, $/worker, total budget needed]
The actual crowd work would be free, using in-app incentives in lieu of payment. Potentially, some sort of hosting costs may exist, we will estimate <100 dollars.

**Where will your data come from?**
[E.g., public datasets, user-generated, scraped data, APIs, etc.]

Our data will be entirely user generated.
**How many crowd workers do you need?**
100s

## Technical Approach

**What are the main steps/components in your system?**

1. User uploads status of truck
2. System verifies validity (sanity check)
3. System computes crown consensus or updates it
4. Food truck is verified on app

**What parts are done by the crowd vs. automated?**
Crowd: input status/hours/location of food truck
Automated: User consensus

**What technologies/tools will you use?**
AWS, React, MTurk

**How will you aggregate results from the crowd?**
Majority filtering with expert data

## Quality Control

**How will you ensure quality of crowd contributions?**

We will use gold standard questions from food truck workers. When that is not available majority voting will constitute the current status of a truck.

**Specific quality control methods:**
- [X] Gold standard questions (test questions with known answers)
- [X] Majority voting across multiple workers
- [X] Expert review or verification (truck workers)
- [X] Attention checks or trap questions
- [ ] Reputation/qualification systems
- [ ] Statistical outlier detection
- [ ] Other: [specify]

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
If the accounts of people missing their food truck decrease from a baseline survey taken before the launch of the application. 

**What would success look like quantitatively?**
1. An decrease of food truck related errors
2. The majority of the food trucks in Ucity having their status on the application

## Challenges & Mitigation Strategies

_For each challenge, propose a mitigation strategy:_

**Challenge 1:** Initial Growth
**Mitigation:**  Tabling on locust can allow for early users of our app.

**Challenge 2:** Keeping users engaged
**Mitigation:** Use in app incentives like enabling super users.

**Challenge 3:** Maintaining Accuracy
**Mitigation:** Continuous verification from users who “check-in” at local food trucks will allow an accurate platform.

## Prior Work

_Are there similar projects or systems? How is yours different?_

Google has some information about food trucks but it is not updated often and is inaccurate. Street Eats solves this with real-time user data,

**Specific related projects:**
- Yelp: It covers full restaurants and other eateries and businesses, this is focused specifically on food trucks and updates in real-time.
- Google: It has food truck info, but is often inaccurate in menu prices, locations, and hours.

## Discussion Notes from Round 2

**What did you agree on?**
The general concept and user aggregation methods

**What concerns or pushback emerged?**
The incentive methods and usage of experts (food truck workers) and the role they should play.

**Why is this idea promising?**
Users are often frustrated by food truck’s changing hours and changing locations and Street Eats solves this problem. 

**What makes this sustainable and feasible?**
Users have internal, in-game, incentives that keep them invested instead of less scalable non-monatary ones. 

## Additional Notes

_Any other relevant information, inspirations, or considerations?_
