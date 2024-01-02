---
aliases:
  - Candid Take home assessment
tags:
  - "status/postponed"
file-created: 2023-10-02
file-modified: 2023-10-10
note-type:
  - general
description: 
linter-yaml-title-alias: Candid Take home assessment
---

%%
Related to
- [[Interview with Candid Co]]
- [[Candid Take home assessment organization]]
%%

# Candid Take home assessment

---

## Agenda

- What is my general framework for problem-solving?
- Dataset exploration
- Answering the [[Candid Take home assessment|assessment]] questions
	- SQL
	- Dashboard review
	- Open ended business questions
- Further discussions

## Problem-solving approach

### Tool selection

- Choice was Google Cloud
	- Similar enough to Amazon RedShift
- Documentation is our friend
	- [Date functions  |  BigQuery  |  Google Cloud](https://cloud.google.com/bigquery/docs/reference/standard-sql/date_functions#date_trunc)
- Alternative was Python, SQLite, SQLite explorer

### Exploring the dataset

- What is the table granularity?
- What are the primary and foreign keys?

![[Data desc for candid.png]]

See also [[Candid Interview Data Relationships.canvas|Candid Interview Data Relationships]]

#### Account loyalty program table

%% - Loyalty tier of an account as well as its time of program applicability %%
- `account_id` and `id` are 1:1 mapping?
- Avoiding collision on `program_start` and `program_end`?

![[Data profiling in BigQuery.png\|800]]

### Creating queries

- Break down the question into small chunks (CTE/Views)
- Quick data spot checks
- Aside: Consider performance bottlenecks of a query

## Part 1 - SQL

### Building a base table

- [Base table view](https://console.cloud.google.com/bigquery?project=candid-interview-400815&ws=!1m5!1m4!4m3!1scandid-interview-400815!2sinterview_answers!3ssql_answer_table) as foundational building block to the questions
- In real work, I would keep some of these CTEs as views.
- Each row represents **ONE individual customer account** (along with its creation date), the date for which its loyalty program applies as well as which tier it belongs.
- For finding out the `account_creation_date` a subquery could have been used.

![[Schema for base SQL answer table.png]]

### Q1

How many new accounts are there per month?

%%
> [!Todo] (Easy) - How many new accounts are there per month?

- [x] Verify SQL Answer 1
%%

- The previous query already truncated the created date into `account_created_year_month`
- Retrieved `account_created_date` using a `min(creation_date)` on the `account_rates` table for each account

[SQL Answer 1](https://console.cloud.google.com/bigquery?project=candid-interview-400815&ws=!1m5!1m4!4m3!1scandid-interview-400815!2sinterview_answers!3snew_accounts_per_month)

![[Answer 1.png|300]]

### Q2

How many accounts in each loyalty tier program where the program happened *during* 4/30/2023?

%%

> [!Todo] How many accounts are in each loyalty tier whose program happened during 4/30/2023

- [x] Verify SQL answer 2

%%

Needs to satisfy two conditions
1. If the `program_start_date` is **before or on** that specific date
2. If the `program_end_date` is **on or after** that specific date

![[Answer 2.png|400]]

[SQL answer 2](https://console.cloud.google.com/bigquery?project=candid-interview-400815&ws=!1m5!1m4!4m3!1scandid-interview-400815!2sinterview_answers!3saccounts_during_period)

### Q3

What are the minimum and maximum case fees (in dollars) per loyalty tier after discounts were applied?

%%

> [!Todo] What are the minimum and maximum case fees (in dollars) per loyalty tier? (applying discounts)

- [ ] Verify SQL answer 3
%%

1. Calculate each case fee as applied
2. From there, return highest and lowest for each tier.
3. Convert the answers to dollars
4. Group by each tier

![[Answer 3.png|400]]

[SQL Answer 3](https://console.cloud.google.com/bigquery?project=candid-interview-400815&ws=!1m5!1m4!4m3!1scandid-interview-400815!2sinterview_answers!3sBounded%2520rates%2520for%2520each%2520loyalty%2520tier)

## Part 2 - Dashboard building

%%
> [!todo] Building dashboard question
> Use any kind of chart that you think might be best to track how many new accounts each loyalty tier there are, aggregated by months (use program start date). (Can use any BI tool)

- [ ] Review dashboard for user-friendliness and ease of reading
%%

![[Candid Assessment dashboard.png|700]]

See also [Candid Dashboard Report](https://lookerstudio.google.com/reporting/2da47036-576a-4088-baf6-d5724d3b0782)

## Part 3 - Open Ended Business Sense Questions

### Trends and observed observations

> [!todo]
> - What are the trends you observed from the data above?
> - If you were to ask to measure the impact of the loyalty tier program, what are some other KPIs you can track with the data above

The primary dimension provided is the loyalty program tier which limits the analysis we can do.

![[Basic descriptive stats - Candid take home assessment.png]]

#### Discount rates

- Discount rates are not **meaningfully different** between tiers.
- Standard has the same rate applied all across while all other tiers have variance.
- Applied rate of Silver is actually more expensive than the Standard tier

#### Account loyalty distribution

- Most accounts are in the Standard tier with few in the Platinum and Diamond tier
- Most accounts take a long time to enter the loyalty program based on their first created date
- October 2022 had a huge influx of new accounts

#### Other KPIs to look at

Other metrics being tracked on the [Candid Dashboard Report](https://lookerstudio.google.com/reporting/2da47036-576a-4088-baf6-d5724d3b0782)

- Average lifespan of loyalty program
- Distribution of the loyalty tier program
- Average rate per tier
- Scatterplot for account_rate vs discount rate (to allow observation of outliers)

---

### Other metrics and expanding on possibilities

> [!todo] Further questions
> - What are some other metrics that you believe might be important, but are not listed above?
> - Can you describe the kind of tracking/dashboard you would like to build to track those metrics?

See also [[Loyalty programs|loyalty programs]].

![[Loyalty programs#Commonly used industry KPIs for loyalty programs]]

#### Customer satisfaction scores (CSAT) and NPS scores

- Are higher loyalty program customers more happy in general and vice-versa? What's the correlation?
- We would need satisfaction survey data
- [Measuring Customer Satisfaction – Dashboard](https://www.tableau.com/data-insights/dashboard-showcase/survey-satisfaction) See Tableau example for what we could do

![[Pasted image 20231004223716.png|600]]

Example of possible dataset `csat_survey`

![[CSAT_Survey data example.png|400]]

---

#### Churn rate

- How many customers are leaving the loyalty program? Depends on how it operates I suppose.

![[Churn rate chart.png|600]]

---

#### Average transaction value per tier

- What's the average transaction value per tier?
	- It would determine if it's better to focus on higher quality versus bigger volume
	- What's the total revenue per tier?

#### Comparing sales revenue

- Do accounts with higher discounts bring in a higher revenue?

![[Sales Revenue Dashboard example - Big book of Dashboard.png|400] from [[The Big Book of Dashboards by Steve Wexler Jeffrey Shaffer Andy Cotgreave|The Big Book of Dashboards by Steve Wexler, Jeffrey Shaffer and Andy Cotgreave]]

#### Loyalty tier movement

- How do people move through the program?
- One of the methods I know how to approach that problem is using Type 2 Slowly Changing Dimensions (SCD) as referenced in the [[The Data Warehouse Toolkit by Ralph Kimball|The Data Warehouse Toolkit by Ralph Kimball]]

---

### Personal comments and general questions

- What is the objective of the Candid loyalty program? How does it work?
	- Increase retention?
	- Generate business development?
	- Increase overall sales volume?
	- Each of these may require alternative solutions which may not be directly answered by a loyalty program
- Why did Candid design a loyalty program?
- How do you currently measure its current effectiveness?

#### Theoretical model of loyalty programs

Under [[Conceptual model of loyalty programs|conceptual models of loyalty programs]]:
- Candid would most likely be considered a high-involvement purchase so direct and immediate rewards would be most effective according to some research.
- According to some recent academic findings, economic discounts are one of the weaker approaches to loyalty programs as it does not lead to long term behavioural attitudinal changes
- Does Candid take into account social contexts for marketing and promotional purposes?
	- Are we involved in industry networking events for oral healthcare professionals?
	- Word-of-mouth effect?

## My questions

- What is the strategy for the upcoming year?
	- Business-wise
	- Technical architecture/data-wise
- Has there been a time where data has challenged company assumptions
