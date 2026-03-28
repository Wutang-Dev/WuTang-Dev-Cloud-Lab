# Day 02 – Windows 365 Cloud PC Deployment (Entra ID)

## Overview  
On Day 02 of the **WuTang-Dev-Cloud Lab**, I deployed a **Windows 365 Cloud PC** using Microsoft’s cloud infrastructure. The goal of this lab was to understand how to provision, assign, and access a Cloud PC using **Microsoft 365**, **Entra ID**, and provisioning policies.

This is a key step in transitioning from on-prem infrastructure (MSP lab) to **cloud-based endpoint management**.

---

## Objectives  
- Deploy a Windows 365 Cloud PC  
- Assign a Windows 365 Enterprise license  
- Create and manage an Entra ID security group  
- Configure a provisioning policy  
- Assign users via group-based provisioning  
- Access the Cloud PC via the web portal  

---

## Environment  
- Platform: Microsoft 365 / Windows 365  
- Identity: Entra ID (Azure AD)  
- License: Windows 365 Enterprise  
- User: Lab Admin (self)  

---

## Step 1 – Assign Windows 365 License  

Assigned a **Windows 365 Enterprise license** to the user account.

**Path:**  
Microsoft 365 Admin Center → Users → Active Users → Licenses  

**Outcome:**  
User is now eligible for Cloud PC provisioning.

---

## Step 2 – Create Entra ID Security Group  

Created a security group to manage Cloud PC assignments.

**Group Name:**  
Microsoft-365-Entra-ID  

**Configuration:**  
- Type: Security  
- Membership: Assigned  
- Members: Lab Admin (self)  

**Outcome:**  
Group created and user added successfully.

---

## Step 3 – Create Provisioning Policy  

Created a provisioning policy to define how Cloud PCs are deployed.

**Policy Name:**  
Windows 365 Entra ID Group Provision  

**Key Configurations:**  
- Join Type: Entra ID Join  
- Region: Default (closest available)  
- Image: Windows 11  
- Network: Microsoft hosted network  

**Assignment:**  
- Target Group: Microsoft-365-Entra-ID  

**Outcome:**  
Provisioning policy successfully linked to the group.

---

## Step 4 – Automatic Cloud PC Provisioning  

Once the provisioning policy was assigned, Windows 365 automatically:

- Detected licensed users in the group  
- Began provisioning a Cloud PC  
- Completed setup in the background  

**Outcome:**  
Cloud PC provisioned without manual VM creation.

---

## Step 5 – Access Cloud PC  

Accessed the Cloud PC via the browser.

**Portal:**  
https://windows365.microsoft.com  

**Process:**  
- Logged in with Entra ID credentials  
- Selected provisioned Cloud PC  
- Launched session via browser  

**Outcome:**  
Successfully connected to Windows 365 Cloud PC.

---

## Key Learnings  

- Windows 365 abstracts traditional VM deployment (no need for Hyper-V/Azure VM setup)  
- Licensing + Group + Provisioning Policy = automated deployment  
- Entra ID plays a central role in identity and access management  
- Group-based provisioning enables scalability (enterprise use case)  
- Cloud PCs can be accessed from anywhere via browser  

---

## Challenges  

- Understanding the relationship between:  
  - License  
  - Group  
  - Provisioning Policy  

- Microsoft UI can be confusing (some options are not immediately visible)

---

## Next Steps (Day 03 Preview)  

- Configure Cloud PC settings  
- Explore Intune device management  
- Apply policies (e.g., Storage Sense, device restrictions)  
- Test management from Endpoint Manager  

---

## Summary  

In this lab, I successfully deployed a **Windows 365 Cloud PC** using **Entra ID group-based provisioning**. This demonstrates how modern organisations can deliver fully managed desktops from the cloud without relying on physical infrastructure.
