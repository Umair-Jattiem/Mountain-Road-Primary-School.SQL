# Mountain-Road-Primary-School.SQL
# Primary School Database

## Overview
This is a SQL database designed to manage information for a primary school. It stores details about learners, their guardians, and the learners' academic results. The database allows for efficient storage, retrieval, and reporting of student and guardian information.

## Database Structure

### Students Table
Stores information about each student.

**Columns:**
- `StudentID` (INT, Primary Key, Auto Increment) – Unique identifier for each student  
- `FirstName` (VARCHAR(50)) – Student’s first name  
- `LastName` (VARCHAR(50)) – Student’s last name  
- `DateOfBirth` (DATE) – Student’s date of birth  
- `Grade` (INT) – Current grade of the student

### Guardians Table
Stores information about the guardians of each student.

**Columns:**
- `GuardianID` (INT, Primary Key, Auto Increment) – Unique identifier for each guardian  
- `StudentID` (INT, Foreign Key) – Links the guardian to a student  
- `FirstName` (VARCHAR(50)) – Guardian’s first name  
- `LastName` (VARCHAR(50)) – Guardian’s last name  
- `PhoneNumber` (VARCHAR(20)) – Contact number  
- `Email` (VARCHAR(100)) – Optional email address

### Results Table
Records academic performance of each student.

**Columns:**
- `ResultID` (INT, Primary Key, Auto Increment) – Unique identifier for each result  
- `StudentID` (INT, Foreign Key) – Links the result to a student  
- `Subject` (VARCHAR(50)) – Name of the subject  
- `Score` (DECIMAL(5,2)) – Score achieved in the subject  
- `Term` (VARCHAR(10)) – Term or semester of the result  
- `Year` (INT) – Academic year of the result

## Features
- Maintain up-to-date student and guardian information  
- Track student academic performance  
- Easy to query and generate reports for administration

## Setup
1. Ensure you have a SQL Server or compatible database installed.  
2. Open your SQL interface (e.g., SQL Server Management Studio).  
3. Run the database script to create the database and tables.  
```sql
CREATE DATABASE PrimarySchool;
USE PrimarySchool;
-- Then create tables as defined
