# FR8_P3_030 — Duplicate Meeting Time Slot Can Be Selected

## Bug Type
Functional

## Severity
Major

## Priority
High

## Environment
Desktop / Web

## Description

A user who had already sent a meeting request for a specific date and time was able to select the same time slot again through the member directory.

The system should prevent users from booking or requesting an already occupied meeting slot.

## Steps to Reproduce

1. Send a meeting request for a specific date and time.
2. Navigate to the member directory.
3. Locate the same member and meeting availability.
4. Select the previously requested date and time slot.
5. Observe the system response.

## Expected Result

The previously selected meeting time slot should no longer be available for another request.

If the user attempts to select the occupied slot, the UI should display an informational message indicating that the slot has already been booked.

## Actual Result

The same date and time slot could be selected again through the directory.

## Impact

This can result in conflicting meeting requests for the same time slot and creates an inconsistent booking experience for users.

## Testing Type

- Functional Testing
- Business Rule Validation
- Negative Testing
- Booking/Appointment Testing
- End-to-End User Journey Testing

## Resolution

Fix Completed

## QA Status

Fixed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
