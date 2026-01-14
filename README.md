# Vehicle Rental System – Database Design & SQL Queries

## 📌 Overview
This project is a **Vehicle Rental System database design** created to demonstrate understanding of **relational database concepts**, **ERD design**, and **SQL queries**.  
The system manages users, vehicles, and bookings while following real-world business rules.

This assignment focuses on:
- Database table design
- Entity Relationship Diagram (ERD)
- SQL queries using JOIN, EXISTS, WHERE, GROUP BY, and HAVING

---

## 🎯 Objectives
By completing this project, you will be able to:
- Design an ERD with **One-to-One**, **One-to-Many**, and **Many-to-One** relationships
- Understand and implement **Primary Keys** and **Foreign Keys**
- Write optimized SQL queries using:
  - INNER JOIN
  - NOT EXISTS
  - WHERE
  - GROUP BY and HAVING

---

## 🗂️ System Modules
The Vehicle Rental System manages the following entities:

- **Users**
- **Vehicles**
- **Bookings**

---

## 🧠 Business Logic & Requirements

### 👤 Users Table
Stores system users.
- User role (Admin or Customer)
- Name, email, password, phone number
- Email must be **unique**

### 🚗 Vehicles Table
Stores vehicle information.
- Vehicle name
- Type (car / bike / truck)
- Model
- Registration number (**unique**)
- Rental price per day
- Availability status:
  - available
  - rented
  - maintenance

### 📖 Bookings Table
Stores rental booking data.
- Linked user (Foreign Key)
- Linked vehicle (Foreign Key)
- Rental start and end date
- Booking status:
  - pending
  - confirmed
  - completed
  - canceled
- Total booking cost

---

## 🧩 Part 1: ERD Design (Mandatory)

### 📌 Required Tables
- Users
- Vehicles
- Bookings

### 🔗 Relationship Requirements
Your ERD must clearly show:
- **One-to-Many**: Users → Bookings
- **Many-to-One**: Bookings → Vehicles
- **One-to-One (logical)**: Each booking links one user and one vehicle

### 🧾 ERD Must Include
- Primary Keys (PK)
- Foreign Keys (FK)
- Relationship cardinality
- Status fields (booking status, vehicle availability)

### 📤 Submission Format
- ERD created using **Lucidchart**
- Submit a **public, shareable ERD link**

⚠️ **Note:** ERD submission is mandatory. Missing ERD will result in **0 marks**.

---

## 🧪 Part 2: SQL Queries

> Sample Input/Output can be found in the `QUERY.md` file.

### 🔹 Query 1: JOIN
Retrieve booking information including:
- Customer name
- Vehicle name  

**Concepts Used:**  
`INNER JOIN`

---

### 🔹 Query 2: EXISTS
Find all vehicles that have **never been booked**.

**Concepts Used:**  
`NOT EXISTS`

---

### 🔹 Query 3: WHERE
Retrieve all **available vehicles** of a specific type (e.g. cars).

**Concepts Used:**  
`SELECT`, `WHERE`

---

### 🔹 Query 4: GROUP BY & HAVING
Find the total number of bookings per vehicle and display only vehicles with **more than 2 bookings**.

**Concepts Used:**  
`GROUP BY`, `HAVING`, `COUNT`

---

## 🎥 Part 3: Theory Questions (Viva Practice)

> Answer the questions in your own words and record a video in **Bengali or English**.  
> Spend about **2 minutes per question**.

> _“This video is a safe space to practice — confidence grows every time you speak.”_

### Questions
1. What is a foreign key and why is it important in relational databases?
2. What is the difference between WHERE and HAVING clauses in SQL?
3. What is a primary key and what are its characteristics?
4. What is the difference between INNER JOIN and LEFT JOIN in SQL?

---

## 🔗 Resources

| Resource        | Link |
|-----------------|------|
| GitHub Repository | [GitHub Repo](https://github.com/your-username/your-repo-name) |
| ERD Diagram       | [ERD Link](https://lucid.app/) |
| Viva Video        | [Viva Video](https://drive.google.com/) |


---

## ✅ Conclusion
This project demonstrates a complete relational database design for a Vehicle Rental System, including ERD modeling, business logic implementation, and SQL query execution following real-world scenarios.

---
