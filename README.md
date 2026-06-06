# Microsoft-Entra-ID-Enterprise-Application-Integration
Simulating Enterprise SaaS application onboarding and access control using Entra ID.
## Overview
This lab demonstrates how Microsoft Entra ID can be used to onboard and manage access to a Software-as-a-Service (SaaS) application while enforcing authorization controls through user assignments.

The objective was to simulate a real-world IAM scenario where users require access to a business application while maintaining least privilege principles and proper access governance.
## Business Scenario 
An organization is deploying Zoom as a SaaS application for employees.

The IAM team is responsible for:

Onboarding the application into Microsoft Entra ID
Controlling which users can access the application
Enforcing authorization through application assignments
Validating user access
Reviewing authentication activity through sign-in logs

To accomplish this, a Zoom Enterprise Application was configured within Microsoft Entra ID and access was granted only to approved users.

## Technologies Used
Microsoft Entra ID
Zoom Enterprise Application
Enterprise Applications
User Assignments
My Apps Portal
Entra Sign-In Logs

## Security Groups Created
Zoom Users 
Zoom Administrators 

## Application Configuration 
A Zoom Enterprise Application was added to Microsoft Entra ID.

The Assignment Required setting was enabled to ensure only explicitly assigned users could access the application.

## Licensing Limitation Encountered 
While performing the lab, a limitation of Microsoft Entra ID Free was identified.

Group-based application assignments require a premium license and therefore could not be utilized.

As a workaround:
Test User 1 was assigned directly to the application
Test User 2 was assigned directly to the application
Test User 3 remained unassigned
This still allowed validation of authorization controls.
