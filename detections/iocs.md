# Indicators of Compromise (IOCs)

## Overview

During the attack simulation, several Indicators of Compromise (IOCs) were generated. These indicators can be used by security analysts to identify malicious activity across Windows endpoints.

---

# File Indicators

| Indicator | Value |
|------------|-------|
| Original Filename | Apollo.exe |
| Renamed Payload | svchost-mydfir.exe |

---

# Hash Indicators

| Algorithm | Value |
|------------|-------|
| SHA256 | F7C5E379EB75272ACB213B26DB08C16A4F7FAC9191126FFB82152EFDAB7CE693 |

---

# Behavioural Indicators

- Process Creation (Sysmon Event ID 1)
- HTTP Command & Control
- RDP Authentication
- Discovery Commands
- PowerShell Activity
- Parent-Child Process Relationships

---

# Detection Opportunities

- File Hash Detection
- Original Filename Detection
- Process Name Detection
- Network Connection Detection
- Behavioural Analytics

---

# MITRE ATT&CK

| Technique | ID |
|------------|----|
| Command and Scripting Interpreter | T1059 |
| Application Layer Protocol | T1071.001 |
| Brute Force | T1110 |
| Data from Local System | T1005 |
