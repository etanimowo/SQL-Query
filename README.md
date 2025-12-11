# SQL-Query

# Project: Filtering SQL Queries in company database

# Overview
In this project, I practiced applying SQL filters to efficiently retrieve specific security‑related information from a company database database. As a security analyst, the ability to craft precise queries helps me quickly locate data needed for investigations, system checks, and organizational tasks.

This lab allowed me to query employee data, machine operating systems, and department information using SELECT, WHERE, and LIKE clauses.

# Scenario
My task was to retrieve specific information about employees, their devices, and department assignments so that my team could:
- Deploy updates to certain machines
- Post privacy notices in specific departments
- Notify an employee whose device had a detected issue

To accomplish this, I queried the organization database and applied filters to narrow down results.

# Task 1: Listing All Organization Machines
I started by retrieving a list of all machines in the organization along with their operating systems. I queried the machines table using:

- SELECT device_id, operating_system
- FROM machines;

Outcome: The query returned 200 rows.

I successfully listed all machine IDs and their operating systems.

# Task 2: Finding Machines Running 'OS 2'
Next, I located all machines currently using OS 2, as these required an update. I applied my first filter using the WHERE clause:

- SELECT device_id, operating_system
- FROM machines
- WHERE operating_system = 'OS 2';

Outcome: The database returned 80 machines running OS 2.

This helped identify which devices required an immediate update.

# Task 3: Listing Employees by Department
I queried the employees table to locate staff in specific departments that needed a privacy notice.

# Finance Department Query
- SELECT *
- FROM employees
- WHERE department = 'Finance';

Result: The first employee_id returned was 1003.

# Sales Department Query
- SELECT *
- FROM employees
- WHERE department = 'Sales';

Result: There were 33 employees in the Sales department.

# Task 4: Identifying Employee Machines
A machine located in South‑109 had an issue. I needed to determine which employee used that office.

# Query for a Specific Office
- SELECT *
- FROM employees
- WHERE office = 'South-109';

Outcome: The user ID of the affected employee was jlansky.

# Query for All Employees in the South Building
I then retrieved every employee working in the South building using the LIKE operator:

- SELECT *
- FROM employees
- WHERE office LIKE 'South%';

Outcome: The first employee listed belonged to the Finance department.

# What This Project Taught Me
- How to use SQL filters to quickly extract precise information.
- The practical benefits of writing targeted queries when handling large datasets.
- How relational databases structure information across tables.
- The importance of filtering data for tasks such as security investigations, system updates, and employee notifications.

# Skills Learned
- SQL querying proficiency, including SELECT, WHERE, and LIKE.
- Data filtering and extraction in company database.
- Problem‑solving using relational databases.
- Efficient information retrieval for security tasks.
- Attention to detail when working with large datasets.
