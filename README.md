📊 FinEdge Solutions — Financial Performance Dashboard

📌 Business Problem

FinEdge Solutions, a B2B SaaS fintech company, had three years of financial transaction data across multiple departments, regions, and revenue streams. However, leadership lacked a structured view of profitability, cost control, and revenue sustainability.

Without a consolidated financial view, the business could not answer critical questions:

Which departments are overspending against budget?

Is revenue growth translating into sustainable margins?

How dependent is the business on recurring revenue?

Is the 2024 revenue decline temporary or structural?

This analysis answers three executive questions:

Is the business operating within a healthy margin range?

Where are the most critical budget overruns?

What is driving changes in revenue performance?

🎯 Key Findings

Revenue & Profitability:
Revenue reached $911M across FY2022–2024 with a 24.5% operating margin, within the healthy SaaS benchmark range. Revenue peaked in 2023 before declining in 2024, indicating a potential market-level correction.

Budget Variance:
Marketing exceeded budget by 32%, the highest across departments, followed by Operations (14%) and Technology (8%). Other departments remained within budget, suggesting localized cost inefficiencies rather than systemic issues.

Recurring Revenue Strength:
50.6% of revenue is recurring, exceeding industry benchmarks and providing predictable cash flow.

Operational Efficiency:
Sales generates $11.3M revenue per employee, significantly outperforming other departments, highlighting strong return on headcount investment.

💼 Business Recommendations

Immediate Actions:

Audit Marketing and Operations spend to address budget overruns

Investigate 2024 revenue decline using churn, renewal, and pipeline data

Resolve unclassified transactions to improve reporting accuracy

Review Technology cost structure under declining revenue conditions

Strategic Direction:

Track Operating Margin and Recurring Revenue as core KPIs

Implement rolling revenue trend monitoring

Introduce department-level budget tracking for ongoing control

Expand reporting to multi-currency analysis

🔍 Analytical Approach

Data Preparation (Power Query):

Standardised inconsistent department names using mapping logic

Cleaned multiple date formats and derived time dimensions

Identified and excluded outliers and reversal transactions

Flagged missing and unclassified records for transparency

Scoped analysis to USD transactions for consistency

Financial Analysis (DAX):

Built Total Revenue and Total Expenses using controlled filters

Calculated Gross Profit and Operating Margin using safe logic

Derived Variance and Variance % from actual vs budget values

Computed Revenue per Employee for efficiency analysis

Measured Recurring Revenue % to assess business stability

Analysis Focus:

Department-level budget variance and cost control

Revenue stream contribution and concentration

Operational efficiency across departments

Quarterly revenue movement across fiscal years

Visualization:

Designed executive-level dashboard with KPI-first layout

Used consistent color logic for performance interpretation

Combined trend, comparison, and ranking visuals

Structured layout for quick executive decision-making

📊 Data Overview

Each row represents a single financial transaction.

Column Name	Description
Transaction_ID	Unique transaction identifier
Transaction_Date	Date of transaction
Fiscal_Year	Financial year
Quarter	Derived time period
Department	Standardized department name
Category	Revenue or Expense
Sub_Category	Transaction type
Region	Geographic region
Currency	Transaction currency
Actual_Amount	Transaction value
Budget_Amount	Planned budget
Is_Recurring_Revenue	Recurring revenue flag
Dept_Headcount	Department headcount
Transaction_Status	Transaction state

Time Period: FY2022–FY2024
Rows: 14,280

🛠 Technical Stack

Power BI Desktop

Power Query (M)

DAX

Excel / CSV

GitHub

⚠️ Limitations

Analysis limited to USD transactions

Unclassified transactions remain unresolved

No customer or marketing attribution data

External market factors not included

Headcount data is annual, not dynamic

🔮 Future Enhancements

Add multi-currency support with exchange rates

Build rolling revenue and margin trends

Introduce row-level security for departments

Incorporate churn and renewal data

Automate monthly reporting pipeline

🔗 Connect

LinkedIn: https://www.linkedin.com/in/rahul-bhagat-6439853b4/?trk=opento_sprofile_topcard
