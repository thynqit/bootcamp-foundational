# Resources – Day 14: Encryption & Security

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

These resources help you understand how data is secured in modern systems.

They cover:

- encoding and decoding techniques
- encryption mechanisms (symmetric & asymmetric)
- hashing and password security
- HTTPS and secure communication
- real-world security practices

Hands-on tools are included to experiment with encoding, hashing, and encryption.

---

## 📖 Official Documentation & Authoritative Sources

---

### Cloudflare – What is Encryption?

https://www.cloudflare.com/learning/ssl/what-is-encryption/

Explains:

- encryption fundamentals
- symmetric vs asymmetric encryption
- real-world usage in HTTPS

---

### Cloudflare – What is SSL/TLS?

https://www.cloudflare.com/learning/ssl/what-is-ssl/

Covers:

- HTTPS communication
- TLS handshake basics
- secure data transfer

---

### OWASP – Cryptographic Storage Cheat Sheet

https://cheatsheetseries.owasp.org/cheatsheets/Cryptographic_Storage_Cheat_Sheet.html

Covers:

- how to store sensitive data securely
- encryption best practices
- common mistakes

---

## 🎓 Structured Learning Material

---

### Auth0 – Encoding vs Encryption vs Hashing

https://auth0.com/blog/encoding-encryption-hashing/

Explains:

- difference between encoding, hashing and encryption
- when to use each
- password security concepts

---

### IBM – What is Encryption?

https://www.ibm.com/topics/encryption

Covers:

- encryption algorithms
- key management
- enterprise use cases

---

### GeeksforGeeks – Symmetric vs Asymmetric Encryption

https://www.geeksforgeeks.org/difference-between-symmetric-and-asymmetric-key-encryption/

Provides:

- clear comparison
- examples of algorithms
- practical understanding

---

## 🛠 Hands-On Tools (Highly Recommended)

Experiment with these tools to build intuition.

---

### 🔐 Base64 Encode/Decode Tool

https://www.base64encode.org/

Use this to:

- encode text → Base64
- decode Base64 → original text

👉 Helps understand why encoding is reversible.

---

### 🔑 Hash Generator (SHA / bcrypt examples)

https://emn178.github.io/online-tools/sha256.html

Use this to:

- generate hashes
- see how same input produces same output
- experiment with small changes

👉 Observe avalanche effect (small change → big hash difference)

---

### 🔐 JWT Decoder / Encoder

https://jwt.io/

Use this to:

- decode JWT tokens
- inspect header, payload, signature
- understand token structure

---

### 🔒 Encryption Playground

https://www.devglan.com/online-tools/aes-encryption-decryption

Use this to:

- encrypt text using AES
- decrypt using same key

👉 Demonstrates symmetric encryption.

---

### 🌐 URL Encoding Tool

https://www.urlencoder.io/

Use this to:

- encode URL parameters
- decode encoded values

---

## 🎥 Recommended Videos

---

### Encryption vs Hashing vs Encoding

https://www.youtube.com/watch?v=rU61yA7E5zA

Explains:

- differences clearly
- real-world examples

---

### Types of Cryptography Algorithms

https://www.youtube.com/watch?v=xzrtPbSBI1w

Covers:

- understanding cryptography and crypto system 
- cryptographic algorithms
- key terms 

---

### Symmetric vs Asymmetric Encryption

https://www.youtube.com/watch?v=AQDCe585Lnc

Explains:

- key differences
- use cases
- practical intuition

---

## 📌 Suggested Learning Flow

1. Start with Cloudflare encryption basics.
2. Understand hashing vs encryption (Auth0).
3. Explore symmetric vs asymmetric encryption.
4. Use tools to:
   - encode/decode data
   - generate hashes
   - encrypt/decrypt content
5. Reflect on real-world use cases.

---

## ⚠️ Key Takeaways While Practicing

- Encoding is reversible → not secure
- Encryption requires keys → secure communication
- Hashing is one-way → used for passwords
- Small input changes → large hash differences
- Keys must be protected, not hardcoded

---

## 🧭 Navigation

← Back to Lesson  
[Day 14](./README.md)

➡ Next: Assignments  
[Assignments](./assignments.md)