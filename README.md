# Ecommerce Funnel Analysis | SQL + Power BI
## How This Repo Is Organized

This repository is organized so readers can quickly find the SQL logic, dashboard output, and supporting project assets. If you want to review the project from start to finish, start with the README summary, then open the SQL files, and finally view the dashboard screenshots or Power BI file.

| Section | What it contains |
| --- | --- |
| [`README.md`](./README.md) | Project overview, business question, key findings, and final recommendations |
| [`sql/`](./sql/) | SQL scripts used for data cleaning, funnel table creation, and Part 1 / Part 2 analysis |
| [`images/`](./images/) | Dashboard screenshots used in the README |
| [`exports/`](./exports/) | Exported tables or CSV files used to review results outside BigQuery / Power BI |

## Project Overview

This project analyzes an e-commerce purchase funnel using SQL (BigQuery) and Power BI to identify where potential purchasers are being lost from start to finish, and user shopping device prioritization to improve conversion and revenue. I chose a funnel analysis approach because it is important to understand how users move through the purchase journey and where they drop off before checking out. Funnel analysis is especially useful here because it makes it possible to measure step-by-step abandonment and connect those losses to business actions, which is exactly how e-commerce companies uses funnel and purchase-journey reporting. 

The analysis is split into two parts:
**Part 1:** overall ecommerce performance overview
**Part 2:** Which device segment has the largest funnel leakage, at which step does the leakage happen, and what optimization would likely produce the biggest revenue impact?

## The final deliverables include:
- cleaned SQL tables built from the source ecommerce dataset
- Power BI dashboards with an overview page and a funnel optimization page
- business recommendations based on funnel drop-off and device-level revenue opportunity
## Business Question
"Which step causes the greatest loss of potential purchasers, and which device segment should the business prioritize to improve conversion and revenue?"

I chose this business question because it moves the project beyond descriptive KPI reporting and toward a more practical business decision. Instead of only asking how the store is performing overall, this question asks where the conversion process is breaking down and where optimization would likely create the biggest return, which is the kind of question funnel analysis is designed to answer.
## Dashboard

### Page 1 — Ecommerce Overview
<img width="1428" height="804" alt="image" src="https://github.com/user-attachments/assets/dbcaecef-9efd-4e77-ad50-2d3c3b5ff1fc" />

### Page 2 — Funnel Optimization
<img width="1421" height="799" alt="image" src="https://github.com/user-attachments/assets/fdc6b3b0-b88e-48ad-8d57-0546bfa17c3a" />

## Key Metrics Tracked

- Product view sessions
- Add-to-cart sessions
- Checkout sessions
- Purchase sessions
- Revenue
- Average order value
- View-to-purchase conversion rate
- Step-level drop-off sessions
- Estimated revenue uplift by device

## Key Findings

The funnel analysis suggests that the business is losing most potential customers before they demonstrate serious purchase intent.

The biggest weakness is at the point where users move from:

**browsing a product** → **adding it to cart**

That usually points to issues higher up in the shopping journey, such as:

- weak add-to-cart visibility
- unclear pricing or shipping information
- product page friction
- low purchase intent traffic
- poor product detail page experience on the target device

This does not explicitly prove the exact cause on its own, but it clearly shows where the problem is happening and where optimization should begin.

---
## Business Recommendations

### 1. Prioritize desktop product-page optimization
The desktop platform should be the first segment targeted because it combines:
- the highest traffic volume
- the highest revenue base
- the largest estimated revenue recovery opportunity

### 2. Focus on improving `View Item → Add to Cart` first
The largest leak happens before users even enter checkout, so the best first move is to improve the product-view-to-cart transition rather than starting with checkout redesign.

### 3. Use mobile as the benchmark
Mobile currently has the strongest view-to-purchase conversion rate, so it can be used as the benchmark when comparing desktop experience and layout decisions.

### 4. Drill deeper into desktop in the next phase
A useful next step would be to segment desktop traffic further by:
- product category
- landing page
- traffic source
- item brand or item type

This would help identify which parts of desktop traffic are driving the largest add-to-cart losses.
## Final Answer to the Business Question

The greatest loss of potential purchasers occurs at the **View Item → Add to Cart** step, where 61,874 sessions are lost, representing an 80.3% drop-off rate.

The business should prioritize the **desktop** segment because it has the highest traffic and revenue base but underperforms mobile on conversion, creating the largest estimated revenue recovery opportunity at roughly 9.15K.

## Dataset

This project uses an ecommerce event dataset exported to **Google BigQuery** and transformed into cleaned analysis tables.
Two cleaned base tables were created first:

- `Event_base` — session/event-level table used for funnel logic
- `Item_base` — item-level table used for revenue analysis

These were then used to build aggregated reporting tables for Power BI.
## Tools Used

| Tool | Purpose |
| --- | --- |
| Google BigQuery / SQL | Data cleaning, transformation, funnel logic, aggregation |
| Power BI | Dashboard design and business-facing visualization |
| Excel | Reviewing exported tables and checking outputs |
| GitHub | Project documentation and portfolio presentation |

## Author

Bill Li
