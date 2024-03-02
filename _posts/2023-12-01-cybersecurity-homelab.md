---
layout: post
tags: [virtualization, VMware]
---

**Technologies:** `VMware` `Pfsense` `Ubuntu` `Security Onion` `Metaploitable2`

<br>


### Why create a homelab?
---
Creating a virtual homelab offers a cost-effective and convenient means of exploring diverse IT and cybersecurity configurations. Virtualization technology enables users to replicate complex network environments and test various security setups without the need for expensive physical hardware. With the flexibility to adjust settings and resources according to individual needs, homelabs provide a safe and scalable platform for hands-on learning and skill development in cybersecurity. For this particular environment, I am using [VMware Workstation Pro 17]() as a hypervisor.

<br>

### Motivation
---
I am currently trying to break into the cybersecurity industry and I understand concepts better once I get hands-on experience. This lab will allow me to get real world experience with defense concepts and this environment will help me begin understanding the fundamentals of penetration testing.


<br>


### Lab Components
---
<br>

| Machine               | Description |
| ---                   | ---         |
| **Kali Linux**        | Threat Actor machine that will try to break into the metasploitable server |
| **Metasploitable2**   | A deliberately vulnerable Linux server.                                    |
| **Security Onion**    | IDS / IPS Solution for monitoring our environment and observing attacks.   |
| **Analyst Machine**   | A computer that can access Security Onion Services.                        |
| **Pfsense**           | Firewall / Routing Solution.                                               |
| **Net Admin Machine** | Computer used to configure firewall settings.

<br>

### Test Bench Configuration
---
**CPU:** Ryzen 9

**Memory:** 32 GB DDR4

**Storage:** 1 TB SSD

**Operating System:** Ubuntu 23.04 x86_64

*To follow along with this lab, a large amount of memory will be the most useful hardware component*

<br>


### Steps
---
1. [Configure Pfsense](homelab-part-1) 
2. [Configuring Security Onion](homelab-part-2)
3. [Connecting End Machines]()
4. [Scanning Network]()
5. [Basic Attacks]()
6. [Next Steps]()

<br>


##### Inspirations / Sources: [Cyberwox Academy]()

<br>

