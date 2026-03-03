# Day 4 – Git Basics (CLI First Approach)

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

Git is a distributed version control system used to track changes in code.

It enables:

- Safe collaboration
- Change history tracking
- Rollbacks
- Branching for parallel development

In this module, we focus on using Git through the **Command Line Interface (CLI)** to understand what actually happens behind graphical tools.

Understanding Git at CLI level builds strong engineering confidence.

---

## 🎯 Learning Objectives

By the end of this module, learners should be able to:

- Initialize a Git repository
- Clone a remote repository
- Stage and commit changes
- Push and pull from remote
- Understand basic branching
- Write meaningful commit messages
- Use and understand `.gitignore`

---

## 🧠 Core Concepts

### 1. What is Version Control?

Version control tracks changes to files over time.

It allows:

- Reverting to previous versions
- Comparing changes
- Collaborating safely

Without version control, teams overwrite each other’s work.

---

### 2. Distributed vs Centralized Version Control

Git is distributed:

- Every developer has a full copy of the repository
- Work can be done offline
- History is local

This improves reliability and speed.

---

### 3. Basic Git Workflow

Working Directory → Staging Area → Local Repository → Remote Repository

1. Modify files
2. Stage changes
3. Commit locally
4. Push to remote

Understanding this flow is critical.

---

### 4. Essential Git CLI Commands

#### Initialize Repository

```
git init
```

Creates a new Git repository.

---

#### Clone Repository

```
git clone <repository-url>
```

Creates a local copy of a remote repository.

---

#### Check Status

```
git status
```

Shows modified, staged, and untracked files.

---

#### Stage Changes

```
git add <file-name>
git add .
```

Moves changes to staging area.

---

#### Commit Changes

```
git commit -m "Meaningful commit message"
```

Records a snapshot of staged changes.

---

#### View Commit History

```
git log
```

---

#### Push to Remote

```
git push origin <branch-name>
```

Uploads local commits to remote repository.

---

#### Pull Latest Changes

```
git pull origin <branch-name>
```

Fetches and merges remote changes.

---

### 5. Writing Good Commit Messages

A good commit message:

- Is clear
- Is specific
- Explains why (not just what)

Bad example:
```
fix stuff
```

Good example:
```
Fix login validation error when email field is empty
```

Recommended format:

```
<type>: <short summary>

Optional detailed explanation
```

Example types:

- feat:
- fix:
- refactor:
- docs:
- test:

---

### 6. What is .gitignore?

`.gitignore` tells Git which files or folders to ignore.

Common examples:

- node_modules/
- build/
- .env
- .idea/
- .DS_Store

Ignoring unnecessary files:

- Reduces repository size
- Avoids exposing secrets
- Keeps history clean

---

### 7. Common Beginner Mistakes

- Committing secrets (.env)
- Writing vague commit messages
- Pushing directly to main branch
- Not pulling before pushing
- Committing compiled files

---

## 🌍 Real-World Relevance

In production:

- Poor commit history makes debugging difficult
- Accidental secret commits can cause security breaches
- Improper branching causes deployment issues
- Not understanding Git leads to merge conflicts

Strong Git discipline is a core engineering skill.

---

## 🔄 Reflection Questions

- Why does Git use a staging area?
- Why is distributed version control powerful?
- Why are commit messages important?
- What happens if secrets are committed accidentally?

---

## 📚 Next Steps

- Review `resources.md`
- Complete `assignments.md`
- Practice all commands via CLI only