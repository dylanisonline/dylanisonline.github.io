---
layout: post
author: Dylan Phan
tags: [🚧, Active Directory, VMware]
---

<br>

This series of posts will go over what Active Directory is and how to configure it based on certain conditions. (STILL IN PROGRESS)

<br>

### What is Active Directory?
---

<img src="https://miro.medium.com/v2/resize:fit:624/0*u8lSOsKnxFapY0qO.png" width=800px height=500px>

<br>

Active Directory (AD) is a directory service developed by Microsoft, primarily used in Windows environments to manage and organize network resources efficiently. At its core, Active Directory serves as a centralized database that stores information about objects within a network, such as users, computers, groups, and resources like printers and shared folders.


One of the primary functions of Active Directory is authentication and authorization. It allows users to log in securely to network resources and determines their level of access based on permissions assigned by administrators. This centralized authentication mechanism enhances security and simplifies user management across the network.

<br>

### Active Directory Services
---

**Group Policy**: Centralized management of security and configuration settings for users and computers.

**Domain Name System (DNS)**: Seamless integration with DNS for name resolution within the network.

**LDAP Directory Services**: Support for the Lightweight Directory Access Protocol (LDAP), enabling interoperability with other directory services and applications.

**Certificate Services**: Issuance and management of digital certificates for secure communication and authentication.

**Single Sign-On (SSO)**: Integration with various authentication protocols, enabling users to access multiple resources with a single set of credentials.

**Replication**: Automatic replication of directory data between domain controllers to ensure high availability and fault tolerance.

<br>

### On Premises vs. Cloud
---

**🏢 On-Prem:** On-premises Active Directory resides within an organization's physical infrastructure, necessitating hardware procurement, maintenance, and security measures. With complete control and ownership, organizations manage scalability by forecasting future needs and allocating resources accordingly. Security relies on traditional measures such as physical access controls and network security protocols.

**☁️ Cloud:** Cloud-based Active Directory, hosted on virtualized infrastructure provided by a cloud service provider, offers a managed service approach. Eliminating the need for physical hardware, organizations benefit from elastic scalability, rapid resource provisioning, and automated updates. Security measures, including encryption, multi-factor authentication, and compliance certifications, are robustly implemented by the provider. 

<br>


### Importance of Understanding Active Directory
---


<br>



### 🧙‍♂️ Choose your own Adventure
---

<br>

**On Premises Approach**

1. [Preparing our environment](on-premises-part-1)
2. [Configuring Firewall and Routing](on-premises-part-2)
3. [Pfsense GUI Configuration](on-premises-part-3)
3. [Creating Domain Controller](on-premises-part-4)
4. [Creating SQL Server and Conncting to Domain Controller](on-premises-part-5)
4. [Creating users and connecting to the Domain Controller](on-premises-part-6)
5. [Implementing SIEM](on-premises-part-7)

<br>

**Azure Approach**




<br>

##### Inspirations: [Cyberwox](), [John Hammond]()
