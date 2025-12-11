✅ PRODUCT REQUIREMENTS DOCUMENT (PRD)
Internet Billing & Subscriber Management System

(Designed to work with Mikrotik-based networks)

1. Overview

The system enables an Internet Service Provider (ISP) to manage subscribers, billing cycles, payments, and network access.
It allows administrators to create service plans, track usage, suspend unpaid users, and review real-time subscriber status.

The system integrates with the ISP’s network infrastructure so that user access is automatically controlled based on billing status.

2. Goals & Objectives

Automate subscriber billing and renewal.

Provide a unified interface for managing customers, packages, and payments.

Enable real-time control of which subscribers may access the internet.

Track usage, session activity, and connection time.

Provide transparency and accuracy for revenue reporting.

3. Primary User Types
1. System Administrator

Creates and manages service plans

Oversees all subscribers

Configures network access rules

Views revenue & system analytics

2. Support/Operations Staff

Activates new customers

Handles payments and renewals

Suspends/unsuspends accounts

Monitors user activity and issues

3. Subscribers (Optional Portal)

View their package

See account status

View payments & usage

Make payments (if self-service is enabled)

4. Core Features
4.1 Subscriber Management

The system must allow administrators to:

1. Create Subscribers

Full name

Contact details

Username for network access

Optional password (if subscriber login applies)

Assigned service plan

Physical address / installation notes

2. Edit Subscriber Details

Update contact information

Change assigned plan

Update access credentials

Modify account status

3. Search & Filter Subscribers

By name

By username

By plan

By status (active / inactive / expired / suspended)

4. Subscriber Status Control

System must support these states:

Active (internet access allowed)

Inactive/Expired (internet access blocked)

Suspended (manually blocked)

Pending Activation

When state changes, network access must update accordingly.

4.2 Service Plans (Packages)

Administrators can create and manage plans:

Plan Fields

Plan name

Speed profile

Billing period (daily/weekly/monthly/custom)

Price

Data limit (optional)

Session timeout options (optional)

Plan Behavior

When a subscriber’s billing cycle renews, their plan should automatically re-activate.

Changing a subscriber’s plan updates their access rules.

4.3 Billing & Payments
Automated Billing Cycles

The system must:

Track renewal dates for each subscriber

Automatically mark users as expired when renewal date passes

Automatically reactivate subscribers when payment is recorded

Payment Recording

Staff can:

Record payments manually

Attach notes or receipts

View payment history per subscriber

Payment Reminders

The system should support:

Notifications for upcoming renewals

Alerts for overdue accounts

(Email/SMS optional based on client needs)

4.4 Network Access Control (MikroTik Integration)
Authentication & Authorization

When a subscriber attempts to connect:

The system validates whether the user is active and paid

Assigns plan speed and usage rules

Denies access for expired or suspended users

Real-Time Control

Admin actions must take effect immediately:

Activating a user

Suspending a user

Changing plan

Disconnecting active sessions

Accounting Data Handling

System should collect:

Total data usage

Session durations

Connection history

Online/offline status

This data powers reporting and analytics.

4.5 Reporting & Analytics
Core Reports

Daily/weekly/monthly revenue

Active vs inactive users

Usage statistics

Package breakdown

User session logs

Connection history

Outstanding balances

Dashboard Views

Total subscribers

Online subscribers

Revenue summary

Overdue accounts

4.6 Optional Features

(Not mandatory but commonly requested)

Self-Service Subscriber Portal

Subscribers can:

View their plan

View status

Renew subscription

View payment history

View usage history

Mobile App or PWA

Admin or subscriber functionality available on mobile.

CSR (Customer Service) Tools

Trouble ticketing

Notes on accounts

5. Non-Functional Requirements
Usability

Intuitive interface for non-technical staff

Clear status badges

Simple onboarding for new subscribers

Security

Role-based access control

Accurate access validation

Audit logs for admin actions

Performance

Subscriber updates must propagate to network access in under 5 seconds

Dashboard must load within 2 seconds

Reliability

System must ensure accurate billing cycles

User status must never mismatch with network access

Scalability

Must handle increasing subscribers without rearchitecture

Should support multiple access locations

6. Success Criteria

The system is considered successful if:

Admins can manage subscribers and plans without touching the Mikrotik router directly

User access automatically aligns with billing status

Payments and renewals are accurately tracked

Operators can quickly find any subscriber’s status, usage, and billing history

The ISP reduces support issues and improves billing efficiency

7. Assumptions & Dependencies

Client already operates a network using Mikrotik devices

PPPoE, Hotspot, or DHCP mechanisms are configured by network engineers

System will integrate with authentication/accounting data from their network

Admin panel will be web-based