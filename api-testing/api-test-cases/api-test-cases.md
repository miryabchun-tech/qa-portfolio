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
## API Test Cases

### API-001 — Get all posts

**Method:** GET  
**Endpoint:** `/posts`

**Test Data:** None

**Expected Result:**
- Response is returned successfully.
- Response body contains a JSON array.
- Posts contain the expected fields.

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
- Response status and body can be inspected.

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
