# Round 4 Reflection: Final Project Decision

**Name**: Yuxuan Tian  
**PennKey**: ytian27  
**Date**: 11/11/2025  

---

## 1. What I Explored Today

_List the projects you seriously considered. Keep it brief._

| Project Name | Source | Key Takeaway (1 sentence) |
|--------------|--------|---------------------------|
| GatherMessageAI | Round 3 | Turning group chat intent into concrete plans is both socially valuable and technically feasible. |
| CrowdScout | Round 2 | Interesting concept, but too dependent on large-scale data and external participants. |
| Loopify | Instructor | Focused on habit formation but less personally compelling or feasible within a semester. |

**Resources I used**:
- [x] Rubric scoring (RUBRIC-PROJECT-VIABILITY.md)  
- [x] V2 detailed analyses (reports/v2-analyses/)  
- [x] Steelman Analysis pathways (STEELMAN-ANALYSIS.md)  
- [x] Group discussions  

---

## 2. My Decision

**Project Name**: GatherMessageAI  

**Decision type**:
- [x] STAYING with Round 3 project (same approach)
- [ ] STAYING with Round 3 project (modified approach/scope)
- [ ] PIVOTING to different project
- [ ] JOINING another team's project

---

## 3. Why This Decision

I decided to continue with **GatherMessageAI** because it solves a genuine and relatable problem — the friction of making social plans — through a lightweight crowdsourcing model that naturally integrates into existing behavior. People already discuss plans in group chats but rarely follow through; this project converts that casual intent into structured, AI-assisted coordination.  

From a design perspective, GatherMessageAI strikes a balance between feasibility and creativity. It doesn’t depend on external labor markets but instead uses “microcrowds” — small, trusted social groups — to crowdsource decisions. It’s also a great opportunity to blend conversational AI, group behavior, and social UX in a space that people actually care about.  

**What convinced me:**
- Relatable use case with immediate utility.  
- Feasible to build within course constraints.  
- Naturally integrates crowdsourcing principles into social behavior.  

**What concerns me (and how I’ll address it):**
- **Low participation rates** → Implement reminders, light gamification, and peer visibility.  
- **Notification fatigue** → Keep UX minimal and allow manual triggers (e.g., `/gather`).  

---

## 4. What I'm Building

**One-sentence project description:**  
An AI assistant embedded in iMessage that turns casual group chat planning (“let’s grab dinner soon”) into structured polls and final decisions through crowdsourcing.  

**MVP Scope (3–4 core features):**
1. **Intent Detection:** Identify when a message implies planning intent.  
2. **Poll Generation:** Automatically create a simple availability and preference poll in-chat.  
3. **Consensus Aggregation:** Use weighted voting to find the best plan.  
4. **Follow-Up Automation:** Send reminders and final confirmations.  

**What I’m explicitly NOT building:**
- Passive monitoring of all chat messages.  
- Full recommendation engine.  
- Cross-platform integrations beyond iMessage (for MVP).  

---

## 5. Week 1 Validation

**The specific test I'll run Week 1:**  
- **Where:** My existing friend and sports group chats on iMessage.  
- **When:** Early next week (Monday–Wednesday evenings).  
- **What:** Post a “let’s meet up” message and manually simulate the GatherMessageAI workflow (send polls, track responses, finalize a time).  
- **Success metric:** ≥60% of participants respond to the poll and at least one event reaches consensus.  

**If Week 1 test fails, I will:**  
- [x] Pivot to a simpler polling interface (Google Form or lightweight web UI).  
- [ ] Try different recruitment channel (Slack or Discord groups).  
- [ ] Simplify decision flow to only time selection.  

---

## 6. **Tentative** Team

**Team members:**  
1. Yuxuan Tian (ytian27) – Backend / AI integration  
2. Hugo Song (songh8) – Frontend & iMessage Extension  
3. Ethan Xia (ethanxia) – Coordination logic & UX  

**Team status:**  
- [x] Same team from Round 3  
- [ ] New team formed during Round 4  
- [ ] Solo (will find teammates later)  
- [ ] Joining an existing team  

---

## 7. Reflection

**Most valuable part of Round 4:**  
Realizing that crowdsourcing can thrive within small, trusted networks — “microcrowds” — without needing large-scale external workers.  

**Biggest surprise:**  
How much coordination failure comes from indecision and friction, not lack of interest. Even small nudges and structure make a big difference.  

**One thing I'd tell future students about Round 4:**  
Pick a problem you personally experience — it makes testing, iteration, and motivation effortless.  

---

## Commitment

**I commit to:**  
- [x] Building the MVP scope above (3–4 features maximum)  
- [x] Running a concrete Week 1 validation test  
- [x] Pivoting if Week 1 shows <20% success  
- [x] Meeting with instructor if I hit major blockers  

**Signature:** _Yuxuan Tian_  
**Date:** _11/11/2025_  
