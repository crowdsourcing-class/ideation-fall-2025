# Crowdsourcing Project Idea: Auralynx 

Aural = relating to hearing + Lynx = sharp vision/predator; metaphor for a system with acute hearing.

## Author  
Alexander Budko (abudko)

## Problem Statement  
Speech-based AI systems often struggle with fairness and accuracy when dealing with diverse voices—especially from different accent groups, age ranges, and emotional states. Meanwhile, human listeners make strong judgements about voice characteristics, but there is little large-scale data linking what a speaker *actually* is, how an AI predicts their voice traits, and how human listeners perceive them. This lack of data limits our ability to understand bias, perception gaps, and to build more inclusive voice technologies.

## Core Concept  
**One-line pitch:** Users record a short prompted phrase, an AI model predicts specific voice traits (accent region, age bracket, emotional tone, native language), the crowd makes the same predictions, and the speaker reveals the truth—creating a rich dataset of **Actual → AI Prediction → Human Perception**.  

**Target users:** Researchers and developers in speech recognition, sociolinguistics, human-computer interaction, and voice assistant fairness.  

**The crowd:**  
- **Speakers:** Anyone with a microphone (students, volunteers, social media users).  
- **Guessers:** Online participants (e.g., MTurk workers or quiz-style volunteers) who listen to clips and make predictions.  

**The task:**  
1. A speaker is given a fixed phrase (approx. 5–8 seconds) to record.  
2. The system’s AI model immediately predicts:  
   - Accent/region of origin (one of ~10 predefined regions)  
   - Age bracket (Child: 0-12, Teen: 13-19, Adult: 20-49, Older: 50+)  
   - Emotional tone (Calm, Happy, Sad, Angry, Neutral)  
   - Native language category (English, Spanish, Chinese, Arabic, Etc.)  
3. Guessers listen to the clip and select the same four traits.  
4. The speaker self-reports their true traits for those same categories.  
5. The system shows a comparison: **AI Prediction vs Crowd Consensus vs Self-Report**, and awards points/badges based on accuracy and surprise.

## Key Features  
1. **Dual mode feedback:** Both AI prediction and human guessing for the same clip, enabling multi-perspective comparison.  
2. **Gamification & analytics dashboard:** Leaderboards for guessers (“Top Golden Ears”), recognition for speakers whose voice led to surprising predictions (“Most Unexpected Voice”), and statistical analytics of perception gaps.  
3. **Perception gap visualization:** A dashboard showing where human listeners and AI diverge from reality—by accent region, age, emotion, and native language category.

## Feasibility Check  
**Data source:**  
Voice clips uploaded by users via a web interface. The system prompts a standardized phrase to ensure consistent input.  

**Budget reality (< $500):**  
- Host via free-tier services (e.g., Firebase, GitHub Pages).  
- Use open-source pretrained models for initial trait predictions (e.g., age/voice/region classifiers).  
- Use small incentive budget (e.g., $100 for top performers, gift‐cards or digital badges) plus voluntary participation to keep costs low.  
- Use unpaid volunteers for initial guesser pool, supplemented by small MTurk batches.  

**Crowd size needed:**  
Approximately 300–500 speakers for a meaningful sample, and about 1,000–1,500 guessers (each making ~5 guesses) to produce robust consensus data.  

**Quality control approach:**  
- Require minimum audio length (≈5 s) and minimum signal-to-noise threshold.  
- Include “control clips” with known traits to test guesser reliability.  
- Track guesser accuracy over control items; weight their future contributions accordingly.  
- Filter out self-reports that are inconsistent or incomplete; remove outliers.

## Technical Approach  
**Human tasks:**  
- Speakers record the prompted phrase and submit self-reported trait values (region, age bracket, emotion, native language).  
- Guessers listen to clips and select predictions for the four traits.  

**Automated tasks:**  
- Immediately upon upload, run pretrained models to generate AI predictions for the four traits.  
- Serve each clip randomly to multiple guessers for human predictions.  
- Score and update leaderboards and badges in real time.  
- Store anonymized data (clip ID, AI prediction, human guesses, self-report) for analysis.  

**Aggregation method:**  
- For each clip and each trait: compute majority vote of guesser predictions (with weights based on guesser reliability).  
- Compare AI prediction vs human consensus vs self-report.  
- Compute “Perception Gap” metrics for each trait = |(Human consensus) – Self-report| and |(AI prediction) – Self-report|.  
- Aggregate gap metrics by speaker region, age bracket, emotion tone and native language to test for systematic bias or difference.

## Prior Work  
**Similar projects:**  
- Mozilla Common Voice: crowdsourced speech transcription dataset but focuses only on what is being said, not on perception of who is speaking.  
- Web apps like “Guess my Accent” that let listeners guess speaker accent, but do not combine AI prediction and self-reported truth at scale.  

**How this differs:**  
This project combines: (a) speaker self-report of ground truth, (b) AI model predictions of voice traits, and (c) human listener predictions—all for the same voice clip. It creates structured data for perception gaps and bias analysis across multiple traits.

**Lessons from past course projects:**  
Crowdsourcing projects that include immediate feedback and gamification (e.g., labeling tasks with leaderboards) achieve higher participation and data quality. Including both the producer (speakers) and consumer (guessers) sides helps sustain engagement and volume.

## Why This Could Work  
This project turns voice trait prediction into a fun, quick quiz while generating scientifically valuable data about human and AI perception of voice. With modern web audio tools and open-source models, it is technically feasible and cost-effective (well under $500). It is socially meaningful (addresses bias and diversity in voice tech) and well-suited to a class-sized prototyping project.