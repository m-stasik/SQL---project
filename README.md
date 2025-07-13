# 🧠 SQL Learning Project

This repository contains a set of tasks I completed while learning the basics of SQL.  
The goal of this project is to showcase my understanding of how to query and manipulate data using SQL syntax and logic.

## 🛠️ What I learned

During the course, I became familiar with key SQL concepts and commands such as:

- **Data selection & filtering:** `SELECT`, `FROM`, `WHERE`, `ORDER BY`, `GROUP BY`, `BETWEEN`, `LIKE`, `IS`, `AND`, `OR`
- **Table operations:** `JOIN`, use of `AS` for aliasing
- **Aggregation functions:** `COUNT`, `SUM`, `MIN`
- **String & date functions:** `GETDATE`, `UPPER`, `LOWER`, `DATEDIFF`

**Below, I present practical examples of how these commands and functions are used in real queries.**

### 🧾 Task 1: Display the `actors` table sorted alphabetically by surname

```sql
SELECT * FROM actors
ORDER BY surname;
```
<img width="806" height="387" alt="218763255-1e594436-edb0-441c-a970-e2faeb462ede" src="https://github.com/user-attachments/assets/76715233-4295-40da-965d-b47f5aec136b" />

### 🧾 Task 2: Display the movie produced in 2019

```sql
SELECT * FROM movies
WHERE year_of_production = '2019';
```
https://user-images.githubusercontent.com/3789650/218768201-b622b015-ebb7-4cd4-bd61-4d794292231f.png<img width="476" height="99" alt="image" src="https://github.com/user-attachments/assets/3c8429d8-748c-469e-a293-928185f17f45" />
