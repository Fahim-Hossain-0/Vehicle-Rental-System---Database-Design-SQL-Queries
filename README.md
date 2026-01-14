# Vehicle Rental System – Database Design & SQL Queries

## 📌 Overview
This project represents a **Vehicle Rental System database** designed to demonstrate core **relational database concepts** and **SQL querying skills**.

The system conceptually manages:
- Users (Admin and Customer)
- Vehicles with availability status
- Bookings connecting users and vehicles

The focus of this assignment is on:
- Understanding ERD relationships
- Using primary and foreign keys correctly
- Writing effective SQL queries using JOIN, EXISTS, WHERE, GROUP BY, and HAVING

All database schema definitions and test data are intentionally excluded from this document.

---

## 🧪 SQL Queries

### Query 1 – INNER JOIN  
Retrieve the customer name and vehicle name for each booking.

```sql
SELECT user_name, vehicle_name
FROM users
INNER JOIN bookings ON users.user_id = bookings.user_id
INNER JOIN vehicles ON vehicles.vehicle_id = bookings.vehicle_id;


Query 2 – NOT EXISTS

Find all vehicles that have never been booked.

SELECT *
FROM vehicles
WHERE NOT EXISTS (
  SELECT 1
  FROM bookings
  WHERE vehicles.vehicle_id = bookings.vehicle_id
);

Query 3 – WHERE

Retrieve all available vehicles of a specific type (e.g. cars).

SELECT *
FROM vehicles
WHERE type = 'car'
  AND availability_status = 'available';

  Query 4 – GROUP BY & HAVING

Find vehicles that have been booked more than two times.

SELECT vehicle_id, COUNT(booking_id)
FROM bookings
GROUP BY vehicle_id
HAVING COUNT(booking_id) > 2;


🎤 Viva / Theory Questions
📘 Question 1

What is a foreign key and why is it important?

Simple Answer:
A foreign key is a column in one table that connects to the primary key of another table.
It is important because it creates a relationship between tables and helps maintain data accuracy.
It also prevents invalid data from being inserted.
For example, user_id in the bookings table is a foreign key that references the users table.

📘 Question 2

What is the difference between WHERE and HAVING?

Simple Answer:
WHERE is used to filter rows before grouping the data.
HAVING is used to filter data after GROUP BY is applied.
WHERE works with normal columns, while HAVING works with aggregate functions like COUNT or SUM.
So, WHERE is applied before GROUP BY, and HAVING is applied after GROUP BY.

📘 Question 3

What is a primary key and its characteristics?

Simple Answer:
A primary key is a column that uniquely identifies each record in a table.
It cannot contain NULL values and cannot have duplicate values.
Each table should have only one primary key.
For example, user_id in the users table is a primary key.

📘 Question 4

What is the difference between INNER JOIN and LEFT JOIN?

Simple Answer:
INNER JOIN returns only the matching records from both tables.
LEFT JOIN returns all records from the left table and matching records from the right table.
If there is no match, LEFT JOIN returns NULL values.
So, INNER JOIN shows common data, while LEFT JOIN shows all left table data.

🔗 Resources

GitHub Repository: https://github.com/your-username/your-repo-name

ERD Diagram: https://lucid.app/

Viva Video: https://drive.google.com/