# Example – Day 27: Monolith Architecture

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

# 📌 Overview

This document demonstrates a simplified example of a monolithic architecture for a Target.com inspired e-commerce platform.

The purpose of this example is to help learners understand:

- how monolithic systems are structured
- how modules interact inside a single application
- how shared databases work
- how monoliths scale
- how engineering teams organize large monolithic applications

This example builds on the foundational system design concepts introduced in:

- Day 26 – System Design Basics

This example intentionally focuses only on:

```plaintext
Monolithic Architecture
```

Microservices architecture will be explored separately in Day 28.

---

# Document Information

| Field | Value |
|------|------|
| Platform | Thynqit Commerce Platform |
| Architecture Type | Monolithic Architecture |
| Document Version | v1.0 |
| Prepared By | Engineering Team |
| Prepared Date | 2026-05-26 |

---

# 1. Business Context

The company is building:

- an online shopping platform
- mobile-friendly checkout
- order tracking workflows
- inventory management
- payment processing

The engineering team is currently:

- small in size
- rapidly iterating product features
- prioritizing faster delivery
- optimizing for simplicity

Because of this, the company selected:

```plaintext
Monolithic Architecture
```

for its initial production platform.

---

# 2. High-Level Monolith Architecture

The platform is designed as:

```plaintext
One Deployable Application
```

containing all major business modules.

---

## Monolith Architecture Diagram

```mermaid
flowchart TD

A[Users]
B[Frontend Application]

subgraph Monolith Application

C[Authentication Module]
D[Catalog Module]
E[Cart Module]
F[Checkout Module]
G[Payment Module]
H[Notification Module]
I[Admin Module]

end

J[(Shared Database)]

A --> B
B --> C
B --> D
B --> E
B --> F
B --> G

C --> J
D --> J
E --> J
F --> J
G --> J
H --> J
I --> J
```

---

# 3. Core Modules

The monolith contains multiple internal modules.

---

## Module Breakdown

| Module | Responsibility |
|------|------|
| Authentication | Login & user identity |
| Catalog | Product listing & search |
| Cart | Shopping cart management |
| Checkout | Order placement |
| Payments | Payment processing |
| Notifications | Emails & SMS |
| Admin | Product and order management |

---

# 4. Shared Database Design

All modules share the same relational database.

---

## Shared Database Diagram

```mermaid
flowchart TD

subgraph Monolith Application

A[Catalog Module]
B[Checkout Module]
C[Payment Module]
D[Admin Module]

end

E[(Shared Database)]

A --> E
B --> E
C --> E
D --> E
```

---

## Example Database Tables

```plaintext
users
products
orders
payments
inventory
notifications
```

---

## 🧠 Engineering Note

Shared databases simplify:

- querying
- reporting
- transactions
- development speed

but can create:

- tight coupling
- migration coordination issues
- scaling bottlenecks

as systems grow.

---

# 5. Request Lifecycle Example

---

## Checkout Workflow

```plaintext
User places order
    ↓
Frontend sends checkout request
    ↓
Checkout module validates cart
    ↓
Payment module processes payment
    ↓
Inventory updated
    ↓
Order stored in database
    ↓
Notification module sends confirmation
```

---

## Checkout Sequence Diagram

```mermaid
sequenceDiagram

participant User
participant Frontend
participant Monolith
participant Database

User->>Frontend: Place Order
Frontend->>Monolith: Checkout Request

Monolith->>Monolith: Validate Cart
Monolith->>Monolith: Process Payment
Monolith->>Monolith: Update Inventory

Monolith->>Database: Store Order
Database-->>Monolith: Success

Monolith->>Monolith: Send Notification

Monolith-->>Frontend: Order Success
Frontend-->>User: Confirmation
```

---

# 6. Monolith Deployment Flow

The entire application deploys together.

---

## Deployment Workflow

```mermaid
flowchart LR

A[Code Changes]
B[Build Application]
C[Run Tests]
D[Deploy Monolith]
E[Production Servers]

A --> B --> C --> D --> E
```

---

## 🧠 Engineering Note

Monolith deployments are operationally simpler because:

- only one deployment artifact exists
- infrastructure complexity stays low
- service coordination is unnecessary

However:

