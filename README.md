<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=header&text=Cybersecurity%20Projects&fontSize=44&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=SOC%20%7C%20Detection%20Engineering%20%7C%20Incident%20Response%20%7C%20Malware%20Analysis&descAlignY=60&descSize=16" alt="header"/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&pause=1200&color=36BCF7&center=true&vCenter=true&width=700&lines=Hands-on+SOC+projects;Detection+engineering+in+Microsoft+Sentinel;Incident+response+%26+threat+hunting;Windows+internals+%26+malware+analysis)](https://git.io/typing-svg)

![IBM-QRadar](https://img.shields.io/badge/IBM%20QRadar-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Splunk](https://img.shields.io/badge/Splunk-000000?style=for-the-badge&logo=splunk&logoColor=white)
![Elastic](https://img.shields.io/badge/Elastic-005571?style=for-the-badge&logo=elastic&logoColor=white)
![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows11&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white)
![Okta](https://img.shields.io/badge/Okta-007DC1?style=for-the-badge&logo=okta&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C%2FC%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)

![License](https://img.shields.io/badge/License-Unlicense-blue?style=flat-square)
![Focus](https://img.shields.io/badge/Focus-Blue%20Team%20%2F%20SOC-informational?style=flat-square)
![MITRE](https://img.shields.io/badge/Mapped%20to-MITRE%20ATT%26CK-red?style=flat-square)
![Status](https://img.shields.io/badge/Status-Actively%20Updated-brightgreen?style=flat-square)

</div>

---

## 👤 About

| | |
|---|---|
| **Author** | Anas Mateen|
| **Repo** | [github.com/xxx/xx](https://github.com/xxx/xx) |
| **Email** | [![Gmail](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:anasmateen@email.com) |
| **LinkedIn** | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anas-mateen-2371a9373/) |

Hands-on security projects focused on **Soc-Analyst work**: detection engineering in Microsoft Sentinel, incident response,

---

## 🗂️ Labs and Projects

| | Project | What it covers |
|:-:|---|---|
| 🛡️ | <a href="https://github.com/AnasMateen369/Detection-Lab">Detection-Lab</a> |Deployed the Splunk Universal Forwarder on a Windows target to capture and centralize Security Event Logs, specifically engineering alerts to detect Event ID 4625 (Failed Account Logins) for real-time brute-force threat identification.
|
| 🧬 | [**edr-project/**](/edr-project) | Custom Windows EDR prototype detecting in-memory process injection (hollowing, shellcode remote thread, image-based) using a kernel driver, user-mode hook DLL, and rules-based chain scoring. Includes a layered Authenticode trust subsystem (path + LOLBin denylist + embedded/catalog signature verification) for false-positive suppression. Validated against SnakeKeylogger and a Defender-evasive injection sample. |
| 🚨 | [**incident-response/**](/incident-response) | Case studies linking malware behavior, Sentinel detections, and analyst actions (triage → containment → recovery). |
| 🎣 | [**phishing-analysis/**](/phishing-analysis) | Triage of real phishing emails: header and `Received` chain analysis, SPF/DKIM/DMARC verdicts, URL and infrastructure assessment, IOC extraction, written verdicts and recommended actions. |
| 🦠 | [**malware-analysis/**](/malware-analysis) | Isolated lab for manual Windows malware analysis (ProcMon, Wireshark). Behaviors and TTPs documented per sample: SnakeKeylogger, Agent Tesla, Pulsar/Quasar RAT, WannaCry. |
| 🔍 | [**vulnerability-management-lab/**](/vulnerability-management-lab) | Nessus Essentials and OpenVAS (Greenbone): scanning, triage, validation, prioritization, remediation, verification. Featured finding takes one critical (an unauthenticated root backdoor) end to end: manual validation, root-cause analysis, verified fix, two-scanner comparison. |
| 🧱 | [**legacy-sentinel-lab/**](/legacy-sentinel-lab) | Foundational Microsoft Sentinel lab (architecture + detections). The associated IR case study lives in [**incident-response/**](/incident-response). |

---

## 🛡️ Detection Lab Breakdown

<details>
<summary><b>Click to expand: detections included in <code>detection-lab/</code></b></summary>

<br>

### 🏢 Active Directory (6 detections)
![AD](https://img.shields.io/badge/Active%20Directory-0078D4?style=flat-square&logo=microsoft&logoColor=white)

| Detection | MITRE ATT&CK |
|---|---|
| Password spray | T1110.003 |
| Kerberoasting | T1558.003 |
| AS-REP roasting | T1558.004 |
| DCSync | T1003.006 |
| Privileged group changes | T1098 |
| GPO abuse | T1484.001 |

### 🔐 Okta Identity (4 detections)
![Okta](https://img.shields.io/badge/Okta-007DC1?style=flat-square&logo=okta&logoColor=white)

| Detection | MITRE ATT&CK |
|---|---|
| Password spray | T1110.003 |
| MFA fatigue | T1621 |
| Admin role grant | T1098.003 |
| Policy tampering | T1562 |

### ☁️ Entra ID (3 detections)
![Entra](https://img.shields.io/badge/Entra%20ID-0089D6?style=flat-square&logo=microsoftazure&logoColor=white)

| Detection | MITRE ATT&CK |
|---|---|
| Privileged role grant | T1098.003 |
| Credential added to an app | T1098.001 |
| OAuth permission grant | T1528 |

### 🦠 Extras
- Malware behavior detections built from, and validated against, samples from my own malware analysis
- Sentinel → Velociraptor automated response playbook

</details>

---

## 🔄 Workflow Across Projects

```mermaid
flowchart LR
    A[Malware Analysis] --> B[Behavior and TTPs]
    B --> C[Sentinel Detections]
    C --> D[Alert Triage]
    D --> E[Containment]
    E --> F[Recovery]
    F --> G[Lessons Learned]
    G --> C
```

---

## 🧰 Tech Stack

<div align="center">

| Category | Tools |
|---|---|
| **SIEM / XDR** | Microsoft Sentinel, Splunk, Elastic Security, Defender XDR |
| **Query languages** | KQL, SPL, Sigma |
| **Endpoint / DFIR** | Sysmon, Velociraptor, Hayabusa, Chainsaw, EvtxECmd |
| **Network** | Wireshark, Zeek, Suricata |
| **Malware analysis** | ProcMon, Any.run, Hybrid Analysis, VirusTotal, CyberChef |
| **Vuln management** | Nessus Essentials, OpenVAS (Greenbone) |
| **Identity** | Active Directory, Entra ID,|

</div>

---

## 📜 License

![License](https://img.shields.io/badge/License-The%20Unlicense-blue?style=for-the-badge)

Released into the public domain under **The Unlicense**.

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,50:203a43,100:0f2027&height=100&section=footer" alt="footer"/>

</div>
