# Crowdsourcing Project Idea: PriceScope

## Authors

**Original Author:** Amber He, heamber

**Contributor:**

## Problem Statement

Grocery store prices vary a lot across different stores, in person, and online. People don't have access to the best prices for each item, unless they check every store or online vendor themselves, which takes up a lot of time. A crowdsourced price reporting system can be accurate, local, and efficient to help shoppers minimize food costs.

## Target Audience

Users & crowd are all shoppers seeking to save money on groceries, people on a budget, and people who want to get the best deals on groceries

## Description

This system crowdsources current grocery prices from shoppers to identify 
the lowest local cost for common grocery items. Users submit prices at checkout 
by uploading a photo of a receipt or shelf tag. The system extracts the item and price, 
verifies location and timestamp, and aggregates multiple reports per product/store pair. 
A search interface then displays the cheapest nearby option for each item, weighted by 
recency and verification level.

## Project Type

- [ ] Human computation algorithm
- [ ] Social science experiment with the crowd
- [ ] Tool for crowdsourcing (requesters or workers)
- [x] Business idea using crowdsourcing
- [ ] Other: [specify]

## Key Features

1. Search interface to look up grocery items and view nearby prices
2. User submission with price entry and photo upload if need be
3. Automatic timestamp and location capture for each price report
4. Verification layer using photo checks and consensus across submissions
5. Price aggregation and ranking to get the lowest verified price per store

## Feasibility: Crowd & Resources

**Where will your crowd workers come from?**
Local shoppers, submitting grocery prices during regular (weekly maybe) store visits. 

**What will they provide?**
item names, prices, store, optional receipt or shelf tag

**What skills do they need?**
basic device use, photograph, applciation use

**Do skills vary widely? How?**
variation is minimal since users may submit bad photos or bad data, but not much skill needed to copy a number down or take a photo. 

**How will you incentivize participation?**
intrinsic savings motivation, leaderboard maybe for top contributors, monthly raffel for verified submissions, for grocery money

**How much will it cost?**
raffle budget: maybe 600 a year, for 50 dollars a month. AWS probably around 50 dollars a month? After a while we can delete the photos and data because they arent needed anymore.

**Where will your data come from?**
user generated price reports, photos

**How many crowd workers do you need?**
around 100-200 people a week maybe

## Technical Approach

**What are the main steps/components in your system?**

1. User submits grocery price for item, size, store, optional photo reciept/shelftag
2. System validates submission: timestamp, GPS within store, OCR on photo, basic format checks
3. Match item with item, create/update item to a standardized unit or brand
4. Aggregation: reputation weighted median price per item per store
5. Search ranks stores by lowest verified price, also shows the confidence and recency scores

**What parts are done by the crowd vs. automated?**
crowd: submit prices and photos, confirm/flag other submissions
automated: OCR, GPS, time, product/size norm, duplicate detection, aggregation, outliers, ranking

**What technologies/tools will you use?**
react, aws, OTP auth, node.js, dynamo for prices, s3 for images, OCR

**How will you aggregate results from the crowd?**
weighted median per item per store, weighted based on reputation or verification

## Quality Control

**How will you ensure quality of crowd contributions?**

- proof capture reciept or self tag image, OCR
- geofence submissions, must be in the same city, timestamp
- item mapping, dont add mismatched sizes

**Specific quality control methods:**
- [ ] Gold standard questions (test questions with known answers)
- [x] Majority voting across multiple workers
- [ ] Expert review or verification
- [ ] Attention checks or trap questions
- [x] Reputation/qualification systems
- [x] Statistical outlier detection

## Evaluation & Success Metrics

**How will you know if your project succeeds?**
Maybe if we get 200 users, 25% of them using it every week, coverage maybe 50% of common grocery items, not too expensive. 

**What would success look like quantitatively?**
90% of searches for "eggs, milk, chicken, bread" return more than 2 verified store options
100 entries per week

## Challenges & Mitigation Strategies

**Challenge 1:** Product and size normalization across variants/brands
**Mitigation:** unit conversions to standardized price per common unit, remove ambigious entries

**Challenge 2:** spam/fraud submissions
**Mitigation:** geofence + timestamp, OCR, rate limiting, reputation weighting, and crowd checks

**Challenge 3:** Prices change fast, some users have their own coupons that others users cant use
**Mitigation:** Only for verified shelf prices, not after discount

## Discussion Notes from Round 2

**What did you agree on?**
[Key points of agreement between partners]

**What concerns or pushback emerged?**
[Questions, challenges, or areas of uncertainty discussed]

**Why is this idea promising?**
[Explain why you chose to develop this idea over the alternative]

**What makes this sustainable and feasible?**
[Specific reasons this can work within course constraints]

## Additional Notes

_Any other relevant information, inspirations, or considerations?_

[Optional: Add any additional context, ideas, or references]
