# Crowdsourcing Project Idea: [Project Title]

## Author
Sofiia Kikaleishvili 49141078

## Problem Statement
In an increasingly globalized world, people are shaped by both local and international influences — yet few realize how their values and attitudes align (or differ) from their own culture. Misunderstandings about friendship, ambition, or social hierarchy often arise from these unseen differences. CultureQuest helps users uncover which cultures they truly think like, creating a dynamic global map of shared mindsets and value systems.

## Core Concept
**One-line pitch:** A global self-discovery quiz where users answer social and life-scenario questions to see which country’s mindset they align with — revealing hidden cultural similarities and differences.

**Target users:** Curious individuals, students, travelers, and professionals interested in psychology, culture, or global communication.

**The crowd:** Volunteers and social media users worldwide motivated by self-understanding and curiosity rather than financial incentives.

**The task:** Participants answer short, realistic situational questions (e.g., about friendship, work, or social hierarchy). Their responses are aggregated with others’ answers to identify which national or cultural clusters their values most closely match.

## Key Features
1. Cultural Alignment Quiz: Users answer 15–20 life-scenario questions about relationships, loyalty, ambition, and values.
2. Cultural Match Results: The platform shows which countries’ response patterns most closely resemble the user’s.
3. Global Social Map: Interactive visualization showing cultural clusters and how each user fits within global social mindsets.

## Feasibility Check
**Data source:** Anonymous responses from users taking the quiz, tagged with basic demographics and country of origin.

**Budget reality:** Developed using free or low-cost tools (React + Flask + Firebase/Airtable). Hosting on free tiers (Vercel, Render). Estimated cost <$100.

**Crowd size needed:** Hundreds for initial cultural clusters; thousands for richer, statistically significant comparisons.

**Quality control approach:** Randomized question order and attention checks to filter spam

Optional verification (e.g., location check or email confirmation)

Removal of incomplete or inconsistent responses

## Technical Approach
**Human tasks:** Provide authentic answers to social and moral scenarios requiring reflection on friendship, success, or honesty.

**Automated tasks:** Aggregate responses by region/country

Compute user–culture similarity using clustering or distance metrics

Visualize cultural proximities via interactive charts or maps

**Aggregation method:** Each country’s responses form an averaged “cultural profile.” A user’s answer vector is compared to these profiles to calculate a similarity score (e.g., “You align 70% with Canadians, 20% with Japanese, 10% unique”).

## Prior Work
**Similar projects:** World Values Survey: Large-scale attitudinal study, but static and academic. CultureQuest adds interactivity and personal feedback.

MoralMap (Penn): Collected moral judgments; CultureQuest explores everyday social and relational attitudes, emphasizing self-discovery.

**Lessons from past course projects:** Projects that rely solely on altruism fade quickly. By offering personalized, curiosity-driven feedback, CultureQuest motivates participation while producing valuable cross-cultural data.

## Why This Could Work
People are naturally curious about who they are and how they compare to others. CultureQuest transforms that curiosity into meaningful data collection — users get instant insights about their cultural alignment, while the aggregated responses form a unique, human dataset for cultural and AI research. The project is low-cost, scalable, and deeply engaging, fitting perfectly within course constraints.
