# 📊 Excel Salary Dashboard

![Salary Dashboard Screenshot](1_Salary_Dashboard.png)

## 🔎 Introduction

This **Excel Salary Dashboard** was created to help job‑seekers explore salary trends across data‑related roles and verify they’re being fairly compensated.  
The underlying dataset comes from my Excel course and covers **2023** job data — titles, salaries, locations, and required skills.

📁 **Dashboard file** → [`1_Salary_Dashboard.xlsx`](1_Salary_Dashboard.xlsx)

---

## 🧠 Excel Skills Used

- 📉 Charts (Bar & Map)
- 🧮 Advanced formulas / array functions
- ❎ Data Validation
- 🔍 Multi‑criteria filtering

---

## 📂 Dataset Overview

Real‑world data‑science job information, including:

- 👨‍💼 **Job Titles**  
- 💰 **Annual Salaries**  
- 📍 **Countries / Locations**  
- 🛠️ **Required Skills & Schedule Types**  

---

## 📈 Dashboard Components

### 📊 1. Data‑Science Job Salaries — Bar Chart

![Chart 1](1_Salary_Dashboard_Chart1.png)

* Horizontal bar chart showing **median salaries** by job title  
* Sorted descending for quick comparison  
* **Insight 💡:** Senior & engineering roles out‑earn analyst roles  

---

### 🗺️ 2. Country Median Salaries — Map Chart

![Chart 2](1_Salary_Dashboard_Chart2.png)

* Excel **map chart** visualizing global salary levels  
* Color‑coded regions for at‑a‑glance disparities  
* **Insight 💡:** Clear view of high vs. low salary regions worldwide  

---

## 🔢 Key Formulas

### 💰 Median Salary by Job Title, Country & Type

    =MEDIAN(
      IF(
        (jobs[job_title_short]=A2) *
        (jobs[job_country]=country) *
        (ISNUMBER(SEARCH(type,jobs[job_schedule_type]))) *
        (jobs[salary_year_avg]<>0),
        jobs[salary_year_avg]
      )
    )

🔍 Filters by job title, country, and type  
📊 Uses an **array formula** for dynamic median calculation  

---

### ⏰ Unique Schedule‑Type Filtering

    =FILTER(
        J2#,
        (NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))
        * (J2#<>0)
      )

🧼 Cleans and filters job schedule types  
🎯 Used in data‑validation dropdowns  

---

## ✅ Data Validation

- 🔒 Applies filtered lists to dropdowns (job title, country, schedule type)  
- 🚫 Prevents invalid or inconsistent entries  
- 👥 Enhances dashboard usability  

---

## 🧾 Conclusion

This project shows how Excel can be leveraged to **explore and visualise job‑market trends** in the data industry.  
By analysing salaries across roles, countries, and job types, the dashboard helps users make more informed career decisions.

Feel free to dive in and adapt the workbook for your own analyses!

---

## 📎 Files Included

- `1_Salary_Dashboard.xlsx`  —  Final interactive dashboard  
- `1_Salary_Dashboard.png`   —  Main dashboard screenshot  
- `1_Salary_Dashboard_Chart1.png` —  Bar chart  
- `1_Salary_Dashboard_Chart2.png` —  Map chart  
- `1_Salary_Dashboard_Type.png`  —  Filtered schedule types  

---

## ⭐ Like this Project?

If you find it useful, please ⭐️ the repository and connect with me!
