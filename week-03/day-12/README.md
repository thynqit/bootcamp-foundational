# Day 12 – Database Design Fundamentals (SQL & NoSQL)

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

Backend systems rely on databases to store, retrieve, and manage data efficiently.

A well-designed database ensures:

- data consistency
- efficient queries
- scalability
- maintainability

Modern applications use **multiple types of databases**, primarily:

- **Relational (SQL)** – structured, consistent, and transactional
- **NoSQL** – flexible, scalable, and optimized for distributed systems

Understanding both is critical for designing real-world backend systems.

Poor database design leads to:

- data duplication
- performance issues
- inconsistent data
- complex queries
- difficult system evolution

This module introduces **database design fundamentals across SQL and NoSQL systems**, helping you understand how to model data effectively for different use cases.

---

## 🎯 Learning Objectives

By the end of this module, learners should be able to:

- Understand how databases store and organize data
- Design relational schemas using tables, keys, and relationships
- Apply normalization principles for structured data
- Understand indexing and constraints for performance and integrity
- Explain NoSQL database types and use cases
- Model data using document-based and denormalized approaches
- Compare SQL vs NoSQL and choose the right approach
- Design simple database schemas for real-world systems

---

## 🧠 Core Concepts

### 1. What is a Database?

A database is a structured system used to store and manage data.

Applications use databases to:

- store user information
- manage transactions
- retrieve and update data efficiently

Databases are broadly categorized into:

- **Relational (SQL)**
- **Non-relational (NoSQL)**

---

### 2. Relational Databases (SQL)

Relational databases organize data into:

- tables
- rows (records)
- columns (fields)

Example:

| id | name | email |
|----|------|------|
| 1 | John | john@example.com |

Examples of relational databases:

- PostgreSQL
- MySQL
- Oracle
- SQL Server

Relational databases enforce structure using schemas.

---

### 3. Tables, Rows, and Columns

Each table represents an entity.

Examples:

```
users
orders
products
```

Each table contains:

- columns → attributes
- rows → records

Example:

```
users
- id
- name
- email
```

---

### 4. Primary Keys

A primary key uniquely identifies each record.

Example:

```
users.id
orders.id
```

Properties:

- unique
- not null
- stable

Primary keys ensure data integrity.

---

### 5. Foreign Keys & Relationships

Foreign keys define relationships between tables.

Example:

```
orders.user_id → users.id
```

Types of relationships:

- one-to-one
- one-to-many
- many-to-many

Example:

```
One user → many orders
```

---

### 6. Normalization

Normalization reduces redundancy by splitting data into related tables.

Benefits:

- avoids duplication
- improves consistency
- simplifies updates

Example:

Instead of duplicating user data in orders:

```
orders → user_id reference
```

---

### 7. Indexing (Performance Optimization)

Indexes improve query performance.

Without index:

```
Full table scan
```

With index:

```
Direct lookup
```

Common use cases:

- searching by email
- joining tables using foreign keys

---

### 8. Constraints

Constraints enforce data integrity.

Examples:

- NOT NULL
- UNIQUE
- FOREIGN KEY
- CHECK

Example:

```
price > 0
email must be unique
```

---

### 9. What is NoSQL?

NoSQL databases are designed for:

- large-scale systems
- flexible schemas
- distributed architectures

They do not require fixed table structures.

Data can be stored as:

- documents (JSON)
- key-value pairs
- columns
- graphs

Example (Document):

```json
{
  "id": 101,
  "name": "John",
  "orders": [
    {
      "order_id": 5001,
      "amount": 250
    }
  ]
}
```

---

### 10. Types of NoSQL Databases

#### Document Databases

- JSON-like documents
- flexible schema

Examples:

- MongoDB
- Couchbase

---

#### Key-Value Stores

- simple key → value storage
- extremely fast

Examples:

- Redis
- DynamoDB

---

#### Column-Family Databases

- store data in columns
- optimized for analytics

Examples:

- Cassandra
- HBase

---

#### Graph Databases

- optimized for relationships

Examples:

- Neo4j

---

### 11. NoSQL Data Modeling

NoSQL uses **denormalization**.

Instead of splitting data:

- related data is stored together

Example:

```json
{
  "order_id": 5001,
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

Advantages:

- faster reads
- fewer joins
- better performance at scale

Trade-offs:

- data duplication
- harder updates
- eventual consistency

---

### 12. SQL vs NoSQL (When to Use What)

| Feature | SQL | NoSQL |
|--------|-----|------|
| Schema | Fixed | Flexible |
| Scaling | Vertical | Horizontal |
| Transactions | Strong (ACID) | Eventual consistency |
| Relationships | Strong | Limited |
| Use Case | Financial systems | High-scale apps |

---

### When to Use SQL

- structured data
- strong consistency required
- complex relationships
- financial systems

---

### When to Use NoSQL

- large-scale systems
- flexible schema requirements
- high read/write throughput
- distributed systems

---

### Real-World Example

E-commerce platform:

- SQL → orders, payments (critical data)
- NoSQL → product catalog, user activity

Most modern systems use a **combination of both**.

---

## 🌍 Real-World Relevance

In production systems:

- poor schema design leads to slow queries
- missing relationships cause inconsistent data
- lack of constraints allows invalid data
- improper modeling affects scalability

Well-designed databases:

- improve performance
- reduce bugs
- support system growth
- simplify development

Database design decisions directly impact system architecture.

---

## 🧩 Practical Understanding

Scenario:

You are building an **Order Management System**.

You need to store:

- users
- orders
- products
- order items

Questions:

- How will you design relational tables?
- What relationships will you define?
- Which data could be denormalized in NoSQL?
- Where would performance matter most?

Think about trade-offs between SQL and NoSQL.

---

## ⚠️ Common Mistakes

- storing duplicate data in relational databases
- missing primary or foreign keys
- over-normalizing or under-normalizing
- not using indexes properly
- ignoring constraints
- choosing NoSQL without understanding trade-offs
- mixing SQL and NoSQL without clear purpose

---

## 🔄 Reflection Questions

- Why is normalization important in relational databases?
- When should NoSQL be preferred over SQL?
- What are the trade-offs of denormalization?
- How do indexes improve performance?
- How do database choices affect system architecture?

---

## 📚 Next Steps

- Review `resources.md`
- Complete `assignments.md`
- Try designing both SQL and NoSQL models for the same system

---

## 🧭 Navigation

← Previous: [Day 11](../day-11/README.md)

➡ Next: [Resources](./resources.md)