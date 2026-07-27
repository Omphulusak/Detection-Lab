# MITRE ATT&CK Mapping

| Stage | Technique | MITRE ID |
|---------|-----------|-----------|
| Initial Access | Brute Force | T1110 |
| Discovery | Account Discovery | T1087 |
| Discovery | System Information Discovery | T1082 |
| Execution | PowerShell | T1059.001 |
| Command & Control | Application Layer Protocol | T1071.001 |
| Collection | Data from Local System | T1005 |

---

## Attack Flow

```
Initial Access
      │
      ▼
Discovery
      │
      ▼
Payload Execution
      │
      ▼
Command & Control
      │
      ▼
Detection
      │
      ▼
Investigation
```
