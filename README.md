# Assignment-5
## Employee Attrition Data Analysis
In this project, I worked on analyzing an employee dataset to gain insights into attrition trends and key HR metrics. 
Below, I’ve summarized exactly how I approached and executed each task:
## Data Ingestion & Storage
I started by ingesting the CSV dataset into a PostgreSQL database. To ensure the data was clean and scalable, I designed a normalized database schema. 
This involved splitting out categorical columns such as JobRole, Department, and EducationField into separate reference tables. 
Doing this helps avoid redundancy and makes the database more maintainable in the long run.
