# Assignments – Day 9: Data Formats

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

## 📌 Overview

These exercises help you understand how structured data formats are used in real systems.

You will work with:

- JSON
- XML
- CSV

The goal is to learn how data is structured, validated, and exchanged between systems.

---

# 🧠 Part 1 – Conceptual Understanding

Answer the following in your own words.

1. What is a data format?
2. Why do software systems use standardized data formats?
3. What advantages does JSON have compared to XML?
4. Why is CSV useful for analytics and reporting?
5. In what scenarios might XML still be preferred over JSON?

---

# 🧩 Part 2 – Design a Nested JSON Object

Create a JSON document representing an **E-commerce Order**.

The structure should include:

- order information
- customer details
- shipping address
- list of products
- payment information

Example fields to include:

- orderId
- orderDate
- customer
- products
- payment
- totalAmount

Your JSON should include **at least two products** in the order.

Example structure (expand and complete it):

```json
{
  "orderId": "ORD-1001",
  "orderDate": "2026-03-10",
  "customer": {
    "name": "Alice Johnson",
    "email": "alice@example.com"
  },
  "products": [
    {
      "productId": "P100",
      "name": "Laptop",
      "price": 1200
    }
  ]
}
```

### Requirements

- Include nested objects
- Include arrays
- Include at least **3 levels of nesting**

---

# 🔄 Part 3 – Convert JSON to XML

Convert your JSON order structure into **XML format**.

Example conversion pattern:

JSON

```json
{
  "name": "Alice",
  "age": 28
}
```

XML equivalent

```xml
<user>
  <name>Alice</name>
  <age>28</age>
</user>
```

Your XML should represent:

- customer
- order details
- products list
- payment information

Make sure XML tags clearly represent the data.

---

# 📊 Part 4 – Work With CSV Data

Create a CSV file representing **product inventory**.

Your CSV should contain at least **8 records**.

Example structure:

```
product_id,product_name,category,price,stock_quantity
P101,Laptop,Electronics,1200,15
P102,Smartphone,Electronics,800,30
P103,Headphones,Accessories,150,50
```

### Requirements

- Include at least **5 columns**
- Include at least **8 rows**
- Use realistic product data

---

# 🔧 Part 5 – Validate JSON

Take the following **invalid JSON** and fix the errors.

Broken JSON:

```json
{
"name": "Alice"
"age": 28,
"email": "alice@example.com",
}
```

Tasks:

1. Identify the syntax errors.
2. Correct the JSON.
3. Validate it using a JSON formatter tool.

---

# 🌐 Part 6 – Explore Real API JSON

Open the following endpoint in your browser:

```
https://jsonplaceholder.typicode.com/users
```

Observe the JSON response.

Answer:

1. How many user records are returned?
2. What fields exist inside each user object?
3. Is there nested JSON inside the response?

Write your observations.

---

# 🧪 Part 7 – Format and Visualize Data

Use the tools from the resources page.

Try the following:

### JSON Formatter

Paste your JSON order object and format it.

### XML Viewer

Paste your XML conversion and visualize the structure.

### CSV Viewer

Upload your CSV file and inspect the tabular data.

Observe how each format represents data differently.

---

# 🧠 Part 8 – Comparison Exercise

Create a comparison table between **JSON, XML, and CSV**.

Include the following columns:

| Format | Structure | Human Readability | Typical Use Cases |
|------|------|------|------|

Fill the table with your observations.

---

# 📋 Self-Evaluation Checklist

- [ ] I created a nested JSON object
- [ ] I converted JSON to XML
- [ ] I created a CSV dataset
- [ ] I fixed broken JSON syntax
- [ ] I explored a real API JSON response
- [ ] I visualized data using formatter tools
- [ ] I compared different data formats

---

# 🚀 Optional Challenge (Advanced)

Design a **User Management API response** using JSON.

The response should include:

- users
- roles
- permissions
- last login timestamp

Example fields:

- userId
- username
- role
- permissions
- accountStatus

Make the JSON structure **clean and realistic**.

---

> Data formats are the foundation of system communication. Engineers must understand how data is structured before designing APIs and distributed systems.

---

## 🧭 Navigation

← Previous: Resources  
[Resources](./resources.md)

➡ Next Lesson  
[Day 10](../day-10/README.md)