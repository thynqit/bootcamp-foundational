# Assignments – Day 18: Logging & Monitoring

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

Apply logging, monitoring, and observability concepts to:

- analyze system behavior  
- debug production issues  
- interpret logs, metrics, and traces  
- think like a production engineer  

---

# 🧠 Part 1 – Conceptual Understanding

Answer in your own words:

1. What is the difference between logging and monitoring?
2. Why are logs alone insufficient in distributed systems?
3. What are metrics and how are they used in monitoring?
4. What is distributed tracing and why is it important?
5. What is a correlation ID and how does it help debugging?

---

# 🔍 Part 2 – Log Analysis

Below are sample logs:

```plaintext
INFO 2026-03-28 10:01:23 Request received /api/orders requestId=abc123

INFO 2026-03-28 10:01:24 Fetching order details orderId=567 requestId=abc123

ERROR 2026-03-28 10:01:25 Database timeout orderId=567 requestId=abc123

WARN 2026-03-28 10:01:26 Retrying request requestId=abc123

ERROR 2026-03-28 10:01:30 Request failed /api/orders requestId=abc123
```

---

## Tasks

1. What went wrong in this system?
2. At which step did the failure occur?
3. What does the correlation ID indicate?
4. How would you debug this issue further?

---

# 🌐 Part 3 – Distributed System Debugging

### Scenario

A request flows through:

```plaintext
API Gateway → Order Service → Payment Service → Database
```

---

## Logs from Services

```plaintext
[Gateway] Request received requestId=xyz789

[Order Service] Processing order requestId=xyz789

[Payment Service] Payment validation started requestId=xyz789

[Payment Service] ERROR Payment declined requestId=xyz789

[Order Service] ERROR Order failed requestId=xyz789
```

---

## Tasks

1. Identify where the failure occurred
2. Trace the request flow using correlation ID
3. Explain how distributed tracing helps here
4. What additional logs would you add?

---

# 📊 Part 4 – Metrics & Monitoring Thinking

### Scenario

System metrics show:

- CPU usage: 95%
- Error rate: increasing
- Latency: high

---

## Tasks

1. What could be the possible reasons?
2. Which metric would you check first and why?
3. What alert should be configured?
4. How would you prevent this in future?

---

# 🚨 Part 5 – Alert Design

Design alerts for:

1. API failure rate > 5%
2. Response time > 2 seconds
3. Database connection failures

---

## Output

For each alert define:

- Condition  
- Severity  
- Action  

---

# 🔗 Part 6 – Correlation ID & Tracing

---

## Task

Explain:

1. How correlation IDs are generated
2. Where they are passed (headers, services)
3. How they are logged across services

---

## Bonus

Design a request flow showing correlation ID usage.

---

# 🛠 Part 7 – Hands-On Exploration

Choose ONE:

---

### Option A – Browser DevTools

1. Open any website
2. Go to Network tab
3. Inspect API calls

Answer:

- What requests are made?
- What response codes are returned?

---

### Option B – Simple Logging

Write a small script:

```javascript
console.log("User login");
console.error("Database failure");
```

Observe:

- log structure
- readability

---

### Option C – Grafana Playground

https://play.grafana.org/

Explore:

- dashboards
- metrics visualization

---

# 🧩 Part 8 – Real-World Debugging Scenario

---

### Scenario

Users report:

> “Checkout is failing randomly”

---

## Tasks

Explain step-by-step:

1. What logs will you check?
2. What metrics will you analyze?
3. How will you trace the request?
4. How will you identify root cause?

---

# 📋 Self-Evaluation Checklist

- [ ] I understand logs vs metrics vs traces
- [ ] I can analyze logs and identify failures
- [ ] I understand correlation IDs
- [ ] I can think through debugging steps
- [ ] I understand monitoring and alerts
- [ ] I can approach real production issues

---

# 🚀 Optional Challenge (Advanced)

Design an observability system for:

👉 A ride-sharing platform (like Uber)

Include:

- logging strategy  
- monitoring metrics  
- alert system  
- tracing approach  

---

## 🧭 Navigation

← Back to Resources  
[Resources](./resources.md)

➡ Next: Day 19 – Networking Basics  
[Next Day](../day-19/README.md)