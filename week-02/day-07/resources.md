# Resources – Day 7: How the Web Works

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

These resources explain the infrastructure behind the modern web.

They help learners understand:

- how the internet is structured
- how DNS resolves domain names
- how global network infrastructure operates
- how browsers communicate with servers

Some resources also allow you to **explore the internet visually**, which helps build intuition about how web systems work at global scale.

---

## 📖 Official Documentation & Authoritative Sources

These sources explain the foundational concepts of the web and internet.

- Cloudflare Learning Center – What is the Internet?  
  https://www.cloudflare.com/en-in/learning/network-layer/how-does-the-internet-work/

- Cloudflare Learning Center – What is DNS?  
  https://www.cloudflare.com/learning/dns/what-is-dns/

- Mozilla Web Docs – How the Web Works  
  https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work

These resources explain web infrastructure in a clear and reliable way.

---

## 🎓 Structured Learning Material

High-quality guides explaining how web systems operate.

- IBM – What is DNS?  
  https://www.ibm.com/topics/dns

- AWS – What is DNS?  
  https://aws.amazon.com/route53/what-is-dns/

- Mozilla Web Docs – How the Web Works  
  https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Web_standards/How_the_web_works

These guides explain how modern cloud systems and platforms rely on internet protocols.

---

## 🌍 Curiosity & Exploration Resources

These interactive tools help visualize the infrastructure powering the internet.

### Global Internet Submarine Cables

Explore the physical cables that connect continents.

https://www.submarinecablemap.com/

These cables carry most of the world's internet traffic across oceans.

---

### DNS Propagation Checker

Check how DNS records propagate globally.

https://www.whatsmydns.net/

You can see how different DNS servers resolve the same domain.

---

### Root DNS Servers

Learn about the global root DNS infrastructure.

https://www.iana.org/domains/root/servers

Root servers are the starting point of the DNS resolution process.

---

### Internet Infrastructure Map

Visualize global internet connectivity.

https://www.internetexchangemap.com/

This shows how networks and internet exchange points connect globally.

---

### End-to-End Web Request Journey

This interactive explanation shows what happens when you enter a URL in your browser and how the request travels across the internet to reach a server and return the response.

https://www.youtube.com/watch?v=7_LPdttKXPc

This walkthrough explains:

- DNS resolution
- TCP connection setup
- HTTP request/response
- Server processing
- Browser rendering

It provides a clear mental model of how modern web communication works.

---

### What Happens to Your Request on the Internet?

When multiple devices in the same network send requests to the internet, each request still reaches the correct destination and returns to the correct device.

This works because of:

- IP addresses
- Port numbers
- Network Address Translation (NAT)
- TCP connections

Interactive explanation:

https://www.ipxo.com/blog/what-is-nat/

Key idea:

```
Device A: 192.168.1.10 → google.com
Device B: 192.168.1.11 → youtube.com
```

Even though both devices share the same public internet connection, routers track each request using **port mappings** and **connection tables**.

Example:

```
192.168.1.10:52341 → PublicIP:40001
192.168.1.11:52342 → PublicIP:40002
```

When responses return, the router knows exactly which internal device initiated the request.

This is how hundreds of devices in a home or office network share one public IP address without mixing traffic.

---

### Visualizing Internet Packet Routing

See how packets travel through the internet using tools like traceroute.

Try this on your system:

Mac / Linux

```
traceroute google.com
```

Windows

```
tracert google.com
```

This command shows the intermediate routers your request passes through before reaching the destination server.

This helps illustrate how the internet routes traffic globally.

---

## 🎥 Recommended Videos

Short explanations showing how the internet and web work.

- What Happens When You Type a URL Into a Browser  
  https://www.youtube.com/watch?v=7_LPdttKXPc

- How the Internet Works in 5 Minutes  
  https://www.youtube.com/watch?v=x3c1ih2NJEg

- DNS Explained in 100 Seconds  
  https://www.youtube.com/watch?v=UVR9lhUGAyU

These videos help visualize the journey of a web request.

---

## 📌 Suggested Learning Flow

1. Read Mozilla's explanation of how the web works.
2. Learn the basics of DNS using Cloudflare's learning center.
3. Watch one short video explaining the request lifecycle.
4. Explore the submarine cable map to understand global connectivity.
5. Use a DNS checker to see how domain resolution works worldwide.

> Understanding the infrastructure behind the web helps engineers diagnose network problems and design more resilient systems.

---

## 🧭 Navigation

← **Back to Lesson**  
[Day 7](./README.md)

➡ **Next: Assignments**  
[Assignments](./assignments.md)