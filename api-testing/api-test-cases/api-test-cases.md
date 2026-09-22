# API Test Cases

## Project

**API:** JSONPlaceholder  
**Base URL:** https://jsonplaceholder.typicode.com  
**Testing Tool:** Postman  
**Test Type:** API Testing

## API Source

For API testing, we use **JSONPlaceholder**, a public fake REST API created for testing and prototyping.

The API is available at:

`https://jsonplaceholder.typicode.com`

Unlike the SauceDemo application used for manual UI testing, JSONPlaceholder is used specifically for practicing REST API testing.

## What We Test

For this project, we use the following JSONPlaceholder resources:

- `/posts`
- `/users`
- `/comments`

We test the following HTTP methods:

- GET
- POST
- PUT
- PATCH
- DELETE

## Test Data

For existing resources, we use data provided by JSONPlaceholder.

Examples:

- `/posts/1`
- `/users/1`
- `/comments?postId=1`

For POST, PUT and PATCH requests, we send our own test data.

Example POST data:

```json
{
  "title": "QA API Test",
  "body": "Testing POST request",
  "userId": 1
}
```

---

# API Test Cases

## GET Requests

### API-001 — Get all posts

**Method:** GET  
**Endpoint:** `/posts`  
**Test Data:** None

**Expected Result:**
- Response is returned successfully.
- Response body contains a JSON array.
- Each post contains the expected fields.

**Status:** Not Run

---

### API-002 — Get post by ID

**Method:** GET  
**Endpoint:** `/posts/1`  
**Test Data:** Existing post ID `1`

**Expected Result:**
- Response is returned successfully.
- Response contains a post object.
- Response contains `userId`, `id`, `title`, and `body`.
- Returned `id` corresponds to the requested post.

**Status:** Not Run

---

### API-003 — Get non-existing post

**Method:** GET  
**Endpoint:** `/posts/9999`  
**Test Data:** Non-existing post ID `9999`

**Expected Result:**
- API handles the request according to its documented behavior.
- Response status and body are inspected.

**Status:** Not Run

---

### API-004 — Get posts by user ID

**Method:** GET  
**Endpoint:** `/posts?userId=1`  
**Test Data:** `userId=1`

**Expected Result:**
- Response is returned successfully.
- Response contains a JSON array.
- Returned posts correspond to the requested user.

**Status:** Not Run

---

### API-005 — Get comments by post ID

**Method:** GET  
**Endpoint:** `/comments?postId=1`  
**Test Data:** `postId=1`

**Expected Result:**
- Response is returned successfully.
- Response contains a JSON array.
- Returned comments are related to post `1`.

**Status:** Not Run

---

## POST Requests

### API-006 — Create a new post

**Method:** POST  
**Endpoint:** `/posts`

**Test Data:**

```json
{
  "title": "QA API Test",
  "body": "Testing POST request",
  "userId": 1
}
```

**Expected Result:**
- Request is processed successfully.
- Response contains the submitted data.
- Response contains an `id`.

**Status:** Not Run

---

### API-007 — Verify POST response fields

**Method:** POST  
**Endpoint:** `/posts`

**Test Data:**

```json
{
  "title": "QA API Test",
  "body": "Testing POST request",
  "userId": 1
}
```

**Expected Result:**
- Response contains `title`.
- Response contains `body`.
- Response contains `userId`.
- Response contains `id`.
- Returned values correspond to the submitted data.

**Status:** Not Run

---

### API-008 — Create post with empty body

**Method:** POST  
**Endpoint:** `/posts`

**Test Data:**

```json
{}
```

**Expected Result:**
- API handles the request according to its documented behavior.
- Response status and body are inspected.

**Status:** Not Run

---

## PUT Requests

### API-009 — Update existing post

**Method:** PUT  
**Endpoint:** `/posts/1`

**Test Data:**

```json
{
  "id": 1,
  "title": "Updated QA Test",
  "body": "Testing PUT request",
  "userId": 1
}
```

**Expected Result:**
- Request is processed successfully.
- Response contains the updated data.
- Returned `id` corresponds to the requested post.

**Status:** Not Run

---

### API-010 — Update non-existing post

**Method:** PUT  
**Endpoint:** `/posts/9999`

**Test Data:**

```json
{
  "id": 9999,
  "title": "Updated Test",
  "body": "Testing non-existing resource",
  "userId": 1
}
```

**Expected Result:**
- API handles the request according to its documented behavior.
- Response status and body are inspected.

**Status:** Not Run

---

## PATCH Requests

### API-011 — Update post title

**Method:** PATCH  
**Endpoint:** `/posts/1`

**Test Data:**

```json
{
  "title": "Updated Title"
}
```

**Expected Result:**
- Request is processed successfully.
- Response contains the updated title.

**Status:** Not Run

---

### API-012 — Update post body

**Method:** PATCH  
**Endpoint:** `/posts/1`

**Test Data:**

```json
{
  "body": "Updated post body"
}
```

**Expected Result:**
- Request is processed successfully.
- Response contains the updated body.

**Status:** Not Run

---

## DELETE Requests

### API-013 — Delete existing post

