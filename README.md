# HR Recruitment Analytics Dashboard 📊

An end-to-end Power BI project that transforms raw recruitment data into an interactive analytics dashboard, helping HR teams track candidates, hires, interviews, and sourcing performance at a glance.

---

## 📌 Project Overview

This project analyzes recruitment activity across departments, sources, and time periods to help HR stakeholders understand hiring performance, candidate flow, and pipeline efficiency. The final deliverable is a single-page interactive **Power BI dashboard** built from a structured Excel data model, supported by data cleaning, exploratory analysis, and KPI tracking.

**Key business questions answered:**

- How many candidates, interviews, hires, and open positions do we have?
- Which departments are hiring the most?
- Which sourcing channels (LinkedIn, Referral, Indeed, Naukri) perform best?
- How is the candidate pipeline distributed by status (Interview, Hired, Rejected, Offer)?
- How do applications and hires trend year-over-year?

---

## 🔄 End-to-End Workflow

1. **Data Collection** – Raw recruitment data gathered into Excel (Candidates, Recruitment Metrics, Interview Schedule).
2. **Data Cleaning & Preparation** – Removed duplicates, fixed nulls/blank fields, standardized text fields (Department, Source, Status), formatted dates.
3. **Data Structuring** – Organized cleaned data into well-defined Excel tables/sheets ready for Power BI import.
4. **Data Modeling** – Loaded tables into Power BI, created relationships between Candidates, Interview Schedule, and Recruitment Metrics.
5. **Exploratory Data Analysis (EDA)** – Reviewed distributions, trends, and outliers to decide which visuals best tell the recruitment story.
6. **Dashboard Design** – Built KPI cards, bar charts, pie/donut charts, line charts, and waterfall charts with filters/slicers.
7. **Validation** – Cross-checked dashboard totals against the raw dataset for accuracy.
8. **Publishing** – Final `.pbix` file packaged with supporting data and documentation.

---

## 🗂️ Data Source

The dataset is a synthetic/sample HR recruitment dataset containing **three tables**:

https://1drv.ms/x/c/00b1e276a52f7d08/IQAAGHCfgdS0RYgx-rh81K2PAduv3h1khv9GXasdOL3Lcm0?e=1ronHA

| Sheet | Rows | Columns |
|---|---|---|
| **Candidates** | 1,000 | Candidate ID, Department, Source, Status, Experience |
| **Recruitment Metrics** | 24 | Month, Open Positions, Applications, Hires |
| **Interview Schedule** | 1,000 | Interview ID, Candidate ID, Interviewer, Interview Date |

---

## 🧹 Data Cleaning & Data Preparation

- Checked for and removed duplicate Candidate IDs / Interview IDs.
- Standardized categorical fields: `Department`, `Source`, `Status`, `Experience` (consistent casing/spelling).
- Validated date fields (Year, Quarter, Month, Day) for consistency in the Interview Schedule.
- Verified numeric fields (Open Positions, Applications, Hires) for non-negative, logical values.
- Ensured `Candidate ID` is consistent as the join key between Candidates and Interview Schedule tables.
- Converted raw flat data into a clean tabular format suitable for Power BI's data model.

---

## 🔍 Exploratory Data Analysis (EDA)

Before dashboard design, EDA was performed to understand:
- Candidate volume by **Department** and **Source**
- Candidate **Status** distribution (Interview → Hired → Rejected → Offer)
- **Hiring Rate** (Hires ÷ Total Candidates)
- Year-over-year trends in **Applications** and **Hires** (2025 vs 2026)
- Interview load per **Interviewer/Manager**

---

## 📊 Power BI Dashboard

A single-page dashboard built with:
- **Slicer Panel:** Filter by Department, Source, Status, Experience
- **KPI Cards:** Total Candidates, Total Hires, Total Interviews, Open Positions, Hiring Rate, Total Applications
- **Total Hires by Department** – Horizontal bar chart
- **Total Candidates by Status** – Line chart (Interview → Hired → Rejected → Offer)
- **Total Applications by Year** – Waterfall chart (2025 → 2026 → Total)
- **Total Candidates by Source** – Donut chart (LinkedIn, Referral, Indeed, Naukri)
- **Sum of Hires by Year** – Column chart (2025 vs 2026)

---

## 💡 Key Insights

