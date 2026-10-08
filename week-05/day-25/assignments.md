# Assignments – Day 25: API Specification & Database Schema

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

# 📌 Overview

In this assignment, learners will think like:

- backend engineers
- database engineers
- solution architects
- API designers

to transform product requirements and feature workflows into scalable APIs and database schemas.

The goal is to understand how:

```plaintext
Business Requirements
    ↓
Product Features
    ↓
User Stories
    ↓
APIs
    ↓
Database Design
```

connect together before architecture and implementation begin.

This assignment continues the same platform selected during:

- Day 21 – BRD
- Day 22 – PRD
- Day 23 – Feature Specification
- Day 24 – User Stories

---

# 🎯 Assignment Objectives

By completing this assignment, learners should be able to:

- design REST APIs
- define API request/response structures
- design relational database schemas
- design NoSQL document structures
- model entity relationships
- understand normalization and denormalization
- identify indexing strategies
- connect product workflows with backend design

---

# 🧩 Continue Your Selected Platform

Continue using the same platform selected in previous assignments.

Examples:

- Amazon / E-Commerce Platform
- Uber / Ride Booking Platform
- Netflix / Streaming Platform
- Swiggy / Food Delivery Platform
- Airbnb / Booking Platform

This continuity mirrors how real-world engineering systems evolve.

---

# 🛠 Part 1 – Feature Selection

Choose:

- 1 major feature
- 3–5 related workflows

---

## Example Features

| Platform | Example Features |
|------|------|
| Amazon | Checkout, Cart, Product Search |
| Uber | Ride Booking, Driver Matching |
| Netflix | Video Streaming, Recommendations |
| Swiggy | Order Placement, Delivery Tracking |
| Airbnb | Booking Management, Availability |

---

# 📘 Part 2 – API Design

Using the provided API Specification template:.

```plaintext
templates/api-spec/api-spec-markdown.md
templates/api-spec/api-spec-document.docx
templates/api-spec/api-spec-document.pdf
```

Your API design should include:

- endpoint names
- HTTP methods
- request payloads
- response payloads
- status codes
- validation rules
- authentication requirements

---

## Example API

### Endpoint

```plaintext
POST /api/v1/orders
```

---

### Request

```json
{
  "userId": "U1001",
  "items": [
    {
      "productId": "P100",
      "quantity": 2
    }
  ]
}
```

---

### Response

```json
{
  "orderId": "ORD-1001",
  "status": "CONFIRMED"
}
```

---

# ⚙️ Part 3 – API Workflow Diagram

Create:

- API communication flow
- request lifecycle diagram

---

## Example Workflow

```plaintext
Frontend
    ↓
Checkout API
    ↓
Payment Service
    ↓
Database
```

---

# 🔐 Part 4 – API Security Planning

Define:

- authentication mechanism
- authorization expectations
- rate limiting strategy
- validation requirements
- encryption expectations

---

## Example Questions

- Which APIs require authentication?
- Which APIs are public?
- Which workflows may require rate limiting?
- Which operations handle sensitive data?

---

# 🗄 Part 5 – SQL Database Schema Design

Using the provided SQL schema template:

```plaintext
templates/db-schema/db-schema-sql.xlsx
```

design a relational database schema.

Your schema should include:

- entities
- fields
- primary keys
- foreign keys
- relationships
- constraints
- indexing considerations

---

## Required Entities (Examples)

| Platform | Example Entities |
|------|------|
| Amazon | Users, Products, Orders, Payments |
| Uber | Riders, Drivers, Trips, Payments |
| Netflix | Users, Movies, WatchHistory |
| Swiggy | Users, Restaurants, Orders |
| Airbnb | Users, Properties, Bookings |

---

# 🔄 Part 6 – Entity Relationship Diagram (ERD)

Create:

- ER diagram
- relationship mapping

---

## Relationship Examples

| Relationship | Example |
|------|------|
| One-to-Many | User → Orders |
| Many-to-Many | Products ↔ Categories |

---

# 📄 Part 7 – NoSQL Database Design

Using the provided NoSQL schema template:

```plaintext
templates/db-schema/db-schema-nosql.xlsx
```

design a NoSQL document structure.

Your design should include:

- collections/documents
- embedded data
- denormalized structures
- query optimization thinking

---

## Example MongoDB Document

```json
{
  "orderId": "ORD-1001",
  "items": [
    {
      "productId": "P100",
      "quantity": 2
    }
  ]
}
```

---

# 📊 Part 8 – SQL vs NoSQL Comparison

Compare:

- relational schema design
- NoSQL document design

---

## Analysis Questions

1. Which data was normalized in SQL?
2. Which data was denormalized in NoSQL?
3. Which design may scale better for reads?
4. Which design provides stronger consistency?
5. Which design is easier for reporting queries?

---

# ⚡ Part 9 – Indexing & Performance Planning

Identify:

- indexed fields
- query-heavy entities
- caching opportunities
- performance bottlenecks

---

## Example

| Entity | Indexed Field | Reason |
|------|------|------|
| Users | email | Faster login |
| Orders | orderId | Faster lookup |

---

# 🧠 Part 10 – Engineering Reflection

Answer the following questions.

---

## Reflection Questions

1. Which API may receive the highest traffic?

2. Which entity may become the largest table/collection?

3. Which workflow may require asynchronous processing?

4. Which API may require stronger security protections?

5. Which database design may create scaling challenges?

6. Which APIs may eventually require versioning?

7. Which workflow may benefit from caching?

---

# 📊 Deliverables

Submit:

| Deliverable | Description |
|------|------|
| API Specification | REST API design document |
| API Workflow Diagram | Communication flow |
| SQL Database Schema | Relational schema |
| ER Diagram | Relationship mapping |
| NoSQL Design | Document database design |
| SQL vs NoSQL Analysis | Design comparison |
| Indexing Strategy | Performance considerations |
| Engineering Reflection | Answers to reflection questions |

---

# 📋 Submission Guidelines

- Use Markdown format for APIs
- Use provided schema templates for databases
- Keep API names RESTful and consistent
- Clearly define relationships
- Include realistic indexing strategies
- Avoid implementation-specific source code

---

# 📊 Evaluation Rubric

| Area | Weight |
|------|------|
| API Design Quality | 20% |
| Database Schema Design | 20% |
| SQL vs NoSQL Understanding | 15% |
| Relationship Modeling | 15% |
| Security & Scalability Thinking | 15% |
| Engineering Reflection | 15% |

---

# 🚀 Optional Challenge

Add advanced backend engineering concepts.

Examples:

- API versioning
- pagination
- event-driven architecture
- distributed caching
- read replicas
- asynchronous messaging
- idempotency handling
- CQRS thinking

Explain how these concepts may improve:

- scalability
- reliability
- maintainability
- performance

---

# 🧠 Engineering Insight

Many production engineering issues originate from:

- poor API design
- inconsistent schemas
- weak indexing strategies
- tightly coupled services
- poor scalability planning

Strong APIs and database schemas create the foundation for scalable engineering systems.

---

# 📚 Next Learning Flow

This assignment completes the Week 5 engineering planning workflow:

```plaintext
BRD
   ↓
PRD
   ↓
Feature Specification
   ↓
User Stories
   ↓
API Specification
   ↓
Database Schema
```

Week 6 will continue into:

```plaintext
High-Level Design
   ↓
Low-Level Design
   ↓
Architecture Thinking
```

This mirrors real-world engineering system planning.

---

# 🧭 Navigation

← Back to Example  
[Example](./example.md)

➡ Next Day  
[Week 6](../../week-06/README.md)