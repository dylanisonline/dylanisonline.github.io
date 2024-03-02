---
layout: post
tags: [virtualization, VMware]
---

## Configuring Pfsense

Pfsense is an opensource firewall and routing solution. I have already used the software previously in my Active Directory Environment project and I have found it to be
the best solution due to its simplicity and functionality.

<br>


### Networking Configuration
---

<br>

| Network     | Machine(s)                  | Description | 
| ---         | ---                         | ---         |
| 192.168.1.1 | Network Admin               | The LAN network that is set for network administration           |
| 192.168.2.1 | Metasploitable2             | The database network that will contain the vulnerable server.           |
| 192.168.3.1 | Kali                        | 'Guest' Network that will have our threat actor machine.           |
| 192.168.4.1 | Security Onion, SOC Analyst | SOC network where the IDS/IPS is housed.           |

<br>

### Pfsense VM settings
---

![Pfsense VM Settings]()


*Note: This machine requires extra interfaces so data can pass from networks over to the Security Onion Machine*

<br>

### Configuring Interfaces 
---

| Interface Name | Network Name    | VMNet  | IP Address  | Subnet Mask |
| ---            | ---             | ---    | ---         | ---         |
| em0            | WAN             | NAT    | Automatic   | Automatic   |
| em1            | LAN             | VMnet2 | 192.168.1.1 | /24         |
| em2            | Servers         | VMnet3 | 192.168.2.1 | /24         | 
| em3            | Guest Network   | VMnet4 | 192.168.3.1 | /24         |
| em4            | Security Onion  | VMnet5 | 192.168.4.1 | /24         |


<br>


### Creating a Network Admin Machine
---

<br>



### Web GUI Configuration
---

#### 1. 

<br>

#### [Return to Main Article](), [Next Part ()]()



