---
layout: post
author: Dylan Phan
tags: [virtualization, VMware]
---


# Routing and Firewall Setup

In this part of the Active Directory "On-Premises" Lab series, I will go over how I configured a pfsense machine to be the routing and firewall solution for this environment.

<br>

| IP Address  | IP Address Range | Subnet Mask | VMnet | Description |
| ---  | --- | --- | --- | --- |
| 192.168.1.1 | 192.168.1.11 - 192.168.1.200 | /24 | vmnet2 | LAN: Where network administration takes place     |
| 192.168.2.1 | 192.168.2.11 - 192.168.2.200 | /24 | vmnet3 | Database Network: Where all of the servers will be |
| 192.168.3.1 | 192.168.3.11 - 192.168.3.200 | /24 | vmnet4 | Workstation Network: Where all of the workstation PCs will be |
| 192.168.4.1 | 192.168.4.11 - 192.168.4.200 | /24 | vmnet5 | SIEM Network: Where our splunk server is located. 

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

![alt](https://i.imgur.com/9MfIoBa.png)

#### 4. Boot up Pfsense VM
#### 5. Use default settings throughout the wizard
#### 6. Reboot into machine

<br>


## Assigning Interfaces
---
#### 1. Option `2` on config console
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

#### 1. Option `3` on config console
#### 2. 

<br>



#### [Return to Home Article](active-directory), [Go to Previous Step](on-premises-part-1), [Go to Next Step](on-premises-part-3)


