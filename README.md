# Enterprise Active Directory & File Server Lab

Simulated a full university-style Windows Server 2022 environment with Active Directory, secure file server, Group Policy automation, and FSRM for data governance. Built using VMware virtualization to mimic real enterprise infrastructure.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Architecture Diagram](#architecture-diagram)
3. [Infrastructure & Identity Setup](#infrastructure--identity-setup)
4. [File Server Engineering](#file-server-engineering)
5. [Group Policy Automation](#group-policy-automation)
6. [Security & FSRM](#security--fsrm)
7. [Troubleshooting](#troubleshooting)
8. [Skills Demonstrated](#skills-demonstrated)
9. [Screenshots](#screenshots)


## Project Overview

This lab simulates a real-world enterprise Active Directory environment for a university scenario. 
The environment includes:

- Domain Controller (Windows Server 2022) named as: UNI-DC
- Member File Server named "Uni-FS."
- Client PCs (Windows 10/11)
- Secure file storage with advanced NTFS permissions
- Group Policy automation for drive mapping and folder redirection
- File Server Resource Manager (FSRM) for file screening
- Enable access based Enumeration
- Virtualized setup using VMware/Hyper-V


## Architecture Diagram

The network topology of the lab environment:

- DC1: Domain Controller (technova.edu)
- Uni-FS: Member File Server
- Client PC: Domain-joined Windows 10/11
- DNS: Points to DC1

![Network Diagram](Simple-Network-Diagram/network-frame.png)



## Infrastructure & Identity Setup

In this step, the Active Directory domain and foundational identity structure were built to simulate a real enterprise environment.

- Installed **Windows Server 2022** and configured **Domain Controller (DC1)**.
- Created Active Directory domain: **technova.edu**.
- Designed Organizational Units (OUs) to logically separate accounts:
  - **Students OU**
  - **Staff OU**
  - **Admins OU**
- Created Security Groups for scalable permission management:
  - **Business_Students**
  - **Staff_Group**
  - **Admin_Group**
- Joined secondary server **Uni-FS** to the domain for file server integration.
- Entire environment virtualized using **VMware/Hyper-V**.

### Screenshots

To demonstrate the setup and provide visual proof:

1. **AD Structure & Security Groups**  
   Shows the OU hierarchy and groups created.  
   ![AD Structure](Screenshots/Active-Directory-Users-and-Computers/DC-ADUC.png)

2. **Domain Controller Roles** *(Optional but recommended)*  
   Shows that **AD DS** and **DNS** roles are installed and domain name is `technova.edu`.  
   ![DC Roles](Screenshots/Active-Directory-Users-and-Computers/DC-localserver.png)

3. **Member Server Join** *(Optional but recommended)*  
   Shows that Uni-FS is successfully joined to the domain.  
   ![Member Server Join](Screenshots/Active-Directory-Users-and-Computers/FS-domain-connected.png)


