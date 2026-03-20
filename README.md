# Online-Food-Order-System
# 🍔 Online Food Order System (SQL Project)

## 📌 Project Description

This project is a database design for an *Online Food Ordering System*. It manages users, restaurants, menu items, and orders using SQL.

---

## 🛠️ Technologies Used

* SQL (MySQL)
* Database Design Concepts

---

## 🗂️ Database Structure

### 1. Users Table

Stores customer information:

* user_id (Primary Key)
* name
* city

### 2. Restaurants Table

Stores restaurant details:

* restaurant_id (Primary Key)
* name
* city
* rating

### 3. Menu Table

Stores food items:

* item_id (Primary Key)
* restaurant_id (Foreign Key)
* item_name
* price

### 4. Orders Table

Stores order details:

* order_id (Primary Key)
* user_id (Foreign Key)
* item_id (Foreign Key)
* quantity
* order_date

---

## 🔗 Relationships

* One user can place many orders
* One restaurant can have many menu items
* Each order is linked to a user and a menu item

---

## 📊 Sample SQL Queries

### 🔹 View all users

sql
SELECT * FROM users;


### 🔹 Get all restaurants

sql
SELECT * FROM restaurants;


### 🔹 Join query (User + Orders)

sql
SELECT users.name, orders.order_id
FROM users
JOIN orders ON users.user_id = orders.user_id;


### 🔹 Get menu with restaurant name

sql
SELECT menu.item_name, restaurants.name
FROM menu
JOIN restaurants ON menu.restaurant_id = restaurants.restaurant_id;


---

## 🚀 How to Run

1. Open MySQL / SQL Workbench
2. Create database:

sql
CREATE DATABASE food_order_system;
USE food_order_system;


3. Run the .sql file
4. Execute queries

---

## 🎯 Features

* User Management
* Restaurant Listing
* Menu Management
* Order Tracking
* SQL Joins & Relationships

---

## 📚 Learning Outcomes

* Database Design
* Table Relationships
* SQL Joins
* Query Writing

---

## 👨‍💻 Author

Ankit Jha
