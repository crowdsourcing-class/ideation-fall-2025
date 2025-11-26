# Crowdsourcing Project Idea: TerraTruth

_Replace [Project Title] with a creative name for your project_

## Authors

**Original Author:** Alexander Mehta (amehta26)

**Contributor:** Brandon Yan (bdonyan)

## Problem Statement

Non-profits, humanitarian organizations, and news agencies lack the manpower to effectively analyze the vast amount of satellite imagery available for tracking critical events like humanitarian crises, environmental disasters, and conflicts. This analysis bottleneck delays real-time awareness and hinders effective response. TerraTruth solves this by creating a dedicated, scalable workforce of volunteers to perform this vital, time-sensitive analysis.

## Target Audience

* **Requesters (Partners):** Non-profit organizations (e.g., Amnesty International, Greenpeace), humanitarian aid groups (e.g., Doctors Without Borders), academic researchers, and journalists who need timely analysis of satellite data.
* **Crowd Workers (Analysts):** Volunteers who are passionate about specific global issues (e.g., conservation, human rights, disaster response) and want to contribute their analytical skills to a meaningful cause.

## Description

TerraTruth is a web-based crowdsourcing platform that connects non-profit organizations with a global pool of trained volunteers. Volunteers select "missions" aligned with causes they care about (e.g., "Estimate deforestation in the Amazon," "Identify damaged infrastructure in a conflict zone"). The platform guides them through analyzing satellite imagery, and their combined inputs are aggregated into verified reports that are provided directly to partner organizations to drive awareness and action.

## Project Type

_Select the category that best fits your project:_

- [X] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 5-8 key features or capabilities of your system. Expand from Round 1:_

1.  **Mission-Based Cause Selection:** Users can browse and join analysis "missions" sponsored by partner non-profits, filtered by cause (e.g., Humanitarian, Environmental, Conflict).
2.  **Reputation & Skill System:** Workers earn accuracy scores and badges based on their performance against gold-standard data, unlocking more complex tasks as their skill is proven.
3.  **Weighted Aggregation Engine:** Responses are aggregated using a weighted average based on the analyst's proven accuracy score, improving reliability and weeding out low-quality data.
4.  **Impact Visibility Dashboard:** A dedicated section showing real-time contribution statistics and publishing updates from non-profits on how the data was used (e.g., "Your analysis was featured in this report...").
5.  **Sensitive Content Filtering:** Users can opt-out of viewing potentially graphic or disturbing imagery, ensuring a safe and comfortable volunteer experience.
6.  **Progressive Training Module:** New users are guided through tutorials and "training missions" with known answers to build their skills before working on live, unverified data.
7.  **Partner Data Portal:** Verified and aggregated data (e.g., counts, affected area polygons, key findings) is made available to partner organizations via a secure API or data export dashboard.

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
Primarily **volunteers** recruited through partner non-profits, university groups, social media campaigns (targeting users interested in humanitarian/environmental causes), and online volunteer portals.

**What will they provide?**
Image annotations (e.g., bounding boxes), object counts (e.g., buildings, vehicles, tents), damage assessments, and land-use classifications (e.g., "deforested," "flooded," "new construction").

**What skills do they need?**
Basic visual pattern recognition and computer literacy. No domain expertise is required for entry-level tasks, as the platform will provide task-specific training.

**Do skills vary widely? How?**
Yes. Some users will naturally be better at
spotting subtle details or more consistent in their counting. Skill will be measured by their accuracy against "gold standard" images, and this will form their reputation score.

**How will you incentivize participation?**
Primarily **intrinsic motivation** (contributing to a cause they believe in). This is supported by:
1.  **Gamification:** Earning badges for achievements, rising on leaderboards, and "leveling up" to unlock harder tasks.
2.  **Impact Visibility:** Regularly showing users how their specific contributions were used by partner organizations.
3.  **Community:** Building a community forum where users can discuss missions and feel part of a team.

**How much will it cost?**
The primary cost is server hosting and platform maintenance (e.g., AWS/GCP). We will operate as a non-profit, funded by grants, donations, or corporate sponsorships. Worker cost is **$0** (volunteers). Imagery will be sourced for **free** via non-profit agreements with providers (like Planet Labs, Maxar) or by using public data (e.g., Sentinel, Landsat).

**Where will your data come from?**
Live satellite imagery feeds and archival data provided by our partner organizations (Amnesty International, etc.) and imagery providers (Planet Labs) under non-profit/humanitarian licenses.

**How many crowd workers do you need?**
To provide meaningful, rapid analysis for multiple "missions," a core group of **100s** of active workers would be needed, with a total user base in the **1000s** to ensure coverage.

## Technical Approach

**What are the main steps/components in your system?**

1.  **Mission Creation:** A partner non-profit defines a task (e.g., "Count destroyed buildings in City X") and uploads a set of satellite images via a secure portal.
2.  **Task Queuing:** The system ingests the images, segments them into individual tasks, and identifies any "gold standard" images (with pre-verified answers) to be mixed in for quality control.
3.  **Task Distribution:** A volunteer logs in, selects the mission, and is served an image from the queue via a simple analysis interface (e.g., "Click on each damaged building").
4.  **Response Collection:** The user's analysis (e.g., coordinates of clicks, count) is submitted to the database, and their performance on any gold-standard tasks is recorded.
5.  **Weighted Aggregation:** The system routes the same image to 3-5 different users. Once all responses are in, it calculates a final, aggregated result for the image (e.g., "Mean count: 12.5," weighted by user accuracy scores).
6.  **Report Generation:** Once all images in a mission are analyzed, a summary report and data export are generated and made available to the partner non-profit.

