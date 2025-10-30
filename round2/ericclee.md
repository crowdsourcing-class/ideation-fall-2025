# Crowdsourcing Project Idea: FoundryMatch


## Authors


**Original Author:** Eric Lee, ericclee


**Contributor:** Mario Valek, mvalek


## Problem Statement


My project solves the problem of the difficulty in founding a startup team. The process of creating a startup involves creating a founding team and an idea that solves a critical problem that many people around the world face.


## Target Audience


Aspiring founders, engineers, designers, and entrepreneurs seeking collaborators or startup ideas.


## Description


Crowd members will:
- Post and describe problems they face or observe.
- Upvote the most compelling problems.
- Join discussion threads or “problem hubs.”
- Form private teams or group chats around promising problems to brainstorm and prototype solutions collaboratively.


## Project Type


_Select the category that best fits your project:_


- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [X] Business idea using crowdsourcing
- [ ] Other: [specify]


## Key Features


_List 5-8 key features or capabilities of your system. Expand from Round 1:_


1. Problem Posting and Voting: Users can share challenges and collectively rank them by upvotes.
2. Team Formation System: Matching users based on shared interests, complementary skills, and time availability.
3. Discussion and Collaboration Hub: Real-time chat or forum for each problem, allowing ideation and coordination.
4. Progress Tracking: Simple tools for groups to document milestones and share progress publicly.
5. Skill-Based Matching: Instead of just matching people to teams, the platform matches them to validate a problem. A user can flag a problem and state for instance: "I need a Digital Marketer to help capture customer acquisition cost for this." The platform then specifically finds marketers interested in the domain to provide preliminary insights, often leading to deeper collaboration.
6. Progress Pulse for the Crowd: A public, anonymized dashboard for each active team showing their status (e.g., "Ideation," "Prototyping," "Launched"). This creates a sense of momentum for the entire community and allows others to learn from the journey.
7. Competitor & Alternative Mapping: A dedicated section within each Problem Hub where the community can collaboratively list and analyze existing solutions. This becomes a living document that every new team member can review to instantly understand the competitive landscape.
8. Market Data Aggregation: For a highly-upvoted problem, the platform could automatically generate a simple one-page report by pulling in publicly available data (e.g., market size from Statista, news trends, relevant subreddit growth). This adds a layer of objective validation that helps teams commit.


## Feasibility: Crowd & Resources


**Where will your crowd workers come from?**
[E.g., MTurk, volunteers, social media users, students, etc.]
Crowd workers will come from online users who want to post niche problems on the internet to see if their problems are relatable or want solved. They can also come from engineers or entrepreneurs who are browsing for potential ideas to work on.


**What will they provide?**
User-generated content — problem submissions, votes, and discussions.
The users will provide ideas for problem identification and vote on which problems are most relatable. They can also start discussions of ideas or once they join a team, start discussions to get started on a project.


**What skills do they need?**
They would need to know how to read and write in English. They would also need programming skills if they are an engineer. General internet users are also welcomed for posting and relating with problems posted by others. 


**Do skills vary widely? How?**
[Explain if some workers will be better than others and why]
On the engineering and entrepreneurship side, some workers will be better than others. For everyday users simply upvoting or posting common problems they face, there will not be much variance in skill. 


**How will you incentivize participation?**
[E.g., payment, gamification, intrinsic motivation, course credit. Be specific about your incentive design.]
Participation will be incentivized through relatability. People will be able to see which problems other people face that they also frequently face. Engineers and entrepreneurs are incentivized for their personal goal of working on a startup. 


**How much will it cost?**
Frontend and backend can be hosted using free tiers (e.g., Render, Firebase). AI-assisted matching and moderation can rely on free or low-cost APIs (< $500 total).


**Where will your data come from?**
[E.g., public datasets, user-generated, scraped data, APIs, etc.]


**How many crowd workers do you need?**
Initial pilot with 100–200 users to ensure meaningful voting and team formation.


## Technical Approach


**What are the main steps/components in your system?**


