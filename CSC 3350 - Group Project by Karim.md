# CSC 3350 - Group Project
Outline by Karim, Youssef, and Teferi
from April 2nd
.md by Ethan
## Programming Tasks
Employee Login with View-Only Access
Employees log in and can only view their own data. Restrict access using MySQL security or application-level filtering.
## Admin Login with CRUD Access
Build a login system that identifies admin users. Admins can create, read, update, and delete any employee record. Implemented using PHP/MySQL.
## Admin Search for Employee using Name, DOB, SSN, EMPID
Ensure admin can enter search criteria in a form. Server queries the database using dynamic filters. Returns matching employee records for editing.
## Update Employee’s Salary by Percentage Based on Range
Admin enters a percentage and a salary range. Application updates all matching employee salaries using a SQL UPDATE query with WHERE salary BETWEEN ...
## Generate Reports using EMPID
We’re creating a reporting module using PHP and MySQL that allows both admins and employees to view key payroll information. Admins can access the full pay history for all employees, while employees can log in and view only their own pay statements based on their session ID. This functionality is implemented using a SQL JOIN between the payroll and employees tables, filtered by empid where necessary. The results are displayed in styled HTML tables, and JavaScript is used to enhance interactivity with features like sorting and filtering.
### Programming Test Cases
Feature A: Update Employee Data
Develop functionality for the admin to update any employee information. This includes fields like name, phone number, email, address, DOB, and job title. The system will use a universal form that dynamically loads an employee's data after selecting them from a search result. Updated values are submitted and saved to the database via an UPDATE SQL query.
#### Test Case A:
Input: Admin selects an employee and updates their address and phone number.
Expected Result: New data is saved in the database.
Pass Criteria: Data appears updated upon page reload or re-query. No SQL or logic errors.
Feature B: Search for Employee (Admin)
Implement an advanced search form where admins can search employees by empID, first name, last name, DOB, or SSN. Backend uses parameterized SQL queries to return accurate search results and prevent SQL injection. Results populate in a responsive table view.
#### Test Case B:
Input: Admin searches for employees using last name = 'Smith'.
Expected Result: All employees with last name 'Smith' are displayed.
Pass Criteria: Only relevant records are returned. Search handles blanks, special characters, and invalid values.
Feature C: Update Salary Based on Range
Build a utility for admins to apply a percentage-based raise to employees whose current salary falls below a certain threshold (e.g., increase by 5% for anyone under $60,000). This uses SQL logic with WHERE and SET.
#### Test Case C:
Input: Admin applies a 5% raise to all employees