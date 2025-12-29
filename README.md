[README.txt](https://github.com/user-attachments/files/24368226/README.txt)
PROMOTION & JOB APPLICATION MANAGEMENT DATABASE SYSTEM
Database Systems Laboratory Project 2023–2024



DESCRIPTION
This project implements a relational database system for managing job postings,
employee applications, evaluation procedures, and database administration logging.
The system is developed using MySQL and focuses on data integrity, automation,
and performance through stored procedures and triggers.


MAIN FEATURES

1. User & Role Management
- Users, Employees, Evaluators, and DBAs
- Separate tables and role-based responsibilities

2. Job & Application Management
- Job postings with evaluators assigned
- Employees can apply for jobs
- Application states: active, completed, cancelled
- Constraints:
  - Maximum 3 active applications per employee
  - Applications must be submitted at least 15 days before job start date
  - Applications cannot be cancelled less than 10 days before job start date

3. Application Evaluation
- Two evaluators per application
- Scores range from 1 to 20
- Automatic calculation of final evaluation score based on:
  - Academic degrees (BSc, MSc, PhD)
  - Known languages
  - Completed projects

4. Application History
- Completed applications are stored in application_history
- Over 60,000 records generated via stored procedure
- Query support by grade range and evaluator

5. Stored Procedures
- manage_application
- get_or_calculate_evaluation_grade
- process_job_applications
- get_applications_in_grade_range
- get_applications_by_evaluator

6. Triggers
- Validation of application constraints on INSERT/UPDATE
- Automatic logging of DBA actions
- Integrity enforcement for critical tables

7. Database Administration (DBA)
- Dedicated DBA role
- Logging of INSERT, UPDATE, DELETE actions
- Audit trail stored in dba_log table



TECHNOLOGIES
- MySQL
- SQL (DDL, DML)
- Stored Procedures
- Triggers
- Constraints & Indexes


EXECUTION STEPS
1. Create the database schema
2. Execute table creation scripts
3. Insert sample data
4. Create stored procedures and triggers
5. Run test queries and procedure calls



STUDENT INFORMATION
Name: Antonis Zaverdas
Student ID: 1093352
Year: 3rd Year
Date: January 2024
