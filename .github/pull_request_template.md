## 📌 Summary

Briefly describe the purpose of this pull request.

Example:
Adds login validation to prevent empty email submission.

---

## 🎯 Problem Being Solved

What issue or limitation does this PR address?

Example:
Users could submit the login form without entering an email, causing a backend validation error.

---

## 🛠 Changes Made

List the main changes in this PR.

- Added email validation in login form
- Updated error message handling
- Added unit tests for login validation

---

## 🧪 How This Was Tested

Explain how the changes were verified.

- Ran unit tests locally
- Manually tested login form with empty email
- Verified error message appears correctly

---

## ⚠️ Risks / Impact

Are there any potential side effects?

- No database changes
- No API changes
- Only frontend validation added

---

## 📷 Screenshots (Optional)

Add screenshots if UI changes are involved.

---

## 🔍 Review Notes

Anything reviewers should focus on.

Example:
Please review validation logic in `LoginController`.

---

## 📋 Checklist

Before submitting the pull request, confirm the following:

- [ ] Code compiles / runs successfully
- [ ] Tests added or updated where necessary
- [ ] No secrets or credentials committed
- [ ] Commit messages follow project conventions
- [ ] Changes are limited to the scope of this PR