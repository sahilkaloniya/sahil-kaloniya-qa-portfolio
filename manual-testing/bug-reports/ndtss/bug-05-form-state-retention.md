# NDTSS_AF_009 — Multi-Step Application Form Data Loss on Page Refresh

## Bug Type
Functional / Usability

## Severity
Major

## Priority
High

## Environment
Web Portal (Cross-Browser / Desktop & Mobile)

## Description

During completion of the multi-step examination application form, refreshing the browser page or experiencing an accidental reload caused all entered candidate data and step progression to reset completely.

The application failed to maintain temporary local state/session storage across pages 1 and 2, forcing users to restart the extensive multi-section application from the beginning.

## Steps to Reproduce

1. Open the NDTSS examination application form.
2. Complete all required fields on Page 1 (Personal details, contact details, certification levels).
3. Proceed to Page 2 (Exam type, schedule selection, file attachments).
4. Enter test data into the Page 2 fields.
5. Trigger a browser refresh (F5 / reload).
6. Observe form state and field values.

## Expected Result

- Form input and current step progression should persist in temporary session/local storage across page refreshes.
- Returning or refreshing the page should restore all previously filled values and keep the user on their active step.
- An unsaved changes prompt or automatic draft saving should protect against data loss.

## Actual Result

The form state was wiped on page refresh, resetting the user to a blank Step 1 and losing all entered information.

## Impact

Losing multi-page form progress creates high user frustration, increases form abandonment rates, and degrades application reliability during lengthy certification submissions.

## Testing Type

- Functional Testing
- Form State & Session Persistence Testing
- Browser Lifecycle & Refresh Testing
- Usability Testing
- Edge Case & Recovery Validation

## Resolution

Fix Completed

## QA Status

Closed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
