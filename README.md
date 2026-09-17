# Product Health Diagnostic & KPI Analytics Platform
### Product Performance, Funnel & User Retention Analysis

## Overview
This project analyzes the health of a food-delivery style product from different parts of the user journey.
The goal was to understand how users interact with the product, where they drop off, whether they come back, which acquisition channels perform better, and how product experiments affect conversion.
I used SQL for the main analysis, Python for exploratory data analysis, and Power BI to build an interactive product health dashboard.

## Business Problem
The product was getting users and generating orders, but looking at total orders or revenue alone did not explain where the product was facing problems.
The analysis focused on questions such as:
- Where are users dropping off in the ordering funnel?
- Is payment failure affecting order completion?
- Which user segments are more likely to churn?
- Which acquisition channels bring users who convert and stay?
- Which product features are being adopted?
- Are A/B test variants actually improving conversion?

## Objectives
- Build a clear view of overall product health
- Analyze the user journey from session to payment
- Identify major funnel drop-offs
- Measure retention and churn
- Compare acquisition channels
- Analyze feature adoption
- Evaluate A/B test performance
- Turn the analysis into practical product recommendations

## Tools Used
- **PostgreSQL** — Data analysis and KPI calculations
- **Python / Pandas** — Exploratory data analysis
- **Power BI** — Dashboard and visualization
- **SQL** — Funnel, retention, churn, acquisition and experiment analysis

## Analysis Covered
### 1. Executive Product Health
Key metrics included:
- Total Users
- Active Users
- Total Orders
- Total Revenue
- Ordering User Rate
- Payment Success
- Order Success
- Cancellation Rate
- Feature Adoption
- Churn
- Product Health Score

The product health score was created to provide a single high-level view while still allowing individual KPIs to be investigated.

### 2. Funnel & Conversion Analysis
The user journey was analyzed across:

**Sessions → Search → Restaurant View → Cart → Checkout → Payment**

The analysis calculated:
- Stage conversion rate
- Stage drop-off
- Overall funnel conversion
- Acquisition-channel funnel performance

The main focus was to identify where users were leaving the journey before reaching the payment stage.

### 3. Retention & Churn Analysis
Users were segmented based on their engagement and activity.

The analysis looked at:
- Retention rate
- Churn rate
- Repeat session rate
- Average sessions per user
- Retention by user segment
- Retention by acquisition channel
- Retention by device

This helped identify segments where improving engagement could have a bigger impact.

### 4. Feature Adoption
Feature usage was analyzed to understand which product features were being used most and least.

Features included:
- AI Recommendations
- Coupons
- Live Tracking
- Scheduled Delivery
- Reorder

This helped identify features that may need further investigation from a product or UX perspective.

### 5. A/B Testing
The project also included experiment analysis to compare control and test variants.

For each experiment, I looked at:
- Experiment participants
- Conversion rate
- Conversion lift
- Ordering users
- Revenue per participant
- Statistical significance

The goal was not just to identify which variant had a higher conversion rate, but to check whether the observed difference was strong enough to support a product decision.

# Key Findings
### Overall Product Health
- Product Health Score: **70.9/100**
- Payment Success: **95%**
- Order Success: **72%**
- Feature Adoption: **61%**
- Retention: **63%**
- Churn: **37%**

Payment performance was relatively strong, while order success and retention were the bigger areas of concern.

### Funnel
The largest drop-offs were seen earlier in the journey, particularly around search/restaurant discovery and moving from restaurant view to cart.
Once users reached the cart, the later stages of the funnel performed comparatively better.

### Retention
Power Users had the strongest retention at **74%**, while New Users had **56% retention** and **44% churn**.
This highlighted new-user activation as an area worth investigating.

### Acquisition
Retention and conversion varied across acquisition channels.
Google Ads had the highest retention at around **78%**, while Instagram Ads had the lowest at around **48%**.
This suggests that acquisition quality should be evaluated using both conversion and retention rather than user volume alone.

### Feature Adoption
AI Recommendations had the highest adoption at **22%**, while Reorder had the lowest at **9%**.
This creates an opportunity to understand whether lower adoption is related to discoverability, usability, or feature relevance.

### A/B Testing
For the selected experiment:

- Variant A: **56.25% conversion**
- Variant B: **53.85% conversion**
- Difference: **-4.27% for B**
- Result: **Not statistically significant**

Because the result was not statistically significant, the conversion difference was not treated as enough evidence to make an immediate rollout decision.

# Business Recommendations
Based on the analysis, I would focus on:

### 1. Investigate order failures
Break the unsuccessful orders down by failure reason, device, user segment, order value and other relevant dimensions to understand the reason behind the 72% order success rate.

### 2. Improve discovery-to-cart conversion
Investigate search, restaurant recommendations, menu experience and other parts of the journey where users are dropping off.

### 3. Improve new-user activation
Compare the early behavior of retained and churned users to understand what helps users become repeat users.

### 4. Evaluate acquisition quality
Track acquisition channels using:
**Conversion + Retention + Revenue**
instead of looking only at acquisition volume.

### 5. Continue controlled experimentation
Use A/B testing to validate product changes and consider statistical significance before making major rollout decisions.

## Dashboard
The Power BI dashboard contains four main pages:

1. **Executive Product Health Overview**
2. **Product Funnel & Conversion Analysis**
3. **User Retention & Churn Analysis**
4. **A/B Testing & Experiment Analysis**

The dashboard allows the analysis to be viewed through different dimensions such as acquisition channel, device, user segment and experiment.
