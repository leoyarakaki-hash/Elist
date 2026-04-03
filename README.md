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
- **What were the refund rates accross Apple products?**

The Tableau Public dashboard can be accessed **[here](https://public.tableau.com/app/profile/leonardo.otake.arakaki/viz/Elist_17744524847660/Dashboard1?publish=yes)** 

---

## Data Structure

Elist's dataset consists of two tables with a total of **108,127 orders** spanning 2019–2022. The EOD can be accessed **[here](https://github.com/leoyarakaki-hash/Elist/blob/main/images/EOD.png)** 

---

## Executive Summary

Between 2019 and 2022, Elist processed **108,127 orders** generating **$28.1M in total revenue** at an approximate average order value of **$260**. The business experienced COVID-driven surge in 2020, followed by a sustained decline through 2021 and 2022. Critically, the nature of the decline differs by year — 2021's revenue drop was driven by AOV compression while order volume actually grew, whereas 2022 saw a full collapse in both volume and pricing. The loyalty program shows a significant retention gap, with 82% of returning customers not enrolled in the program. Apple products refund rates are higher than non-apple products, but numbers are declining. 

<img width="1450" height="943" alt="image" src="https://github.com/user-attachments/assets/7179e56d-5158-406f-bd0a-44758e8c7557" />
<img width="1445" height="945" alt="image" src="https://github.com/user-attachments/assets/53e1ad2a-5013-4c0a-aa24-6fcc76032d1d" />

---

## Insights Deep-Dive

### Overall Sales Trend

<img width="1909" height="943" alt="image" src="https://github.com/user-attachments/assets/92d2131f-7f35-4190-b84c-83aff87314d2" />


- **Pre-COVID 6-month average (Sep 2019 – Feb 2020): $415K per month.** Revenue was growing steadily but modestly in the lead-up to the pandemic.
- **Post-COVID 6-month average (Mar 2020 – Aug 2020): $845K per month — a +104% increase.** The surge reflects accelerated digital adoption and increased consumer electronics demand as remote work and home entertainment became priorities.
- **Revenue peaked in December 2020 at $1,246,007** — the highest single month in the dataset — driven by holiday demand compounding the COVID-19 effect.
- **The last 6-month average (Jul – Dec 2022): $318K** — below pre-COVID levels, suggesting the business was unable to sustain the gains made during the pandemic period, revealing the need to improve client retention and attraction. 

---

### Year-over-Year Growth

<img width="1423" height="264" alt="image" src="https://github.com/user-attachments/assets/1f4d4b1f-fdb2-455a-a7d3-72f5e092ce4a" />

The YoY decomposition reveals that 2021 and 2022 represent fundamentally different business problems:

<div align="center">
  
| Year | Revenue | Orders | AOV |
|---|---|---|---|
| 2019 | $3.9M | 14,294 | $271 |
| 2020 | $10.2M | 28,907 | $351 |
| 2021 | $9.1M | 30,733 | $297 |
| 2022 | $5.0M | 18,966 | $261 |
</div>


- **2020 → 2021:** Revenue fell -10.1% despite order count growing +6.3%. The driver was AOV compression of -15.4% — customers kept buying but spent less per order. This potentially is a pricing and product mix problem.
- **2020 → 2022:** Revenue collapsed -45.7% driven by both a -38.3% drop in order count and a further -12.0% AOV decline. This represents a full demand contraction and requires a different response than the 2021 issue.

---

### Regional Performance

<div align="center">
<img width="706" height="619" alt="image" src="https://github.com/user-attachments/assets/2d69bf61-43f1-4030-8aac-9108b175f416" />
</div>

- **North America (NA) dominates at 51.8% of total revenue ($14.6M)** with 55,805 orders — consistent with it being the company's primary market.
- **Europe, Middle East, and Africa (EMEA) contributes 29.2% ($8.2M)** and represents the largest international opportunity, with an AOV ($259) nearly matching NA ($260).
- **Asia-Pacific (APAC) shows the highest AOV at $279** despite being the third-largest region by revenue ($3.7M) — suggesting a premium customer profile that may warrant targeted investment.
- **Latin America (LATAM) has the lowest AOV ($231) and smallest revenue share (6.0%)** — currently underdeveloped relative to its population potential.

---

### Loyalty Program

<div align="center">
<img width="705" height="556" alt="image" src="https://github.com/user-attachments/assets/f49438dc-0532-4c53-9d2f-5e5102e7765b" />
</div>

- **The loyalty program generated near-zero revenue in 2019**, ramping significantly from mid-2020 as the program matured during the COVID period.
- **By 2021, loyal and non-loyal revenue lines converge and decline in parallel** — the program failed to provide a protective buffer against the broader revenue decline, suggesting it did not meaningfully change customer purchase behavior.
- **Non-loyal customers account for 61% of total revenue ($17.1M)** despite the program existing across the full analysis period.
- **Of 5,940 returning customers, 82% (4,876) are not enrolled in the loyalty program.** These customers are already demonstrating repeat purchase behavior without any incentive — they represent the highest-value conversion opportunity for the loyalty team. Also it shows that the **loyalty program is not effective** in helping customers make a second purchase, which is the main reason for such a program.

---

### Refund Analysis
<div align="center">
<img width="700" height="224" alt="image" src="https://github.com/user-attachments/assets/7e5e9b66-bef1-4e57-90ad-76472f0dbc66" />
</div>
<div align="center">
<img width="700" height="304" alt="image" src="https://github.com/user-attachments/assets/f7013941-ba9b-4c8d-a901-baea91452fb0" />
</div>

- **Macbook Air has the highest refund rate across all products**, reaching 22% in 2019 and 19.8% in 2020 — nearly 3x the non-Apple average of 6–9% in those years.
- **All Apple products showed significant refund rate improvement from 2020 to 2021:** Macbook Air dropped from 19.8% to 7.5%, AirPods from 11.2% to 4.8%, iPhone from 13.1% to 6.1%.
- **The AOV of refunded orders is consistently higher than kept orders** across all Apple products. Suggesting customers who return products may have purchased during promotional periods or made impulse purchases at discounted prices.

---

## Recommendations

### Revenue Recovery
- **Diagnose the AOV compression in 2021 separately from the volume collapse in 2022.** AOV compression suggests a product mix or pricing issue, while volume collapse suggests a demand generation or retention problem. Treating them as the same problem risks misallocating resources.
- **Investigate the Dec 2020 peak drivers** to understand whether any were replicable — if specific campaigns or product launches drove the spike or if it was driven by seasonal purchases and COVID-19 adaptation needs.

### Loyalty Program
- **Prioritize enrolling returning non-loyal customers.** 4.876 customers are already coming back without incentive. A targeted enrollment campaign for this segment could help the retention of these clients. 
- **Review loyalty program mechanics.** The data shows loyal members have lower repeat purchase rates than non-loyal returning customers. The program may need restructuring to reward frequency rather than just enrollment.
- **Create a new client attraction program.** Since sales decreased in AOV and quantity there is a urgent need to attract new clients on top of rewarding and retaining existing ones.

### Refund Reduction (Operations & Product Team)
- **Investigate the Macbook Air refund root cause.** At 18–22% in 2019–2020, this is an outlier that warrants a qualitative review of return reasons. With Apple being a reputable and well known brand there might have been some fulfillment issues driving those high numbers.
- **Investigate the higher AOV for refunded products.** This may indicate that customers are making impulse purchases over promotional periods or taking advantage of the return policy.

### Regional Expansion (Growth & Strategy Team)
- **APAC's premium AOV ($279) warrants further investment.** The region's customers spend more per order than any other region despite the second lowest volumw. Understanding what's driving this could inform product positioning globally and represent a great opportunity in acquiring new clients since it is the most populated region in the world. 
- **LATAM remains underdeveloped** relative to population size. Before investing, a market assessment comparing Elist's product mix to local purchasing power and competitor presence would clarify whether the opportunity is addressable.

---

## Assumptions & Caveats

- **Region assignment:** Some North American countries had null region values in the source data. These were assigned to "NA".
- **2022 refund anomaly:** All products show 0% refund rates in 2022. This is treated as a data quality issue throughout this analysis and excluded from refund trend conclusions.
- **Returning customer definition:** A customer is classified as returning if they have more than one distinct order in the dataset across the full 2019–2022 period.
- **AOV calculation:** It reflects average revenue per order, not per item, as the dataset does not include item-level quantity data.
- **COVID-19 reference date:** March 2020 is used as the COVID-19 marker.
