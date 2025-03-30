# Apply Filters to SQL Queries

## Project Description
This project demonstrates how to use SQL queries to filter data effectively based on various criteria. The queries focus on retrieving specific login attempts and employee information from a database.

---

## Retrieve After-Hours Failed Login Attempts
To retrieve failed login attempts that occurred outside of business hours (assuming business hours are from 8 AM to 6 PM), we use the `WHERE` clause with `TIME` functions.

```sql
SELECT * FROM login_attempts
WHERE status = 'failed'
AND attempt_time BETWEEN '08:00:00' AND '18:00:00';
```

```sql
SELECT * FROM login_attempts
WHERE status = 'failed'
AND (HOUR(attempt_time) < 8 OR HOUR(attempt_time) > 18);
```

---

## Retrieve Login Attempts on Specific Dates
To filter login attempts that occurred on a specific date, we use the `DATE` function:

```sql
SELECT * FROM login_attempts
WHERE DATE(attempt_time) = '2024-03-29';
```

For multiple dates:

```sql
SELECT * FROM login_attempts
WHERE attempt_time BETWEEN '2024-03-29' AND '2024-03-30';
```

```sql
SELECT * FROM login_attempts
WHERE DATE(attempt_time) IN ('2024-03-29', '2024-03-30');
```

---

## Retrieve Login Attempts Outside of Mexico
To filter login attempts that are not from Mexico:

```sql
SELECT * FROM login_attempts
WHERE NOT country LIKE 'Mex%';
```

```sql
SELECT * FROM login_attempts
WHERE country <> 'Mexico';
```

Alternatively, using `NOT IN`:

```sql
SELECT * FROM login_attempts
WHERE country NOT IN ('Mexico');
```

---

## Retrieve Employees in Marketing
To retrieve employees belonging to the Marketing department:

```sql
SELECT * FROM employees
WHERE department = 'Marketing';
```

---

## Retrieve Employees in Finance or Sales
To filter employees from Finance or Sales departments:

```sql
SELECT * FROM employees
WHERE department = 'Finance' OR department = 'Sales';
```

```sql
SELECT * FROM employees
WHERE department IN ('Finance', 'Sales');
```

---

## Retrieve All Employees Not in IT
To exclude employees in the IT department:

```sql
SELECT * FROM employees
WHERE NOT department LIKE 'Information Technology';
```

```sql
SELECT * FROM employees
WHERE department <> 'IT';
```

Or using `NOT IN`:

```sql
SELECT * FROM employees
WHERE department NOT IN ('IT');
```

---

## Summary
This document provides SQL queries to filter login attempts and employee records based on specific conditions. These queries demonstrate the use of filtering techniques like `WHERE`, `IN`, `NOT IN`, `<>`, `HOUR()`, and `DATE()`, which are essential for extracting meaningful data from a database efficiently.