1. User Onboarding & Profile Creation: Users sign up and create a detailed profile, listing their skills, interests, commitment level, and past project experience.
2. Problem Submission & Initial Curation: Users post problems they've observed. An automated system performs initial checks for quality and duplicates. 
3. Crowd Validation & Engagement: The crowd upvotes, comments on, and discusses posted problems within "Problem Hubs." The system calculates a dynamic "Problem-Market Fit" score.
4. Intelligent Matching & Team Formation: The system suggests potential collaborators to users and forms teams based on complementary skills, interests, and commitment levels within active Problem Hubs.
5. Collaborative Workspace Activation: When a team forms, a private, feature-rich workspace is automatically created with tools for chat, progress tracking, and resource sharing.
6.  Progress Tracking & Community Showcase: Teams document their milestones. The platform aggregates anonymized progress data to showcase community momentum and successful "alumni" teams.




**What parts are done by the crowd vs. automated?**
Human tasks: Posting problems, voting, evaluating feasibility, and collaborating on solutions.
Automated Tasks: Ranking posts, suggesting potential teammates based on shared interests or skill tags, and flagging duplicate or low-quality submissions.


**What technologies/tools will you use?**
[E.g., Python, React, AWS, specific ML libraries, MTurk API, etc.]
We will use React for frontend and a SQL database 


**How will you aggregate results from the crowd?**
We will aggregate results through our frontend website where they can interact with the platform and users. 


## Quality Control


**How will you ensure quality of crowd contributions?**


Weighted voting (by participation level), spam detection, and text content moderation through AI tools


**Specific quality control methods:**
- [ ] Gold standard questions (test questions with known answers)
- [X] Majority voting across multiple workers
- [X] Expert review or verification
- [ ] Attention checks or trap questions
- [ ] Reputation/qualification systems
- [ ] Statistical outlier detection
- [ ] Other: [specify]


## Evaluation & Success Metrics


**How will you know if your project succeeds?**
500+ registered users within the first 3 months. 50+ high-quality problem submissions (receiving >10 upvotes) per month. Average session duration of >5 minutes. Team Formation:  20+ teams formed within the first 3 months. Average team size of 2-4 members with complementary skills.


**What would success look like quantitatively?**
500+ registered users within the first 3 months. 50+ high-quality problem submissions (receiving >10 upvotes) per month. Average session duration of >5 minutes. Team Formation:  20+ teams formed within the first 3 months. Average team size of 2-4 members with complementary skills.


## Challenges & Mitigation Strategies


_For each challenge, propose a mitigation strategy:_




**Challenge 1:** The "Cold Start" Problem attracts a critical mass of users to make matching effective.
**Mitigation:** Mitigation: Start by targeting specific, tight-knit communities (e.g., university entrepreneurship clubs, tech incubators). Seed the platform with well-defined, interesting problems before the public launch to give early users immediate value.


**Challenge 2:** Maintaining high-quality, spam-free discussions and problem submissions
**Mitigation:** Implement the robust quality control system outlined above, combining automated AI moderation with a user reputation system. Onboarding will include clear community guidelines.  


**Challenge 3:** Teams forming but failing to make progress, leading to user churn.
**Mitigation:** Provide structured guidance within the collaborative workspace (e.g., milestone templates, links to startup resources). Introduce optional weekly check-in prompts for teams and showcase "Team of the Week" to foster accountability and motivation.


## Prior Work


_Are there similar projects or systems? How is yours different?_


Our project starts with crowd-validated problems, not people or ideas, integrating the entire journey from problem identification to team formation and collaboration in one structured platform.


**Specific related projects:**
- Reddit r/Entrepreneur and IndieHackers (discussion-based but lack structured collaboration tools).
- Kickstarter (crowdfunds ideas but doesn’t crowdsource their creation).


## Discussion Notes from Round 2


**What did you agree on?**
[Key points of agreement between partners]


**What concerns or pushback emerged?**
[Questions, challenges, or areas of uncertainty discussed]


**Why is this idea promising?**
[Explain why you chose to develop this idea over the alternative]


**What makes this sustainable and feasible?**
FoundryMatch transforms problem-solving into a social, collaborative process. It’s technically feasible within course limits, promotes creativity and teamwork, and leverages crowdsourcing principles—aggregation, diversity, and iterative refinement—to help users co-create startup ideas and teams with real-world potential.


## Additional Notes


_Any other relevant information, inspirations, or considerations?_


[Optional: Add any additional context, ideas, or references]
