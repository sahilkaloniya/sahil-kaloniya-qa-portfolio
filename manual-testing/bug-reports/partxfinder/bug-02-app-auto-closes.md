# PXF_007 — App Auto-Closes When Selecting Highlighted Fields

## Bug Type
Functional

## Severity
Major

## Priority
Critical

## Environment
Mobile App

## Description

The application automatically closes whenever the user attempts to select a value from one of the highlighted fields.

## Steps to Reproduce

1. Open the PartXFinder application.
2. Navigate to the screen containing the highlighted fields.
3. Select any highlighted field.
4. Attempt to choose a value from the available options.
5. Observe the application behavior.

## Expected Result

The selected field should remain open and allow the user to choose a value successfully.

The application should continue running normally without closing or exiting the current flow.

## Actual Result

The application automatically closes when the user attempts to select a value from the highlighted fields.

## Impact

This prevents users from completing the affected interaction and can block the associated workflow entirely.

Because the application closes unexpectedly during a user action, this represents a critical functional issue.

## Testing Type

- Functional Testing
- Crash Testing
- Input/Interaction Testing
- Mobile Application Testing
- Negative Testing
- User Journey Testing

## Resolution

Fix Completed

## QA Status

Closed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
