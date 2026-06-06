# Enterprise SaaS Application Access Management Lab (Microsoft Entra ID)

## Overview

This lab demonstrates how Microsoft Entra ID can be used to onboard and manage access to a Software-as-a-Service (SaaS) application while enforcing authorization controls through user assignments.

## Business Scenario

An organization is deploying Zoom as a SaaS application for employees.

The IAM team is responsible for:

- Onboarding the application into Microsoft Entra ID
- Controlling which users can access the application
- Enforcing authorization through application assignments
- Validating user access
- Reviewing authentication activity through sign-in logs

## Technologies Used

- Microsoft Entra ID
- Zoom Enterprise Application
- Enterprise Applications
- My Apps Portal
- Entra Sign-In Logs

## Lab Configuration

### Users Created

| User | Purpose |
|--------|--------|
| Test User 1 | Authorized User |
| Test User 2 | Authorized User |
| Test User 3 | Unauthorized User |

### Security Groups Created

- Zoom Users
- Zoom Administrators

### Application Configuration

A Zoom Enterprise Application was added to Microsoft Entra ID.
![Zoom Enterprise App Creation](ZoomEnterpriseAppCreation.png)

The **Assignment Required** setting was enabled to ensure only explicitly assigned users could access the application.



## Licensing Limitation Encountered

Microsoft Entra ID Free does not support group-based application assignments.

As a workaround:

- Test User 1 was assigned directly
- Test User 2 was assigned directly
- Test User 3 remained unassigned

## Access Validation Testing

### Test 1 – Authorized User Access

**Expected Result:**
Assigned users should see the Zoom application.

**Actual Result:**
PASS

Test User 1 successfully authenticated and accessed the application.



### Test 2 – Unauthorized User Access

**Expected Result:**
Unassigned users should not see the application.

**Actual Result:**
PASS

Test User 3 could not view the Zoom application.



## Sign-In Log Review

After access testing, Entra sign-in logs were reviewed to validate authentication activity.



## IAM Concepts Demonstrated

- Authentication
- Authorization
- Least Privilege
- Enterprise Application Administration
- SaaS Access Management
- User Assignment Enforcement

## Lessons Learned

- Enterprise applications can be centrally managed through Entra ID.
- Authorization controls can be enforced through application assignments.
- Least privilege reduces unnecessary access.
- Sign-in logs provide visibility into authentication events.

## Skills Demonstrated

- Microsoft Entra ID Administration
- IAM
- Access Control
- SaaS Governance
- Identity Security
