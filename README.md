# Excel_Project_2
# 📊 Excel Salary Dashboard

![Salary Dashboard Screenshot](1_Salary_Dashboard.png)

## 🔎 Introduction

This **Excel Salary Dashboard** was created to help job seekers explore salary trends across data-related job roles and ensure they're being fairly compensated. The dataset comes from my Excel course, which offers a foundation in analyzing data using powerful Excel features.

The dashboard showcases data from **2023**, including job titles, salaries, countries, and required skills — all presented in a visually appealing format.

📁 **Dashboard File**: [`1_Salary_Dashboard.xlsx`](1_Salary_Dashboard.xlsx)

---

## 🧠 Excel Skills Used

- 📉 Charts (Bar Chart & Map Chart)
- 🧮 Advanced Formulas and Array Functions
- ❎ Data Validation
- 🔍 Multi-Criteria Filtering

---

## 📂 Dataset Overview

The dataset used in this project contains **real-world job data** for data science roles and includes:

- 👨‍💼 Job Titles  
- 💰 Annual Salaries  
- 📍 Job Locations  
- 🛠️ Required Skills & Schedule Types  

---

## 📈 Dashboard Components

### 📊 1. Data Science Job Salaries – Bar Chart

![Chart 1](1_Salary_Dashboard_Chart1.png)

- 🛠️ **Feature**: Horizontal bar chart showing median salaries by job title  
- 🎨 **Design**: Sorted in descending order for clarity  
- 💡 **Insight**: Senior and engineering roles offer higher compensation than analyst positions  

---

### 🗺️ 2. Country Median Salaries – Map Chart

![Chart 2](1_Salary_Dashboard_Chart2.png)

- 🛠️ **Feature**: Excel’s map chart to visualize global salary trends  
- 🎨 **Design**: Color-coded regions based on median salary  
- 💡 **Insight**: Highlights geographic disparities in compensation  

---

## 🔢 Key Formulas

### 💰 Median Salary by Job Title, Country & Type

```excel
=MEDIAN(
  IF(
    (jobs[job_title_short]=A2) *
    (jobs[job_country]=country) *
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type]))) *
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
  )
)

