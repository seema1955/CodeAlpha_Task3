# CodeAlpha_Task3
Snort IDS setup for detecting ICMP packets and monitoring live network traffic
# 🛡️ Network-Based Intrusion Detection System using Snort

This project is a part of my cybersecurity internship task to set up a **Network-Based Intrusion Detection System (NIDS)** using **Snort** on a Linux system. It demonstrates how to install, configure, and test Snort for real-time threat detection on a local network.

---

## ✅ Task Objectives

1. ✅ Set up a network-based intrusion detection system using tools like Snort or Suricata.
2. ✅ Configure rules and alerts to detect suspicious or malicious activity.
3. ✅ Monitor network traffic continuously for potential threats.
4. ✅ Implement response mechanisms for detected intrusions.

---

## 🧰 Tools Used

- 💻 OS: Ubuntu / Kali Linux
- 🐍 Tool: [Snort v2.9.20](https://www.snort.org/)
- 📡 Interface: `enxXXXXXX` (USB LAN Adapter)
- 🔧 Editors: `nano`, terminal

---

## 🔧 Setup & Configuration

### Step 1: Snort Installation

```bash
sudo apt update
sudo apt install snort

# ✅ Test the Snort configuration file
sudo snort -T -c /etc/snort/snort.conf

# 🔍 Run Snort in verbose (packet dump) mode
sudo snort -v -i <interface>

# 🧠 Run Snort in IDS mode with alerts to console
sudo snort -A console -q -c /etc/snort/snort.conf -i <interface>

# 🛠️ Edit or add local rule file
sudo nano /etc/snort/rules/local.rules

# 🧾 Example rule (ICMP ping detection)
alert icmp any any -> any any (msg:"ICMP Ping Detected"; sid:1000001; rev:1;)

# 🚦 Check IP address and interface
ip a









