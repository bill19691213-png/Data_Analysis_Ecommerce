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
**Part 2:** identify the biggest funnel leak and recommend where to optimize first

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

## Business Decision Layer
### 1. Business need

The business is generating product interest, but too many potential purchasers are leaving before they add an item to cart. The biggest leak happens at the View Item → Add to Cart step, where 61,874 sessions are lost, equal to an 80.3% drop-off rate. This means the most urgent business problem is to reduce early-stage purchase friction on the product-view stage. The analysis also shows that desktop is the most important segment to prioritize first because it combines the highest traffic and revenue base with the largest estimated recovery opportunity at roughly 9.15K.

### 2. Desired outcome

The goal is to improve conversion and revenue by reducing loss at the product-view-to-cart stage, starting with the segment where improvement is likely to create the greatest business return. In practical terms, the desired outcome is to increase desktop add-to-cart behavior without damaging downstream performance such as purchase conversion or average order value. This keeps the project focused on a business decision, not just KPI reporting.

### 3. Constraints, assumptions, and risks

This analysis identifies where the problem is happening, but it does not directly prove the exact cause. The likely explanations could be product-page friction, weak add-to-cart visibility, unclear pricing or shipping information, low-intent traffic, or a weaker product detail page experience on desktop. The recommendation should be treated as a prioritized starting point rather than final proof of root cause. The main risk is acting too broadly, for example redesigning checkout first, even though the evidence shows the largest drop happens earlier in the journey.

### 4. Stakeholders and what they need

| Stakeholder          | What they care about                     | What this analysis helps them decide                                                  |
| -------------------- | ---------------------------------------- | ------------------------------------------------------------------------------------- |
| Ecommerce manager    | Revenue growth and conversion efficiency | Which funnel step should be optimized first                                           |
| Product / UX manager | Product page friction and user flow      | Which experience area should be tested first                                          |
| Marketing manager    | Traffic quality by segment               | Whether poor performance is likely caused by low-intent traffic or landing experience |
| Analyst / BI team    | KPI tracking and validation              | Which metrics should be monitored after rollout                                       |

### 5. Prioritization

| Option                                  | Expected impact | Effort | Confidence from current evidence | Priority |
| --------------------------------------- | --------------- | -----: | -------------------------------: | -------: |
| Desktop product-page optimization       | High            | Medium |                             High |        1 |
| Traffic-source / landing-page drilldown | Medium          | Medium |                           Medium |        2 |
| Checkout redesign                       | Medium          |   High |                    Low to medium |        3 |

### 6. Recommended Action

The business should prioritize desktop product-page optimization at the View Item → Add to Cart step as the first improvement initiative.

This recommendation is based on three factors already supported by the analysis:

the largest funnel loss occurs at View Item → Add to Cart
desktop represents the largest business-value recovery opportunity
fixing the earlier-stage leak is likely to be more valuable than starting with checkout changes when the main drop-off occurs before checkout begins

In practical terms, the first round of business action should focus on hypotheses such as:

weak or less visible Add to Cart calls-to-action on desktop
product-page friction that slows decision-making
unclear pricing, shipping, or value communication before cart entry
desktop layout differences that reduce buying intent compared with mobile

These are still hypotheses, not proven root causes. The current project identifies where optimization should begin; the next phase would test why this step is underperforming.

### 8. Success Measures

To evaluate whether the recommended action is working, the business should track:

Primary metric

Desktop View Item → Add to Cart conversion rate

Secondary metrics

Desktop purchase conversion rate
Desktop revenue per session
Desktop average order value

Operational review window

First 2–4 weeks after rollout, then compare against baseline

## SQL Tables Used

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
