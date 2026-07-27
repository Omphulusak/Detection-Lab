# 01 - Lab Overview

## Detection Lab Architecture

The following diagram illustrates the complete Detection Lab environment, including the Vultr cloud infrastructure, Elastic Stack, Fleet Server, Windows endpoint, Mythic C2 server, and osTicket integration.

![Detection Lab Architecture](../architecture/detection-lab-architecture.png)

## Introduction

The Detection Lab is an end-to-end Security Operations Center (SOC) environment built to simulate realistic cyber attacks and demonstrate the complete blue team workflow.

The project combines enterprise security tools to collect endpoint telemetry, detect malicious activity, investigate alerts, and document incidents.

Rather than focusing on a single technology, the lab demonstrates how multiple security platforms integrate to support modern security operations.

---

# Project Goals

The primary objectives of this project were to:

- Build a cloud-based SOC environment.
- Deploy a centralized SIEM platform.
- Collect Windows endpoint telemetry.
- Simulate realistic attacker behaviour.
- Develop custom detection rules.
- Investigate alerts using Elastic Security.
- Document incident response procedures.
- Integrate a ticketing platform into the investigation workflow.

---

# Lab Components

The Detection Lab consists of the following systems.

| Component | Purpose |
|----------|---------|
| Ubuntu Server | Hosts Elasticsearch, Kibana and Fleet |
| Windows Server 2025 | Target endpoint used for monitoring and attack simulation |
| Kali Linux | Attack machine |
| Mythic C2 | Command and Control framework used for adversary simulation |
| osTicket | Incident management platform |

---

# Detection Workflow

The project follows the complete SOC lifecycle.

```text
Infrastructure Deployment
          │
          ▼
Telemetry Collection
          │
          ▼
Attack Simulation
          │
          ▼
Detection Engineering
          │
          ▼
Alert Investigation
          │
          ▼
Incident Response
```

---

# Skills Demonstrated

Throughout this project, the following skills were developed and demonstrated:

- Cloud Infrastructure Deployment
- SIEM Administration
- Endpoint Monitoring
- Detection Engineering
- Threat Hunting
- Windows Event Analysis
- Incident Response
- Technical Troubleshooting
- Security Documentation

---

# What You'll Learn

This repository documents the complete deployment process and demonstrates how security professionals can build a practical Detection Lab using freely available tools and cloud infrastructure.

Each section builds on the previous one, taking the reader from infrastructure deployment through attack simulation, detection engineering, and incident response.

---

# Next Step

The next document covers the deployment of the cloud infrastructure that forms the foundation of the Detection Lab.

➡️ **Next:** `02-Infrastructure.md`
