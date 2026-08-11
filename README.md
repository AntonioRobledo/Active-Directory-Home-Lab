# Active Directory Home Lab
 
A self-directed home lab built to develop hands-on Active Directory administration skills, using Hyper-V to virtualize a Windows Server domain controller and a Windows 11 Pro client.
 
## Overview
 
This lab simulates a small enterprise environment to practice core AD administration tasks: directory structure design, user/group/computer object management, Group Policy configuration, and account lifecycle management.
 
**Environment:**
- **Hypervisor:** Microsoft Hyper-V (host: Windows 10/11 PC)
- **Domain Controller:** Windows Server 2025
- **Client:** Windows 11 Pro (domain-joined)
## Architecture
 
```
Host PC (Hyper-V)
├── VM 1: Domain Controller (Windows Server 2025)
│   └── Active Directory Domain Services (AD DS)
│   └── DNS
└── VM 2: Client (Windows 11 Pro)
    └── Domain-joined workstation
```
 
## Setup Workflow
 
### 1. Hyper-V & Virtual Machine Provisioning
- Enabled Hyper-V role on host PC
- Created a virtual switch to provide networking between host and VMs
- Provisioned two VMs: one for the domain controller, one for the Windows 11 Pro client
- Allocated virtual resources (CPU, RAM, disk) appropriate for each role
### 2. Domain Controller Setup
- Installed Windows Server 2025 on the domain controller VM
- Assigned a static IP address for network stability
- Installed the **Active Directory Domain Services (AD DS)** role
- Promoted the server to a domain controller and established a new forest/domain
- Configured DNS to support domain name resolution
### 3. Directory Structure & Object Creation
- Designed an Organizational Unit (OU) structure to simulate an enterprise directory
- Created **user accounts** representing simulated employees
- Created **computer objects** for domain-joined machines
- Created **security groups** to manage access/permissions
- Created **distribution lists** to simulate email group functionality
### 4. Client Domain Join
- Configured the Windows 11 Pro client VM's network settings to point to the domain controller for DNS
- Joined the client VM to the domain
- Verified connectivity and domain authentication from the client
### 5. Group Policy Configuration
- Created Group Policy Objects (GPOs) for select OUs
- Applied GPOs to manage client-side configuration settings
- Tested policy application on the domain-joined client
### 6. Account Administration Testing
- Practiced common help-desk/AD admin tasks against the simulated directory:
  - User account creation
  - Password resets
  - Account disabling and enabling
## Skills Demonstrated
- Active Directory Domain Services (AD DS) deployment and administration
- Organizational Unit (OU) design
- User, computer, and group object management (security groups, distribution lists)
- Group Policy Object (GPO) creation and application
- Account lifecycle management (creation, password resets, enable/disable)
- Hyper-V virtualization and VM networking
## Notes
This is a self-directed learning project built to reinforce Active Directory concepts and administration workflows relevant to IT support and systems administration roles. It is not a production environment.

I also decided to use the fictional Star Wars Universe to act as my supposed enterprise as it was fun and easier to remember users, groups, and who reports to who this way. 
