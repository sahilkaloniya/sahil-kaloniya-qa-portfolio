# NDTSS_MM_051 — Cross-Entity Membership State Conflict During Admin Approval

## Bug Type
Functional / Business Logic

## Severity
High

## Priority
Major

## Environment
Web Portal (Desktop)

## Description

When a user submitted an Individual Membership form followed by a Corporate Membership form under the same account, the user profile incorrectly displayed only the Corporate Membership status. Furthermore, when an admin approved the pending Individual Membership from the backend portal, the system erroneously applied the approval status to the Corporate Membership instead.

The application failed to isolate and map distinct application entity states between the user profile frontend and the administrative approval dashboard.

## Steps to Reproduce

1. Register and log in with a new user account on the NDTSS portal.
2. Complete and submit the **Individual Membership** form.
3. Complete and submit the **Corporate Membership** form under the same account.
4. Navigate to the user profile and check the membership status section.
5. Log in to the Admin portal with administrator credentials.
6. Open the pending applications queue and approve the **Individual Membership** application.
7. Return to the user profile dashboard and verify the statuses of both memberships.

## Expected Result

- The user profile dashboard should distinctly list both Individual and Corporate membership requests along with their respective statuses (e.g., Pending, Approved, Rejected).
- Approving an Individual Membership in the admin panel should only change the status of the Individual Membership record.
- The Corporate Membership application should remain in its independent pending state until explicitly actioned.

## Actual Result

- The user profile UI only showed the Corporate Membership status, overwriting the Individual record view.
- Approving the Individual Membership in the admin portal incorrectly updated the Corporate Membership status to Approved.

## Impact

Cross-entity data collisions cause severe data corruption, grant unauthorized corporate membership access based on personal applications, and obstruct auditing and fee processing.

## Testing Type

- Functional Testing
- Role-Based Workflow Testing
- Entity Relationship & State Mapping Testing
- Integration Testing (Admin Portal to Client Dashboard)
- End-to-End User Journey Testing

## Resolution

Fix Completed

## QA Status

Closed

## Confidentiality

Project-specific URLs, screenshots, internal references and other confidential information have been removed from this public portfolio version.
