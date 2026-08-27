# SALO_P3_004 — Individual Service Discount Allowed to Exceed Service Price in Quick Sale

## Bug Type
Functional / Business Logic

## Severity
Major

## Priority
High

## Environment
Android Mobile App

## Description

When adding multiple services during a Quick Sale checkout, the application allowed the discount applied to an individual service to exceed that specific service's price, resulting in an incorrect final total calculation.

The system failed to enforce boundary checks preventing line-item discounts from exceeding the individual item value.

## Steps to Reproduce

1. Open the Salonist Partner application.
2. Navigate to the Quick Sale checkout screen.
3. Add multiple services to the cart (e.g., Service A at $50 and Service B at $30).
4. Apply an individual discount to Service A that exceeds its base price (e.g., $60).
5. Review the updated line-item summary and total amount payable.

## Expected Result

- The discount applied to any individual service should not exceed that specific service's price (maximum allowed discount = 100% of line-item value).
- The system should display an inline validation error and prevent checkout if an invalid discount amount is entered.
- Total payable calculation should remain consistent and not reflect invalid negative balances on individual items.

## Actual Result

The application accepted the excessive discount on the individual service without validation, causing an incorrect reduction across the overall bill total.

## Impact

Flawed calculation logic can lead to financial losses, inaccurate invoice generation, and revenue discrepancies in sales reporting.

## Testing Type

- Functional Testing
- Business Logic Validation
- Boundary Value Analysis (BVA)
- Calculation & Billing Testing
- Negative Testing
- Data Integrity Testing

## Resolution

Fix Completed

## QA Status

Closed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
