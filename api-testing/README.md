# 🔌 API Testing with Postman

A collection of real-world API test suites covering RESTful CRUD operations, schema assertions, status code validations, header verifications, and negative boundary scenarios.

---

## 📂 Exported Postman Collections

* 📄 [ReqRes Demo API Testing Collection](./REQRES%20-%20Demo%20API%20Testing.postman_collection.json)
* 📄 [GitHub REST API Testing Collection](./Github%20-%20API%20Testing.postman_collection.json)

---

## 🧪 Test Coverage Breakdown

### 1. ReqRes REST API Test Suite
* **Scope:** User lifecycle management (CRUD) and authentication boundaries.
* **Key Scenarios:**
  - `GET /api/users?page=2` — Validates HTTP `200 OK`, response time < 500ms, pagination metadata integrity, and non-empty user arrays.
  - `POST /api/users` — Asserts `201 Created` with dynamic payload verification and timestamp generation.
  - `PUT /api/users/2` — Verifies resource mutation and matching update timestamps.
  - `DELETE /api/users/2` — Verifies resource deletion returning HTTP `204 No Content`.
  - `POST /api/login` (Negative) — Asserts strict `400 Bad Request` handling when submitting missing credentials (`"error": "Missing password"`).

### 2. GitHub REST API Testing
* **Scope:** Repository management, authenticated user profile data, and rate-limiting headers.
* **Key Scenarios:**
  - Querying authenticated user endpoints using Personal Access Tokens.
  - JSON response schema validation and header verification (`X-RateLimit-Limit`, `Content-Type`).
  - Negative validation on restricted branch endpoints without adequate permissions (`403 Forbidden`).

---

## 📊 Postman Test Script Examples

```javascript
// Status Code Assertion
pm.test("Status code is 200 OK", function () {
    pm.response.to.have.status(200);
});

// Response Time Validation
pm.test("Response time is under 500ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});

// JSON Schema and Value Verification
pm.test("User payload contains required keys", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.data).to.be.an("object");
    pm.expect(jsonData.data).to.have.property("id");
    pm.expect(jsonData.data).to.have.property("email");
    pm.expect(jsonData.data.email).to.include("@reqres.in");
});
