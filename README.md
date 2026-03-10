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

## Security Tools + Defense

### Microsoft Active Directory
Active Directory serves as the identity and access management backbone of the lab environment. It is used to manage user accounts, authenticate systems, enforce permissions, and simulate enterprise-style administration across domain-joined systems.

### Wazuh
Wazuh acts as the lab’s primary host-based monitoring and detection platform. It is used to collect and analyze logs from systems in the network, detect security-relevant activity such as authentication events, and provide centralized visibility into endpoint and server behavior. In practice, it supports hands-on work with log analysis, alert review, vulnerability visibility, and defensive monitoring across the domain-based environment.

### Security Onion
Security Onion is an open-source Linux distribution designed for threat hunting, enterprise security monitoring, and log management. In this lab, it complements Wazuh by providing network-level analysis and support for incident investigation. It also includes a suite of integrated security tools, such as Zeek, Suricata, the Elastic Stack, CyberChef, and a dedicated web interface.

### MailHog
MailHog provides a safe internal mail testing capability within the lab environment. Rather than sending messages to real external inboxes, it captures application-generated email locally for review through a web interface. In this lab, it supports testing workflows involving notifications, account actions, and other email-dependent behavior without requiring an external mail service.
