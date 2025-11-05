# Crowdsourcing Project Idea: MoodMap@Penn

## Authors

**Original Author:** Tiffany Lian (tilian)

**Round 2 Contributors:** Arriella Mafuta (arriella)

**Round 3 Contributors:** Veda Mantena (vmantena)

## Problem Statement

Penn students often struggle with high stress, burnout, and the social pressure to appear fine even when they are not. This culture, known as “Penn Face,” leads many to hide their emotions behind a sense of constant achievement and composure. MoodMap@Penn addresses this by allowing students to anonymously share how they are actually feeling, revealing that they are not alone and helping build a more open, supportive campus community.

## Target Audience

**End Users:** Penn students, wellness organizations, and peer support groups.

**Crowd Workers:** Penn students who voluntarily submit their mood check-ins through the app. They represent the same population the system aims to help.

**Stakeholders:** Penn students (primary users and contributors), Penn Wellness and CAPS staff, Student organizations focused on mental health (e.g., Active Minds), Course instructors and project developers, University IT and data privacy offices

## Description

MoodMap@Penn is a crowdsourced mood-tracking platform that visualizes the collective emotional atmosphere across Penn’s campus. Students can log their current mood, add a short note or emoji, and tag their location. The system aggregates all check-ins into a color-coded heatmap that updates in real time, showing how different areas of campus “feel.” By making emotional data visible and anonymous, the project encourages empathy, reflection, and community awareness.

## Project Type

_Select the primary category:_

- [ ] Human computation algorithm
- [X] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 8-10 key features or capabilities of your system:_

1. **Campus Mood Heatmap** showing live emotional trends by location.  
2. **Anonymous Mood Check-ins** with short notes or emojis.  
3. **Daily Streaks and Reflection Badges** to encourage consistent participation.  
4. **Anonymous Peer Comparison** to show students they are not alone.  
5. **Time Decay Function** that updates maps dynamically as moods change.  
6. **Data Dashboard for Wellness Groups** to identify areas of high stress.  
7. **Weekly Summary Insights** sent to participants.  
8. **Privacy and Verification System** using Penn email to ensure valid participation.
9. **Community Challenges and Events** that encourage collective participation during key times like midterms or Wellness Week.

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
Penn Students

**What will they provide?**
Short mood entries, optional notes, and location tags.

**What skills do they need?**
None beyond basic smartphone or web access.

**Do skills vary widely? How?**
No, the main focus is the selection of mood and map location, adding a detailed note is up to the user.

**How will you incentivize participation?**

1. **Drive 2: Development & Accomplishment**  
   - Daily Streaks and Reflection Badges reward consistent participation, giving users visible milestones and progress indicators.  
   - Progress bars and level icons reinforce a sense of mastery and achievement.  

2. **Drive 5: Social Influence & Relatedness**  
   - Anonymous Peer Comparison lets students see shared experiences, reducing stigma and isolation.  
   - Public community goals (e.g., “1,000 mood check-ins this week”) encourage a sense of collective progress.  

3. **Drive 1: Epic Meaning & Calling**  
   - The app’s purpose—fighting Penn Face and promoting emotional openness—creates an intrinsic reason to participate.  
   - Framing contributions as helping the community fosters empathy and purpose-driven engagement.  

4. **Drive 3: Empowerment of Creativity & Feedback**  
   - Users can express moods with emojis, color gradients, or short captions, giving creative freedom within the system.  
   - Seeing instant visual impact on the heatmap provides immediate feedback.  

5. **Drive 6: Scarcity & Impatience**  
   - Limited-time Campus Challenges (like “Midterm Check-in Week”) create short bursts of engagement.  
   - Unlockable reflection badges available only during special events boost participation frequency.  

6. **Drive 4: Ownership & Possession**  
   - Each user has a Personal Mood Journal tracking their own emotional history, creating a sense of personal value and attachment to the app.  

**Budget & Cost Analysis:**

