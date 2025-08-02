
# 🧠 SQL Core Concepts Explained Simply (Day 1)

This guide will help you understand the foundational SQL clauses clearly with examples, and clarify the difference between how we **write** a query vs how SQL **executes** it.

---

## 🔹1. `SELECT`
- Used to **choose columns** you want in the output.
- You can:
  - Select all → `SELECT *`
  - Select specific → `SELECT name, age`
- You can also use functions like `SUM()`, `COUNT()`, etc.

---

## 🔹2. `FROM`
- Tells SQL **which table** to fetch data from.

```sql
SELECT name, age
FROM employees;
```

---

## 🔹3. `WHERE`
- Used to **filter individual rows** before any grouping.
- Only brings rows that satisfy a condition.

```sql
SELECT name, age
FROM employees
WHERE age > 30;
```

---

## 🔹4. `GROUP BY`
- Groups rows based on a column and allows aggregate functions.

```sql
SELECT department, COUNT(*) AS total_employees
FROM employees
GROUP BY department;
```

---

## 🔹5. `HAVING`
- Filters **groups** (after `GROUP BY`) based on aggregate conditions.

```sql
SELECT department, COUNT(*) AS total_employees
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;
```

> ✅ Use `WHERE` for filtering rows  
> ✅ Use `HAVING` for filtering grouped data

---

## 🔹6. `DISTINCT`
- Returns **only unique** rows for selected columns.

```sql
SELECT DISTINCT department
FROM employees;
```

---

## 🔹7. `TOP` / `LIMIT`
- Limits the number of rows shown in the result.

```sql
-- SQL Server
SELECT TOP 5 * FROM employees;

-- MySQL/PostgreSQL
SELECT * FROM employees
LIMIT 5;
```

---

## 🔀 Order of Writing vs Execution

| 🔤 **Written Order**        | ⚙️ **Execution Order**           |
|----------------------------|----------------------------------|
| 1. SELECT                  | 1. FROM                          |
| 2. FROM                    | 2. WHERE                         |
| 3. WHERE                   | 3. GROUP BY                      |
| 4. GROUP BY                | 4. HAVING                        |
| 5. HAVING                  | 5. SELECT                        |
| 6. ORDER BY                | 6. ORDER BY                      |
| 7. LIMIT / TOP             | 7. LIMIT / TOP                   |

---

## 🎯 Full Query Example:

```sql
SELECT department, COUNT(*) AS total
FROM employees
WHERE age > 25
GROUP BY department
HAVING COUNT(*) > 3
ORDER BY total DESC
LIMIT 5;
```

### What SQL does behind the scenes:
1. FROM → Get data from `employees`
2. WHERE → Filter rows where `age > 25`
3. GROUP BY → Group rows by `department`
4. HAVING → Keep only groups with count > 3
5. SELECT → Select department and count
6. ORDER BY → Sort by total descending
7. LIMIT → Return only 5 rows

---


