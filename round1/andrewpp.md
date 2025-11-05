# Crowdsourcing Project Idea: TrashTag Tracker

## Author
Jun Hyun Park - andrewpp

## Problem Statement
Urban and campus areas accumulate litter in spots that city services do not monitor closely. People often want to help clean up, but they lack data on where cleanup efforts are needed most. This project will crowdsource information about trash hotspots and verify cleanup progress so that volunteers can meaningfully target their efforts.

## Core Concept
**One-line pitch:** A crowd-powered platform where people report litter hotspots and confirm when they’ve been cleaned.

**Target users:** City residents, college students, local volunteer groups, environmental organizations.

**The crowd:** Anyone with a smartphone: campus community, neighborhood groups, social media users.

**The task:** Workers upload a quick photo of a littered area, tag the location, and choose a trash category (plastics, food waste, recyclables, etc.). Other workers review submissions and confirm status updates when trash is later removed.

## Key Features
1. Trash hotspot submission with photo + geolocation  
2. Verification workflow where multiple users confirm cleanups or flag duplicates  
3. A live “Cleanup Map” showing high-priority zones

## Feasibility Check
**Data source:** User-submitted images and GPS coordinates collected through a lightweight web app or form-based system.

**Budget reality:** Under $500 by relying on volunteers and free hosting tiers; paid crowd workers only for small validation batches if necessary.

**Crowd size needed:** Approximately 100–300 workers to cover a campus or community region.

**Quality control approach:** Majority agreement verification, duplicate detection, and auto-flagging inconsistent data.

## Technical Approach
**Human tasks:**  
Identifying trash presence, selecting trash categories, confirming cleanup completion.

**Automated tasks:**  
Spatial clustering of reports into hotspots, duplicate image detection, hotspot severity ranking.

**Aggregation method:**  
Weighted scoring of multiple reports per location. A hotspot is marked as clean only after sufficient independent confirmations.

## Prior Work
**Similar projects:**  
This project is actually not really similar to any of the previous projects.

**Lessons from past course projects:**  
However, from looking at previous course projects, it seems to me that clear microtasks and built-in verification processes increase engagement and data quality.

## Why This Could Work
People already notice litter but don’t always have a channel to help. By making environmental action quick, collaborative, and visible through a live map, this project motivates contributions while keeping scope and cost fully manageable for the course.
