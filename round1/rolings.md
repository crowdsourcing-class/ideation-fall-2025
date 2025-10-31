# Crowdsourcing Project Idea: PlantSafe

## Author
Simon Roling

## Problem Statement
If you are trapped in the wilderness foraging for plants, or just on a hike in the rainforest, you may come across some plants that you don't know if you can eat. PlantSafe Allows users to upload images of plants and rely on crowd intelligence to build a community-driven guide to plant edibility.

## Core Concept
**One-line pitch:** My crowd-powered app allows users to upload images of plants, and the crowd helps verify whether they are edible or toxic.

**Target users:** Hikers, campers, people who are curious about local plants, or people who are trapped alone in the wilderness

**The crowd:** Volunteers and botanitss who enjoy plant identification. Potentially volunteers that like nature or gardening.

**The task:**  Crowd workers will review uploaded photos, tag the species, and vote on whether it is saqfe to eat, toxic, or uncertain, citing sources wherever possible.

## Key Features
1. Photo upload and auto tagging: user uploads images and the system guesses using some sort of plant identification api.
2. Crowd verification: other users confirm or correct the id, and vote on edibility.
3. Safety DB: Aggregated verified results form an open sourced, searchable library for other users to look through.

## Feasibility Check
**Data source:** User submitted images and safety assessments integrated with public plant datasets like Plant.id

**Budget reality:** Using free tiers of image recognition APIs and hosting services, and incentivising engagement with in-app rewards rather than paid ones makes this probably cost less than $100 all in.

**Crowd size needed:** roughly 100-300 workers

**Quality control approach:** Voter weightings, verified safe lables, and expert review for edge cases.

## Technical Approach
**Human tasks:** Identify/confirm species visually, assess and vote on safety level, flag misingormation

**Automated tasks:** pre-classify images, aggregate votes, filter spam.

**Aggregation method:** Votes will be verified via weighted consensus. This will only be considered as verified when there is at least a 90% consensus with at least 5 voters, then the response will be sent back to the user.
## Prior Work
**Similar projects:** iNaturalist has an automated plant identification technology, but doesn't really focus on safety or edibility.

**Lessons from past course projects:** The main flaw I saw with last year's projects was unrealistic scope:
        Some projects did not have a robust enough dataset to fully make accurate predictions, we fix this by keeping humans in the loop.


## Why This Could Work
Plant safe can work because it relies primarily on human judgement, but has robust quality control in place. Additionally, it falls in botanist and gardener interests ensuring an eager crowd.
