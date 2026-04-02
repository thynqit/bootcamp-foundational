# Assignments – Day 20: Linux CLI for Engineers

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

This assignment focuses on **hands-on CLI usage and basic shell scripting**.

You will:

- navigate systems using CLI
- work with files and logs
- debug using command-line tools
- simulate real production scenarios
- automate tasks using shell scripts

⚠️ This is a **practice-heavy module**. You must execute commands — reading alone is not sufficient.

---

## 🧠 Part 1 – CLI Fundamentals Practice

Perform the following on your system (Mac/Linux/WSL/Cloud VM):

### Tasks:

1. Create a directory:
   ```
   thynqit-cli-practice
   ```

2. Inside it, create:
   - 3 folders: `logs`, `data`, `scripts`
   - 3 files:
     ```
     app.log
     users.txt
     config.env
     ```

3. Add sample data:

   In `app.log`:
   ```
   INFO Server started
   ERROR Database connection failed
   INFO Retry attempt
   ERROR Timeout occurred
   ```

4. Practice commands:

   - List files (`ls`)
   - Navigate directories (`cd`)
   - View file content (`cat`, `less`)
   - Check current directory (`pwd`)

---

## 🔍 Part 2 – Log Analysis (Real Debugging)

Using CLI tools:

1. Find all ERROR logs:
   ```
   grep "ERROR" app.log
   ```

2. Count number of ERROR entries:
   ```
   grep -c "ERROR" app.log
   ```

3. Save ERROR logs to a new file:
   ```
   grep "ERROR" app.log > errors.log
   ```

4. Monitor logs in real-time:
   ```
   tail -f app.log
   ```

---

## 📁 Part 3 – File & Directory Operations

Perform:

- Copy `users.txt` to `data/`
- Rename `config.env` to `app.env`
- Delete a test file safely
- Create nested directories:
  ```
  mkdir -p backups/2026/april
  ```

---

## 🔐 Part 4 – Permissions

1. Create a script file:
   ```
   script.sh
   ```

2. Make it executable:
   ```
   chmod +x script.sh
   ```

3. Verify permissions:
   ```
   ls -l
   ```

---

## 🌐 Part 5 – Networking Commands

Run the following:

1. Check connectivity:
   ```
   ping google.com
   ```

2. Call an API:
   ```
   curl https://jsonplaceholder.typicode.com/posts/1
   ```

3. Download a file:
   ```
   wget https://example.com
   ```

4. Inspect open ports:
   ```
   netstat -an
   ```

---

## ⚙️ Part 6 – Process Management

1. List running processes:
   ```
   ps aux
   ```

2. Run a background process:
   ```
   sleep 1000 &
   ```

3. Kill the process:
   ```
   kill <process-id>
   ```

---

## 📊 Part 7 – System Monitoring

Run:

```
df -h
du -h
free -h
```

Answer:

- What is your available disk space?
- How much memory is being used?

---

## 🔗 Part 8 – Pipes & Redirection

1. Combine commands:

```
cat app.log | grep ERROR
```

2. Save output:

```
ls > files.txt
```

3. Append output:

```
echo "New log entry" >> app.log
```

---

## 🧾 Part 9 – Shell Scripting (Core Assignment)

Create a script:

### `analyze_logs.sh`

```bash
#!/bin/bash

echo "Analyzing logs..."

ERROR_COUNT=$(grep -c "ERROR" app.log)

echo "Total Errors: $ERROR_COUNT"

if [ $ERROR_COUNT -gt 0 ]; then
  echo "Errors detected. Check logs."
else
  echo "System looks healthy."
fi
```

---

### Run Script:

```
chmod +x analyze_logs.sh
./analyze_logs.sh
```

---

## 🧩 Part 10 – Real-World Scenario

### Scenario: Production Issue

You logged into a server and found:

- application is slow
- logs are growing rapidly
- CPU usage is high

### Tasks:

Using CLI, explain how you would:

1. Identify the issue using logs
2. Find heavy processes
3. Kill problematic process
4. Monitor system after fix

Write your steps using actual commands.

---

## 📋 Self-Evaluation Checklist

- [ ] I can navigate directories using CLI
- [ ] I can analyze logs using grep and tail
- [ ] I can manage files and permissions
- [ ] I can run network commands
- [ ] I understand process management basics
- [ ] I created and executed a shell script
- [ ] I can debug basic system issues using CLI

---

## 🚀 Optional Challenge (Advanced)

1. Create a script that:

   - scans all `.log` files
   - extracts ERROR lines
   - stores them in a single file

2. Create a backup script:

   ```
   backup.sh
   ```

   - compress a folder
   - store it with timestamp

3. Extend your script:

   - send output to a file
   - include timestamps

---

## 🧠 Engineering Insight

Great engineers are not just developers — they are operators.

CLI + scripting enables:

- debugging production systems
- automating workflows
- working in cloud environments
- handling real-world incidents

This is where engineering becomes **practical and powerful**.

---

## 🧭 Navigation

← Back to Resources  
[Resources](./resources.md)

➡ Next Module  
[Week 5](../../week-05)