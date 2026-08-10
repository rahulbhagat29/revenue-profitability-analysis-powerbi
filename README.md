# 📊 FinEdge Solutions — Financial Performance Dashboard

## 📌 Business Problem

FinEdge Solutions, a B2B SaaS fintech company, had three years of financial transaction data across 8 departments, 5 global regions, and multiple revenue streams. However, leadership lacked structured visibility into whether expenses were under control, which departments were destroying margin, and whether the 2024 revenue decline was a temporary correction or a structural problem.

Without a clean, consolidated financial view, the company could not answer critical profitability questions:

- Which departments are consistently overspending their budgets?
- Is revenue growth translating into sustainable operating margin?
- Are recurring revenue streams healthy enough to support future planning?
- Where should leadership cut or invest heading into the next fiscal year?

This analysis answers three critical executive questions:

- Is the business operating within a healthy margin benchmark?
- Where are the budget overruns and how severe are they?
- Is the 2024 revenue decline department-specific or market-wide?

---

## 🎯 Key Findings

<img width="2718" height="1352" alt="Executive Summary" src="https://github.com/user-attachments/assets/bbec6c0e-00b6-492e-8733-b906f48dbccd" />

**Revenue Performance:** Total revenue reached $911M across FY2022–2024 with an Operating Margin of 24.5%, sitting within the healthy SaaS benchmark of 20–28%. Revenue peaked at $410M in 2023 — a 58% increase over 2022 — before declining 39% in 2024, signalling a market-level correction across all revenue departments simultaneously.

<img width="2706" height="1345" alt="Trade   Variance" src="https://github.com/user-attachments/assets/5853f32d-f37e-4fd2-808b-7c56574a2eb5" />

**Budget Variance — Critical Finding:** Marketing overspent its expense budget by 32%, the largest variance across all departments. Operations overspent by 14% and Technology by 8%. Customer Success and Sales came in under budget, demonstrating disciplined cost management.

**Recurring Revenue Health:** 50.6% of total revenue is recurring — Subscription Fees, Renewal Revenue, and New ARR — exceeding the 40% SaaS benchmark and providing leadership with a predictable cash flow base for planning.

<img width="2703" height="1348" alt="Department Deep Dive" src="https://github.com/user-attachments/assets/339ad578-c7b0-4f8f-9f25-e262edf150c0" />

**Revenue per Employee:** Sales generates $11.3M revenue per employee — more than 3x the next department — confirming that Sales headcount delivers the highest return on people investment across the organisation.

---

## 💼 Business Recommendations

**Immediate Actions:**

- Audit Marketing spend immediately — a 32% budget overrun in a pure cost centre with no direct revenue contribution is not sustainable heading into FY2025
- Investigate the 2024 revenue decline through churn rates, contract renewal data, and pipeline coverage ratios to determine whether this is cyclical or structural
- Resolve 628 unclassified transactions at source — this data governance gap will compound every reporting cycle until addressed
- Review Technology cost structure — expense overspend combined with revenue decline in 2024 creates compressing net contribution from both sides

**Strategic Direction:**

- Adopt Operating Margin and Recurring Revenue % as primary KPIs alongside total revenue
- Introduce rolling 12-month revenue trend tracking for forward-looking momentum assessment
- Implement department-level budget variance dashboards for monthly CFO review
- Build an exchange rate table to bring EUR, GBP, and AED transactions into scope for global reporting

---

## 🔍 Analytical Approach

**Data Cleaning (Power Query — 9 Issues Resolved):**

- Standardised 36 department name variants into 8 clean names using a lookup table merge
- Parsed 6 mixed date formats (ISO, DD-MM-YYYY, MM-DD-YYYY, DD-Mon-YY, slash format) using a custom M parsing function
- Derived Quarter directly from Transaction_Date to correct 2.5% of wrong entries in the raw Quarter column
- Flagged 7% missing Budget_Amount rows rather than imputing — excluded from variance calculations only
- Isolated 629 blank Category rows as Unclassified — data governance gap, not a cleaning decision
- Separated 140 documented reversals from revenue using Notes column cross-reference
- Removed 10 duplicate Transaction IDs inflating revenue and expense totals
- Scoped analysis to USD transactions — 4 currencies present with no exchange rate table
- Flagged outlier transactions above 3 standard deviations for exclusion from expense aggregates

**Revenue & Margin Analysis (DAX):**

