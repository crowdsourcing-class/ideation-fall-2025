# V2 Analysis: MicroProof

## Project Overview
**Author:** Omar Pareja (pareja)
**One-line pitch:** A micro-fact-checking platform where residents verify or debunk local claims with on-the-ground photo and video evidence.

## Quick Viability Score: 24/30

### Score Breakdown (Estimated from Round 1)
- **Problem-Solution Fit (8/10):** Addresses real issue of unverified local claims spreading on social media. Hyperlocal fact-checking gap exists.
- **Crowdsourcing Fit (9/10):** Excellent crowdsourcing mechanics - claim submission, physical verification, photo evidence, cross-validation. Strong multi-stage workflow.
- **Technical Feasibility (7/10):** Solid tech plan (Firebase, Google Maps API, Flask/Vercel) under $300. Geo-validation and EXIF checks are feasible but require careful implementation.

### Strengths
1. **Sophisticated QC Design:** Credibility scoring based on historical accuracy, geo-tag validation, EXIF timestamp checks, 2+ confirmations required
2. **Physical Verification:** Requires on-the-ground evidence (photos/video), not just opinions - higher quality bar
3. **Clear Value Proposition:** Restores trust in local information through collective verification
4. **Thoughtful Aggregation:** Weighted consensus combining evidence count, user credibility, and time decay
5. **Strong Prior Work Analysis:** References Fun Facts (2024), WeightIn, and learned from past projects
6. **Real Social Impact:** Reduces community misinformation at neighborhood scale

### Weaknesses
1. **Geographic Dispersion:** Requires critical mass in each neighborhood; can't pool contributions across cities
2. **Verification Burden:** Physical verification takes significant time/effort - higher friction than online tasks
3. **Gaming Concerns:** Coordinated groups could manipulate local claims if not enough diverse verifiers
4. **Photo Manipulation:** Despite EXIF checks, photos can be faked or misleading (old photos of closed business)
5. **Scope Creep Risk:** "Bus line canceled" vs. "road flooded" vs. "restaurant closed" - very different verification complexities

### Critical Questions
- **Response Time:** How quickly can crowd verify claims? If bus is "canceled," claim is only useful if verified in <30 min
- **Incentive Design:** Why would people physically go verify claims? What's the motivation beyond civic duty?
- **Cold Start:** Need many verifiers in same area; starts empty and stays empty without critical mass
- **Claim Sourcing:** Who posts claims? Manual entry or automated scraping? Scraping adds complexity

## Why Was This Dropped?

**Most Likely Reasons:**
1. **Geographic Fragmentation:** Each neighborhood is its own crowd; can't pool contributors across regions
2. **High Friction Tasks:** Physical verification is harder than online clicking; participation concerns
3. **Unclear Immediate Value:** Users don't get personal benefit from verifying claims (unlike personal productivity apps)
4. **Time Sensitivity:** Local claims (bus canceled, road flooded) expire quickly; verification must be rapid
5. **Scope Ambiguity:** "Local claims" is broad - restaurant closures vs. emergency situations have very different requirements

## Was This the Right Decision?

**Verdict: BORDERLINE - Could Have Progressed with Narrower Scope**

**Arguments for Dropping:**
- **High task friction:** Physical verification is much harder than online tasks
- **Geographic constraints:** Requires critical mass in specific neighborhoods
- **Time sensitivity:** Many claims need rapid verification (bus canceled NOW)
- **Unclear incentives:** Why would strangers verify claims for others?
- **Cold start problem:** Empty map until sufficient contributions

**Arguments Against Dropping:**
- **Excellent crowdsourcing design:** Multi-stage workflow, credibility scoring, evidence-based verification
- **Real social value:** Hyperlocal misinformation is genuine problem
- **Differentiates from past work:** Physical evidence requirement is novel
- **Strong technical plan:** Realistic budget, clear automation strategy
- **Demonstrates course concepts:** Quality control, aggregation, incentive design

**The Key Issue: Scope and Incentives**

The project shows sophisticated understanding of crowdsourcing principles but struggles with:
1. **Motivation:** Why verify claims that don't directly benefit you?
2. **Specificity:** "Local claims" is too broad - need to focus on one claim type
3. **Time constraints:** Many hyperlocal claims need instant verification

**Hidden Gem Potential:** MEDIUM-HIGH

This is a well-designed crowdsourcing project that likely got dropped for execution concerns rather than conceptual flaws. The quality control mechanisms are sophisticated, and the evidence-based approach is strong.

## What Could Have Saved It

**More Focused Scope:**
- Focus ONLY on business closures/openings (less time-sensitive than bus cancellations)
- Start with Penn campus only (dining halls, study spaces, building hours)
- Frame as "campus status updates" rather than "fact-checking"

**Better Incentive Design:**
- Contributor leaderboard with campus recognition
- Small gift card raffles for weekly top contributors
- Frame as "help fellow students" rather than "combat misinformation"
- Show contributor's impact (X people used your verification)

**Lower Friction:**
- Allow text-only reports ("I'm at the bus stop, no bus came")
- Make photo optional enhancement rather than requirement
- Reduce verification burden (1 confirmation instead of 2 for low-stakes claims)

## Comparison to Progressed Projects

**Similar successful project: bdonyan (TerraTruth)**
- Also requires physical verification (wait times at dining halls/gyms)
- Also uses photos and GPS validation
- Narrower, more specific use case (just wait times, not all local claims)
- Clearer personal benefit (students save time by checking wait times)

MicroProof is more ambitious and sophisticated but less focused. If it had narrowed to campus-specific claims with clear student benefit, it might have progressed.

## Lessons for Future Selection

- **Sophisticated QC != Guaranteed Success:** Well-designed projects can still fail on incentives or scope
- **Physical tasks need strong motivation:** Online clicking is easy; going somewhere to verify is hard
- **Scope matters:** "Local fact-checking" is broad; "campus dining hall status" is focused
- **Personal benefit drives participation:** Projects that save users time/effort engage better than pure civic duty
- **Time sensitivity is challenging:** Real-time verification requirements add significant complexity

**Conclusion:** MicroProof deserved serious consideration and possibly could have progressed with a narrower scope (campus-only) and stronger incentive design. The underlying crowdsourcing mechanics are sound, but the broad "hyperlocal fact-checking" framing may have seemed too ambitious. This is a borderline case where the decision could have gone either way.
