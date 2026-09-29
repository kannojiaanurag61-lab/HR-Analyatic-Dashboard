# HR Analytics Dashboard

A one-page Power BI report on employee headcount and attrition. Filter by gender, marital status, business travel and education, then read the same numbers by age, department, job role and education field.

**File:** `dashboard_1.pbix`  
**Page:** Dashboard (1280 × 720)  
**Data table:** `HR data`

## Dashboard layout

| Area | Visual | Fields |
|---|---|---|
| Top | Title text box | none |
| Top right | Education slicer | Education |
| KPI row | Total Employees card | Total Employees |
| KPI row | Total Attrition card | Total Attrition |
| KPI row | Attrition Rate card | Attrition Rate |
| KPI row | Age card (Sum) | Age |
| KPI row | Active Employee card | Active Employee |
| KPI row | Monthly Income card (Sum) | Monthly Income |
| Left column | Slicers | Gender, Marital Status, Business Travel |
| Middle row | Clustered column chart | Age Group, Gender, Total Employees |
| Middle row | Area chart | Age, Total Attrition |
| Middle row | Donut chart | Department, Total Attrition |
| Bottom row | Clustered bar chart | Job Role, Attrition Rate |
| Bottom row | Matrix | Job Role, Job Satisfaction, Total Employees |
| Bottom row | Funnel chart | Education Field, Total Attrition |

## Field dictionary

| Field | Type | Meaning |
|---|---|---|
| Total Employees | Measure | Headcount for the current filters |
| Total Attrition | Measure | Number of employees who left |
| Attrition Rate | Measure | Attrition as a share of headcount |
| Active Employee | Measure | Employees who have not left |
| Age | Column | Employee age in years |
| Age Group | Column | Age band used on the column chart |
| Monthly Income | Column | Monthly pay per employee |
| Gender | Column | Employee gender |
| Marital Status | Column | Single, married or divorced |
| Business Travel | Column | How often the role involves travel |
| Education | Column | Education level |
| Education Field | Column | Field of study |
| Department | Column | Department |
| Job Role | Column | Role title |
| Job Satisfaction | Column | Satisfaction score |

> The measure formulas (DAX) are not documented here. Copy them from Power BI Desktop (Model view, select the measure).

## How to use

1. Read the four KPI cards first: Total Employees, Total Attrition, Attrition Rate and Active Employee.
2. Pick a value in the Gender slicer and watch every card and chart update.
3. Add Marital Status or Business Travel to narrow the group.
4. Click a slice in the department donut to focus the page on one department.
5. Use the job role bar chart to find the roles with the highest attrition rate.
6. Check the same role in the satisfaction matrix to see where its people sit.
7. Click a selection again, or use Ctrl + click, to clear or combine selections.
8. Right-click any visual and choose **Show as a table** to see the numbers behind it.

Slicers and chart clicks cross-filter every other visual by default. Change this under **Format → Edit interactions**.

## Setup

1. Open `dashboard_1.pbix` in Power BI Desktop (Windows).
2. Choose **Home → Refresh** to reload the `HR data` table.
3. If the source has moved, use **Transform data → Data source settings → Change source**.

The report uses the CY24SU10 base theme. The title colour is navy `#12239E`. Six images are embedded in the file, so there is nothing extra to copy.

## Known issues

- The **Age** and **Monthly Income** cards use **Sum**. A summed age has no useful meaning. Change both to **Average**, or add measures such as `Avg Age` and `Avg Income`.

## Screenshot

Export the page from Power BI (**File → Export → PNG**), save it as `screenshots/dashboard.png`, and add it here:

```markdown
![Dashboard](screenshots/dashboard.png)
```
