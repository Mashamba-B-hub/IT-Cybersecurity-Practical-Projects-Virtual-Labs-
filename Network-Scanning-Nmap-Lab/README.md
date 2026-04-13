# Reconnaissance and Scanning (Nmap & Kali Linux)

## Overview

This project demonstrates active network reconnaissance and scanning techniques using Nmap within an isolated lab environment. The lab simulates the preliminary stages of penetration testing, where an attacker identifies live hosts, enumerates services, and evaluates potential vulnerabilities.

The focus of this lab is on performing structured scans, analyzing results, and understanding the impact of firewall configurations on network exposure.


## Objectives

* Perform active network reconnaissance
* Identify live hosts within a subnet
* Scan and analyze open TCP ports
* Evaluate the impact of firewall configurations
* Identify potential vulnerabilities based on scan results

## Lab Environment

### Virtual Machines

* **Attacker Machine:** Kali Linux / Windows 10

  * Tools: Nmap, Zenmap
  * IP Address: `10.0.0.101`

* **Target Server:** Windows Server 2022

  * IP Address: `10.0.0.1`

* **Target Workstation:** Windows 10

  * IP Address: `10.0.0.50`

### Network Configuration

* Subnet: `10.0.0.0/24`
* Environment: **Isolated private network (no Internet access)**
* Static IP addressing used

## Phase 1: Environment Setup

* Configured static IP addresses on all machines
* Verified all systems are on the same isolated network
* Installed Nmap (v7.98) and Zenmap GUI on the attacker machine
* Ensured firewall is initially **enabled** on all targets

## Phase 2: Network Analysis

### Step 1: Connectivity Verification (Ping)

**Purpose:** Confirm that target systems are reachable

ping 10.0.0.50
ping 10.0.0.1

**Result:**

* Successful replies confirmed connectivity


### Step 2: Host Discovery

**Purpose:** Identify active hosts on the network

nmap -sn -n -v 10.0.0.0/24

**Key Concepts:**

* Host discovery without port scanning
* No DNS resolution for faster results

**Result:**

* Identified all active devices in the subnet

### Step 3: Port Scanning & Service Enumeration

**Purpose:** Identify open ports and running services

nmap -sS -p1-1024 -sV -T4 10.0.0.0/24

**Key Concepts:**

* SYN (stealth) scan
* Banner grabbing (service/version detection)
* Timing templates for scan optimisation

**Observations:**

* With firewall ON:

  * Most ports appear **filtered**
* With firewall OFF:

  * More ports become **open/visible**
  * Increased attack surface

###  Step 4: Aggressive Scan (Advanced Enumeration)

**Purpose:** Gather detailed system and service information

nmap -A -T4 10.0.0.1

**Includes:**

* OS detection
* Service version detection
* NSE scripts
* Traceroute

##  Firewall Impact Analysis

### Firewall Enabled

* Limited exposed ports
* Reduced attack surface
* Increased security

### Firewall Disabled

* Multiple ports exposed (e.g., RPC, SMB)
* Increased vulnerability risk
* Easier service enumeration

##  Key Security Findings

* Remote Desktop (RDP) can be exposed if not restricted
* Disabling the firewall significantly increases risk
* Services such as SMB and RPC may become accessible
* Open ports provide entry points for attackers


##  Reflection & Insights

### Reliability of Results

* **Most reliable:** Open ports and live hosts
* **Least reliable:** OS detection and version guesses (affected by firewalls and virtualization)

---

### Limitations of Nmap

* Cannot fully detect application-layer vulnerabilities
* May produce false positives/negatives
* Limited accuracy in OS fingerprinting in virtual environments

### Key Takeaways

* Always verify firewall status before scanning
* Never expose administrative ports unnecessarily
* Use layered security (firewall + access control)
* Network reconnaissance is critical in identifying vulnerabilities

## Skills Demonstrated

* Network reconnaissance
* Port scanning and service enumeration
* Cybersecurity analysis
* Use of Nmap and Zenmap
* Understanding of TCP/IP networking

## Ethical Considerations

All activities were performed in a controlled lab environment. These techniques should only be used on authorized systems for ethical and legal purposes.


## Conclusion

This lab provided practical experience in reconnaissance and scanning, highlighting how attackers identify live hosts, discover open ports, and analyze services. It reinforced the importance of firewalls and secure configurations in protecting network infrastructure.
