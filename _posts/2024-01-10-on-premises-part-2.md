---
layout: post
author: Dylan Phan
tags: [virtualization, VMware]
---


# Routing and Firewall Setup

In this part of the Active Directory "On-Premises" Lab series, I will go over how I configured a pfsense machine to be the routing and firewall solution for this environment.

<br>

**Networks**:
- Infrastructure Network (LAN): 
- Database Network (OPT1):
- Workstation Network (OP2):
- Splunk Network (OP3):

<br>

## Configuring VMware Virtual Networks
---
In creating this lab, I've realized that for some reason the Linux Version of VMware Workstation requires manually configuring the Virtual Networks

#### 1. Edit -> Virtual Network Editor
#### 2. Create new virtual networks
#### 3. Final Result:

![vmnet settings](https://i.imgur.com/9MfIoBa.png)

<br>


## Creating Pfsense Virtual Machine
---
The first virtual machine to be created is the pfsense machine as it manages the segmentation of our network.

#### 1. Create new virtual machine.
#### 2. Choose the pfsense ISO
#### 3. Settings used for Pfsense hardware:

![alt](https://i.imgur.com/Kkn3Tt9.png)

#### 4. Boot up Pfsense VM
#### 5. Use default settings throughout the wizard
#### 6. Reboot into machine

<br>


## Assigning Interfaces
---
#### 1. Option `1` on config console
#### 2. Options for assignment

| Assignment | Interface |
| --- | --- |
| WAN | em0 |
| LAN | em1 |
| OPT1 | em2 |
| OPT2 | em3 |
| OPT3 | em4 |

<br>

### Configuring IP Addresses
---

#### 1. Option `2` on config console
#### 2. Used the following options:

| Interface Name | IP Address  | IP Address Range             | Subnet Mask | DHCP |
| ---            | ---         | ---                          | ---         | ---  |
| LAN            | 192.168.1.1 | 192.168.1.11 - 192.168.1.200 | /24         | Yes  |
| OPT1           | 192.168.2.1 | 192.168.2.11 - 192.168.2.200 | /24         | No   |
| OPT2           | 192.168.3.1 | 192.168.3.11 - 192.168.3.200 | /24         | No   |
| OPT3           | 192.168.4.1 | 192.168.4.11 - 192.168.4.200 | /24         | No   |


#### 3. Final Result: 

<br>



#### [Return to Home Article](active-directory), [Go to Previous Step](on-premises-part-1), [Go to Next Step](on-premises-part-3)


