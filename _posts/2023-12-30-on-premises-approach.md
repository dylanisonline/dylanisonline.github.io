---
layout: post
author: Dylan Phan
tags: [virtualization, VMware]
---


To implement an on-premises approach of active directory, I used VMware Workstation Pro as a hypervisor solution for this environment.


### Environment Components
---
<br>

| Machine    | Description |
| ------     | ------      |
| Server     | Domain controller that will allows us to                  |
| Pfsense    | Routing and Firewall Solution                                 |
| SQL Server | A server that will only certain users will be given access to |
| Workstation 1 | Windows Workstation |
| Workstation 2 | Windows Workstation | 



### House Keeping
---

#### 1. Created a seperate folder to store system ISOs

#### 2. Created a seperate folder to store VMs for this lab:

```
Active Directory Lab
│
├───firewall
│   ├───pfsense
│        └───pfsense.vmx
│
├───servers
│   ├───domain-controller
│   	   └───DCserver.vmx
│   ├───splunk
│   	   └───SPLUNKserver.vmx
│   ├───SQL
│   	   └───SQLserver.vmx
│
└───workstations
    ├───win1
         └───WIN1.vmx
    ├───win2
         └───WIN2.vmx
	├───linux1
         └───LIN1.vmx
```

#### 4. VMware File System:

<img src="https://i.imgur.com/s697hCP.png">

<br>

## Cre