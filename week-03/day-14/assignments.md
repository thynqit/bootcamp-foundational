# Assignments – Day 14: Encryption & Security

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

In this module, you will:

- differentiate encoding, encryption, and hashing through hands-on practice
- experiment with real-world tools
- identify insecure implementations
- design secure data handling strategies

This assignment focuses on **practical understanding**, not memorization.

---

## 🧠 Part 1 – Encoding vs Encryption vs Hashing

---

### Task

For the following inputs:

```
HelloWorld123
Thynqit@2026
password123
```

Perform:

1. Base64 Encoding
2. Base64 Decoding
3. SHA-256 Hashing

---

### Questions

- Can Base64 be reversed? Why?
- Can hashing be reversed? Why not?
- What happens when you hash the same input twice?
- What happens when you slightly change input?

---

## 🛠 Part 2 – Hands-On Tool Exploration

Use the tools from `resources.md`.

---

### Task

Perform the following:

#### Encoding

- Encode a string using Base64
- Decode it back

---

#### Hashing

- Generate SHA-256 hash for:
  - `password123`
  - `password124`

Compare results.

---

#### Encryption

- Encrypt a message using AES tool
- Decrypt it using same key

---

### Questions

- What happens if the key is wrong?
- Why is encryption reversible but hashing is not?

---

## 🔐 Part 3 – Password Storage Design

---

### Scenario

You are building a **user login system**.

---

### Task

Answer:

1. How will you store passwords securely?
2. Will you use encoding, encryption, or hashing?
3. Which algorithm will you use (bcrypt / SHA / Argon2)?
4. Will you use salting? Why?
5. What risks exist if passwords are stored incorrectly?

---

### Output

Write a short design (5–10 lines).

---

## 🌐 Part 4 – HTTPS & Secure Communication

---

### Task

Explain the flow of HTTPS:

- client request
- server response
- key exchange
- encrypted communication

---

### Questions

- Why is asymmetric encryption used first?
- Why switch to symmetric encryption later?
- What risks exist without HTTPS?

---

## ⚠️ Part 5 – Identify Security Flaws

---

### Scenario 1

A developer stores:

```
password = "user123"
```

in database.

---

### Scenario 2

API sends:

```
Authorization: Basic dXNlcjpwYXNz
```

(Base64 encoded credentials)

---

### Scenario 3

Sensitive API runs over HTTP instead of HTTPS.

---

### Task

For each:

- what is wrong?
- what risk exists?
- how would you fix it?

---

## 🧩 Part 6 – Secure System Design

---

### Scenario

You are designing a **payment system**.

---

### Task

Define:

- how passwords are stored
- how data is transmitted
- where encryption is used
- where hashing is used
- how keys are managed

---

### Output

Create a structured answer.

---

## 🔄 Part 7 – Reflection

Answer briefly:

1. Why is encoding not considered secure?
2. Why is hashing used for passwords instead of encryption?
3. What is the biggest risk in poor key management?
4. Why is HTTPS mandatory in modern systems?
5. What is the difference between data at rest and data in transit?

---

## 📋 Self-Evaluation Checklist

- [ ] I understand encoding vs encryption vs hashing
- [ ] I performed hands-on experiments
- [ ] I understand password security
- [ ] I can explain HTTPS flow
- [ ] I can identify insecure implementations

---

## 🚀 Optional Challenge (Advanced)

Take it further:

- implement password hashing using bcrypt (Node / Java / Python)
- simulate JWT token signing and verification
- design key rotation strategy
- research a real-world data breach and analyze failure

---

## 🧭 Navigation

← Back to Resources  
[Resources](./resources.md)

➡ Next: Day 15  
[Day 15](../day-15/README.md)