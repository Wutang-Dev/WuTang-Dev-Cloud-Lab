# Day 05 — Intune + Entra Device Enrollment and Application Deployment

## Overview

This lab focused on building a fully functional Microsoft Entra ID and Microsoft Intune managed Windows endpoint environment.

The objective was to simulate a real-world cloud-managed enterprise workstation deployment using Microsoft cloud technologies and endpoint management practices.

The Ryzen-LAB workstation was wiped, enrolled into Microsoft Entra ID, automatically enrolled into Microsoft Intune, assigned to managed device groups, and validated through successful Win32 and Company Portal application deployments.

This project also included troubleshooting device enrollment synchronization, network connectivity issues, DHCP reservations, GitHub SSH integration, and endpoint validation testing.

---

# Environment Information

## Tenant

- Microsoft 365 Tenant
- Microsoft Entra ID
- Microsoft Intune

## Endpoint

| Item | Value |
|---|---|
| Device Name | RYZEN-LAB |
| Operating System | Windows 11 |
| Join Type | Microsoft Entra Joined |
| MDM | Microsoft Intune |
| Ownership | Corporate |

---

# Objectives

- Enroll a Windows device into Microsoft Entra ID
- Enable automatic Intune enrollment
- Configure managed device groups
- Deploy applications through Intune
- Validate Company Portal functionality
- Configure Git and GitHub SSH authentication
- Simulate enterprise endpoint provisioning workflow

---

# Configurations Completed

## Microsoft Entra Device Settings

Configured:

- Users may join devices to Microsoft Entra → Enabled
- Device registration enabled
- Local administrator settings configured
- Corporate ownership validation
- Device management integration with Intune

---

## Microsoft Intune Enrollment Settings

Configured:

- MDM User Scope → All
- Automatic MDM Enrollment
- Intune Enrollment URLs validated
- Windows enrollment integration operational

---

# Device Enrollment Process

## Actions Performed

1. Wiped Ryzen-LAB workstation
2. Reinstalled Windows 11
3. Joined device to Microsoft Entra ID
4. Verified automatic Intune enrollment
5. Verified device visibility in:
   - Microsoft Entra
   - Microsoft Intune
6. Added device into:
   - Enrolled-devices security group

---

# Networking Troubleshooting

## Issue Encountered

The device initially failed Intune synchronization due to network connectivity issues.

## Root Cause

DHCP reservation mismatch on the TP-Link AX3000 router.

## Resolution

- Added new DHCP reservation for Ryzen-LAB
- Verified Wi-Fi connectivity
- Re-ran Intune synchronization
- Confirmed successful sync completion

---

# Application Deployment

## Deployment Method

Applications were deployed through Microsoft Intune using:

- Required installs
- Available installs
- Company Portal integration

---

# Applications Successfully Deployed

| Application | Deployment Status |
|---|---|
| Cisco Packet Tracer | Successful |
| Google Chrome | Successful |
| Git | Successful |
| Splashtop Business | Successful |
| Python | Successful |
| 7-Zip | Successful |

---

# Company Portal Validation

Validated:

- Device appears in Company Portal
- Available applications visible
- Managed applications successfully install
- Device reports as compliant and managed

---

# Git and GitHub Integration

## Git Configuration

Git was deployed automatically through Intune.

## SSH Authentication Setup

Generated SSH key using:

```bash
ssh-keygen -t ed25519 -C ravigordon687@gmail.com
```

Added public SSH key to GitHub account.

Validated authentication using:

```bash
ssh -T git@github.com
```

Successful authentication confirmed.

---

# Repository Integration

Cloned existing cloud engineering repository onto Ryzen-LAB:

```bash
git clone git@github.com:Wutang-Dev/WuTang-Dev-Cloud-Lab.git
```

Repository stored on dedicated lab M.2 storage drive.

---

# Skills Demonstrated

## Cloud Technologies

- Microsoft Entra ID
- Microsoft Intune
- Microsoft 365
- Endpoint enrollment
- Cloud identity management

## Endpoint Management

- Device enrollment
- MDM integration
- Application deployment
- Company Portal management
- Device group assignment

## Networking

- DHCP reservations
- Connectivity troubleshooting
- Endpoint synchronization troubleshooting

## Development Tooling

- Git
- GitHub SSH authentication
- Repository management

---

# Real-World Concepts Simulated

- Enterprise endpoint provisioning
- Zero-touch management concepts
- Centralized application deployment
- Cloud-managed workstation lifecycle
- Endpoint compliance workflows
- Managed device onboarding

---

# Lessons Learned

- Intune synchronization may fail if endpoint networking is unstable
- DHCP reservations can impact managed device communication
- Company Portal significantly improves software deployment visibility
- GitHub SSH authentication improves development workstation workflow
- Managed device groups simplify application targeting

---

# Future Improvements

## Planned Next Steps

- Dynamic device groups
- Compliance policies
- BitLocker deployment
- Windows Update rings
- Microsoft Defender onboarding
- Conditional Access policies
- PowerShell remediation scripts
- Windows Autopilot testing
- Automated device configuration profiles

---

# Outcome

Successfully built a functioning Microsoft Entra ID and Microsoft Intune managed endpoint environment with:

- Cloud-managed identity
- Device enrollment
- Application deployment
- Company Portal integration
- GitHub development integration
- Enterprise-style endpoint management workflow

This project simulates real-world modern workplace management and endpoint administration practices used in enterprise and MSP environments.
