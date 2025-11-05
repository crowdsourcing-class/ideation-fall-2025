# Crowdsourcing Project Idea: TripTuner

## Authors

**Original Author:** Jevin Ta (jevinta)  
**Contributor:** Nikki Liu

---

## Problem Statement

Planning a trip can be time-consuming and stressful — travelers must juggle budget, time, and interests while sifting through biased blogs and outdated reviews. Many struggle to decide how to allocate days or choose between similar attractions. **TripTuner** aims to simplify travel planning by letting the crowd collaboratively curate and refine realistic, experience-based itineraries for popular destinations.

---

## Target Audience

- **End users:** Travelers looking for personalized, crowd-approved itineraries that match their interests and budgets.  
- **Crowd workers:** Volunteers (students, Reddit users, travel enthusiasts) who share and rate itineraries based on their own experiences or preferences.  

---

## Description

**TripTuner** is a crowdsourced platform that builds the “best” travel itinerary for each destination through user submissions and crowd voting. Travelers can submit mini-itineraries (e.g., “3 days in Kyoto under $600”), upvote others’ suggestions, and suggest small tweaks (add, remove, or reorder attractions). The system aggregates results to identify the most balanced, popular, and cost-effective plans — effectively turning the community into a collective travel planner.

---

## Project Type
- [x] Business idea using crowdsourcing  
- [ ] Human computation algorithm  
- [ ] Social science experiment with the crowd  
- [ ] Tool for crowdsourcing (requesters or workers)  
- [ ] Other  

---

## Key Features

1. **Itinerary Submission Portal:** Form where users share destination, duration, activities, and cost.  
2. **Voting & Feedback System:** Crowd votes on best itineraries based on realism, variety, and fun factor.  
3. **Comment & Edit Suggestions:** Users propose swaps or improvements to others’ itineraries.  
4. **Aggregated Rankings:** Platform ranks top itineraries using weighted scores.  
5. **Tag-Based Filtering:** Sort itineraries by travel style (e.g., “foodie,” “budget,” “adventure”).  
6. **Local Tips Section:** Short crowd-sourced insights about transport, safety, and must-try foods.  
7. **Leaderboard / Gamification:** Contributors earn points for highly rated itineraries.  
8. **Data Visualization Dashboard:** Displays trends like “average trip cost per destination.”  

---

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**  
Reddit communities (e.g., r/travel, r/solotravel), Penn students, and social media volunteers.  

**What will they provide?**  
Mini-itineraries, votes, and feedback comments.  

**What skills do they need?**  
Basic travel experience and web literacy; no technical expertise required.  

**Do skills vary widely? How?**  
Yes — experienced travelers provide richer itineraries; casual travelers contribute fresh perspectives or simpler ideas.  

**How will you incentivize participation?**  
Intrinsic motivation (sharing travel experiences), social visibility (leaderboards), and gamified point badges (“Master Trip Designer,” “Local Expert”).  

**How much will it cost?**  
$0–$100 maximum for hosting (Render, Firebase) and optional MTurk pilot ($0.05/task for 200 votes ≈ $10).  

**Where will your data come from?**  
User-generated itineraries and open data from Wikivoyage/TripAdvisor for seeding.  

**How many crowd workers do you need?**  
Around 100–200 users for 3–5 destinations to generate meaningful aggregation.  

---

## Technical Approach

**Main steps/components in your system:**  
1. User submits an itinerary through a web form.  
2. Platform stores entries in database and displays them for voting.  
3. Crowd votes and comments on itineraries.  
4. Aggregation algorithm ranks itineraries by weighted metrics (votes, completeness, feedback sentiment).  
5. Dashboard displays top itineraries and insights.  

**Parts done by the crowd vs. automated:**  
- **Crowd:** Create itineraries, vote, provide comments/suggestions.  
- **Automated:** Aggregate results, calculate popularity scores, detect duplicates, visualize data.  

**Technologies/tools:**  
React + Firebase or Next.js + Firestore; optional OpenAI API for summarizing feedback; Google Maps API for displaying locations.  

**Aggregation method:**  
Weighted scoring = 0.6(votes) + 0.2(feedback positivity) + 0.2(completeness).  

---

## Quality Control

**How will you ensure quality of crowd contributions?**  
- Require minimum details (budget, number of days, at least 3 activities).  
- Use upvote ratios to filter low-quality submissions.  
- Automatic text moderation (OpenAI or Perspective API).  
- Manual review for spam or duplicates.  

**Specific quality control methods:**  
- [x] Majority voting across multiple workers  
- [x] Reputation/qualification systems (leaderboards)  
- [x] Statistical outlier detection (flag unrealistic budgets)  
- [ ] Expert review or verification  
- [ ] Gold standard questions  
- [ ] Attention checks  
- [ ] Other: AI-based text moderation  

---

## Evaluation & Success Metrics

**How will you know if your project succeeds?**  
- Minimum of 100 itineraries or votes collected.  
- At least 3 destinations with aggregated crowd rankings.  
- Positive user feedback (≥80% say results were “useful”).  

**Quantitative success metrics:**  
- 70% agreement rate on top itinerary rankings.  
- Average of ≥5 votes per itinerary.  
- System uptime ≥95%.  

---

## Challenges & Mitigation Strategies

**Challenge 1:** Low participation.  
**Mitigation:** Seed the platform with example itineraries; post calls to action on Reddit and Penn forums.  

**Challenge 2:** Inconsistent or unrealistic submissions.  
**Mitigation:** Require budget and duration inputs; auto-flag extreme outliers.  

**Challenge 3:** Bias toward popular destinations.  
**Mitigation:** Rotate featured cities weekly; display “underrated destination” sections.  

---

## Prior Work

**Similar projects or systems:**  
- *TripAdvisor* and *Google Travel* recommend activities but lack iterative crowd refinement.  
- *Fun Facts (NETS 2130)* inspired the voting and feedback loop.  
- *Loopify (NETS 2130)* showed how subjective judgments (like “vibes”) can be effectively aggregated.  

**How this differs:**  
TripTuner centers on *collective itinerary design*, where human creativity and contextual knowledge matter more than factual correctness.

---

## Discussion Notes from Round 2

**What did you agree on?**  
To keep the scope focused on a small number of destinations and prioritize quality aggregation over scale.  

**What concerns or pushback emerged?**  
Feasibility of gathering enough crowds without MTurk and ensuring consistent quality.  

**Why is this idea promising?**  
Travel inspires participation naturally; people love sharing experiences. It fits the course goal of exploring how collective input can produce better subjective outcomes.  

**What makes this sustainable and feasible?**  
Minimal infrastructure needs, clear user motivation, and well-defined human–machine task boundaries make it achievable within one semester and under $100.

---

## Additional Notes

- Future extension: personalize itineraries based on user profiles (“budget traveler,” “food lover”).  
- Potential collaboration with Penn Abroad or student travel clubs for crowd testing.  
- Could evolve into a real-world startup idea combining crowdsourced itineraries with AI recommendations. 
