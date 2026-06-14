# Day-15 – PowerShell Fundamentals, Execution Policies & Microsoft Graph Introduction

## 🎯 Objective

Continue progressing through the MS-102 learning path by exploring:

- PowerShell fundamentals
- Script execution policies
- Microsoft Graph concepts
- Modern Microsoft administration
- Microsoft Graph PowerShell installation

---

## ⚡ PowerShell Execution Policies

Continued learning the fundamentals of PowerShell administration through the MS-102 course.

Reviewed PowerShell execution policies and how they control script execution on Windows devices.

Command explored:

```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass
```

Purpose:

```plaintext
Allow PowerShell scripts to run without restrictions.
```

---

## 🔒 Security Considerations

Although the command was demonstrated during the course, I chose to leave my system configured with the default execution policy.

Reason:

```plaintext
I am still very new to PowerShell.
```

Allowing unrestricted script execution would mean:

- Scripts could execute without warning
- Potentially unsafe scripts could run
- Increased risk of accidental mistakes

For a learning environment, the default restrictions provide a useful safety net.

Learning takeaway:

```plaintext
Just because you can bypass security controls
doesn't mean you should.
```

---

## 🏢 Enterprise Management Concepts

Learned that execution policies can be centrally managed in enterprise environments.

Methods include:

### Group Policy

Administrators can configure execution policies across multiple devices through:

```plaintext
Group Policy Objects (GPOs)
```

allowing standardised PowerShell behaviour across an organisation.

---

### Cloud Management

Modern device management solutions can also be used to enforce PowerShell-related settings through cloud-managed endpoints.

This reinforced how organisations can manage hundreds or thousands of devices from a central location.

---

## 🌐 Introduction to Microsoft Graph

Started learning about Microsoft Graph and its role within the Microsoft ecosystem.

Microsoft Graph acts as a centralised API layer that allows administrators and developers to interact with multiple Microsoft services through a single interface.

Examples include:

```plaintext
Microsoft Teams
OneDrive
SharePoint
Exchange Online
Microsoft Intune
Microsoft Entra ID
Outlook
```

---

## 📚 Why Microsoft Graph Exists

Learned some of the limitations of traditional PowerShell administration.

Historically, administrators often required separate modules for different Microsoft services.

Examples:

```plaintext
Exchange Module
Entra Module
SharePoint Module
Teams Module
```

Challenges included:

- Multiple management tools
- Separate authentication methods
- Limited cross-service automation
- Increased complexity

---

## 🚀 Benefits of Microsoft Graph

Microsoft Graph was designed to simplify administration by providing:

```plaintext
Centralised Access
Unified Authentication
Cross-Service Automation
Modern API Framework
```

This allows administrators to interact with multiple Microsoft services from a single platform.

---

## 💻 Microsoft Graph Installation Lab

Practised installing Microsoft Graph PowerShell on the Jellyfin workstation.

### Step 1 – Launch PowerShell as Administrator

Opened:

```plaintext
Windows Terminal (Administrator)
```

to perform module installation tasks.

---

### Step 2 – Configure Execution Policy

Temporarily enabled script execution.

Command used:

```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass
```

Purpose:

Allow installation scripts to execute without being blocked.

---

### Step 3 – Install Microsoft Graph

Installed the Microsoft Graph PowerShell module.

Command used:

```powershell
Install-Module Microsoft.Graph -Scope CurrentUser -Repository PSGallery -Force
```

Parameters:

```plaintext
CurrentUser
→ Install for current user only

PSGallery
→ Use PowerShell Gallery repository

Force
→ Suppress confirmation prompts
```

---

## ✅ Installation Outcome

Successfully installed:

```plaintext
Microsoft Graph PowerShell SDK
```

This prepares the environment for future labs involving:

- Microsoft Entra ID
- Microsoft Intune
- Microsoft 365 Administration
- User Management
- Device Management
- Automation

---

## 📚 Learning Reflection

Today's learning marked the first real introduction to modern Microsoft automation.

Key concepts explored:

```plaintext
PowerShell
Execution Policies
Microsoft Graph
PowerShell Modules
Modern Microsoft Administration
```

One particularly useful takeaway was understanding why Microsoft Graph is becoming the preferred management platform.

Rather than learning separate management tools for every Microsoft service, Microsoft Graph provides a centralised method for interacting with the Microsoft ecosystem.

This aligns closely with the broader learning philosophy of:

```plaintext
Work Smart
↓
Automate
↓
Scale
```

rather than performing repetitive administrative tasks manually.

---

## 🔜 Next Steps

Potential future labs:

- Connect to Microsoft Graph
- Query tenant information
- Retrieve users using Graph PowerShell
- Explore Microsoft Graph permissions
- Compare Graph PowerShell to traditional modules
- Continue MS-102 automation and administration topics
