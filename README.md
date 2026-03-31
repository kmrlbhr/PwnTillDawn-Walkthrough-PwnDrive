# PwnTillDawn - Week 3 Lab: First Beginner Box

## 📖 Overview
This repository contains a step-by-step walkthrough for compromising the first vulnerable machine on the **PwnTillDawn** network, completed as part of the Week 3 Lab. 

* **Difficulty:** Easy
* **Network Range:** `10.150.150.10 - 10.150.150.254`
* **Objective:** Perform the stages of system hacking to find the flag (proof of compromise).

---

## 🛠️ Phase 1: Environment Setup & Connection
To interact with the target network, I first downloaded the unique Connection Pack from the PwnTillDawn portal. I established a secure tunnel using OpenVPN:

```bash
# Connect to the PwnTillDawn VPN
sudo openvpn PwnTillDawn.ovpn

## Phase 2: Target Discovery & Scanning
Once connected to the internal network, I needed to identify the active target and discover its vulnerabilities.

1. Host Discovery (Ping Scan)
I scanned the provided subnet to find the live IP address of the target machine:
