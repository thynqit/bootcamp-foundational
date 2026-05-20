# Assignments – Day 28: Microservices Architecture

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

# 📌 Overview

In this assignment, learners will think like:

- distributed systems engineers
- cloud architects
- platform engineers
- backend engineering teams

to evolve their previously designed monolithic system into a distributed microservices architecture.

The goal is to understand:

- service decomposition
- distributed communication
- API Gateway patterns
- database-per-service architecture
- observability requirements
- reliability strategies
- distributed systems trade-offs

This assignment continues the same platform selected during previous modules.

---

# 🎯 Assignment Objectives

By completing this assignment, learners should be able to:

- decompose systems into microservices
- define service boundaries
- design service communication flows
- design API Gateway architecture
- design database-per-service systems
- identify distributed system challenges
- design observability workflows
- evaluate microservices trade-offs

---

# 🧩 Continue Your Selected Platform

Continue using the same platform selected in previous assignments.

Examples:

- Amazon / E-Commerce Platform
- Uber / Ride Booking Platform
- Netflix / Streaming Platform
- Swiggy / Food Delivery Platform
- Airbnb / Booking Platform

This continuity mirrors how real-world systems evolve from monoliths into distributed architectures.

---

# 🛠 Part 1 – Decompose the Monolith

Using your Day 27 monolith design, break the system into independently deployable services.

---

## Example Services

| Platform | Example Services |
|------|------|
| Amazon | Catalog, Checkout, Payments |
| Uber | Rider, Driver, Trips |
| Netflix | Streaming, Recommendations |
| Swiggy | Orders, Restaurants, Delivery |
| Airbnb | Listings, Bookings, Payments |

---

## Deliverables

Define:

- service names
- service responsibilities
- ownership boundaries

---

# 🧱 Part 2 – Design High-Level Microservices Architecture

Design a distributed architecture for your platform.

---

## Architecture Requirements

Your architecture should include:

- frontend applications
- API Gateway
- microservices
- service communication
- databases
- cache layer
- queues
- observability systems

---

# 📄 Part 3 – Create Microservices Architecture Diagram

Create a complete distributed system architecture diagram.

---

## Diagram Requirements

Visualize:

- API Gateway
- services
- databases
- communication flow
- queues
- infrastructure components

---

## Example Flow

```plaintext
Users
    ↓
API Gateway
    ↓
Microservices
    ↓
Service Databases
```

---

# 🔄 Part 4 – Service Communication Design

Choose ONE important workflow.

Examples:

- checkout
- ride booking
- order placement
- video streaming
- property booking

Design:

- inter-service communication
- synchronous workflows
- asynchronous workflows

---

## Deliverables

Include:

- sequence diagram
- service interaction explanation
- communication protocols

---

# 🗄 Part 5 – Database-Per-Service Design

Design isolated databases for your services.

---

## Deliverables

Define:

- service-owned databases
- isolated entities
- cross-service data dependencies

---

## Example Questions

- Which services own which data?
- Which workflows require cross-service communication?
- Which data may become duplicated?

---

# 🌍 Part 6 – API Gateway Design

Design an API Gateway layer.

---

## Gateway Responsibilities

Include:

- authentication
- routing
- monitoring
- rate limiting
- security

---

## Deliverables

Create:

- API Gateway diagram
- routing flow
- authentication workflow

---

# 📬 Part 7 – Asynchronous Processing Design

Identify workflows requiring asynchronous communication.

Examples:

- notifications
- retries
- analytics
- recommendation systems

---

## Deliverables

Include:

- queue architecture
- worker processing
- retry strategy

---

# 📈 Part 8 – Independent Scaling Analysis

Analyze how services scale independently.

---

## Example Questions

- Which service receives highest traffic?
- Which service requires autoscaling?
- Which service is latency-sensitive?
- Which database may require replicas?

---

## Deliverables

Create:

- scaling diagram
- traffic analysis
- scaling strategy explanation

---

# 🛡 Part 9 – Reliability & Failure Handling

Design resilience strategies for distributed systems.

---

## Include

- retries
- timeouts
- redundancy
- failover
- circuit breakers

---

## Example Questions

- What happens if Payment Service fails?
- How are retries handled?
- How are cascading failures prevented?

---

# 📊 Part 10 – Observability Design

Design observability systems for your distributed platform.

---

## Include

- centralized logging
- monitoring
- metrics
- distributed tracing
- correlation IDs

---

## Deliverables

Create:

- observability architecture diagram
- tracing workflow
- monitoring strategy

---

# ⚖️ Part 11 – Trade-Off Analysis

Analyze the trade-offs of microservices architecture.

---

## Example

| Benefit | Trade-Off |
|------|------|
| Independent deployments | Operational complexity |
| Service isolation | Distributed debugging |

---

# 🧠 Part 12 – Engineering Reflection

Answer the following questions.

---

## Reflection Questions

1. Which service requires the highest scalability?

2. Which workflow becomes hardest in distributed systems?

3. Why is observability critical in microservices?

4. Which services require strongest reliability guarantees?

5. Which operations should use asynchronous communication?

6. Which distributed system challenge concerns you most?

7. At what company scale does microservices become beneficial?

---

# 📊 Deliverables

Submit:

| Deliverable | Description |
|------|------|
| Service Decomposition | Service boundaries |
| Microservices Architecture Diagram | Distributed system design |
| Service Communication Diagram | Workflow interactions |
| Database-Per-Service Design | Data ownership |
| API Gateway Design | Gateway responsibilities |
| Async Workflow Design | Queue & worker architecture |
| Reliability Strategy | Failure handling |
| Observability Design | Monitoring & tracing |
| Trade-Off Analysis | Architecture evaluation |
| Engineering Reflection | Answers to reflection questions |

---

# 📋 Submission Guidelines

- Use Markdown format
- Use Mermaid diagrams or architecture diagrams
- Clearly separate service responsibilities
- Focus on architecture—not implementation code
- Explain distributed system trade-offs clearly

---

# 📊 Evaluation Rubric

| Area | Weight |
|------|------|
| Service Decomposition | 15% |
| Architecture Clarity | 20% |
| Communication Design | 15% |
| Reliability Thinking | 15% |
| Observability Design | 10% |
| Scalability Analysis | 10% |
| Trade-Off Analysis | 10% |
| Engineering Reflection | 5% |

---

# 🚀 Optional Challenge

Add advanced cloud-native concepts.

Examples:

- Kubernetes autoscaling
- service mesh
- event-driven architecture
- saga pattern
- distributed caching
- multi-region deployments
- blue-green deployments
- canary releases

Explain how these concepts improve:

- scalability
- deployment safety
- resilience
- operational maturity

---

# 🧠 Engineering Insight

Microservices are powerful because they improve:

- independent scaling
- deployment flexibility
- team autonomy
- fault isolation

However, they also introduce major complexity in:

- distributed debugging
- observability
- networking
- reliability engineering
- infrastructure operations

Successful microservices architectures require strong engineering maturity—not just more services.

---

# 📚 Next Learning Flow

This assignment continues the distributed systems evolution journey:

```plaintext
System Design Basics
   ↓
Monolith Architecture
   ↓
Microservices Architecture
   ↓
Scalability & Distributed Systems
   ↓
Performance & Reliability
```

This mirrors how many real-world engineering systems evolve over time.

---

# 🧭 Navigation

← Back to Example  
[Example](./example.md)

➡ Next Day  
[Day 29](../day-29/README.md)