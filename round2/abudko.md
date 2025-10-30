# Crowdsourcing Project Idea: Auralynx

*Aural* = relating to hearing; *Lynx* = a sharp-eared predator — a metaphor for a system with acute auditory perception.

## Authors

**Original Author:** Alexander Budko (abudko)  
**Contributor:** Sofiia Kikaleishvilli, Anton Bakhurov

---

## Problem Statement

Speech-based AI systems often fail to accurately interpret who is speaking, their emotional tone, or their linguistic background. Models trained on limited datasets struggle with accents, age diversity, and expressive variation, leading to biased performance in real-world use. Human listeners also make subjective judgements about a voice — but we lack a large-scale dataset comparing how *AI* and *people* perceive the same voice relative to ground truth. This limits our ability to design fairer and more perceptive voice technologies.

---

## Target Audience

- **Users / Researchers:** Speech recognition and language-technology researchers, sociolinguists, and AI fairness experts seeking perception-gap data.  
- **Crowd Workers:**  
  - **Speakers:** Anyone with a microphone who records short voice clips.  
  - **Guessers:** Online participants (e.g., MTurk workers, volunteers, or students) who listen to the recordings and make structured predictions about speaker traits.

---

## Description

**Auralynx** is a gamified crowdsourcing platform that compares how humans and AI perceive voices.  
Speakers record a short prompted phrase (5–8 seconds). The system’s AI model immediately predicts specific traits — *accent region, age bracket, emotional tone,* and *native language category*. Human guessers listen to the same clip and make their own predictions. The speaker then self-reports their true traits.  
Auralynx aggregates all three layers — **Actual → AI → Human** — revealing where machine and human perception diverge. The process feels like a quiz game but yields valuable bias-and-fairness data for voice AI research.

---

## Project Type

- [x] Social science experiment with the crowd  
- [x] Human computation algorithm  
- [ ] Tool for crowdsourcing  
- [ ] Business idea using crowdsourcing  
- [ ] Other

---

## Key Features

1. **Dual-mode feedback:** AI and human guessing on the same voice sample for side-by-side comparison.  
2. **Standardized prompts:** Fixed short phrases ensure uniform acoustic input across speakers.  
3. **Gamified interface:** Leaderboards, streaks, and “Golden Ear” badges reward accurate guessers; “Most Unexpected Voice” badges reward surprising speakers.  
4. **Perception analytics dashboard:** Visualizes where AI or humans systematically misjudge accent, emotion, or age.  
5. **Bias measurement engine:** Quantifies “perception gaps” between AI, crowd consensus, and self-reported truth.  
6. **Open-data export:** Produces anonymized perception datasets for future research.  
7. **Lightweight tech stack:** Browser-based audio capture, open-source ML models, free cloud hosting.  
8. **Privacy controls:** Optional trait disclosure and anonymized audio IDs.

---

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**  
Volunteers and students recruited through social media and class networks, plus small MTurk batches to scale the guesser pool.

**What will they provide?**  
Speakers: recorded short phrases + self-reports.  
Guessers: categorical labels for accent region, age bracket, emotional tone, and native-language category.

**What skills do they need?**  
Basic listening comprehension and internet literacy; no domain expertise required.

**Do skills vary widely? How?**  
Yes. Some guessers have better accent familiarity or emotion recognition; the system tracks reliability and weights their votes higher.

**How will you incentivize participation?**  
Gamification (leaderboards, badges), intrinsic motivation (“beat the AI”), and small rewards ($100 budget for top performers or gift cards).

**How much will it cost?**  
- MTurk seed data collection: ~$200  
- Prizes & recognition: ~$100  
- Hosting / storage (Firebase free tier): ~$0–$20  
- Total budget: **≈ $300–$400**

**Where will your data come from?**  
User-generated recordings collected via web interface; AI predictions generated from open-source pretrained voice models (e.g., Hugging Face, PyTorch SpeechBrain).

**How many crowd workers do you need?**  
≈ 300–500 speakers and 1,000–1,500 guessers (each contributing 5–10 guesses).

---

## Technical Approach

**Main system steps:**

