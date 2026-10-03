# Excel Salary Dashboard
![Salary Dashboard](assets/Salary_Dashboard.png)`

## Introduction

This data jobs salary dashboard helps job seekers explore salaries for the roles they want, so they can check they are being paid fairly. You pick a job title, country, and schedule type, and the dashboard shows the median salary, how roles compare, where in the world pay is highest, and the **top skill** employers ask for in that role.

I built it as part of my transition into data analytics, to practice turning a raw dataset into something interactive and useful.

> ✏️ **[EDIT]** Add 1-2 sentences in your own words about why you built this and what you wanted to learn.

## Dataset

The data comes from Luke Barousse's Excel course and contains real-world data job postings from 2023, including:

- 👨‍💼 Job titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills

## Dashboard File

My final dashboard is in `Salary_Dashboard.xlsx`.

> ✏️ **[EDIT]** Make sure this matches your actual file name.

## Excel Skills Used

- 📉 Charts
- 🧮 Formulas and Functions
- ❎ Data Validation
- 🃏 Dashboard cards (KPI-style callouts)

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart

> 📸 **[INSERT IMAGE: bar chart]** Right-click the chart in Excel, choose *Save as Picture*, and add: `![Bar chart](assets/Chart1.png)`

- 🛠️ **Excel Features:** Bar chart with formatted salary values and a layout cleaned up for clarity.
- 🎨 **Design Choice:** Horizontal bars make it easy to compare median salaries across job titles.
- 📉 **Data Organization:** Job titles sorted by descending salary.
- 💡 **Insights Gained:** ✏️ [e.g., Senior roles and engineers tend to earn more than analyst roles. Replace with what *your* chart shows.]

#### 🗺️ Country Median Salaries - Map Chart

> 📸 **[INSERT IMAGE: map chart]** `![Map chart](assets/Chart2.png)`

- 🛠️ **Excel Features:** Excel's map chart to plot median salary by country.
- 🎨 **Design Choice:** Color scale to separate higher- and lower-paying regions.
- 📊 **Data Representation:** Median salary for every country with available data.
- 💡 **Insights Gained:** ✏️ [What stands out about global salary differences?]

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Title

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, and schedule type, and skips blank salaries.
- 📊 **Array Formula:** `MEDIAN()` wrapped around a nested `IF()` to work on an array.
- 🎯 **Tailored Insights:** Gives salary figures for the exact title, country, and type selected.
- 🔢 **Formula Purpose:** Fills the background table that feeds the charts.

#### 🍽️ Background Table

> 📸 **[INSERT IMAGE: screenshot of the background table]** `![Background table](assets/Background_Table.png)`

#### 🃏 Top Skill Card

> ✏️ **[EDIT]** This is the part that makes your dashboard different, so explain it well. Paste your real formula below.

```excel
-- PASTE YOUR TOP SKILL FORMULA HERE
```

- 🔍 **What it does:** ✏️ [In one line: e.g., finds the skill that appears most often for the selected job title, country, and type.]
- 🧰 **Functions used:** ✏️ [List the functions you used]
- 🔄 **Interactivity:** The card updates whenever the dropdown selections change.
- 💡 **Why a skill card:** ✏️ [Why you chose it: it tells job seekers what to learn, not just what they might earn.]

> 📸 **[INSERT IMAGE: close-up of the Top Skill card]** `![Top skill card](assets/Top_Skill_Card.png)`

#### ⏰ Job Schedule Type List

```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Unique List Generation:** `FILTER()` removes entries containing "and" or commas, and drops zero values.
- 🔢 **Formula Purpose:** Produces a clean list of schedule types for the dropdown.

> 📸 **[INSERT IMAGE: schedule type list]** `![Schedule types](assets/Type_List.png)`

### ❎ Data Validation

- 🔒 **Filtered list as a dropdown:** The cleaned schedule-type list is used as a Data Validation rule for the Job Title, Country, and Type inputs (Data tab → Data Validation).
- 🎯 Users can only choose valid, predefined options.
- 🚫 Typos and inconsistent entries are prevented.
- 👥 The dashboard is easier to use.

> 📸 **[INSERT IMAGE or GIF: dropdown in action]** Record a short screen capture of you changing the dropdowns and the charts and Top Skill card updating (ScreenToGif on Windows, or Win+G Game Bar), then add: `![Dropdown demo](assets/Dropdown_Demo.gif)`

## 🎥 Demo Video (optional)

> 🎥 **[INSERT VIDEO: 1-2 minute walkthrough]** Record yourself using the dashboard, upload it to YouTube as "Unlisted", and add a clickable thumbnail: `[![Watch the demo](assets/video_thumbnail.png)](https://youtube.com/your-video-link)`

## What I Learned

- ✏️ [Skills you practiced, e.g., array formulas, `FILTER`, map charts, data validation]
- ✏️ [What was hardest, and how you worked through it]

## Conclusion

✏️ [3-4 sentences: what the dashboard shows about salary trends, what the Top Skill card adds, and how a job seeker could use it.]

## Acknowledgments

Dataset and course by Luke Barousse. Dashboard design and the Top Skill card are my own additions.

> ✏️ **[EDIT]** Keep that last sentence only if it's true.

---

📫 Connect with me on [GitHub](https://github.com/Manoah1401)
