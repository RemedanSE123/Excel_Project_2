# 📊  Data‑Jobs Market Analysis



## 🔎 Introduction
As a former job‑seeker, I wanted to explore which **skills** earn the highest **pay** in the data‑science market.  
This project answers four core questions using Excel’s advanced analytics stack.

---

## ❓ Questions to Analyze
1. **Do more skills get you better pay?**  
2. **What’s the salary for data jobs in different regions?**  
3. **What are the top skills of data professionals?**  
4. **What’s the pay for the top 10 skills?**  

---

## 🧠 Excel Skills Used
- 📊 Pivot Tables
- 📈 Pivot Charts
- 🧮 DAX (Data Analysis Expressions)
- 🔍 Power Query
- 💪 Power Pivot

---

## 📂 Dataset Overview
Real‑world **2023** data‑science job postings:

- 👨‍💼 Job titles  
- 💰 Salaries  
- 📍 Locations  
- 🛠️ Skills  

Dataset available via my Excel course.

---

# 1️⃣ Do more skills get you better pay?

### 🔍 Power Query Workflow

| Phase | Description |
|-------|-------------|
| **Extract** | Imported `data_salary_all.xlsx` into two queries:<br>• **`data_jobs_all`** — full job dataset<br>• **`data_job_skills`** — skills per job‑ID |
| **Transform** | Cast data types, removed unused columns, cleaned text, trimmed whitespace |

<img width="244" height="312" alt="image" src="https://github.com/user-attachments/assets/20a138a2-7289-4d76-acd2-5ac2c251284d" />

<img width="243" height="328" alt="image" src="https://github.com/user-attachments/assets/6c5a499f-3a2d-4cea-b68e-a3635cc488f5" />



| **Load** | Loaded both queries into the workbook for analysis |
<img width="1916" height="649" alt="image" src="https://github.com/user-attachments/assets/700d76db-e48d-4e24-be36-074d6ff7ca27" />
<img width="1914" height="702" alt="image" src="https://github.com/user-attachments/assets/e1342332-cb98-4136-b370-dd682d7f850c" />



### 📊 Analysis
<img width="874" height="537" alt="image" src="https://github.com/user-attachments/assets/ed8dd0d9-a800-46ad-a738-a8396200bec2" />


**Insight 💡**  
- More skills correlate with higher median salary (e.g., Senior Data Engineer, Data Scientist).  
- Fewer skills (e.g., Business Analyst) → lower pay.

---

# 2️⃣ Salary by Region
<img width="1776" height="738" alt="image" src="https://github.com/user-attachments/assets/ab810ed6-9153-4e51-a632-c4a78c5c5cea" />

### 🧮 PivotTable + DAX

```excel
-- Measure for US‐only median
US Median Salary :=
CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States"
)

-- General median
Median Salary := MEDIAN(data_jobs_all[salary_year_avg])

```
## 💡 Insight — Salary by Region
- **Senior Data Engineer & Data Scientist** command the top salaries in both US and global markets.  
- **US roles** pay a noticeable premium, especially for high‑tech positions.

---

## 3️⃣ Top Skills of Data Professionals

### 🔧 Power Pivot Data Model
Relationship: `data_jobs_all[job_id]` ↔ `data_job_skills[job_id]`
<img width="1918" height="742" alt="image" src="https://github.com/user-attachments/assets/dfd640d8-0e2e-4c7b-9e98-c21dd0974e93" />
<img width="759" height="513" alt="image" src="https://github.com/user-attachments/assets/f4c81a4d-379f-4928-ab98-8cd53684ef2f" />

**Insight 💡**  
- **SQL & Python** remain the most in‑demand skills.  
- **Cloud platforms** (AWS, Azure) are rising rapidly in popularity.

---

## 4️⃣ Pay of the Top 10 Skills
<img width="759" height="513" alt="image" src="https://github.com/user-attachments/assets/c3e6dfa8-a243-4d44-99cb-ffb4d899b836" />

<img width="862" height="452" alt="image" src="https://github.com/user-attachments/assets/0b759319-5952-4162-8a1c-667499cfceaf" />


### 📈 Combo PivotChart
- **Primary axis**: Median Salary (Clustered Column)  
- **Secondary axis**: Skill Likelihood % (Line + Diamond markers)

**Insight 💡**  
- Highest salaries tied to **Python, Oracle, SQL**.  
- General tools (**PowerPoint, Word**) show the lowest pay and presence.

---

## 🧾 Conclusion
Using **Power Query, PivotTables, Power Pivot, DAX, and charts**, this study demonstrates that possessing multiple, in‑demand skills (Python, SQL, cloud tech) is strongly correlated with higher salaries.  
Leverage these insights for career planning, salary negotiations, and strategic hiring.

---

