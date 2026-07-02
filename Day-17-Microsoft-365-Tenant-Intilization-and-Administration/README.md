# Day 17 - Microsoft 365 Tenant Initialization and Administration

## Overview

This project focused on preparing my Microsoft 365 tenant for enterprise administration by configuring core organizational settings, implementing pilot user management, enabling security and compliance features, and validating the PowerShell modules required for future Microsoft 365 administration tasks.

Unlike a basic lab, this project was completed within my own Microsoft 365 Business Premium tenant, allowing me to gain practical experience using production administration tools and PowerShell.

---

## Objectives

- Configure Microsoft 365 organization settings.
- Configure release preferences for pilot users.
- Create a Microsoft 365 pilot group.
- Customize Microsoft 365 tenant branding.
- Enable Information Rights Management (IRM).
- Validate Microsoft Graph PowerShell installation.
- Install and configure Exchange Online PowerShell.
- Enable Unified Audit Logging.
- Troubleshoot Exchange Online organization customization.

---

# Environment

| Component | Configuration |
|-----------|---------------|
| Tenant | Microsoft 365 Business Premium |
| Identity | Microsoft Entra ID |
| Collaboration | SharePoint Online |
| Messaging | Exchange Online |
| Administration | Microsoft 365 Admin Center |
| PowerShell | Windows PowerShell |
| Modules | Microsoft Graph SDK, ExchangeOnlineManagement |

---

# Part 1 - Configure Organization Profile

Configured the Microsoft 365 organization profile.

Updated:

- Technical contact
- Preferred language
- Organization information
- Verified tenant configuration

This ensures administrative contact details and organizational information are correctly configured throughout Microsoft 365.

---

# Part 2 - Configure Release Preferences

Configured release preferences to support a pilot deployment strategy.

Implemented:

- Targeted Release
- Pilot user deployment model

Using Targeted Release allows new Microsoft 365 features to be tested before organization-wide deployment.

---

# Part 3 - Create Pilot User Group

Created a pilot group for future Microsoft 365 testing.

Configuration:

- WT Pilot Users
- Owner assigned
- Initial member added

This group can later be used for:

- Microsoft 365 preview features
- Intune assignments
- Conditional Access policies
- SharePoint testing
- Teams testing
- Future Copilot deployment

---

# Part 4 - Configure Tenant Branding

Customized the Microsoft 365 tenant theme.

Configured:

- Navigation colours
- Accent colours
- Organization branding
- WuTangLAN identity

Maintaining consistent branding provides a more professional administrative environment.

---

# Part 5 - Enable SharePoint Information Rights Management

Enabled Information Rights Management (IRM) within SharePoint Online.

Configuration:

- Enabled IRM service
- Refreshed SharePoint IRM settings

This prepares the tenant for future Microsoft Purview and Information Protection labs.

---

# Part 6 - Validate Microsoft Graph PowerShell

Verified the Microsoft Graph PowerShell SDK was correctly installed.

Validated modules included:

- Microsoft.Graph.Authentication
- Microsoft.Graph.Groups
- Microsoft.Graph.Users
- Microsoft.Graph.Identity.DirectoryManagement

This confirms the tenant is ready for Microsoft Graph administration and automation.

---

# Part 7 - Exchange Online PowerShell

Installed the Exchange Online Management module.

Connected successfully using:

```powershell
Connect-ExchangeOnline
```

This provides administrative access to Exchange Online through PowerShell.

---

# Part 8 - Enable Unified Audit Logging

Enabled Unified Audit Logging within Exchange Online.

Command used:

```powershell
Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
```

Initially the command failed because Exchange Online required organization customization before administrative configuration could be modified.

Resolved using:

```powershell
Enable-OrganizationCustomization
```

After enabling organization customization, the audit logging configuration completed successfully.

Verified using:

```powershell
Get-AdminAuditLogConfig
```

Confirmed:

```text
UnifiedAuditLogIngestionEnabled : True
```

Unified Audit Logging is a prerequisite for many Microsoft 365 security and compliance services, including Microsoft Defender, Microsoft Purview, and audit investigations.

---

# Skills Demonstrated

- Microsoft 365 Administration
- Microsoft Entra ID Administration
- Exchange Online Administration
- SharePoint Online Administration
- Microsoft Graph PowerShell
- Exchange Online PowerShell
- Microsoft 365 Groups
- Tenant Branding
- Release Management
- Information Rights Management
- Unified Audit Logging
- Security & Compliance
- PowerShell Administration
- PowerShell Troubleshooting

---

# Troubleshooting

## Issue

Attempting to enable Unified Audit Logging returned the following error:

```text
The command you tried to run isn't currently allowed in your organization.
Run:
Enable-OrganizationCustomization
```

## Resolution

Executed:

```powershell
Enable-OrganizationCustomization
```

Re-ran:

```powershell
Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
```

Verified configuration:

```powershell
Get-AdminAuditLogConfig
```

Audit logging was successfully enabled.

---

# Key Takeaways

- Configured core Microsoft 365 tenant settings.
- Implemented a pilot deployment strategy.
- Customized tenant branding.
- Enabled SharePoint Information Rights Management.
- Validated Microsoft Graph PowerShell.
- Installed and configured Exchange Online PowerShell.
- Enabled Unified Audit Logging.
- Resolved a real-world Exchange Online prerequisite by enabling organization customization before applying audit configuration.

---

# Outcome

This project established a fully initialized Microsoft 365 tenant configured with enterprise administration, security, compliance, and PowerShell management capabilities.

The tenant is now prepared for future Microsoft 365 administration labs involving Microsoft Defender, Microsoft Purview, Exchange Online, Microsoft Graph automation, and advanced security configuration.
