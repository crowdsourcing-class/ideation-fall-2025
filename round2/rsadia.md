# Crowdsourcing Project Idea: Penn Sustainability Tracker

## Authors

**Original Author:** Sadia Rahman rsadia

**Contributor:** N/A (no partner since I was not in class)

## Problem Statement

Penn's sustainability initiatives often lack a comprehensive and easily accessible system for tracking individual and community efforts. With diverse actions across campus, from recycling to energy-saving behaviors, it’s difficult to gauge real-time progress or ensure that sustainability efforts are being actively maintained. There is a clear need for a crowdsourced platform to track and improve sustainable actions across the campus.

## Target Audience

The primary users will be Penn students, faculty, and staff, specifically those interested in sustainability initiatives on campus. Crowd workers will include members of the Penn community who will report sustainability actions they have taken and verify the actions of others.

## Description

Penn Sustainability Tracker is a crowdsourced platform that enables Penn community members to track and verify sustainable actions across campus. The platform will allow users to submit actions they’ve taken, such as recycling or energy-saving measures, and validate the actions of others. By incorporating gamification and community verification, the platform aims to increase awareness, participation, and accountability in Penn’s sustainability initiatives.
## Project Type

_Select the category that best fits your project:_

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [X] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [] Other: [specify]

## Key Features

_List 5-8 key features or capabilities of your system. Expand from Round 1:_

1. Real-time reporting of sustainability actions (e.g., recycling, energy savings).
2. Community verification and validation of sustainability actions.
3. Gamified points and rewards system for verified actions.
4. Public leaderboards to encourage competition and accountability.
5. Integration with Penn’s sustainability data for tracking long-term trends.
6. Periodic sustainability challenges to increase participation.

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
The crowd workers will be Penn students, faculty, and staff, who will participate through the web platform or mobile app.

**What will they provide?**
Users will submit sustainability actions and verify the actions of others, such as confirming whether recycling bins are used correctly or if energy-saving actions are reported accurately.

**What skills do they need?**
Basic internet skills, familiarity with sustainability concepts, and an interest in improving campus sustainability.

**Do skills vary widely? How?**
The skills required are relatively basic, as the tasks involve simple reporting and verification. However, users with more knowledge of sustainability practices might be better at accurately verifying actions.

**How will you incentivize participation?**
Participation will be incentivized through a point system, where users earn points for reporting and verifying sustainability actions. These points can be redeemed for rewards, such as discounts at local businesses, stores/restaurants around campus, or exclusive sustainability-related events. Leaderboards and periodic challenges will also drive engagement.

**How much will it cost?**
The initial cost will be for development and maintenance of the platform, including server hosting and reward management. Rough estimate: $400-$500 for development and hosting for the first semester.

**Where will your data come from?**
Data will come from user-generated content, including actions they’ve taken (e.g., recycling, energy savings) and verifications of others' actions.

**How many crowd workers do you need?**
Approximately 100–500 users for initial implementation, with plans for scale as awareness grows.

## Technical Approach

**What are the main steps/components in your system?**

1. Users sign up and log in to the platform.
2. Users report sustainability actions (e.g., recycling, energy-saving measures).
3. Other users verify the actions by voting or commenting.
4. The system aggregates results based on majority votes.
5. Points are awarded to users based on the validity of their submissions and verifications.

**What parts are done by the crowd vs. automated?**
Crowd tasks: Reporting sustainability actions and verifying the actions of others.
Automated tasks: Aggregating results, updating leaderboards, sending notifications for challenges, and generating sustainability reports.

**What technologies/tools will you use?**
React (for frontend), Node.js (for backend), AWS (for hosting), and possibly an API for integrating Penn’s sustainability data.

**How will you aggregate results from the crowd?**
Majority voting will be used for verifying submissions. Users with a higher reputation score (based on consistent accuracy in reporting and verifying) will have their votes weighted more heavily.

## Quality Control

**How will you ensure quality of crowd contributions?**

Users earn points for accurate submissions and verifications, and their past contributions influence the weight of their votes. Actions will be verified by multiple users, and the majority vote will be used for validation. Periodic sustainability challenges will encourage engagement and moderation of contributions.

**Specific quality control methods:**
- [X] Gold standard questions (test questions with known answers)
- [X] Majority voting across multiple workers
- [ ] Expert review or verification
- [ ] Attention checks or trap questions
- [X] Reputation/qualification systems
- [ ] Statistical outlier detection
- [ ] Other: [specify]

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
Success will be evaluated based on the number of active users (target: 100 users in the first month), engagement rate (number of actions reported and verified per user), accuracy of reported actions (percentage of verified actions vs. false reports), and feedback from users regarding usability and motivation.

**What would success look like quantitatively?**
At least 500 actions reported and verified within the first 3 months. 80% of actions verified by at least two other users. 75% positive feedback on usability and incentives.

## Challenges & Mitigation Strategies

_For each challenge, propose a mitigation strategy:_

**Challenge 1:** Ensuring accurate verification of sustainability actions.
**Mitigation:** Implement a reputation system that rewards verified actions and penalizes false reports. Users with higher reputation scores will have their votes weighted more heavily.

**Challenge 2:** Engaging enough users to generate meaningful data.
**Mitigation:** Implement gamification and challenges, such as "Sustainability Week," to drive participation. Partner with sustainability clubs and organizations at Penn for promotional efforts.

**Challenge 3:** Managing scalability as the platform grows.
**Mitigation:** Use cloud-based infrastructure (AWS) to scale easily. Initially, the system will handle a smaller number of users, but it can be scaled up as needed.

## Prior Work

_Are there similar projects or systems? How is yours different?_

This project focuses on real-time reporting and verification of sustainability actions, with strong community engagement through gamification and rewards. It also targets the specific context of Penn’s campus, which is crucial for creating actionable and localized sustainability data.

**Specific related projects:**
Recyclebank: A rewards-based system for encouraging recycling, which is similar in terms of incentivizing sustainable actions. However, Penn Sustainability Tracker focuses specifically on real-time tracking across various sustainability efforts on campus.

Cal State's Greenpoints: A platform for funding sustainability projects on campus. Our project differs by using crowdsourcing to track and verify individual sustainability actions.

## Discussion Notes from Round 2

**Absent in class so I did this myself**

**What did you agree on?**
This idea addresses a real need for more visibility into sustainability efforts on campus and will increase engagement through gamification and community verification.

**What concerns or pushback emerged?**
The main concern is ensuring accurate verification of reported actions and dealing with possible false reports. The reputation system and community-based verification are designed to mitigate this.

**Why is this idea promising?**
Sustainability is a key issue at Penn, and this project will engage the community in a meaningful way while providing valuable data for future initiatives.

**What makes this sustainable and feasible?**
The project can be scaled as needed, and the low-cost platform can be built on existing tools (React, Node.js, AWS). It also benefits from Penn’s strong sustainability focus, which will attract users.

## Additional Notes

_Any other relevant information, inspirations, or considerations?_

N/A
