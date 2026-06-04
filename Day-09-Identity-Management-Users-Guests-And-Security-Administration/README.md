# Day-10 – Identity Management, Users, Guests & Security Group Administration

## 🎯 Objective

Continue progressing through the MS-102 learning path by exploring:

- Service health reporting
- Identity management concepts
- User administration
- Guest user management
- Contact creation
- Security group administration
- Device-based security group assignments

---

## 🏥 Microsoft Service Health Reporting

Started by reviewing Microsoft service health functionality.

Using the MS-102 course material, completed a simulation of submitting a service health report to Microsoft.

After reviewing the process in the course, replicated the workflow inside the tenant to become familiar with:

```plaintext
Microsoft 365 Health
Service Health
Support Requests
Operational Monitoring
```

This provided additional exposure to day-to-day Microsoft 365 administration activities.

---

## 👤 Identity Management Concepts

Continued learning around identity management.

One concept reinforced during today's study was:

```plaintext
Identity = User Account
```

Within Microsoft Entra ID, identities represent the accounts used to access Microsoft resources and services.

Areas explored:

- User identities
- Guest identities
- Administrative management
- User lifecycle concepts

---

## 👥 User Administration – Microsoft Entra ID

Practised creating users directly inside Microsoft Entra ID.

Created:

```plaintext
Jude Bellingham
```

Purpose:

Gain familiarity with:

- User creation workflows
- Account configuration
- Identity administration
- Entra ID management

No licence was assigned.

Reason:

```plaintext
Preserve available licences
Control lab costs
```

---

## 🏢 User Administration – Microsoft 365 Admin Center

Repeated the user creation process using the Microsoft 365 Admin Center.

Created:

```plaintext
Gabriel Magalhães
```

This provided useful comparison between:

```plaintext
Microsoft Entra Admin Center
vs
Microsoft 365 Admin Center
```

Observation:

As a Microsoft 365 Administrator, user creation would commonly be performed from the Microsoft 365 Admin Center where licensing can also be assigned during onboarding.

No licence assigned to maintain available resources.

---

## 🌍 External User Management

Explored guest user administration inside Microsoft Entra ID.

Created a guest account using a personal email address.

Display name used:

```plaintext
LeBron James
```

Purpose:

Understand:

- B2B collaboration concepts
- Guest account invitations
- External identity management
- Guest user administration

This provided practical experience with Microsoft's external collaboration capabilities.

---

## 📇 Contact Management

Practised creating organisational contacts through the Microsoft 365 Admin Center.

Created:

```plaintext
Personal Email Contact
```

Purpose:

Gain exposure to:

- Contact management
- Address book administration
- External contact records

---

## 🔐 Security Group Administration

Continued practising security group management.

Created the following groups:

```plaintext
Barcelona
Real Madrid
```

Assigned memberships:

```plaintext
Yamal → Barcelona
Jude Bellingham → Real Madrid
```

This reinforced:

- Group creation
- Membership management
- Identity segmentation
- Access organisation

---

## 💻 Device Security Group Design

Designed a future lab structure for device-specific policy deployment.

Created:

```plaintext
Arsenal Devices
Real Madrid Devices
Barcelona Devices
```

Purpose:

Allow individual Toshiba endpoints to receive different policies and configurations in future labs.

Planned structure:

```plaintext
WT-LAB-01 → Arsenal Devices

WT-LAB-02 → Real Madrid Devices

WT-LAB-03 → Barcelona Devices
```

---

## ⚙️ Security Group vs Microsoft 365 Group

During group creation, reviewed the differences between:

```plaintext
Microsoft 365 Groups
```

and

```plaintext
Security Groups
```

Decision:

Created device groups as:

```plaintext
Security Groups
```

Reason:

Microsoft 365 Groups cannot contain device objects.

Security Groups provide the flexibility required for:

- Device assignments
- Application deployments
- Policy targeting
- Endpoint management

---

## 🛠️ Troubleshooting Exercise

Encountered an issue when attempting to add:

```plaintext
WT-LAB-01
```

to:

```plaintext
Arsenal Devices
```

Initial attempt failed.

Troubleshooting steps:

```plaintext
Deleted group
↓
Recreated group
↓
Retested membership assignment
```

Result:

```plaintext
WT-LAB-01 successfully added
```

This reinforced a key administration skill:

> Troubleshoot, validate, retest.

---

## 📚 Learning Reflection

Today's session focused heavily on identity and access administration.

Key topics covered:

```plaintext
Service Health
Identity Management
Users
Guests
Contacts
Security Groups
Device Groups
Troubleshooting
```

One useful takeaway was understanding the distinction between:

```plaintext
User Objects
Guest Objects
Contact Objects
Device Objects
```

and how Microsoft Entra ID manages each type.

The creation of device-specific security groups also lays the foundation for future endpoint policy testing across individual Toshiba lab devices.

---

## 🔜 Next Steps

Potential future labs:

- Assign different configuration profiles to each device group
- Deploy separate applications to each Toshiba endpoint
- Explore dynamic group membership
- Test Conditional Access concepts
- Continue progressing through MS-102 identity management topics
