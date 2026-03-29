# Day 03 – Azure Virtual Network (VNet) & Windows 365 Connectivity

## Overview  
On Day 03 of the **WuTang-Dev-Cloud Lab**, I explored **Azure networking fundamentals** by creating a **Virtual Network (VNet)** to support connectivity for my Windows 365 Cloud PC.

This lab focused on understanding how cloud resources communicate within Azure, including **subnets, virtual NICs, NSGs, VNet peering**, and how **Windows 365 integrates with Azure networking**.

---

## Objectives  
- Create an Azure Virtual Network (VNet)  
- Define IP address space and subnetting  
- Understand VNet communication rules  
- Learn VNet peering basics  
- Explore Network Security Groups (NSGs)  
- Understand Azure Network Connections (Windows 365)  
- Gain exposure to VPN Gateway and ExpressRoute concepts  

---

## Environment  
- Platform: Microsoft Azure  
- Resource Group: LabRG  
- VNet Name: WutangLan1  
- Region: East US  

---

## Step 1 – Create Virtual Network  

Created a Virtual Network in Azure to simulate a cloud-based network environment.

**Configuration:**  
- Address Space: `10.1.0.0/16`  
- Subnet Name: WutangLanSubnet1  
- Subnet Range: `10.1.1.0/24`  

**Outcome:**  
VNet successfully deployed and ready for resource connectivity.

---

## Step 2 – Subnetting & IP Planning  

Defined a subnet within the VNet to segment the network.

**Key Learning:**  
- A `/16` network provides **65,536 IP addresses**  
- A `/24` subnet provides **256 IP addresses**  
- Subnets allow logical separation of resources within a VNet  

**Outcome:**  
Clear understanding of Azure subnet structure and IP allocation.

---

## Step 3 – VNet Communication  

Tested and learned how communication works inside Azure VNets.

**Key Concepts:**  
- Resources within the **same VNet** can communicate by default  
- Resources in **different subnets (same VNet)** can communicate  
- Resources in **different VNets** cannot communicate by default  

**Solution for cross-VNet communication:**  
- Use **VNet Peering**

---

## Step 4 – VNet Peering (High-Level)**  

Explored how separate VNets can communicate.

**Key Learning:**  
- VNet Peering connects two VNets privately over Azure backbone  
- No need for public internet  
- Low latency, high performance  

**Outcome:**  
Understood how to scale multi-network environments in Azure.

---

## Step 5 – Network Security Groups (NSGs)**  

Introduced to NSGs for controlling traffic.

**Key Concepts:**  
- NSGs act like a **firewall** at subnet or NIC level  
- Control inbound and outbound traffic  
- Use rules based on:
  - Source/Destination  
  - Port  
  - Protocol  

**Outcome:**  
Basic understanding of securing Azure network resources.

---

## Step 6 – Virtual NICs & Communication  

Learned how Azure resources connect to the network.

**Key Concepts:**  
- Each VM/Cloud resource uses a **Virtual Network Interface (NIC)**  
- NICs are assigned private IP addresses from the subnet  
- Communication happens via these virtual interfaces  

**Outcome:**  
Understanding of how devices communicate within Azure.

---

## Step 7 – Windows 365 & Azure Networking  

Explored how Windows 365 integrates with Azure networking.

**Key Concepts:**  
- Windows 365 uses **Azure Network Connections (ANC)**  
- Enables Cloud PCs to connect to:
  - VNets  
  - On-prem environments  
- Allows hybrid scenarios  

**Outcome:**  
Understanding of how Cloud PCs integrate into enterprise networks.

---

## Step 8 – VPN Gateway & ExpressRoute (Intro)**  

Brief introduction to hybrid connectivity options.

**VPN Gateway:**  
- Connects on-prem network to Azure over the internet  

**ExpressRoute:**  
- Private, dedicated connection to Azure  
- Higher reliability and performance  

**Outcome:**  
High-level understanding of hybrid cloud networking.

---

## Key Learnings  

- VNets are the foundation of Azure networking  
- Subnetting is critical for organisation and scalability  
- Same VNet = communication allowed by default  
- Different VNets = require peering  
- NSGs provide traffic control and security  
- Virtual NICs enable resource communication  
- Windows 365 integrates with Azure networking via ANC  
- Hybrid connectivity is possible via VPN or ExpressRoute  

---

## Challenges  

- Understanding how all components connect together (VNet, subnet, NIC, NSG)  
- Grasping the difference between VNet peering vs same VNet communication  
- Azure UI navigation and terminology  

---

## Next Steps (Day 04 Preview)  

- Deploy Azure Virtual Machines into the VNet  
- Assign NSGs and test traffic rules  
- Simulate real network scenarios (allow/deny traffic)  
- Connect resources to Windows 365 Cloud PC  

---

## Summary  

In this lab, I built a foundational understanding of **Azure Virtual Networking**, including how resources communicate, how networks are segmented, and how security is applied.

This is a critical step towards building **real-world cloud infrastructure and hybrid networking environments**.
