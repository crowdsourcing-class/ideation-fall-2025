# Crowdsourcing Project Idea: MoodMap@Penn

## Authors

**Original Author:** Tiffany Lian (tilian)

**Contributor:** Arriella Mafuta (arriella) and Veda Mantena (vmantena)

## Problem Statement

Penn students often struggle with high stress, burnout, and the social pressure to appear fine even when they are not. This culture, known as “Penn Face,” leads many to hide their emotions behind a sense of constant achievement and composure. MoodMap@Penn addresses this by allowing students to anonymously share how they are actually feeling, revealing that they are not alone and helping build a more open, supportive campus community.

## Target Audience

**Users:** Penn students, wellness organizations, and peer support groups.  
**Crowd workers:** Penn students who voluntarily submit their mood check-ins through the app. They represent the same population the system aims to help.

## Description

MoodMap@Penn is a crowdsourced mood-tracking platform that visualizes the collective emotional atmosphere across Penn’s campus. Students can log their current mood, add a short note or emoji, and tag their location. The system aggregates all check-ins into a color-coded heatmap that updates in real time, showing how different areas of campus “feel.” By making emotional data visible and anonymous, the project encourages empathy, reflection, and community awareness.

## Project Type

_Select the category that best fits your project:_

- [ ] Human computation algorithm
- [X] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 5-8 key features or capabilities of your system. Expand from Round 1:_

1. **Campus Mood Heatmap** showing live emotional trends by location.  
2. **Anonymous Mood Check-ins** with short notes or emojis.  
3. **Daily Streaks and Reflection Badges** to encourage consistent participation.  
4. **Anonymous Peer Comparison** to show students they are not alone.  
5. **Time Decay Function** that updates maps dynamically as moods change.  
6. **Data Dashboard for Wellness Groups** to identify areas of high stress.  
7. **Weekly Summary Insights** sent to participants.  
8. **Privacy and Verification System** using Penn email to ensure valid participation.

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
The emotional benefit of self-reflection and seeing community trends serve as intrinsic motivation. We can also include gamified streaks and badges.

**How much will it cost?**
Approx. $400–$500 total for hosting (Firebase, Mapbox API).

**Where will your data come from?**
User-generated mood entries collected directly from the Penn student crowd.

**How many crowd workers do you need?**
100s

## Technical Approach

**What are the main steps/components in your system?**

1. Student logs mood, emoji, and optional note.  
2. System collects and timestamps entry.  
3. Location data is clustered into campus zones.  
4. Aggregation algorithm computes average mood score per zone.  
5. Heatmap updates on the web interface.  
6. Weekly summaries and streak rewards are generated automatically.

**What parts are done by the crowd vs. automated?**
- Human: Mood submission, text input, and engagement.  
- Automated: Data aggregation, time decay, visualization, and streak tracking. 

**What technologies/tools will you use?**
Firebase (backend), React/Next.js (frontend), Mapbox or Leaflet (visualization), and Python for data aggregation scripts.

**How will you aggregate results from the crowd?**
Weighted averaging by mood type and time, removing outdated data automatically.

## Quality Control

**How will you ensure quality of crowd contributions?**

Require Penn email login to limit fake users, apply rate limits to prevent spam, users must choose from a selection of moods.

**Specific quality control methods:**
- [ ] Gold standard questions (test questions with known answers)
- [ ] Majority voting across multiple workers
- [ ] Expert review or verification
- [ ] Attention checks or trap questions
- [X] Reputation/qualification systems
- [ ] Statistical outlier detection
- [ ] Other: [specify]

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
Increased engagement, repeat participation, and visible diversity in mood data across campus.

**What would success look like quantitatively?**

- 100 unique users within first month  
- 70% repeat participation rate  
- Balanced distribution of mood entries across major campus areas  
- Positive feedback in post-use survey about feeling “less alone”

## Challenges & Mitigation Strategies

_For each challenge, propose a mitigation strategy:_

**Challenge 1:** Low participation due to stigma around emotional sharing.  
**Mitigation:** Keep data anonymous, use inclusive language, and promote through trusted student groups.  

**Challenge 2:** Inaccurate or joke submissions.  
**Mitigation:** Require Penn login, apply rate limits, and filter statistical outliers.  

**Challenge 3:** Sustaining engagement over time.  
**Mitigation:** Add streaks, badges, and periodic campus-wide mood challenges to maintain interest.  

## Prior Work

_Are there similar projects or systems? How is yours different?_

[Describe similar work and what makes your approach unique or improved]

**Specific related projects:**

- **Mappiness (LSE):** Collected large-scale mood data but lacked a localized or community focus.  
- **SafePaths Crowd (Fall 2024):** Focused on perceived safety rather than emotional well-being.  

MoodMap@Penn differs by targeting a single, emotionally charged campus environment with a social goal—reducing isolation and promoting empathy among peers.

## Discussion Notes from Round 2

**What did you agree on?**
Focus on simplicity and emotional transparency; emphasize Penn Face as the core motivator.

**What concerns or pushback emerged?**
Possible privacy and data misuse concerns; ensuring anonymity is key.

**Why is this idea promising?**
It addresses a real social issue on campus with low technical overhead and strong intrinsic motivation.

**What makes this sustainable and feasible?**
Small scope, low cost, simple technology stack, and clear emotional benefit to participants make it realistic within course constraints.  

## Additional Notes

MoodMap@Penn can partner with Penn Wellness, CAPS, or student mental health initiatives to increase participation and ensure responsible data use. Future expansions could include weekly sentiment summaries or cross-campus comparisons.
