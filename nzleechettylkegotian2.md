# Crowdsourcing Project Idea: RampCheck – Mapping Curb Ramp Accessibility

## Authors

**Original Author:** egotian

**Contributor:** nathan lee : nzlee kieran chetty : chettylk

## Problem Statement

Accessible sidewalks are essential for wheelchair users, parents with strollers, and seniors, yet cities often lack up-to-date data on where curb ramps exist and whether they are usable. Manual municipal surveys are expensive and slow. We will crowdsource rapid, low-cost labels on curb ramp presence and condition from street-level imagery to produce an actionable accessibility map.

## Target Audience

Primary users: city planners, disability advocates, campus facilities teams, and navigation apps that can route around barriers. Crowd workers: Amazon Mechanical Turk workers for scale and volunteers from local accessibility and student groups for validation.

## Description

RampCheck queues street-level images (e.g., Mapillary/OpenStreetCam) at intersections and asks crowd workers four quick questions: curb ramp present, condition (good/damaged/blocked), tactile paving present, and slope looks excessive. Workers can optionally click a point on the ramp for better geolocation. We apply redundancy and quality controls, then aggregate responses with worker reliability weighting to generate per-location confidence scores. Outputs are visualized as a live accessibility layer and exportable as CSV/GeoJSON for partners.

## Project Type

_Select the category that best fits your project:_

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [x] Tool for crowdsourcing (requesters or workers)
- [ ] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

_List 5-8 key features or capabilities of your system. Expand from Round 1:_

1. Microtask UI optimized for 15–25 seconds/image with clear examples and tooltips.
2. Built-in quality control: hidden gold questions, redundancy (3–5 labels/image), attention checks.
3. Live map dashboard overlaying OpenStreetMap with per-location confidence scoring.
4. Data export as CSV/GeoJSON for city partners and advocacy groups.
5. Volunteer review queue for high-disagreement images and spot audits.
6. Optional click-to-mark the curb ramp point to improve geolocation.
7. Lightweight pre-filtering of candidate images/tiles to focus on intersections and sidewalks.
8. Simple photo upload form to supplement gaps where imagery is missing.

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
Amazon Mechanical Turk workers for primary throughput; campus accessibility and student groups for volunteer validation.

**What will they provide?**
Binary/multi-class labels on ramp presence/condition, tactile paving, slope; optional point clicks.

**What skills do they need?**
Basic visual reasoning, ability to follow short instructions, familiarity with street scenes.

**Do skills vary widely? How?**
Yes; some workers are more consistent and attentive. We model worker reliability and use qualification quizzes to filter.

**How will you incentivize participation?**
Paid MTurk tasks (~$0.03–$0.05 per judgment) with fair hourly rates via short tasks; volunteers motivated by local accessibility impact and recognition on the map.

**How much will it cost?**
~$0.03–$0.05 per judgment, 3 judgments/image → ~$0.09–$0.15 per image. Target 3,000 images → ~$270–$450 plus platform fees; capped within <$500.

**Where will your data come from?**
Street-level imagery via Mapillary and OpenStreetCam APIs; seed locations from OpenStreetMap; optional user uploads for coverage gaps.

**How many crowd workers do you need?**
Hundreds of MTurk workers for throughput; 20–40 volunteers for validation and spot checks.

## Technical Approach

**What are the main steps/components in your system?**

1. Fetch/queue candidate images near intersections from Mapillary/OpenStreetCam.
2. Pre-filter tiles likely to contain sidewalks/curbs; deduplicate near-duplicates.
3. Launch microtasks on MTurk/volunteer portal with golds and attention checks.
4. Aggregate labels with worker reliability weighting; compute confidence scores.
5. Generate map tiles and exports; route low-confidence tiles back for review.

**What parts are done by the crowd vs. automated?**
Crowd: visual judgments (presence/condition/tactile/slope), optional ramp point click, edge-case review. Automated: image retrieval/queuing, heuristics for pre-filtering, deduplication, aggregation and confidence scoring, map tiling and data export.

**What technologies/tools will you use?**
Python (FastAPI) for backend; React for task UI; Mapillary/OpenStreetCam APIs; MTurk API; PostgreSQL/PostGIS; Leaflet/Mapbox for map; Pandas for aggregation; S3 or similar object storage.

**How will you aggregate results from the crowd?**
Majority vote with worker reliability weights; per-location confidence scores; cluster nearby positives to a single curb-ramp feature; surface disagreements for re-labeling.

## Quality Control

**How will you ensure quality of crowd contributions?**

Qualification quiz with clear positive/negative examples; 10–15% embedded gold questions; time-on-task thresholds; redundancy (3–5 labels/image); automatic routing of high-disagreement items to review; small expert/volunteer audits.

**Specific quality control methods:**
- [x] Gold standard questions (test questions with known answers)
- [x] Majority voting across multiple workers
- [x] Expert review or verification
- [x] Attention checks or trap questions
- [x] Reputation/qualification systems
- [x] Statistical outlier detection
- [x] Other: Disagreement routing and time-on-task thresholds

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
High label accuracy on gold questions, strong inter-rater agreement, actionable map for at least one neighborhood/campus, and positive feedback from an accessibility stakeholder.

**What would success look like quantitatively?**
≥90% accuracy on golds; Cohen's kappa ≥0.6; median task time ≤25s; cost ≤$0.12 per image (median); 1,000+ images labeled; 200+ confirmed curb ramps mapped with confidence ≥0.8.

## Challenges & Mitigation Strategies

_For each challenge, propose a mitigation strategy:_

**Challenge 1:** Ambiguous or occluded imagery (cars, shadows, poor angle).
**Mitigation:** Allow "unclear" option; route to review; fetch alternative images nearby; require redundancy.

**Challenge 2:** Low-quality or inattentive workers.
**Mitigation:** Qualification quiz; golds and attention checks; reliability-weighted aggregation; blocklist.

**Challenge 3:** Coverage gaps in street-level imagery.
**Mitigation:** Accept volunteer uploads; focus on high-coverage areas first; partner with campus/city for targeted capture.

## Prior Work

_Are there similar projects or systems? How is yours different?_

Project Sidewalk (UW) crowdsources sidewalk accessibility audits; OSM and Mapillary support community mapping of curb cuts. RampCheck narrows scope to curb ramps for faster microtasks, leverages existing imagery to reduce cost, and focuses on producing a ready-to-use accessibility layer with confidence scores.

**Specific related projects:**
na
## Discussion Notes from Round 2

**What did you agree on?**
Narrow scope to curb ramps only; use existing imagery first; prioritize a simple, fast task UI with clear examples; deliver a live map and CSV/GeoJSON export.

**What concerns or pushback emerged?**
Imagery licensing/availability, budget limits on MTurk, and ensuring fair hourly pay; avoiding overclaiming when confidence is low.

**Why is this idea promising?**
High social impact, concrete deliverables, and well-understood microtask design. Leverages free data sources and a focused scope to stay within time and budget.

**What makes this sustainable and feasible?**
Low per-label costs, volunteer supplementation, straightforward aggregation and QC, and incremental deployment (pilot one neighborhood, then expand).

## Additional Notes

_Any other relevant information, inspirations, or considerations?_

Pilot plan: run a 50–100 image pilot to tune instructions and pricing, then scale to ~3,000 images in the target area. Share results with a local disability group for feedback before broader rollout.
