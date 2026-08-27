# SALO_P2_017 — Customer Search Does Not Handle Reset and No-Result States Correctly

## Bug Type
Functional

## Severity
Moderate

## Priority
High

## Environment
Android Mobile App

## Description

The customer search functionality did not behave correctly when clearing the search input or searching for a customer who does not exist.

Clearing the search did not restore the default customer list, and searching for a non-existent customer displayed the full customer list instead of an appropriate empty-state message.

## Steps to Reproduce

1. Open the Salonist Partner application.
2. Navigate to the customer search functionality.
3. Enter a customer name in the search field.
4. Clear the search input.
5. Observe the customer list.
6. Enter a name that does not exist in the customer list.
7. Observe the search results.

## Expected Result

- Clearing the search input should restore the default customer list.
- Searching for a non-existent customer should display a clear **"No results found"** state.
- The application should not display unrelated customer records.

## Actual Result

- Clearing the search input did not reset the customer list to its default state.
- Searching for a non-existent customer displayed the full customer list instead of a **"No results found"** state.

## Impact

Incorrect search behavior can make it difficult for staff to locate customers and can cause confusion when the application displays unrelated records for a search that should return no results.

## Testing Type

- Functional Testing
- Search Testing
- Negative Testing
- Empty-State Validation
- Input Validation
- User Experience Testing

## Resolution

Fix Completed

## QA Status

Closed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
