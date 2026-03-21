# Assignments – Day 12: Database Design Fundamentals

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

In real-world systems, database design is one of the most critical responsibilities of backend engineers.

Poor database design leads to:

- data inconsistency
- performance bottlenecks
- scalability limitations
- complex and fragile systems

This assignment simulates how engineers design **production-grade database schemas**.

You will design both:

- **Relational (SQL) schema**
- **NoSQL (document-based) schema**

for real-world platforms.

---

## 🧠 Part 1 – System Selection

Choose **one platform** to model:

- Uber (Ride Booking System)
- Amazon / BestBuy (E-commerce Platform)

---

## 🧩 Part 2 – Identify Core Entities

Based on your selected system, identify key entities.

---

### Example (Uber)

- Users
- Drivers
- Rides
- Bookings
- Payments
- Addresses

---

### Example (E-commerce)

- Users
- Products
- Orders
- Order Items
- Payments
- Cart
- Addresses

---

### Task

List:

- all possible entities
- key attributes for each entity

---

## 🛠 Part 3 – Relational Database Design (SQL)

Using the provided [**SQL Excel template**](../../templates/db-schema/db-schema-sql.xlsx), design your schema.

Template file:

```
templates/db-schema/db-schema-sql.xlsx
```

---

### Requirements

- define tables
- define columns and data types
- assign primary keys
- define foreign key relationships
- apply constraints (NOT NULL, UNIQUE, etc.)

---

### Example Relationships

```
users → orders
orders → order_items
order_items → products
payments → orders
```

---

### Expectations

- proper normalization
- minimal data duplication
- clear relationships
- consistent naming conventions

---

## 📦 Part 4 – NoSQL Data Modeling

Using the provided [**NoSQL Excel template**](../../templates/db-schema/db-schema-nosql.xlsx), design the same system using a document-based approach.

Template file:

```
templates/db-schema/db-schema-nosql.xlsx
```

---

### Requirements

- define collections
- design JSON-like structures
- decide between:
  - embedding (nested data)
  - referencing (linked data)

---

### Example

```json
{
  "order_id": 1001,
  "user": {
    "id": 1,
    "name": "John"
  },
  "items": [
    {
      "product_id": 101,
      "name": "Laptop",
      "price": 1000
    }
  ]
}
```

---

### Expectations

- reduced number of joins
- optimized read performance
- thoughtful use of denormalization

---

## ⚖️ Part 5 – SQL vs NoSQL Comparison

Compare both designs.

---

### Answer the following:

1. Which design is more normalized?
2. Which design is better for read-heavy systems?
3. Where is data duplication present?
4. Which system is easier to scale horizontally?
5. Which design is easier to maintain consistency?

---

### Output

Write a short comparison (5–10 points).

---

## 🔐 Part 6 – Data Integrity & Constraints

Explain how you ensure data integrity.

---

### Cover:

- primary key usage
- foreign key relationships
- constraints (NOT NULL, UNIQUE)
- validation at database level

---

### For NoSQL:

- how do you prevent invalid data?
- how do you maintain consistency?

---

## 🚀 Part 7 – Scalability Thinking

Think beyond basic schema design.

---

### Answer:

- What happens when your system grows to millions of users?
- Which parts of your system will scale first?
- Would you continue using SQL, NoSQL, or both?
- Where would caching be introduced?

---

## 🔄 Part 8 – Reflection

Answer briefly:

1. What was challenging in designing relational schema?
2. What was different in NoSQL modeling?
3. When would you prefer SQL over NoSQL?
4. How do database decisions impact system architecture?

---

## 📋 Self-Evaluation Checklist

- [ ] I identified relevant entities
- [ ] I designed relational schema using proper relationships
- [ ] I applied normalization principles
- [ ] I designed NoSQL document structures
- [ ] I compared SQL and NoSQL designs
- [ ] I considered scalability and performance

---

## 🧭 Navigation

← Back to Resources  
[Resources](./resources.md)

➡ Next: Day 13  
[Day 13](../day-13/README.md)