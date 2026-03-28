# Assignments – Day 16: Cloud Fundamentals

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

In this assignment, you will:

- map real-world systems to cloud infrastructure
- identify core cloud components
- design scalable and reliable systems
- think about failures and security
- get hands-on exposure to real cloud platforms

This assignment focuses on **system thinking and architecture**, not cloud UI usage.

---

# 🧠 Part 1 – Conceptual Understanding

Answer briefly:

1. What problem does cloud computing solve compared to on-premise systems?
2. What is the difference between IaaS, PaaS, and SaaS (with examples)?
3. Why is horizontal scaling preferred over vertical scaling in modern systems?
4. What is the role of a load balancer?
5. Why is IAM critical in cloud environments?

---

# 🧩 Part 2 – System Architecture Design

---

## Scenario: E-Commerce Platform

Design a high-level architecture for:

```
An e-commerce platform (like Amazon / Flipkart)
```

---

### Tasks

1. Draw a diagram including:

- Users
- CDN
- Load Balancer
- API Gateway
- Application Servers
- Database
- Storage

---

2. Explain:

- where each component sits
- how requests flow through the system
- how static and dynamic content are handled

---

### Expected Output

- Architecture diagram (hand-drawn / digital)
- Written explanation (clear and structured)

---

# 🔍 Part 3 – Identify Cloud Components

---

## Scenario

You are given a system:

```
Users → Internet → ??? → Servers → Database
```

---

### Tasks

1. Fill missing components:

- Where does CDN go?
- Where does Load Balancer go?
- Where does API Gateway go?

---

2. Explain:

- why each component is placed there
- what problem it solves

---

# 📈 Part 4 – Scaling Scenario

---

## Scenario

Your application traffic increases **10x overnight**.

---

### Tasks

1. What will break first?

- server?
- database?
- network?

---

2. What should you scale?

- vertically or horizontally?

---

3. Where does load balancing help?

---

4. How would you redesign your system?

---

# ⚠️ Part 5 – Failure & High Availability

---

## Scenario

One of your application servers crashes.

---

### Tasks

1. What happens to user requests?

2. How does a load balancer help?

3. How can you design system to avoid downtime?

4. What is the role of multiple availability zones?

---

# 🔐 Part 6 – Security Thinking

---

## Scenario

Your system is exposed to:

- unauthorized API access
- DDoS attack
- data leakage risk

---

### Tasks

1. Where would you use:

- IAM
- Firewall
- API Gateway protections

---

2. What risks exist if:

- no IAM is implemented?
- no firewall is used?

---

# 🌐 Part 7 – Cloud Provider Mapping

---

### Task

Map the following components to AWS, Azure, and GCP:

| Component | AWS | Azure | GCP |
|----------|-----|------|-----|
| Virtual Machine | ? | ? | ? |
| Object Storage | ? | ? | ? |
| Managed Database | ? | ? | ? |
| Load Balancer | ? | ? | ? |

---

### Goal

Understand that:

```
Concepts are same, naming differs
```

---

# 🧩 Part 8 – Real-World Thinking

---

### Scenario

You built an API in Week 3.

---

### Tasks

Answer:

1. Where does your API run in the cloud?
2. Where is your database hosted?
3. How does a user request reach your backend?
4. How would your system handle 1 million users?

---

# ☁️ Part 9 – Hands-On Cloud (Free Tier)

---

## Objective

Get basic exposure to real cloud platforms.

---

### Step 1 – Create Free Accounts

- AWS Free Tier  
- Azure Free Account  
- Google Cloud Free Tier  

---

### Step 2 – Perform Basic Setup (Choose ANY ONE platform or try all)

---

#### 🔹 Compute

- Launch a virtual machine (VM)
- Connect using SSH / browser-based terminal

---

#### 🔹 Storage

- Create object storage bucket
- Upload a file
- Access it via URL

---

#### 🔹 Database

- Create a managed database instance
- Understand:
  - connection string
  - access configuration

---

### Step 3 – Observe

- What configurations are required?
- What security settings are enforced?
- How does cloud abstract infrastructure?

---

## ⚠️ Important Notes

- Stay within free tier limits
- Do not expose sensitive data
- Delete unused resources

---

# 🔄 Part 10 – Reflection

Answer briefly:

1. How does cloud simplify infrastructure management?
2. What is the most important component in your architecture?
3. What happens if scaling is not handled properly?
4. Why is security critical in cloud systems?
5. What surprised you during hands-on cloud usage?

---

# 📋 Self-Evaluation Checklist

- [ ] I designed a system architecture diagram
- [ ] I understand request flow in cloud systems
- [ ] I can explain scaling and load balancing
- [ ] I understand failure handling
- [ ] I understand IAM and security basics
- [ ] I explored at least one cloud platform

---

# 🚀 Optional Challenge (Advanced)

Design a high-level architecture for:

- Ride Booking System (Uber)
- Video Streaming Platform (Netflix)

Include:

- CDN
- scaling strategy
- high availability
- global users

---

## 🧭 Navigation

← Back to Resources  
[Resources](./resources.md)

➡ Next: Day 17 – DevOps & CI/CD  
[Day 17](../day-17/README.md)