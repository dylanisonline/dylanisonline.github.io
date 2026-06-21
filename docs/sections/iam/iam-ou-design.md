# Organizational Unit Design

<br>

Before creating users, security groups, and administrative permissions, I first designed an Organizational Unit structure for the kojima.test domain.

<br>

The goal was to create a structure that would support:

- Clear separation between standard and privileged accounts
- Role-based access control
- Delegated Active Directory administration
- Targeted Group Policy application
- Department-specific workstation management
- Future expansion of the environment

<br>

---

#### Final Design

The completed structure separates identities, computers, roles, and resource-access groups into distinct Organizational Units.

<br>

![kojima.test domain OU structure](../../assets/images/iam/ou-structure.png){ style="width:60%; display:block; margin:0 ; border-radius:8px;" }

<br>


**Top Level OUs:**

| OU | Purpose |
|---|---|
| Kojima Users | Contains standard employee accounts | 
| Kojima Admins | Contain dedicated privilged accounts | 
| Kojima Computers | Contains domain-joined workstations and servers | 
| Kojima Roles | Contian Global security groups representing job and administrative roles | 
| Kojima Resources | Contain Domain local groups representing permissions and access to resources | 

<br>


---



### Identity OUs

The identity OUs separate standard employee accounts from privileged administrative accounts.

<br>

```

Kojima 
├── Kojima Users 
│   ├── IT (Standard IT User Accounts)
│   ├── Development (Standard Development User Accounts)
│   └── Operations (Standard Operations User Accounts)
|
└── Kojima Admins 
    ├── AD Admins (Active Directory administrative Acccounts)
    ├── Server Admins (Server administrative accounts)
    └── Workstation Admins (Workstation administrative accounts)
                            
```

<br>

This separation allows standard and privileged accounts to be managed independently. Administrative accounts can later receive stricter Group Policies, logon restrictions, auditing requirements, and privileged-access controls without affecting standard user accounts.

<br>

---

### Computer OUs

The computer OUs separate member servers from end-user workstations.

<br>

```
Kojima Computers
├── Kojima Servers       (Domain-joined member servers)
└── Kojima Workstations  (Domain-joined user endpoints)
    ├── IT               (IT-assigned workstations)
    ├── Development      (Developer workstations)
    └── Operations       (Operations workstations)

```

<br>

Servers and workstations are stored separately because they require different security baselines, administrative controls, and Group Policy settings.

The workstation structure is further divided by department so that policies can be applied only where they are needed.

For example:

- Development workstations may receive approved local-administrator access and development tooling.
- Operations workstations may receive a more restrictive standard-user configuration.
- IT workstations may receive administrative utilities and support tools.

<br>

---

<br>

### Roles OUs

The role OUs contain Global security groups that describe what an account does within the organization.

<br>

```

Kojima Roles
├── Admin Roles          (Domain-joined member servers)
└── Department Roles     (Domain-joined user endpoints)
    ├── IT               (IT department role groups)
    ├── Development      (Development department role groups)
    └── Operations       (Operations department role groups)


```

<br>

Department role groups will represent normal organizational membership.

Examples include:

- GG-Role-IT-Staff
- GG-Role-Development-Staff
- GG-Role-Operations-Staff

Administrative role groups will represent elevated responsibilities.

Examples include:

- GG-Role-IT-AD-Administrator
- GG-Role-IT-System-Administrator
- GG-Role-IT-Helpdesk-Analyst

<br>

---

<br>

### Resource OUs

<br>

```

Kojima Resources
├── Domain Access (Delegated Active Directory permissions)
├── Computer Access (Workstation, server, and management access)
└── File Shares (NTFS and share-permission groups)

```
<br>

Examples include:

- DL-AD-Password-Reset
- DL-AD-Workstation-Onboarding
- DL-All-Workstations-LocalAdmins
- DL-FS01-Operations-Modify

<br>

---

<br>