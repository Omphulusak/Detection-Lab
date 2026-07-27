# 10 - Incident Response

## Objective

After detecting malicious activity within Elastic Security, the next phase involved investigating the alerts and documenting the incident using a structured incident response process.

The objective was to validate the alerts, determine whether they represented a true positive, identify the affected systems, and recommend appropriate remediation actions.

---

# Incident Response Workflow

The Detection Lab followed the workflow below.

```text
Attack Simulation
        │
        ▼
Elastic Detection
        │
        ▼
Security Alert
        │
        ▼
Alert Investigation
        │
        ▼
Incident Classification
        │
        ▼
Remediation
        │
        ▼
Documentation
```

---

# Alert Validation

Each alert was reviewed to determine:

- Detection Rule
- Time Generated
- Host Name
- User Account
- Event Source
- Severity
- Process Information

This information provided the context required to begin the investigation.

---

# Investigation Process

The following telemetry was analysed during the investigation:

- Process Creation Events
- Parent Process
- Command-line Arguments
- Network Connections
- PowerShell Activity
- Windows Defender Events
- Windows Event Logs

The collected telemetry helped reconstruct the attack timeline and identify attacker activity.

---

# Indicators of Compromise (IOCs)

The following indicators were identified during the investigation.

| Indicator | Description |
|-----------|-------------|
| svchost-mydfir.exe | Renamed Apollo payload |
| Apollo.exe | Original filename |
| HTTP Callback | Mythic Command & Control |
| Sysmon Event ID 1 | Process Creation |
| RDP Authentication | Initial Access |

---

# Incident Classification

The investigation concluded that the activity represented a **True Positive**.

### Reason

The collected telemetry confirmed that:

- A simulated attacker successfully accessed the endpoint.
- The Apollo payload executed successfully.
- Command and Control communication was established.
- Endpoint telemetry matched the expected attack behaviour.

---

# Recommended Remediation

If this activity occurred in a production environment, the following actions would be recommended:

- Isolate the affected endpoint.
- Terminate the malicious process.
- Remove the payload.
- Reset compromised credentials.
- Review Windows Event Logs.
- Investigate additional endpoints.
- Continue monitoring for similar indicators.

---

# osTicket Integration

To improve incident management, osTicket was deployed within the Detection Lab.

The intended workflow was:

```text
Elastic Alert
      │
      ▼
Security Investigation
      │
      ▼
osTicket Incident
      │
      ▼
Remediation
```

During testing, Elastic successfully communicated with the osTicket web server.

However, automatic incident creation through the osTicket API returned HTTP 500 responses and was not fully completed during the project.

The issue was investigated by reviewing Apache, PHP, and osTicket logs and has been documented as future work.

---

# Lessons Learned

Incident response extends beyond detecting malicious activity.

Effective investigations require:

- Validating alerts
- Collecting evidence
- Identifying Indicators of Compromise
- Documenting findings
- Recommending remediation actions

The project demonstrated the importance of integrating detection platforms with incident management systems to support efficient SOC operations.

---

# Summary

At the end of this phase:

- Alerts investigated
- True Positive confirmed
- Indicators of Compromise identified
- Remediation recommendations documented
- osTicket deployment completed
- API integration partially implemented

---

## Next Step

The next document summarises the project, key lessons learned, and planned future improvements.

➡️ **Next:** `11-Lessons-Learned.md`
