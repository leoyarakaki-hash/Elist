# Elist E-Commerce Sales Analysis (2019–2022)

## Table of Contents
- [Project Background](#project-background)
- [Data Structure](#data-structure)
- [Executive Summary](#executive-summary)
- [Insights Deep-Dive](#insights-deep-dive)
  - [Overall Sales Trend](#overall-sales-trend)
  - [Year-over-Year Growth](#year-over-year-growth)
  - [Regional Performance](#regional-performance)
  - [Loyalty Program](#loyalty-program)
  - [Refund Analysis](#refund-analysis)
- [Recommendations](#recommendations)
- [Assumptions & Caveats](#assumptions--caveats)

---

## Project Background

Elist is an e-commerce company founded in 2018 selling consumer electronics across global markets. The company offers popular electronics products and operates a loyalty program alongside standard customer accounts.

Despite having access to transactional data from 2019 to 2022, performance had historically been tracked in isolation without a unified view across sales trends, regional distribution, loyalty behavior, and product returns. This project delivers an analysis of Elist's order data answering the following core business questions:

- **What were the overall trends in sales during 2019-2022?**
- **What were the growth rates?**
- **How is the loyalty program performing?**
- **What were the refund rates?**

The Tableau Public dashboard can be accessed **[here](https://public.tableau.com/app/profile/leonardo.otake.arakaki/viz/Elist_17744524847660/Dashboard1?publish=yes)** 

---

## Data Structure

Elist's dataset consists of two tables with a total of **108,127 orders** spanning 2019–2022. The EOD can be accessed **[here](##)** 

---

## Executive Summary

Between 2019 and 2022, Elist processed **108,127 orders** generating **$28.1M in total revenue** at an approximate average order value of **$260**. The business experienced COVID-driven surge in 2020, followed by a sustained decline through 2021 and 2022. Critically, the nature of the decline differs by year — 2021's revenue drop was driven by AOV compression while order volume actually grew, whereas 2022 saw a full collapse in both volume and pricing. The loyalty program shows a significant retention gap, with 82% of returning customers not enrolled in the program. Apple products refund rates are higher than non-apple products, but numbers are declining. 

---

## Insights Deep-Dive

### Overall Sales Trend

![Monthly Sales Trend](images/monthly_sales_trend.png)

- **Pre-COVID 6-month average (Sep 2019 – Feb 2020): $415K per month.** Revenue was growing steadily but modestly in the lead-up to the pandemic.
- **Post-COVID 6-month average (Mar 2020 – Aug 2020): $845K per month — a +104% increase.** The surge reflects accelerated digital adoption and increased consumer electronics demand as remote work and home entertainment became priorities.
- **Revenue peaked in December 2020 at $1,246,007** — the highest single month in the dataset — driven by holiday demand compounding the COVID-19 effect.
- **The last 6-month average (Jul – Dec 2022): $318K** — below pre-COVID levels, suggesting the business was unable to sustain the gains made during the pandemic period, revealing the need to improve client retention and attraction. 

---

### Year-over-Year Growth

![YoY Growth Rates](images/yoy_growth.png)

The YoY decomposition reveals that 2021 and 2022 represent fundamentally different business problems:

| Year | Revenue | Orders | AOV |
|---|---|---|---|
| 2019 | $3.9M | 14,294 | $271 |
| 2020 | $10.2M | 28,907 | $351 |
| 2021 | $9.1M | 30,733 | $297 |
| 2022 | $5.0M | 18,966 | $261 |

- **2020 → 2021:** Revenue fell -10.1% despite order count growing +6.3%. The driver was AOV compression of -15.4% — customers kept buying but spent less per order. This is a pricing and product mix problem, not a demand problem.
- **2020 → 2022:** Revenue collapsed -45.7% driven by both a -38.3% drop in order count and a further -12.0% AOV decline. This represents a full demand contraction and requires a fundamentally different response than the 2021 issue.

---

### Regional Performance

![Regional Scatter](images/regional_scatter.png)

- **North America dominates at 51.8% of total revenue ($14.6M)** with 55,805 orders — consistent with it being the company's primary market.
- **EMEA contributes 29.2% ($8.2M)** and represents the largest international opportunity, with an AOV ($259) nearly matching NA ($260).
- **APAC shows the highest AOV at $279** despite being the third-largest region by revenue ($3.7M) — suggesting a premium customer profile that may warrant targeted investment.
- **LATAM has the lowest AOV ($231) and smallest revenue share (6.0%)** — currently underdeveloped relative to its population potential.

---

### Loyalty Program

![Loyalty Revenue](images/loyalty_revenue.png)
![Returning Customers](images/returning_customers.png)

- **The loyalty program generated near-zero revenue in 2019**, ramping significantly from mid-2020 as the program matured during the COVID period.
- **By 2021, loyal and non-loyal revenue lines converge and decline in parallel** — the program failed to provide a protective buffer against the broader revenue decline, suggesting it did not meaningfully change customer purchase behavior.
- **Non-loyal customers account for 61% of total revenue ($17.1M)** despite the program existing across the full analysis period.
- **Of 4,876 returning customers, 88% (4,244) are not enrolled in the loyalty program.** These customers are already demonstrating repeat purchase behavior without any incentive — they represent the highest-value conversion opportunity for the loyalty team.
- Only 18% of loyal customers made more than one purchase, compared to 82% of non-loyal returning customers — the program is not effectively driving repeat behavior among its own members.

---

### Refund Analysis

![Refund Heatmap](images/refund_heatmap.png)
![Refund Count and AOV](images/refund_aov.png)

- **Macbook Air has the highest refund rate across all products**, reaching 22% in 2019 and 19.8% in 2020 — nearly 3x the non-Apple average of 6–9% in those years.
- **All Apple products showed significant refund rate improvement from 2020 to 2021:** Macbook Air dropped from 19.8% to 7.5%, AirPods from 11.2% to 4.8%, iPhone from 13.1% to 6.1%.
- **The AOV of refunded orders is consistently lower than kept orders** across all Apple products — suggesting customers who return products may have purchased during promotional periods or made impulse purchases at discounted prices.
- **Loyal customers refund at a slightly higher rate (7.5%) than non-loyal customers (6.3%)** — counter-intuitive and worth monitoring as it may indicate the loyalty program is attracting trial behavior rather than committed purchasing.

---

## Recommendations

### Revenue Recovery (Leadership & Commercial Team)
- **Diagnose the AOV compression in 2021 separately from the volume collapse in 2022.** These require different responses — AOV compression suggests a product mix or pricing issue, while volume collapse suggests a demand generation or retention problem. Treating them as the same problem risks misallocating resources.
- **Investigate the Dec 2020 peak drivers** to understand whether any were replicable — if specific campaigns or product launches drove the spike, those levers may still be available.

### Loyalty Program (CRM & Marketing Team)
- **Prioritize enrolling returning non-loyal customers.** 4,244 customers are already coming back without incentive — a targeted enrollment campaign for this segment would likely yield the highest ROI of any loyalty initiative.
- **Review loyalty program mechanics.** The data shows loyal members have lower repeat purchase rates than non-loyal returning customers — the program may need restructuring to reward frequency rather than just enrollment.

### Refund Reduction (Operations & Product Team)
- **Investigate the Macbook Air refund root cause.** At 18–22% in 2019–2020, this is an outlier that warrants a qualitative review of return reasons — whether driven by product quality, expectation mismatch, or fulfillment issues.
- **Validate 2022 refund data before using it in reporting.** The 0% figure across all products is statistically improbable and should be confirmed with the data engineering team before drawing any operational conclusions.

### Regional Expansion (Growth & Strategy Team)
- **APAC's premium AOV ($279) warrants further investment.** The region's customers spend more per order than any other region despite lower volume — understanding what's driving this could inform product positioning globally.
- **LATAM remains underdeveloped** relative to population size. Before investing, a market assessment comparing Elist's product mix to local purchasing power and competitor presence would clarify whether the opportunity is structural or addressable.

---

## Assumptions & Caveats

- **Region assignment:** North American countries (US, Canada, and Caribbean territories) had null region values in the source data. These were assigned to "NA" using a calculated field in Tableau based on country code mapping.
- **Refund rate calculation:** Refund rate is calculated as `SUM(REFUNDED) / COUNTD(ORDER_ID)`. The `REFUNDED` field is a binary flag (0/1) — any order with a non-null `REFUND_TS` is counted as refunded.
- **2022 refund anomaly:** All products show 0% refund rates in 2022. This is treated as a data quality issue throughout this analysis and excluded from refund trend conclusions.
- **Returning customer definition:** A customer is classified as returning if they have more than one distinct order in the dataset across the full 2019–2022 period.
- **AOV calculation:** AOV is calculated as `SUM(USD_PRICE) / COUNTD(ORDER_ID)` — it reflects average revenue per order, not per item, as the dataset does not include item-level quantity data.
- **COVID-19 reference date:** March 2020 is used as the COVID-19 marker, aligned with the WHO's pandemic declaration date.
- **All products show 0% refund rates in 2022.** This requires validation — it is likely a data completeness issue (refunds not yet recorded) rather than a genuine operational improvement. This should be flagged before using 2022 refund data in any business decision.
