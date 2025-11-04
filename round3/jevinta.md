# Crowdsourcing Project Idea: TripTuner

## Authors

**Original Author:** Jevin Ta (jevinta)  
**Round 2 Contributors:** Jevin Ta (jevinta), Nikki Liu (nikkiliu)
**Round 3 Contributors:** Jevin Ta (jevinta), Nikki Liu (nikkiliu), Julia Zhuo (juzhuo), Arushi Agarwal (arushiga), Liana Veerasamy (lianav), Sadia Rahman (rsadia)

---

## Problem Statement

Planning a trip is often stressful and inefficient — travelers must balance budget, timing, and preferences while sorting through biased blogs and inconsistent reviews. Many struggle to design realistic itineraries that fit their schedule and price range. **TripTuner** streamlines this process by crowdsourcing authentic, experience-based itineraries and ranking them through community feedback and automated aggregation.

---

## Target Audience

**End Users:** Travelers seeking realistic, crowd-curated itineraries that match their budget, interests, and timeframe.  
**Crowd Workers:** Students, travel enthusiasts, Reddit users, and social-media volunteers who share itineraries, rate submissions, and provide feedback.  
**Stakeholders:** Tourism organizations, travel startups, and student travel clubs interested in collective insight from real travelers.

---

## Description

**TripTuner** is a community-driven travel-planning platform where users collaboratively design and refine itineraries. Travelers submit sample plans (e.g., “3 days in Kyoto under $600”), while the crowd votes, comments, and suggests edits. The system aggregates input using a weighted algorithm combining votes, feedback sentiment, and completeness, surfacing the most balanced itineraries. Over time, TripTuner becomes a dynamic library of realistic travel plans enriched with local insight and crowd wisdom.

---

## Project Type

_Select the primary category:_

- [ ] Human computation algorithm  
- [ ] Social science experiment with the crowd  
- [ ] Tool for crowdsourcing (requesters or workers)  
- [x] Business idea using crowdsourcing  
- [ ] Other: [specify]

---

## Key Features

1. **Itinerary Submission Portal** – Structured form for destination, budget, duration, and activities.  
2. **Voting & Feedback System** – Crowd evaluates itineraries by realism, value, and fun factor.  
3. **Editable Suggestions** – Users can propose swaps or reorder activities.  
4. **Aggregated Ranking Engine** – Weighted scoring formula (0.6 votes + 0.2 feedback + 0.2 completeness).  
5. **Tag-Based Filtering** – Filter by themes like foodie, budget, adventure, romantic.  
6. **Local Tips Hub** – Crowd-sourced advice on transport, safety, and hidden gems.  
7. **Leaderboard & Gamification** – Points and badges for top contributors (e.g., “Local Expert”).  
8. **Visualization Dashboard** – Graphs showing average trip costs and popularity by region.  
9. **Duplicate Detection** – NLP-based system to merge similar submissions.  
10. **AI Summarization Assistant** – Generates concise feedback summaries for users.

---

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**  
Reddit communities (r/travel, r/solotravel), Penn student forums, Instagram travel accounts, and volunteer networks.

**What will they provide?**  
Mini-itineraries, votes on existing plans, and short feedback comments.

**What skills do they need?**  
Basic travel experience, web literacy, and interest in sharing advice. No technical expertise required.

**Do skills vary widely? How?**  
Yes — some contributors are seasoned travelers providing depth, others are casual travelers offering fresh perspectives.

**How will you incentivize participation?**  
Intrinsic motivation (share travel stories), social recognition (leaderboards and badges), and gamification (ranking titles like “Master Trip Designer”).

**Budget & Cost Analysis:**  
- Estimated cost per task: $0.05 (vote on MTurk)  
- Estimated cost per worker: $0.50 (for ~10 votes)  
- Number of tasks needed: 250 votes + 50 itinerary submissions  
- Total estimated budget: $75–$100  
- Justification: Covers Firebase hosting + pilot crowd testing.

**Where will your data come from?**  
User-generated itineraries and open APIs (Wikivoyage, TripAdvisor, Google Travel).

**Scale Requirements:**  
- Minimum viable crowd size: 100 workers  
- Target crowd size: 200 workers for 5 destinations  
- Scalable to: >1,000 users via social media promotion.

---

## Technical Architecture

**System Components:**

1. Frontend web interface (React or Next.js)  
2. Backend API (Node.js + Express)  
3. Database (Firebase Firestore or PostgreSQL)  
4. Feedback processing (OpenAI API for summarization and moderation)  
5. Visualization (D3.js or Chart.js dashboard)

**Detailed Workflow:**

1. User submits an itinerary via the web portal.  
2. System validates inputs (budget, duration, activities).  
3. Crowd votes and leaves comments.  
4. Algorithm computes aggregate score (0.6 votes + 0.2 feedback + 0.2 completeness).  
5. Top ranked itineraries and insights display on dashboard.  
6. AI moderation filters spam and duplicates.

**Human vs. Automated Tasks:**

| Task | Performed By | Why? |
|------|--------------|------|
| Submit itineraries | Human | Requires creativity and context knowledge |
| Voting and feedback | Human | Subjective judgment best done by people |
| Aggregation and ranking | Automated | Ensures consistency and scalability |
| Spam and duplicate detection | Automated | Pattern recognition via NLP |

**Technologies & Tools:**  
- Frontend: React / Next.js  
- Backend: Node.js / Express  
- Database: Firebase Firestore  
- ML/AI: OpenAI API for text analysis and summaries  
- Crowdsourcing Platform: Custom + Reddit integration  
- Hosting: Vercel or Render  

