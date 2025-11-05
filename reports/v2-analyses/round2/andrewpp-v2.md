# V2 Viability Analysis: TrashTag Tracker (Round 2 - DROPPED)

## Project Summary
**TrashTag Tracker** - A crowd-powered platform for reporting and verifying trash hotspots to guide community cleanup efforts

**Authors:** Jun Hyun Park (andrewpp), Eric Lee

---

## Viability Score Assessment

### 1. Technical Feasibility: 3/5
**Score: Challenging but Doable**
- Photo upload with GPS tagging
- Spatial clustering of reports
- Duplicate detection (likely using computer vision APIs)
- Mapbox/OpenStreetMap integration
- Firebase/Supabase backend
- **Moderate complexity:** Not just CRUD, involves mapping + image analysis
- Computer vision for duplicate detection could be tricky

### 2. Crowdsourcing Viability: 3/5
**Score: Moderate Value**
- Environmental/social good has intrinsic appeal
- But requires active participation (taking photos, verifying)
- Value accrues to community, not individual user
- Gamification helps but may not sustain long-term
- Similar to "volunteer cleanup" - some people care, many don't

### 3. Incentive Design: 3/5
**Score: Acceptable**
- Intrinsic motivation (helping environment)
- Gamification: badges, streaks, leaderboards
- Potential partnerships with campus orgs for rewards
- Task time: ~2-5 minutes to photograph and submit
- Social impact visible through map updates
- **Weakness:** No immediate personal benefit, relies on altruism

### 4. Scope Appropriateness: 4/5
**Score: Slight Stretch**
- 5 key features listed (reasonable)
- Photo + GPS submission, verification workflow, live map, gamification, duplicate detection
- Core loop is manageable: submit photo → others verify → map updates
- Could build working demo in 2 weeks
- Some features (duplicate detection, spatial clustering) add complexity but not insurmountable

### 5. Recruitment Strategy: 2/5
**Score: Vague Hope**
- "Volunteers from campus community, social media outreach, environmental clubs"
- No specific clubs or channels named
- "Partnerships with campus orgs" is aspirational, not concrete
- No evidence of testing recruitment or securing commitments
- Depends on people caring enough to participate

### 6. Quality Control: 4/5
**Score: Thoughtful**
- Redundant validation for all submissions
- Reputation/trust scoring per user
- Automated flagging of suspicious uploads
- Weighted majority voting
- Multiple independent confirmations for cleanup verification
- Well-designed multi-layered approach

**TOTAL SCORE: 19/30**

---

## Verdict: NEEDS MAJOR REVISION

This falls at the top of the 15-19 range: "Project has multiple serious issues. Needs significant rethinking."

Borderline with 20-24 "Weak GO" territory.

---

## Why Was It Dropped?

**Likely reasons:**

1. **Uncertain user motivation** - Relies entirely on volunteers caring about litter cleanup
2. **Weak recruitment plan** - No concrete path to 100-300 active contributors
3. **Behavioral assumption** - Assumes people will consistently photograph trash and verify others' reports
4. **Limited personal value** - Community benefit doesn't translate to individual incentive
5. **Competing priorities** - Students have many demands on their time; litter tracking is low priority

**Evidence from proposal:**
- Recruitment: "social media outreach, environmental clubs" (vague)
- Incentives: Gamification and "positive social impact" (weak for tedious task)
- Discussion notes acknowledge: "Ensuring enough users consistently verify hotspots rather than only submitting them"
- This verification bottleneck was identified but not solved

---

## Was This the Right Decision?

**MAYBE - This was a borderline call.**

**Arguments FOR dropping:**
- Scores only 19/30, just barely in "Needs Major Revision"
- Weakest dimensions (Viability: 3/5, Recruitment: 2/5, Incentives: 3/5) are hard to fix
- Similar civic-tech projects struggle with sustained engagement
- Environmental action apps have low retention rates unless mandated

**Arguments AGAINST dropping:**
- Technical feasibility is reasonable (3/5)
- Scope is appropriate (4/5)
- Quality control is thoughtful (4/5)
- With better recruitment strategy, could reach 20-22 range (Weak GO)
- Social good angle could attract passionate niche audience

**What tipped the scales:**
The combination of:
1. Weak recruitment plan (no specific channels)
2. Unvalidated assumption about user motivation
3. Verification bottleneck acknowledged but unsolved
4. No evidence of testing the concept with potential users

**Better projects likely existed** that scored higher or had clearer paths to success.

---

## Hidden Gem Potential?

**MODERATE-TO-HIGH - This could have succeeded with better execution and targeting**

**The gem inside:**
- Clean problem statement
- Reasonable technical scope
- Well-thought-out quality control
- Clear value to community (if adoption happened)
- Positive social impact narrative

**What would unlock it:**

1. **Hyper-local launch:**
   - Focus on ONE specific area: "Penn campus only"
   - Partner with ONE org: Facilities Services or Green Fund
   - Get official backing: "Help us map trash for grounds crew"
   - Turns it from volunteer project to official campus initiative

2. **Flip the incentive:**
   - Make it competitive between dorms/buildings
   - Monthly prize for cleanest area or most-improved
   - Turns social good into tangible reward
   - Leverages existing dorm communities

3. **Simplify verification:**
   - Don't require crowd verification
   - Just report → auto-added to map → facilities checks periodically
   - Reduces friction massively
   - Shifts burden from crowd to small expert team

4. **Concrete recruitment:**
   - Actually approach 3-5 environmental clubs BEFORE building
   - Get commitments from club leaders to participate
   - Seed with their members (30-50 people committed day 1)
   - Eliminates recruitment uncertainty

5. **Proof before platform:**
   - Week 1: Create simple Google Form + manual map
   - Test with 20 friends: will they actually submit trash photos?
   - If yes → build platform
   - If no → pivot immediately

**With these changes:** Could score 22-24/30
- Technical: 3/5 (unchanged)
- Viability: 4/5 (official backing + simplified)
- Incentives: 4/5 (competitive element)
- Scope: 4/5 (unchanged)
- Recruitment: 3/5 (still general, but tested)
- QC: 4/5 (unchanged)

**Key insight:** The proposal was well-structured and thoughtful, but lacked the critical element of VALIDATION. They never tested whether anyone would actually use this. A single week of testing with a Google Form would have either:
- Proven demand → strengthen the proposal
- Revealed lack of interest → pivot early

**Bottom line:** Not a hidden gem in its submitted form, but had solid bones. With entrepreneurial hustle (partnerships, testing, pivoting), could have become viable. The team seemed to design carefully but execute cautiously - the opposite of what's needed for crowdsourcing projects.
