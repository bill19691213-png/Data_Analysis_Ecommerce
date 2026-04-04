# Ecommerce Funnel Analysis | SQL + Power BI
Bill Li
## Project Overview
This project analyzes an e-commerce purchase funnel using SQL (BigQuery) and Power BI to identify where potential purchasers are being lost from start to finish, and user shopping device prioritization to improve conversion and revenue. I chose a funnel analysis approach because it is important to understand how users move through the purchase journey and where they drop off before checking out. Funnel analysis is especially useful here because it makes it possible to measure step-by-step abandonment and connect those losses to business actions, which is exactly how e-commerce companies uses funnel and purchase-journey reporting. 

The analysis is split into two parts:
**Part 1:** overall ecommerce performance overview
**Part 2:** funnel optimization analysis focused on conversion loss and device prioritization

The final deliverables include:
## Business Question
"Which step causes the greatest loss of potential purchasers, and which device segment should the business prioritize to improve conversion and revenue?"

I chose this business question because it moves the project beyond descriptive KPI reporting and toward a more practical business decision. Instead of only asking how the store is performing overall, this question asks where the conversion process is breaking down and where optimization would likely create the biggest return, which is the kind of question funnel analysis is designed to answer.
## Dashboard

## Dataset
This project uses an ecommerce event dataset exported to **Google BigQuery** and transformed into cleaned analysis tables.
Two cleaned base tables were created first:

- `Event_base` — session/event-level table used for funnel logic
- `Item_base` — item-level table used for revenue analysis

These were then used to build aggregated reporting tables for Power BI.
## Key Findings

## Business Recommendations
## Tools Used
## Files in This Repository
## What I Learned
