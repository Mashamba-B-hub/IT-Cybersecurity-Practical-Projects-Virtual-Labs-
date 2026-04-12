# South Africa Multi-Site Network (Johannesburg, Durban & Cape Town)

## Project Overview

This project demonstrates the design, configuration, and troubleshooting of a **multi-site enterprise network** using Cisco Packet Tracer. The network connects Johannesburg, Durban, and Cape Town within a **single topology**, enabling communication between LANs and access to an external server.

The project focuses on routing, WAN connectivity, and troubleshooting to ensure successful communication across all sites.


## Objectives

- Configure routers and switches using Cisco CLI  
- Implement IPv4 addressing and subnetting  
- Establish WAN connectivity between multiple locations  
- Configure static and default routing  
- Troubleshoot connectivity to reach a remote server  
- Apply basic network security  


##  Network Design

###  LAN Networks

| Location       | Network Address | Subnet Mask       | Default Gateway |
|---------------|----------------|------------------|-----------------|
| Johannesburg  | 172.25.0.0     | 255.255.254.0    | 172.25.1.254    |
| Durban        | 172.25.2.0     | 255.255.254.0    | 172.25.3.254    |


### WAN Links

- Johannesburg - Durban - `10.10.10.0 /30`  
- Durban - Cape Town - `10.10.10.4 /30`  
- Cape Town - ISP - `203.15.5.44 /30`  


##  Configuration Summary

###  Johannesburg

#### Switch (SW-JOH)

enable
configure terminal
hostname SW-JOH

line con 0
password ADMIN
login
exit

line vty 0 15
password REMOTE
login
exit

service password-encryption
enable secret EXAM
