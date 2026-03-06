# Thynqit Labs – Foundational Engineering Bootcamp

![Curriculum](https://img.shields.io/badge/Curriculum-Engineering-blue)
![Level](https://img.shields.io/badge/Level-Foundational-green)
![License](https://img.shields.io/badge/License-MIT-orange)
![Maintained](https://img.shields.io/badge/Maintained-Active-success)
![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen)

A structured, comprehensive foundational engineering curriculum curated by **Thynqit Labs**. It is designed to help software engineers understand modern software development, cloud systems, security practices, and scalable architecture.

This repository acts as a **step-by-step engineering handbook** that learners can follow sequentially.

It is suitable for:

- Software Developers
- QA Engineers
- DevOps Engineers
- Engineering Students
- Early-career Professionals
- Anyone transitioning into software engineering

---

# 📑 Table of Contents

- Overview
- Quick Navigation
- Learning Goals
- Curriculum Navigation Map
- Bootcamp Structure
- Curriculum Roadmap
- System Design Use Case
- Expected Learning Outcomes
- Repository Structure
- CLI Philosophy
- Contribution Guide
- License

---

# 📘 Overview

Modern software engineering requires more than programming knowledge.

Engineers must understand:

- Security awareness
- Software delivery processes
- Agile collaboration
- Version control
- APIs and backend systems
- Cloud infrastructure
- Linux command-line environments
- System design
- Architecture documentation

This curriculum introduces these topics progressively to build **real-world engineering intuition**.

---

# 🧭 Quick Navigation

Start your learning journey here:

- **Begin Learning → [Week 1 – Security & Software Delivery](./week-01-security-software-delivery)**
- **Explore System Design → [Week 5 – System Design](./week-05-system-design)**
- **Architecture Documentation → [Week 6 – Engineering Documentation](./week-06-engineering-documentation)**

---

# 🎯 Learning Goals

By completing this bootcamp, learners will:

- Understand modern software delivery workflows
- Build a security-first engineering mindset
- Use Git professionally
- Design APIs and databases
- Understand cloud infrastructure basics
- Learn Linux command-line fundamentals
- Understand scalable system design
- Produce professional engineering documentation
- Communicate architecture clearly

---

# 🗺 Curriculum Navigation Map

The program follows a progressive engineering learning path:

```mermaid
flowchart TD
    A[Cybersecurity Awareness]
    B[Software Development Lifecycle]
    C[Agile & Scrum]
    D[User Stories & Project Tracking]
    E["Version Control (Git)"]
    F[Web Fundamentals]
    G[API Design]
    H[Backend Engineering]
    I[Cloud Infrastructure]
    J[Linux CLI]
    K[System Design]
    L[Engineering Documentation]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    H --> I
    I --> J
    J --> K
    K --> L
```

Each step builds upon the previous concept.

---

# 📚 Bootcamp Structure

The curriculum follows a **5-day work week learning structure**.

```
Week
 ├── Day 01
 │    ├── README.md
 │    ├── resources.md
 │    └── assignments.md
```

Each day contains:

- Concept explanations
- Curated learning resources
- Hands-on exercises
- Reflection questions

---

# 🛣 Curriculum Roadmap

## Week 1 – Security & Software Delivery Foundations
[Open Week 1](./week-01-security-software-delivery)

| Day | Topic |
|----|------|
| Day 1 | [Cybersecurity Fundamentals](./week-01-security-software-delivery/day-01-cybersecurity) |
| Day 2 | [Software Development Lifecycle](./week-01-security-software-delivery/day-02-sdlc) |
| Day 3 | [Agile & Scrum](./week-01-security-software-delivery/day-03-agile-scrum) |
| Day 4 | [User Stories & Project Tracking](./week-01-security-software-delivery/day-04-user-stories-project-tracking) |
| Day 5 | [Git Basics](./week-01-security-software-delivery/day-05-git-basics) |

---

## Week 2 – Git Collaboration & Web Fundamentals
[Open Week 2](./week-02-web-git-collaboration)

| Day | Topic |
|----|------|
| Day 6 | [Git Branching & Code Review](./week-02-web-git-collaboration/day-06-git-advanced-code-review) |
| Day 7 | [How the Web Works](./week-02-web-git-collaboration/day-07-how-the-web-works) |
| Day 8 | [HTTP Fundamentals](./week-02-web-git-collaboration/day-08-http-fundamentals) |
| Day 9 | [APIs & REST Design](./week-02-web-git-collaboration/day-09-api-design) |
| Day 10 | [Data Formats](./week-02-web-git-collaboration/day-10-data-formats) |

---

## Week 3 – Backend Engineering Foundations
[Open Week 3](./week-03-backend-foundations)

| Day | Topic |
|----|------|
| Day 11 | [API Design Principles](./week-03-backend-foundations/day-11-api-design) |
| Day 12 | [Database Design Fundamentals](./week-03-backend-foundations/day-12-database-design) |
| Day 13 | [Authentication & Authorization](./week-03-backend-foundations/day-13-auth-auth) |
| Day 14 | [Encryption & Security](./week-03-backend-foundations/day-14-encryption-security) |
| Day 15 | [Testing Fundamentals](./week-03-backend-foundations/day-15-testing) |

---

## Week 4 – Cloud & Infrastructure
[Open Week 4](./week-04-cloud-infrastructure)

| Day | Topic |
|----|------|
| Day 16 | [Cloud Fundamentals](./week-04-cloud-infrastructure/day-16-cloud-basics) |
| Day 17 | [DevOps & CI/CD](./week-04-cloud-infrastructure/day-17-devops-cicd) |
| Day 18 | [Logging & Monitoring](./week-04-cloud-infrastructure/day-18-observability) |
| Day 19 | [Networking Basics](./week-04-cloud-infrastructure/day-19-networking) |
| Day 20 | [Linux CLI for Engineers](./week-04-cloud-infrastructure/day-20-linux-cli) |

---

## Week 5 – System Design
[Open Week 5](./week-05-system-design)

| Day | Topic |
|----|------|
| Day 21 | [System Design Basics](./week-05-system-design/day-21-system-design) |
| Day 22 | [Monolith Architecture](./week-05-system-design/day-22-monolith) |
| Day 23 | [Microservices Architecture](./week-05-system-design/day-23-microservices) |
| Day 24 | [Scalability Concepts](./week-05-system-design/day-24-scalability) |
| Day 25 | [Performance & Reliability](./week-05-system-design/day-25-performance) |

---

## Week 6 – Engineering Documentation
[Open Week 6](./week-06-engineering-documentation)

| Day | Topic |
|----|------|
| Day 26 | [Business Requirement Document](./week-06-engineering-documentation/day-26-brd) |
| Day 27 | [Product Requirement Document](./week-06-engineering-documentation/day-27-prd) |
| Day 28 | [Feature Specification](./week-06-engineering-documentation/day-28-feature-spec) |
| Day 29 | [API Specification & DB Schema](./week-06-engineering-documentation/day-29-api-db) |
| Day 30 | [Architecture Documentation](./week-06-engineering-documentation/day-30-architecture-docs) |

---

# 🧱 System Design Use Case

Throughout the curriculum we will design a simplified **e-commerce platform inspired by Target.com**.

Learners will progressively build:

- Business Requirement Document (BRD)
- Product Requirement Document (PRD)
- Scope definition
- Feature specification
- User stories
- API design
- Database schema
- Architecture diagrams
- Monolith vs Microservices comparison

This teaches **end-to-end system thinking** rather than isolated concepts.

---

# 🏆 Expected Learning Outcomes

By completing this curriculum, learners will produce:

- Engineering architecture documentation
- API specifications
- Database schema designs
- System architecture diagrams
- Production-grade engineering workflows
- Scalable system design thinking

---

# 📂 Repository Structure

```
bootcamp-foundational
│
├── templates
│
├── week-01-security-software-delivery
├── week-02-web-git-collaboration
├── week-03-backend-foundations
├── week-04-cloud-infrastructure
├── week-05-system-design
└── week-06-engineering-documentation
```

---

# 💻 CLI Philosophy

Modern engineering environments frequently operate without graphical interfaces.

Engineers must be comfortable with:

- Git CLI
- Linux CLI
- Cloud terminal environments

Understanding CLI tools improves debugging ability and operational confidence.

---

# 🧭 How to Use This Repository

1. Follow modules sequentially.
2. Complete exercises before progressing.
3. Take notes and build small practical examples.
4. Discuss concepts with peers or mentors.
5. Revisit sections when working on real systems.

---

# 🌍 About Thynqit Labs

Thynqit Labs is an engineering-focused technology company building scalable mobile, web, cloud, and SaaS platforms.

We believe strong fundamentals create strong systems.

---

# 🤝 Contribution Guide

Contributions are welcome.

You can help by:

- Improving explanations
- Adding better learning resources
- Suggesting exercises
- Fixing documentation issues

Please open a Pull Request.

---

# 📜 License

This project is licensed under the **MIT License**.

You are free to use, modify, and distribute this curriculum with attribution.

See the `LICENSE` file for full license details.