# SD_016 — Cart Note Not Reflected in Checkout

## Bug Type
Functional

## Severity
Major

## Priority
Medium

## Environment
Desktop / Web

## Description

The user was not properly notified after adding a note, and the added note could not be found on the checkout page.

## Steps to Reproduce

1. Add a product to the cart.
2. Use the available option to add a note.
3. Enter a note and submit/save it.
4. Proceed toward checkout.
5. Check whether the added note is available on the checkout page.

## Expected Result

The user should receive appropriate feedback after adding the note, and the saved note should remain available and be displayed at the relevant stage of the checkout flow.

## Actual Result

The user did not receive proper notification after adding a note, and the added note was not available on the checkout page.

## Impact

This can cause users to believe that their instructions were successfully saved when they are not carried forward to checkout, potentially resulting in important order information being missed.

## Testing Type

- Functional Testing
- End-to-End Testing
- Data Persistence Testing
- User Journey Testing

## Resolution

Fix Completed

## QA Status

Done

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
