# 📜 Commands Used — Wazuh + Sysmon Endpoint Detection Lab

A complete list of commands used in this project.

---

# 🔧 Sysmon Commands

Download:
```powershell
Invoke-WebRequest -Uri "https://download.sysinternals.com/files/Sysmon.zip" -OutFile "Sysmon.zip"
```

Extract:
```powershell
Expand-Archive .\Sysmon.zip -DestinationPath "C:\Sysmon"
```

Install:
```powershell
C:\Sysmon\Sysmon64.exe -accepteula -i C:\Sysmon\sysmon-config.xml
```

Check config:
```powershell
C:\Sysmon\Sysmon64.exe -c
```

View events:
```powershell
Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" -MaxEvents 20
```

---

# 🔧 Wazuh Docker Commands

Start:
```bash
docker compose up -d
```

Stop:
```bash
docker compose down
```

Check containers:
```bash
docker ps
```

---

# 🔧 Wazuh Linux Services

Start:
```bash
sudo systemctl start wazuh-indexer
sudo systemctl start wazuh-manager
sudo systemctl start wazuh-dashboard
```

Restart:
```bash
sudo systemctl restart wazuh-manager
```

Status:
```bash
sudo systemctl status wazuh-manager
```

---

# 🔧 Wazuh Agent (Windows)

Restart:
```powershell
Restart-Service -Name wazuh-agent
```

Check:
```powershell
Get-Service wazuh-agent
```

Log file:
```powershell
type "C:\Program Files (x86)\ossec-agent\ossec.log"
```

---

# 🔧 Git Commands

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```

---
