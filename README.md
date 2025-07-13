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

### 🧾 Task 11: Correct the surname of customer with ID 3 from "Muler" to "Miler"

```sql
UPDATE customers
SET surname = 'Miler'
WHERE customer_id = 3;
```
<img width="453" height="289" alt="image" src="https://github.com/user-attachments/assets/2e2958fe-cb16-4427-9c0b-cc16cfc187f5" />

### 🧾 Task 12: Find the name and email of the customer who bought the movie with ID 4 using JOIN

```sql
SELECT sale.movie_id, customers.name, customers.surname, customers.email
FROM customers
JOIN sale ON customers.customer_id = sale.customer_id
WHERE sale.movie_id = 4;
```
<img width="228" height="103" alt="image" src="https://github.com/user-attachments/assets/cad028bc-d953-4a82-924f-a4273dc017bc" />

### 🧾 Task 13: Update the email of the customer named Patrycja to pati@mail.com

```sql
UPDATE customers
SET email = 'pati@mail.com'
WHERE name LIKE 'Patrycja';
```
<img width="443" height="276" alt="image" src="https://github.com/user-attachments/assets/6b4ae6a0-1a4f-47fd-8c67-690339c60b88" />

### 🧾 Task 14: Display the name and surname of customers along with the title of the rented movie for each purchase using INNER JOIN

```sql
SELECT customers.name, customers.surname, movies.title
FROM sale
INNER JOIN customers ON customers.customer_id = sale.customer_id
INNER JOIN movies ON sale.movie_id = movies.movie_id;
```
<img width="492" height="555" alt="image" src="https://github.com/user-attachments/assets/d6739871-61cc-49ac-a758-e09786637f0a" />

### 🧾 Task 15: Add a ‘pseudonym’ column and fill it with pseudonyms created from the first two letters of the name and the last letter of the surname

```sql
ALTER TABLE customers ADD pseudonym VARCHAR(200);

UPDATE customers
SET pseudonym = CONCAT(LEFT(name, 2), RIGHT(surname, 1));
```
<img width="563" height="273" alt="image" src="https://github.com/user-attachments/assets/e2da0436-addc-4396-b0e2-398fc8f345f1" />

### 🧾 Task 16: Display titles of purchased movies without duplicates

```sql
SELECT DISTINCT movies.movie_id, movies.title
FROM sale
INNER JOIN movies ON sale.movie_id = movies.movie_id
ORDER BY movies.movie_id;
```
<img width="448" height="380" alt="image" src="https://github.com/user-attachments/assets/993cf642-0d20-431a-85c5-969932f73761" />

### 🧾 Task 17: Display a combined, alphabetically ordered list of all actor and customer names using UNION

```sql
SELECT name FROM actors
UNION
SELECT name FROM customers
ORDER BY name;
```
<img width="157" height="627" alt="image" src="https://github.com/user-attachments/assets/3a2fa97b-1218-44ac-a82e-9c5ac452ae14" />

### 🧾 Task 18: Increase the price of all movies produced after the year 2000 by 2.5

```sql
UPDATE movies
SET price = price + 2.5
WHERE year_of_production > 2000;
```
<img width="634" height="387" alt="image" src="https://github.com/user-attachments/assets/69ee0260-3ce4-427a-995f-7414f3d4e676" />

### 🧾 Task 19: Display the name and surname of the actor with ID 4 and the title of the movie they acted in

```sql
SELECT actors.actor_id, actors.name, actors.surname, movies.title
FROM actors
JOIN cast ON cast.actor_id = actors.actor_id
JOIN movies ON movies.movie_id = cast.movie_id
WHERE actors.actor_id = 4;
```
<img width="291" height="101" alt="image" src="https://github.com/user-attachments/assets/bb607381-a521-4f50-9bfa-33dcf2d67925" />

### 🧾 Task 20: Add a new customer with specific details including pseudonym

```sql
INSERT INTO customers (customer_id, name, surname, email, pseudonym)
VALUES (7, 'Honia', 'Stuczka-Kucharska', 'honia@mail.com', 'Hoa');
```
<img width="626" height="308" alt="image" src="https://github.com/user-attachments/assets/9a46382e-2503-4c52-8b2a-2b257f1f8a86" />
