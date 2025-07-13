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
<img width="476" height="99" alt="image" src="https://github.com/user-attachments/assets/3c8429d8-748c-469e-a293-928185f17f45" />

### 🧾 Task 3: Display all movies produced between 1900 and 1999

```sql
SELECT * FROM movies
WHERE year_of_production BETWEEN '1900' AND '1999';
```
<img width="634" height="167" alt="image" src="https://github.com/user-attachments/assets/cc441a44-407c-4872-a8c6-cb2df023c481" />

### 🧾 Task 4: Display titles and prices of movies that cost less than 7

```sql
SELECT title, price FROM movies
WHERE price < 7;
```
<img width="382" height="243" alt="image" src="https://github.com/user-attachments/assets/131d1408-0c51-45e8-a602-512e46d473b6" />