**Aggregation Method:**  
Weighted scoring = 0.6 × votes + 0.2 × feedback sentiment + 0.2 × completeness. Scores are normalized to produce final rankings.

---

## Quality Control

**Quality Control Strategy:**  
Combine community feedback with automated filters to prioritize complete, authentic, and realistic itineraries.

**Specific QC Mechanisms:**
- [ ] Gold standard questions – _not applicable to creative tasks_  
- [x] Majority voting – Each itinerary receives ≥ 5 votes; ties broken by feedback sentiment.  
- [x] Expert review (optional) – Top entries spot-checked by experienced travelers.  
- [x] Reputation system – Points and badges build trust.  
- [x] Statistical outlier detection – Flag budgets 2σ above/below mean.  
- [x] AI moderation – Filter spam and offensive text using Perspective API.  

**Handling Low-Quality Work:**  
Flagged itineraries are temporarily hidden for review; repeat low-quality contributors lose visibility points.

---

## Evaluation & Success Metrics

**Primary Success Metrics:**

1. ≥ 100 unique itinerary submissions (measured via database entries).  
2. ≥ 80 % positive user feedback on usefulness (post-survey).  
3. ≥ 70 % consensus agreement on top ranked plans.

**Evaluation Methodology:**  
Collect user interaction logs, analyze agreement rates between voters, and conduct post-use surveys for satisfaction and realism.

**Baseline Comparisons:**  
Compare TripTuner output to TripAdvisor’s top activities to measure diversity and authenticity.

**Success Criteria:**  
- **Minimum:** 30 itineraries and 150 votes.  
- **Target:** 100 itineraries and 500 votes.  
- **Stretch:** 500 active users and stable aggregation performance.

---

## Challenges & Mitigation Strategies

**Challenge 1:** Low Participation  
- **Why it's a risk:** Without enough crowd input, aggregation is weak.  
- **Mitigation strategy:** Seed example itineraries and post calls to action on Reddit.  
- **Backup plan:** Use MTurk for initial pilot votes.

**Challenge 2:** Inconsistent Quality  
- **Why it's a risk:** Low-effort or unrealistic entries reduce trust.  
- **Mitigation strategy:** Require minimum details (budget + 3 activities).  
- **Backup plan:** Manual moderation by admins.

**Challenge 3:** Bias Toward Popular Destinations  
- **Why it's a risk:** Lesser-known cities get ignored.  
- **Mitigation strategy:** Rotate featured cities and highlight “Hidden Gem” section.  
- **Backup plan:** Weighted promotion of low-submission cities.

---

## Prior Work & Related Projects

**Similar Existing Systems:**

1. **TripAdvisor / Google Travel**  
  - Description: Crowd-review platforms listing activities per destination.  
  - Similarities: Crowd input and ranking mechanisms.  
  - Differences: Lack of iterative crowd refinement or editable itineraries.  

2. **Fun Facts (NETS 2130)**  
  - Description: Used voting and feedback loops for subjective judgments.  
  - Similarities: Relies on community aggregation.  
  - Differences: TripTuner applies it to creative planning and ranking.

3. **Loopify (NETS 2130)**  
  - Description: Crowdsourced music loop recommendations based on vibes.  
  - Similarities: Subjective input aggregation.  
  - Differences: TripTuner emphasizes structured itinerary data and budget factors.

**Lessons from Past Course Projects:**  
Successful projects focused on tight scope and gamification; TripTuner adopts both for better crowd engagement and data quality.

---

## Ethical Considerations

**Potential Ethical Issues:**  
- Privacy concerns with user travel data.  
- Fair compensation for any paid crowd tasks.  
- Accuracy and safety of user-generated content.

**Mitigation Strategies:**  
- Anonymize submissions and store non-identifiable data only.  
- Use volunteer model for creative tasks; pay only microtasks fairly.  
- AI moderation and manual review of sensitive or unsafe suggestions.

**IRB Considerations:**  
Likely exempt — no sensitive personal data or interventions involved.

---

## Business Viability (Optional)

**Revenue Model:** Affiliate links for bookings, ads, and freemium analytics dashboards.  
**Market Size:** Young travelers and students aged 18-30 looking for budget planning tools.  
**Competitive Advantage:** Editable, community-curated plans vs. static review sites.  
**Sustainability:** Low hosting costs and scalable UGC model enable continuity beyond course.

---

## Steel-Man Discussion (Round 3)

**Idea A Steel-Man:** TripTuner — Collaborative travel itinerary platform using crowd aggregation and weighted feedback for ranking.  
**Idea B Steel-Man:** CrowdBudget — Crowdsourced budget-optimization tool for college students.  

**Why We Chose This Idea:** TripTuner offered clearer task boundaries, stronger intrinsic motivation, and broader real-world appeal.  
**What We Agreed On:** Focus on 3-5 destinations for pilot; emphasize aggregation and gamified feedback loop.  
**What Concerns Emerged:** Recruiting enough participants and managing moderation load.  
**Key Insights:** Gamification and Reddit integration drive free, sustainable participation without monetary rewards.

---

## Implementation Timeline (Optional)

**Week 1-2:** Design UI, set up Firebase and database.  
**Week 3-4:** Develop submission form and voting system.  
**Week 5-6:** Pilot launch with 3 destinations; collect votes and feedback.  
**Week 7-8:** Analyze data, refine ranking algorithm, add visualizations.

---

## Additional Notes

We collaborated with a total of 3 pairs, because 1 pair wasn't able to find another pair to partner with.

---

## References & Inspiration

1. Wikivoyage Open Travel Dataset  
2. TripAdvisor Developer API  
3. NETS 2130 Projects (Fun Facts, Loopify) 
