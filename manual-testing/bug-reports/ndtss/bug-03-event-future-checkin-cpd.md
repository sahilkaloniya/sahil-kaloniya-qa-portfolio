# NDTSS_EV_013 — Premature Check-in/Check-out Allowed on Future Events Granting CPD Points

## Bug Type
Functional / Business Logic

## Severity
Major

## Priority
High

## Environment
Web Portal (Desktop)

## Description

Users were able to execute the check-in and check-out workflows for upcoming events scheduled on future dates, allowing them to illegitimately claim Continuing Professional Development (CPD) points before the event occurred.

The application lacked server-side date-time validation to restrict attendance actions exclusively to active event windows.

## Steps to Reproduce

1. Log in to the NDTSS member portal with a valid registered account.
2. Navigate to the **Events** module.
3. Locate and join an event scheduled for an upcoming/future date.
4. Open the event details/registration modal.
5. Trigger the **Check-in** action.
6. Trigger the **Check-out** action.
7. Navigate to the user profile dashboard and verify the accumulated CPD points balance.

## Expected Result

- Check-in and check-out actions must be disabled and locked until the event's designated start time.
- Attempting to check in early should return an informative validation message (e.g., "Check-in will be available when the event starts").
- CPD points must only be awarded upon validated attendance during active event hours.

## Actual Result

The system permitted premature check-in and check-out on future events, immediately crediting CPD points to the user profile.

## Impact

Allowing premature attendance confirmation undermines the professional certification process, compromises continuing education integrity, and enables unauthorized credential points accumulation.

## Testing Type

- Functional Testing
- Business Logic Validation
- Date & Time Boundary Testing
- Points & Accreditation Integrity Testing
- Negative Flow Testing
- API / Server-Side Validation

## Resolution

Fix Completed

## QA Status

Closed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
