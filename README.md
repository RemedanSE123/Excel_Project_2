# 📊 Excel Salary Dashboard



https://github.com/user-attachments/assets/35f7d682-103b-4659-ab9f-a3fe728fa07e



## 🔎 Introduction

This **Excel Salary Dashboard** was created to help job‑seekers explore salary trends across data‑related roles and verify they’re being fairly compensated.  
The underlying dataset  covers **2023** job data — titles, salaries, locations, and required skills.

📁 **Dashboard file** → <img width="1202" height="559" alt="Screenshot 2025-07-14 170944" src="https://github.com/user-attachments/assets/8faaf10e-6a06-486f-a199-2293999624da" />


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

![Chart 1]<img width="435" height="527" alt="Screenshot 2025-07-14 172556" src="https://github.com/user-attachments/assets/415a015b-2698-4b30-8087-d024700dfb0c" />


* Horizontal bar chart showing **median salaries** by job title  
* Sorted descending for quick comparison  
* **Insight 💡:** Senior & engineering roles out‑earn analyst roles  

---

### 🗺️ 2. Country Median Salaries — Map Chart

![Chart 2]<img width="393" height="493" alt="Screenshot 2025-07-14 172616" src="https://github.com/user-attachments/assets/c82e6f2a-108c-4d20-a91e-44653b9091fc" />


* Excel **map chart** visualizing global salary levels  
* Color‑coded regions for at‑a‑glance disparities  
* **Insight 💡:** Clear view of high vs. low salary regions worldwide  

---

<img width="408" height="507" alt="Screenshot 2025-07-14 172628" src="https://github.com/user-attachments/assets/c17ee929-7196-4250-9359-d99cb2e5982d" />


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


---

## ⭐ Like this Project?

If you find it useful, please ⭐️ the repository and connect with me!
