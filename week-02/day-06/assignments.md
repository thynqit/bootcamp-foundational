# Assignments – Day 6: Git Branching & Code Review

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

This assignment simulates a **real collaborative Git workflow** used by engineering teams.

You will practice:

- creating feature branches
- pushing code to a remote repository
- opening pull requests
- performing code reviews
- resolving merge conflicts
- merging code safely

All Git operations must be performed using the **Command Line Interface (CLI)** wherever possible.

GitHub or Bitbucket UI may be used **only for pull requests and review steps**.

---

# 🛠 Setup – Create Collaboration Repository

Create a repository on **GitHub or Bitbucket**.

Example repository name:

```
git-collaboration-lab
```

Clone the repository locally.

```
git clone <repository-url>
cd git-collaboration-lab
```

Create a base README.

```
touch README.md
```

Add sample content:

```
# Git Collaboration Lab
Practicing branching, pull requests, and merge workflows
```

Commit the change.

```
git add README.md
git commit -m "docs: add base project README"
git push origin main
```

---

# 🌿 Exercise 1 – Feature Branch Development

Create a new branch.

```
git checkout -b feature-login
```

Create a file.

```
touch login.txt
```

Add content describing login functionality.

Stage and commit.

```
git add login.txt
git commit -m "feat: add login feature placeholder"
```

Push the branch.

```
git push origin feature-login
```

---

# 🔀 Exercise 2 – Create Pull Request

Using GitHub or Bitbucket:

1. Open your repository
2. Navigate to **Pull Requests**
3. Create a **Pull Request**

Example:

```
feature-login → main
```

Add description:

```
Adds initial login feature placeholder.
```

Do not merge yet.

---

# 🧑‍💻 Exercise 3 – Code Review Simulation

Open the pull request.

Simulate a review by adding comments such as:

Example comments:

```
Can we expand this file with login validation details?
```

```
Please follow commit message conventions.
```

```
Consider separating authentication logic later.
```

Add at least **two review comments**.

---

# ⚠️ Exercise 4 – Generate a Merge Conflict

We will now intentionally create a conflict.

### Step 1 – Modify File in Main Branch

Switch to main.

```
git checkout main
```

Edit `README.md`.

Add a line:

```
This project demonstrates Git collaboration workflows.
```

Commit and push.

```
git add README.md
git commit -m "docs: update project description"
git push origin main
```

---

### Step 2 – Modify Same File in Feature Branch

Switch back.

```
git checkout feature-login
```

Edit the **same line in README.md** differently.

Example:

```
This repository is used to practice Git pull requests.
```

Commit the change.

```
git add README.md
git commit -m "docs: update README description"
git push origin feature-login
```

---

# ⚔️ Exercise 5 – Merge Conflict Resolution

Now attempt to merge.

```
git checkout main
git pull origin main
git merge feature-login
```

Git will report a **merge conflict**.

Open the conflicted file.

You will see:

```
<<<<<<< HEAD
This project demonstrates Git collaboration workflows.
=======
This repository is used to practice Git pull requests.
>>>>>>> feature-login
```

Resolve the conflict manually.

Example final version:

```
This repository demonstrates Git collaboration workflows and pull request practice.
```

Stage and commit.

```
git add README.md
git commit -m "fix: resolve merge conflict in README"
```

Push changes.

```
git push origin main
```

---

# 🔄 Exercise 6 – Complete Pull Request

Return to GitHub or Bitbucket.

You should now be able to **merge the pull request**.

Merge using:

```
Merge Pull Request
```

After merging, delete the branch.

---

# 🔍 Exercise 7 – Inspect Git History

Run the following command.

```
git log --graph --oneline --all
```

Observe:

- branch structure
- merge commit
- commit history

---

# 🧩 Practical Reflection

Create a file:

```
reflection.md
```

Answer briefly:

1. Why should teams avoid committing directly to `main`?
2. Why are pull requests important?
3. What caused the merge conflict?
4. How did Git help resolve it safely?

Commit the file.

---

# 📋 Self-Evaluation Checklist

- [ ] Repository created on GitHub or Bitbucket
- [ ] Feature branch created
- [ ] Pull request opened
- [ ] Code review comments added
- [ ] Merge conflict generated
- [ ] Conflict resolved via CLI
- [ ] Pull request merged
- [ ] Git history inspected

---

# 🚀 Optional Challenge (Advanced)

Simulate collaboration between **two developers**.

Have a second person:

1. Clone the repository
2. Create a new feature branch
3. Push changes
4. Open a pull request
5. Perform mutual code reviews

---

> Professional engineering requires disciplined collaboration.  
> Git branching and code review are fundamental practices in modern software teams.

---

## 🧭 Navigation

← **Previous: Resources**  
[Resources](./resources.md)

➡ **Next Lesson**  
[Day 7](../day-07/README.md)