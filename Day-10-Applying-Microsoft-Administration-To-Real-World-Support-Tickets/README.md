# Day-11 – Applying Microsoft 365 Administration Skills to Real-World Support Tickets

## 🎯 Objective

Apply concepts learned through MS-102 study and tenant labs to real-world production support requests.

Today's focus reinforced how Microsoft 365 administration can be used to automate and scale management tasks through groups, assignments, and Conditional Access rather than performing repetitive manual actions.

---

## 💻 Ticket 1 – Microsoft 365 Apps Removal from Student Devices

### Request

A request was received to remove Microsoft 365 Apps from a large number of student devices.

Estimated device count:

```plaintext
30+ devices
```

---

## Traditional Approach

The manual approach would have involved:

```plaintext
Visit each device
↓
Uninstall Microsoft 365 Apps
↓
Repeat 30+ times
```

This would have been time-consuming and difficult to manage at scale.

---

## Implemented Solution

Instead of manually touching every endpoint, existing device groups were leveraged to target the required devices.

The relevant student device groups were assigned to the:

```plaintext
Microsoft 365 Apps for Windows
```

deployment and added to the:

```plaintext
Uninstall Assignment
```

section.

This allowed Intune to handle the removal automatically.

Workflow:

```plaintext
Device Groups
↓
Uninstall Assignment
↓
Intune Processing
↓
Application Removal
```

---

## Skills Practised

- Intune application management
- Group-based targeting
- Application uninstall assignments
- Endpoint management at scale
- Administrative automation

---

## 🔐 Ticket 2 – Library Access Restriction Workflow

### Request

A process was required to restrict access for users with outstanding library fees.

---

## Implemented Solution

Created a dedicated security group:

```plaintext
Library_Restricted
```

Purpose:

Users requiring restrictions can be added to this group when necessary.

---

## Conditional Access Configuration

Configured a Conditional Access policy designed to:

```plaintext
Target:
Restricted Users

AND

Target:
Library Devices
```

Result:

```plaintext
Restricted user
↓
Attempts to access library devices
↓
Access blocked
```

This creates a scalable process where future restrictions can be applied simply by adding users to the security group.

---

## Testing Strategy

Created a dedicated test user account to validate the policy.

Workflow:

```plaintext
Create Test User
↓
Add to Restricted Group
↓
Validate Conditional Access Behaviour
↓
Review Results
```

Using a test account reduces risk and follows a safer deployment methodology.

---

## Skills Practised

- Conditional Access
- Security Groups
- User targeting
- Access control
- Policy testing
- Identity management

---

## 📚 Learning Reflection

Today's work highlighted one of the key advantages of Microsoft 365 administration:

```plaintext
Groups
↓
Policies
↓
Automation
↓
Scale
```

Rather than managing users and devices individually, administrative tasks can be applied through group membership and policy assignments.

This aligns directly with concepts currently being studied through the MS-102 learning path.

A major takeaway was understanding how:

```plaintext
Users
Groups
Devices
Policies
```

can work together to create scalable management solutions.

---

## 🚀 Key Achievement

Applied Microsoft 365 concepts learned through:

```plaintext
MS-102 Study
↓
Tenant Labs
↓
Production Environment
```

to solve real-world support requests.

This reinforced that practical implementation is significantly more valuable than simply consuming training material.

---

## 🔜 Next Steps

Potential future activities:

- Validate Conditional Access policy behaviour
- Review sign-in logs and policy reporting
- Continue MS-102 identity and access management topics
- Expand security group-based administration workflows
- Continue documenting practical Microsoft 365 implementations
