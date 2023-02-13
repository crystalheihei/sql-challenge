#### sql-challenge

It’s been two weeks since you were hired as a new data engineer at Pewlett Hackard (a fictional company). Your first major task is to do a research project about people whom the company employed during the 1980s and 1990s. All that remains of the employee database from that period are six CSV files.

For this project, you’ll design the tables to hold the data from the CSV files, import the CSV files into a SQL database, and then answer questions about the data. That is, you’ll perform data modeling, data engineering, and data analysis, respectively.

### Data Modeling
Inspect the CSV files, and then sketch an Entity Relationship Diagram of the tables.
![Entity Relationship Diagram](https://user-images.githubusercontent.com/118711472/218352594-fc9402bd-6755-4174-b179-9c63041fe972.png)

### Data Engineering
Use the provided information to create a table schema for each of the six CSV files.

## departments
-
dept_no PK VARCHAR
dept_name VARCHAR

##dept_emp
-
emp_no PK INT FK >- employees.emp_no
dept_no PK VARCHAR FK >- departments.dept_no

##dept_manager
-
dept_no PK VARCHAR FK >- departments.dept_no
emp_no PK INT FK >- employees.emp_no

employees
-
emp_no PK INT
emp_title_id VARCHAR FK >- titles.title_id
birth_date DATE
first_name VARCHAR
last_name VARCHAR
sex VARCHAR
hire_date DATE

salaries
-
emp_no INT FK >- employees.emp_no
salary INT

titles
-
title_id PK VARCHAR
title VARCHAR
