# V2 Viability Analysis: Auralynx (Round 2 - DROPPED)

## Project Summary
**Auralynx** - A gamified platform comparing how humans vs. AI perceive voices (accent, age, emotion, native language)

**Authors:** Alexander Budko, Sofiia Kikaleishvilli, Anton Bakhurov

---

## Viability Score Assessment

### 1. Technical Feasibility: 2/5
**Score: Very Risky**
- Audio ML pipeline with multiple pretrained models (accent, age, emotion, language detection)
- Browser-based audio capture with preprocessing (SNR filtering, length validation)
- Complex tech stack: Flask/FastAPI, React, Firebase, Hugging Face, SpeechBrain, Web Audio API, MTurk API
- Real-time ML inference on audio clips
- **Red flags:** Complex ML integration, audio processing pipeline, multiple external models

### 2. Crowdsourcing Viability: 3/5
**Score: Moderate Value**
- "Beat the AI" has intrinsic appeal
- But requires two distinct crowds: speakers AND guessers
- Cold-start problem: need enough recordings before guessers have content
- Value proposition unclear for speakers (why record yourself?)
- Guessers get gamified fun, but may lose interest quickly

### 3. Incentive Design: 3/5
**Score: Acceptable**
- Gamification (leaderboards, badges like "Golden Ear", "Most Unexpected Voice")
- $100 budget for top performers
- Task time: Speakers ~2 min, Guessers ~1 min per clip
- Intrinsic motivation ("beat the AI") is good but may not sustain long-term
- Weak incentive for speakers (no clear benefit to being recorded/judged)

### 4. Scope Appropriateness: 2/5
**Score: Overscoped**
- 8 key features including perception analytics dashboard, bias measurement engine, open-data export
- Complex dual-mode system (AI + human + ground truth)
- Requires integrating multiple pretrained ML models
- Privacy controls, leaderboards, reliability scoring, weighted voting
- This is effectively building a research platform in 5 weeks
- **Reality check:** Could core loop work in 2 weeks? Unlikely with ML integration

### 5. Recruitment Strategy: 3/5
**Score: General Plan**
- "Social media and class networks" + "small MTurk batches"
- No specific channels named
- Needs 300-500 speakers AND 1,000-1,500 guessers
- Two-sided marketplace problem: need both groups simultaneously
- No evidence of testing recruitment

### 6. Quality Control: 4/5
**Score: Thoughtful**
- Gold-standard control clips with known traits
- Weighted reliability scores per guesser
- Audio length/SNR validation
- Statistical outlier detection
- Random audits
- Well thought-out QC mechanisms

**TOTAL SCORE: 17/30**

---

## Verdict: NEEDS MAJOR REVISION

This falls in the 15-19 range: "Project has multiple serious issues. Needs significant rethinking."

---

## Why Was It Dropped?

**Likely reasons:**

1. **Technical complexity too high** - Audio ML pipeline with multiple models is 3-4 week project alone
2. **Overscoped for timeline** - Building a research-grade perception-gap dataset platform in 5 weeks is unrealistic
3. **Two-sided marketplace risk** - Need both speakers and guessers; chicken-egg problem
4. **Unclear core value** - The research insight is interesting but the user value proposition is weak
5. **Budget mismatch** - Aiming for 300-500 speakers + 1,000-1,500 guessers on $300-400 budget with complex tech

**Evidence from proposal:**
- 8 features including "Bias measurement engine" and "Open-data export"
- Complex ML stack (Hugging Face, SpeechBrain, pretrained models)
- Massive scale needed (1,500+ total participants across two roles)
- Research-oriented rather than product-oriented

---

## Was This the Right Decision?

**YES - This was correctly dropped.**

**Reasoning:**
- Core technical risk (audio ML) alone scores 2/5 - very risky
- Combined with overscoping (2/5) and moderate viability (3/5), total is only 17/30
- The rubric explicitly states 15-19 = "Needs Major Revision" and "multiple serious issues"
- Even with revision, the fundamental technical complexity (audio + ML + multiple models) makes this unsuitable for 5-week timeline
- Two-sided marketplace dependency compounds the risk

**What would have made it viable:**
- Drop ALL ML components, use manual categorization by experts to create "AI" labels
- Focus on human perception only (just guessers + ground truth, no AI comparison)
- Reduce to 50-100 total participants
- Simplify to 3-4 core features
- Even then, audio handling is still risky for the timeline

---

## Hidden Gem Potential?

**MODERATE - This could have succeeded with MAJOR descoping**

**The gem inside:**
The core insight about perception gaps between AI/humans/reality is genuinely interesting and novel. The "tri-layer dataset" concept is research-worthy.

**What would it take to unlock it:**

1. **Pivot to simpler modality:**
   - Use text snippets instead of audio (guess age/background from writing style)
   - Or use profile photos instead of voice (still perception-gap, easier tech)

2. **Drop real-time ML:**
   - Pre-run AI predictions on a small fixed dataset before launch
   - System just presents AI's answer + audio + human guess interface
   - Reduces to CRUD app with voting mechanism

3. **Reduce scale dramatically:**
   - 50 recordings, 150 guesses (3 per recording)
   - Focus on proof-of-concept, not research-grade dataset

4. **Single-sided first:**
   - Pre-record all audio clips yourself (team of 3 records 50 clips)
   - Launch with guessing only
   - Eliminates cold-start and two-sided marketplace problem

**With these changes:** Could potentially score 22-24/30 (Weak GO)
- Technical: 4/5 (simple voting system)
- Viability: 4/5 (single task for users)
- Incentives: 3/5 (still gamified)
- Scope: 4/5 (focused on core loop)
- Recruitment: 3/5 (still general)
- QC: 4/5 (keeps good mechanisms)

**But:** The team seemed committed to the complex vision, making pivot unlikely. The sophisticated, research-oriented approach was both the project's strength (novelty) and fatal flaw (infeasible scope).
