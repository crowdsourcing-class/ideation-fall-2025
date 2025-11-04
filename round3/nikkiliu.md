# Crowdsourcing Project Idea: [Project Title]

_Replace [Project Title] with a creative name for your project_

## Authors

**Original Author:** Nikki Liu, nikkiliu

**Round 2 Contributors:** Nikki Liu, nikkiliu & Jevin Ta, jevinta

**Round 3 Contributors:** Nikki Liu, nikkiliu & Jevin Ta, jevinta & Brandon Yan, bdonyan

## Problem Statement

Climate change is intensifying droughts, floods, and pest outbreaks that threaten global food production. Automated satellite-monitoring systems often miss early signs of crop stress, especially in smallholder regions with varied soil and vegetation patterns. AgriAid addresses this problem by using the power of human perception to label subtle crop stress indicators in satellite images — helping NGOs, researchers, and governments detect food insecurity risks before they escalate.

## Target Audience

**End Users:** Environmental scientists, agricultural researchers, NGOs (e.g., FAO, WFP), and data scientists studying food security.

**Crowd Workers:** Citizen scientists, sustainability volunteers, and students interested in climate and data science.

**Stakeholders:** Humanitarian organizations, policymakers, agricultural extension services, and local communities impacted by food insecurity.

## Description

AgriAid is a citizen-science platform that invites volunteers to label satellite image pairs of agricultural regions captured weeks apart. Users tag each area as healthy, stressed, or bare and identify possible causes such as drought, flood, or pests. The system aggregates human insights to build a global crop-stress dataset and visual “early warning” dashboard. By combining human intuition and open satellite data, AgriAid provides an affordable and scalable tool for detecting emerging agricultural crises in data-poor regions.

## Project Type

_Select the primary category:_

- [✓] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 8-10 key features or capabilities of your system:_

1. Before/After Image Labeling: Users view satellite image pairs to assess visible crop changes.
2. Multi-Class Classification: Labels include healthy, stressed, bare, and likely cause.
3. Confidence Scoring: Workers self-report confidence (1–5), improving reliability weighting.
4. Interactive Global Dashboard: Aggregates crowd-labeled stress data into live regional maps.
5. Redundant Labeling & Consensus: Each image is labeled by ≥5 users for robust aggregation.
6. Gamification: Leaderboards and badges reward accuracy and consistency.
7. Quality Control Layer: Includes gold-standard tiles and reliability scoring.
8. Data Export for Research: Clean, labeled dataset downloadable for ML model training.
9. [Feature 9 - optional]
10. [Feature 10 - optional]

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
University environmental clubs, social media (Reddit r/environment, Discord climate servers), and student science courses offering participation credit.

**What will they provide?**
Image labels describing vegetation health and suspected stress cause, along with optional confidence ratings.

**What skills do they need?**
Basic visual recognition; ability to compare two images and detect subtle color/texture changes.

**Do skills vary widely? How?**
Yes — those with remote-sensing or agriculture experience may be more accurate, but redundancy compensates for variability.

**How will you incentivize participation?**
- Intrinsic: Contribution to climate resilience and global food security.
- Extrinsic: Public leaderboards, badges, “Top Contributor” profiles, and data-impact visualizations.
- Academic: Optional extra-credit participation for university volunteers.

**Budget & Cost Analysis:**
- Estimated cost per task: $0.00 (volunteer-based)
- Estimated cost per worker: $0.00
- Number of tasks needed: ≈10 000 tiles
- Total estimated budget: <$100 (hosting, storage, APIs)
- Justification: Open satellite imagery + free hosting tiers make the system sustainable.

**Where will your data come from?**
Open Sentinel-2 and Landsat imagery via Google Earth Engine API and public STAC repositories.

**Scale Requirements:**
- Minimum viable crowd size: 50–100 workers
- Target crowd size for full functionality: 300–500 workers
- Potential to scale to: 5000+ volunteers for global coverage

## Technical Architecture

**System Components:**

