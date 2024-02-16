---
layout: post
author: Dylan Phan
tags: [🚧, Active Directory, VMware]
---

<br>

The reality of building an on-prem setup can be very tedious and expensive due to the amount of equipment required. Instead of investing all of that money into learning the basics of Active Directory, this enviornment will use 
a virtalized setting to implement this setup. The following machines will be used in this lab:

<br>

| Machine Name | Description  |
| --------- | ---------- |
| WIN-DC     | A windows server machine that will act as the domain controller for this environment      |
| WIN-SQL    | A windows SQL server that will be managed by the domain controller |
| WORK-1     | A windows workstation with access to the SQL Server |
| WORK-2     | A windows workstation that CANNOT access the SQL Server |
| NET-ADMIN | A linx machine that will be used to configure our firewall |
| PFSENSE | Our firewall and Routing 

<br>

### Hypervisor
---
In this lab, I will be using VMware Workstation Pro to create the Active Directory Environment


<br>

### My Hardware Setup
---
- **Laptop**: Asus ROG Strix G15 Advantage Edition
- **CPU**: AMD Ryzen 9
- **RAM**: 32 GB DDR4 
- **GPU**: AMD 6800XT
- **Storage**: 1TB SSD 

<br>

### Getting Images and File structure
---

#### 1. Windows Server and Desktop



#### 2. Ubuntu Desktop


#### 3. Pfsense



<br>

##### [Return to Home Article](active-directory), [Go to Next Step (Part 2 - Configuring the firewall)](on-premises-part-2)