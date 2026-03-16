# Assignments – Day 7: How the Web Works

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

These exercises help you observe how the internet works in practice.

You will use networking tools available on your system to explore:

- DNS resolution
- network routing
- server connectivity
- browser network requests

These commands allow engineers to debug real-world connectivity issues.

---

# 🧭 Exercise 1 – DNS Lookup using `nslookup`

DNS converts domain names into IP addresses.

Run the following command:

Mac / Linux / Windows

```
nslookup google.com
```

Example output:

```
Server: 192.168.1.1
Address: 192.168.1.1#53

Non-authoritative answer:
Name: google.com
Address: 142.250.183.206
```

### Observe

- What IP address was returned?
- Which DNS server handled your query?

### Try More Domains

```
nslookup github.com
nslookup amazon.com
nslookup openai.com
```

Notice that each domain resolves to different IP addresses.

---

# 🔍 Exercise 2 – Advanced DNS Lookup using `dig` (Mac/Linux)

`dig` provides detailed DNS resolution information.

Mac / Linux:

```
dig google.com
```

Important sections to observe:

```
QUESTION SECTION
ANSWER SECTION
Query time
SERVER
```

Example:

```
google.com. 300 IN A 142.250.183.206
```

### Questions

- What is the query time?
- Which DNS server responded?

---

# 🌐 Exercise 3 – Trace Internet Route

Your request travels through multiple routers before reaching the destination server.

Trace the route to a website.

Mac / Linux

```
traceroute google.com
```

Windows

```
tracert google.com
```

Example output:

```
1  192.168.1.1
2  10.0.0.1
3  isp-router.net
4  regional-network.net
5  google-network.net
```

### Observe

- How many hops did your request take?
- Which networks handled the request?

Each hop represents a router forwarding your request.

---

# 📡 Exercise 4 – Check Connectivity using `ping`

The `ping` command checks if a server is reachable.

Run:

```
ping google.com
```

Example output:

```
64 bytes from 142.250.183.206: icmp_seq=1 ttl=116 time=14 ms
```

### Observe

- Response time (latency)
- Packet delivery success

### Try Another Website

```
ping github.com
```

Compare latency values.

---

# 🌍 Exercise 5 – Observe Browser Network Requests

Open your browser and inspect network activity.

Steps:

1. Open Chrome / Edge / Firefox
2. Open Developer Tools

Mac

```
Cmd + Option + I
```

Windows

```
Ctrl + Shift + I
```

3. Go to **Network Tab**
4. Visit a website

Example:

```
https://github.com
```

Observe:

- multiple network requests
- CSS
- JavaScript
- images
- API calls

### Questions

- How many requests were made to load the page?
- What type of resources were downloaded?

---

# 🔎 Exercise 6 – Inspect DNS Propagation

Visit:

```
https://www.whatsmydns.net/
```

Enter a domain such as:

```
google.com
```

Observe:

- how DNS resolves from different locations worldwide.

This demonstrates how DNS operates globally.

---

# 🧠 Exercise 7 – Trace a Website's IP

Run:

```
nslookup github.com
```

Copy the IP address returned.

Then run:

```
ping <ip-address>
```

Example:

```
ping 140.82.113.3
```

You are now directly communicating with the server's IP.

---

# 🧩 Practical Thinking

Create a file called:

```
network-observations.md
```

Write answers to the following:

1. What IP address did `google.com` resolve to?
2. How many hops did `traceroute` show?
3. What was the average latency when using `ping`?
4. How many requests were loaded when opening a website in the browser?
5. What surprised you most while exploring these tools?

Commit the file in a small practice repository.

---

# 📋 Self-Evaluation Checklist

- [ ] Performed DNS lookup using `nslookup`
- [ ] Explored detailed DNS output using `dig`
- [ ] Traced network route using `traceroute`
- [ ] Measured latency using `ping`
- [ ] Inspected network requests in browser developer tools
- [ ] Observed global DNS propagation

---

# 🚀 Optional Challenge (Advanced)

Choose a website such as:

```
amazon.com
netflix.com
github.com
```

Perform the following:

1. Resolve the domain using `nslookup`
2. Trace its route using `traceroute`
3. Measure latency using `ping`
4. Inspect its network requests using browser developer tools

Write a short report explaining how your request traveled across the internet.

---

> Great engineers understand not only how to write code but also how their systems communicate across the network.

---

## 🧭 Navigation

← **Previous: Resources**  
[Resources](./resources.md)

➡ **Next Lesson**  
[Day 8](../day-08/README.md)