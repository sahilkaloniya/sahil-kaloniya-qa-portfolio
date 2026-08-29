# 🔌 API Testing with Postman

A collection of real-world API test suites covering RESTful CRUD operations, OAuth 2.0 authentication workflows, schema assertions, status code validations, and negative boundary scenarios.

---

## 📂 Exported Postman Collections

* 📄 [ReqRes Demo API Testing Collection](./reqres-api-testing.json)
* 📄 [Google OAuth 2.0 API Testing Collection](./google-oauth2-api-testing.json)
* 📄 [GitHub REST API Testing Collection](./github-api-testing.json)

---

## 🧪 Test Coverage Breakdown

### 1. Google OAuth 2.0 & Token Authorization
* **Scope:** Authentication workflows, token retrieval, and bearer token authorization.
* **Key Scenarios:**
  - Token request generation and refresh token lifecycle.
  - Access token validation against protected resource endpoints.
  - Negative validation: expired token rejection (`401 Unauthorized`) and invalid client secret handling (`400 Bad Request`).

### 2. GitHub REST API Testing
* **Scope:** Repository management, user profile data, and header validation.
* **Key Scenarios:**
  - Querying authenticated user endpoints using Personal Access Tokens.
  - JSON response schema validation and header checks (`X-RateLimit`, `Content-Type`).
  - Negative tests on restricted branch endpoints without adequate permissions (`403 Forbidden`).

### 3. ReqRes REST API Test Suite
* **Scope:** User lifecycle management (CRUD).
* **Key Scenarios:**
  - `GET /api/users?page=2` — Asserting `200 OK`, response time < 500ms, pagination metadata, and non-empty user arrays.
  - `POST /api/users` — Asserting `201 Created` with dynamic payload verification and timestamp generation.
  - `POST /api/login` (Negative) — Asserting `400 Bad Request` with exact payload error message validation (`"error": "Missing password"`).

---

## 📊 Postman Test Script Examples

```javascript
// Status Code Assertion
pm.test("Status code is 200 OK", function () {
    pm.response.to.have.status(200);
});

// Response Time Check
pm.test("Response time is under 400ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(400);
});

// JSON Schema and Value Verification
pm.test("User payload contains required keys", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.data).to.be.an("object");
    pm.expect(jsonData.data).to.have.property("id");
    pm.expect(jsonData.data).to.have.property("email");
});
