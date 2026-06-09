# Day-14 – Bulk User Creation, Windows Provisioning Packages & PowerShell Fundamentals

## 🎯 Objective

Continue progressing through the MS-102 learning path by exploring:

- Bulk user creation
- User administration
- Windows provisioning
- PowerShell fundamentals
- Remote administration concepts
- Event log management

---

## 👥 Bulk User Creation

Explored bulk user creation using the Microsoft 365 graphical administration portal.

Used Microsoft's CSV template functionality to import multiple users simultaneously.

Users created:

```plaintext
Declan Rice
William Saliba
David Raya
```

After creation, assigned users to:

```plaintext
Arsenal Security Group
```

This provided practical experience with:

- Bulk user onboarding
- CSV imports
- Group membership assignments
- Administrative efficiency

---

## 📊 Learning Reflection – Bulk Administration

A useful takeaway was understanding how bulk administration can reduce repetitive tasks.

Rather than creating users individually:

```plaintext
User 1
User 2
User 3
```

administrators can leverage:

```plaintext
CSV Imports
↓
Bulk Creation
↓
Group Assignments
```

to improve efficiency.

---

## 💻 Real-World Ticket – Windows Provisioning Package

Worked on a production support ticket involving Windows device provisioning.

Created a provisioning package using:

```plaintext
Windows Configuration Designer
```

---

### Deployment Process

Created:

```plaintext
Provisioning Package (.ppkg)
```

Copied package to USB media.

Deployment process:

```plaintext
Insert USB
↓
Boot Device
↓
Press F12
↓
Launch Provisioning Process
↓
Apply Configuration Package
```

Successfully deployed the provisioning package to a laptop.

---

## 🧠 Skills Practised

- Windows Configuration Designer
- Provisioning packages
- USB deployment
- Device onboarding
- Windows deployment workflows

---

## ⚡ PowerShell Fundamentals

Started the PowerShell section of the MS-102 course.

PowerShell is Microsoft's command-line and automation framework used to manage Windows systems, Microsoft 365 services, and Azure resources.

---

## 🔧 Service Management

Reviewed commands for managing Windows services.

### View Services

```powershell
Get-Service
```

Purpose:

Display all services and their current status.

---

### Start Service

```powershell
Start-Service -Name winrm
```

Purpose:

Start the Windows Remote Management service.

---

### Stop Service

```powershell
Stop-Service -Name winrm
```

Purpose:

Stop the Windows Remote Management service.

---

## 🌐 Remote Administration

Explored PowerShell remoting concepts.

### Query Remote Services

```powershell
Get-Service -ComputerName CLIENT10
```

Purpose:

Retrieve service information from a remote device.

---

### Remote Session

```powershell
Enter-PSSession -ComputerName CLIENT10
```

Purpose:

Create an interactive PowerShell session on a remote computer.

---

## 🖥️ Process Management

### View Running Processes

```powershell
Get-Process
```

Purpose:

Display running processes on the local machine.

---

### Export Remote Processes

```powershell
Get-Process -ComputerName CLIENT10,CLIENT11,CLIENT12 | Out-File C:\clientprocesses.txt
```

Purpose:

Collect process information from multiple devices and save results to a file.

---

## 📚 Command Discovery

Explored how PowerShell commands are structured.

### List Available Commands

```powershell
Get-Command
```

---

### Commands Using "Get"

```powershell
Get-Command -Verb Get
```

---

### Commands Using "Net"

```powershell
Get-Command -Noun Net*
```

Purpose:

Identify networking-related cmdlets.

---

## 📖 Help System

Reviewed PowerShell help functionality.

```powershell
Get-Help Get-EventLog
```

Purpose:

Access built-in documentation for PowerShell commands.

---

## 📜 Event Log Management

### View Security Logs

```powershell
Get-EventLog -LogName Security -Newest 10
```

Purpose:

Retrieve recent security log entries.

---

### Format Output

```powershell
Get-EventLog -LogName Security -Newest 10 | Format-List
```

Purpose:

Improve readability of event log output.

---

### Export Logs

```powershell
Get-EventLog -LogName Security -Newest 10 | Format-List | Out-File C:\security_log.txt
```

Purpose:

Save event log output to a file for analysis.

---

## 📦 Variables

Introduced PowerShell variables.

### Store Computer Name

```powershell
$computername = "CLIENT10"
```

---

### Simple Arithmetic

```powershell
$num1 = 1
$num2 = 2

$num1 + $num2
```

Result:

```plaintext
3
```

---

## 🔒 Execution Policies

Reviewed PowerShell execution policies.

### Check Policy

```powershell
Get-ExecutionPolicy
```

Purpose:

View current script execution restrictions.

---

### Bypass Policy

```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass
```

Purpose:

Temporarily allow unrestricted script execution.

Note:

Use with caution in production environments.

---

## 📚 Learning Reflection

Today's learning introduced the foundations of PowerShell administration.

Key areas explored:

```plaintext
Bulk User Management
Provisioning Packages
PowerShell Commands
Remote Administration
Event Logs
Variables
Execution Policies
```

One major takeaway was seeing how PowerShell enables administrators to move beyond graphical interfaces and begin automating repetitive tasks.

This aligns closely with the broader goal of:

```plaintext
Work Smart
↓
Automate
↓
Scale
```

rather than performing repetitive actions manually.

---

## 🔜 Next Steps

Potential future labs:

- Create PowerShell scripts
- Explore PowerShell remoting further
- Automate user management tasks
- Learn Microsoft Graph PowerShell
- Continue MS-102 PowerShell modules
- Expand Windows provisioning knowledge
