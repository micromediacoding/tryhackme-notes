# 🛡️ SOC Home Lab – Wazuh SIEM Detection

![Wazuh](https://img.shields.io/badge/SIEM-Wazuh-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-green)
![Attack](https://img.shields.io/badge/Attack-SSH%20Brute%20Force-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

SOC Home Lab with Wazuh SIEM for security monitoring, SSH attack detection, and log analysis across Windows and Linux systems
---


## 📌 Overview


This project demonstrates a **hands-on SOC (Security Operations Center) lab** where real-world attack scenarios were simulated and analyzed using **Wazuh SIEM**.

The focus of this lab is to detect and analyze **SSH brute-force attacks**, perform **log analysis**, and understand how alerts are generated and investigated across Windows and Linux systems.

#### ⚙️ Setup Guide
##### 👉 [![Setup Guide](https://img.shields.io/badge/Setup-Guide-blue)](setup-guide.md)



---

## 🧭 Lab Architecture

```text
Kali Linux (Attacker)
        ↓
SSH Brute Force Attack
        ↓
Windows / Linux Targets
        ↓
Wazuh Agent → Wazuh Server → Dashboard
```

## 🖥️ Wazuh Setup

 ### Wazuh Web Interface

<img src="screenshots/wazuh-webpage.png" width="800"/>

### Wazuh Dashboard

<img src="screenshots/wazuh-dashboard.png" width="800" style="border-radius:10px"/>

### Wazuh Endpoints (Agents)

<img src="screenshots/wazuh-endpoints.png" width="800"/>

## 🧠 MITRE ATT&CK Mapping

| Technique | ID | Description |
|----------|----|------------|
| Brute Force | T1110 | Repeated login attempts using SSH |
| Valid Accounts | T1078 | Successful login after multiple failures |


## 🚨 Attack Simulation – SSH Brute Force

• Simulated SSH login attempts from Kali Linux

• Generated multiple failed authentication logs

• Observed attack detection in Wazuh SIEM

## 🔍 Detection Logic

- Multiple failed login attempts (Event ID 4625)
- Followed by a successful login (Event ID 4624)
- Indicates potential brute-force attack

## 🔍 Log Analysis

### 🪟 Windows Log Analysis

#### • Event ID 4625 → Failed login attempts

#### • Event ID 4624 → Successful login

<img src="screenshots/failed-attempt-log-analysis.png" width="700"/> 

<img src="screenshots/login-success-log-analysis.png" width="700"/>

 ## Multiple Failed Attempts Detection
 
• Detected repeated login failures

• Identified potential brute-force attack pattern

<img src="screenshots/multiple-failed-attempt-events.png" width="700"/>

## 🚀 Key Outcomes

✔️ Built a SOC lab using Wazuh SIEM  
✔️ Simulated SSH brute-force attacks  
✔️ Detected authentication failures  
✔️ Correlated logs to identify attack patterns  
✔️ Performed alert investigation  

## 💼 Use Case

This project simulates a real SOC scenario where an analyst monitors authentication logs to detect brute-force attacks and investigates suspicious login patterns.


## 🎯 Skills Demonstrated

#### • SIEM: Wazuh

#### • Log Analysis (Windows & Linux)

#### • Security Monitoring & Alert Investigation

#### • SSH Brute-force Attack Simulation

#### • Event Correlation

## 🔗 Connect With Me

#### 💼 LinkedIn: https://linkedin.com/in/manoj-root
#### 🌐 Portfolio: https://www.cybergodfather.me/
#### 🐙 GitHub: https://github.com/Manoj-Root


