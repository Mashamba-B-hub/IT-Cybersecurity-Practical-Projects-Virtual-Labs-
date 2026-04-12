## Network Diagrams Documentation
# Overview

This folder contains network diagrams created to visually represent the architecture of the Enterprise Active Directory Environment. The diagrams illustrate how the Domain Controller, client machine, and network services (DNS and DHCP) are connected within the environment.

Two diagram tools were used:

Cisco Packet Tracer (for network simulation)
Microsoft Visio (for professional network design)

# Diagram Description

The network topology includes:

Domain Controller (DC01)
Hosts:
Active Directory Domain Services (AD DS)
DNS Server
DHCP Server
Client Machine (Workstation 001 -024)
Joined the domain
Receives IP configuration from DHCP
Network Components
Private/Internal network connection
IP addressing scheme
DNS name resolution flow
DHCP IP assignment process

# Network Flow Explanation
The DHCP Server automatically assigns IP addresses to client machines
The DNS Server resolves domain names to IP addresses
The Domain Controller authenticates users and manages resources
The Client Machine communicates with the Domain Controller for login and access

# Notes
The Cisco Packet Tracer diagram was used to simulate the logical network setup
The Visio diagram was created to present a clean and professional network layout
Both diagrams represent the same environment but from different perspectives:
Simulation view (Packet Tracer)
Documentation view (Visio)

# Purpose
These diagrams help to:

Visualise the network structure and components
Understand how services interact within the domain
Support the configuration and implementation steps
Provide clear documentation for reporting and assessment
