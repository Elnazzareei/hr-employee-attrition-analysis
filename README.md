# HR-Employee-Attrition-Analysis
Excel-based analysis of employee attrition drivers using the IBM HR Analytics dataset — pivot tables, chi-square significance testing, and an interactive dashboard.
# Objective
Determine the key drivers of employee attrition and identify high-risk employee segments to help HR prioritize retention strategies.
# Dataset
IBM HR Analytics Employee Attrition & Performance (Kaggle),
A fictional dataset created by IBM data scientists, containing 1,470 employee records across 35 attributes including demographics, compensation, job role, satisfaction scores, and attrition status.
# Workflow
1-Data Cleaning
Removed constant/non-informative columns (EmployeeCount, Over18, StandardHours),
Converted Attrition (Yes/No) to a numeric flag (0/1) for pivot table calculations.
2-Feature Engineering
Created binned categorical variables from continuous fields to enable meaningful group comparisons:
AgeBand (18-25, 26-35, 36-45, 46+),
TenureBand (0-2, 3-5, 6-10, 10+ years),
DistanceFromHomeBand (Short, Medium, Long),
MonthlyIncome grouped into bands via pivot table grouping.
3-Exploratory Analysis (Pivot Tables)
Built pivot tables calculating attrition rate (Average of Attrition) across 8 dimensions: OverTime, Job Role, Department, Age Band, Tenure Band, Income Band, Distance From Home, Business Travel.
4-Statistical Testing
Ran chi-square tests of independence on each dimension to validate whether observed differences in attrition rate were statistically significant (vs. due to chance)
All 8 tested variables showed statistically significant relationships with attrition (p < 0.05).
5-Dashboard Design
Built an interactive Excel dashboard with KPI cards, 8 pivot charts, cross-filtering slicers (Gender, OverTime, Distance, Department), and a significance summary table
Applied consistent formatting (percentage axes, sorted rankings, dark theme) for a business-ready presentation.
# Tools Used
Microsoft Excel — Pivot Tables & Pivot Charts, Data Analysis ToolPak (CHISQ.TEST), Slicers, structured Tables.
# Key findings (all statistically validated via chi-square tests, p<0.05):
Overtime is the single strongest driver. Employees working overtime leave at 3x the rate of those who don't (31% vs. 10%).
Tenure and age compound the risk. Employees in their first 2 years show 30% attrition, and those aged 18–25 show 36% — new, young employees are the highest-risk segment.
Compensation matters. Attrition falls from 25% in the lowest income band to under 10% in higher bands.
Role concentration is severe. Sales Representatives show 40% attrition — roughly 13x higher than Research Directors (3%).
Travel and department add secondary risk. Frequent travelers (25%) and Sales/HR departments (19–21%) show elevated attrition versus their counterparts.
# Recommendation: 
HR should prioritize retention interventions on the compound-risk segment (overtime + long commute alone accounts for 101 employees) — starting with a review of overtime policy and compensation structure in the lowest income bands, since these show the largest, most statistically robust effects.
