# 🛡️ How to Use Nmap for Ethical SSH Scanning

> ⚠️ **Educational Use Only**  
> This guide is for ethical hacking simulations on systems you own or have explicit permission to test.

---

## 📦 Requirements

- Linux (Ubuntu, Kali, Parrot OS)
- Nmap installed:
  ```bash
  sudo apt update
  sudo apt install nmap
  ```

---

## 🔍 Step 1: Discover Live Hosts

Scan your LAN to find active devices:
```bash
nmap -sn 192.168.1.0/24
```
- `-sn`: Ping scan (no ports)
- Lists online devices without probing services

---

## 🔐 Step 2: Scan for SSH (Port 22)

Check if SSH is running:
```bash
nmap -p 22 -sV 192.168.1.10
```
- `-p 22`: Scan SSH port
- `-sV`: Detect service version

**Example Output:**
```
22/tcp open  ssh     OpenSSH 8.2p1 Ubuntu
```

---

## 🧠 Step 3: OS Fingerprinting (Optional)

Try to identify the operating system:
```bash
nmap -O 192.168.1.10
```
- `-O`: OS detection (may require root)

---

## 🧨 Step 4: Aggressive Scan (All-in-One)

Run a full scan with extra details:
```bash
nmap -A 192.168.1.10
```
- Combines OS detection, version detection, script scanning, and traceroute

---

## 📁 Step 5: Save Results for Logging

Store scan output in a file:
```bash
nmap -A 192.168.1.10 -oN ssh_scan.txt
```
- `-oN`: Save as plain text

---

## 🧪 LAN Simulation Setup

- Use a Raspberry Pi or VM with SSH enabled
- Scan from your Ubuntu PC
- Log results for forensic analysis or teaching

---

## ✅ Ethical Checklist

- ✅ You own the device or have written permission
- ✅ You’re testing on a LAN or isolated lab
- ✅ You’re logging results for learning or documentation

---

## 🧰 Optional Add-ons

- MAC vendor analysis with `arp-scan`
- Timestamped logs via Flask overlay
- Visual dashboards for classroom use

---

## 🎓 Credits

Created by [catgamer19](https://github.com/catgamer19)  
For LAN-only simulations and ethical hacking education
