# Symphony of SQL

Welcome to my GitHub profile! Here, you can explore my projects and contributions. 
One of the featured repositories is **Symphony of SQL**, which showcases my skills in working with complex datasets and SQL through various case studies.

## Symphony of SQL Overview

The Symphony of SQL is a collection of diverse SQL case studies, including the HR Database Schema, designed to manage an organization's data related to employees, departments, jobs, and locations. This schema is a downloaded dataset that I have used to enhance my SQL skills and understanding of database management.

### Schema Tables Overview

| Table           | Columns                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| **regions**     | region_id, region_name                                                                                                        |
| **countries**   | country_id, country_name, region_id                                                                                           |
| **locations**   | location_id, street_address, postal_code, city, state_province, country_id                                                    |
| **departments** | department_id, department_name, manager_id, location_id                                                                       |
| **jobs**        | job_id, job_title, min_salary, max_salary                                                                                     |
| **employees**   | employee_id, first_name, last_name, email, phone_number, hire_date, job_id, salary, commission_pct, manager_id, department_id |
| **job_history** | employee_id, start_date, end_date, job_id, department_id                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------------------------|
### Sample SQL Queries

Below are some sample SQL queries used to interact with the HR Database:

1. **Retrieve Employee Details:**
   ```sql
   SELECT * FROM employees WHERE employee_id = 101;

2. **List of Departments and Locations:**
   ```sql
    SELECT d.department_name, l.city 
    FROM departments d 
    JOIN locations l ON d.location_id = l.location_id;

3. **Employee Salary Details:**
   ```sql
    SELECT first_name, last_name, salary 
    FROM employees 
    WHERE department_id = 100;
