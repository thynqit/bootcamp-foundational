# User APIs – REST API Specification

> Part of the Thynqit Labs – Foundational Engineering Bootcamp

---

# Overview

This document describes the REST APIs used for managing **Users** in the system.

These APIs follow standard **REST principles** and support the following operations:

- Create a user
- Retrieve users
- Retrieve a specific user
- Update a user
- Partially update a user
- Delete a user

---

# Base URL

```
https://api.example.com/api/{api_version}
```

Example

```
https://api.example.com/api/v1
```

---

# Authentication

All APIs require authentication using a **Bearer Token**.

Example header:

```
Authorization: Bearer {access_token}
```

---

# Standard Headers

| Header | Required | Description |
|------|------|------|
| Authorization | Yes | Bearer access token |
| Content-Type | Yes | application/json |

---

# Standard Error Format

All APIs return errors in the following format.

```json
{
  "status": "failure",
  "code": "APP_ERROR_CODE",
  "message": "HUMAN_READABLE_MESSAGE",
  "data": {}
}
```

---

# Pagination Format

List APIs follow this response structure:

```json
{
  "page": 1,
  "limit": 20,
  "total": 100,
  "data": []
}
```

---

# API Index

| # | API | Method | Endpoint | Description |
|---|---|---|---|---|
| 1 | Create User | POST | `/users` | Create a new user |
| 2 | Get All Users | GET | `/users` | Retrieve all users |
| 3 | Get User By ID | GET | `/users/{user_id}` | Retrieve user by ID |
| 4 | Update User | PUT | `/users/{user_id}` | Replace user details |
| 5 | Patch User | PATCH | `/users/{user_id}` | Partially update user |
| 6 | Delete User | DELETE | `/users/{user_id}` | Delete user |

---

# API Specifications

---

<details>
<summary><b>1. Create User</b></summary>

## Description

Creates a new user in the system.

---

## Endpoint

```
POST /users
```

---

## Request Headers

| Header | Value |
|------|------|
| Authorization | Bearer {token} |
| Content-Type | application/json |

---

