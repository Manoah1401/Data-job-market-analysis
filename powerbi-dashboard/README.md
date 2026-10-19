# Data Job Dashboard (Power BI)

An interactive Power BI dashboard that explores the data job market: how much each role pays and which skills are required for the corresponding role.

![Data Job Dashboard demo](assets/Final-Project-Demo.gif)


Check out the Power BI file here: [Data Job Dashboard demo](Final-Project.pbix)


## What the dashboard shows

**Headline KPIs (all filters set to "All")**

| Metric | Value |
|---|---|
| Job Count | 479K |
| Skills per Job | 4.8 |
| Median Yearly Salary | $113K |
| Median Hourly Salary | $47.62 |

**Visuals**

- **How much does each role pay?** Ranks roles by median salary, from Senior Data Scientist and Machine Learning Engineer at the top down to Business Analyst and Data Analyst.
- **What are the skills needed?** Ranks skills by demand. Python and SQL lead, followed by AWS, Azure, Tableau, Spark and R.

**Interactivity**

- **Slicers** filter everything by *Job Title* and *Country*.
- **Button toggles** switch the pay chart between *Median Yearly Salary* and *Median Hourly Salary*, and the skills chart between *Job Count* and *Skill Percent*.
- **Light/dark mode switch** built with bookmarks.

## Power BI features used

- **Power Query**: cleaning and transforming the raw data, including append vs. merge and M language basics
- **Data modelling**: relationships between tables in the Model view
- **DAX**: explicit measures such as medians and percentages
- **Parameters**: driving dynamic visuals
- **Visuals**: bar and column charts, tables and cards
- **Slicers, buttons and bookmarks**: filtering, metric toggles and theme switching
- **Power BI Service**: publishing and sharing the dashboard



## What I learned

- Cleaning and shaping data in Power Query before it reaches the report
- Writing DAX measures instead of relying on default aggregations
- Designing a dashboard that is easy to scan and interactive for the viewer
- Publishing and sharing a report through Power BI Service

## Credits

Course and dataset by [Luke Barousse](https://www.youtube.com/@LukeBarousse).