- **Estimated cost per task:** $0.00 (voluntary participation; no paid microtasks)  
- **Estimated cost per worker:** ~$1.00 (raffle rewards or small Penn-themed incentives)  
- **Number of tasks needed:** ~500–800 mood check-ins across 200–300 students  
- **Total estimated budget:** **$300–$400**  
- **Justification:**  
  This budget covers Firebase hosting, Mapbox API usage, and small participation rewards. Because MoodMap@Penn relies on intrinsic motivation and gamified engagement rather than direct payments, most participation is voluntary. The total remains well within the $500 course constraint while providing enough incentive and technical support for meaningful participation.


**Where will your data come from?**
User-generated mood entries collected directly from the Penn student crowd.

**Scale Requirements:**
**Scale Requirements:**  
- **Minimum viable crowd size:** ~100 workers (enough to populate initial campus mood data and visualize basic trends)  
- **Target crowd size for full functionality:** ~300–500 workers (to cover major campus locations and generate meaningful daily patterns)  
- **Potential to scale to:** ~1,000+ workers (including students from all schools and residential communities at Penn)  

## Technical Architecture

**System Components:**

1. Frontend web interface (React/Next.js PWA with Mapbox/Leaflet)
2. Backend API (Firebase Cloud Functions or Node/Express)
3. Realtime database and auth (Firebase Firestore + Penn email/OAuth verification)
4. Analytics and aggregation pipeline (scheduled Cloud Functions / Python jobs for time-decay, geohash binning)
5. External services (Mapbox tiles, email notifications via SendGrid)

**Detailed Workflow:**

_Step-by-step description of how the system works:_

1. User signs in with Penn email, consents to anonymous participation, and opens the check-in form.
2. User submits mood rating, optional short note/emoji, and selects or confirms campus location.
3. Backend validates auth, applies rate limits, geohashes location, timestamps entry, and writes to Firestore.
4. Scheduled job computes time-decayed mood scores per geohash and filters outliers and spammy bursts.
5. Aggregation updates a cached dataset for the heatmap and peer-comparison summaries.
6. Frontend fetches the cached dataset and renders a live heatmap and user dashboard; streaks and badges update.
7. Weekly job generates summary insights, sends opt-in email digests, and refreshes the wellness dashboard export.

**Human vs. Automated Tasks:**

| Task                                              | Performed By | Why?                                                                                          |
| ------------------------------------------------- | ------------ | --------------------------------------------------------------------------------------------- |
| Submitting mood check-ins with notes and emojis   | Human        | Requires self-reflection, emotion recognition, and personal input that cannot be automated.   |
| Validating Penn email and storing submissions     | Automated    | Ensures secure participation and data integrity through authentication scripts.               |
| Aggregating and updating campus mood heatmap      | Automated    | Involves processing large datasets and applying time-decay calculations efficiently.          |
| Reviewing aggregated trends for wellness insights | Human        | Wellness staff and student leaders interpret results and take action based on human judgment. |

**Technologies & Tools:** 

- **Frontend:** React/Next.js with Tailwind CSS and Mapbox for interactive visualization  
- **Backend:** Node.js with Express and Firebase Cloud Functions for serverless operations  
- **Database:** Firebase Firestore for real-time data storage and user authentication  
- **ML/AI:** Python scripts for mood trend analysis and time-decay aggregation (optional extension)  
- **Crowdsourcing Platform:** Custom web-based platform built for Penn students (verified via Penn email login)  
- **Hosting:** Vercel for frontend deployment and Firebase Hosting for backend services  
- **Other:** SendGrid for weekly summary emails, GitHub for version control, and Google OAuth for authentication  


**Aggregation Method:**
**Aggregation Method (Simple):**

1. **Location binning:** Group check-ins by campus area (e.g., building or geohash cell).

2. **Score mapping:** Convert moods to numbers (example):  
   happy = +1, calm = +0.5, neutral = 0, stressed = −0.5, anxious = −1.

3. **Optional time decay:** Give recent check-ins more weight:  
   weight_time = exp(−Δt / τ), where Δt is hours since submission and τ is a half-life (e.g., 12 h).  
   If not using decay, set all weights to 1.

4. **Average per area:**  
   For each area, compute the weighted average:  
   score_area = Σ(score_i × weight_time_i) ÷ Σ(weight_time_i).