**Method:** DELETE  
**Endpoint:** `/posts/1`  
**Test Data:** Existing post ID `1`

**Expected Result:**
- Request is processed successfully.
- Response is returned according to JSONPlaceholder behavior.

**Status:** Not Run

---

### API-014 — Delete non-existing post

**Method:** DELETE  
**Endpoint:** `/posts/9999`  
**Test Data:** Non-existing post ID `9999`

**Expected Result:**
- API handles the request according to its documented behavior.
- Response status and body are inspected.

**Status:** Not Run

---

## Users

### API-015 — Get user by ID

**Method:** GET  
**Endpoint:** `/users/1`  
**Test Data:** Existing user ID `1`

**Expected Result:**
- Response is returned successfully.
- Response contains a user object.
- Response contains expected user information such as `id`, `name`, `username`, and `email`.

**Status:** Not Run

---

### API-016 — Get non-existing user

**Method:** GET  
**Endpoint:** `/users/9999`  
**Test Data:** Non-existing user ID `9999`

**Expected Result:**
- API handles the request according to its documented behavior.
- Response status and body are inspected.

**Status:** Not Run

---

## Comments

### API-017 — Get comments for a post

**Method:** GET  
**Endpoint:** `/posts/1/comments`  
**Test Data:** Post ID `1`

**Expected Result:**
- Response is returned successfully.
- Response contains a JSON array.
- Returned comments are related to post `1`.

**Status:** Not Run

---

## Response Validation

### API-018 — Verify Content-Type header

**Method:** GET  
**Endpoint:** `/posts/1`  
**Test Data:** Existing post ID `1`

**Expected Result:**
- Response contains a `Content-Type` header.
- Response is returned as JSON.

**Status:** Not Run

---

### API-019 — Verify response structure

**Method:** GET  
**Endpoint:** `/posts/1`  
**Test Data:** Existing post ID `1`

**Expected Result:**

Response contains the following fields:

- `userId`
- `id`
- `title`
- `body`

**Status:** Not Run

---

### API-020 — Verify ID data type

**Method:** GET  
**Endpoint:** `/posts/1`  
**Test Data:** Existing post ID `1`

**Expected Result:**
- `id` field is present.
- `id` is returned as a number.

**Status:** Not Run

---

### API-021 — Verify POST response structure

**Method:** POST  
**Endpoint:** `/posts`

**Test Data:**

```json
{
  "title": "QA API Test",
  "body": "Testing POST request",
  "userId": 1
}
```

**Expected Result:**
- Response is valid JSON.
- Response contains the submitted fields.
- Response contains an `id`.

**Status:** Not Run

---

## Query Parameters

### API-022 — Filter posts by user ID

**Method:** GET  
**Endpoint:** `/posts?userId=2`  
**Test Data:** `userId=2`

**Expected Result:**
- Response is returned successfully.
- Response contains a JSON array.
- Returned posts correspond to `userId=2`.

**Status:** Not Run

---

## Negative Testing

### API-023 — Request invalid endpoint

**Method:** GET  
**Endpoint:** `/invalid-endpoint`  
**Test Data:** Invalid endpoint

**Expected Result:**
- API handles the invalid endpoint according to its documented behavior.
- Response status and body are inspected.

**Status:** Not Run

---

### API-024 — Request post using invalid ID format

**Method:** GET  
**Endpoint:** `/posts/abc`  
**Test Data:** Invalid ID `abc`

**Expected Result:**
- API handles the invalid ID according to its documented behavior.
- Response status and body are inspected.

**Status:** Not Run

---

## Performance

### API-025 — Verify response time

**Method:** GET  
**Endpoint:** `/posts/1`  
**Test Data:** Existing post ID `1`

**Expected Result:**
- Response is returned within an acceptable response time.
- Actual response time is recorded in Postman.

**Status:** Not Run

---

# HTTP Method Coverage

| HTTP Method | Resource | Covered |
|---|---|---|
| GET | `/posts` | Yes |
| GET | `/users` | Yes |
| GET | `/comments` | Yes |
| POST | `/posts` | Yes |
| PUT | `/posts` | Yes |
| PATCH | `/posts` | Yes |
| DELETE | `/posts` | Yes |

# Validation Coverage

The test suite covers:

- Positive scenarios
- Negative scenarios
- HTTP status codes
- Response body validation
- JSON structure validation
- Data type validation
- Response header validation
- Query parameter validation
- Request body validation
- CRUD operations
- Invalid endpoints
- Invalid resource IDs
- Response time

# Test Execution

**Total Test Cases:** 25  
**Passed:** 0  
**Failed:** 0  
**Blocked:** 0  
**Not Run:** 25

The test cases will be executed using **Postman**.

Actual PASS/FAIL results will be added after executing the requests and validating the responses.

# Important Note

JSONPlaceholder is a **public fake REST API** intended for testing and prototyping.

The API provides sample resources such as posts, users, and comments.

Write operations such as POST, PUT, PATCH, and DELETE are simulated and are not intended to provide persistent database changes.

Therefore, API test results must be based on the actual responses received from JSONPlaceholder during Postman execution.
