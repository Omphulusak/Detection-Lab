# Detection Lab

> An end-to-end Security Operations Center (SOC) Detection Lab built using Elastic Stack, Fleet, Sysmon, Microsoft Defender, Mythic C2, and osTicket to simulate real-world attacks, engineer detections, investigate alerts, and document incident response.

<p align="center">

<img src="https://img.shields.io/badge/Elastic-005571?style=for-the-badge&logo=elastic&logoColor=white"/>
<img src="https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white"/>
<img src="https://img.shields.io/badge/Kibana-005571?style=for-the-badge&logo=kibana&logoColor=white"/>
<img src="https://img.shields.io/badge/Fleet-005571?style=for-the-badge&logo=elastic&logoColor=white"/>
<img src="https://img.shields.io/badge/Elastic_Agent-005571?style=for-the-badge&logo=elastic&logoColor=white"/>

<br>

<img src="https://img.shields.io/badge/Sysmon-0078D6?style=for-the-badge&logo=windows&logoColor=white"/>
<img src="https://img.shields.io/badge/Microsoft_Defender-5E5E5E?style=for-the-badge&logo=microsoft&logoColor=white"/>
<img src="https://img.shields.io/badge/Windows_Server-0078D6?style=for-the-badge&logo=windows&logoColor=white"/>
<img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white"/>
<img src="https://img.shields.io/badge/Kali_Linux-268BEE?style=for-the-badge&logo=kalilinux&logoColor=white"/>

<br>

<img src="https://img.shields.io/badge/Mythic_C2-8A2BE2?style=for-the-badge"/>
<img src="https://img.shields.io/badge/osTicket-0099CC?style=for-the-badge"/>
<img src="https://img.shields.io/badge/KQL-FFB000?style=for-the-badge"/>
<img src="https://img.shields.io/badge/MITRE_ATT&CK-CC0000?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Vultr-007BFC?style=for-the-badge&logo=vultr&logoColor=white"/>

</p>

## Architecture

![Detection Lab Architecture](screenshots/detection-lab-architecture.png)

> An end-to-end Security Operations Center (SOC) Detection Lab built using Elastic Stack, Fleet, Sysmon, Microsoft Defender, Mythic C2, and osTicket to simulate real-world attacks, engineer detections, investigate alerts, and document incident response.

---

## Project Overview

This project demonstrates the deployment of a cloud-based Detection Lab capable of collecting endpoint telemetry, simulating adversary activity, detecting malicious behaviour, and managing security incidents.

The lab was built in Vultr Cloud using multiple virtual machines connected through a private network and incorporates enterprise security tools commonly used by Security Operations Centers (SOCs).

---

## Technologies Used

| Category | Technology |
|----------|------------|
| Cloud | Vultr |
| SIEM | Elasticsearch |
| Visualization | Kibana |
| Endpoint Management | Fleet |
| Endpoint Monitoring | Elastic Agent |
| Endpoint Telemetry | Sysmon |
| Endpoint Protection | Microsoft Defender |
| Command & Control | Mythic C2 |
| Ticketing | osTicket |
| Operating Systems | Ubuntu Server, Windows Server 2025, Kali Linux |

![GitHub last commit](https://img.shields.io/github/last-commit/Omphulusak/Detection-Lab?style=for-the-badge)
![GitHub repo size](https://img.shields.io/github/repo-size/Omphulusak/Detection-Lab?style=for-the-badge)
![GitHub stars](https://img.shields.io/github/stars/Omphulusak/Detection-Lab?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/Omphulusak/Detection-Lab?style=for-the-badge)

---

## Lab Objectives

- Deploy a cloud-based SOC environment.
- Collect Windows endpoint telemetry.
- Simulate attacker behaviour using Mythic C2.
- Create custom detection rules in Elastic Security.
- Investigate alerts using Kibana.
- Integrate osTicket into the incident response workflow.
- Document the complete deployment and investigation process.

---

## Documentation

The complete project walkthrough can be found in the **docs** folder.

| Document | Description |
|----------|-------------|
| Lab Overview | Project architecture and objectives |
| Infrastructure | Vultr deployment and networking |
| Elastic Stack | Elasticsearch and Kibana installation |
| Fleet | Fleet Server and Agent configuration |
| Windows Telemetry | Sysmon, Defender, and Event Logs |
| Mythic C2 | Deployment and payload generation |
| Attack Simulation | Adversary emulation |
| Detection Engineering | Custom Elastic detection rules |
| Incident Response | Alert investigation and analysis |
| osTicket | Deployment and integration |
| Lessons Learned | Project reflection and future improvements |

---

## Repository Structure

```text
Detection-Lab
│
├── architecture/
├── detections/
├── docs/
├── screenshots/
└── README.md
```

---

## Skills Demonstrated

- Security Monitoring
- Detection Engineering
- Threat Hunting
- Incident Response
- SIEM Administration
- Windows Security
- Linux Administration
- Cloud Infrastructure
- Network Security
- Technical Documentation

---

## Future Improvements

- Complete Elastic → osTicket API integration
- Add VirusTotal enrichment
- Implement Sigma rules
- Expand Active Directory attack scenarios
- Add automated alert enrichment
- Integrate SOAR workflows

---

## Author

**Omphulusa Khavhatondwi**

- GitHub: https://github.com/Omphulusak
- LinkedIn: https://www.linkedin.com/in/omphulusa-khavhatondwi-86a907246
