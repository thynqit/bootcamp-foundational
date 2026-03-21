# Assignments – Day 13: Authentication & Authorization

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

Authentication and authorization are critical for securing modern applications.

In this assignment, you will design a **complete authentication and authorization system** for a real-world platform.

You will apply concepts such as:

- login systems
- token-based authentication (JWT)
- role-based access control (RBAC)
- API-level security
- OAuth-based login

This assignment simulates how backend engineers design secure systems.

---

## 🧠 Part 1 – System Definition

Choose one platform:

- E-commerce Platform (Amazon / BestBuy)
- Ride Booking Platform (Uber)

---

### Task

Define:

- types of users (customer, admin, driver, etc.)
- roles in the system
- high-level permissions

---

### Example

| Role | Permissions |
|------|------------|
| Admin | Full access |
| User | View and place orders |
| Driver | Accept and complete rides |

---

## 🔐 Part 2 – Authentication Design

Design how users will authenticate.

---

### Cover:

- login method (email/password, OTP, social login)
- password storage (hashing)
- session vs token-based approach
- token expiration strategy

---

### Task

Answer:

- What authentication method will you use?
- Will you use JWT or sessions? Why?
- How will you store user credentials securely?

---

## 🔑 Part 3 – JWT-Based Authentication Flow

Design a JWT-based authentication system.

---

### Include:

1. User login flow
2. Token generation
3. Token validation on each API request
4. Token expiration handling

---

### Example Header

```
Authorization: Bearer <JWT>
```

---

### Task

Draw or describe the full flow:

```
Client → Login → Server → JWT → Client → API Requests
```

Explain each step clearly.

---

## 🧩 Part 4 – Authorization (RBAC)

Define role-based access control.

---

### Task

Create:

- roles (admin, user, etc.)
- permissions per role
- API access rules

---

### Example

```
GET /orders → user can access own orders
DELETE /users → only admin allowed
```

---

### Output

Create a table mapping:

| API | Role | Access |
|-----|------|--------|

---

## 🔐 Part 5 – API Security Enforcement

Design how backend will enforce security.

---

### Cover:

- validating JWT tokens
- checking user roles
- restricting access to own data
- handling unauthorized access

---

### Example

```
User A cannot access User B’s order
```

---

## 🔒 Part 6 – Multi-Factor Authentication (MFA)

Add an additional security layer.

---

### Task

Define:

- when MFA is required (login, payments, etc.)
- type of MFA (OTP, authenticator app)
- user flow

---

## 🌐 Part 7 – OAuth Integration

Design social login using OAuth.

---

### Example:

```
Login with Google
Login with GitHub
```

---

### Task

Explain:

- how OAuth flow works
- what tokens are exchanged
- why passwords are not shared

---

## ⚙️ Part 8 – Security Best Practices

List at least 8 best practices.

---

### Examples

- never store passwords in plain text
- use HTTPS
- validate tokens on every request
- implement token expiration
- use least privilege access

---

## 🔄 Part 9 – Reflection

Answer briefly:

1. Why is JWT preferred for APIs?
2. What risks exist without proper authorization?
3. How does RBAC simplify permission management?
4. Why is MFA important for sensitive operations?
5. What problems does OAuth solve?

---

## 📋 Self-Evaluation Checklist

- [ ] I designed a complete authentication system
- [ ] I defined roles and permissions
- [ ] I implemented JWT flow conceptually
- [ ] I designed RBAC access rules
- [ ] I included MFA and OAuth
- [ ] I considered security best practices

---

## 🚀 Optional Challenge (Advanced)

Take your design further:

- design refresh token flow
- define token expiration strategy
- simulate API middleware for authentication
- design database schema for auth system

---

## 🧭 Navigation

← Back to Resources  
[Resources](./resources.md)

➡ Next: Day 14  
[Day 14](../day-14/README.md)