# Assignments – Day 10: APIs & REST Design

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

In this assignment you will design and document a **REST API for a Product Service**.

You will design APIs for the `/products` resource and document them using **three different API documentation formats**.

This exercise simulates how engineering teams document APIs before implementation.

You will practice:

- REST API design
- API documentation
- OpenAPI / Swagger specification
- YAML syntax
- professional API documentation formats

---

# 🧠 Part 1 – Conceptual Understanding

Answer the following questions.

1. What is an API?
2. Why are APIs essential in distributed systems?
3. What makes REST APIs different from SOAP APIs?
4. Why is API versioning important?
5. Why should APIs use nouns instead of verbs in resource paths?

---

# 🧩 Part 2 – REST API Design

Design APIs for the resource:

```
/products
```

Your API must support the following operations.

| Operation | Endpoint |
|----------|----------|
| Create Product | POST /products |
| Get All Products | GET /products |
| Get Product By ID | GET /products/{product_id} |
| Update Product | PUT /products/{product_id} |
| Partially Update Product | PATCH /products/{product_id} |
| Delete Product | DELETE /products/{product_id} |

---

# 📦 Part 3 – Product Data Model

Use the following fields for the product resource.

```
id
title
description
category
price
rating
stock
createdAt
```

Example product JSON:

```json
{
  "id": "prd_101",
  "title": "Wireless Headphones",
  "description": "Noise cancelling headphones",
  "category": "electronics",
  "price": 199.99,
  "rating": 4.5,
  "stock": 50,
  "createdAt": "2026-03-15T10:00:00Z"
}
```

---

# ✍️ Part 4 – Write API Specification Using Markdown

Use the [**Markdown API specification template**](../../templates/api-spec/api-spec-markdown.md) provided in this repository.

Template file:

```
templates/api-spec/api-spec-markdown.md
```

This template demonstrates a full REST API documentation structure including:

- API overview
- authentication
- headers
- API index
- request examples
- response examples
- error handling

Example template reference: :contentReference[oaicite:4]{index=4}

---

### Your Task

Using this template:

Create the Markdown API specification to support **Product APIs**.

Update:

```
/users
```

to

```
/products
```

---

# 🧾 Part 5 – Write Swagger / OpenAPI Specification (YAML)

Use the [**Swagger/OpenAPI template**](../../templates/api-spec/api-spec-swagger.yaml) provided.

Template file:

```
templates/api-spec/api-spec-swagger.yaml
```

This specification already includes:

- OpenAPI structure
- API paths
- request schemas
- response schemas
- authentication configuration

---

### Your Task

Create the Swagger specification to support **Product APIs**.

Update:

```
/users
```

to

```
/products
```

Also update the schema definitions to represent the **Product model**.

---

# 📄 Part 6 – Write Enterprise API Document (PDF Format)

Use the [**API specification document template**](../../templates/api-spec/api-spec-document.pdf) provided.

Template file:

```
templates/api-spec/api-spec-document.pdf
```

This document demonstrates how APIs are documented in enterprise environments and includes:

- document control
- versioning
- API index
- request/response schemas
- error codes
- pagination format
- authentication details

The template currently documents **User APIs**.

---

### Your Task

Create a **Product API Specification Document** by adapting this template.

Update the following sections:

- API overview
- API index
- endpoints
- request body schema
- response body schema

Replace:

```
/users
```

with

```
/products
```

---

# 🧪 Part 7 – Explore Real APIs

Use one of the following tools:

- Postman
- Bruno
- Hoppscotch

Test APIs using:

```
https://fakestoreapi.com/products
```

Try these endpoints:

```
GET https://fakestoreapi.com/products
GET https://fakestoreapi.com/products/1
```

Observe:

- response structure
- response headers
- HTTP status codes

---

# 🔍 Part 8 – API Design Review

Review your API design and answer:

1. Are resource names consistent?
2. Did you follow REST naming conventions?
3. Did you include proper HTTP status codes?
4. Is your API versioned correctly?
5. Are request and response structures consistent?

---

# 📋 Self-Evaluation Checklist

- [ ] Designed REST API endpoints
- [ ] Defined product data model
- [ ] Documented APIs using Markdown template
- [ ] Wrote OpenAPI/Swagger YAML specification
- [ ] Adapted enterprise API documentation template
- [ ] Explored real APIs using Postman or Bruno

---

# 🚀 Optional Challenge (Advanced)

Extend the API design to include additional resources.

```
/users
/orders
/carts
```

Design REST APIs for these resources following the same documentation standards.

---

> Clear API documentation is a critical engineering skill. Well-designed APIs improve maintainability, integration, and developer experience.

---

## 🧭 Navigation

← Previous: Resources  
[Resources](./resources.md)

➡ Next Module  
[Week 3](../../week-03/README.md)