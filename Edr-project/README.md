
<div align="center">

# 🛡️ EDR-Project  — Wazuh SIEM | Threat Detection & Log Monitoring

<!-- BADGES ROW 1 -->
<img src="https://img.shields.io/badge/SIEM-WAZUH-blue?style=for-the-badge&logo=wazuh&logoColor=white" alt="Wazuh" />
<img src="https://img.shields.io/badge/ATTACKER-KALI_LINUX-red?style=for-the-badge&logo=kalilinux&logoColor=white" alt="Kali Linux" />
<img src="https://img.shields.io/badge/ENDPOINT-WINDOWS_10-blue?style=for-the-badge&logo=windows&logoColor=white" alt="Windows 10" />

<!-- BADGES ROW 2 -->
<br>
<img src="https://img.shields.io/badge/STATUS-COMPLETED-brightgreen?style=for-the-badge" alt="Status" />
<img src="https://img.shields.io/badge/PLATFORM-VIRTUALBOX-orange?style=for-the-badge&logo=virtualbox&logoColor=white" alt="Platform" />

<br>
<br>

**A practical cybersecurity End-Point Detection lab focused on SIEM monitoring, endpoint security, threat detection, vulnerability assessment, and incident response using industry-relevant tools.**

</div>

---

## 📌 Project Overview

This project builds a functional SOC environment from scratch, where cyberattacks are generated, monitored, detected, and investigated using SIEM technology. It replicates the core workflow of a real SOC analyst 
---

## 🏗️ Lab Architecture

*(Add a diagram or description of your setup here)*

*   **SIEM:** Wazuh Manager (Ubuntu Server)
*   **Attacker:** Kali Linux
*   **Endpoint:** Windows 10 (with Sysmon installed)
*   **Hypervisor:** VirtualBox

---

## 🎯 Objectives

*   Deploy and configure Wazuh SIEM.
*   Configure Windows 10 to forward logs and Sysmon events to Wazuh.
*   Simulate real-world attacks using Kali Linux (e.g., Nmap scans, brute force, Mimikatz).
*   Create custom detection rules and alerts.
*   Investigate alerts and map them to the MITRE ATT&CK framework.

---

## 🚀 Step-by-Step Implementation

### 1. SIEM Deployment (Wazuh)

### 2. Endpoint Configuration (Windows 10)
*(Explain installing the Wazuh agent and Sysmon)*

### 3. Attack Simulation (Kali Linux)
*(List the tools used, e.g., Hydra, Nmap, Metasploit)*

### 4. Threat Detection & Investigation
*(Show screenshots of the Wazuh dashboard detecting the attacks)*

---

## 🛠️ Tools Used

*   [Wazuh](https://wazuh.com/) (SIEM & XDR)
*   [VirtualBox](https://www.virtualbox.org/) (Virtualization)
*   [Kali Linux](https://www.kali.org/) (Attacker Machine)
*   [Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon) (Windows Event Monitoring)
*   [MITRE ATT&CK](https://attack.mitre.org/) (Threat Intelligence)

---

## 📸 Screenshots


`![Dashboard](link-to-your-image.png)`
[Sysmon Configure] <img width="1024" height="768" alt="configure-sysmon" src="https://github.com/user-attachments/assets/ec2016e8-c2cc-4d10-8776-040502a4697b"/>


---

## 📚 Lessons Learned

*   Explain what you learned about log ingestion.
*   Explain how you tuned out false positives.
*   the challenges of configuring Sysmon failed to xml configuration.

---

<div align="center">
  <i>Built for educational purposes to enhance Blue Team skills.</i>
</div>
