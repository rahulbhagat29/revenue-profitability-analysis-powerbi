📊 Financial Performance & Profitability Analysis (Power BI)

Why did revenue grow 58% and then drop 39% — and which departments caused it?

📌 Business Problem

FinEdge Solutions, a B2B SaaS fintech company, had three years of financial transaction data across departments, regions, and revenue streams. However, leadership lacked a clear view of profitability, cost control, and revenue sustainability.

Without a structured financial view, the business could not answer:

Which departments are overspending and impacting margins?

Is revenue growth translating into sustainable profitability?

How dependent is the business on recurring revenue?

Is the 2024 revenue decline temporary or structural?

🎯 Key Findings

Revenue & Profitability
Revenue reached $911M with a 24.5% operating margin, within healthy SaaS benchmarks. Revenue peaked in 2023 before declining in 2024, indicating a potential market correction.

Budget Variance (Critical Insight)
Marketing exceeded budget by 32%, Operations by 14%, and Technology by 8%. Other departments remained within budget, indicating localized inefficiencies rather than systemic failure.

Recurring Revenue Strength
50.6% of revenue is recurring, providing predictable and stable income streams.

Operational Efficiency
Sales generates $11.3M revenue per employee, significantly outperforming all other departments.

💼 Business Impact

Identified cost overruns in Marketing and Operations, enabling targeted cost control

Highlighted strong dependency on recurring revenue, improving financial predictability

Exposed efficiency gaps across departments, guiding resource allocation

Provided a clear direction for profitability improvement and budget discipline

🔍 Analytical Approach

Data Preparation (Power Query)

Standardized inconsistent department names

Cleaned mixed date formats and derived time dimensions

Removed reversals, duplicates, and statistical outliers

Flagged unclassified and missing values for transparency

Scoped analysis to USD transactions

Financial Analysis (DAX)

Built Total Revenue, Expenses, and Profit measures

Calculated Operating Margin using safe DIVIDE logic

Derived Budget Variance and Variance %

Computed Revenue per Employee for efficiency analysis

Measured Recurring Revenue %

Analysis Focus

Department-level cost control

Revenue stream contribution

Budget variance and risk

Operational efficiency

Year-over-year revenue movement

📊 Dashboard Overview

Sections Covered:

KPI Overview → Revenue, Profitability, Margin

Trend Analysis → Revenue vs Expenses

Budget Control → Department variance

Revenue Drivers → Stream contribution

Efficiency → Revenue per employee

📊 Data Overview

Each row represents a financial transaction.

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
Total Records: 14,280

🛠 Technical Stack

Power BI Desktop

Power Query (M)

DAX

Excel / CSV

GitHub

⚠️ Limitations

Analysis limited to USD transactions

Unclassified transactions remain unresolved

No marketing attribution data available

External macroeconomic factors not included

Headcount data is annual, not dynamic

🔮 Future Enhancements

Add multi-currency reporting with exchange rates

Implement rolling 12-month trend analysis

Introduce row-level security for departments

Incorporate churn and renewal data

Automate monthly reporting pipeline

👤 Author

Rahul Bhagat
Aspiring Data Analyst | Finance & E-commerce Focus
