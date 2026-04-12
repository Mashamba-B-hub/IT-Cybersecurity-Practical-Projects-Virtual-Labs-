## Enterprise Active Directory Environment
# Overview

This project demonstrates the deployment and configuration of an enterprise-level Active Directory environment using Windows Server 2022. The lab simulates a real-world business network where a Domain Controller is configured to manage users, devices, and policies centrally.

The implementation includes Active Directory Domain Services (AD DS), DNS integration, DHCP configuration, Organizational Units (OUs), user and group management, and Group Policy Objects (GPOs).

# Environment Setup
Domain Controller:
Windows Server 2022 (DC01)
Roles: AD DS, DNS, DHCP
Client Machine:
Windows 10 (CLIENT01)
Domain-joined workstation
Virtualisation Platform:
Hyper-V / VirtualBox
Network Type:
Private/Internal Network

# Architecture Diagram

Located in: diagrams/active-directory-network-topoplogy.png
Located in: diagrams/visio-active-directory-diagram.png

This diagram illustrates:

Domain Controller (DC01)
Client machine (Workstation 001-024)
Internal network structure
DNS and DHCP flow

# Configurations Performed
1. Domain Controller Setup
Installed Windows Server 2022
Configured a static IP address
Renamed server to DC01
Installed required server roles

See: screenshots/server-manager.png

2. Active Directory Domain Services (AD DS)
Installed the AD DS role
Promoted the server to Domain Controller
Created a new forest:
Example: company.local

3. DNS Integration
Configured DNS during AD DS installation
Verified name resolution using:
nslookup
Confirmed dynamic DNS updates

4. DHCP Configuration
Installed the DHCP Server role
Created IPv4 scope:
Defined IP range
Subnet mask
Default gateway
Configured DNS servers in scope options

See: screenshots/dhcp-scope.png

5. Organisational Units (OUs)

Created structured OUs for management:

Sales Team
Technical Team
Admin

6. Users and Groups
Created domain users:
Admin users
Standard users
Created security groups:
Sales Team
James Smith

7. Group Policy (GPO)
Created and linked GPOs to OUs
Configured policies such as:
Password policies
Desktop restrictions
Security settings

See: screenshots/gpo-management.png
See: screenshots/gpo-settings.png

 8. Domain Join (Client Machine)
Connected Windows 10 client to the domain
Verified domain membership
Confirmed DHCP IP assignment using:
ipconfig /all

See: screenshots/ipconfig.png
  
# Key Features
Centralised user and device management
Automated IP address allocation via DHCP
Secure authentication using Active Directory
Policy enforcement using Group Policy
Integrated DNS for name resolution

# Key Learnings
Installed and configured Active Directory Domain Services
Managed users, groups, and organisational units
Implemented DNS and DHCP in a domain environment
Applied Group Policy for centralised control
Joined and managed client machines within a domain

# Conclusion

This project demonstrates the deployment of a fully functional enterprise Active Directory environment. It highlights essential system administration skills required in real-world IT infrastructure management.
