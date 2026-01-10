🏥 Healthcare Patient Appointment & No-Show Analysis
📌 Executive Summary
This project analyzes 4,000+ patient records to identify the primary drivers behind appointment "No-Shows." In the healthcare industry, missed appointments lead to decreased clinic efficiency and significant revenue loss. By utilizing SQL for data engineering, Excel for risk modeling, and Power BI for executive reporting, this project provides a data-driven strategy to reduce no-show rates by targeting high-risk patient segments.

🛠️ Technical Workflow
1. Data Engineering (SQL)
I used a Recursive CTE to generate a robust dataset of 4,000 appointments across four key departments (Cardiology, Pediatrics, Mental Health, and General Medicine).

Skills: Common Table Expressions (CTEs), CASE statements for data cleaning, and DATE functions.

Key KPI: Developed a script to calculate the No-Show Rate % per department, identifying which clinics require the most administrative support.

2. Predictive Risk Modeling (Excel)
Using the processed data, I built a Weighted Risk Score to move from descriptive to predictive analytics.

Logic: Assigned weights to variables: Wait Time > 15 days (+5), In-Person visits (+3), and Vulnerable Age Groups (+2).

Actionable Insight: Automated a "Recommendation Column" using nested IFS to flag patients for SMS or phone call interventions based on their score.

3. Interactive Dashboard (Power BI)
The final phase involved building a high-fidelity dashboard for Hospital Administrators to monitor operational health.

DAX Measures: Created custom measures for Total Patients, Avg Wait Time, and Dynamic No-Show %.

Visualizations: * Departmental Performance: A bar chart comparing no-show rates across specialties.

Visit Type Analysis: A donut chart showing the impact of Telehealth vs. In-Person visits.

Slicer Controls: Interactive filters for Age Range and Appointment Date.

🔍 Key Findings
Wait Time Impact: Patients waiting more than 14 days are 22% more likely to miss their appointment.

Telehealth Advantage: Telehealth visits reduced no-shows by 15% in the Mental Health department.

Peak Risks: The highest volume of no-shows occurred on Friday afternoons, suggesting a need for targeted confirmation calls during those blocks.

📂 Repository Structure
/SQL_Scripts: setup_data.sql (4k row generator) and analysis_queries.sql.

/Excel_Models: Patient_Risk_Calculator.xlsx with formulas and pivot tables.

/PowerBI_Reports: Hospital_Operations_Dashboard.pbix file.

🚀 How to Run
Execute setup_data.sql in your SQL environment to build the database.

Load the resulting data into the Power BI file to populate the visuals.

Review the Excel model to see the Risk Scoring logic in action.
