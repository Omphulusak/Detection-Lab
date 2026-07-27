# 09 - Detection Engineering

## Objective

Following the attack simulation, the next phase focused on developing custom detection logic within Elastic Security.

The objective was to identify malicious activity generated during the attack by analysing endpoint telemetry collected from Elastic Agent, Sysmon, Microsoft Defender, and Windows Event Logs.

Rather than relying solely on default Elastic detections, custom KQL queries were developed to improve visibility into attacker behaviour.

---

# Detection Strategy

The Detection Lab was designed to detect attacker activity throughout the attack lifecycle.

The primary telemetry sources included:

- Elastic Agent
- Sysmon
- Windows Event Logs
- Microsoft Defender

These data sources enabled visibility into process execution, authentication events, network activity, and command execution.

---

# Detection Opportunities

The simulated attack generated several high-value detection opportunities.

| Activity | Data Source |
|----------|-------------|
| RDP Authentication | Windows Security Logs |
| Process Creation | Sysmon Event ID 1 |
| Network Connections | Sysmon Event ID 3 |
| PowerShell Activity | Windows Event Logs |
| Command and Control | Sysmon & Elastic Agent |
| Defender Events | Microsoft Defender |

---

# Custom Detection Rule

To identify execution of the Mythic Apollo payload, a custom KQL rule was created.

```kql
event.code:1 and (
process.name:"svchost-mydfir.exe"
or
winlog.event_data.OriginalFileName:"Apollo.exe"
)
```

This rule detects process creation events where the renamed payload or the original Apollo filename is observed.

---

# IOC-Based Detection

Additional detections can be created using file hashes and Indicators of Compromise (IOCs).

Examples include:

- SHA256 hash
- Original filename
- Process name
- Parent process
- Command-line arguments

Using multiple indicators improves detection accuracy and reduces false positives.

---

# Investigation Fields

When analysing alerts, the following fields were reviewed:

- host.name
- user.name
- process.name
- process.parent.name
- process.command_line
- process.hash.sha256
- process.executable
- destination.ip
- destination.port

These fields help determine:

- What executed
- Who executed it
- How it started
- Whether external communication occurred

---

# Detection Workflow

```text
Attack Activity
       │
       ▼
Elastic Agent
       │
       ▼
Elasticsearch
       │
       ▼
Detection Rule
       │
       ▼
Security Alert
       │
       ▼
SOC Investigation
```

---

# MITRE ATT&CK Coverage

| Technique | MITRE ID |
|-----------|-----------|
| Brute Force | T1110 |
| Account Discovery | T1087 |
| PowerShell | T1059.001 |
| System Information Discovery | T1082 |
| Application Layer Protocol | T1071.001 |
| Data from Local System | T1005 |

---

# Lessons Learned

Creating custom detection rules demonstrated that effective detection depends on collecting high-quality telemetry and understanding attacker behaviour.

Rather than relying exclusively on built-in rules, security teams can tailor detections to their own environments, improving visibility and reducing the likelihood of missed malicious activity.

---

# Summary

At the end of this phase:

- Custom KQL detections created
- IOC-based detections developed
- Endpoint telemetry validated
- Detection workflow established

---

## Next Step

The next phase focuses on investigating the generated alerts and documenting the incident using osTicket.

➡️ **Next:** `10-Incident-Response.md`
