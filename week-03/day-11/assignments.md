# Assignments – Day 11: API Design Principles

> Apply professional API design practices by improving poorly designed APIs and implementing enterprise-grade standards.

---

## 📌 Overview

In real-world systems, engineers often encounter **poorly designed APIs**.

Your task is to:

- identify design issues
- refactor APIs using best practices
- enforce request validation
- standardize responses
- improve scalability and maintainability

This assignment simulates real backend engineering work.

---

## 🧠 Part 1 – Identify API Design Issues

Below is a poorly designed API for an **Order Management System**.

---

### ❌ Bad API Design

```
POST /createOrder
GET /getOrders
GET /getOrderById?id=123
POST /updateOrder
POST /deleteOrder
```

Sample Request:

```json
{
  "orderId": "",
  "user": "123",
  "amount": -500,
  "items": []
}
```

---

### Task

Identify issues in:

- endpoint naming
- HTTP method usage
- request structure
- validation gaps
- missing status codes
- lack of consistency

Write at least **8–10 problems**.

---

## 🛠 Part 2 – Redesign the API (Professional Standard)

Redesign the API using REST principles.

---

### Requirements

Design endpoints for:

- Create Order
- Get All Orders
- Get Order by ID
- Update Order
- Delete Order

---

### Expected Improvements

- Use proper HTTP methods (GET, POST, PUT, DELETE)
- Use resource-based naming
- Use path parameters instead of query misuse
- Maintain consistent structure

Example (reference only):

```
POST /orders
GET /orders
GET /orders/{order_id}
PUT /orders/{order_id}
DELETE /orders/{order_id}
```

---

## 🧩 Part 3 – Request Validation Design

Define validation rules for:

### Order Creation

Fields:

- user_id
- items (array)
- total_amount

---

### Task

Define validation rules such as:

- required fields
- correct data types
- value constraints

Example:

- total_amount must be > 0
- items array must not be empty
- user_id must be a valid identifier

---

### Add Validation Error Responses

Design structured error responses:

```json
{
  "status": "failure",
  "code": 4001,
  "message": "Validation failed",
  "errors": [
    {
      "field": "total_amount",
      "message": "Must be greater than 0"
    }
  ]
}
```

---

## 📦 Part 4 – Standardize API Responses

Design a consistent response format.

---

### Success Response

```json
{
  "status": "success",
  "code": 1000,
  "message": "Order created successfully",
  "data": {}
}
```

---

### Error Response

```json
{
  "status": "failure",
  "code": 4000,
  "message": "Invalid request",
  "data": {}
}
```

---

### Task

Ensure:

- all APIs return consistent structure
- HTTP status codes match response type
- messages are meaningful

---

## ⚙️ Part 5 – Add Advanced API Features

Enhance your API with:

---

### Pagination

```
GET /orders?page=1&limit=10
```

---

### Filtering

```
GET /orders?status=completed
```

---

### Sorting

```
GET /orders?sort=created_at
```

---

### Versioning

```
/api/v1/orders
```

---

### Task

Update your API design to include all of the above.

---

## 🔐 Part 6 – API Security Considerations

Explain how you would secure this API.

---

### Cover:

- request validation (backend)
- authentication (token-based)
- authorization (user can only access their orders)
- rate limiting
- preventing malicious input

---

## 🔄 Part 7 – Reflection

Answer briefly:

1. What were the biggest problems in the original API?
2. Why is request validation critical on backend systems?
3. How does consistency improve developer experience?
4. Why should APIs be versioned?
5. What risks exist in poorly designed APIs?

---

## 📋 Self-Evaluation Checklist

- [ ] I identified API design issues clearly
- [ ] I redesigned endpoints using REST principles
- [ ] I added proper request validation rules
- [ ] I defined structured error responses
- [ ] I implemented pagination, filtering, and versioning
- [ ] I considered security aspects

---

## 🚀 Optional Challenge (Advanced)

Take your redesigned API and:

- write OpenAPI (Swagger YAML) specification
- implement mock APIs using Postman / Bruno
- simulate API responses
- design database schema for orders

---

## 🧭 Navigation

← Back to Resources  
[Resources](./resources.md)

➡ Next: Day 12  
[Day 12](../day-12/README.md)