5. **Display:** Show score_area on the heatmap; optionally include count of check-ins for basic confidence.

## Quality Control

**Quality Control Strategy:**  
Because MoodMap@Penn collects self-reported emotional data, the focus is on preventing spam, false entries, and extreme outliers rather than judging “correctness.” Quality control relies on authentication, basic statistical filtering, and transparent aggregation to ensure valid, representative data while maintaining anonymity.

**Specific QC Mechanisms:**

- [ ] Gold standard questions (test questions with known answers)  
  - _Details:_ Not applicable since mood is subjective and there are no “right” answers.  

- [ ] Majority voting across multiple workers  
  - _Details:_ Not used; instead, the system averages all entries within a location/time window.  

- [ ] Expert review or verification  
  - _Details:_ Wellness staff may occasionally review aggregated trends for anomalies or misuse.  

- [ ] Attention checks or trap questions  
  - _Details:_ Light rate-limiting and location validation prevent repeated spam submissions.  

- [x] Reputation/qualification systems  
  - _Details:_ Only verified Penn email accounts can submit, limiting fake data. Each account can only post a few times per day to prevent manipulation.  

- [x] Statistical outlier detection  
  - _Details:_ System filters sudden bursts or extreme values using time-based thresholds and simple outlier checks.  

- [ ] Redundancy and agreement metrics  
  - _Details:_ Agreement ensured implicitly through averaging multiple check-ins per area.  

- [x] Other: Time-based decay and smoothing  
  - _Details:_ Older check-ins gradually lose weight in the average, keeping data current and reducing long-term bias.

**Handling Low-Quality Work:**  
If low-quality or spam submissions are detected, the system flags and removes them automatically from aggregation. Entries from flagged users are rate-limited or hidden from the map. Since all participants are verified Penn users, there are no formal penalties—just automatic filtering and soft restrictions to preserve data integrity.

## Evaluation & Success Metrics

**Primary Success Metrics:**

1. **Participation Rate:** At least 100 verified Penn students contributing mood check-ins during the pilot phase (measured via unique Penn logins).  
2. **Engagement Consistency:** 60% of users completing 3+ check-ins per week (tracked through streak data).  
3. **User Impact:** 80% of survey respondents reporting that MoodMap@Penn made them feel more connected or less alone (post-use feedback form).

**Evaluation Methodology:**  
- Collect usage logs (check-ins per user, session duration, streaks).  
- Conduct a post-pilot survey assessing usability, emotional impact, and perceived value.  
- Use descriptive statistics to compare engagement trends over time.  
- Optionally, run a small A/B test: one group sees the heatmap; the other only personal mood logs.

**Baseline Comparisons:**  
- Compare to no-tool baseline (self-reported student mood awareness from survey).  
- Measure improvement via increase in self-reported connection and frequency of reflection.

**Success Criteria:**  
- **Minimum viable success:** 100 participants with consistent daily check-ins for one week.
- **Target success:** 300+ participants and 60% repeat engagement.  
- **Stretch success:** 500+ participants and integration with Penn Wellness outreach efforts.

---

## Challenges & Mitigation Strategies

**Challenge 1:** Low participation or initial adoption.

- **Why it's a risk:** Without enough users, data will look empty and lose value.  
- **Mitigation strategy:** Partner with student orgs, advertise on social media, and promote during Wellness Week.  
- **Backup plan:** Launch targeted dorm or school-specific pilots first to build data density.

**Challenge 2:** Privacy concerns and data sensitivity.  
- **Why it's a risk:** Students may hesitate to share emotional data, even anonymously.  
- **Mitigation strategy:** Anonymize all entries, require no personal data, and clearly communicate privacy measures.  
- **Backup plan:** Allow “private mode” where users only see personal trends but still contribute anonymously.

**Challenge 3:** Data skew or spam entries.  
- **Why it's a risk:** Inaccurate mood reports could distort heatmaps.  
- **Mitigation strategy:** Use Penn email verification, limit submissions per user, and apply outlier filtering.  
- **Backup plan:** Enable manual review or temporary data resets if spam occurs.

