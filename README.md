# 🚀 Endpoint Detection & Response (EDR) Lab — Wazuh + Sysmon

A complete hands-on cybersecurity project demonstrating how Sysmon telemetry is captured on a Windows endpoint, forwarded to the Wazuh Agent, analyzed by the Wazuh Manager, and visualized in the Wazuh Dashboard.

This project simulates real-world SOC workflows, detection engineering basics, and endpoint monitoring.

---

![Header](.\images\Screenshot 2025-11-18 125344.png")

## 📌 Project Overview
This lab includes:
- Sysmon installation & configuration  
- Wazuh Manager + Dashboard setup  
- Wazuh Agent integration  
- Custom detection rules  
- Attack simulation for alert generation  
- Event analysis & MITRE ATT&CK mapping

---

## 🏗 Architecture (Overview)
Windows Endpoint → Sysmon → Wazuh Agent → Wazuh Manager (Indexer) → Wazuh Dashboard

---

## 📂 Files Included in Repository
- **README.md** — Full documentation  
- **installation-guide.md** — Step-by-step setup  
- **commands-used.md** — All commands used in the project  
- Configs, scripts, logs (optional future additions)

---

## 🛠 Features of This Lab
- Detailed Sysmon telemetry collection  
- Event forwarding to Wazuh Manager  
- Correlation rule testing  
- Alert triage and SOC-style investigation  
- Hands-on detection engineering

---

## 📘 What This Project Teaches
- Endpoint monitoring  
- SIEM fundamentals (Wazuh)  
- Telemetry processing  
- Creating and tuning detection rules  
- Investigating suspicious behavior  
- Threat mapping with MITRE ATT&CK

---

## 🧩 Future Enhancements
- Add Sigma → Wazuh rule converter  
- Add Linux endpoint monitoring  
- Add YARA scanning  
- Add advanced correlation rules

---
