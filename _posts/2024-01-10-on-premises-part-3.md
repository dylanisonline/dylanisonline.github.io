---
layout: post
author: Dylan Phan
tags: [🚧, Active Directory, VMware]
---

# Pfsense GUI Configuration

Now that the network segments are defined, there are more advanced options that need to be configured in the pfsense web browser interface. To interact with it, I created another virtual machine that will act as a network administrator.

<br>

## Creating Ubuntu Virtual Machine
---
#### 1. Create new virtual machine with Ubuntu ISO
#### 2. Settings for new virtual machine:

![pfsense virutal machine settings](https://i.imgur.com/x52qlms.png)

#### 3. Once install is finished install vmware tools


> sudo apt update && upgrade

> sudo apt install open-vm-tools-desktop 

<br>

## Connecting to web interface
---

#### 1. Opening Browser and Connecting to IP address of the Pfsense machine `192.168.1.1`

#### 2. Logging in with default login (username: `admin` password: `pfsense`)

![default login](https://i.imgur.com/eeEZjT8.png)

#### 3. Assign new DNS Servers. Primary: `8.8.8.8` Secondary `4.4.4.4`

![Assigning new DNS Servers](https://i.imgur.com/ZgklWnH.png)

#### 4. Allow Private and Bogon Networks to connect

![Bogon and Private Networks](https://i.imgur.com/9dYVNsi.png)

#### 5. Change default Admin Password

![Admin Password Change](https://i.imgur.com/rfwRXFo.png)

<br>

## Renaming Interfaces
---

#### 1. Interfaces -> Choose Any Interface

![Interfaces](https://i.imgur.com/9qOzu3a.png)

#### 2. Change Interface Description

![Changing interface name](https://i.imgur.com/zBOSlpo.png)

<br>

## Firewall Rules
---
For testing purposes, we will allow all traffic to flow through the network. This is not recommended for actual enterprise settings.

#### 1. Firewall -> Rules

![Firewall -> Rules](https://i.imgur.com/JzmZPqF.png)

#### 2. On every interface add a firewall rule

#### 3. Action: `pass` Protocol: `any`

![Firewall Rule](https://i.imgur.com/3kFBn7k.png)

#### 4. Save and Apply changes

<br>

#### [Return to Home Article](active-directory), [Go to Previous Step](on-premises-part-2), [Go to Next Step](on-premises-part-4)