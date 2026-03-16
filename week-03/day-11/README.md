# Day 11 – API Design Principles

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

APIs define how software systems communicate with each other.

A well-designed API is **consistent, predictable, secure, and easy to use**. Poorly designed APIs, on the other hand, create confusion, increase development time, and introduce security risks.

In modern backend systems, APIs must be designed carefully to support:

- scalability
- maintainability
- backward compatibility
- security
- developer usability

This module explores **professional API design principles used by engineering teams** and introduces best practices that ensure APIs remain reliable as systems evolve.

---

## 🎯 Learning Objectives

By the end of this module, learners should be able to:

- Apply REST API design best practices
- Use consistent naming conventions for resources
- Understand API versioning strategies
- Implement pagination and filtering for scalable APIs
- Handle errors using standardized response formats
- Understand idempotent API operations
- Validate incoming API requests securely
- Design APIs that are predictable and maintainable

---

## 🧠 Core Concepts

### 1. Resource-Oriented API Design

REST APIs should represent **resources**, not actions.

Good API design uses **nouns instead of verbs**.

Good examples:

```
GET /users
GET /orders
POST /products
```

Bad examples:

```
GET /getUsers
POST /createOrder
```

Resources should represent entities within the system.

Examples:

```
/users
/products
/orders
/carts
```

This approach makes APIs intuitive and consistent.

---

### 2. Consistent Naming Conventions

Consistency is one of the most important API design principles.

Use predictable naming patterns.

Examples:

```
/users
/users/{user_id}
/orders
/orders/{order_id}
/products
/products/{product_id}
```

Recommended conventions:

- use **plural nouns**
- use **lowercase**
- use **hyphen-separated names**

Example:

```
/user-orders
/payment-transactions
```

Avoid mixing naming styles.

---

### 3. API Versioning

APIs evolve over time.

Without versioning, updates can break existing clients.

Example:

```
/api/v1/users
/api/v2/users
```

Versioning allows systems to introduce improvements while maintaining compatibility.

Common versioning approaches:

- URL versioning (`/v1`)
- header-based versioning
- query parameter versioning

Most systems use **URL versioning** for simplicity.

---

### 4. Pagination, Filtering, and Sorting

APIs should avoid returning extremely large datasets.

Instead, APIs should support **pagination**.

Example:

```
GET /products?page=1&limit=20
```

Typical response:

```json
{
  "page": 1,
  "limit": 20,
  "total": 150,
  "data": [...]
}
```

Filtering example:

```
GET /products?category=electronics
```

Sorting example:

```
GET /products?sort=price
```

These features improve performance and scalability.

---

### 5. Standardized Error Handling

APIs should return **clear and consistent error responses**.

Example error response:

```json
{
  "status": "failure",
  "code": 4001,
  "message": "Invalid email format.",
  "data": {}
}
```

Benefits of standardized error responses:

- easier debugging
- better developer experience
- predictable client-side handling

Common HTTP status codes:

```
200 OK
201 Created
400 Bad Request
401 Unauthorized
404 Not Found
500 Internal Server Error
```

---

### 6. Idempotent API Operations

Idempotent operations produce the **same result even if executed multiple times**.

Examples:

```
GET /users
DELETE /users/{id}
PUT /users/{id}
```

Calling these multiple times does not change the final state.

Non-idempotent example:

```
POST /orders
```

Calling POST multiple times could create multiple resources.

Understanding idempotency helps build **reliable distributed systems**.

---

### 7. Request Validation (Critical Backend Responsibility)

A common misconception is:

> "The frontend already validates the request, so backend validation is unnecessary."

This assumption is **dangerous and incorrect**.

Clients can include:

- web browsers
- mobile apps
- third-party integrations
- automated scripts
- malicious actors

Because of this, **backend systems must always validate incoming requests**.

Backend validation should verify:

- required fields exist
- data types are correct
- value ranges are valid
- formats are correct (email, phone, etc.)
- unauthorized data is not accepted

Example validation checks:

```
price must be a positive number
email must be a valid format
required fields cannot be empty
```

Without proper validation, systems become vulnerable to:

- corrupted data
- security vulnerabilities
- application crashes

Backend validation is a **fundamental security and reliability practice**.

---

### 8. API Consistency

APIs should follow consistent patterns across the entire system.

Example consistency:

```
GET /users
GET /users/{id}

GET /products
GET /products/{id}
```

Response structures should also be consistent:

```json
{
  "status": "success",
  "code": 1001,
  "message": "Operation successful",
  "data": {...}
}
```

Consistency improves **developer experience and system maintainability**.

---

## 🌍 Real-World Relevance

In real production systems, poorly designed APIs cause:

- integration failures
- inconsistent behavior
- difficult debugging
- security vulnerabilities

Well-designed APIs:

- reduce development time
- simplify integrations
- improve maintainability
- enable system scalability

Large technology companies invest heavily in **API design standards** to maintain platform stability.

---

## 🧩 Practical Understanding

Scenario:

You are building APIs for an **E-commerce Platform**.

Endpoints might include:

```
GET /products
POST /products
GET /orders
POST /orders
GET /users/{id}
```

Questions to consider:

- Are the resource names consistent?
- Are responses structured consistently?
- Are requests validated before processing?
- Are errors returned in a standard format?

Good API design ensures that **new developers can understand the system quickly**.

---

## ⚠️ Common Mistakes

- Using verbs instead of nouns in endpoints
- Inconsistent response formats
- Returning excessive data without pagination
- Not versioning APIs
- Ignoring backend validation of request parameters
- Returning unclear error messages
- Mixing naming conventions across endpoints

---

## 🔄 Reflection Questions

- Why should APIs represent resources rather than actions?
- What problems occur when APIs are not versioned?
- Why is pagination necessary for scalable APIs?
- Why must backend systems validate requests even if clients perform validation?
- How does API consistency improve developer experience?

---

## 📚 Next Steps

- Review `resources.md`
- Complete `assignments.md`
- Examine API documentation from real platforms such as GitHub, Stripe, or AWS

---

## 🧭 Navigation

← **Previous Module**  
[Week 3](../README.md)

➡ **Next: Resources**  
[Resources](./resources.md)