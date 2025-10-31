# Crowdsourcing Project Idea: Where2Go

## Authors

**Original Author:** Vedha Avali (vavali)

**Contributor:** Leha Choppara (lehac)

## Problem Statement

Finding a clean, safe, and accessible public restroom is a daily challenge in many cities and campuses. Existing maps rarely include information on cleanliness, privacy, or accessibility. This project crowdsources bathroom ratings and reviews to help users(starting with Penn students) locate reliable restrooms across Philadelphia.

## Target Audience

Students, tourists, delivery workers, and city residents who frequently move around Philadelphia and need trustworthy bathroom information.

## Description
Where2Go is a crowdsourced web and mobile platform that helps students and visitors locate, rate, and review public restrooms on and around the University of Pennsylvania campus. Users contribute by uploading photos, rating cleanliness and accessibility, and confirming or flagging existing listings. The system aggregates these contributions into an interactive, color-coded map that highlights the best and most reliable restroom options in real time. By leveraging community input, Where2Go builds a continuously improving, trustworthy resource for everyone on campus.

## Project Type

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [x] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 5-8 key features or capabilities of your system. Expand from Round 1:_

1. Bathroom rating system: cleanliness, accessibility, privacy, and supply level
2. Interactive map: shows nearby restrooms with crowd-sourced ratings and filters.
3. Photo and review upload: users can add images, notes,and confirm/flag inaccurate reviews.
4. Leaderboard system: top contributors are given in-app medals.
5. Computer vision, review filtering and user reporting for quality control: Photos/reviews with upsetting content will be filtered out. Users can also report photos and suspicious reviews.

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
Initially limited to Penn Students.

**What will they provide?**
Photos, bathroom ratings (cleanliness, privacy, supply levels, accessibility), verification/comments on other reviews, bathroom access codes.

**What skills do they need?**
Only basic smartphone skills are required, the average person is capable of contributing.

**Do skills vary widely? How?**
There may be minor variations in attention to detail or judgment of cleanliness, but overall consistency is expected.

**How will you incentivize participation?**
Gamification (leaderboards, badges, streaks), intrinsic motivation (help peers and community), and small prize raffles (<$50).

**How much will it cost?**
Estimated <$200 total: Basic AWS hosting, Google Maps API, and small prizes.

**Where will your data come from?**
User submissions (ratings, photos, comments) and, optionally, open data sources from the City of Philadelphia for initial seeding

**How many crowd workers do you need?**
A smaller crowd is sufficient for a proof of concept (i.e. 50-100 students), then the project is expandable for the Penn community as a whole.

## Technical Approach

**What are the main steps/components in your system?**

1. User uploads restroom rating, and optionally a review and/or a photo.
2. System highlights nearby reviewed restrooms. After a user has navigated to a restroom, the system will ask it to add their own rating and verify unverified photos.
3. System aggregates rating, with slight rating by recency

**What parts are done by the crowd vs. automated?**
Human tasks: Identify and review restrooms, upload photos, rate key features, and validate others’ posts.
Automated tasks: Compute average scores, merge duplicate entries (same coordinates), and generate visual heatmaps of restroom quality.

**What technologies/tools will you use?**
Python backend, AWS for storage, Google Maps API (or something similar).

**How will you aggregate results from the crowd?**
Weighted averages of user ratings by reputation; entries within a small distance (e.g., 15 m) merged into a single bathroom record.

## Quality Control

**How will you ensure quality of crowd contributions?**

- Reputation system: verified contributors’ votes carry more weight.
- Cross-validation: multiple users must confirm new bathroom entries.
- Flagging and admin moderation for spam or false data.

**Specific quality control methods:**
- [ ] Gold standard questions (test questions with known answers)
- [x ] Majority voting across multiple workers
- [x] Expert review or verification
- [ ] Attention checks or trap questions
- [x] Reputation/qualification systems
- [x] Statistical outlier detection
- [ ] Other: [specify]

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
Success will be measured by user engagement, verified data coverage, and system reliability.

**What would success look like quantitatively?**
- ≥ 100 restroom entries in pilot phase
- ≥ 25 unique contributors
- ≥ 50% entries confirmed by multiple users (verified entries confirmed by ≥2 users)
- 80% positive user satisfaction in survey

## Challenges & Mitigation Strategies


**Challenge 1:** Users could review bomb.
**Mitigation:** Flag restrooms with abnormally high number of low ratings for trusted users to verify ratings.

**Challenge 2:** Lack of data on less-frequented restrooms.
**Mitigation:** Extra leaderboard points or perhaps monetary rewards to incentivize more reviews for under-reviewed locations.

**Challenge 3:** Unrelated/upsetting photos.
**Mitigation:** Photos will be screened with computer vision for upsetting content. Other users will be asked if example photos are irrelevant (i.e. not of a restroom) and if it passes community guidelines. 

## Prior Work

**Specific related projects:**
- Got2Go NYC: This is an application containing reviews of bathrooms specifically in New York City, and originated from a TikTok creator’s account and her personal reviews. The app is not necessarily crowdsourced, as many of the reviews are from this individual TikTok creator. 
- StudySphere (past course project): Similarly to our application, this app was built for students to crowdsource information, and for other students to benefit from this crowdsourced information. 

## Discussion Notes from Round 2

**What did you agree on?**
We agreed to focus the project on campus restrooms around Penn as a contained and testable environment before expanding city-wide. We both also supported using gamification (leaderboards, streaks, and badges) along with small prizes to add additional incentives.

**What concerns or pushback emerged?**
Some concerns were raised about maintaining participation and about potential misuse, such as joke submissions or irrelevant photos. There were also questions around privacy (e.g., avoiding people appearing in restroom photos) and moderation workload for potentially verifying reports.

**Why is this idea promising?**
We felt this idea was both immediately useful and easy to pilot on campus. It solves a real, everyday student pain point while being simple enough to test within the semester. Unlike abstract crowd projects, Where2Go produces visible, verifiable results, as students can instantly benefit from the data they help create.

**What makes this sustainable and feasible?**
The proof of concept can operate on low-cost tools and intrinsic motivation, keeping costs minimal. The tasks are short, intuitive, and rewarding, allowing even a small initial crowd to generate meaningful coverage. Because the system’s data can be automatically validated by GPS and photos, it requires minimal manual oversight, making it scalable and sustainable beyond the course timeline.


