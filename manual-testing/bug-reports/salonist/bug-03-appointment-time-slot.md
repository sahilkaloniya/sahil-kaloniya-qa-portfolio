# SALO_P2_011 — Appointment Time Slot Validation Issue

## Bug Type
Functional

## Severity
Major

## Priority
High

## Environment
Android Mobile App

## Description

The appointment booking flow did not correctly validate the availability of the selected appointment time slot.

The application allowed an appointment time to be selected even when the slot should not have been available.

## Steps to Reproduce

1. Open the Salonist Partner application.
2. Navigate to the appointment booking flow.
3. Select a customer and the required appointment details.
4. Open the available date and time-slot selection.
5. Select a time slot that is not available.
6. Continue with the appointment booking flow.
7. Observe the application behavior.

## Expected Result

The application should display only valid and available appointment time slots.

Unavailable slots should not be selectable, and the system should prevent an appointment from being created for an unavailable time.

## Actual Result

The appointment flow did not correctly validate the selected time slot.

## Impact

Incorrect time-slot validation can result in scheduling conflicts and may allow appointments to be created for unavailable periods, affecting both staff and customers.

## Testing Type

- Functional Testing
- Appointment/Booking Testing
- Business Rule Validation
- Time-Slot Validation
- Negative Testing
- End-to-End Testing

## Resolution

Fix Completed

## QA Status

Closed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