1. Frontend: Streamlit or React web interface for labeling.
2. Backend: Python (Flask) API handling task assignment and data submission.
3. Database: Firebase / Firestore storing user profiles and labels.
4. Image Source: Google Earth Engine API serving pre-processed tiles.
5. Computation: Python + NumPy + OpenCV for preprocessing, NDVI computation, and consensus logic.

**Detailed Workflow:**

_Step-by-step description of how the system works:_

1. System retrieves satellite tiles (before + after).
2. Pre-processing enhances color and contrast.
3. Each task assigned to ≥5 volunteers.
4. Volunteers label vegetation health and cause.
5. System stores labels and confidence scores.
6. Aggregation engine computes weighted consensus.
7. Results visualized on an interactive world map.

**Human vs. Automated Tasks:**

| Task | Performed By | Why? |
|------|--------------|------|
| Image labeling| Human | Humans detect nuanced visual cues AI misses |
| Confidence scoring | Human | Reflects subjective certainty |
| Label aggregation | Automated | Scalable and objective consensus |
| NDVI correlation & mapping | Automated | Quantitative validation |

**Technologies & Tools:**
- Frontend: Streamlit / React
- Backend: Python/Flask
- Database: [Firebase / Firestore
- ML/AI: scikit-learn / OpenCV / NumPy
- Crowdsourcing Platform: Google Earth Engine, STAC
- Hosting: Google Cloud / Heroku
- Other: [any other relevant tools]

**Aggregation Method:**
Weighted majority vote using both inter-rater agreement and self-confidence scores. Disagreements trigger re-labeling by high-reliability users.

## Quality Control

**Quality Control Strategy:**
Quality ensured through redundancy, agreement metrics, and reliability tracking. Expert-verified “gold” tiles periodically seeded to evaluate accuracy.

**Specific QC Mechanisms:**
- [✓] Gold standard questions (test questions with known answers)
  - _Details: 10% of tiles have known labels; workers falling below 70% accuracy are flagged.
- [✓] Majority voting across multiple workers
  - _Details: Five workers per tile; ties broken by weighted confidence.
- [✓] Expert review or verification
  - _Details: Random 5% sample reviewed by graduate researchers.
- [ ] Attention checks or trap questions
  - _Details: [What types? How often? Consequences?]_
- [✓] Reputation/qualification systems
  - _Details: Reliability increases with consistent agreement.
- [✓] Statistical outlier detection
  - _Details: Removes labels >2 SD from consensus.
- [✓] Redundancy and agreement metrics
  - _Details: Min 70% agreement threshold for “verified” labels.
- [ ] Other: [specify]
  - _Details: [Explain custom QC approaches]_

**Handling Low-Quality Work:**
Low-agreement labels are discarded and re-tasked to new users; persistent low-accuracy users lose ranking visibility.

## Evaluation & Success Metrics

**Primary Success Metrics:**

1. Label Agreement Rate: ≥70 % inter-rater consensus across tasks.
2. Correlation with NDVI: ≥0.6 Pearson correlation between human and NDVI stress detection.
3. Engagement: ≥500 unique contributors and >10 000 tiles labeled.

**Evaluation Methodology:**

Compare crowd labels to NDVI trends and expert ground truth on selected regions; analyze precision, recall, and F1 scores. Track participation analytics (average tasks/worker, retention).

**Baseline Comparisons:**
- Baseline = pure NDVI-based classification.
- Improvement = regions humans detect stress earlier than NDVI flagging.

**Success Criteria:**
- Minimum viable success: 100 users, 70 % agreement
- Target success: 300 users, 0.6 correlation
- Stretch success: 500 users, 0.75 correlation + dataset adopted by researchers

## Challenges & Mitigation Strategies

**Challenge 1:** Volunteer retention and engagement
- **Why it's a risk:** Sustained labeling needed for coverage
- **Mitigation strategy:** Gamification, progress tracking, social sharing
- **Backup plan:** Run labeling drives with university clubs

**Challenge 2:** Subjectivity in visual judgment
- **Why it's a risk:** Workers interpret “stress” differently
- **Mitigation strategy:** Training examples + redundant labeling
- **Backup plan:** Aggregate with confidence weighting

**Challenge 3:** Data imbalance across regions
- **Why it's a risk:** Popular regions get more labels
- **Mitigation strategy:** Algorithmically assign under-labeled areas first
- **Backup plan:** Manual rebalancing through task sampling

**Challenge 4:** [Optional additional challenge]
- **Why it's a risk:** [Explain the impact]
- **Mitigation strategy:** [Detailed plan to address it]
- **Backup plan:** [Alternative if mitigation fails]

## Prior Work & Related Projects

**Similar Existing Systems:**

1. **GeoWiki**
   - Description: Crowdsourced global land-use classification.
   - Similarities: Human labeling of satellite tiles.
   - Differences: AgriAid detects temporal crop stress and causes, not static land type.
   - Citation/Link: https://www.geo-wiki.org

2. **Radiant Earth MLHub**
   - Description: Expert-curated geospatial datasets.
   - Similarities: Both produce structured, ML-usable geospatial data.
   - Differences: AgriAid democratizes data creation via public volunteers.
   - Citation/Link: https://registry.opendata.aws/radiant-mlhub/

3. **PlantVillage**
   - Description: A mobile app where farmers upload photos of individual plants to diagnose crop diseases using AI models.
   - Similarities: Both aim to improve agricultural resilience and early detection of plant stress.
   - Differences: PlantVillage operates at the micro scale (single plant, smartphone photo), while AgriAid operates at the macro scale (satellite fields, regional stress mapping).
   - Citation/Link: https://plantvillage.psu.edu

**Lessons from Past Course Projects:**
Past projects (e.g., Memory Mosaic, MoralMap) show real-world testing and clear incentive design drive participation. We’ll apply that by integrating visual dashboards and real-impact feedback.

## Ethical Considerations

**Potential Ethical Issues:**
- Privacy of satellite imagery (identifiable farms)
- Volunteer data misuse or burnout
- Potential misinterpretation of “food insecurity” signals

**Mitigation Strategies:**
- Use only public, anonymized tiles.
- Clear participation consent form.
- Disclaimers that results are research-supporting, not definitive.

**IRB Considerations:**
Likely exempt — no personal data or sensitive human subjects involved.

## Business Viability (Optional)

_If your project has business potential, consider:_

**Revenue Model:**
Freemium research API for NGOs and startups.

**Market Size:**
Environmental data providers, agritech firms, and humanitarian agencies.

**Competitive Advantage:**
Faster and cheaper early-warning data than expert labeling.

**Sustainability:**
Volunteer-driven model; potential long-term support via open-source partnerships.

## Steel-Man Discussion (Round 3)

**Idea A Steel-Man:**
SafeRoute — crowdsourced campus safety heatmap; strong UI but crowded market.

**Idea B Steel-Man:**
[AgriAid — human-AI hybrid for crop-stress detection.

**Why We Chose This Idea:**
Why We Chose AgriAid: Broader social impact, novel application of crowdsourcing, realistic build scope.

**What We Agreed On:**
Focus on dynamic labeling + scientific relevance.

**What Concerns Emerged:**
Sustaining engagement; addressed through gamification.

**Key Insights from Round 3 Discussion:**
Human perception complements NDVI well; volunteers value tangible impact.

## Implementation Timeline (Optional)

_If you were to build this, what would the timeline look like?_

**Week 1-2:** Data collection & UI prototype.
**Week 3-4:** Launch MVP + initial crowd recruitme
**Week 5-6:** Implement QC + aggregation dashboard.
**Week 7-8:** Finalize visualizations + evaluation report.

## Additional Notes

_Any other relevant information, inspirations, or considerations?_

[Optional: Add any additional context, ideas, or references]

## References & Inspiration

_Include any references, papers, articles, or sources that inspired or informed this project idea:_

1. Radiant Earth Foundation (2023). MLHub Datasets. https://mlhub.earth
2. [Reference 2]
3. [Reference 3]
