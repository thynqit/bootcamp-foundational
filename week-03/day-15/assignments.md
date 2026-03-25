# Assignments – Day 15: Testing Fundamentals

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

In this assignment, you will:

- write unit tests
- validate API behavior
- test interactions between components
- improve code testability
- think like a backend engineer responsible for quality

This assignment focuses on **developer responsibilities in testing**, not QA workflows.

---

# 🧠 Part 1 – Unit Testing

---

### Scenario

You are given the following function:

```javascript
function calculateDiscount(price, discountPercentage) {
    return price - (price * discountPercentage / 100);
}
```

---

### Tasks

1. Write test cases for:

- normal input
- zero discount
- 100% discount
- negative values
- invalid inputs (null, string)

2. Identify:

- edge cases
- failure scenarios

---

### Goal

Ensure your function behaves correctly under all conditions.

---

# 🔗 Part 2 – Integration Testing

---

### Scenario

You have two components:

```javascript
function getUser(userId) {
    return { id: userId, name: "John Doe" };
}

function getUserOrders(userId) {
    return ["order1", "order2"];
}
```

---

### Task

Create a function:

```javascript
function getUserProfile(userId)
```

That combines:

- user data
- user orders

---

### Testing Task

- test if both components integrate correctly
- simulate failure in one function
- validate error handling

---

### Goal

Ensure components work correctly **together**, not just individually.

---

# 🌐 Part 3 – API Testing

---

### Scenario

Use a public API:

```
https://fakestoreapi.com/products
```

---

### Tasks

1. Send request using:

- curl (CLI) OR
- Postman / Bruno

---

2. Validate:

- status code
- response structure
- data types
- empty / invalid responses

---

3. Test:

- GET all products
- GET product by ID
- invalid endpoint

---

### Goal

Understand how backend APIs behave under different conditions.

---

# 🧪 Part 4 – Code-Level Validation

---

### Scenario

You are building an API:

```
POST /users
```

Payload:

```json
{
  "email": "user@example.com",
  "password": "12345"
}
```

---

### Tasks

Define validation rules:

- email format
- password length
- required fields

---

### Test Cases

Write test scenarios for:

- missing fields
- invalid email
- weak password
- valid request

---

### Goal

Ensure backend does not rely on frontend validation.

---

# 🧩 Part 5 – Writing Testable Code

---

### Scenario

Bad Code:

```javascript
function processPayment(amount) {
    if (amount > 0) {
        console.log("Payment successful");
    } else {
        console.log("Invalid payment");
    }
}
```

---

### Tasks

1. Refactor code to:

- return values instead of printing
- separate logic from side effects

---

2. Write unit tests for refactored code

---

### Goal

Understand:

```
Testable code = predictable + modular + isolated
```

---

# ⚠️ Part 6 – Identify Testing Gaps

---

### Scenario

A developer writes:

- only happy path tests
- no edge case testing
- no validation tests

---

### Task

Answer:

- what risks exist?
- what bugs may go unnoticed?
- what additional tests are required?

---

### Goal

Develop **testing mindset**, not just testing skill.

---

# 🔄 Part 7 – Reflection

Answer briefly:

1. Why should developers write unit tests?
2. What is the difference between unit and integration testing?
3. Why is API testing important?
4. Why should backend validate inputs?
5. What makes code testable?

---

# 📋 Self-Evaluation Checklist

- [ ] I wrote unit tests with edge cases
- [ ] I tested integration between components
- [ ] I validated API responses
- [ ] I implemented input validation tests
- [ ] I improved code testability
- [ ] I identified testing gaps

---

# 🚀 Optional Challenge (Advanced)

Take it further:

- write automated API tests using Postman collection
- simulate failure scenarios (timeouts, errors)
- mock external dependencies
- integrate tests into CI/CD pipeline (conceptual)

---

## 🧭 Navigation

← Back to Resources  
[Resources](./resources.md)

➡ Next Module: Week 4  
[Week 4](../../week-04/README.md)