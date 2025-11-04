# AgriAid - Adversarial Analysis (V1)

**Authors**: Nikki Liu (nikkiliu), Jevin Ta (jevinta), Brandon Yan (bdonyan)

## EXECUTIVE SUMMARY
Earnest, well-intentioned project with strong social impact potential, but fundamental viability issues: volunteer recruitment strategy unrealistic, task requires expert knowledge they claim isn't needed, 5-week timeline severely underestimates satellite data infrastructure complexity. Most critically, building "human-AI hybrid" where modern NDVI/ML systems already outperform untrained humans at crop stress detection.

## VERDICT: WEAK GO - Needs Major Pivot

**Main Issue**: Fundamental expertise mismatch - if automated systems with NDVI/ML miss subtle signs, how will untrained undergrads spot them? The task requires domain knowledge contradicting their claim of "basic visual recognition."

**Critical Flaws**:
- Volunteer recruitment fantasy (50-100 workers from WHERE specifically?)
- Catastrophic scope underestimation (GEE API, geospatial processing, NDVI = month-long work)
- Weak gamification as retention solution
- LLM elephant not addressed (why not GPT-4 Vision?)
- Scale requirements disconnect (10,000 tiles × 5 workers = 1,667 hours of volunteer work)
- No gold standard dataset creation plan

**Strengths**:
- Specific numbers throughout (budgets, metrics)
- Detailed QC mechanisms beyond platitudes
- Honest challenge identification
- Prior work research
- Clear success criteria

**Rating**: C+ crowdsourcing (frameworks cited but incentives broken), C technical feasibility

**Alternative Pivot**: Human-AI hybrid where AI flags suspicious regions, humans verify (reduces volunteer load 90%). Or local expert networks in affected regions (not Penn students) providing ground truth.

**Most Critical Change**: Validate recruitment FIRST. Post in one Discord/Reddit with 10 sample tiles. If <20% complete them (likely), pivot scope to match realistic recruitment.

**Predicted Outcome**: Weeks 1-3 building satellite pipeline, week 4 realize no volunteers, label yourselves, demo with 200 labels (team + friends). Technical elegant, crowdsourcing thin. Grade: B for effort.
