# API Testing with Postman

API testing project created using Postman and the public JSONPlaceholder REST API.

The project demonstrates practical API testing skills including request execution, HTTP status code validation, response body validation, JSON structure validation, request parameters, request bodies, negative testing, and automated assertions.

---

## API Under Test

**API:** JSONPlaceholder

**Base URL:** `https://jsonplaceholder.typicode.com`

JSONPlaceholder is a public fake REST API designed for testing and learning purposes.

---

## Testing Tool

- Postman
- JavaScript assertions in Postman Tests
- REST API
- JSON

---

## Testing Scope

The API testing covers:

- GET requests
- POST requests
- PUT requests
- PATCH requests
- DELETE requests
- Path parameters
- Query parameters
- Multiple query parameters
- Request body validation
- Response body validation
- JSON structure validation
- HTTP status code validation
- Positive scenarios
- Negative scenarios
- Automated API assertions
- Collection Runner execution
- Test result reporting

---

## API Resources

The following JSONPlaceholder resources were tested:

- `/posts`
- `/users`
- `/comments`

---

## HTTP Methods Tested

| Method | Purpose |
|---|---|
| GET | Retrieve resources |
| POST | Create resources |
| PUT | Update a resource |
| PATCH | Partially update a resource |
| DELETE | Delete a resource |

---

## Postman Collection

The project includes a Postman collection containing **25 API requests**.

The collection is available here:

[`JSONPlaceholder-API-Collection.json`](./JSONPlaceholder-API-Collection.json)

---

## API Test Cases

Detailed API test cases are documented separately:

[`API Test Cases`](../api-test-cases/api-test-cases.md)

The test cases cover:

- retrieving posts
- retrieving users
- retrieving comments
- invalid resource IDs
- filtering resources
- creating posts
- updating posts
- deleting posts
- path parameters
- query parameters
- request bodies
- response validation
- JSON structure validation
- HTTP status code validation

---

## Automated Assertions

The Postman collection uses automated assertions to validate API responses.

### HTTP Status Code Validation

Checks whether the API returns the expected HTTP status code.

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

### JSON Array Validation

Checks whether the response body contains a JSON array.

```javascript
pm.test("Response is a JSON array", function () {
    pm.expect(pm.response.json()).to.be.an("array");
});
```

### Response Field Validation

Checks whether the response contains the expected fields.

```javascript
pm.test("Response contains expected fields", function () {
    const data = pm.response.json();

    ["id", "title", "body", "userId"].forEach(function (field) {
        pm.expect(data).to.have.property(field);
    });
});
```

### Response Value Validation

Checks whether a response field contains the expected value.

```javascript
pm.test("Response contains post ID 1", function () {
    pm.expect(pm.response.json().id).to.eql(1);
});
```

### Response Structure Validation

Checks whether the response has the expected JSON structure.

```javascript
pm.test("Post contains required fields", function () {
    const data = pm.response.json();

    pm.expect(data).to.have.property("userId");
    pm.expect(data).to.have.property("id");
    pm.expect(data).to.have.property("title");
    pm.expect(data).to.have.property("body");
});
```

### Query Parameter Validation

Checks whether returned resources match the requested query parameter.

```javascript
pm.test("All returned posts belong to userId 1", function () {
    pm.response.json().forEach(function (post) {
        pm.expect(post.userId).to.eql(1);
    });
});
```

### Response Collection Validation

Checks the contents of multiple objects returned in an array.

```javascript
pm.test("All comments belong to postId 1", function () {
    pm.response.json().forEach(function (comment) {
        pm.expect(comment.postId).to.eql(1);
    });
});
```

### Response Length Validation

Checks the number of returned resources.

```javascript
pm.test("Response contains no more than 3 comments", function () {
    pm.expect(pm.response.json().length).to.be.at.most(3);
});
```

### Assertion Coverage

The collection includes automated checks for:

- HTTP status codes
- JSON arrays
- JSON objects
- Response fields
- Response values
- Response structure
- Query parameter results
- Multiple response objects
- Response collection length

---

## Test Coverage

### GET Requests

- Get all posts
- Get post by ID
- Get invalid post ID
- Get posts by `userId`
- Get all users
- Get user by ID
- Get invalid user ID
- Get all comments
- Get comments by `postId`
- Validate path parameters
- Validate query parameters
- Validate multiple query parameters

### POST Requests

- Create a new post
- Create a post without title
- Create a valid post
- Validate POST response structure

### PUT / PATCH Requests

- Update a post using PUT
- Update a post using PATCH
- Validate updated response data

### DELETE Requests

- Delete a post
- Test DELETE with an invalid ID
- Validate DELETE response

### Response Validation

- HTTP status codes
- JSON arrays
- JSON objects
- Required response fields
- Response values
- Resource IDs
- Query parameter filtering
- Response structure
- Response collection length

