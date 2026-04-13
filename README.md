# SQL Learning Project

## 📘  String Functions

This  explores built-in SQL string functions used to manipulate and analyze text data.

---

## 🔍 Key Concepts

String functions allow you to:

* Transform text (UPPER, LOWER)
* Clean data (TRIM)
* Extract parts of strings (SUBSTRING, LEFT, RIGHT)
* Search within text (LOCATE)
* Replace characters (REPLACE)
* Combine columns (CONCAT)

---

## 🔤 Functions Covered

### 1. LENGTH

Returns the number of characters in a string

```sql id="t9w0df"
SELECT LENGTH('Skyfall');
```
<img width="1751" height="834" alt="image" src="https://github.com/user-attachments/assets/0cbe71bd-59df-4c49-bbe3-bc42373bdf4a" />

---

### 2. UPPER & LOWER

Convert text to uppercase or lowercase

```sql id="l1h9gs"
SELECT UPPER('sky');
SELECT LOWER('SKY');
```
<img width="1500" height="713" alt="image" src="https://github.com/user-attachments/assets/51ab6a69-5975-4204-8f5d-6720608b9457" />


<img width="1592" height="833" alt="image" src="https://github.com/user-attachments/assets/db46d0c6-f226-4f24-bc98-bc0b2adf1dfe" />

---

### 3. TRIM Functions

Remove spaces from text

```sql id="0e7l8z"
SELECT TRIM('     Sky    ');
SELECT LTRIM('     Sky    ');
SELECT RTRIM('     Sky    ');
```
<img width="1790" height="815" alt="image" src="https://github.com/user-attachments/assets/5a5aaa5b-ff51-4246-bee7-a916b9b64e9a" />

<img width="1912" height="507" alt="image" src="https://github.com/user-attachments/assets/dfba04a2-8d36-42a2-a6e0-3c562ecbb4ae" />

<img width="1712" height="781" alt="image" src="https://github.com/user-attachments/assets/44a21438-9459-4e82-b102-c6187f12a043" />

---

### 4. LEFT, RIGHT, SUBSTRING

Extract parts of strings

```sql id="2y6qpo"
SELECT 
  LEFT(first_name,4),
  RIGHT(first_name,4),
  SUBSTRING(first_name,3,2)
FROM employee_demographics;
```
<img width="1660" height="883" alt="image" src="https://github.com/user-attachments/assets/acbf384a-af9a-43f7-a76e-b67abb85401f" />

---

### 5. Extracting Data (Example: Month from Date)

```sql id="k3rmq1"
SELECT 
  birth_date,
  SUBSTRING(birth_date, 6,2) AS birth_month
FROM employee_demographics;
```
<img width="1683" height="896" alt="image" src="https://github.com/user-attachments/assets/f9cfdda4-992f-4878-80c3-069a288212b9" />

---

### 6. REPLACE

Replace characters in a string

```sql id="3g1o8w"
SELECT first_name, REPLACE(first_name, 'a','z')
FROM employee_demographics;
```
<img width="1481" height="880" alt="image" src="https://github.com/user-attachments/assets/1f221666-6a8a-4cf0-b104-343f8168e1c6" />

---

### 7. LOCATE

Find position of a substring

```sql id="k6z2xq"
SELECT LOCATE('x', 'lexander');
```
<img width="1312" height="775" alt="image" src="https://github.com/user-attachments/assets/cd6134b4-7d0b-4805-a3e9-bb5644312a78" />

---

### 8. CONCAT

Combine multiple columns into one

```sql id="9fz8gm"
SELECT 
  first_name, 
  last_name,
  CONCAT(first_name,' ', last_name) AS full_name
FROM employee_demographics;
```
<img width="1748" height="962" alt="image" src="https://github.com/user-attachments/assets/ddd7eddb-37fe-4e54-a24f-b796953c45fc" />

---

## 🧠 Summary

| Function             | Purpose               |
| -------------------- | --------------------- |
| LENGTH               | Count characters      |
| UPPER / LOWER        | Change text case      |
| TRIM / LTRIM / RTRIM | Remove spaces         |
| LEFT / RIGHT         | Extract from ends     |
| SUBSTRING            | Extract from position |
| REPLACE              | Replace characters    |
| LOCATE               | Find position         |
| CONCAT               | Combine text          |

---



