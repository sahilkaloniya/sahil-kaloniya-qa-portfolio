# SD_024 — Incorrect Stock Availability Message

## Bug Type
Functional

## Severity
Major

## Priority
High

## Environment
Desktop / Web

## Description

The product page displayed an "Only 1 remaining" availability message even though the product was simultaneously displayed as "Sold out."

This created conflicting stock information for the user.

## Steps to Reproduce

1. Navigate to the affected product page.
2. Observe the product availability information.
3. Compare the displayed stock-status messages.

> Note: The original internal bug sheet records the affected product page but does not contain a detailed step-by-step reproduction sequence. No additional steps have been invented for this public version.

## Expected Result

The product should display a single accurate stock status that reflects its actual availability.

## Actual Result

The UI displayed "Only 1 remaining" while the product was also shown as "Sold out."

## Impact

The conflicting messages can mislead users about product availability and create confusion during the purchase journey.

## Testing Type

- Functional Testing
- UI Validation
- Edge-Case Testing

## Resolution

Fix Completed

## QA Status

Done

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
