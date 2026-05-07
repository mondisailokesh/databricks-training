# databricks-training
# Week-1 / day1day2/ SQL Practice Queries

A complete collection of **65 SQL practice queries** designed for beginners to intermediate learners.  
This project covers all major SQL concepts including:

- Basic Queries
- String Matching
- Date Functions
- Aggregate Functions
- GROUP BY & HAVING
- ORDER BY
- JOIN Operations
- Nested & Correlated Subqueries
- Moderate Difficulty SQL Problems

---

# Database Schema

## Employee Table

| Column Name | Data Type |
|------------|------------|
| emp_id | INT |
| name | VARCHAR |
| age | INT |
| salary | INT |
| department_id | INT |
| hire_date | DATE |

---

## Department Table

| Column Name | Data Type |
|------------|------------|
| department_id | INT |
| name | VARCHAR |

---

## Project Table

| Column Name | Data Type |
|------------|------------|
| project_id | INT |
| name | VARCHAR |
| department_id | INT |

---

# Sample Data

## Employee Table

| emp_id | name | age | salary | department_id | hire_date |
|-------|------|-----|--------|---------------|------------|
| 1 | John Doe | 28 | 50000 | 1 | 2020-01-15 |
| 2 | Jane Smith | 34 | 60000 | 2 | 2019-07-23 |
| 3 | Bob Brown | 45 | 80000 | 1 | 2018-02-12 |
| 4 | Alice Blue | 25 | 45000 | 3 | 2021-03-22 |
| 5 | Charlie P. | 29 | 50000 | 2 | 2019-12-01 |

---

## Department Table

| department_id | name |
|---------------|------|
| 1 | IT |
| 2 | HR |
| 3 | Finance |
| 4 | Marketing |

---

## Project Table

| project_id | name | department_id |
|------------|------|---------------|
| 1 | Project Alpha | 1 |
| 2 | Project Beta | 2 |
| 3 | Project Gamma | 1 |
| 4 | Project Delta | 3 |
| 5 | Project Epsilon | 4 |

---

# Topics Covered

## Basic Queries
- SELECT statements
- WHERE clause
- Column selection

## String Matching Queries
- LIKE operator
- Wildcards
- Pattern searching

## Date Queries
- YEAR()
- MONTH()
- Date filtering

## Aggregate Functions
- SUM()
- AVG()
- MIN()
- MAX()
- COUNT()

## GROUP BY Queries
- Department-wise grouping
- Aggregated reports

## HAVING Queries
- Filtering grouped data

## ORDER BY Queries
- Ascending & descending sorting

## JOIN Queries
- INNER JOIN
- LEFT JOIN
- Multi-table joins

## Nested & Correlated Queries
- Subqueries
- Correlated subqueries
- Nth highest salary

## Moderate Difficulty SQL Queries
- Advanced filtering
- Aggregation with joins
- Complex SQL analysis

---

# Total Queries

| Category | Queries |
|----------|----------|
| Basic Queries | 5 |
| String Matching Queries | 5 |
| Date Queries | 5 |
| Aggregate Queries | 5 |
| GROUP BY Queries | 5 |
| HAVING Queries | 5 |
| ORDER BY Queries | 5 |
| JOIN Queries | 10 |
| Nested & Correlated Queries | 10 |
| Combined Moderate Difficulty Queries | 10 |

##Total = 65 Queries

---

# Setup Instructions

## Step 1: Create Database

```sql
CREATE DATABASE sql_practice;
USE sql_practice;
```

---

## Step 2: Create Tables

```sql
CREATE TABLE Department (
    department_id INT PRIMARY KEY,
    name VARCHAR(50)
);

CREATE TABLE Employee (
    emp_id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    salary INT,
    department_id INT,
    hire_date DATE,
    FOREIGN KEY (department_id)
    REFERENCES Department(department_id)
);

CREATE TABLE Project (
    project_id INT PRIMARY KEY,
    name VARCHAR(50),
    department_id INT,
    FOREIGN KEY (department_id)
    REFERENCES Department(department_id)
);
```

---

## Step 3: Insert Sample Data

```sql
INSERT INTO Department VALUES
(1, 'IT'),
(2, 'HR'),
(3, 'Finance'),
(4, 'Marketing');

INSERT INTO Employee VALUES
(1, 'John Doe', 28, 50000, 1, '2020-01-15'),
(2, 'Jane Smith', 34, 60000, 2, '2019-07-23'),
(3, 'Bob Brown', 45, 80000, 1, '2018-02-12'),
(4, 'Alice Blue', 25, 45000, 3, '2021-03-22'),
(5, 'Charlie P.', 29, 50000, 2, '2019-12-01');

INSERT INTO Project VALUES
(1, 'Project Alpha', 1),
(2, 'Project Beta', 2),
(3, 'Project Gamma', 1),
(4, 'Project Delta', 3),
(5, 'Project Epsilon', 4);
```

---
