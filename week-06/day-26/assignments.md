# Assignments – Day 26: System Design Basics

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

# 📌 Overview

In this assignment, learners will think like:

- system designers
- backend engineers
- solution architects
- platform engineers

to transform product requirements into foundational system architecture.

The goal is to understand how:

```plaintext
Business Requirements
    ↓
APIs & Databases
    ↓
System Components
    ↓
Architecture Design
```

connect together before detailed architecture implementation begins.

This assignment continues the same platform selected during:

- Day 21 – BRD
- Day 22 – PRD
- Day 23 – Feature Specification
- Day 24 – User Stories
- Day 25 – APIs & Database Design

---

# 🎯 Assignment Objectives

By completing this assignment, learners should be able to:

- identify core system components
- design high-level architectures
- visualize request lifecycle
- identify scalability considerations
- identify reliability considerations
- explain architecture trade-offs
- connect non-functional requirements with system design decisions

---

# 🧩 Continue Your Selected Platform

Continue using the same platform selected in previous assignments.

Examples:

- Amazon / E-Commerce Platform
- Uber / Ride Booking Platform
- Netflix / Streaming Platform
- Swiggy / Food Delivery Platform
- Airbnb / Booking Platform

This continuity mirrors how real-world engineering systems evolve from requirements into architecture.

---

# 🛠 Part 1 – System Requirement Analysis

Review your previously created:

- PRD
- Feature Specification
- APIs
- Database Schema

Identify:

- critical workflows
- high-traffic operations
- latency-sensitive operations
- reliability-sensitive workflows

---

## Example Questions

- Which APIs may receive the highest traffic?
- Which workflows require low latency?
- Which operations cannot tolerate downtime?
- Which workflows involve background processing?

---

# 🧱 Part 2 – Identify Core System Components

Design a foundational architecture for your platform.

Your system should include:

| Required Component | Purpose |
|------|------|
| Frontend Application | User interaction |
| Backend/API Layer | Business logic |
| Database | Persistent storage |
| Cache | Faster data retrieval |
| Load Balancer | Traffic distribution |
| CDN | Static asset delivery |
| Storage System | Images/files/videos |
| Queue System | Async processing |

---

# 📄 Part 3 – High-Level Architecture Diagram

Create a complete high-level architecture diagram.

---

## Diagram Requirements

Your diagram should visualize:

- user flow
- frontend
- APIs/services
- database
- cache
- CDN
- queues
- storage systems

---

## Example Flow

```plaintext
Users
    ↓
CDN
    ↓
Load Balancer
    ↓
API Layer
    ↓
Database
```

---

# 🔄 Part 4 – Request Lifecycle Design

Choose ONE important workflow from your platform.

Examples:

- product search
- ride booking
- checkout
- order tracking
- video streaming

Document:

- request flow
- backend interactions
- cache usage
- database access
- async processing

---

## Deliverables

Include:

- request lifecycle explanation
- request flow diagram
- performance optimization ideas

---

# ⚡ Part 5 – Caching Strategy

Identify:

- cacheable data
- high-read operations
- potential cache invalidation challenges

---

## Example Questions

- Which APIs may benefit from caching?
- Which data changes frequently?
- Which workflows require real-time data?

---

# 🌍 Part 6 – CDN & Static Content Planning

Identify:

- static assets
- global delivery needs
- media-heavy workflows

---

## Example Assets

- product images
- videos
- CSS
- JavaScript

---

# 📬 Part 7 – Queue & Background Processing

Identify operations that should be asynchronous.

Examples:

- email notifications
- analytics processing
- payment retries
- recommendation generation

---

## Deliverables

Include:

- async workflows
- queue diagrams
- retry handling strategy

---

# 📈 Part 8 – Scalability Analysis

Analyze:

- expected traffic growth
- scaling bottlenecks
- horizontal scaling opportunities

---

## Example Questions

- Which component may fail first during traffic spikes?
- Which APIs may require scaling?
- Which database operations may become bottlenecks?

---

# 🛡 Part 9 – Reliability Analysis

Identify:

- critical system failures
- failover requirements
- retry requirements
- monitoring needs

---

## Example Questions

- What happens if database fails?
- What happens if cache becomes unavailable?
- Which workflows require retries?
- Which systems require redundancy?

---

# ⚖️ Part 10 – Architecture Trade-Off Analysis

Analyze trade-offs for at least:

- caching
- CDN usage
- replication
- queue systems
- load balancing

---

## Example

| Decision | Benefit | Trade-Off |
|------|------|------|
| Cache | Faster responses | Cache invalidation complexity |

---

# 🧠 Part 11 – Engineering Reflection

Answer the following questions.

---

## Reflection Questions

1. Which system component is most critical?

2. Which workflow may generate the highest traffic?

3. Which workflow requires lowest latency?

4. Which system component may become a scaling bottleneck?

5. Which operations should run asynchronously?

6. Which workflow requires strongest reliability guarantees?

7. Which non-functional requirement most heavily influenced your architecture?

---

# 📊 Deliverables

Submit:

| Deliverable | Description |
|------|------|
| High-Level Architecture Diagram | Complete system visualization |
| Request Lifecycle Diagram | Workflow interaction design |
| Caching Strategy | Cache analysis |
| CDN & Storage Planning | Static asset delivery |
| Queue & Async Workflow Design | Background processing strategy |
| Scalability Analysis | Scaling considerations |
| Reliability Analysis | Failover and resilience planning |
| Trade-Off Analysis | Architecture decision evaluation |
| Engineering Reflection | Answers to reflection questions |

---

# 📋 Submission Guidelines

- Use Markdown format
- Use Mermaid diagrams or architecture diagrams
- Clearly label system components
- Focus on architecture thinking—not implementation code
- Include scalability and reliability considerations

---

# 📊 Evaluation Rubric

| Area | Weight |
|------|------|
| Architecture Clarity | 20% |
| Request Lifecycle Understanding | 15% |
| Scalability Thinking | 15% |
| Reliability Planning | 15% |
| Component Justification | 15% |
| Trade-Off Analysis | 10% |
| Engineering Reflection | 10% |

---

# 🚀 Optional Challenge

Add advanced architecture concepts.

Examples:

- API Gateway
- service discovery
- distributed caching
- read replicas
- event-driven systems
- edge computing
- autoscaling
- observability systems

Explain how these concepts may improve:

- scalability
- reliability
- maintainability
- operational efficiency

---

# 🧠 Engineering Insight

Strong system design is not about adding more technologies.

It is about understanding:

- what the system needs
- where bottlenecks may occur
- how systems scale
- how failures are handled
- how trade-offs affect complexity

Good architectures evolve gradually with system requirements.

---

# 📚 Next Learning Flow

This assignment introduces foundational architecture thinking.

Upcoming modules will continue into:

```plaintext
Monolith Architecture
   ↓
Microservices Architecture
   ↓
Scalability Patterns
   ↓
Reliability & Performance
```

This mirrors how real-world systems evolve from simple applications into distributed platforms.

---

# 🧭 Navigation

← Back to Example  
[Example](./example.md)

➡ Next Day  
[Day 27](../day-27/README.md)