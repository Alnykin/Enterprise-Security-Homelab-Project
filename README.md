# Enterprise Security Homelab Project

## Overview
This project involved building a virtualized homelab designed to simulate the core components of a corporate network. The goal was to develop hands-on experience with enterprise infrastructure, identity management, endpoint administration, centralized monitoring, and defensive security operations. The lab also serves as a flexible foundation for future exercises and attack-and-defense scenarios.

## Network Architecture

![Alt text](https://github.com/Alnykin/Enterprise-Security-Homelab-Project/blob/main/Network%20Layout.png)

The environment consists of six virtual machines, each fulfilling a specific role within the network. We have Active Directory for centralized authentication, an administrative jump box for controlled access to services, a dedicated security server with Wazuh SIEM monitoring, and a MailHog server for internal email functionality and testing. The environment also includes a separate Windows, Linux, and security-focused workstation to simulate user and analyst activity.

#### Network Layout: 10.0.0.0/24
| System | IP Address | Operating System |
|--------|------------|------------------|
| Domain Controller | 10.0.0.5 | Windows Server 2025 |
| Corporate Server | 10.0.0.8 | Ubuntu Server |
| Security Server | 10.0.0.10 | Ubuntu Desktop |
| Security Toolbox | 10.0.0.103 | Security Onion |
| Windows Workstation | 10.0.0.100 | Windows 11 Enterprise |
| Linux Workstation | 10.0.0.101 | Ubuntu Desktop |

### Setup Details

#### Domain Controller - [8d6-labs-dc] 
Acts as the core infrastructure server, running Active Directory Domain Services, DNS, DHCP, File and Storage Services, and IIS to provide centralized authentication, networking, shared storage, and internal web hosting.

#### Corporate Server - [8d6-labs-corp-svrt] 
This is our jumpbox server. From here, we provision and access services such as FTP, DNS, and email. By limiting administrative access through a dedicated jumpbox, we reduce the network’s attack surface.

#### Security Server - [8d6-labs-sec-box]
Serves as a domain-connected security management host. Centralizes security tooling, logs, alerts, and vulnerability data for the environment. Separating it from the main server improves performance, protects data, and reflects realistic deployment practices.

#### Security Workstation [8d6-labs-sec-work]
This is our Security Onion system. It acts as the analyst-facing monitoring box for reviewing network activity and conudcting investigation.

#### Windows Workstation - [8d6-labs-win-client] 
Emulates a Windows host.

#### Linux Workstation - [8d6-labs-linux-client]
Emulates a Linux host.


## Enterprise Tools + Defense

### Microsoft Active Directory
Active Directory serves as the identity and access management backbone of the lab environment. It is used to manage user accounts, authenticate systems, enforce permissions, and simulate enterprise-style administration across domain-joined systems.

### Wazuh
Wazuh acts as the lab’s primary host-based monitoring and detection platform. It is used to collect and analyze logs from systems in the network, detect and generate alerts for security-relevant events, and provide centralized visibility into endpoint and server behavior. 

### Security Onion
Security Onion is an open-source Linux distribution designed for threat hunting, enterprise security monitoring, and log management. In this lab, it complements Wazuh by providing network-level analysis and support for incident investigation. It also includes a suite of integrated security tools, such as Zeek, Suricata, the Elastic Stack, CyberChef, and a dedicated web interface.

### MailHog
MailHog provides a safe internal mail testing capability. Rather than sending messages to real external inboxes, it captures application-generated email locally for review through a web interface. It supports testing workflows involving notifications, account actions, and other email-dependent behavior without requiring an external mail service.

---
![Alt tezt](https://github.com/Alnykin/Enterprise-Security-Homelab-Project/blob/main/images/ADComputersEndState.png)

*End State of Active Directory with Connected Computers*

![Alt text](https://github.com/Alnykin/Enterprise-Security-Homelab-Project/blob/main/images/ADUsersEndState.png)

*End State of Active Directory with Connected Users*

![Alt text](https://github.com/Alnykin/Enterprise-Security-Homelab-Project/blob/main/images/VMEndState.png)

*End State of VMs*

# Full Write-up and Notes
Download the full PDF write-up below, or view directly within GitHub from the file viewer at the top of this page.

[![PDF](https://img.shields.io/badge/view_full_project_writeup-blue?style=for-the-badge)](https://github.com/user-attachments/files/25952371/Enterprise.Security.Homelab.Project.Write-up.pdf)



