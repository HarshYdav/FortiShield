# 🛠 Installation Guide — Wazuh + Sysmon Endpoint Detection Lab

This installation guide helps you set up:
- Wazuh Manager & Dashboard
- Wazuh Windows Agent
- Sysmon with configuration
- Log forwarding & detection testing

---

# 1️⃣ Install Wazuh (Docker Version — Recommended)

Clone repository:
```bash
git clone https://github.com/wazuh/wazuh-docker.git
cd wazuh-docker/single-node
```

Start Wazuh:
```bash
docker compose up -d
```

Check containers:
```bash
docker ps
```

---

# 2️⃣ Install Wazuh Agent (Windows)

Download installer:
```powershell
Invoke-WebRequest -Uri "https://packages.wazuh.com/4.x/windows/wazuh-agent.msi" -OutFile "wazuh-agent.msi"
msiexec /i wazuh-agent.msi /quiet
```

Restart Agent:
```powershell
Restart-Service -Name wazuh-agent
```

Check Agent Status:
```powershell
Get-Service -Name wazuh-agent
```

---

# 3️⃣ Install Sysmon (Windows)

Download Sysmon:
```powershell
Invoke-WebRequest -Uri "https://download.sysinternals.com/files/Sysmon.zip" -OutFile "Sysmon.zip"
Expand-Archive .\Sysmon.zip -DestinationPath "C:\Sysmon"
```

Install Sysmon with Config:
```powershell
C:\Sysmon\Sysmon64.exe -accepteula -i C:\Sysmon\sysmon-config.xml
```

Verify Sysmon:
```powershell
Get-Service sysmon
C:\Sysmon\Sysmon64.exe -c
```

Check events:
```powershell
Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" -MaxEvents 20
```

---

# 4️⃣ Verify Manager Logs

```bash
sudo tail -f /var/ossec/logs/ossec.log
```

---

# 5️⃣ Simulate Test Alerts

Example command:
```powershell
powershell -nop -w hidden -enc <base64>
```

(This triggers benign detection events for testing.)

---
