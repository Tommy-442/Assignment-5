# Assignment-5
##Below are the Queries used in excuting my task:
--Total number of employees who left, grouped by department
SELECT 
	e.department,
	COUNT(*) AS total_left
FROM employee e
JOIN department d ON e.department = d.department_name
WHERE e.attrition = 'Yes'
GROUP BY e.department;

--Average monthly income by job role
SELECT
	e.jobrole,
	ROUND(AVG(e.monthlyincome),2) AS avg_monthly_income
FROM employee e
JOIN job_role j ON e.jobrole = j.job_role
GROUP BY e.jobrole;

--Percentage of Employees who left by age range
SELECT 
	CASE
		WHEN age < 30 THEN '<30'
		WHEN age BETWEEN 30 AND 40 THEN '30-40'
		ELSE '>40'
	END AS age_range,
	ROUND(
		(SUM(CASE WHEN attrition = 'Yes' THEN 1 ELSE 0 END)::decimal * 100)/COUNT(*),
		2
	) AS attrition_percentage 
FROM employee
Group by age_range;

--Number of Employees with OverTime ='Yes' AND jobsatisfaction<3
SELECT COUNT(*) AS low_satisafction_overtime_employees
FROM employee
WHERE Overtime = 'Yes' AND jobsatisfaction <3;
