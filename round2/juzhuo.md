# Crowdsourcing Project Idea: GroceryLens

## Author
Julia Zhuo 83554455
Arushi Agarwal 61322095

## Problem Statement
Grocery prices and product quality can vary dramatically even between stores in the same neighborhood. Shoppers often lack transparent, localized data to compare value or identify which stores provide the best deals. *GroceryLens* aims to address this information gap by crowdsourcing real-time data on grocery prices and quality, empowering communities to make informed decisions, reduce overspending, and promote fair competition among local retailers.

## Core Concept
**One-line pitch:** *GroceryLens* crowdsources and visualizes neighborhood-level grocery data—combining price, quality, and user validation—to help shoppers find the best value for their money.

**Target users:** Everyday grocery shoppers such as college students, families, and budget-conscious consumers who seek affordable yet high-quality products.

**The crowd:** Local volunteers and shoppers who regularly visit nearby stores and are motivated by community engagement, rewards, or savings insights.

**The task:** Crowd workers upload photos of grocery items, input prices, rate quality (freshness, packaging, taste) on a 1–5 scale, and specify the store name and location. They can also verify or flag others’ submissions, ensuring data reliability and accountability.

## Key Features
1. **Interactive Grocery Map:** A live visual map displaying average prices, item availability, and quality scores by store and product category (produce, dairy, snacks, etc.).
2. **Reputation and Validation System:** Contributors earn “trust points” for accurate submissions. Verified entries carry more weight, and users can flag inconsistent data.
3. **Analytics Dashboard:** Visual insights showing neighborhood trends—price fluctuations, seasonal quality shifts, and store performance over time.
4. **Smart Recommendations:** Suggests nearby stores offering the best price-to-quality ratio for popular items (e.g., milk, apples, rice).
5. **Gamified Contributions:** Leaderboards and digital rewards encourage ongoing participation and healthy community competition.

## Feasibility Check
**Data source:** User-submitted entries (photos, prices, quality ratings) through a simple mobile app or web platform with geolocation tagging.

**Budget reality:** Under $500 total—funds allocated to cloud hosting, lightweight data processing (e.g., Firebase or Airtable backend), and small gift card incentives for early contributors.

**Crowd size needed:** Approximately 300–500 active users across several neighborhoods to generate meaningful comparisons and statistical reliability.

**Quality control approach:**
- Automated photo verification to ensure product label and price tag visibility.
- Weighted consensus: at least three independent submissions per product/store for data validation.
- Trust-based scoring: frequent and accurate contributors gain higher influence in aggregate results.

## Technical Approach
**Human tasks:**
- Submitting grocery data (photo, price, rating, store info).
- Reviewing and validating others’ submissions.
- Reporting errors or price changes.

**Automated tasks:**
- Aggregating and averaging verified data using weighted means.
- Detecting anomalies or fake entries through statistical outlier detection.
- Generating real-time dashboards and maps using simple visualization frameworks.

**Aggregation method:** Each product-store pair’s score is a weighted average of verified entries, adjusted by contributor reliability and recency of submission.

## Prior Work
**Similar projects:** Yelp, PriceSpy, and Waze all use crowdsourced input, but *GroceryLens* differentiates itself by focusing on *structured grocery data* (price + quality) rather than subjective reviews or navigation.

**Lessons from past projects:** Routine tasks—like grocery shopping—encourage consistent engagement. A simple, feedback-driven interface and visual insights increase both participation and data quality.

## Why This Could Work
*GroceryLens* is feasible because it relies on everyday human experiences and simple data collection tasks. The platform transforms small, routine actions into valuable community insights that help users save money, shop smarter, and promote market transparency. The project combines human intuition with lightweight automation, operates well within a limited budget, and creates tangible local impact—making it both socially meaningful and technically achievable.