- Built Total Revenue and Total Expenses measures with explicit filters for Completed status, USD scope, and positive amounts
- Calculated Gross Profit and Operating Margin % using safe DIVIDE logic
- Built Variance and Variance % measures from Actual_Amount and Budget_Amount — not pre-calculated in source data
- Implemented Revenue per Employee and Cost per Employee linking financial output to headcount investment
- Created Recurring Revenue % to track SaaS health against industry benchmark

**Risk & Overspend Analysis:**

- Analysed Budget Variance % by department using conditional colour formatting — red for overspend, blue for under budget
- Evaluated revenue stream concentration across 7 sub-categories to assess dependence risk
- Measured Revenue per Employee across all 4 revenue-generating departments
- Compared quarterly revenue trends across 3 fiscal years to identify seasonality and decline patterns

**Visualisation:**

- Designed a 3-page executive report (Exec Summary, Trend & Variance, Department Deep-Dive) with a custom JSON report theme and button-based page navigation
- Applied a semantic colour system — purple/lavender for revenue and neutral metrics, coral for expenses and budget overrun, green for budget increases — so colour encodes meaning rather than acting as decoration
- Built department and revenue-stream comparison visuals (bar, waterfall, horizontal bar) with year/quarter slicer filtering on the Trend & Variance page
- Presented a balanced mix of KPI cards, trend lines, comparison bars, and ranking charts

---

## 📊 Data Overview

The analysis uses a raw transactional dataset cleaned and transformed entirely within Power Query before loading into the Power BI data model.

Each row represents a single financial transaction record.

**Data Schema (Raw Dataset):**

| Column Name | Description |
| --- | --- |
| Transaction_ID | Unique transaction identifier |
| Transaction_Date | Date of transaction (6 mixed formats — cleaned) |
| Month_Name / Month_Number | Calendar month for trend slicing |
| Fiscal_Year | Financial year (2022, 2023, 2024) |
| Quarter | Derived from Transaction_Date in Power Query |
| Department | Department name (36 raw variants — standardised to 8) |
| Cost_Center | Department cost centre code |
| Category | Revenue or Expense (4.4% blank — isolated as Unclassified) |
| Sub_Category | 25 revenue and expense sub-types |
| Region | 5 global regions |
| Currency | USD, EUR, GBP, AED |
| Actual_Amount | Transaction amount in local currency |
| Budget_Amount | Approved budget amount (7% missing — flagged) |
| Profit_Margin_Pct | Margin % — cross-validated against Actual/Budget |
| Is_Recurring_Revenue | Yes/No flag for ARR calculation |
| Contract_Type | Annual, Monthly, One-time |
| Dept_Headcount | Headcount per department per year |
| Transaction_Status | Completed, Pending, Cancelled, Failed |
| Payment_Method | Bank Transfer, Wire, ACH, Credit Card, Online |
| Approved_By | Approving manager (8.3% missing — flagged) |
| Notes | Free-text audit trail for reversals and approvals |

**Time Period Covered:** FY2022 — FY2024

**Total Rows After Cleaning:** 14,280

---

## 🛠 Technical Stack

- **Power BI Desktop:** Data modeling, dashboard development, conditional formatting, custom JSON report theming, button-based navigation
- **Power Query (M):** Data cleaning, transformation, custom parsing functions
- **DAX:** Financial measures, variance calculations, employee productivity metrics
- **Excel / CSV:** Source dataset preparation and validation
- **GitHub:** Version control and project portfolio hosting

---

## ⚠️ Limitations

- Analysis is scoped to USD-denominated transactions only — EUR, GBP, and AED transactions excluded due to absence of an exchange rate table
- 628 unclassified transactions could not be allocated to Revenue or Expense without business context
- Headcount data is annual — intra-year hiring or departures are not reflected in monthly Revenue per Employee calculations
- No marketing attribution data available to assess ROI on Marketing spend overruns
- External macroeconomic factors contributing to the 2024 revenue decline are not modelled

---

## 🔮 Future Enhancements

- Add an exchange rate dimension table to bring all currencies into scope for global reporting
- Build a rolling 12-month revenue and margin trend for forward-looking momentum tracking
- Implement row-level security so department heads see only their own cost centre data
- Incorporate customer churn and renewal rate data to explain the 2024 revenue decline
- Automate data refresh pipeline for monthly CFO reporting cycle
- Add a budget reforecast model projecting Q3 and Q4 based on H1 actuals and variance trends

---

## 🔗 Connect

**LinkedIn:** https://www.linkedin.com/in/rahul-bhagat-6439853b4/?trk=opento_sprofile_topcard
