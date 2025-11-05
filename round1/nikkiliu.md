# Crowdsourcing Project Idea: AgriAid

## Author
Nikki Liu (nikkiliu)

## Problem Statement
AI models struggle to reliably detect early signs of crop stress (drought, flooding, or pest damage) across diverse regions because visual signals vary by soil, crop type, and climate. Governments and NGOs often learn of local food shortages after they happen. AgriAid crowdsources human intuition to label satellite imagery for visible crop stress, creating an early-warning dataset for food insecurity prediction.

## Core Concept
**One-line pitch:** A web platform where volunteers label satellite images for signs of crop distress to help identify regions at risk of food insecurity.

**Target users:** Agricultural researchers, humanitarian NGOs, and climate data scientists.

**The crowd:** Students, sustainability volunteers, and anyone interested in climate-tech or humanitarian data.

**The task:** Volunteers view small satellite image patches (before/after a given date) and answer short questions: Does this field show healthy, stressed, or bare vegetation?
What is the likely cause (drought, flood, pests, unknown)? Rate confidence (1–5).

## Key Features
1. Before/After Viewer: Displays two images of the same area a few weeks apart.
2. Simple Label Set: Healthy / Stressed / Bare + optional cause tag. 
3. Global Dashboard: Aggregates crowd votes into regional “crop stress intensity” maps.

## Feasibility Check
**Data source:** Public Sentinel-2 or Planet NICFI imagery (open for low-res humanitarian use).

**Budget reality:** Free API access (Earth Engine or STAC browser exports) + Streamlit/Firebase web app. Volunteer crowd only. <$100 total.

**Crowd size needed:** 200–400 volunteers labeling ~5,000 image pairs — enough to train baseline models or validate NDVI signals.

**Quality control approach:** Each image labeled by ≥5 people; consensus + inter-rater agreement used. Compare with vegetation index data to spot systematic errors. Outlier raters down-weighted over time.

## Technical Approach
**Human tasks:** Visual assessment of plant health and possible stress causes.

**Automated tasks:** Compute vegetation indices (NDVI, EVI) and overlay with human judgments to test correlation.

**Aggregation method:** Weighted consensus labeling with confidence scaling.

## Prior Work
**Similar projects:** 
GeoWiki: static land-use classification.

Radiant Earth MLHub: ML dataset hosting (expert-curated).

PlantVillage: local crop-disease photos, not satellite or crowd-driven.

How this differs:
AgriAid focuses on dynamic agricultural stress detection, not general land use — the human crowd acts as an early-warning signal complementing vegetation indices, not replacing them.

**Lessons from past course projects:** 
From MoralMap: Real human perception captures nuance machines miss (e.g., partial yellowing).

From WeightIn: Visual feedback drives participation (“You just helped detect 12 hectares of stressed crops”).

From Memory Mosaic: Real-world pilot testing (e.g., crowd-labeling one country’s season) boosts credibility.

## Why This Could Work
This project fills a genuine data gap - early detection of crop stress before harvest failure - and supports humanitarian use cases. It’s technically straightforward (image labeling + consensus aggregation), visually compelling, and ethically meaningful. The end product - a global crop-stress map built from human perception - is both original and impactful, while perfectly aligned with the course’s focus on quality control, incentives, and aggregation.
