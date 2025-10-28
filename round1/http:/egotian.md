# Crowdsourcing Project Idea: RampCheck – Mapping Curb Ramp Accessibility

## Author
egotian

## Problem Statement
Accessible sidewalks are essential for wheelchair users, parents with strollers, and seniors, yet cities often lack up-to-date data on where curb ramps exist and whether they are usable. Manual municipal surveys are expensive and slow. We will crowdsource rapid, low-cost labels on curb ramp presence and condition from street-level imagery to produce an actionable accessibility map.

## Core Concept
**One-line pitch:** Crowd-label street photos to map where curb ramps exist and whether they are usable.

**Target users:** City planners, disability advocates, navigation apps (e.g., routing around barriers), campus facilities teams.

**The crowd:** Amazon Mechanical Turk workers for scale, plus volunteer mappers from local accessibility and student groups.

**The task:** For a given street-level image and location, workers answer 4 multiple-choice questions: (1) curb ramp present? (yes/no/unclear), (2) condition? (good/damaged/blocked), (3) tactile paving present? (yes/no), (4) slope looks excessive? (yes/no/unclear). Workers may optionally click a rough point on the ramp to help geolocate.

## Key Features
1. Microtask UI optimized for 15–25s/image with clear examples and tooltips.
2. Built-in quality control: hidden gold questions, redundancy (3–5 labels/image), and disagreement review.  
3. Live map dashboard overlaying OpenStreetMap, with CSV/GeoJSON export for city partners.

## Feasibility Check
**Data source:** Free street-level imagery from Mapillary and OpenStreetCam; seed locations from OpenStreetMap curb-related tags; optional student-collected photos via a simple upload form.

**Budget reality:** <$500 by paying ~$0.03–$0.05 per judgment, 3 judgments per image, targeting ~3,000–5,000 images on MTurk (~$270–$750). We cap paid labels at ~3,000 images (~$450 max) and supplement with volunteers.

**Crowd size needed:** Hundreds of MTurk workers for throughput; 20–40 campus volunteers for validation.

**Quality control approach:** Qualification quiz with examples; 10–15% gold tasks; time-on-task and attention checks; redundancy with Dawid–Skene reliability weighting; spot manual audits on high-disagreement tiles.

## Technical Approach
**Human tasks:** Interpret photos; judge ramp presence/condition; flag occlusions; optionally mark a point on the ramp; validate edge cases in review tasks.

**Automated tasks:** Fetch/queue images by location; pre-filter likely ramp scenes using a lightweight detector or heuristic (e.g., sidewalk intersection tiles); deduplicate near-duplicate images; geocode outputs; generate map tiles and exports.

**Aggregation method:** Majority vote with worker reliability weights; per-location confidence scores; cluster nearby positive points to a single curb-ramp feature; surface low-confidence tiles for re-labeling.

## Prior Work
**Similar projects:** na

**Lessons from past course projects:** Keep tasks atomic and well-instructed; pilot with 50–100 items first;
## Why This Could Work
We leverage free imagery and proven microtask designs, keeping costs low while producing a useful accessibility layer for real users. The scope is narrow, aggregation is standard, and quality control is well-understood, making this feasible within a semester.
