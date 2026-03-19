# Day 15 – Testing Fundamentals

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

Testing ensures that software systems are:

- correct
- reliable
- secure
- maintainable

Without proper testing:

- bugs reach production
- user experience degrades
- systems become unstable

Modern engineering teams treat testing as a **core responsibility across roles**, not just QA.

This module covers:

- types of testing across roles
- testing strategies used in startups and enterprises
- how testing fits into development lifecycle

---

## 🎯 Learning Objectives

By the end of this module, learners should be able to:

- understand different types of testing
- differentiate between manual, automated, and developer testing
- explain unit, integration, and system testing
- understand black-box, white-box, and grey-box testing
- explain regression and functional testing
- understand testing in CI/CD pipelines
- identify testing responsibilities across roles

---

## 🧠 Core Concepts

---

### 1. Why Testing Matters

Testing helps:

- detect bugs early
- ensure system stability
- improve code quality
- reduce production risk

---

### 2. Testing Across Roles

---

#### 👨‍💻 Developer Responsibilities

- Unit Testing
- Integration Testing
- API Testing
- Code-level validation
- Writing testable code

---

#### 🧪 Manual QA Responsibilities

- Functional Testing
- Exploratory Testing
- Usability Testing
- Regression Testing
- End-to-End validation

---

#### 🤖 Automation Engineer Responsibilities

- Test automation frameworks
- Regression automation
- API automation
- UI automation
- CI/CD test integration

---

### 3. Types of Testing (Core)

---

#### Unit Testing

- tests individual components
- written by developers

Example:

```
function add(a, b) → test with inputs
```

---

#### Integration Testing

- tests interaction between components

Example:

- API + database interaction

---

#### System Testing

- tests complete system

---

#### End-to-End (E2E) Testing

- simulates real user flows

Example:

```
Login → Add to Cart → Checkout
```

---

### 4. Functional vs Non-Functional Testing

---

#### Functional Testing

- verifies features work correctly

Example:

- login works
- payment succeeds

---

#### Non-Functional Testing

Focuses on system qualities:

- performance
- scalability
- security
- reliability

---

### 5. Black Box, White Box, Grey Box

---

#### Black Box Testing

- tester does not know internal logic
- tests based on inputs/outputs

---

#### White Box Testing

- tester knows internal code
- tests logic paths

---

#### Grey Box Testing

- partial knowledge of system

---

### 6. Regression Testing

Ensures:

```
New changes do not break existing features
```

Critical in:

- large systems
- frequent releases

---

### 7. API Testing

- validate endpoints
- check request/response
- verify status codes

---

### 8. Performance Testing

Measures:

- response time
- system load handling

Types:

- load testing
- stress testing

---

### 9. Security Testing

Validates:

- authentication
- authorization
- vulnerabilities

---

### 10. Test Automation

Automation helps:

- run tests repeatedly
- speed up regression testing
- integrate with CI/CD

---

### 11. CI/CD & Testing

In modern systems:

```
Code → Build → Test → Deploy
```

Tests run automatically before deployment.

---

### 12. Test Pyramid (Important Concept)

```
        E2E Tests
      Integration Tests
   Unit Tests
```

- more unit tests
- fewer E2E tests

---

### 13. Common Testing Mistakes

- relying only on manual testing
- skipping unit tests
- writing brittle automation tests
- ignoring edge cases
- not testing failure scenarios

---

## 🌍 Real-World Relevance

In production systems:

- lack of testing → outages
- poor regression → broken features
- no automation → slow releases

High-performing teams:

- automate testing
- integrate testing in CI/CD
- test continuously

---

## 🧩 Practical Understanding

Scenario:

You are building a **ride booking app**.

- what tests will developers write?
- what will QA validate?
- what will be automated?

---

## 🔄 Reflection Questions

- Why should developers write tests?
- Why is regression testing critical?
- What is the difference between functional and non-functional testing?
- Why is automation important?
- What risks exist without testing?

---

## 📚 Next Steps

- Review `resources.md`
- Complete `assignments.md`
- Explore testing tools and frameworks

---

## 🧭 Navigation

← Previous: 
[Day 14](../day-14/README.md)

➡ Next: 
[Resources](./resources.md)