**Challenge 4:** Sustaining engagement after novelty fades.  
- **Why it's a risk:** Participation may drop once the initial excitement wears off.  
- **Mitigation strategy:** Introduce recurring challenges, streak resets, and new seasonal badges.  
- **Backup plan:** Integrate data visualization into campus wellness newsletters or Instagram updates.

---

## Prior Work & Related Projects

**Similar Existing Systems:**

1. **Mappiness (LSE)**  
   - **Description:** A mobile app tracking users’ happiness across time and location.  
   - **Similarities:** Collects self-reported mood and geolocation data.  
   - **Differences:** National focus and paid participants; MoodMap@Penn is local, anonymous, and community-driven.  
   - **Citation:** MacKerron, G. (2012). Mappiness Project.  

2. **SafePaths Crowd (Fall 2024 Penn Project)**  
   - **Description:** Mapped perceived safety levels around campus.  
   - **Similarities:** Used crowdsourced, subjective data from students.  
   - **Differences:** Focused on safety perception, not emotional well-being.  

3. **Be My Eyes**  
   - **Description:** A global volunteer network connecting sighted users with visually impaired people for assistance.  
   - **Similarities:** Leverages empathy-driven crowdsourcing.  
   - **Differences:** Provides direct human assistance rather than data visualization.

**Lessons from Past Course Projects:**  
Many past projects failed to sustain crowd engagement because they lacked intrinsic motivation or visible community impact. MoodMap@Penn addresses this by making participation personally meaningful and socially visible through emotional awareness and gamified feedback.

---

## Ethical Considerations

**Potential Ethical Issues:**  
- Privacy concerns with emotional and location data.  
- Risk of emotional triggering when viewing negative trends.  
- Misuse of data by non-wellness entities.

**Mitigation Strategies:**  
- Use anonymous submissions and general area mapping (no pinpoint GPS).  
- Provide on-screen disclaimers and mental health resources (CAPS link).  
- Restrict raw data access to verified project admins and wellness staff only.

**IRB Considerations:**  
IRB review may be required if data is used for research or publication since it involves emotional self-reporting. For classroom use only, anonymization and non-identifiable aggregation should be sufficient to avoid full review.

---

## Business Viability (Optional)

**Revenue Model:**  
Potential partnership with universities or wellness offices offering annual licensing for campus mood dashboards.

**Market Size:**  
Target market includes universities and mental health programs seeking community-based wellness tools.

**Competitive Advantage:**  
Localized, community-driven design with high trust due to Penn verification and clear wellness purpose.

**Sustainability:**  
Could be sustained by student wellness groups or integrated into Penn’s existing digital wellness infrastructure.

---

## Steel-Man Discussion (Round 3)

**Idea A Steel-Man:** A data visualization system for emotional mapping across universities.  
**Idea B Steel-Man:** A campus-level wellness journal with private reflection tools.  
**Why We Chose This Idea:** MoodMap@Penn combines the strongest parts of both—collective awareness (A) and private reflection (B)—while staying achievable within the course scope.  
**What We Agreed On:** Keep it anonymous, lightweight, and community-focused.  
**What Concerns Emerged:** Privacy management, data interpretation accuracy.  
**Key Insights from Round 3 Discussion:** Simplicity and purpose-driven design sustain engagement better than complex technical features.

---

## Implementation Timeline (Optional)

**Week 1-2:** Design UI wireframes and set up Firebase backend.  
**Week 3-4:** Build frontend and integrate Mapbox for heatmap display.  
**Week 5-6:** Test with small group of students, refine submission and decay logic.  
**Week 7-8:** Full campus soft launch, collect feedback, and generate initial summary reports.

---

## Additional Notes

- Could integrate with Penn Wellness newsletters or push notifications.  
- Future feature: sentiment analysis of optional text notes for deeper insights.

---

## References & Inspiration

1. MacKerron, G. (2012). *Mappiness Project*. London School of Economics.  
2. Be My Eyes (2023). *Empathy-driven volunteer platform*.  
3. Penn Wellness (2024). *Student mental health initiatives and engagement reports*.  
