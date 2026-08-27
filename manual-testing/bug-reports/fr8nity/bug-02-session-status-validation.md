FR8_P1_006 — Active Session Not Invalidated After Membership Status Change
Bug Type

Functional

Severity

Minor

Priority

High

Environment

Desktop / Web

Description

If a previously approved user's profile status changes to Pending, Suspended, or Membership Cancelled, refreshing the user's active session should force the user to log out until the profile is approved again.

Steps to Reproduce
Use a previously approved member account.
Keep the member logged in with an active session.
Change the member's profile status to Pending, Suspended, or Membership Cancelled.
Refresh the active session.
Observe whether the user remains logged in.

Note: The original bug report records the required status-change and session-refresh conditions but does not provide a more detailed reproduction sequence. No additional project-specific steps have been invented for this public portfolio version.

Expected Result

After the profile status changes from approved to Pending, Suspended, or Membership Cancelled, refreshing the active session should invalidate the session and force the user to log out.

The user should only regain access after the profile is approved again.

Actual Result

The active session was not properly invalidated after the user's membership status changed.

Impact

Allowing a user to remain authenticated after their membership becomes pending, suspended, or cancelled can result in unauthorized access to functionality that should no longer be available to that account.

Testing Type
Functional Testing
Session Management Testing
State-Based Testing
Access Control Validation
Negative Testing
Resolution

Fix Completed

QA Status

Fixed

Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
