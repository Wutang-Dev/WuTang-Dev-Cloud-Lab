# Day 04 – Windows 365 Azure Network Permissions (RBAC)

## Overview  
On Day 04 of the **WuTang-Dev-Cloud Lab**, I focused on configuring the **required Azure permissions (RBAC)** to allow Windows 365 to integrate with Azure networking.

This lab followed Microsoft documentation to understand how **role-based access control (RBAC)** enables Windows 365 to interact with VNets, subnets, and other network resources.

---

## Objectives  
- Understand RBAC in Azure  
- Assign required roles for Windows 365 networking  
- Configure permissions at different scopes  
- Enable Windows 365 to use Azure Network Connections (ANC)  
- Follow Microsoft documentation for best practice  

---

## Environment  
- Platform: Microsoft Azure  
- Resource Group: LabRG  
- VNet: WutangLan1  
- Identity: Windows 365 service (group)  

**Reference:**  
https://learn.microsoft.com/en-us/windows-365/enterprise/create-azure-network-connection  

---

## Step 1 – Assign Reader Role (Subscription Level)  

Assigned the **Reader** role to allow Windows 365 to view Azure resources.

**Scope:**  
- Subscription  

**Role:**  
- Reader  

**Member:**  
- Windows 365 (group/service)  

**Outcome:**  
Windows 365 can now read Azure resource configurations.

---

## Step 2 – Assign Network Contributor (Resource Group Level)  

Granted permissions to manage network resources within the lab environment.

**Scope:**  
- Resource Group: LabRG  

**Role:**  
- Network Contributor  

**Member:**  
- Windows 365 (group/service)  

**Outcome:**  
Windows 365 can create and manage network-related resources within the resource group.

---

## Step 3 – Assign Network User (VNet Level)  

Allowed Windows 365 to use the Virtual Network.

**Scope:**  
- VNet: WutangLan1  

**Role:**  
- Network User  

**Member:**  
- Windows 365 (group/service)  

**Outcome:**  
Windows 365 can attach Cloud PCs to the VNet.

---

## Key Learnings  

- Azure uses **RBAC (Role-Based Access Control)** to manage permissions  
- Permissions can be assigned at different scopes:
  - Subscription  
  - Resource Group  
  - Resource (e.g., VNet)  
- Windows 365 requires specific roles to interact with Azure networking  
- Least privilege principle:
  - Reader → View access  
  - Network Contributor → Manage network resources  
  - Network User → Use VNet  

---

## Why This Matters  

Without these permissions:
- Windows 365 cannot connect to Azure VNets  
- Azure Network Connections (ANC) will fail  
- Cloud PCs cannot communicate with other Azure resources  

This configuration is essential for:
- Enterprise deployments  
- Hybrid networking scenarios  
- Secure cloud environments  

---

## Challenges  

- Understanding which roles are required and why  
- Navigating Azure RBAC scopes (subscription vs resource group vs VNet)  
- Interpreting Microsoft documentation  

   

---

## Summary  

In this lab, I configured the **required Azure RBAC permissions** for Windows 365 to interact with Azure networking.  

This enables Cloud PCs to securely connect to VNets and communicate with other resources, forming the foundation for **real-world enterprise cloud networking setups**.
