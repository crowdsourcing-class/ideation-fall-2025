# Crowdsourcing Project Idea: [Project Title]

## Author
Jevin Ta, jevinta

## Problem Statement
My prject will help people plan their travel itineraries for their dream vacations, as people might struggle with deciding what to do and where exactly to travel based on their budgets, travel styles, activity preferences, etc.

## Core Concept
**One-line pitch:** Serve as a crowdsourced travel agent, relying on other people's ratings and travel experiences to curate the best travel itinerary for someone

**Target users:** Travelers looking to seek advice/assistance with planning a trip

**The crowd:** Volunteer workers will be recruited via Reddit (r/travel), social media, and classmates who have traveled before and are willing to provide advice or insight on their experiences.

**The task:** Workers will submit itineraries for certain destinations, vote on which itinerary they think is best, suggest edits to the itinerary or must-sees, etc.

## Key Features
1. Itinerary Submission Portal
2. Crowd Voting + Feedback: 
3. Aggregated Recommendations Dashboard

## Feasibility Check
**Data source:** Crowd-submitted itineraries collected through the platform; optionally seeded with a few example trips from open-source datasets (TripAdvisor) to start.

**Budget reality:** All the infrastructure (backend, frontend, database), can be hosted on free platforms or low-cost platforms, and will be able to fit within the budget of $500.

**Crowd size needed:** We will need roughly 10-50 workers to provide meaningful feedback.

**Quality control approach:** 
Require minimum trip-length and budget fields.
Use upvote ratio to surface trusted itineraries.
Flag low-effort or duplicated submissions.
Optionally, moderation using OpenAI’s content filter for inappropriate text.

## Technical Approach
**Human tasks:** Submitting travel itineraries, evaluating other peoples' itineraries and providing feedback, providing local tips/hidden gems.

**Automated tasks:** Aggregating top itineraries per location, calculating popularity scores and sentiment summaries, and clustering similar itineraries using activity overlap.

**Aggregation method:** Weighted ranking combining upvotes, comment positivity, and itinerary completeness, to generate a score.

## Prior Work
**Similar projects:** Google Travel and TripAdvisor offer algorithmic itinerary suggestions, but lack crowdsourced iteration and refinement.

**Lessons from past course projects:** Fun Facts and Loopify demonstrated how user voting can effectively curate subjective content — inspiration for this system’s rating design.

## Why This Could Work
My project is feasible within one semester: it only requires basic web submission and voting features, a small-scale crowd (100–200 users), and free-tier hosting. The idea leverages genuine human expertise — travelers love sharing their experiences — making it a natural fit for crowdsourcing. By focusing on aggregation and usability rather than scale, it remains achievable and meaningful within NETS 2130’s scope.