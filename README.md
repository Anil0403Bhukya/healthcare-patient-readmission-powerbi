# 🏥 Healthcare Patient Readmission Dashboard

### Power BI dashboard project analyzing healthcare patient readmissions using Excel-cleaned hospital data.

---

## 📌 Project Overview
This project focuses on identifying patterns in **hospital readmissions** and **patient appointment no-shows**. By analyzing a dataset of 4,000+ patient records, this dashboard provides healthcare administrators with actionable insights to improve patient outcomes and reduce the financial penalties associated with high 30-day readmission rates.

## 🛠️ Tech Stack
* **SQL:** Data extraction, cleaning, and calculating key metrics (KPIs).
* **MS Excel:** Risk stratification modeling and data validation.
* **Power BI:** Interactive dashboarding, DAX measures, and data storytelling.

---

## 📈 Technical Workflow

### 1. Data Engineering (SQL)
I processed a dataset of 4,000+ records to create a reliable foundation for analysis.
* **KPI Logic:** Wrote queries to identify "30-Day Readmissions" by comparing discharge and re-admission dates.
* **Categorization:** Used `CASE WHEN` statements to segment patients by department (Cardiology, Pediatrics, Mental Health, General Medicine).

### 2. Analytical Modeling (Excel)
Before visualization, I developed a **Patient Risk Score** (0-10) to move from descriptive to predictive analytics.
* **Weighting Logic:**
    * **Wait Time > 15 Days:** +5 Points
    * **In-Person Visit:** +3 Points
    * **Age Vulnerability (<18 or >75):** +2 Points
* **Result:** Created an "Action Plan" column to flag high-risk patients for proactive clinical follow-ups.

### 3. Data Visualization (Power BI)
Created an interactive dashboard to monitor hospital operations and clinical trends.
* **DAX Measures:** Developed measures for `Total Patients`, `Readmission Rate %`, and `No-Show Rate`.
* **Visuals:** * **Readmission Trend:** Line chart showing spikes in patient returns.
    * **Risk Matrix:** Treemap highlighting the volume of patients in the "High Risk" category.
    * **Departmental Slicers:** Allows users to filter all visuals by medical specialty.

---

## 🔍 Key Insights
* **Readmission Correlation:** Patients who missed their follow-up appointment within the first 7 days were **30% more likely** to be readmitted within 30 days.
* **The Wait Time Factor:** Appointments booked more than **14 days** in advance showed a significant spike in "No-Shows."
* **Departmental Trends:** The Cardiology department had the highest readmission rate, primarily among patients aged 65+.

---

## 📂 Repository Structure
* **SQL_Scripts:** `readmission_analysis.sql` (Calculates rates and cleans data).
* **Excel_Data:** `Risk_Score_Model.xlsx` (The cleaned data and risk formulas).
* **PowerBI_Reports:** `Healthcare_Readmission_Dashboard.pbix` (The interactive file).

---

## 🚀 How to Use
1. **View the Dashboard:** Open the `.pbix` file in Power BI Desktop.
2. **Review the Data:** Check the Excel file for the "Risk Score" logic.
3. **Run the Analysis:** Use the SQL scripts to see how the raw metrics were calculated.
