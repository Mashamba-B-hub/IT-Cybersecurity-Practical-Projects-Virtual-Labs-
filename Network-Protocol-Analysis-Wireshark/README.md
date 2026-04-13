# Network Protocol Analysis with Wireshark

## Overview

This project demonstrates hands-on network traffic analysis using Wireshark. The objective was to capture, filter, and analyse real-time network packets to understand how communication occurs across different layers of the TCP/IP model.

The analysis focuses on key protocols such as ARP, ICMP, DNS, and TCP/HTTPS, along with practical packet filtering techniques used in network troubleshooting and monitoring.

## Tools & Environment

* **Tool Used:** Wireshark
* **Operating System:** Windows 10 / Windows 11
* **Capture Interface:** Ethernet / Wi-Fi Adapter
* **Capture Duration:** 1–2 minutes per session


## Protocol Analysis

### 1. ARP (Address Resolution Protocol)

* Captured ARP Request and Reply packets
* Analysed Layer 2 (MAC) and Layer 3 (IP) address mapping

**Key Findings:**

* Source MAC: `42:8f:6b:84:05:b4`
* Destination MAC: `74:12:b3:d2:03:61`
* Source IP: `192.168.8.1`

screenshots/arp-request.png`
screenshots/arp-reply.png`

### 2. ICMP (Ping Traffic)

* Identified Echo Request and Echo Reply packets
* Verified Layer 3 addressing within IPv4 headers

**Key Details:**

* Echo Request Type: **8 (Request)**
* Echo Reply Type: **0 (Reply)**

`screenshots/ping-request.png`
`screenshots/ping-reply.png`

### 3. DNS Analysis

* Captured DNS Query and Response traffic
* Analysed name resolution process

**Key Findings:**

* Protocol: UDP
* Source Port: `64225`
* Destination Port: `53`
* DNS Server: `192.168.8.1`
* Record Type: **A Record**
* Resolved IP: `142.251.47.168`

`screenshots/dns-query.png`
`screenshots/dns-response.png`

### 4. TCP Three-Way Handshake

The TCP connection establishment process ensures reliable communication:

1. **SYN** – Client initiates connection
2. **SYN-ACK** – Server acknowledges request
3. **ACK** – Client confirms connection

`screenshots/tcp-handshake.png`

## Findings & Insights

* ARP resolves IP addresses to MAC addresses within local networks
* ICMP is essential for connectivity testing and diagnostics
* DNS enables domain name resolution to IP addresses
* HTTPS ensures secure communication through encryption
* TCP guarantees reliable data transfer using connection-oriented communication

## Skills Demonstrated

* Network traffic capture and analysis
* TCP/IP protocol understanding
* Packet filtering and troubleshooting
* DNS and HTTP/HTTPS analysis
* Practical use of Wireshark

## Conclusion

This project provided practical experience in analysing real network traffic and understanding protocol behaviour across multiple layers. It strengthened troubleshooting skills and reinforced core networking concepts used in real-world environments.
