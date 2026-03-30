# Resources – Day 17: DevOps & CI/CD

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

These resources help you understand:

- DevOps mindset and practices
- CI/CD concepts and pipelines
- software delivery lifecycle
- artifacts and environments
- deployment strategies
- how CI/CD works across web, mobile, and cloud applications

This section focuses on **conceptual clarity and real-world understanding**, not tool-specific tutorials.

---

# 🔧 1. DevOps Fundamentals

---

## 📖 Learn

- https://www.atlassian.com/devops  
- https://www.redhat.com/en/topics/devops  

---

## 🧠 Key Understanding

- DevOps = collaboration + automation  
- bridges gap between development and operations  
- enables faster and reliable delivery  

---

# 🔁 2. CI/CD Concepts

---

## 📖 Learn

- https://www.redhat.com/en/topics/devops/what-is-ci-cd  
- https://www.atlassian.com/continuous-delivery/principles  

---

## 🧠 Key Understanding

- CI → frequent integration + automated testing  
- CD → continuous delivery or deployment  
- reduces release risk  

---

# 🏗 3. CI/CD Pipelines

---

## 📖 Learn

- https://www.atlassian.com/continuous-delivery/principles/pipeline  
- https://circleci.com/continuous-integration/  

---

## 🧠 Key Understanding

- pipeline automates build → test → deploy  
- triggered by Git events  
- ensures consistent delivery  

---

# 📦 4. Artifacts & Build Systems

---

## 📖 Learn

- https://jfrog.com/devops-tools/article/what-is-an-artifact/  

---

## 🧠 Key Understanding

- artifact = build output  
- versioned and deployed across environments  
- ensures consistency  

---

# 🌍 5. Environments

---

## 📖 Learn

- https://docs.aws.amazon.com/prescriptive-guidance/latest/choosing-git-branch-approach/understanding-the-devops-environments.html  

---

## 🧠 Key Understanding

- dev → staging → production  
- prevents direct production failures  
- enables safe testing  

---

# 🚀 6. Deployment Strategies

---

## 📖 Learn

- https://www.redhat.com/en/topics/devops/what-is-blue-green-deployment  
- https://martinfowler.com/bliki/CanaryRelease.html  

---

## 🧠 Key Understanding

- rolling → gradual updates  
- blue-green → environment switch  
- canary → small user testing  

---

# ⚙️ 7. Infrastructure as Code (IaC)

---

## 📖 Learn

- https://aws.amazon.com/what-is/iac/  

---

## 🧠 Key Understanding

- infrastructure defined as code  
- reproducible and version-controlled  
- enables automation  

---

# 🔄 8. Monitoring & Feedback

---

## 📖 Learn

- https://www.ibm.com/think/topics/devops-monitoring
- https://www.atlassian.com/devops/devops-tools/devops-monitoring  

---

## 🧠 Key Understanding

- monitor system after deployment  
- logs and metrics provide insights  
- feedback improves system  

---

# 🛠 9. DevOps Tools (Awareness Only)

---

| Category | Tools |
|----------|------|
| CI/CD | GitHub Actions, Jenkins |
| Build | Maven, Gradle |
| Containers | Docker |
| Orchestration | Kubernetes |
| Artifact Repo | Nexus, JFrog |

---

# 🌐 10. CI/CD Across Application Types

---

## 🔹 Web Applications

---

### Flow

```
Code → Build (bundle) → Test → Deploy to server/CDN
```

---

### Tools (Awareness)

- Build: Webpack, Vite  
- CI/CD: GitHub Actions, GitLab CI  
- Hosting: Netlify, Vercel  

---

### 📖 Learn

- https://vercel.com/docs/concepts/deployments  
- https://docs.netlify.com/site-deploys/overview/  

---

### 🧠 Understanding

- frontend is built into static assets  
- deployed globally via CDN  
- fast delivery to users  

---

## 🔹 Mobile Applications

---

### Flow

```
Code → Build APK/IPA → Test → Publish to Store
```

---

### Tools (Awareness)

- CI/CD: Bitrise, Codemagic, GitHub Actions  
- Build: Gradle (Android), Xcode (iOS)  

---

### 📖 Learn

- https://docs.bitrise.io/en/bitrise-ci/getting-started/getting-started.html  
- https://docs.codemagic.io/getting-started/adding-apps/  

---

### 🧠 Understanding

- builds generate installable apps  
- deployment involves app stores  
- release cycles are controlled  

---

## 🔹 Backend / Cloud Applications

---

### Flow

```
Code → Build → Test → Artifact → Deploy to Cloud
```

---

### Tools (Awareness)

- CI/CD: Jenkins, GitHub Actions  
- Containers: Docker  
- Cloud: AWS, Azure, GCP  

---

### 📖 Learn

- https://aws.amazon.com/devops/what-is-devops/  
- https://cloud.google.com/architecture/devops  

---

### 🧠 Understanding

- APIs deployed on servers or containers  
- artifacts reused across environments  
- scalable and monitored systems  

---

# 🎥 Recommended Videos

---

### DevOps Explained Simply

https://www.youtube.com/watch?v=j5Zsa_eOXeY

---

### CI/CD Pipeline Explained

https://www.youtube.com/watch?v=m0a2CzgLNsc

---

### Deployment Strategies Explained

https://www.youtube.com/watch?v=AWVTKBUnoIg

---

# 📌 Suggested Learning Flow

1. Start with DevOps fundamentals.
2. Understand CI/CD concepts.
3. Learn pipeline stages.
4. Understand artifacts and environments.
5. Explore deployment strategies.
6. See how CI/CD differs across application types.
7. Connect concepts to real-world systems.

---

## ⚠️ Key Takeaways

- DevOps is a mindset, not just tools  
- CI/CD reduces release risk  
- automation improves reliability  
- artifacts ensure consistency  
- environments prevent production failures  
- different platforms have different pipelines  

---

## 🧭 Navigation

← Back to Lesson  
[Day 17](./README.md)

➡ Next: Assignments  
[Assignments](./assignments.md)