```plaintext
A small bug can affect the entire application.
```

---

# 7. Scaling the Monolith

As traffic grows, the platform scales by adding more monolith instances.

---

## Horizontal Scaling Example

```mermaid
flowchart LR

A[Users]
B[Load Balancer]

B --> C[Monolith Instance 1]
B --> D[Monolith Instance 2]
B --> E[Monolith Instance 3]

C --> F[(Shared Database)]
D --> F
E --> F

A --> B
```

---

# 8. Monolith Infrastructure Components

Even monoliths often use modern infrastructure components.

---

## Infrastructure Diagram

```mermaid
flowchart TD

A[Users]
B[CDN]
C[Load Balancer]

D[Monolith Server 1]
E[Monolith Server 2]

F[Cache]
G[(Shared Database)]
H[(Object Storage)]
I[Background Workers]

A --> B
B --> C

C --> D
C --> E

D --> F
E --> F

F --> G

D --> H
E --> H

D --> I
E --> I
```

---

# 9. Background Processing Example

Some workflows are processed asynchronously.

Examples:

- emails
- analytics
- inventory sync
- payment retries

---

## Queue Workflow

```mermaid
flowchart LR

A[Monolith Application]
B[Queue]
C[Notification Worker]

A --> B
B --> C
```

---

# 10. Monolith Advantages in This Example

---

## Why This Architecture Was Selected

| Reason | Benefit |
|------|------|
| Small Team | Faster coordination |
| Rapid Product Iteration | Faster feature delivery |
| Lower Infrastructure Complexity | Easier operations |
| Simpler Deployment | Faster releases |
| Shared Database | Easier transactions |

---

# 11. Challenges Emerging Over Time

As the platform grows:

- deployments become slower
- codebase becomes larger
- database traffic increases
- module dependencies increase
- release coordination becomes difficult

---

## Example Future Challenges

| Area | Challenge |
|------|------|
| Catalog | Heavy search traffic |
| Checkout | Peak traffic during sales |
| Payments | High reliability requirements |
| Notifications | Background processing growth |

---

# 12. Modular Monolith Evolution

To improve maintainability, the engineering team later introduces:

```plaintext
Modular Monolith Structure
```

---

## Example Folder Structure

```plaintext
/catalog
/checkout
/payments
/notifications
/authentication
/admin
```

Each module has:

- clearer boundaries
- internal ownership
- reduced coupling

while remaining:

```plaintext
One Deployable Application
```

---

## Modular Monolith Diagram

```mermaid
flowchart TD

subgraph Modular Monolith

A[Catalog Module]
B[Checkout Module]
C[Payment Module]
D[Notification Module]

end

E[(Shared Database)]

A --> E
B --> E
C --> E
D --> E
```

---

# 13. Reliability Considerations

The platform improves reliability using:

| Strategy | Purpose |
|------|------|
| Load Balancing | Traffic distribution |
| Cache | Faster responses |
| Database Replicas | Read scalability |
| Background Workers | Async processing |
| Monitoring | Failure detection |

---

# 14. Future Architecture Evolution

As traffic and engineering teams grow, the company may eventually evolve toward:

```plaintext
Microservices Architecture
```

---

## Example Evolution Journey

```plaintext
Simple App
    ↓
Monolith
    ↓
Modular Monolith
    ↓
Microservices
```

---

## 🧠 Engineering Note

This gradual evolution is common because:

- early simplicity matters
- operational maturity develops over time
- distributed systems introduce major complexity

---

# 15. Key Takeaways

This example demonstrates how monoliths:

- organize application modules
- simplify deployments
- centralize business logic
- share infrastructure components
- scale using replication and caching
- evolve gradually as systems grow

Monoliths remain highly effective for:

- startups
- MVPs
- moderate-scale systems
- rapidly evolving products

when engineered properly.

---

# 📚 Related Learning Flow

This example continues the same engineering journey:

```plaintext
Requirements
   ↓
APIs & Databases
   ↓
System Design Basics
   ↓
Monolith Architecture
   ↓
Microservices Architecture
```

This mirrors how many real-world systems evolve.

---

# 🧭 Navigation

← Back to Resources  
[Resources](./resources.md)

➡ Next: Assignments  
[Assignments](./assignments.md)