## Request Body

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@example.com",
  "phone": "+919876543210",
  "status": "active"
}
```

---

## Request Body Schema

| Field | Type | Required | Description |
|------|------|------|------|
| firstName | string | Yes | User's first name |
| lastName | string | Yes | User's last name |
| email | string | Yes | User email address |
| phone | string | No | User phone number |
| status | string | Yes | User status (active/inactive) |

---

## Example Request

```bash
curl -X POST https://api.example.com/api/v1/users \
-H "Authorization: Bearer TOKEN" \
-H "Content-Type: application/json" \
-d '{
"firstName": "John",
"lastName": "Doe",
"email": "john@example.com",
"phone": "+919876543210",
"status": "active"
}'
```

---

## Success Response

```json
{
  "status": "success",
  "code": 1001,
  "message": "User created successfully.",
  "data": {
    "id": "usr_101",
    "firstName": "John",
    "lastName": "Doe",
    "email": "john@example.com",
    "phone": "+919876543210",
    "status": "active",
    "createdAt": "2026-03-13T10:00:00Z"
  }
}
```

---

## Error Response

```json
{
  "status": "failure",
  "code": 1051,
  "message": "First name is missing in the request.",
  "data": {}
}
```

---

## Response Body Schema

| Field | Type | Description |
|------|------|------|
| status | string | Status of API execution (success/failure) |
| code | Integer | Application Codes, to be used by client apps for localization |
| message | string | Human readable message, for developers |
| id | string | Unique ID of the user created |
| firstName | string | User's first name |
| lastName | string | User's last name |
| email | string | User email address |
| phone | string | User phone number |
| status | string | User status (active/inactive) |
| createdAt | timestamp | Timestamp when user was created |

---

## HTTP Response Codes

| Code | Meaning |
|-----|------|
| 201 | User created successfully |
| 400 | Bad request |
| 401 | Unauthorized |
| 500 | Internal server error |

---

## Application Response Codes

| Code | Meaning |
|-----|------|
| 1001 | User created successfully |
| 1051 | First name is missing in the request |
| 1052 | Last name is missing in the request |
| 1053 | Email address is missing in the request |

</details>

---

<details>
<summary><b>2. Get All Users</b></summary>

## Description

Returns a paginated list of users.

---

## Endpoint

```
GET /users?page={page_number}&limit={page_limit}
```

---

## Request Headers

| Header | Value |
|------|------|
| Authorization | Bearer {token} |
| Content-Type | application/json |

---

## Query Parameters

| Parameter | Type | Required | Description |
|------|------|------|------|
| page | integer | No | Page number |
| limit | integer | No | Number of results per page |

---

## Example Request

```bash
curl -X GET "https://api.example.com/api/v1/users?page=1&limit=20" \
-H "Authorization: Bearer TOKEN"
```

---

## Success Response

```json
{
  "status": "success",
  "code": 1002,
  "message": "Users retrieved successfully.",
  "data": {
    "page": 1,
    "limit": 20,
    "total": 100,
    "data": [
      {
        "id": "usr_101",
        "firstName": "John",
        "lastName": "Doe",
        "email": "john@example.com"
      }
    ]
  }
}
```

---

## Error Response

```json
{
  "status": "failure",
  "code": 1061,
  "message": "Failed to fetch list of users.",
  "data": {}
}
```

---

## Response Body Schema

| Field | Type | Description |
|------|------|------|
| status | string | Status of API execution (success/failure) |
| code | Integer | Application Codes, to be used by client apps for localization |
| message | string | Human readable message, for developers |
| page | Integer | Current page number |
| limit | Integer | Number of results per page |
| total | Integer | Total number of results |
| id | string | Unique ID of the user created |
| firstName | string | User's first name |
| lastName | string | User's last name |
| email | string | User email address |

---

## HTTP Response Codes

| Code | Meaning |
|-----|------|
| 200 | Success |
| 401 | Unauthorized |
| 500 | Internal server error |

---

## Application Response Codes

| Code | Meaning |
|-----|------|
| 1002 | Users retrieved successfully |
| 1061 | Failed to fetch list of users |

</details>

---

<details>
<summary><b>3. Get User By ID</b></summary>

## Description

Returns a specific user.

---

## Endpoint

```
GET /users/{user_id}
```

---

## Request Headers

| Header | Value |
|------|------|
| Authorization | Bearer {token} |
| Content-Type | application/json |

---

## Path Parameters

| Parameter | Type | Required | Description |
|------|------|------|------|
| user_id | string | Yes | Unique ID of the user to be fetched |

---

## Example Request

```bash
curl -X GET https://api.example.com/api/v1/users/usr_101 \
-H "Authorization: Bearer TOKEN"
```

---

## Success Response

```json
{
  "status": "success",
  "code": 1003,
  "message": "User retrieved successfully.",
  "data": {
    "id": "usr_101",
    "firstName": "John",
    "lastName": "Doe",
    "email": "john@example.com",
    "phone": "+919876543210",
    "status": "active"
  }
}
```

---

## Error Response

```json
{
  "status": "failure",
  "code": 1062,
  "message": "User not found.",
  "data": {}
}
```
---

## Response Body Schema

| Field | Type | Description |
|------|------|------|
| status | string | Status of API execution (success/failure) |
| code | Integer | Application Codes, to be used by client apps for localization |
| message | string | Human readable message, for developers |
| id | string | Unique ID of the user created |
| firstName | string | User's first name |
| lastName | string | User's last name |
| email | string | User email address |
| phone | string | User phone number |
| status | string | User status (active/inactive) |

---

## HTTP Response Codes

| Code | Meaning |
|-----|------|
| 200 | Success |
| 404 | User not found |
| 500 | Internal server error |

---

## Application Response Codes

| Code | Meaning |
|-----|------|
| 1003 | User retrieved successfully |
| 1062 | User not found |

</details>

---

<details>
<summary><b>4. Update User</b></summary>

## Description

Update a specific user.

---

## Endpoint

```
PUT /users/{user_id}
```

---

## Request Headers

| Header | Value |
|------|------|
| Authorization | Bearer {token} |
| Content-Type | application/json |

---

## Path Parameters

| Parameter | Type | Required | Description |
|------|------|------|------|
| user_id | string | Yes | Unique ID of the user to be updated |

---

## Example Request

```bash
curl -X PUT https://api.example.com/api/v1/users/usr_101 \
-H "Authorization: Bearer TOKEN" \
-H "Content-Type: application/json" \
-d '{
  "first_name": "Tom",
  "last_name": "Doe",
  "phone": "+919876543210",
  "status": "active"
}'
```

---

## Request Body

```json
{
  "firstName": "Tom",
  "lastName": "Doe",
  "phone": "+919876543210",
  "status": "active"
}
```

---

## Request Body Schema

| Field | Type | Required | Description |
|------|------|------|------|
| firstName | string | Yes | User's first name to be updated |
| lastName | string | Yes | User's last name to be updated |
| email | string | Yes | User email address to be updated |
| phone | string | No | User phone number to be updated |
| status | string | Yes | User status (active/inactive) to be updated |

---

## Success Response

```json
{
  "status": "success",
  "code": 1004,
  "message": "User updated successfully.",
  "data": {
    "id": "usr_101",
    "firstName": "Tom",
    "lastName": "Doe",
    "email": "john@example.com",
    "phone": "+919876543210",
    "status": "active"
  }
}
```

---

## Error Response

```json
{
  "status": "failure",
  "code": 1062,
  "message": "User not found.",
  "data": {}
}
```

---

## Response Body Schema

| Field | Type | Description |
|------|------|------|
| status | string | Status of API execution (success/failure) |
| code | Integer | Application Codes, to be used by client apps for localization |
| message | string | Human readable message, for developers |
| id | string | Unique ID of the user created |
| firstName | string | User's first name |
| lastName | string | User's last name |
| email | string | User email address |
| phone | string | User phone number |
| status | string | User status (active/inactive) |

---

## HTTP Response Codes

| Code | Meaning |
|-----|------|
| 200 | Success |
| 404 | User not found |
| 500 | Internal server error |

---

## Application Response Codes

| Code | Meaning |
|-----|------|
| 1004 | User updated successfully |
| 1062 | User not found |

</details>

---

<details>
<summary><b>5. Patch User</b></summary>

## Description

Partially update a specific user.

---

## Endpoint

```
PATCH /users/{user_id}
```

---

## Request Headers

| Header | Value |
|------|------|
| Authorization | Bearer {token} |
| Content-Type | application/json |

---

## Path Parameters

| Parameter | Type | Required | Description |
|------|------|------|------|
| user_id | string | Yes | Unique ID of the user to be updated |

---

## Example Request

```bash
curl -X PATCH https://api.example.com/api/v1/users/usr_101 \
-H "Authorization: Bearer TOKEN" \
-H "Content-Type: application/json" \
-d '{
  "phone": "+919876543211"
}'
```

---

## Request Body

```json
{
  "phone": "+919876543211"
}
```

---

## Request Body Schema

| Field | Type | Required | Description |
|------|------|------|------|
| firstName | string | Yes | User's first name to be updated |
| lastName | string | Yes | User's last name to be updated |
| email | string | Yes | User email address to be updated |
| phone | string | No | User phone number to be updated |
| status | string | Yes | User status (active/inactive) to be updated |

---

## Success Response

```json
{
  "status": "success",
  "code": 1004,
  "message": "User updated successfully.",
  "data": {}
}
```

---

## Error Response

```json
{
  "status": "failure",
  "code": 1062,
  "message": "User not found.",
  "data": {}
}
```

---

## Response Body Schema

| Field | Type | Description |
|------|------|------|
| status | string | Status of API execution (success/failure) |
| code | Integer | Application Codes, to be used by client apps for localization |
| message | string | Human readable message, for developers |

---

## HTTP Response Codes

| Code | Meaning |
|-----|------|
| 200 | Success |
| 404 | User not found |
| 500 | Internal server error |

## Application Response Codes

| Code | Meaning |
|-----|------|
| 1004 | User updated successfully |
| 1062 | User not found |

</details>

---

<details>
<summary><b>6. Delete User</b></summary>

## Description

Delete a specific user.

---

## Endpoint

```
DELETE /users/{user_id}
```

---

## Request Headers

| Header | Value |
|------|------|
| Authorization | Bearer {token} |
| Content-Type | application/json |

---

## Path Parameters

| Parameter | Type | Required | Description |
|------|------|------|------|
| user_id | string | Yes | Unique ID of the user to be deleted |

---

## Example Request

```bash
curl -X DELETE https://api.example.com/api/v1/users/usr_101 \
-H "Authorization: Bearer TOKEN"
```

---

## Success Response

```json
{
  "status": "success",
  "code": 1005,
  "message": "User deleted successfully.",
  "data": {}
}
```

---

## Error Response

```json
{
  "status": "failure",
  "code": 1062,
  "message": "User not found.",
  "data": {}
}
```

---

## Response Body Schema

| Field | Type | Description |
|------|------|------|
| status | string | Status of API execution (success/failure) |
| code | Integer | Application Codes, to be used by client apps for localization |
| message | string | Human readable message, for developers |

---

## HTTP Response Codes

| Code | Meaning |
|-----|------|
| 204 | User deleted |
| 404 | User not found |
| 500 | Internal server error |

## Application Response Codes

| Code | Meaning |
|-----|------|
| 1005 | User deleted successfully |
| 1062 | User not found |

</details>

---

# Thynqit Labs

**Thynqit Labs – Foundational Engineering Bootcamp**

Building strong engineering foundations through practical system design, APIs, and production-grade development practices.

---