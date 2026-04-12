## 1. Changing Hostname

Method 1: Control Panel → System → Rename PC

Method 2: Right-click Start → System → Rename this PC

## 2. Configuring Static IP Address

Method 1:
Settings → Network & Internet → Adapter Options
Select Ethernet → Properties → IPv4 → Manual IP

Method 2:
Control Panel → Network & Internet → Network & Sharing Center
Change Adapter Settings → Ethernet → Properties → IPv4
Enter:
IP Address
Subnet Mask
Default Gateway

## 3. Configuring DNS Servers
Go to:
Network & Internet Settings → Adapter Options
Ethernet → Properties → IPv4
Add DNS Servers:
10.0.0.1
1.1.1.1
8.8.8.8
Click Advanced → DNS → Add

# Verify:
Open Command Prompt:
ipconfig /all

## 4. Enabling ICMP (Ping) in Firewall
Open:
Windows Defender Firewall with Advanced Security
Go to:
Inbound Rules
Enable:
Core Network Diagnostics – ICMP Echo Request

## 5. Creating Local Users
Right-click Start → Computer Management
Navigate to:
Local Users and Groups → Users

Create User 1:
Username: FFlintstone
Full Name: Fred Flintstone
Description: IT Manager

Create User 2:
Username: BRubble
Full Name: Barney Rubble
Description: Lawyer

##6. Assigning User to Administrator Group
Go to:
Computer Management → Local Users and Groups → Groups
Open Administrators
Click Add
Add user: FFlintstone

## 7. Date and Time Configuration
Go to:
Settings → Time & Language → Date & Time
Turn OFF:
Adjust for daylight saving time automatically

## 8. DNS Lookup Verification
Open Command Prompt:
nslookup
Check DNS server being used

## 9. Power Plan Configuration
Go to:
Settings → Power & Sleep
Set:
Screen timeout → 30 minutes
Then:
Additional Power Settings → Select High Performance

## 10. Disk Management & Mirrored Drive (RAID 1)
Open:
Right-click Start → Disk Management
Steps:
Add new disks in Hyper-V (SCSI Controller)
Initialize disks
Right-click disk → New Mirrored Volume
Add a second disk
Assign:
Drive letter: M:
Name: Data

## 11. Check Disk Utility (CHKDSK)
Open Command Prompt as Administrator:
chkdsk

## 12. Remote Desktop Protocol (RDP)
Enable RDP:
Settings → Remote Desktop → Turn ON
Connect to Remote PC:
Open the Remote Desktop Connection App
Enter:
IP address of the target PC
Username (e.g., FFlintstone)
Password

## 13. Enable Network Discovery & File Sharing
Control Panel → Network & Sharing Centre
Click:
Change Advanced Sharing Settings
Under Private Network:
Turn ON:
Network Discovery
File and Printer Sharing

## 14. Creating a Shared Folder
File Explorer → This PC → Local Disk (C:)
Right-click → New Folder
Example name: Fred Shared

## 15. Configuring Folder Sharing Permissions
Right-click folder → Properties → Sharing Tab
Click Share
Add User:
Enter username (e.g., HClement or BRubble)
Click Add
Set Permissions:
Read/Write
Click Share → Done

## 16. Firewall Rule for File Sharing
Open:
Windows Defender Firewall
Enable:
File and Printer Sharing