---

## Positive Test Scenarios

Examples of positive scenarios covered by the collection:

- GET existing post
- GET existing user
- GET existing comments
- GET posts using query parameters
- POST a valid post
- PUT an existing post
- PATCH an existing post
- DELETE a post
- Validate successful API responses
- Validate expected JSON response structures

---

## Negative Test Scenarios

Examples of negative scenarios covered by the collection:

- GET post with invalid ID
- GET user with invalid ID
- POST request without title
- DELETE request with invalid ID

Negative scenarios were used to verify and document the actual behavior of the tested API.

---

## Request Body Validation

POST, PUT and PATCH requests were tested with JSON request bodies.

Example:

```json
{
  "title": "QA Test Post",
  "body": "This is a test post created via Postman.",
  "userId": 1
}
```

The request body was used to validate how the API processes submitted JSON data and how the data is reflected in the response.

---

## Request Parameters

The collection includes testing of both path and query parameters.

### Path Parameter Example

```text
GET /posts/1
```

The ID `1` is passed as part of the endpoint path.

### Query Parameter Example

```text
GET /posts?userId=1
```

The `userId` parameter is used to filter the returned posts.

### Multiple Query Parameters Example

```text
GET /comments?postId=1&_limit=3
```

Multiple query parameters are used to filter the response and limit the number of returned resources.

---

## Automated Test Execution

The Postman collection was executed using the **Collection Runner**.

### Execution Result

| Metric | Result |
|---|---:|
| API Requests | 25 |
| Automated Assertions | 43 |
| Passed | 43 |
| Failed | 0 |
| Skipped | 0 |
| Errors | 0 |

### Final Result

**43 / 43 automated assertions passed.**

The collection completed successfully with:

- 25 API requests executed
- 43 automated assertions executed
- 43 assertions passed
- 0 failed assertions
- 0 skipped tests
- 0 execution errors

---

## Example Test Result

The Collection Runner validated API responses using automated Postman tests.

Examples of validated responses include:

```text
GET /posts
200 OK
PASS
```

```text
GET /posts/1
200 OK
PASS
```

```text
GET /posts/9999
404 Not Found
PASS
```

The `404` response for an invalid resource ID is considered a successful test because the test verifies the expected error behavior.

---

## Important API Behavior

JSONPlaceholder is a fake REST API used for testing and learning.

Write operations such as:

- POST
- PUT
- PATCH
- DELETE

are simulated by the API and are not persisted as changes to a real production database.

During testing, a POST request without a title returned a successful `201 Created` response. This behavior was documented as part of the API testing and demonstrates that the tested fake API does not enforce the same validation rules as a production application might.

---

## Repository Structure

```text
qa-portfolio/
└── api-testing/
    ├── api-test-cases/
    │   └── api-test-cases.md
    │
    └── postman/
        ├── README.md
        └── JSONPlaceholder-API-Collection.json
```

---

## Skills Demonstrated

This project demonstrates practical experience with:

- API testing
- REST APIs
- Postman
- HTTP methods
- HTTP status codes
- JSON
- GET requests
- POST requests
- PUT requests
- PATCH requests
- DELETE requests
- Path parameters
- Query parameters
- Multiple query parameters
- Request bodies
- Response validation
- JSON array validation
- JSON object validation
- Response field validation
- Response value validation
- Response structure validation
- Negative testing
- Positive testing
- Automated API assertions
- Postman Collection Runner
- Test execution
- Test result analysis
- API test case documentation
- Defect-oriented thinking
- QA documentation

---

## Testing Workflow

The API testing process followed this workflow:

```text
API Test Cases
      ↓
Postman Collection
      ↓
API Requests
      ↓
Request Parameters / Request Body
      ↓
API Response
      ↓
HTTP Status Validation
      ↓
JSON Validation
      ↓
Response Field Validation
      ↓
Response Structure Validation
      ↓
Automated Assertions
      ↓
Collection Runner
      ↓
Test Results
```

---

## Test Execution Environment

**Testing Tool:** Postman

**API:** JSONPlaceholder

**Base URL:** `https://jsonplaceholder.typicode.com`

**Execution Type:** Manual execution using Postman Collection Runner

**Collection:** JSONPlaceholder API Collection

**API Requests:** 25

**Automated Assertions:** 43

**Passed:** 43

**Failed:** 0

**Skipped:** 0

**Errors:** 0

---

## Conclusion

This API testing project demonstrates a complete basic API testing workflow using Postman and JSONPlaceholder.

The project includes documented API test cases, a reusable Postman collection, request and response validation, positive and negative scenarios, automated JavaScript assertions, and Collection Runner execution.

The final execution successfully completed **25 API requests** with **43 automated assertions**, resulting in **43 passed tests and 0 failed tests**.