1. Speaker receives a random short phrase and records it.  
2. Audio upload triggers automatic preprocessing (length, noise filtering).  
3. Pretrained ML models predict four traits:  
   - Accent / region (10 regional classes)  
   - Age bracket (child 0-12, teen 13-19, adult 20-49, older 50+)  
   - Emotional tone (calm, happy, sad, angry, neutral)  
   - Native-language category (English, Spanish, Chinese, Arabic, other)  
4. Clip is queued for human guessers via web interface.  
5. Each clip receives ≥ 3 independent human guesses.  
6. Speaker self-reports their true values.  
7. System aggregates AI, crowd, and truth → computes perception-gap metrics.  
8. Leaderboards and analytics dashboards update dynamically.

**Crowd vs. automated:**  
- *Human:* recording, listening, labeling, and self-reporting.  
- *Automated:* AI trait prediction, clip distribution, aggregation, scoring, and visualization.

**Technologies/tools:**  
Python (Flask / FastAPI), React front-end, Firebase Auth + Firestore, Hugging Face Transformers / SpeechBrain, Web Audio API, MTurk API (optional).

**Aggregation method:**  
Weighted majority voting (weights = guesser reliability). Compare distributions of human vs AI vs truth to compute perception-gap statistics.

---

## Quality Control

**How will you ensure quality of crowd contributions?**

- Automatic checks for audio length > 5 s and minimum SNR.  
- Gold-standard control clips with known traits to monitor guesser accuracy.  
- Weighted reliability scores for each guesser.  
- Removal of inconsistent self-reports and statistical outliers.  
- Random audits of audio for validity.

**Specific quality-control methods:**  
- [x] Gold standard questions  
- [x] Majority voting across multiple workers  
- [x] Reputation/qualification weighting  
- [x] Statistical outlier detection  
- [ ] Expert review or verification (optional)  
- [ ] Attention checks

---

## Evaluation & Success Metrics

**How will you know if your project succeeds?**  
Success = usable perception-gap dataset + sustained user engagement.

**Quantitative metrics:**  
- ≥ 80 % valid recordings after QC.  
- ≥ 1,000 guessers contributing ≥ 5 guesses each.  
- Inter-rater agreement (Fleiss κ > 0.6).  
- ≥ 200 clips with both human and AI predictions + self-report.  
- ≤ $1 per labeled clip average cost.  
- Statistically significant perception-gap trends across traits.

---

## Challenges & Mitigation Strategies

**Challenge 1:** Low-quality or noisy recordings.  
**Mitigation:** Enforce automatic signal-to-noise filtering and prompt re-recording.

**Challenge 2:** Guessers rushing or random guessing.  
**Mitigation:** Use control clips, reliability scoring, and gamified accuracy feedback.

**Challenge 3:** Privacy and ethical concerns.  
**Mitigation:** Use anonymized clip IDs, optional self-reports, and clear consent terms; no storage of personal identifiers.

---

## Prior Work

**Similar projects:**  
- *Mozilla Common Voice* — crowd collects transcribed speech; no perception or demographic labeling.  
- *Guess My Accent* — casual web game; lacks AI comparison or structured data.  

**How Auralynx differs:**  
It unites AI prediction, human perception, and self-reported truth on the same clip to quantify bias and perception gaps — a first-of-its-kind tri-layer dataset.

---

## Discussion Notes from Round 2

**Agreements:**  
- Keep traits limited to four interpretable categories (accent, age, emotion, native-language).  
- Use gamification rather than payment for sustained engagement.  
- Focus on perception-gap analytics as the research output.

**Concerns:**  
- Possible imbalance in accent representation.  
- Need for robust quality checks on noisy user audio.

**Why promising:**  
Bridges crowdsourcing, fairness, and voice AI — producing publishable-quality perception data in a fun, scalable way.

**Sustainability & feasibility:**  
Feasible with free tools and volunteer crowd; expandable post-course into a real research platform.

---

## Additional Notes

Potential future extensions:  
- Add gender-expression or confidence-level prediction (with ethical review).  
- Integrate fine-tuned transformer models (e.g., Whisper, Wav2Vec2) for deeper trait inference.  
- Open-source anonymized dataset for academic use.

