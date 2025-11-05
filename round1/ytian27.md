# Crowdsourcing Project Idea: GatherAI

## Author
Yuxuan Tian; ytian27

## Problem Statement
Coordinating social plans among friends often fails due to indecision, 
scheduling conflicts, 
and lack of initiative. 
People casually mention ideas “we should grab dinner next week”.
but the plans rarely materialize. 
The challenge lies in transforming scattered intent across group chats into concrete, actionable events without endless coordination.

## Core Concept
**One-line pitch:** An AI assistant that turns iMessage group chat ideas into real social plans by crowdsourcing availability and preferences.

**Target users:** Busy friend groups, roommates, small social circles who want to hang out but struggle to coordinate time and activities.

**The crowd:** The users themselves (friends in the chat) serve as the crowd—each contributing preferences, availability, and suggestions.

**The task:**  Crowd participants reply naturally via iMessage with their availability or preferred activities; the AI aggregates responses to propose the optimal time and plan.

## Key Features
1. iMessage Integration — Users can text the AI directly in a group chat with “we should hang out” or ideas like “brunch or hike this weekend?”
2. Crowdsourced Scheduling — The AI collects each member’s input (availability, preferences, budget) and finds a consensus automatically.
3. Smart Plan Suggestion — AI recommends activities or venues based on aggregated preferences and past successful outings.

## Feasibility Check
**Data source:** User messages and metadata (availability inputs, preference votes) collected through iMessage or a lightweight web interface.

**Budget reality:** Implementable under $500 using OpenAI API credits and free-tier iMessage automation (Shortcuts + webhook integration).

**Crowd size needed:** 10s of users per group, with hundreds of total groups to gather diverse scheduling and social behavior data.

**Quality control approach:** Automatic consistency checks (e.g., calendar conflicts), natural-language parsing validation, and confirmation loops (“Does this plan work for everyone?”).

## Technical Approach
**Human tasks:** Providing ideas, voting on activity options, confirming preferences, and finalizing choices.

**Automated tasks:** Extracting event intents from chat text, summarizing availability, optimizing time and activity selections, and sending confirmation messages.


**Aggregation method:** Weighted majority consensus combining availability overlap and preference strength (e.g., time with highest mutual availability + most-liked activity).

## Prior Work
**Similar projects:** 
- Calendar.help: Workflow-based scheduling agent with humans in the loop
- An Evolutionary Algorithm for Task Scheduling in Crowdsourced Software Development (Saremi et al., 2021)

**Lessons from past course projects:** 	
- Integration into users’ existing behavior (like LingoLoop’s web quiz) increases participation.
- Incentives can be intrinsic—social payoff (getting plans made) instead of points or badges.

## Why This Could Work
This project is viable within course constraints because it uses small, naturally forming crowds (friend groups), requires minimal infrastructure (iMessage bot + basic backend), and generates valuable behavioral data on collective decision-making. It demonstrates how micro-crowdsourced consensus can bridge human intent and AI action in everyday life.
