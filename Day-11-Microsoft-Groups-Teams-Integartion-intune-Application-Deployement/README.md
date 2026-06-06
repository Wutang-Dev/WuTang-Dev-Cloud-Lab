# Day-12 – Microsoft 365 Groups, Teams Integration & Intune Application Deployment

## 🎯 Objective

Continue progressing through the MS-102 learning path by exploring:

- Microsoft 365 Groups
- Group ownership and membership
- Teams-enabled groups
- Group email addresses
- Private group access controls
- Dynamic group concepts
- Intune application deployment
- Microsoft Store app deployment

---

## 👥 Microsoft 365 Group Administration

Created three Microsoft 365 Groups to better understand group management and collaboration capabilities.

Groups created:

```plaintext
Arsenal-365
RealMadrid-365
Barcelona-365
```

Assigned myself as the owner of each group.

Purpose:

- Manage membership
- Control access
- Simulate organisational team structures
- Prepare for future Microsoft Teams labs

---

## 🏆 Group Membership Management

Configured membership for each Microsoft 365 Group.

### Arsenal-365

Members:

```plaintext
Saka
Gabriel
```

### RealMadrid-365

Members:

```plaintext
Jude Bellingham
```

### Barcelona-365

Members:

```plaintext
Yamine Yamal
```

This provided practical experience with:

- Group membership management
- Group ownership
- Access administration

---

## 📧 Group Email Address Configuration

Created dedicated email addresses for each Microsoft 365 Group.

Configured:

```plaintext
arsenal365@rg-wutanglan.co.uk

realmadrid365@rg-wutanglan.co.uk

barcelona365@rg-wutanglan.co.uk
```

This reinforced how Microsoft 365 Groups can provide:

- Shared collaboration spaces
- Shared mailboxes
- Shared calendars
- Shared communication channels

---

## 💬 Microsoft Teams Integration

Selected the option to create a Microsoft Teams workspace for each Microsoft 365 Group.

Purpose:

```plaintext
Future Microsoft Teams Labs
```

This demonstrated how Microsoft 365 Groups act as the foundation for many Microsoft 365 services.

Services linked to Microsoft 365 Groups include:

- Teams
- Outlook
- SharePoint
- Planner
- OneDrive collaboration

---

## 🔒 Private Group Configuration

Configured each group as:

```plaintext
Private
```

Result:

```plaintext
Only Owners
↓
Can manage membership

Only Members
↓
Can access group resources
```

This provided practical experience with:

- Group privacy settings
- Access management
- Collaboration controls

---

## ☁️ Group Management in Microsoft Entra ID

Explored group creation through the Azure / Microsoft Entra portal.

Observation:

Regardless of where a group is created:

```plaintext
Microsoft 365 Admin Center
or
Microsoft Entra ID
```

all groups ultimately exist within Microsoft Entra ID.

This helped reinforce Microsoft's identity architecture.

---

## ⚙️ Dynamic Group Exploration

Learned that:

```plaintext
Microsoft 365 Admin Center
```

does not support creation of dynamic groups.

To create dynamic groups, administration must be performed through:

```plaintext
Microsoft Entra ID
```

This highlighted an important distinction between the two administration portals.

---

## 🧪 Dynamic Group Lab

To understand the process, created a test group:

```plaintext
Marketing
```

Added myself as a member.

Purpose:

Gain familiarity with the group creation workflow inside Microsoft Entra ID.

Future learning objective:

```plaintext
Dynamic Membership Rules
```

---

## 💻 Intune Application Deployment Lab

A separate project required Visual Studio Code to be installed on the Jellyfin workstation for an upcoming Proxmox and Immich deployment.

Rather than installing manually, decided to use Intune for deployment practice.

This allowed the Proxmox project and Microsoft 365 learning journey to overlap.

---

## 🚀 Microsoft Store Application Deployment

Selected:

```plaintext
Microsoft Store App (New)
```

Application deployed:

```plaintext
Visual Studio Code
```

Reason:

Microsoft Store applications provide a simplified deployment experience with preconfigured installation settings.

---

## 🎯 Application Assignment

Assigned Visual Studio Code to:

```plaintext
Managed Devices
```

security group.

Target devices included:

```plaintext
RYZEN-LAB
Jellyfin
```

along with any future managed endpoints.

---

## ✅ Deployment Validation

Restarted Jellyfin and signed in using:

```plaintext
rg@rg-wutanglan.co.uk
```

Visual Studio Code was successfully installed.

Additional validation:

Signed out and logged in locally.

Observed notification indicating:

```plaintext
Intune had deployed Visual Studio Code
```

This confirmed successful deployment processing.

---

## 📊 Intune Reporting Validation

Verified deployment inside:

```plaintext
Microsoft Intune Admin Center
```

Confirmed:

```plaintext
Installed Successfully
```

for the targeted devices.

---

## 📚 Learning Reflection

Today's learning reinforced how Microsoft 365 services are interconnected.

Key concepts explored:

```plaintext
Microsoft 365 Groups
Teams
Email Integration
Group Ownership
Private Access Controls
Microsoft Entra Groups
Dynamic Groups
Intune App Deployment
Microsoft Store Apps
```

One particularly useful takeaway was understanding that Microsoft 365 Groups serve as the foundation for many collaboration services within the Microsoft ecosystem.

The Visual Studio Code deployment also demonstrated how endpoint management can support wider infrastructure projects, linking Microsoft 365 administration with the ongoing Proxmox and Immich homelab work.

---

## 🔜 Next Steps

Potential future labs:

- Explore Dynamic Membership Rules
- Test Microsoft Teams functionality within created groups
- Deploy additional Microsoft Store applications
- Create Configuration Profiles for Toshiba endpoints
- Continue MS-102 group and collaboration learning
- Complete Immich deployment project using Visual Studio Code on Jellyfin
