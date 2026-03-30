# Resources – Day 18: Logging & Monitoring

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

These resources help you understand:

- logging fundamentals
- monitoring systems
- observability concepts
- logs vs metrics vs traces
- distributed tracing and correlation IDs
- how engineers debug production systems

This section focuses on **conceptual clarity and real-world understanding**.

---

# 📖 Official Documentation & Authoritative Sources

---

### Google SRE – Monitoring Distributed Systems

https://sre.google/sre-book/monitoring-distributed-systems/

Covers:

- monitoring principles  
- golden signals (latency, traffic, errors, saturation)  
- production system reliability  

---

### OpenTelemetry – Observability Concepts

https://opentelemetry.io/docs/concepts/observability-primer/

Explains:

- logs, metrics, traces  
- observability fundamentals  
- modern distributed system visibility  

---

### Microsoft – Logging and Monitoring (Cloud Perspective)

https://learn.microsoft.com/en-us/azure/architecture/best-practices/monitoring

Covers:

- monitoring strategies  
- logging practices  
- alerting concepts  

---

# 🎓 Structured Learning Material

---

### Red Hat – What is Observability?

https://www.redhat.com/en/topics/devops/what-is-observability

Explains:

- observability vs monitoring  
- logs, metrics, traces  
- system visibility  

---

### IBM – What is Application Monitoring?

https://www.ibm.com/topics/application-monitoring

Covers:

- performance monitoring  
- system health tracking  
- real-world monitoring use cases  

---

### Grafana Labs – Observability Explained

https://grafana.com/docs/grafana-cloud/introduction/what-is-observability/

Explains:

- why need of observability  
- what data is collected  
- how data is collected  

---

# 🛠 Tools Awareness (High-Level)

---

## 🔹 Logging Systems

- ELK Stack (Elasticsearch, Logstash, Kibana)  
- Splunk  

👉 Used for storing, searching, and visualizing logs

---

## 🔹 Monitoring Systems

- Prometheus  
- Grafana  
- Datadog  

👉 Used for tracking metrics and system health

---

## 🔹 Distributed Tracing

- Jaeger  
- Zipkin  

👉 Used for tracking request flow across services

---

# 🌐 Hands-On Exploration (Optional but Recommended)

---

### 🔹 View Logs in Browser (Frontend)

Open Chrome DevTools:

- Network Tab → inspect API calls  
- Console Tab → view logs  

---

### 🔹 Public Observability Playground

https://play.grafana.org/

Explore:

- dashboards  
- metrics  
- visualization  

---

### 🔹 Try Logs with Simple App

Run a basic Node.js or Python app and print logs:

```javascript
console.log("User login attempt");
console.error("Database connection failed");
```

Observe:

- log levels  
- timestamps  
- debugging usefulness  

---

# 🎥 Recommended Videos

---

### Logs vs Metrics vs Traces Explained

https://www.youtube.com/watch?v=ZVKrN1RLetI

---

### Observability Explained (Simple)

https://www.youtube.com/watch?v=TQur9GJHIIQ

---

### Observability vs Monitoring vs Logging vs Alerting

https://www.youtube.com/watch?v=TYE2u7QZNVA

---

# 📌 Suggested Learning Flow

1. Start with Google SRE monitoring principles.
2. Understand observability using OpenTelemetry.
3. Learn difference between logs, metrics, and traces.
4. Explore monitoring concepts via Microsoft docs.
5. Explore Grafana dashboards (hands-on).
6. Relate concepts to real production debugging.

---

## ⚠️ Key Takeaways

- logs show what happened  
- metrics show trends  
- traces show request flow  
- observability combines all three  
- monitoring detects issues early  
- alerting enables fast response  

---

## 🧭 Navigation

← Back to Lesson  
[Day 18](./README.md)

➡ Next: Assignments  
[Assignments](./assignments.md)