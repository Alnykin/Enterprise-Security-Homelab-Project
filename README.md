# Enterprise Security Homelab Project

## Overview
This project documents the deployment of a virtualized homelab simulating the core components of a corporate network. The lab was built to develop hands-on experience with enterprise infrastructure, identity management, endpoint administration, centralized monitoring, and defensive security operations. 

## Architecture

This environment consists of seven virtual machines, each fulfilling a distinct role within the network. Core services include Active Directory for centralized authentication and identity management, a jumpbox for controlled access to internal systems, Wazuh for security monitoring and log analysis, and a MailHog server for internal email functionality and testing.

#### Network Layout: 10.0.0.0/24
| System | IP Address | Operating System |
|--------|------------|------------------|
| Domain Controller | 10.0.0.5 | Windows Server 2025 |
| Corporate Server | 10.0.0.8 | Ubuntu Server |
| Security Server | 10.0.0.10 | Ubuntu Desktop |
| Security Toolbox | 10.0.0.103 | Security Onion |
| Windows Workstation | 10.0.0.100 | Windows 11 Enterprise |
| Linux Workstation | 10.0.0.101 | Ubuntu Desktop |
| Attacker Machine | Dynamic | Kali Linux |

##Security Tooling

