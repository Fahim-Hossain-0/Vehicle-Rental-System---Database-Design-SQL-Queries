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

### 🔹 Query 1: INNER JOIN  
Retrieve customer name and vehicle name for each booking.

```sql
SELECT user_name, vehicle_name
FROM users
INNER JOIN bookings ON users.user_id = bookings.user_id
INNER JOIN vehicles ON vehicles.vehicle_id = bookings.vehicle_id;

🔹 Query 2: NOT EXISTS

Find all vehicles that have never been booked.

SELECT *
FROM vehicles
WHERE NOT EXISTS (
  SELECT 1
  FROM bookings
  WHERE vehicles.vehicle_id = bookings.vehicle_id
);

🔹 Query 3: WHERE

Retrieve all available vehicles of a specific type (e.g. cars).

SELECT *
FROM vehicles
WHERE type = 'car'
AND availability_status = 'available';

🔹 Query 4: GROUP BY & HAVING

Find vehicles that have been booked more than 2 times.

SELECT vehicle_id, COUNT(booking_id)
FROM bookings
GROUP BY vehicle_id
HAVING COUNT(booking_id) > 2;


## 🔗 Resources

| Resource          | Link |
|------------------|------|
| GitHub Repository | [GitHub Repo](#) |
| ERD Diagram       | [ERD Link](#) |
| Viva Video        | [Viva Video](#) |