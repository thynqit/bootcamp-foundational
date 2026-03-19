# Day 14 – Encryption & Security

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

Modern software systems handle sensitive data such as:

- passwords
- payment information
- personal user data
- business-critical information

Protecting this data is a fundamental responsibility of engineers.

This module introduces:

- encoding vs encryption (a commonly misunderstood topic)
- encryption techniques used in real systems
- hashing for secure storage
- how secure communication works (HTTPS, TLS)

Understanding these concepts is essential for building **secure and trustworthy systems**.

---

## 🎯 Learning Objectives

By the end of this module, learners should be able to:

- differentiate between encoding, encryption, and hashing
- understand why encoding is not security
- explain symmetric and asymmetric encryption
- understand hashing and password security
- explain how HTTPS secures communication
- recognize real-world security practices

---

## 🧠 Core Concepts

---

### 1. Encoding vs Encryption vs Hashing

This is one of the most misunderstood areas.

| Concept | Purpose | Reversible | Use Case |
|--------|--------|-----------|----------|
| Encoding | Data representation | Yes | Data transfer |
| Encryption | Data protection | Yes (with key) | Secure communication |
| Hashing | Data integrity | No | Password storage |

---

### 2. What is Encoding?

Encoding converts data into a specific format so it can be:

- transmitted
- stored
- processed

Encoding is **not secure**.

---

### Common Encoding Methods

#### Base64 Encoding

Example:

```
Hello → SGVsbG8=
```

Used in:

- API payloads
- email attachments
- binary-to-text conversion

---

#### URL Encoding

Example:

```
space → %20
```

Used in:

- query parameters
- URLs

---

#### Character Encoding (UTF-8)

Used to represent text across systems.

---

### Key Insight

Encoding is reversible and does NOT protect data.

---

### 3. What is Encryption?

Encryption protects data by converting it into an unreadable format.

Only authorized parties with a **key** can decrypt it.

---

### 4. Types of Encryption

---

#### Symmetric Encryption

- same key used for encryption and decryption

Example:

- AES (Advanced Encryption Standard)

```
Plain Text → Encrypted → Decrypted using same key
```

Used in:

- data storage
- internal systems

---

#### Asymmetric Encryption

- uses two keys:

  - public key (encrypt)
  - private key (decrypt)

Example:

- RSA

```
Public Key → Encrypt  
Private Key → Decrypt
```

Used in:

- HTTPS
- secure key exchange

---

### 5. Hashing (Critical for Passwords)

Hashing converts data into a fixed-length value.

It is **one-way** (cannot be reversed).

---

#### Example

```
password → hashed value
```

---

### Common Hashing Algorithms

- SHA-256
- bcrypt (recommended for passwords)
- Argon2 (modern secure hashing)

---

### Key Insight

Passwords should NEVER be stored in plain text — always hashed.

---

### 6. Salting (Important Security Concept)

Salt = random value added before hashing.

```
password + salt → hashed value
```

Prevents:

- rainbow table attacks
- identical password hashes

---

### 7. How HTTPS Works (High-Level)

HTTPS secures communication using:

- TLS (Transport Layer Security)
- asymmetric + symmetric encryption

---

### Flow (Simplified)

1. Client requests server
2. Server shares public key
3. Client generates session key
4. Session key encrypted using public key
5. Secure communication begins

---

### Key Insight

- asymmetric encryption → used for key exchange  
- symmetric encryption → used for actual data transfer  

---

### 8. Data at Rest vs Data in Transit

| Type | Description |
|-----|------------|
| Data in Transit | moving across network (HTTPS) |
| Data at Rest | stored in database (encryption at rest) |

Both must be protected.

---

### 9. Common Security Practices

- always use HTTPS
- encrypt sensitive data at rest
- hash passwords with bcrypt/argon2
- never expose secrets in code
- rotate encryption keys
- validate and sanitize input

---

### 10. Common Mistakes

- using Base64 instead of encryption ❌
- storing passwords in plain text ❌
- using weak hashing (MD5, SHA1) ❌
- not using HTTPS ❌
- hardcoding API keys ❌

---

## 🌍 Real-World Relevance

In production systems:

- poor encryption → data breaches
- weak hashing → password leaks
- improper key handling → system compromise

Most major security incidents happen due to:

```plaintext
Incorrect implementation of basic security principles
```

---

## 🧩 Practical Understanding

Scenario:

You are building a **payment system**.

- user passwords must be stored
- payment data must be transmitted securely
- APIs must be protected

Questions:

- where will you use hashing?
- where will you use encryption?
- how will HTTPS help?

---

## 🔄 Reflection Questions

- Why is encoding not secure?
- Why must passwords be hashed instead of encrypted?
- Why is symmetric encryption faster?
- Why is asymmetric encryption used in HTTPS?
- What risks exist if HTTPS is not used?

---

## 📚 Next Steps

- Review `resources.md`
- Complete `assignments.md`
- Explore real-world encryption implementations

---

## 🧭 Navigation

← Previous: [Day 13](../day-13/README.md)

➡ Next: [Resources](./resources.md)