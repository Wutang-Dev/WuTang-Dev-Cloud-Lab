# Day 06 - Intune Win32 App Packaging And PowerShell Deployments

## Overview

Today focused on practical Microsoft Intune administration tasks using a personal Microsoft 365 tenant and enrolled Windows device (Ryzen Lab).

The goal was to continue building real-world endpoint management skills by deploying applications, troubleshooting installation issues, and creating a PowerShell-based Win32 deployment for distributing ZIP files through Intune.

This simulated realistic IT support and school environment deployment scenarios.

---

# Objectives

- Deploy Win32 applications through Microsoft Intune
- Practice silent installs and uninstall commands
- Configure detection rules
- Troubleshoot failed deployments
- Deploy PowerShell scripts through Intune
- Simulate exam file distribution to managed devices
- Improve understanding of user vs system context deployments

---

# Environment

## Tenant Services

- Microsoft Intune
- Microsoft Entra ID
- Company Portal
- Windows 11 Device Enrollment

## Test Device

- Ryzen Lab PC
- Enrolled into Entra ID and Intune

---

# Applications Successfully Packaged And Deployed

## PuTTY

### Deployment Type
- Win32 App (.intunewin)

### Installer
- putty-64bit-0.83-installer.msi

### Result
- Successfully deployed through Company Portal

### Skills Practiced
- MSI packaging
- Silent install configuration
- Detection rules
- Company Portal deployment

---

## Python 3.10.0

### Deployment Type
- Win32 App (.intunewin)

### Installer
- python-3.10.0-amd64.exe

### Silent Install Command

```powershell
python-3.10.0-amd64.exe /quiet InstallAllUsers=1 PrependPath=1
```

### Key Troubleshooting

Initial deployment failed because the install command referenced the incorrect filename.

Correct filename:
```powershell
python-3.10.0-amd64.exe
```

instead of:
```powershell
python-3.10.0.exe
```

### Result
- Successfully deployed after correcting installer name

### Skills Practiced
- EXE packaging
- Silent installs
- Detection rules
- Intune troubleshooting
- Company Portal deployments

---

## LibreOffice

### Result
- Successfully packaged and deployed

### Skills Practiced
- Larger Win32 deployments
- Software deployment workflow repetition
- Intune app assignments

---

# Hyper-V PowerShell Deployment Project

## Goal

Attempted to enable Hyper-V using PowerShell deployment through Intune.

### Script Used

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All -NoRestart
```

### Outcome

The script successfully worked locally in PowerShell but did not execute correctly through Intune scripting assignments.

### Key Learning Points

- Difference between local execution and Intune execution context
- User vs System execution context
- Intune script assignment behavior
- Intune Management Extension troubleshooting
- Importance of remediation scripts and execution policies

### Resolution

Hyper-V was enabled locally to continue lab building.

---

# ZIP File Deployment Project (Real-World Scenario)

## Scenario

Simulated a real school IT deployment scenario where exam ZIP files need to be distributed to multiple computers without using USB drives.

Goal:
- Deploy ZIP file silently to managed devices
- Copy ZIP directly into a user's Documents folder
- Prevent student access
- Reduce manual deployment workload

---

# PowerShell Deployment Script

```powershell
$source = "$PSScriptRoot\ComputerSciencePaper1.zip"
$destination = "C:\Users\RaviGordon\Documents\ComputerSciencePaper1.zip"

Copy-Item -Path $source -Destination $destination -Force
```

---

# Packaging Process

## Folder Structure

```text
ExamDeploy
│
├── Deploy-Exam.ps1
└── ComputerSciencePaper1.zip
```

---

# Intune Packaging Tool

Used:
- Microsoft Win32 Content Prep Tool

Generated:
```text
Deploy-Exam.intunewin
```

---

# Install Command

```powershell
powershell.exe -ExecutionPolicy Bypass -File Deploy-Exam.ps1
```

---

# Detection Rule

## Rule Type
- File

## Path
```text
C:\Users\RaviGordon\Documents
```

## File
```text
ComputerSciencePaper1.zip
```

## Detection Method
- File or folder exists

---

# Key Learning Points

- Packaging PowerShell deployments as Win32 apps
- Deploying non-application content through Intune
- File-based detection rules
- User-context deployments
- Real-world school IT deployment workflows
- Endpoint management scalability

---

# Real-World Use Case

This workflow can be adapted in production environments to:

- Deploy exam files
- Push resources to teacher accounts
- Distribute scripts or templates
- Avoid USB-based deployments
- Automate file distribution across classrooms

---

# Skills Developed

- Microsoft Intune administration
- Entra ID device management
- Win32 app packaging
- Silent installations
- PowerShell scripting
- Detection rule configuration
- Endpoint troubleshooting
- Company Portal deployments
- User vs system deployment context
- Real-world endpoint management workflows

---

# Next Steps

- Deploy Hyper-V successfully through Intune
- Test remediation scripts
- Implement compliance policies
- Configure update rings
- Test BitLocker policies
- Integrate additional Microsoft 365 security features
- Continue building scalable endpoint management workflows
