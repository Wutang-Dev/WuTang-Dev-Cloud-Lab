# Day-08 – Intune Application Deployment Validation & Security Group Testing

## 🎯 Objective

Validate an end-to-end Microsoft Intune application deployment workflow using a dedicated security group.

Goal:

- Test security group targeting
- Validate Win32 app deployment
- Confirm successful endpoint installation
- Review deployment reporting inside Intune

---

## 🧪 Lab Scenario

Following the previous lab where dedicated endpoint security groups were created, the next step was to validate whether group-based application deployments functioned correctly.

Lab target:

```plaintext
Lab-Security-Group
```

Current membership:

```plaintext
WT-LAB-01
```

(Currently the only enrolled endpoint inside the security group.)

---

## 💻 Application Tested

Application selected:

```plaintext
Google Chrome
```

Deployment method:

```plaintext
Windows Win32 Application
(.intunewin)
```

Google Chrome had already been configured within the Intune tenant.

The objective was to test deployment targeting against the newly created endpoint group.

---

## ⚙️ Deployment Configuration

Updated the Google Chrome deployment assignment.

Assigned security group:

```plaintext
Lab-Security-Group
```

This created the following deployment workflow:

```plaintext
Security Group
↓
App Assignment
↓
Endpoint Targeting
↓
Deployment Processing
↓
Installation Validation
```

---

## 🚀 Deployment Execution

Triggered deployment against the target group.

Target device:

```plaintext
WT-LAB-01
```

Allowed Intune policy/application processing to complete.

Validated deployment through:

```plaintext
Microsoft Intune Admin Center
→ Apps
→ Windows Apps
→ Google Chrome
→ Device Install Status
```

---

## ✅ Deployment Results

Successful deployment confirmed.

Device status showed:

```plaintext
RYZEN-LAB — Installed
WT-LAB-01 — Installed
```

WT-LAB-01 successfully received the deployment after being added to:

```plaintext
Lab-Security-Group
```

Observed status:

```plaintext
Installed
```

No failures reported.

No pending installations reported.

---

## 📊 Skills Practised

This lab provided practical experience with:

- Microsoft Intune application deployment
- Security group targeting
- Win32 application assignments
- Endpoint deployment workflows
- Device installation monitoring
- Intune reporting validation

---

## 🔐 Group Deployment Validation

Successfully confirmed that the newly created:

```plaintext
Lab-Security-Group
```

is functioning correctly as a deployment target.

This establishes a controlled deployment model for future labs.

Potential future use cases:

- Pilot application rollouts
- Compliance policy testing
- Configuration profile assignments
- Deployment troubleshooting
- Safe pre-production validation

---

## 📚 Learning Reflection

Today's lab reinforced a core endpoint administration workflow:

```plaintext
Create Security Group
↓
Assign Deployment
↓
Target Device
↓
Sync / Process Policy
↓
Validate Installation
↓
Review Reporting
```

This moves the environment closer to a structured endpoint management model similar to real-world enterprise workflows.

Practical implementation continues to reinforce MS-102 learning through direct tenant experience rather than theory alone.

---

## 🔜 Next Steps

Potential follow-up labs:

- Deploy **7-Zip** to Lab-Security-Group
- Deploy **LibreOffice** to Toshiba endpoints
- Test configuration profile assignments
- Create first compliance policy baseline
- Compare **Test-Group** vs **Lab-Security-Group** deployment strategies
- Enroll and validate WT-LAB-02 and WT-LAB-03 deployments