**What parts are done by the crowd vs. automated?**
* **Human Tasks (Crowd):** The core analysis—identifying objects, assessing damage, classifying land use, and other complex visual interpretations that AI struggles with.
* **Automated Tasks (System):** User management, reputation scoring, task distribution (queuing), serving images, collecting responses, running quality control checks, aggregating data (weighted averaging), and generating final reports.

**What technologies/tools will you use?**
* **Frontend:** React (for a dynamic, responsive analysis interface).
* **Backend:** Python (Django or Flask) for the API, user management, and aggregation logic.
* **Database:** PostgreSQL (with PostGIS extension for handling geographic data/coordinates).
* **Hosting:** AWS (e.g., EC2 for servers, S3 for image storage, RDS for database) or a similar cloud provider.

**How will you aggregate results from the crowd?**
We will use a **weighted average** (for numerical tasks like counting) or **weighted majority vote** (for classification tasks). Each user's vote/input is weighted by their historical accuracy score, which is continuously updated based on their performance on gold standard questions.

## Quality Control

**How will you ensure quality of crowd contributions?**

Our primary method is a reputation system built on performance. High-accuracy users have their contributions weighted more heavily. Low-accuracy or malicious users will have their contributions down-weighted or discarded. We will require a new user to pass a "training mission" before they can contribute to live data.

**Specific quality control methods:**
- [X] **Gold standard questions (test questions with known answers):** This is the core of our QC. A subset of tasks will have known answers, set by expert admins or trusted users.
- [X] **Majority voting across multiple workers:** Every image will be shown to *n* (e.g., 3-5) different users to allow for aggregation and outlier detection.
- [ ] Expert review or verification (Too resource-intensive, *except* for setting the initial gold standards).
- [ ] Attention checks or trap questions (This is a form of gold standard).
- [X] **Reputation/qualification systems:** Users will be ranked (e.g., "Recruit," "Analyst," "Expert") based on their accuracy, and this rank will determine the weight of their contributions and their access to more complex tasks.
- [X] **Statistical outlier detection:** Automatically flag responses that are far from the weighted mean for manual review or to be discarded.

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
Success is measured by (1) the accuracy of the aggregated data, (2) the level of volunteer engagement, and (3) the tangible impact reported by partner non-profits.

**What would success look like quantitatively?**
* **Accuracy:** >95% aggregated accuracy on gold standard tasks.
* **Engagement:** >500 active monthly volunteers within the first year.
* **Throughput:** >10,000 images analyzed per month.
* **Impact:** At least 3 partner non-profits (e.g., Amnesty, Human Rights Watch) publicly citing data from TerraTruth in their reports or advocacy work.

## Challenges & Mitigation Strategies

_For each challenge, propose a mitigation strategy:_

**Challenge 1:** Sourcing consistent, high-quality, and *timely* satellite imagery for free.
**Mitigation:** Start by focusing on publicly available data (e.g., Sentinel, Landsat) to build the platform and user base. Use this demonstrated capability and user-base size to then secure formal partnerships with providers like Planet Labs and Maxar for their non-profit/humanitarian data streams.

**Challenge 2:** Maintaining volunteer engagement and preventing burnout, especially for difficult tasks.
**Mitigation:** Implement strong gamification (badges, levels) and a best-in-class "Impact Dashboard." We must work *very* closely with non-profit partners to get regular, tangible updates and human stories to share with the volunteers to close the feedback loop.

**Challenge 3:** Ensuring data accuracy from untrained volunteers for complex analysis (e.g., "is this building damaged by conflict or just under construction?").
**Mitigation:** Use a **progressive task model**. New users *must* pass simple "training" missions (e.g., "find all the cars"). As their accuracy score improves, they "unlock" more complex tasks, ensuring difficult analysis is only done by proven, high-skill users.

## Prior Work

_Are there similar projects or systems? How is yours different?_

Our system is inspired by past successes in citizen science and digital volunteering but fills a specific niche.

**Specific related projects:**
-   **Zooniverse:** This is the most similar model (volunteer-based analysis for science). TerraTruth is different because it is not focused on general academic science (like galaxy classification) but specifically on **time-sensitive humanitarian and environmental action**. Our "why" is activism and real-time awareness, not just scientific discovery.
-   **Amnesty International's "Decoders" Program:** This was a past project that successfully used volunteers to analyze images from Sudan. TerraTruth aims to be a *permanent, scalable platform* that serves *multiple* organizations, rather than a single, short-term campaign run by one NGO. We are building the *tool* for all of them.
-   **DataLabeler :** This is focused on training machine learning models. They are similar in task (image annotation), but differ entirely in their *goal* and *incentive*. TerraTruth is driven by intrinsic motivation and a non-profit mission.

## Discussion Notes from Round 2

**What did you agree on?**
We agreed on the fact that we need a task that can have a real impact and that is exciting to both of us.

**What concerns or pushback emerged?**
We were a bit worried about sourcing the images as well as how you deal with hard situations like when there are depictions of violence in the satelite imagery.

**Why is this idea promising?**
Because we feel that it has a broader use case and greater potential over all. The alternative focused on keeping track of lines at Penn but we feel users would be unlikely to open a new website just to help others know how long lines are etc.

**What makes this sustainable and feasible?**
The technology required is feasible and there are options for imagery that dont involve a license from companies (ie: public NASA Imagery etc)

## Additional Notes

_Any other relevant information, inspirations, or considerations?_

[Optional: Add any additional context, ideas, or references]