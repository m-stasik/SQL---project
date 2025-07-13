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

### 🧾 Task 5: Display actors with `actor_id` between 4 and 7 (inclusive), using the AND operator

```sql
SELECT * FROM actors
WHERE actor_id >= 4 AND actor_id <= 7;
```
<img width="307" height="208" alt="image" src="https://github.com/user-attachments/assets/670efe7d-a4cc-4d89-8948-3ecd118a10ee" />

### 🧾 Task 6: Display customers with IDs 2, 4, and 6 using logical conditions

```sql
SELECT * FROM customers
WHERE customer_id = 2 OR customer_id = 4 OR customer_id = 6;
```
<img width="445" height="180" alt="image" src="https://github.com/user-attachments/assets/7a739b27-2603-49f3-b116-aac6fe4e2695" />

### 🧾 Task 7: Display customers with IDs 1, 3, and 5 using the IN operator

```sql
SELECT * FROM customers
WHERE customer_id IN (1, 3, 5);
```
<img width="450" height="176" alt="image" src="https://github.com/user-attachments/assets/59f9a330-a5d9-4806-9845-9a499d1326ab" />

### 🧾 Task 8: Display all actors whose names start with "An"

```sql
SELECT * FROM actors
WHERE name LIKE 'An%';
```
<img width="297" height="141" alt="image" src="https://github.com/user-attachments/assets/0918a750-d0f7-499d-ba64-892d58d63f5f" />

### 🧾 Task 9: Display customers who do not have an email address

```sql
SELECT * FROM customers
WHERE email IS NULL;
```
<img width="392" height="107" alt="image" src="https://github.com/user-attachments/assets/4a406462-21b2-4b7e-b2e6-0edad8796908" />

### 🧾 Task 10: Display all movies priced above $9 with movie_id between 2 and 8

```sql
SELECT * FROM movies
WHERE price > 9 AND movie_id BETWEEN 2 AND 8;
```
<img width="475" height="177" alt="image" src="https://github.com/user-attachments/assets/d405c32c-b62f-420f-8763-566fe58d0bec" />

