# Assignments – Day 19: Networking Fundamentals

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

Apply networking concepts to:

- understand how data travels across layers  
- use CLI tools to inspect network behavior  
- map protocols to OSI/TCP-IP models  
- debug real-world connectivity issues  

This module focuses on **practical networking for engineers**.

---

# 🧠 Part 1 – Conceptual Understanding

Answer in your own words:

1. Why do networking models like OSI and TCP/IP exist?
2. What is the key difference between OSI and TCP/IP?
3. Which layers are responsible for:
   - routing  
   - data transmission  
   - application communication  
4. Why is layering important in networking?

---

# 🧱 Part 2 – Layer Mapping Exercise

### Scenario

A user opens a browser and accesses:

```
https://example.com/api/products
```

---

## Tasks

Map the request across layers:

| Layer | Responsibility | Protocol |
|------|---------------|----------|

Also answer:

- Where does HTTP operate?
- Where does TCP operate?
- Where does IP operate?

---

# 🔄 Part 3 – Encapsulation Deep Dive

Explain the transformation:

```plaintext
Data → Segment → Packet → Frame → Bits
```

---

## Tasks

1. What is added at each layer?
2. Why is encapsulation required?
3. What happens during de-encapsulation?

---

# 🌐 Part 4 – CLI Hands-On (Mandatory)

Run the following commands:

---

## 🔹 1. Ping

```
ping google.com
```

### Answer:

- What IP address is resolved?
- What does latency indicate?

---

## 🔹 2. Traceroute

```
traceroute google.com
```

(or `tracert` on Windows)

### Answer:

- How many hops are there?
- What do intermediate IPs represent?

---

## 🔹 3. NSLookup

```
nslookup google.com
```

### Answer:

- What IP addresses are returned?
- Why are there multiple IPs?

---

# 🔍 Part 5 – curl Deep Inspection

Run:

```
curl -v https://example.com
```

---

## Tasks

Identify:

- request headers  
- response headers  
- status code  
- connection details  

---

## Reflection

- Which layer does curl operate at?
- What parts of OSI/TCP-IP are visible here?

---

# 🔌 Part 6 – Ports & Protocol Mapping

---

## Tasks

Map the following:

| Use Case | Port | Protocol | Layer |
|----------|------|----------|------|
| Web (HTTP) | | | |
| Secure Web | | | |
| SSH Access | | | |
| Database (MySQL) | | | |

---

## Questions

- Why are ports required?
- What happens if a port is blocked?

---

# 🧩 Part 7 – Network Debugging Scenario

---

### Scenario

A frontend app cannot call backend API.

---

## Tasks

List possible issues:

- DNS failure  
- server down  
- port blocked  
- firewall restriction  

---

## Step-by-Step Debug Plan

Explain how you would debug using:

- ping  
- nslookup  
- curl  
- traceroute  

---

# 🌍 Part 8 – Real Packet Journey

---

### Scenario

```
Laptop → Router → ISP → Internet → Server → Database
```

---

## Tasks

1. Map each step to OSI layers
2. Identify protocols involved
3. Explain how routing happens

---

# 🛠 Part 9 – Wireshark Exploration (Advanced)

---

## Task

Install Wireshark and:

1. Capture network traffic
2. Filter HTTP or DNS packets
3. Observe:

- packet structure  
- source/destination IP  
- protocol  

---

## Questions

- What layers can you observe?
- What protocol is most visible?
- What surprised you?

---

# 📋 Self-Evaluation Checklist

- [ ] I understand OSI vs TCP/IP models
- [ ] I can map protocols to layers
- [ ] I can use networking CLI tools
- [ ] I can inspect HTTP requests using curl
- [ ] I understand ports and protocols
- [ ] I can debug network-related issues
- [ ] I understand packet flow across systems

---

# 🚀 Optional Challenge (Advanced)

Debug the following scenario:

> API works locally but fails in production

---

## Tasks

- Identify possible networking causes
- Explain debugging approach
- Map failure to network layers

---

## 🧭 Navigation

← Back to Resources  
[Resources](./resources.md)

➡ Next: Day 20  
[Next Day](../day-20/README.md)