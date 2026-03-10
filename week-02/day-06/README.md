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

## 🧭 Git Collaboration Best Practices

Professional engineering teams follow disciplined Git workflows to ensure stability, traceability, and collaboration.

Below are widely accepted practices used across many organizations.

---

### 1. Write Meaningful Commit Messages

Commit messages should clearly explain the purpose of a change.

**Recommended format**

```
<type>: <short summary>

Optional explanation describing why the change was needed
```

Common commit types:

- `feat:` new feature
- `fix:` bug fix
- `docs:` documentation changes
- `refactor:` internal code improvements
- `test:` test updates
- `chore:` maintenance tasks

**Good Example**

```
feat: add login validation for empty email field
```

**Bad Example**

```
fix stuff
update code
misc changes
```

Good commit messages help future engineers understand the history of a system.

---

### 2. Keep Pull Requests Small

Large pull requests are difficult to review.

Small pull requests are preferred because they:

- reduce review time
- reduce risk
- make bugs easier to detect
- simplify rollbacks

**Best practice**

- 1 feature per pull request
- avoid hundreds of changed files

Small changes improve code review quality.

---

### 3. Push Changes Frequently

Do not keep large changes only on your local machine.

Best practice:

```
Commit often
Push frequently
```

Reasons:

- protects work if the system fails
- allows early collaboration
- reduces large merge conflicts later

Engineering environments are unpredictable — frequent pushes reduce risk.

---

### 4. Use Meaningful Branch Names

Branch names should describe the work being done.

Common conventions:

```
feature/login-system
feature/payment-integration

bugfix/session-timeout

hotfix/security-patch

release/v1.2.0
```

Avoid vague names like:

```
test
temp
newbranch
```

Clear branch names improve repository clarity.

---

### 5. Delete Branches After Merge

After a pull request is merged:

- delete the feature branch

Reasons:

- prevents accidental reuse
- keeps repository clean
- avoids confusion about active work

Most repositories automatically suggest branch deletion after merge.

---

### 6. Always Pull Before Starting Work

Before beginning work:

```
git checkout main
git pull origin main
```

This ensures your branch starts from the **latest codebase**.

Failing to do this increases the chance of merge conflicts.

---

### 7. Do Not Commit Secrets

Never commit sensitive data such as:

- `.env` files
- API keys
- private tokens
- credentials

Use `.gitignore` to prevent these files from entering version control.

Exposing secrets can cause **serious security incidents**.

---

### 8. Run Tests Before Opening Pull Requests

Before submitting a pull request:

- run unit tests
- ensure builds pass
- verify basic functionality

Submitting broken code wastes reviewer time.

---

### 9. Review Code Respectfully

Code reviews should focus on **improving code**, not criticizing people.

Good review culture includes:

- constructive feedback
- clear explanations
- collaborative discussion

Healthy review culture strengthens engineering teams.

---

### 10. Keep the Main Branch Stable

Production systems often rely on the `main` branch.

Best practices include:

- avoid direct commits to `main`
- require pull requests
- run automated checks before merging

This ensures the main branch always remains deployable.

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