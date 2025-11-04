# Crowdsourcing Project Idea: PriceScope

## Author
Amber He, heamber

## Problem Statement
Grocery store prices vary a lot across different stores, in person, and online.
People don't have access to the best prices for each item, unless they check every store or 
online vendor themselves, which takes up a lot of time. A crowdsourced price reporting system
can be accurate, local, and efficient to help shoppers minimize food costs. 

## Core Concept
**One-line pitch:** Platform to identify the lowest local prices for grocery items in real time. 

**Target users:** All shoppers seeking to save money on groceries. 

**The crowd:** Shoppers at grocery stores submitting price data during grocery trips.

**The task:** Shoppers will enter a product name/catagory/price, store location OR application, and optionally upload photo of price or reciept. 

## Key Features
1. Searchable grocery item database: like milk, eggs, apples
2. Live price map/list showing the cheapest options
3. Price tags or receipt-backed verification

## Feasibility Check
**Data source:** User submitted prices from local stores or online like Weee

**Budget reality:** QR posters at stores, ads on applications, small raffle incentives

**Crowd size needed:** maybe 100-200 workers providing more than one price weekly (once a week grocery shopping)

**Quality control approach:** receipt or shelf photo/screenshot

## Technical Approach
**Human tasks:** workers need to submit price and item, upload photo, confirm other submission photos

**Automated tasks:** normalize product names, geotag stores, calc cheapest

**Aggregation method:** weighted median price per item per store, higher weight for verified entries/people

## Prior Work
**Similar projects:** Flipp is for coupons and estimated prices, but this one is more local and easier to use

**Lessons from past course projects:** Needs to be valuable to all users, and it is. Needs to be narrow domain, so that the data isn't too complex. So it is easier to implement as well. This is also a everyday practical problem. 

## Why This Could Work
Submission effort is low, incentives are very direct. I, as well as everyone wants to save money and buy the best groceries for the cheapest price. I struggle spending time to figure out where to buy eggs versus apples from. Data quality will be easier to control because the domain is limited to only groceries.
