# HOSPITAL
Hospital Patient Analytics Dashboard  

## Overview  
This Power BI dashboard tracks **hospital performance**, focusing on admissions, patient demographics, readmissions, and revenue.  

## Features  
- Total patients, admissions, and readmissions KPIs  
- Patient demographics by age & gender  
- Department-wise patient load  
- Readmission analysis with root causes  
- Revenue tracking by service type (OPD, IPD, Surgery)  

## Tools & Tech  
- SQL (data aggregation)  
- Power BI (visualization)  
- DAX (calculations)  

## Key Insight  
- Readmission rate: **12%**, highest in **Cardiology**  
- Majority of patients: **age 30–50**  
- Revenue highest from **surgery services**

 SQL
- SELECT Department, COUNT(PatientID) AS Total_Admissions
FROM Admissions
GROUP BY Department;

-- Readmission Rate
SELECT 
    COUNT(CASE WHEN Readmitted = 'Yes' THEN 1 END) * 100.0 / COUNT(*) AS ReadmissionRate
FROM Admissions;
