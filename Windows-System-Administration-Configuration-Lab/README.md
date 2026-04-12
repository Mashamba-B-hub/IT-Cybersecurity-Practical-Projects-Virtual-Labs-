## Windows System Administration Configuration Lab
# Overview

This project demonstrates the configuration and administration of Windows 10 and Windows 11 virtual machines in a controlled lab environment. The lab simulates a real-world IT support scenario where workstations are prepared for a business client.

The configurations include system setup, network configuration, user and group management, file sharing, storage setup, and backup procedures.

# Environment Setup
Virtual Machines:
Windows 10 (PC10)
Windows 11 (PC11)
Network Type: Private Virtual Switch
Platform Used: Hyper-V / VirtualBox
 
# Configurations Performed
1. Windows Installation & Initial Setup
Renamed machines:
Windows 10 → PC10
Windows 11 → PC11
Verified system functionality after setup

See: screenshots/hostname-change-pc10.png
see: screenshots/hostname-change-pc11.png

2. Network Configuration
Assigned static IP addresses:
PC10 → 10.0.0.10 /24
PC11 → 10.0.0.11 /24
Enabled ICMP (ping) in Windows Firewall
Verified connectivity between machines

See: screenshots/static-ip-config-pc10.png
see: screenshots/static-ip-config-pc11.png
See: screenshots/firewall-icmp.png

3. User & Group Management

Created local user accounts:

Fred Flintstone
Role: Administrator
Barney Rubble
Role: Standard User

See: screenshots/users-created.png

4. DNS Configuration

Configured multiple DNS servers:

10.0.0.1 (Local DNS)
1.1.1.1 (Cloudflare)
8.8.8.8 (Google)

See: screenshots/verify-dns.png

5. System Settings
Disabled automatic daylight saving adjustment
Set the power plan to High Performance
Configured screen timeout to 30 minutes

See: screenshots/power-plan.png

6. Storage Configuration (Windows 11)
Added two additional 2GB drives
Configured Mirrored Volume (RAID 1)
Assigned drive letter M:
Verified disks using chkdsk

See: screenshots/mirrored-drive.png
See: screenshots/verify-chkdsk.png

7. Remote Desktop Configuration
Enabled Remote Desktop on PC11
Restricted access to Fred Flintstone only

See: screenshots/remote-desktop.png

8. File Sharing & Permissions
Enabled:
Network Discovery
File and Printer Sharing
Created shared folder:
C:\Fred Shared
Permissions:
Barney Rubble → Read/Write access

9. Backup & Recovery
Created System Restore Points on both machines
Created VM checkpoints
Exported Windows 11 VM for backup

See: screenshots/restore-point.png

# Key Learnings
Configured static IP addressing and DNS settings
Managed Windows users and permissions
Implemented secure file sharing
Configured RAID storage and verified disk health
Enabled and secured remote desktop access
Practiced backup and recovery strategies

# Conclusion

This lab provided practical experience in Windows system administration, simulating tasks commonly performed by IT support professionals in a business environment.
