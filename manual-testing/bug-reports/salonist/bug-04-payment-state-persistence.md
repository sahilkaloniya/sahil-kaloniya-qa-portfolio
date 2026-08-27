# SALO_P3_030 — Payment Amount Carries Over After Navigating Back During Ongoing Transaction

## Bug Type
Functional / State Management

## Severity
Major

## Priority
High

## Environment
Android Mobile App

## Description

When initiating a transaction and navigating back before completing payment, the entered payment amount persisted and automatically carried over into subsequent new quick sales and calendar appointments.

The application failed to reset the transaction state when the user navigated away, causing stale payment data to leak across different checkout sessions.

## Steps to Reproduce

1. Open the Salonist Partner application.
2. Initiate a transaction (via Quick Sale or Appointment checkout).
3. Enter or select a payment amount.
4. Without completing the transaction, navigate back using the app or system back button.
5. Initiate a new, separate Quick Sale or select a different calendar appointment for checkout.
6. Observe the payment amount field.

## Expected Result

- Navigating back from an incomplete checkout should cancel or reset the active transaction state.
- Initiating a new transaction or appointment checkout should display the correct default/calculated amount for that specific transaction, without stale data from previous sessions.

## Actual Result

The previously entered payment amount remained in memory and automatically populated into newly initiated transactions and appointments.

## Impact

Carrying over unfinalized transaction amounts can lead to incorrect customer billing, financial discrepancies, and confusion during checkout operations.

## Testing Type

- Functional Testing
- Transaction State Management Testing
- Data Persistence & Leakage Testing
- Navigation & Back-Stack Testing
- Negative Flow Validation
- User Journey Testing

## Resolution

Fix Completed

## QA Status

Closed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
