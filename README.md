# Sahil Kaloniya — QA Engineer Portfolio

## QA Engineer | Manual Testing | API Testing | Playwright | TypeScript / JavaScript

QA Engineer with 2+ years of experience in manual and automation testing of web and mobile applications. Experienced in functional, regression, smoke, sanity, UI/UX, cross-browser, cross-device, and end-to-end testing.

Specialized in test planning, defect isolation, bug reproduction, fix verification, multi-role workflow validation, API testing with Postman, and building Page Object Model (POM) test automation frameworks with Playwright and TypeScript.

---

## 🏆 Featured Defect: Cross-Entity State Conflict & Admin Approval Leak

> **Project:** NDTSS Examination & Membership Portal  
> **Module:** Membership & Administrative Approval API  
> **Severity:** High | **Priority:** Major  
> **Report:** [View Full Defect Report](./manual-testing/bug-reports/ndtss/bug-02-membership-state-conflict.md)

* **The Issue:** When a user submitted both an Individual and Corporate Membership application under the same account, the user profile UI collapsed both into a single entity. Upon an administrator approving the **Individual Membership** in the backend admin portal, the system erroneously updated and approved the **Corporate Membership** instead.
* **How It Was Found:** Traced during multi-role exploratory workflow testing by monitoring API network request payloads and state transitions between the admin approval endpoint and the user profile database records.

---

## 🧪 QA Skills

### Manual Testing
- Functional, Smoke, Sanity & Regression Testing
- End-to-End & User Journey Validation
- Cross-Browser & Multi-Device Testing
- Positive, Negative, Edge-Case & Boundary Testing
- Role-Based Access Control (RBAC) & Multi-Role Workflow Validation

### Test Documentation
- Test Cases, Scenarios & Test Execution Tracking
- Test Planning & QA Strategy Documentation
- Clear, Actionable Defect Reporting with Root-Cause Context
- Retesting, Fix Verification & Regression Analysis

### API Testing
- Postman Collection Management & Environment Variables
- REST API Request/Response Payload Validation
- HTTP Status Code, Schema & Header Verification
- Positive & Negative API Testing Scenarios

### Automation
- Playwright Test Framework
- TypeScript & JavaScript
- Page Object Model (POM) Design Pattern
- Dynamic Test Fixtures & Data-Driven Testing
- GitHub Actions CI/CD Integration & Cross-Browser Execution

### Tools & Methodologies
- JIRA, GitHub, Postman, Playwright, Allure Reports, Agile/Scrum

---

## 📂 Proof of Work

### 🐞 Manual Testing & Bug Reports
Real-world, sanitized defect reports covering complex workflows, state persistence issues, boundary limits, and data leaks.
- [View All Bug Reports](./manual-testing/bug-reports/)
  - [NDTSS Portal Defect Reports (5 Bugs)](./manual-testing/bug-reports/ndtss/)
  - [Salonist Partner App Defect Reports (5 Bugs)](./manual-testing/bug-reports/salonist/)
  - [FR8NITY Defect Reports](./manual-testing/bug-reports/fr8nity/)
  - [PartXFinder Defect Reports](./manual-testing/bug-reports/partxfinder/)
  - [Sierra-Darien Defect Reports](./manual-testing/bug-reports/sierra-darien/)

### 🤖 Playwright Test Automation Framework
Full-scale E2E automation repository built with Playwright, TypeScript, and Page Object Model, complete with CI/CD integration.
- [View Playwright Automation Repository](https://github.com/sahilkaloniya/playwright-typescript-automation)

### 🧪 Test Cases
Structured test suites demonstrating positive, negative, boundary, and role-based test coverage.
- [View Test Cases](./manual-testing/test-cases/)

### 📋 Test Planning
Strategic test planning documents detailing scope, test matrices, and exit criteria.
- [View Test Plans](./manual-testing/test-plans/)

### 🔌 API Testing
Postman collections, environment configurations, and REST API test validations.
- [View API Testing](./api-testing/)

---

## 💼 Project Experience

### NDTSS — Exam & Certification Management Platform
- Validated end-to-end multi-role workflows across Candidates, Invigilators, Examiners, and Super Admins.
- Tested certificate generation idempotency, multi-tier membership lifecycles, and event check-in point tracking.

### Salonist — Salon & Spa Partner Management App (Android)
- Executed functional, session, and transaction testing across booking calendars and Quick Sale POS modules.
- Tested boundary discounts, payment carry-over persistence, and customer search empty states.

### PartxFinder — Used Cars & Car Parts Marketplace
- Tested buyer, seller, sub-admin, and super-admin permissions and transaction workflows.
- Executed search filtering, inventory listing validation, and responsive mobile testing.

### Qwaiting — Queue Management Solution
- Reproduced client-reported production defects and verified bug fixes.
- Performed regression testing across multi-role administrative queues and kiosk interfaces.

### Sierra Darien — Fashion E-commerce Platform
- Tested user journeys from product catalog to cart note validations and checkout flows.
- Executed UI/UX, responsive layout, and cross-browser compatibility tests.

---

## 🛠️ Technology Stack

| Category | Tools / Technologies |
|---|---|
| **Manual Testing** | Functional, Regression, Smoke, Sanity, UI/UX, E2E, Boundary Value Analysis |
| **API Testing** | Postman, REST APIs, JSON Validation |
| **Automation** | Playwright, TypeScript, JavaScript, Page Object Model (POM) |
| **CI/CD & Reporting** | GitHub Actions, Playwright HTML Reporter, Allure |
| **Collaboration** | JIRA, GitHub, Agile / Scrum |

---

## 🎯 QA Approach

- **User-Centric & Edge-Focused:** Identify how real users break workflows when performing unexpected actions.
- **Data & Boundary Integrity:** Rigorously test boundaries, state transitions, and calculation formulas.
- **Frontend vs. Backend Cohesion:** Verify that client-side UI states accurately reflect API payloads and database records.
- **Developer-Friendly Defect Reports:** Document clear reproduction steps, environment details, expected vs. actual outcomes, and system impact.

---

## 📫 Contact

**Sahil Kaloniya**  
QA Engineer  
Email: sahilkaloniya0@gmail.com  
GitHub: [github.com/sahilkaloniya](https://github.com/sahilkaloniya)
