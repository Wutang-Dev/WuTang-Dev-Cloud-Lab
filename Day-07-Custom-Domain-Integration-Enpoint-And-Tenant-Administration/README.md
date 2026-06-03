# Day-07 – Custom Domain Integration, Endpoint Enrollment & Tenant Administration

## 🎯 Objective

Continue expanding the Microsoft 365 / Intune lab environment by:

- Practising custom domain integration
- Standardising endpoint naming
- Expanding Intune device management
- Creating security groups for controlled deployments
- Building familiarity with Microsoft 365 tenant administration

---

## ☁️ Custom Domain Configuration

Purchased a custom domain from GoDaddy to practise real-world Microsoft 365 domain administration.

Domain purchased:

```plaintext
rg-wutanglan.co.uk
```

Added the domain into the Microsoft 365 tenant.

### Steps Performed

```plaintext
Settings
→ Domains
→ Add Domain
→ Verify Ownership
→ Set as Default Domain
```

After successful verification, updated the tenant default domain.

Before:

```plaintext
rg@wutanglan20.onmicrosoft.com
```

After:

```plaintext
rg@rg-wutanglan.co.uk
```

---

## 👥 User Identity Management

Updated existing user accounts to align with the new custom domain.

### Primary Admin Account

Before:

```plaintext
rg@wutanglan20.onmicrosoft.com
```

After:

```plaintext
rg@rg-wutanglan.co.uk
```

---

### Lab User Updates

Updated existing tenant users.

Users modified:

```plaintext
Saka
Yamal
```

New format:

```plaintext
bsaka@rg-wutanglan.co.uk
byamal@rg-wutanglan.co.uk
```

This provided additional practice with:

- Microsoft 365 user administration
- Identity management
- Custom domain user assignments

---

## 🧪 Security Group Configuration

Created deployment and endpoint management groups to support future testing workflows.

### Test Deployment Group

Created:

```plaintext
Test-Group
```

Purpose:

Used as a controlled pilot environment before wider deployment.

Added device:

```plaintext
RYZEN-LAB
```

Future use cases:

- Application testing
- Compliance policy testing
- Configuration profile validation
- Controlled deployment troubleshooting

---

### Endpoint Security Group

Created:

```plaintext
Lab-Security-Group
```

Purpose:

Dedicated security group for lab endpoints.

Designed for:

- Application deployments
- Compliance targeting
- Configuration profile assignments
- Endpoint segmentation

---

## 💻 Endpoint Standardisation — Toshiba Lab Devices

Prepared newly acquired Toshiba devices for cloud endpoint management.

Applied a consistent device naming convention.

Renamed devices:

```plaintext
WT-LAB-01
WT-LAB-02
WT-LAB-03
```

Purpose:

Introduce standardised endpoint naming practices similar to production environments.

---

## 🔐 Intune Device Enrollment

Successfully enrolled Toshiba lab devices into Microsoft Intune.

Devices enrolled:

```plaintext
WT-LAB-01
WT-LAB-02
WT-LAB-03
```

Validated enrollment inside:

```plaintext
Microsoft Intune Admin Center
```

Confirmed:

- Device visibility
- Successful registration
- Endpoint availability for future deployment testing

---

## 🛡️ Security Group Assignment

After successful enrollment, assigned lab devices into the newly created endpoint security group.

Group:

```plaintext
Lab-Security-Group
```

Devices added:

```plaintext
WT-LAB-01
WT-LAB-02
WT-LAB-03
```

This prepares the environment for future:

- App deployments
- Compliance policy assignments
- Configuration profile testing
- Endpoint management labs

---

## ⚙️ Microsoft 365 Tenant Exploration

Spent additional time exploring Microsoft 365 administration settings to improve overall tenant familiarity.

### Organisation Settings

Reviewed:

- General tenant settings
- Administrative configuration options

---

### Themes & Branding

Experimented with:

- Tenant themes
- Appearance customisation
- UI branding settings

May have got slightly carried away 😂😂😂

---

### Service Health

Started exploring:

```plaintext
Health
→ Service Health
```

Reviewed concepts around:

- Microsoft service incidents
- Advisory notifications
- Platform health monitoring
- Tenant operational visibility

---

## 📚 Learning Reflection

Today's session focused entirely on practical Microsoft tenant administration.

Areas covered:

```plaintext
Custom Domains
Identity Management
Security Groups
Endpoint Enrollment
Intune Administration
Tenant Familiarisation
```

No Proxmox work completed today — intentional prioritisation to focus on cloud endpoint administration and Microsoft tenant learning.

Still aligned with current learning philosophy:

> Turn up every day. Learn practically. Improve incrementally.

---

## 🔜 Next Steps

Planned follow-up labs:

- Validate application deployment using **Lab-Security-Group**
- Test app assignments against **Test-Group**
- Begin compliance policy experimentation
- Continue MS-102 learning implementation
- Resume Proxmox homelab progression
