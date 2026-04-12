## Enterprise Network Design (SAM–ELLA Topology)

This project is a dual-site network design built using Cisco routers and switches in Cisco Packet Tracer. It demonstrates IPv4 and IPv6 configuration, static routing, and inter-network connectivity between two LANs connected through an ISP router.

## Project Overview

# The network consists of:

SAM Site (172.23.16.0/24 + IPv6)
ELLA Site (192.168.0.0/24 + IPv6)
Core Router (SAM-N-ELLA-RTR)
ISP Router
Interconnected using point-to-point /30 links

# The design supports:

IPv4 static routing
IPv6 static routing
Default routes
End-to-end connectivity between LANs
Network Topology

# IP Addressing Scheme

# IPv4 Networks
SAM LAN: 172.23.16.0/24
ELLA LAN: 192.168.0.0/24
WAN Links: 10.0.0.0/30, 10.0.0.4/30, 10.0.0.8/30

# IPv6 Networks
2001:DB8:9876::/64 (SAM side)
2001:DB8:9876:2::/64 (ELLA side)
2001:DB8:9876:1::/64 (core links)
2001:DB8:9876:3::/64 & 4::/64 (WAN/ISP links)

# Technologies Used
Cisco Routers & Switches
IPv4 Addressing
IPv6 Dual Stack
Static Routing
Default Routes
VLAN Interface (SVI)
Basic Security (password encryption)

# Key Configurations

# Switch Configuration
VLAN 1 management IP
Console & VTY password security
Password encryption enabled

# Router Configuration
Interface IP assignment (IPv4 + IPv6)
Static routes for inter-network communication
Default routes to the ISP
