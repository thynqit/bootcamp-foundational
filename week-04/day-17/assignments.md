# Assignments – Day 17: DevOps & CI/CD

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

Apply DevOps and CI/CD concepts to design real-world delivery pipelines across:

- Web applications
- Backend systems
- Mobile applications

Focus on **system thinking, automation, environments, and deployment strategies**.

---

# 🧠 Part 1 – Conceptual Understanding

Answer in your own words:

1. What problem does CI/CD solve in modern software development?
2. What is the role of environments (dev, staging, production)?
3. What is an artifact? Why is it important in CI/CD?
4. Why should deployments be automated?
5. What risks exist if CI/CD is not implemented?

---

# 🏗 Part 2 – CI/CD Pipeline Design (Backend System)

### Scenario

You are building a **backend system for an e-commerce platform**.

### Task

Design a complete CI/CD pipeline.

Include:

- Trigger (e.g., push, pull request)
- Build stage
- Test stage
- Artifact creation
- Deployment stages
- Environments (dev → staging → production)

---

### Output Format

Explain your pipeline in:

1. Step-by-step flow
2. Simple diagram (optional)
3. Description of each stage

---

# 🧾 Part 3 – YAML Pipeline Design

---

## 🔹 3A – Pseudo YAML (Conceptual)

Write a simplified CI/CD pipeline:

```yaml
pipeline:
  trigger: on_push

  stages:
    - build
    - test
    - package
    - deploy_dev
    - deploy_staging
    - deploy_production
```

Expand this with:

- test steps
- environment-based deployments
- basic conditions

---

## 🔹 3B – Real Example (GitHub Actions Style)

Write a basic workflow:

```yaml
name: CI-CD Pipeline

on:
  push:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - checkout code
      - install dependencies
      - run build

  test:
    runs-on: ubuntu-latest
    steps:
      - run tests

  deploy:
    runs-on: ubuntu-latest
    steps:
      - deploy to server
```

Enhance it with:

- environment separation
- conditional deployment
- staging vs production logic

---

# 🌍 Part 4 – Environment Strategy

For the same system:

1. What happens in:
   - Development
   - Staging
   - Production

2. Define:

    - What is tested in each environment?
    - Who has access?
    - What approvals are required?

---

# 🚀 Part 5 – Deployment Strategy Decision

For each scenario, choose a deployment strategy:

---

### Scenario 1 – High Traffic System

- Millions of users
- Cannot afford downtime

👉 Choose:
- Rolling / Blue-Green / Canary  
Explain why

---

### Scenario 2 – Risky New Feature

- Major architecture change

👉 Choose strategy and justify

---

### Scenario 3 – Small Bug Fix

- Low risk change

👉 Choose strategy and justify

---

# 🐳 Part 6 – Docker Integration

---

## Task

Explain how Docker fits into your pipeline:

- Where is Docker used?
- What does the Docker image contain?
- Why is Docker useful in CI/CD?

---

## Practical Thinking

Write a simple Dockerfile:

```dockerfile
FROM node:18
WORKDIR /app
COPY . .
RUN npm install
CMD ["npm", "start"]
```

Explain:

- build step
- image creation
- deployment usage

---

# ☸️ Part 7 – Kubernetes Awareness

---

## Task

Explain:

1. Why Kubernetes is used in production systems
2. How it integrates with CI/CD
3. What happens after deployment

---

## Example Flow

```
CI/CD → Build Docker Image → Push to Registry → Deploy to Kubernetes
```

Explain each step.

---

# 🌐 Part 8 – CI/CD Across Application Types

---

## 🔹 Web Application

Design pipeline for:

- React / frontend app

Include:

- build (bundle)
- deploy to CDN
- caching strategy

---

## 🔹 Backend Application

Design pipeline for:

- API service

Include:

- build
- test
- Docker
- deployment to cloud

---

## 🔹 Mobile Application

Design pipeline for:

- Android / iOS app

Include:

- build APK / IPA
- testing
- distribution

---

# 🛠 Part 9 – Hands-On (Light Practical)

Choose ONE:

### Option A

Create a basic GitHub Actions workflow in a sample repo

---

### Option B

Observe any public GitHub repo:

- Identify CI/CD pipeline
- List steps used

---

### Option C

Simulate full pipeline in markdown

---

# 📋 Self-Evaluation Checklist

- [ ] I understand CI/CD concepts clearly
- [ ] I can design a pipeline end-to-end
- [ ] I understand environments and deployment flow
- [ ] I can write basic YAML pipelines
- [ ] I understand Docker in CI/CD
- [ ] I understand Kubernetes at a high level
- [ ] I can differentiate pipelines across platforms

---

# 🚀 Optional Challenge (Advanced)

Design a CI/CD pipeline for:

👉 A ride-sharing platform (like Uber)

Include:

- backend services
- mobile apps
- deployment strategy
- monitoring integration
- rollback strategy

---

## 🧭 Navigation

← Back to Resources  
[Resources](./resources.md)

➡ Next: Day 18  
[Next Day](../day-18/README.md)