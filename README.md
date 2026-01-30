# FY 2024 Budget Performance Dashboard (Power BI)
##📊 Project Overview

This Power BI dashboard simulates a real-world FP&A reporting scenario focused on tracking Actual vs. Budget performance, analyzing variance trends, and answering a core finance question:

“Are we on track, and how is performance evolving over time?”

The project emphasizes financial storytelling, clean data modeling, and executive-ready design—prioritizing clarity over visual noise.

##❓ What This Dashboard Answers

- Are we over or under budget YTD?
- Which months contributed most to unfavorable variance?
- Is performance improving or deteriorating toward year-end?
- How large is the variance—and is it material?
- Can an executive understand the story in under 10 seconds?

##📌 Key Takeaways (FY 2024)

- Actuals: ~$28.17M

- Budget: ~$28.22M

- Variance: –$50K (–0.2%)

Performance dipped mid-year but showed a clear recovery in Q4, indicating improved budget discipline toward year-end.

##🧱 Data Model & Architecture

The model follows best-practice star schema design to ensure accuracy, scalability, and clean filtering behavior.

Tables
 - Fact_FPA
    . Actual $
    . Budget $
    . Variance $
    . Variance %
    . Department

DimMonth
    . One row per month
    . Properly sorted Year-Month field

DimDate
    . Supporting calendar logic for future expansion

All relationships are one-to-many, and calculations are handled using explicit measures to avoid hidden aggregations.

##🧮 Key Measures (DAX)

All calculations are measure-driven for transparency and reuse:
- Actual $
- Budget $
- Variance $
- Variance %
- YTD Actual
- YTD Budget
- YTD Variance

Favorable / Unfavorable indicator

##🎨 Visual Design Choices (Intentional)

Combo Chart (Columns + Line)

 - Columns: Actual vs. Budget

 - Line: Variance % (secondary axis)

KPI Cards

 - Summarize YTD performance at a glance

Design Principles

 - Muted color palette suitable for finance leadership
 - Red used only to highlight unfavorable variance
 - Minimal axis labeling to reduce visual noise

Goal: clarity over decoration.

##🔄 Interactivity
- Department slicer enables quick scenario analysis
- Tooltips provide month-level context without clutter
- Dashboard tiles link back to the full interactive report

##🌐 Live Dashboard

🔗 Power BI Public Report:
👉 (https://app.powerbi.com/view?r=eyJrIjoiYjNiOThkOGItMWUxZC00ZmIxLWEwOWMtOGFjNjc5MmRmYzUwIiwidCI6ImRkMjQ2ZTRhLTU0MzQtNGUxNS04YWUzLTkxYWQ5Nzk3YjIwOSIsImMiOjN9)

Note: Data is simulated and used strictly for portfolio demonstration purposes.

##🛠️ Tools Used
. Power BI Desktop & Power BI Service
. DAX
. Power Query
. Data modeling (star schema)
. Financial analytics & FP&A concepts

##🎯What This Project Demonstrates
This project reflects how FP&A dashboards are used in real organizations to monitor performance against plan:
- Budget vs. actual variance analysis at a monthly and YTD level
- Clear separation of performance totals and gap metrics for executive consumption
- Clean dimensional modeling to support time-based analysis
- Visual storytelling focused on decision-making, not decoration
- The dashboard is designed to support management review conversations rather than exploratory analysis.

##🚀WWhat I’d Build Next
- Department-level drill-through analysis
- Forecast vs Actual comparisons
- Rolling 3-month and quarterly variance views
- Variance driver analysis
