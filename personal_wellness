
-- Personal Wellness SQL Project
-- Schema: visits(id, user_id, visit_date, systolic, diastolic, bmi, pulse, notes)
-- Author: Aziza Brown

-- Task 1: Visits per year
SELECT strftime( '%Y', visit_date) AS yr, COUNT(*) AS visits
FROM visits
GROUP BY  yr
ORDER BY yr;

--Task 2: Average vitals overall
SELECT AVG(systolic) AS avg_sys, AVG(diastolic) AS avg_diastolic, AVG(bmi) AS avg_bmi, AVG(pulse) AS avg_pulse
FROM visits;

-- Task 3: Users with elevated average BP
SELECT user_id, 
      AVG(systolic) AS avg_sys, AVG(diastolic) AS avg_diastolic
FROM visits
GROUP BY user_id
HAVING AVG(systolic) >= 130 OR AVG(diastolic) >= 80
ORDER BY avg_systolic DESC, avg_diastolic DESC;

-- Task 4: BMI categories count
SELECT CASE
      WHEN bmi < 18.5 THEN 'Under'
      WHEN bmi < 25   THEN 'Normal'
      WHEN bmi < 30   THEN 'Over'
      ELSE 'Obese'
    END As bmi_band,
    COUNT (*) AS n
FROM vists
GROUP BY bmi_band
ORDER BY n DESC;

-- Task 5: Last visit per user
SELECT user_id, MAX(visit_date) AS last_visit
FROM visits
GROUP BY user_id
ORDER BY last_visit DESC;

-- Task 6: Monthly average pulse trend (last 6)
SELECT strftime('%Y', visit_date) AS ym, AVG(pulse) AS avg_pulse
FROM visits
GROUP BY ym
ORDER BY ym DESC
LIMIT 6;

-- Task 7: Outlier systoliic readings (>180)
SELECT user_id, visit_date, systolic
FROM vistits
WHERE systolic > 180
ORDER BY systolic DESC;

-- Task 8: Distinct users seen
SELECT COUNT(DISTINCT user_id) AS users FROM visits;

-- Task 9: Monthly visits (last 12)
SELECT
FROM
GROUP BY
ORDER BY
LIMIT

-- Task 10: Percent of visits by BMI category
WITH b AS
  SELECT CASE
          WHEN bmi < 18.5 THEN 'Under'
          WHEN bmi < 25   THEN 'Normal'
          WHEN bmi < 30   THEN 'Over'
          ELSE 'Obese'
        END AS band
    FROM visits
)
SELECT band
       ROUND(100.0 * COUNT(*) / (SELECT COUNT(*) FROM b), 2) AS pct
FROM b
GROUP BY band
ORDER BY pct DESC;
