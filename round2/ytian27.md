# Crowdsourcing Project Idea: GatherAI

## Authors

**Original Author:** Yuxuan Tian (ytian27)  
**Contributor:** Hugo Song (songh8)

---

## Problem Statement

Coordinating social gatherings among friends often fails because ideas get lost in chat threads and no one takes the lead to finalize plans. People casually suggest “we should get dinner” or “let’s do something next week,” but scheduling across multiple calendars and preferences becomes too time-consuming. *GatherAI* solves this problem by transforming casual group-chat intent into concrete, optimized plans through lightweight crowdsourced input.

---

## Target Audience

**Users:** Busy friends, classmates, coworkers, and roommates who frequently communicate via iMessage but struggle to actually coordinate hangouts.  
**Crowd workers:** The users themselves—the friends in each group chat who collectively contribute availability, preferences, and votes.

---

## Description

*GatherAI* is an AI-powered group-chat assistant that listens for social planning cues (e.g., “brunch this weekend?”) and automatically launches a micro-poll for availability, preferred activities, and locations. Friends simply reply in-line through iMessage or a web link; the system aggregates everyone’s responses to propose an optimal time and plan. By turning chat noise into structured crowdsourced data, *GatherAI* makes planning spontaneous, low-friction, and fun.

---

## Project Type

- [ ] Human computation algorithm  
- [x] Social science experiment with the crowd  
- [x] Tool for crowdsourcing (requesters or workers)  
- [ ] Business idea using crowdsourcing 

---

## Key Features

1. **iMessage Integration** – Detects planning cues and launches automatic mini-polls.  
2. **Crowdsourced Scheduling** – Collects each participant’s availability directly via text responses.  
3. **Activity Consensus** – Users suggest or vote on activities (“picnic,” “karaoke,” “game night”).  
4. **Smart Recommendations** – AI suggests times, venues, and activities based on preferences and past patterns.  
5. **Consensus Scoring** – Weighted aggregation algorithm chooses the plan with maximum overlap.  
6. **Follow-Up Automation** – Sends confirmation texts, reminders, and optional calendar invites.  
7. **Privacy-Preserving NLP** – Local parsing of chat content to detect planning intent without storing full message histories.  
8. **Gamified Feedback Loop** – Users get “Social Organizer” badges for initiating successful gatherings.

---

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**  
Friend groups using iMessage or similar messaging apps.

**What will they provide?**  
Availability responses, activity suggestions, and votes on proposed plans.

**What skills do they need?**  
Basic texting ability; no technical skill required.

**Do skills vary widely? How?**  
Yes—some users respond faster or propose better ideas. *GatherAI* tracks response reliability and weights input accordingly.

**How will you incentivize participation?**  
Intrinsic motivation (making real plans with friends), lightweight gamification (streaks / badges), and social payoff (successful events).  

**How much will it cost?**  
<$500 total using existing APIs:  
- OpenAI / GPT API credits (~$100)  
- Firebase or Supabase backend (free tier)  
- Twilio / iMessage integration (~$50)  
- Hosting / domain / misc. ($100)  
- Small user-testing incentives ($200)

**Where will your data come from?**  
User-generated responses and message metadata (availability, preferences). No full message storage.

**How many crowd workers do you need?**  
Tens per group chat; hundreds of total participants across small pilot groups.

---

## Technical Approach

**Main steps/components:**

1. Detect planning intent (“we should…” / “let’s hang out”) via lightweight NLP trigger.  
2. Generate quick poll (dates / times / activities).  
3. Collect user replies through text or link.  
4. Aggregate responses using weighted consensus scoring.  
5. Propose final plan + send follow-up confirmations.  
6. Log anonymized engagement data for improvement.

**Crowd vs. automated:**  
- *Human:* Providing preferences, confirming attendance, suggesting activities.  
- *Automated:* Intent detection, data aggregation, consensus computation, scheduling, and notifications.

**Technologies/tools:**  
Python (FastAPI backend), Twilio / Apple Messages API, Firebase or Supabase DB, OpenAI GPT API for text parsing, React frontend (optional web dashboard).

**Aggregation method:**  
Weighted majority voting (weights = reliability × response time). Algorithm maximizes overlap across time slots and activity votes.

---

## Quality Control

**How will you ensure quality of crowd contributions?**

- Validate replies using structured templates (“Fri 7 PM”, “Brunch Saturday”).  
- Reputation scoring for consistent responders.  
- Duplicate or incoherent responses filtered automatically.  
- Feedback loop: AI asks for clarification when uncertain.

**Specific quality-control methods:**  
- [ ] Gold standard questions  
- [x] Majority voting across multiple workers  
- [ ] Expert review or verification  
- [ ] Attention checks  
- [x] Reputation/qualification systems  
- [x] Statistical outlier detection  

---

## Evaluation & Success Metrics

**How will you know if your project succeeds?**  
High participation and successful plan generation indicate strong utility.

**Quantitative success metrics:**  
- ≥ 75 % of polls reach consensus within 24 hours  
- ≥ 80 % satisfaction from post-event survey  
- ≥ 100 unique users in first pilot month  
- Average response time < 1 hour per poll  
- < 5 % failed or abandoned planning threads

---

## Challenges & Mitigation Strategies

**Challenge 1:** Low response rate from users.  
**Mitigation:** Auto-reminders and gamified nudges (“You’re the last to reply!”).  

**Challenge 2:** Over-automation causing privacy concerns.  
**Mitigation:** Only parse lightweight message metadata and obtain explicit opt-in.  

**Challenge 3:** Ambiguous or conflicting preferences.  
**Mitigation:** Weighted voting + AI clarification prompts (“Would you rather do brunch Sat or Sun?”).  

---

## Prior Work

**Similar projects:**  
- **Reclaim.ai / Motion:** AI calendar tools for professionals; lack group-chat integration or preference polling.  
- **WeightIn** (2023 project) crowdsourced opinions through polls; *GatherAI* applies that polling mechanism to dynamic scheduling.  
- **Kinnect** (2024 project) leveraged intrinsic motivation for community engagement; *GatherAI* similarly depends on intrinsic social payoff.

**How it differs:**  
*GatherAI* focuses on spontaneous, conversational planning via natural language—no app downloads, no manual setup—transforming lightweight text input into collective decisions.

---

## Discussion Notes from Round 2

**What did you agree on?**  
- Focus on low-friction iMessage integration.  
- Keep NLP lightweight and privacy-preserving.  
- Pilot with 3–5 friend groups to test group-decision consensus.  

**What concerns or pushback emerged?**  
- Risk of false triggers or over-notification.  
- Balancing automation vs. user control in scheduling.  

**Why is this idea promising?**  
Because it solves a universal pain point—friends failing to coordinate plans—using small, natural crowds that already exist in group chats. It combines AI and human consensus seamlessly.

**What makes this sustainable and feasible?**  
Requires no external workforce, runs on free APIs, and naturally motivates participation since successful plans benefit the participants themselves.

---

## Additional Notes

Potential future directions:  
- Integrate with Google Calendar / Apple Calendar.  
- Add “Smart Venue Suggestions” via Yelp API.  
- Expand to Slack / Discord / WhatsApp groups.  
- Enable “micro-community analytics” (e.g., average time to plan across groups).  

