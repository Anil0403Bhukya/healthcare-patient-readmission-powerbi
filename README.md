# 🏥 Healthcare Patient Readmission Analysis

### Power BI dashboard project analyzing healthcare patient readmissions using Excel-cleaned hospital data.

---

## 📌 Executive Summary
This project analyzes **4,000+ patient records** to identify the primary drivers behind hospital readmissions and appointment "No-Shows." By utilizing **SQL** for data engineering, **Excel** for risk modeling, and **Power BI** for executive reporting, this project provides a data-driven strategy to reduce operational revenue loss and improve patient outcomes.

---

## 🛠️ Tech Stack
* **SQL:** Data cleaning, Recursive CTEs, and KPI calculations.
* **MS Excel:** Risk stratification modeling and data validation.
* **Power BI:** DAX measures, interactive visualizations, and dashboard design.

---

## 📈 Technical Workflow

### 1. Data Engineering (SQL)
I built a robust database of 4,000 records across departments like Cardiology and Pediatrics.
* **Key KPI:** Developed a script to calculate the **Readmission Rate %** per department.
* **Logic:** Used `CASE` statements to distinguish between 'Completed', 'No-Show', and 'Readmitted' statuses.

### 2. Predictive Risk Modeling (Excel)
I developed a **Weighted Risk Score** (0-10) to identify high-risk patients before they miss an appointment.
* **Wait Time > 15 days:** +5 Points
* **In-Person Visit:** +3 Points
* **Age Factor (<18 or >75):** +2 Points
* **Action:** Created an automated "Intervention Plan" column to trigger phone reminders for scores of 8+.

### 3. Interactive Dashboard (Power BI)
Created a high-fidelity dashboard for Hospital Administrators to monitor facility health.
* **DAX Measures:** Created measures for `Total Patients`, `Avg Wait Time`, and `Dynamic Readmission %`.
* **Visuals:** Included departmental heatmaps and visit-type comparison charts.

---

## 🔍 Key Insights
* **Wait Times:** Appointments with wait times over **14 days** saw a **22% increase** in no-shows.
* **Telehealth Impact:** Mental Health departments using Telehealth saw **15% fewer missed appointments**.
* **High-Risk Segment:** Patients with a risk score of **8+** accounted for nearly **60% of all readmissions**.

---

## 📂 Repository Structure
* `/SQL_Scripts`: `setup_data.sql` and `analysis_queries.sql`.
* `/Excel_Models`: `Patient_Risk_Calculator.xlsx`.
* `/PowerBI_Reports`: `Hospital_Operations_Dashboard.pbix`.

---

## 🚀 How to Use
1. Run the `setup_data.sql` script to generate the database.
2. Load the cleaned data into Power BI.
3. Use the slicers to filter by **Department** or **Age Group** to see specific trends.
