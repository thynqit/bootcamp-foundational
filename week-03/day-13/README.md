# Day 13 – Authentication & Authorization

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

Modern software systems must ensure that:

1. **Users are who they claim to be** (Authentication)
2. **Users can only access what they are allowed to** (Authorization)

Without proper authentication and authorization:

- sensitive data can be exposed
- systems can be compromised
- unauthorized actions can be performed

This module introduces **industry-standard mechanisms** used to secure applications, including:

- authentication methods
- authorization models
- token-based security
- enterprise identity systems

These concepts are foundational for building **secure backend systems and APIs**.

---

## 🎯 Learning Objectives

By the end of this module, learners should be able to:

- Explain authentication and authorization clearly
- Differentiate between authentication and authorization
- Understand session-based and token-based authentication
- Explain JWT and token-based security
- Understand RBAC (Role-Based Access Control)
- Explain MFA (Multi-Factor Authentication)
- Understand OAuth and SAML
- Recognize how APIs enforce security

---

## 🧠 Core Concepts

### 1. What is Authentication?

Authentication verifies **who the user is**.

Example:

- logging in with email and password
- entering OTP
- biometric authentication

If authentication fails → user is denied access.

---

### 2. What is Authorization?

Authorization determines **what the user can do**.

Example:

- admin can delete users
- normal user cannot
- user can only access their own data

Authorization happens **after authentication**.

---

### 3. Authentication vs Authorization

| Aspect | Authentication | Authorization |
|-------|---------------|--------------|
| Purpose | Verify identity | Grant permissions |
| Question | Who are you? | What can you do? |
| Happens When | Before access | After authentication |

---

### 4. Session-Based Authentication

Traditional approach:

- user logs in
- server creates a session
- session ID stored in cookie

Flow:

```
Client → Login → Server
Server → Creates Session → Returns Session ID
Client → Sends Session ID on each request
```

Used in:

- traditional web applications

---

### 5. Token-Based Authentication (JWT)

Modern systems use **tokens instead of sessions**.

Example:

```
Authorization: Bearer <token>
```

JWT (JSON Web Token) contains:

- user identity
- permissions
- expiry

Advantages:

- stateless
- scalable
- suitable for APIs

---

### 6. Role-Based Access Control (RBAC)

Access is controlled based on roles.

Example:

| Role | Permissions |
|-----|------------|
| Admin | Full access |
| User | Limited access |

Example logic:

```
if (role == "admin") → allow delete
```

RBAC simplifies permission management.

---

### 7. Multi-Factor Authentication (MFA)

MFA requires multiple verification methods:

- password (something you know)
- OTP / phone (something you have)
- biometric (something you are)

Example:

```
Login → Password → OTP → Access granted
```

MFA significantly improves security.

---

### 8. OAuth (Authorization Framework)

OAuth allows users to **grant access without sharing passwords**.

Example:

```
Login with Google
Login with GitHub
```

Flow:

- user logs in via provider
- provider returns access token
- application uses token to access data

OAuth is widely used in modern applications.

---

### 9. SAML (Enterprise Authentication)

SAML is used in **enterprise SSO systems**.

Example:

- logging into multiple company apps with one login

Flow:

```
User → Identity Provider (IdP)
IdP → Authentication
IdP → Sends assertion to application
```

Used in:

- corporate environments
- enterprise platforms

---

### 10. Access Tokens vs Refresh Tokens

Access Token:

- short-lived
- used for API calls

Refresh Token:

- long-lived
- used to generate new access tokens

This improves security by limiting token exposure.

---

### 11. API Security

APIs must enforce:

- authentication (who is calling)
- authorization (what they can access)

Example:

```
GET /orders/{id}
```

Backend must verify:

- user is authenticated
- user owns the order

---

### 12. Common Security Practices

- never trust client-side validation
- always validate tokens on backend
- use HTTPS for all communication
- implement token expiration
- restrict access based on roles

---

## 🌍 Real-World Relevance

In production systems:

- weak authentication leads to account takeover
- poor authorization leads to data leaks
- missing validation leads to security vulnerabilities

Modern systems use:

- JWT for APIs
- OAuth for third-party access
- SAML for enterprise SSO
- MFA for additional protection

Security is a core responsibility of backend engineers.

---

## 🧩 Practical Understanding

Scenario:

You are building an **E-commerce Platform**.

Requirements:

- users must log in
- users can view only their orders
- admins can manage products
- payments require additional verification

Questions:

- how will you authenticate users?
- how will you restrict access?
- where will you use roles?

---

## ⚠️ Common Mistakes

- confusing authentication with authorization
- trusting frontend validation
- storing sensitive data insecurely
- not expiring tokens
- giving excessive permissions
- not implementing MFA

---

## 🔄 Reflection Questions

- Why must authentication happen before authorization?
- What risks exist without proper authorization?
- Why are tokens preferred over sessions in APIs?
- How does MFA improve security?
- When should OAuth be used?

---

## 📚 Next Steps

- Review `resources.md`
- Complete `assignments.md`
- Explore real-world authentication flows

---

## 🧭 Navigation

← Previous: [Day 12](../day-12/README.md)

➡ Next: [Resources](./resources.md)