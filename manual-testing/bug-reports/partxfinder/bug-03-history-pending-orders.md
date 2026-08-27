# PXF_019 — Pending Order Requests Missing From History

## Bug Type
Functional

## Severity
Moderate

## Priority
Medium

## Environment
Mobile App

## Description

The History tab was empty even though there were pending order requests associated with the user.

Pending order requests should be visible in the user's order history.

## Steps to Reproduce

1. Open the PartXFinder application.
2. Create or submit an order request.
3. Ensure the order request remains in a pending state.
4. Navigate to the History section.
5. Observe the displayed order history.

## Expected Result

The History section should display the user's pending order requests along with the relevant order information and current status.

## Actual Result

Pending order requests were not displayed in the History section.

## Impact

Missing pending requests can make users believe that their order request was not submitted successfully and prevents them from tracking the current status of their request.

## Testing Type

- Functional Testing
- Workflow Testing
- History/Tracking Validation
- State-Based Testing
- End-to-End Testing

## Resolution

Fix Completed

## QA Status

Closed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
