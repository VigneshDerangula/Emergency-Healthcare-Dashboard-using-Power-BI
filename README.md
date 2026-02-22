# 🏥 Hospital Emergency Room Dashboard

<div align="center">

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![PowerPoint](https://img.shields.io/badge/PowerPoint-B7472A?style=for-the-badge&logo=microsoftpowerpoint&logoColor=white)
![CSV](https://img.shields.io/badge/Data-CSV-orange?style=for-the-badge&logo=databricks&logoColor=white)

**Interactive Power BI dashboard analysing 9,216 ER patient records across wait times, admissions, satisfaction scores, and demographics**

[📊 KPI Summary](#-kpi-summary) · [🔍 Key Findings](#-key-findings) · [📁 File Structure](#-file-structure) · [🛠️ Data Dictionary](#️-data-dictionary)

</div>

---

## 📌 Project Summary

A hospital emergency room generates thousands of patient records every year — but without a structured analytics layer, operational bottlenecks stay invisible. This project transforms raw ER data into a **fully interactive Power BI dashboard** that helps hospital administrators and clinical managers answer:

> *"Are patients waiting too long? Who is being admitted and why? Which departments are overloaded? Where are the satisfaction gaps?"*

Built using **9,216 real-structure ER patient records** spanning two years, the dashboard delivers actionable operational and demographic insights through a clean, filterable single-page view.

---

## 📊 KPI Summary

| Metric | Value |
|--------|-------|
| 🏥 **Total Patients** | 9,216 |
| ⏱️ **Average Wait Time** | 35.3 minutes |
| ⏱️ **Wait Time Range** | 10 – 60 minutes |
| ✅ **Hospital Admission Rate** | 50.0% (4,612 admitted) |
| ⭐ **Average Satisfaction Score** | 4.99 / 10 |
| 📋 **Satisfaction Response Rate** | 27.3% (2,517 patients rated) |
| 👨 **Male Patients** | 51.1% (4,705) |
| 👩 **Female Patients** | 48.7% (4,487) |
| 🏥 **Avg Age** | 39.9 years (range: 1–79) |
| 🔬 **Top Referral Dept** | General Practice (20.0%) |
| 🏳️ **Largest Race Group** | White (27.9%) |

---

## 🔍 Key Findings

### 1. ⏱️ Wait Times Are Consistently High Across All Departments
The average ER wait time is **35.3 minutes** with a range of 10–60 minutes. Neurology has the highest average wait at **36.8 minutes**, followed by Physiotherapy at **36.6 minutes** — suggesting these specialist pathways are creating bottlenecks even within the ER triage flow.

### 2. 🏥 Half of All ER Patients Are Admitted
A **50% hospital admission rate** is significantly high for an emergency room setting. This signals either a high-acuity patient population or potential over-admission patterns that warrant clinical review. Filtering by department and demographics in the dashboard reveals which cohorts drive this rate.

### 3. 🔬 Department Referral Breakdown
| Department | Patients | Share |
|------------|----------|-------|
| No Referral (ER-only) | 5,400 | 58.6% |
| General Practice | 1,840 | 20.0% |
| Orthopedics | 995 | 10.8% |
| Physiotherapy | 276 | 3.0% |
| Cardiology | 248 | 2.7% |
| Neurology | 193 | 2.1% |
| Gastroenterology | 178 | 1.9% |
| Renal | 86 | 0.9% |

Over **58% of patients** are treated and discharged within the ER with no specialist referral — yet these patients still average 35-minute wait times, indicating a systemic triage or capacity issue rather than a referral complexity issue.

### 4. 👥 Demographic Diversity
| Race | Patients | Share |
|------|----------|-------|
| White | 2,571 | 27.9% |
| African American | 1,951 | 21.2% |
| Two or More Races | 1,557 | 16.9% |
| Asian | 1,060 | 11.5% |
| Declined to Identify | 1,030 | 11.2% |
| Pacific Islander | 549 | 6.0% |
| Native American/Alaska Native | 498 | 5.4% |

The highly diverse patient population makes the dashboard particularly valuable for **healthcare equity analysis** — filtering satisfaction scores and wait times by race can surface systemic disparities in ER care delivery.

### 5. ⭐ Low Satisfaction Response Rate Limits Insight
Only **27.3% of patients** provided a satisfaction score. With an average of **4.99/10**, the data suggests moderate-to-poor satisfaction, but the low response rate means this metric should be treated cautiously. Improving collection methodology is a recommended operational action.

### 6. 👶 Age Group Distribution
| Age Group | Patients |
|-----------|----------|
| 0–18 | 2,110 (22.9%) |
| 19–35 | 1,985 (21.5%) |
| 36–50 | 1,776 (19.3%) |
| 51–65 | 1,728 (18.8%) |
| 65+ | 1,617 (17.5%) |

Paediatric patients (0–18) are the single largest age group — a finding that may inform staffing decisions, especially for paediatric-specialised ER resources.

---

## 📁 File Structure

```
hospital-er-dashboard/
│
├── 📊 hospital_emewrgency_room_dashboard.pbix   # Power BI dashboard file
│   ├── Page 1 — Executive Summary
│   │   ├── Total Patients KPI card
│   │   ├── Avg Wait Time card
│   │   ├── Admission Rate card
│   │   ├── Avg Satisfaction Score card
│   │   ├── Patients by Month (line/bar trend)
│   │   ├── Patients by Age Group (bar)
│   │   ├── Patients by Race (bar)
│   │   └── Department Referral breakdown (donut/bar)
│   └── Filters — Date · Gender · Race · Department · Age Group
│
├── 📋 hospital_er_data.csv                      # Raw ER patient dataset
│   ├── 9,216 rows · 12 columns
│   ├── Date range: 2023–2024
│   └── Fields: Patient ID, Admission Date, Gender, Age, Race,
│             Department, Admission Flag, Satisfaction, Wait Time
│
├── 📖 data_terminology.docx                     # Data dictionary
│   └── Definition of all 12 fields with business context
│
├── 📽️ Hospital-Emergency-Room-Dashboard.pptx    # Presentation deck
│   └── Executive-ready slides summarising dashboard insights
│
└── 🖼️ hospital_image.png                        # Project visual / logo
```

---

## 🛠️ Data Dictionary

| Column | Type | Description |
|--------|------|-------------|
| `Patient Id` | Text | Unique alphanumeric identifier per patient |
| `Patient Admission Date` | DateTime | Date and time of ER admission |
| `Patient First Initial` | Text | Anonymised first name initial |
| `Patient Last Name` | Text | Patient surname |
| `Patient Gender` | Text | M / F / NC (Non-Conforming) |
| `Patient Age` | Integer | Age at time of admission (1–79) |
| `Patient Race` | Text | Self-reported racial/ethnic identity |
| `Department Referral` | Text | Specialist department referred to (or None) |
| `Patient Admission Flag` | Boolean | TRUE = admitted to hospital · FALSE = discharged from ER |
| `Patient Satisfaction Score` | Integer | Patient-rated score (0–10 scale) · 72.7% left blank |
| `Patient Waittime` | Integer | Minutes from ER arrival to first clinical contact |
| `Patients CM` | Binary | Whether a Case Manager was assigned (0 or 1) |

---

## 🏗️ Dashboard Design

The Power BI dashboard is built as a **single-page executive view** with:

- **KPI Cards** — Total patients, avg wait time, admission rate, satisfaction score
- **Time Trend** — Monthly patient volume to spot seasonal peaks
- **Demographic Breakdown** — Age group, gender, and race distribution
- **Department Analysis** — Referral volume and wait time by department
- **Satisfaction Analysis** — Score distribution and response rate
- **Interactive Slicers** — Filter entire dashboard by date, gender, race, department, and age group

### Colour Theme
The dashboard uses a **clinical blue palette** — consistent with healthcare contexts, easy to read in presentation mode, and accessible for colour-impaired viewers.

---

## 🚀 How to Use

### Open the Power BI Dashboard

```
1. Download hospital_emewrgency_room_dashboard.pbix
2. Open in Power BI Desktop (free download: powerbi.microsoft.com)
3. Use slicers to filter by department, race, age group, gender, or date
4. Hover over charts for detailed tooltips
```

### Explore the Raw Data

```python
import pandas as pd

df = pd.read_csv('hospital_er_data.csv')
print(df.shape)          # (9216, 12)
print(df.describe())
```

### View the Presentation

```
Open Hospital-Emergency-Room-Dashboard.pptx in PowerPoint or Google Slides
Suitable for sharing with clinical directors, hospital administrators, or interview panels
```

---

## 💡 Business Use Cases

| Stakeholder | Question Answered |
|-------------|------------------|
| **ER Director** | Which hours / days have the highest patient volume? |
| **Clinical Manager** | Which departments are driving the most referrals? |
| **Quality Lead** | Where are satisfaction scores lowest — and why? |
| **Equity Officer** | Do wait times or admission rates differ by race or gender? |
| **Ops Manager** | What percentage of patients are admitted vs discharged? |
| **HR / Staffing** | Which age groups dominate — do we have the right mix of specialists? |

---


## 🤝 Connect

⭐ Star this repo if you found it useful, or reach out via [LinkedIn]([https://linkedin.com/in/yourprofile](https://www.linkedin.com/in/vigneshderangula/) for questions or collaboration.

---

<div align="center">

*Built with Power BI · Excel · CSV · PowerPoint*

</div>
