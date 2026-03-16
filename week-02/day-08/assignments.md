# Assignments – Day 8: HTTP Fundamentals

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

These exercises help you explore how HTTP works in real systems.

You will use command-line tools and browser developer tools to:

- send HTTP requests
- inspect responses
- analyze HTTP headers
- observe HTTP status codes
- inspect HTTPS certificates

These tools are commonly used by engineers when debugging production systems.

---

# 🧪 Exercise 1 – Send Your First HTTP Request using curl

`curl` is a command-line tool used to send HTTP requests.

Run the following command in your terminal.

Mac / Linux / Windows

```
curl https://httpbin.org/get
```

Example response:

```
{
  "args": {},
  "headers": {
    "Host": "httpbin.org",
    "User-Agent": "curl/7.79"
  },
  "origin": "your-ip-address",
  "url": "https://httpbin.org/get"
}
```

### Observe

- response body
- headers returned by the server
- your public IP address

---

# 📄 Exercise 2 – Inspect HTTP Headers

HTTP responses contain metadata called **headers**.

Run:

```
curl -I https://google.com
```

Example output:

```
HTTP/2 200
content-type: text/html
cache-control: private
server: gws
```

### Questions

- What status code did the server return?
- What is the value of `content-type`?
- Which server software responded?

---

# 🔍 Exercise 3 – Trigger a 404 Status Code

Send a request for a resource that does not exist.

```
curl -I https://httpbin.org/status/404
```

Expected response:

```
HTTP/1.1 404 NOT FOUND
```

### Try other status codes

```
curl -I https://httpbin.org/status/200
curl -I https://httpbin.org/status/500
```

Observe how servers communicate errors using HTTP status codes.

---

# 📨 Exercise 4 – Send a POST Request

Send a POST request with data.

```
curl -X POST https://httpbin.org/post \
-d "username=testuser"
```

Observe the response showing the request body received by the server.

### Questions

- What HTTP method was used?
- Where is the submitted data shown in the response?

---

# 🔐 Exercise 5 – Inspect HTTPS Certificate

Open a browser and visit:

```
https://github.com
```

Click the **lock icon 🔒** in the browser address bar.

Inspect:

- certificate issuer
- validity period
- encryption protocol

### Questions

- Which organization issued the certificate?
- When does the certificate expire?

---

# 🌐 Exercise 6 – Inspect HTTP Requests in Browser

Open a browser and inspect network requests.

Steps:

1. Open **Developer Tools**

Mac:

```
Cmd + Option + I
```

Windows:

```
Ctrl + Shift + I
```

2. Open the **Network Tab**

3. Visit a website:

```
https://github.com
```

### Observe

- number of requests
- HTTP methods used
- response status codes
- response sizes

Click any request and inspect:

- headers
- response body
- request method

---

# 🔄 Exercise 7 – Observe Redirects

Run the following command:

```
curl -I http://google.com
```

You will likely see:

```
HTTP/1.1 301 Moved Permanently
```

This shows that the website redirects HTTP traffic to HTTPS.

Follow redirects automatically:

```
curl -L http://google.com
```

---

# 🌍 Exercise 8 – Explore HTTP with an Online Tool

Open:

```
https://httpbin.org/
```

Try the following endpoints in your browser:

```
https://httpbin.org/get
https://httpbin.org/status/200
https://httpbin.org/status/404
https://httpbin.org/headers
```

Observe how different HTTP responses behave.

---

# 🧠 Practical Thinking

Create a file:

```
http-observations.md
```

Answer the following:

1. What HTTP status code did `google.com` return?
2. What headers were returned by `httpbin.org`?
3. What happens when you request a missing resource?
4. What HTTP method is used when opening a webpage?
5. What differences did you observe between HTTP and HTTPS requests?

Commit your observations to a practice repository.

---

# 📋 Self-Evaluation Checklist

- [ ] Sent HTTP request using `curl`
- [ ] Inspected HTTP headers
- [ ] Observed HTTP status codes
- [ ] Sent POST request with data
- [ ] Inspected HTTPS certificate in browser
- [ ] Observed network requests in developer tools
- [ ] Explored HTTP endpoints using httpbin

---

# 🚀 Optional Challenge (Advanced)

Use `curl` to fetch headers from multiple websites.

Example:

```
curl -I https://github.com
curl -I https://amazon.com
curl -I https://openai.com
```

Compare:

- status codes
- response headers
- server identifiers

Write a short summary explaining the differences.

---

> HTTP is the foundation of communication on the web. Understanding how requests and responses work helps engineers debug systems, analyze APIs, and build reliable services.

---

## 🧭 Navigation

← Previous: Resources  
[Resources](./resources.md)

➡ Next Lesson  
[Day 9](../day-09/README.md)