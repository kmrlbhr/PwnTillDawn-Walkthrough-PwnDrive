# PwnTillDawn - Week 3 Lab: First Beginner Box

## Target Profile
* **Hostname: PwnDrive** 
* **IP Address: 10.150.150.11**
* **Operating System: Windows** 
* **Objective: Retrieve FLAG1**

## 🛠️ Phase 1: Environment Setup & Connection
To interact with the target network, I first downloaded the unique Connection Pack from the PwnTillDawn portal. I established a secure tunnel using OpenVPN:

```bash
# Connect to the PwnTillDawn VPN
sudo openvpn PwnTillDawn.ovpn
```
## 🛠️ Phase 2: Environment Setup & Connection
To interact with the target network, I first downloaded the unique Connection Pack from the PwnTillDawn portal. I established a secure tunnel using OpenVPN:
Bash
# Sweep the network for active hosts
```nmap -sn 10.150.150.10-254```
(Note: Identified the target IP. For this write-up, it will be referred to as 10.150.150.X)

2. Service Enumeration
After identifying the target, I ran a detailed Nmap scan to find open ports, running services, and potential entry points:

```Bash
# Scan the specific IP for service versions and default scripts
nmap -sV -sC 10.150.150.X
Scan Results:

Port 21: FTP (File Transfer Protocol) - Open

Port 80: HTTP (Web Server) - Open
```
🔓 Phase 3: Gaining Access
I started by investigating the web server running on Port 80.

Navigated to http://10.150.150.11 in the browser.

Discovered an administrator login portal.

Attempted to bypass authentication using common default credentials.

Exploitation:

Username: admin

Password: admin

🚩 Phase 4: Capture The Flag (Post-Exploitation)
Once authenticated as an administrator, I explored the dashboard interface. I successfully located the target file named flag.txt.

When i opened flag.txt, it show the flag "PwnTillDawnIsAwesome!!!"
