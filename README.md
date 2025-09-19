# Personal Wellness SQL Project

## Scenario
A wellness-focused client tracks routine vitals and wants simple analyses.

### Schema 
**Table: visits**
- id (INTEGER, PRIMARY KEY)
- patient_id (INTEGER)
- visit_date (DATE)
- systolic (INTEGER)
- diastolic (INTEGER)
- bmi (REALL)
- pulse (INTEGER)
- notes (TEXT)

  ## Tasks
  1. How many visits occurred each year?
  2. What are the overall average vitals (systolic, diastolic, BMI, pulse)?
  3. Which patients show elevated average BP (avg sys >=130 or avg dia >=80)?
  4. BMI category counts (Under/Normal/Over/Obese).
  5. Last visist date per patient.
  6. Montly average pulse trend (last 6 months).
  7. Outlier systolic readings (>180)
  8. How many distinct patients were seen?
  9. Visits per month for the last 12 months.
  10. Percent of visits by BMI category.
 
  ## What this project shows
  - Grouping, aggregation, and filtering
  - CASE expressions for categories
  - Date functions for monthly rollups
 
  > **Disclaimer**
  > Fictional dataset for educational/portfolio use. No real medical data. 