- **Operations (60)** and **HR (53)** departments recorded the highest number of hires; **Finance (36)** the lowest.
- Sourcing is fairly balanced across channels, with **LinkedIn (26%)** and **Referral (26%)** slightly ahead of Indeed (24%) and Naukri (24%).
- Overall **hiring rate stands at 25%**, meaning 1 in 4 candidates convert to a hire.
- **Total applications nearly doubled** from 3.5K (2025) to 3.3K+ growth into 2026, reaching 6.8K cumulative.
- **Hires grew from 380 (2025) to 489 (2026)**, indicating an improving recruitment funnel.
- Candidate status funnel shows a natural drop-off from Interview (286) to Offer (228) stage.

---

## 🛠️ Tools & Technologies

- **Microsoft Excel** – Raw data structuring & cleaning
- **Power BI Desktop** – Data modeling, DAX measures, dashboard design
- **Power Query** – ETL (Extract, Transform, Load)
- **DAX (Data Analysis Expressions)** – KPI calculations (Hiring Rate, Totals)

---

## 📁 Repository Structure

```
HR-Recruitment-Analytics-Dashboard/
│
├── 📂 Raw_Data/
│   └── HR_Recruitment_Raw.xlsx
│
├── 📂 Cleaned_Structured_Data/
│   └── HR_Recruitment_Analytics_1000_Rows.xlsx
│       ├── Candidates
│       ├── Recruitment Metrics
│       └── Interview Schedule
│
├── 📂 PowerBI/
│   └── HR_Recruitment_Analytics_Dashboard.pbix
│
├── 📂 Dashboard_Preview/
│   ├── Dashboard_Overview.png
│   └── Candidate_Interview_Records.png
│
├── README.md
├── LICENSE
└── DISCLAIMER.md
```

---

## 📑 Excel Structuring

The Excel workbook is structured into three normalized tables to support relational modeling in Power BI:
1. **Candidates** – Master candidate-level data (Department, Source, Status, Experience)
2. **Recruitment Metrics** – Monthly aggregated metrics (Open Positions, Applications, Hires)
3. **Interview Schedule** – Interview-level transactional data, linked to Candidates via Candidate ID

---

## 📥 Raw Converted Data

Original raw data was converted from its source format into Excel to allow easy cleaning, validation, and direct import into Power BI's data model.

<img width="1908" height="752" alt="Raw Data " src="https://github.com/user-attachments/assets/226d886e-9146-4202-8141-d99045006080" />


---

## ✅ Structured & Cleaned Data

Final cleaned dataset used in Power BI:
- **1,000 candidate records**
- **1,000 interview records**
- **24 months of recruitment metrics**
- All fields validated, deduplicated, and formatted consistently for accurate reporting.

---

## 🖥️ Power BI

- Data model with relationships between Candidates, Interview Schedule, and Recruitment Metrics
- DAX measures for Hiring Rate, Total Hires, Total Applications, etc.
- Slicers for Department, Source, Status, and Experience
- Fully interactive cross-filtering visuals

---

## 📺 Dashboard Preview

**HR Recruitment Analytics Dashboard**
Includes KPI cards, hires by department, candidate status funnel, applications by year, candidates by source, and hires by year.

<img width="1313" height="750" alt="Dashbord HR  1 " src="https://github.com/user-attachments/assets/04ba46c4-2013-4b94-ac1a-bcbfca4ee3ec" />

**Candidate Interview Records**
A detailed table view of interview-level data (Interview ID, Candidate ID, Interviewer, Year, Quarter, Month, Day).

<img width="1338" height="737" alt="Dashboard HR 2 " src="https://github.com/user-attachments/assets/38e6dcaf-378e-493a-b88b-a747aafb4e86" />


---

## 🌟 Project Highlights

- Clean, single-page, recruiter-friendly dashboard design
- Fully interactive filters (Department, Source, Status, Experience)
- Combination of KPI cards, trend lines, bar charts, donut chart, and waterfall chart
- Clear storytelling: from candidate sourcing → interview → hiring outcome

---

## 🚀 Future Enhancements

- Add **time-intelligence DAX measures** (MoM/YoY growth %)
- Build a **drill-through page** for individual interviewer performance
- Add **diversity & experience-level analytics**
- Integrate **predictive hiring rate forecasting**
- Automate data refresh via **Power BI Service / Power Automate**

---

## ⚠️ Disclaimer

This project uses a **synthetic/sample dataset** created for learning and portfolio purposes only. It does not represent real candidates, companies, or HR records. Any resemblance to actual persons or organizations is purely coincidental.

---

## 📄 License

This project is licensed under the **MIT License** — feel free to use, modify, and share with attribution.

---

## 👤 Author

**[J Sai Abhinay]**

HR / Data Analytics Enthusiast

📧 [jsaibhinay53@gmail.com] 

🔗 [https://www.linkedin.com/in/j-sai-abhinay-594822362/] 

---
