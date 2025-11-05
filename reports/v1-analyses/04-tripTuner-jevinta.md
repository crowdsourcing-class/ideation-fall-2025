# TripTuner - Adversarial Analysis (V1)

**Authors**: Jevin Ta (jevinta), Nikki Liu (nikkiliu), Julia Zhuo (juzhuo), Arushi Agarwal (arushiga), Liana Veerasamy (lianav), Sadia Rahman (rsadia)

## EXECUTIVE SUMMARY
Well-documented travel itinerary crowdsourcing platform with clear structure and thoughtful features, but fatal flaw: weak incentive design for creative, high-effort task. Team hasn't adequately addressed why strangers would spend 15-30 minutes crafting detailed itineraries for imaginary travelers.

## VERDICT: WEAK GO

**Main Issue**: Asking for CREATION (hard, 20-30 min) but offering BADGES (worthless). Budget backwards: paying for votes ($0.05) while expecting itineraries for free.

**Critical Flaws**:
- High-friction task (create itinerary) with low-value rewards (badges)
- Vague recruitment ("Reddit communities")
- 100-200 worker target unrealistic with weak incentives
- AI/NLP features are premature optimization
- Competing with abundant existing solutions

**Strengths**:
- Specific numbers throughout (budget, metrics, targets)
- Sophisticated QC (6 mechanisms specified)
- Thoughtful aggregation formula
- Appropriate technical scope (if features cut)

**Rating**: C- crowdsourcing (fatal incentive mismatch), B technical feasibility

**Three Paths Forward**:
1. Pivot to paid contributions ($3-5 per itinerary, 15-25 total)
2. Reduce task burden (single activity recs vs. full itineraries)
3. Accept seeding it yourselves (team creates 10-15 each)

**Most Critical Change**: Solve incentive problem or reduce task burden. Either pay for content creation, make task much lighter, or plan to generate content yourselves.

**Predicted Outcome**: Build platform weeks 1-3, realize week 4 Reddit doesn't care, MTurk week 4-5, demo with 25-30 itineraries (8 team + 10 MTurk + 5 friends). Grade: B+/A- for execution but weak crowdsourcing validation.
