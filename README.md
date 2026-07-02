# Student Management System

A robust console-based Java application utilizing JDBC to perform complete CRUD (Create, Read, Update, Delete) operations on a MySQL database. This project serves as a practical demonstration of core Java architectures, database connectivity, and automated integration testing using JUnit 5.

---

## 🛠️ Tech Stack & Dependencies

* **Language:** Java (JDK 8 or higher)
* **Database:** MySQL Server
* **IDE:** IntelliJ IDEA
* **Libraries:**
    * `mysql-connector-j:8.3.0` (Database Driver)
    * `junit-jupiter:5.10.2` (Automated Testing Framework)

---

## 🚀 Features & CRUD Operations

The system provides a loop-driven console interface supporting the following operations:

1.  **Add Student (Create):** Captures name, phone number, and city, instantiates a `Student` model object, and persists it via a `PreparedStatement`.
2.  **Delete Student (Delete):** Removes a student record dynamically using their unique primary key ID (`sid`).
3.  **Display Students (Read):** Fetches and streams all student records into a cleanly aligned, formatted console table layout.
4.  **Update Student City (Update):** Modifies the city attribute of a specific student identified by their ID.

---

## 📊 Database Schema Setup

Before running the application, initialize your local MySQL instance and run the following script to configure the schema:

```sql
CREATE DATABASE IF NOT EXISTS student_manage;
USE student_manage;

CREATE TABLE IF NOT EXISTS students (
    sid INT NOT NULL AUTO_INCREMENT,
    sname VARCHAR(100) NOT NULL,
    sphone VARCHAR(15) NOT NULL,
    scity VARCHAR(50) NOT NULL,
    PRIMARY KEY (sid)
);
