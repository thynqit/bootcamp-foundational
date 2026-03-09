# Day 6 – Git Branching & Code Review

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

In professional software development, multiple engineers work on the same codebase simultaneously.

Git branching allows teams to develop features independently without affecting the stability of the main codebase.

Code review ensures that changes are inspected before merging, improving:

- code quality
- maintainability
- security
- team knowledge sharing

This module introduces the collaborative workflows used by engineering teams when working with Git repositories.

---

## 🎯 Learning Objectives

By the end of this module, learners should be able to:

- Understand why Git branching is essential in collaborative development
- Create and switch branches using Git CLI
- Merge branches safely
- Understand pull request workflows
- Explain the purpose of code reviews
- Identify common branching strategies used in teams

---

## 🧠 Core Concepts

### 1. Why Branching Exists

When multiple developers modify the same codebase, conflicts can occur.

Branching allows developers to:

- work independently
- isolate experimental features
- test changes safely
- merge work only when it is ready

Branches act as **parallel lines of development**.

---

### 2. What is a Git Branch?

A branch is simply a **pointer to a sequence of commits**.

The default branch is usually:

```
main
```

New work is typically done in **feature branches**.

Example:

```
feature-login
feature-payment
bugfix-session-timeout
```

This keeps the main branch stable.

---

### 3. Creating and Switching Branches

Create a new branch:

```
git branch feature-login
```

Switch to the branch:

```
git checkout feature-login
```

Or combine both:

```
git checkout -b feature-login
```

Verify current branch:

```
git branch
```

---

### 4. Merging Branches

After completing work in a feature branch, it is merged into the main branch.

Example workflow:

Switch to main:

```
git checkout main
```

Merge feature branch:

```
git merge feature-login
```

Git will combine the histories of both branches.

---

### 5. Merge Conflicts

Conflicts occur when two branches modify the same part of a file.

Example scenario:

Developer A modifies line 10  
Developer B modifies line 10

Git cannot automatically decide which version to keep.

Developers must manually resolve conflicts.

---

### 6. Pull Requests

In collaborative environments (GitHub, GitLab, Bitbucket), changes are typically merged through **Pull Requests (PRs)**.

Pull requests allow teams to:

- review code changes
- discuss improvements
- run automated tests
- ensure quality before merging

Typical workflow:

1. Create feature branch
2. Push branch to remote
3. Open Pull Request
4. Code review happens
5. Merge into main branch

---

### 7. Code Reviews

Code reviews are an essential engineering practice.

They help ensure:

- correctness of logic
- code readability
- security practices
- adherence to team standards

Code reviews also help share knowledge across the team.

---

## 🌍 Real-World Relevance

In production environments:

- Direct commits to the main branch are usually restricted.
- All changes go through pull requests.
- Automated checks run before merging.
- Code reviews prevent bugs and security issues.

Collaborative Git workflows are fundamental to modern engineering teams.

---

## 🧩 Practical Understanding

Scenario:

Two engineers are working on the same application.

Engineer A builds a **login feature**.  
Engineer B builds a **notification feature**.

Without branching:

- their changes could overwrite each other
- the application could break

With branching:

- both features are developed independently
- changes are reviewed
- stable code is merged safely

---

## ⚠️ Common Mistakes

- Working directly on the `main` branch
- Creating very large pull requests
- Ignoring code review feedback
- Merging without pulling latest changes
- Leaving branches unmerged for long periods

These mistakes increase the risk of conflicts and unstable releases.

---

## 🔄 Reflection Questions

- Why should teams avoid committing directly to the main branch?
- How do branches enable parallel development?
- Why are code reviews important for team collaboration?
- What risks occur when pull requests are skipped?

---

## 📚 Next Steps

- Review `resources.md`
- Complete `assignments.md`
- Practice Git branching workflows locally
- Observe how pull requests work on GitHub repositories

---

## 🧭 Navigation

← **Previous Module**  
[Week 2](../README.md)

➡ **Next: Resources**  
[Resources](./resources.md)