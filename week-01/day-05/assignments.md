# Assignments – Day 5: Git Basics (CLI First Approach)

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

This assignment focuses on learning Git through **hands-on practice using the Command Line Interface (CLI)**.

You will practice:

- initializing repositories
- committing changes
- working with Git history
- pushing code to a remote repository
- collaborating using Git

All exercises must be completed **using the terminal / command prompt**, not graphical Git tools.

---

## 🛠 Setup – Install Git

If Git is not installed:

Mac (Homebrew)

```
brew install git
```

Ubuntu / Linux

```
sudo apt install git
```

Windows

Download and install Git from:

https://git-scm.com/downloads

Verify installation:

```
git --version
```

---

## ⚙️ Step 1 – Configure Git

Configure your Git identity.

```
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Verify configuration:

```
git config --list
```

---

## 📁 Step 2 – Create a Local Repository

Create a new project folder.

```
mkdir git-practice
cd git-practice
```

Initialize Git.

```
git init
```

Check repository status.

```
git status
```

---

## ✍️ Step 3 – Create and Commit Your First File

Create a README file.

```
touch README.md
```

Add content inside the file.

Example:

```
# Git Practice Repository
Learning Git through CLI
```

Stage the file.

```
git add README.md
```

Commit the change.

```
git commit -m "feat: add initial README file"
```

Check commit history.

```
git log
```

---

## 📝 Step 4 – Practice Multiple Commits

Add another file.

```
touch notes.txt
```

Add some sample content.

Stage and commit.

```
git add notes.txt
git commit -m "docs: add learning notes file"
```

Modify README.md again.

Commit the change.

```
git add README.md
git commit -m "docs: update repository description"
```

View commit history again.

```
git log --oneline
```

---

## 🚫 Step 5 – Practice `.gitignore`

Create a `.gitignore` file.

```
touch .gitignore
```

Add example entries.

```
node_modules/
.env
build/
```

Create a fake `.env` file.

```
touch .env
```

Run:

```
git status
```

Observe that `.env` is ignored.

Commit `.gitignore`.

```
git add .gitignore
git commit -m "chore: add gitignore file"
```

---

## 🌿 Step 6 – Practice Branching

Create a new branch.

```
git branch feature-profile
```

Switch to the branch.

```
git checkout feature-profile
```

Create a new file.

```
touch profile.txt
```

Commit the change.

```
git add profile.txt
git commit -m "feat: add profile feature placeholder"
```

View branches.

```
git branch
```

---

## ☁️ Step 7 – Push to Remote Repository

Create a repository on **GitHub or Bitbucket**.

Example name:

```
git-cli-practice
```

Add remote repository.

```
git remote add origin <repository-url>
```

Push your code.

```
git push -u origin main
```

Push your feature branch.

```
git push origin feature-profile
```

---

## 🔄 Step 8 – Pull Changes

Make a change in GitHub web editor (edit README).

Then pull changes locally.

```
git pull origin main
```

Verify updates locally.

---

## 🧩 Practical Thinking

Answer the following:

1. What is the difference between `git add` and `git commit`?
2. Why does Git use a staging area?
3. Why should `.env` files never be committed?
4. Why are branches important in collaborative development?

Write answers in a short markdown file:

```
reflection.md
```

Commit the file.

---

## 📋 Self-Evaluation Checklist

- [ ] Git installed and configured
- [ ] Local repository initialized
- [ ] Multiple commits created
- [ ] `.gitignore` configured
- [ ] Feature branch created
- [ ] Code pushed to remote repository
- [ ] Changes pulled from remote
- [ ] Reflection answers written

---

## 🚀 Optional Challenge (Advanced)

Try the following additional exercises.

Create another branch:

```
git checkout -b feature-auth
```

Make changes in both branches and merge them.

```
git checkout main
git merge feature-auth
```

Explore commit history visually:

```
git log --graph --oneline --all
```

---

> Git proficiency is one of the most important engineering skills.  
> Engineers who understand Git deeply collaborate more safely and confidently.

---

## 🧭 Navigation

← **Previous: Resources**  
[Resources](./resources.md)

➡ **Next Module**  
[Week 2](../../week-02/README.md)