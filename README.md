# Assignment-5
## Employee Attrition Data Analysis
In this project, I worked on analyzing an employee dataset to gain insights into attrition trends and key HR metrics. 
Below, I’ve summarized exactly how I approached and executed each task:
## Data Ingestion & Storage
I started by ingesting the CSV dataset into a PostgreSQL database. To ensure the data was clean and scalable, I designed a normalized database schema. 
This involved splitting out categorical columns such as JobRole, Department, and EducationField into separate reference tables. 
Doing this helps avoid redundancy and makes the database more maintainable in the long run.
## Data Cleaning
I handled missing or inconsistent values across the dataset. I standardized categorical data by unifying formats for example, 
converting job roles like Sales Executive to sales executive to maintain consistency and simplify querying. 
I also ensured all column names and string data followed a consistent style.
## Reporting & SQL Queries
I wrote several SQL queries to generate key insights:
1. The total number of employees who left, grouped by department.
2. Average monthly income broken down by job role.
3. Percentage of employees who left, grouped into age buckets: <30, 30–40, and >40.
4. Number of employees who worked overtime (OverTime = 'Yes') and had a job satisfaction score below 3.
