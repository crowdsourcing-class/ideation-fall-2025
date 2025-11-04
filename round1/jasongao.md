# Crowdsourcing Project Idea: AccessWatch — Crowd-Mapped Sidewalk & Crossing Accessibility

## Author
Jason Gao, jasongao

## Problem Statement
A lot of cities like Philly still have many missing or degraded curb ramps, blocked sidewalks, and unsafe crossings that prevent these places from being accessible. Traditional audits and 311 reporting are very slow and incomplete so all of these access issues remain invisible and end up piling up over time. There's a clear gap to bridge reporting and awareness.

## Core Concept
**One-line pitch:**  
A lightweight platform where residents can report, verify and map accessibility issues with geotagged photos, producing a live, open data layer cities and campuses can act on.

**Target users:**  
Anybody with mobility or vision impairments, seniors, parents with strollers, delivery workers, campus facilities teams and urban planners could all benefit from this platform.

**The crowd:**  
Local residents, disability advocates, students, commuters

**The task:**  
Crowd members will:
- Submit reports with issue type (e.g, missing curb ramp, obstruction), precise location and photos/vids 
- Verify or dispute others people's reports and add confirming evidence.
- Mark issues “resolved” when fixed and provide after-photos.
- Triage urgent items for faster escalation.

## Key Features
1. **Issue Cards & Live Map:** Each location shows status (Open/Verified/Resolved), timestamps, and evidence; filter by type, urgency, or age.
2. **Verification Ledger & Reputation:** Weighted confirmations; “Verified” requires ≥2 independent confirmations within 7 days or 1 confirmation + public-data match.
3. **Data Bridges:** Optional overlays from 311 categories and Vision Zero corridors to prioritize the most impactful fixes.
4. **Open Data Exports:** One-click GeoJSON/CSV for city/campus teams and a simple public dashboard.

## Feasibility Check
**Data source:**  
User evidence (EXIF/geo-tagged photos and short notes) plus read-only overlays from public datasets (e.g. city 311 service requests, Vision Zero corridors)

**Budget reality:**  
Providing a free-tier stack for a semester pilot: Supabase (Auth/Postgres/Storage), Firebase Hosting/CDN, and Mapbox starter tier. Domain + incidentals ~$20–$40; total is comfortably < $300.

**Crowd size needed:**  
Pilot (Penn campus / 1–2 neighborhoods): 100–200 users to seed ~300–600 reports and ~1,000 verifications in a month. City-scale: 500–1,000 active contributors.

## Technical Approach
**Human tasks:**  
Report issues with structured labels, verify/dispute reports, add corroborating media, and mark resolutions.

**Automated tasks:**  
Geo-validation (within 20–30 m of pin + timestamp sanity checks), duplicate clustering (Haversine/DBSCAN), spam filtering, and optional sync for public data overlays.

## Prior Work
**Similar projects:**
- **Project Sidewalk (UW):** Demonstrates that crowds can label accessibility barriers at scale; AccessWatch focuses on fresh, on-the-ground verification and fix tracking.
- **Wheelmap.org / SeeClickFix (311 CRMs):** Show that simple labeling and civic reporting work; AccessWatch specializes in access-specific evidence and exports data to 311 where appropriate.

**Lessons from past course projects:**  
Based on the lessons from **PixelPatchwork**, sustained engagement will beat one-off tasks → streaks and “impact counters.”  

## Why This Could Work
AccessWatch would turn everyday walks into micro-contributions that add up to have immediate local impact. The build uses off-the-shelf, free-tier tools and open data which keeps the build scope realistic for a semester.
