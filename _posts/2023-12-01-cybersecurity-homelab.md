---
layout: post
tags: [virtualization, VMware]
---


This series of post will go over how I setup my own virtualized Cybersecurity Analyst Environment using VMware.

### Why create a Homelab?
---

<img src="https://i.pinimg.com/originals/fb/5b/48/fb5b48cd0d259376d6fcd35ab8404cbf.gif" width=800 height=400>

A homelab is a safe environment for cybersecurity enthusiests to implement configurations and learn new skills with minimal risk.

<br>

### Testing Workstation
---
Virtualization can be heavy on various hardware components. Luckily, I have a good test bench for this setup, but following along with specs below mine can cause a varying outcome.

- **Laptop:** Asus ROG Strix G15 Advantage Edition
- **CPU:** AMD Ryzen 9 5900
- **RAM:** 32 GB DDR4
- **GPU:** AMD 6900XT
- **Storage:** 1TB
- **OS:** Ubuntu 22.04 x64


<br>

## Lab Components
---

<br>


| Machine       | Description           | 
| ------------- | ------------- |
| Pfsense    | Firewall / Routing Solution | 
| Security Onion    | IDS / IPS Solution that will allow monitoring of this environment.      |
| Metasploitable2 | A deliberately vulnerable server that will be targeted by our threat actor.     |
| Kali Linux | Our threat actor machine that will attempt to attack the metasploitable server.|



<br>

## Steps
---

1. [Configuring Firewall / Routing](homelab-part-1)
2. [Firewall GUI Configuraton](homelab-part-2)
3. [Setting Up Security Onion](homelab-part-3)
4. [Connecting Metasploitable Server]()
5. [Connecting Kali Attack Machine]()

<br>


##### Inspiration: [Cyberwox]()