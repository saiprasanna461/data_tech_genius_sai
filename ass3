# User Management API Documentation

## Overview
The User Management API allows users to register, login, and retrieve user information.

**Base URL:** `https://api.example.com/v1`

---

## 1. Register API

### Endpoint Details

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /register | Creates a new user account |

### Request Headers
- Content-Type: application/json

### Request Body

```json
{
  "fullName": "Sai Prasanna",
  "email": "sai@example.com",
  "password": "Password@123"
}
```

### Success Response (201 Created)

```json
{
  "success": true,
  "message": "User registered successfully",
  "userId": 101
}
```

### Error Responses
- 400 Bad Request – Invalid input data
- 409 Conflict – Email already registered

---

## 2. Login API

### Endpoint Details

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /login | Authenticates a user |

### Request Headers
- Content-Type: application/json

### Request Body

```json
{
  "email": "sai@example.com",
  "password": "Password@123"
}
```

### Success Response (200 OK)

```json
{
  "success": true,
  "message": "Login successful",
  "token": "JWT_TOKEN"
}
```

### Error Responses
- 400 Bad Request – Missing fields
- 401 Unauthorized – Invalid credentials

---

## 3. Get User API

### Endpoint Details

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /users/{id} | Retrieves user details |

### Request Headers
- Authorization: Bearer JWT_TOKEN
- Content-Type: application/json

### Success Response (200 OK)

```json
{
  "success": true,
  "data": {
    "id": 101,
    "fullName": "Sai Prasanna",
    "email": "sai@example.com"
  }
}
```

### Error Responses
- 401 Unauthorized – Invalid or missing token
- 404 Not Found – User not found

---

## Authentication Flow

1. Register a user using `/register`
2. Login using `/login`
   - Receive JWT Token
3. Access protected APIs
   - Add `Authorization: Bearer JWT_TOKEN`
4. Retrieve user details using `/users/{id}`

---

## Common Status Codes

| Code | Meaning |
|------|---------|
| 200 | OK |
| 201 | Created |
| 400 | Bad Request |
| 401 | Unauthorized |
| 404 | Not Found |
| 409 | Conflict |
| 500 | Internal Server Error |

## Repository Link

https://github.com/your-username/user-management-api