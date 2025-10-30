# Crowdsourcing Project Idea: CrowdSolver

## Author
Anton Bakhurov

## Problem Statement


## Core Concept
**One-line pitch:** It uses crowd wisdom to come up with optimal solutions for global/local problems. 

**Target users:** Organizations which need to solve some pressing issues but are unsure how to approach them

**The crowd:** Anyone interested in contributing to the solutions of global challenges or learning about these solutions. 

**The task:** They will suggest their solutions to the problems posted on the platform (by the platform itself and by other users) and then vote on the best solution for each 

## Key Features
1. Allowing users to post a challenge/problem that think requires a solution achieved by crowd wisdom
2. Allowing users to suggest solutions to proposed challenges 
3. Allowing users to upvote the best solutions for each problem 
4. Using NLP to aggregate user results to display the aggregated/average solution of the crowd

## Feasibility Check
**Data source:** From the users. The prompts for problems may come from the platform as well. 

**Budget reality:** This doesn't need any money, as the main incentives here are not based on monetary rewards. 

**Crowd size needed:** The more the better, although about 100 people should be enough to either find the optimal idea or to achieve a strong aggregated result 

**Quality control approach:** To ensure quality, the platform will combine crowd moderation and reputation-based weighting. Users can flag low-effort or duplicate submissions, while active contributors with strong voting histories gain greater influence in rankings.

## Technical Approach
**Human tasks:** 
Posting meaningful problem statements and proposed solutions.
Evaluating and upvoting ideas based on clarity, feasibility, and impact.
Providing qualitative feedback and refining others’ suggestions.

**Automated tasks:** 
Clustering similar solutions using NLP models 
Calculating weighted scores based on upvotes, credibility, and textual similarity.
Generating summarized “crowd consensus” solutions using AI summarization tools.
Monitoring for spam or irrelevant content automatically.


**Aggregation method:** 
Weighted aggregation: combine votes, text similarity, and user reliability scores to identify top solutions. The NLP system will then synthesize an averaged “crowd solution” by merging common themes and phrasing them coherently. 

## Prior Work
**Similar projects:** - 

**Lessons from past course projects:** - 

## Why This Could Work
CrowdSolver is feasible within course constraints because it relies primarily on user-generated input and simple NLP aggregation, requiring minimal infrastructure and no financial incentives. It combines scalable computation with authentic human creativity, enabling meaningful results even from a small, motivated community of contributors.`
