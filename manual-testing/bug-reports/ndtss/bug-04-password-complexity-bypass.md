# NDTSS_RG_008 — Registration Successfully Initiated Despite Failing Password Complexity Rules

## Bug Type
Functional / Security

## Severity
High

## Priority
Major

## Environment
Web Portal (Windows / Chrome / Desktop)

## Description

The user registration process permitted accounts to be created using weak passwords that violated established security policy criteria (such as requiring uppercase letters, lowercase letters, numbers, and special characters).

The application lacked robust client and server-side password complexity validation prior to submitting the registration payload.

## Steps to Reproduce

1. Open the NDTSS registration page.
2. Fill in all required personal information fields with valid data.
3. In the password field, enter a weak password that violates mandatory complexity requirements (e.g., all lowercase letters with no numbers or special symbols).
4. Enter the matching value in the Confirm Password field.
5. Click the **Register** / **Sign Up** button.
6. Observe the registration flow behavior.

## Expected Result

- The system should evaluate password strength against required criteria in real time and upon submission.
- Form submission should be blocked if any password condition is unmet.
- Clear inline validation messages should specify missing criteria (e.g., "Password must contain at least one uppercase letter, one number, and one special character").

## Actual Result

The application initiated and completed the registration process without validating the password complexity requirements.

## Impact

Allowing weak and non-compliant passwords weakens system authentication security, increases exposure to credential brute-forcing, and fails compliance standards.

## Testing Type

- Functional Testing
- Security & Authentication Testing
- Input Field Validation
- Form Submission Integrity
- Negative Flow Testing

## Resolution

Fix Completed

## QA Status

Closed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
