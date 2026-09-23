# 📚 Library Management Database

A database design for a **Library Management System**, created to practice database fundamentals, relational modeling, and Entity-Relationship Diagrams (ERD).

---

## 🗂️ Database Overview

This project models the main operations of a library, including:

* Managing users
* Managing books and their physical copies
* Borrowing and returning books
* Book reservations
* Managing fines

---

## 🧩 Database Entities

### 👤 Users

Stores information about library users.

**Fields:**

* `User_ID` — Primary Key
* `Name`
* `Contact_Info`
* `LibraryCardNumber`

---

### 📚 Books

Stores information about books.

**Fields:**

* `Book_ID` — Primary Key
* `Title`
* `Genre`
* `ISBN`
* `Publication_Date`
* `Additional_Details`

---

### 📖 Book Copies

Represents the physical copies of books available in the library.

**Fields:**

* `Copy_ID` — Primary Key
* `Book_ID` — Foreign Key
* `Availability_Status`

A single book can have multiple physical copies.

---

### 🔄 Borrowing Records

Stores book borrowing and return information.

**Fields:**

* `Borrowing_and_Returns_ID` — Primary Key
* `User_ID` — Foreign Key
* `Copy_ID` — Foreign Key
* `Borrowing_Date`
* `Due_Date`
* `Actual_Return_Date`

---

### 📅 Reservations

Stores reservations made by users for book copies.

**Fields:**

* `Reservations_ID` — Primary Key
* `User_ID` — Foreign Key
* `Copy_ID` — Foreign Key
* `Reservation_Date`

---

### 💰 Fines

Stores fines associated with borrowing records.

**Fields:**

* `Fine_ID` — Primary Key
* `User_ID` — Foreign Key
* `Borrowing_Record_ID` — Foreign Key
* `Amount`

---

## 🔗 Relationships

The database follows these main relationships:

```text
Users
 ├── Borrowing Records
 ├── Reservations
 └── Fines

Books
 └── Book Copies
       ├── Borrowing Records
       └── Reservations

Borrowing Records
 └── Fines
```

---

## 🧠 Concepts Practiced

* Relational Database Design
* Entity-Relationship Modeling
* Primary Keys
* Foreign Keys
* One-to-Many Relationships
* Database Normalization
* Library Management System Modeling

---

## 📐 ERD

The database structure is represented using an **Entity-Relationship Diagram (ERD)** created with draw.io / diagrams.net.

---

## 🎯 Goal

The goal of this project is to strengthen my understanding of **SQL databases, relational database design, and data modeling** as part of my journey toward becoming a **.NET Backend Developer**.
