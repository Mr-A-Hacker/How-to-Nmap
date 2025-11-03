# How-to-Nmap

🛡️ How to Use Nmap for Ethical SSH Scanning
⚠️ Educational Use Only: This guide is for ethical hacking simulations on systems you own or have permission to test.

📦 Requirements
Linux (Ubuntu, Kali, Parrot OS)

Nmap installed:

bash
sudo apt update
sudo apt install nmap
🔍 Step 1: Discover Live Hosts
bash
nmap -sn 192.168.1.0/24
-sn: Ping scan (no ports)

Lists active devices on your LAN

🔐 Step 2: Scan for SSH (Port 22)
bash
nmap -p 22 -sV 192.168.1.10
-p 22: Scan SSH port

-sV: Detect service version

Example Output:

Code
22/tcp open  ssh     OpenSSH 8.2p1 Ubuntu
🧠 Step 3: OS Fingerprinting (Optional)
bash
nmap -O 192.168.1.10
-O: Attempts to identify the operating system

🧨 Step 4: Aggressive Scan (All-in-One)
bash
nmap -A 192.168.1.10
Combines OS detection, version detection, script scanning, and traceroute

📁 Step 5: Save Results
bash
nmap -A 192.168.1.10 -oN ssh_scan.txt
Saves output to a text file for forensic logging

🧪 Sample LAN Simulation Setup
Use a Raspberry Pi or VM with SSH enabled

Scan from your Ubuntu PC

Log results for educational analysis

✅ Ethical Checklist
✅ You own the device or have written permission

✅ You’re testing on a LAN or isolated lab

✅ You’re logging results for learning or documentation
