# Crowdsourcing Project Idea: Street Eats

## Author
Braden Johnson (bradenj)

## Problem Statement
Have you ever walked to your favorite food-truck just be to be dissapointed that it is not there? Finding food trucks can be tough due to inconsitent schedules and locations especially if the owners are not updating live on social media or something similar. Customers need an app that provides real-time crowd source updates on food truck statuses and quality reviews.

## Core Concept
**One-line pitch:** It provides a real-time, crowd-powered map of food truck locations and quality so people always know where to find the food they want.

**Target users:** Everyday people looking for a quick meal.

**The crowd:** Everyday app users out in the city, including both customers who spot food trucks and truck owners who can update their status directly

**The task:** For food trucks they have been to, crowd workers will provide information on both the menu and the location/hours of the food truck.

## Key Features
1. Live, crowd updated map of food-truck locations.
2. Menu reviews with images for each truck. 
3. Ability to favorite trucks and recieve notifications about them.

## Feasibility Check
**Data source:** Input data will come from the crowd's submissions on location, schedules, and menus. Initially we could also scrape data from online on food trucks and use that as a base.

**Budget reality:** The main cost issues here will come with maintaining the server and database the app will run on. 

**Crowd size needed:** Depending on the region/number of foodd trucks, I think 100s of workers would probably be ideal.

**Quality control approach:** The app can use reputation based weighting for reports and encourage photo submissions as confirmation.

## Technical Approach
**Human tasks:** Physically going to, verifiying, and reviewing the food truck.

**Automated tasks:** Updating the map and food-truck pages. Managing user reputation scores.

**Aggregation method:** The crowd responses and updates on food truck will be used to update the pages. For things like menu reviews which are not time-dependent, the updates should be rather straight-forward. For the time-based updates like food-truck location verification, we need to update the map live.

## Prior Work
**Similar projects:** [Name 1-2 related projects and how yours differs]

**Lessons from past course projects:** [What did you learn from reviewing past projects?]

## Why This Could Work
Finding food trucks is a real, everyday problem and users are naturally motivated to contribute when they benefit immediately from accurate information. The core features rely on straightforward crowdsourcing behaviors and lightweight aggregation methods that are manageable to prototype within the course.
