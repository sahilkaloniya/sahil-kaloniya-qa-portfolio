# NDTSS_AFR_009 — Duplicate Certificate Generation on Repeated Approval Attempts

## Bug Type
Functional / Workflow

## Severity
Major

## Priority
High

## Environment
Web Portal (Chrome / Desktop)

## Description

When an AQB, Certificate Manager, or Super Admin encountered an intermittent UI error while generating a certificate and retried the action, the backend processed multiple approval requests, resulting in duplicate certificates being generated for the same user profile.

The system lacked idempotency safeguards to prevent multiple certificate entities from being created upon repeated submission requests.

## Steps to Reproduce

1. Log in to the NDTSS Admin portal with Super Admin or Certificate Manager credentials.
2. Navigate to the pending renewal/recertification candidate list.
3. Open a candidate record ready for final certificate generation.
4. Click the **Generate Certificate** / **Approve** button.
5. In case of an intermittent error response, click the button again or refresh the page.
6. Navigate to the candidate’s user profile under the Final Certificate section.
7. Observe the number of generated certificates.

## Expected Result

- The system should ensure idempotent certificate generation: each approved record must produce exactly one unique certificate.
- Repeated clicks or subsequent retries should be locked until the active request completes or safely fails.
- Only a single valid certificate entry should appear in the candidate's profile.

## Actual Result

Multiple duplicate certificate records were generated and displayed in the user profile.

## Impact

Duplicate certificate generation creates administrative inconsistencies, clutters user verification records, and risks issuing conflicting certification numbers to the public registry.

## Testing Type

- Functional Testing
- Workflow Testing
- Idempotency & Concurrency Validation
- Admin Role & Permission Testing
- Data Integrity Testing

## Resolution

Fix Completed

## QA Status

Closed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
