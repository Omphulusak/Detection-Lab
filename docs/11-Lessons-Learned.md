# 11 - Lessons Learned & Future Improvements

## Project Summary

The Detection Lab was built to simulate the workflow of a modern Security Operations Center (SOC), from infrastructure deployment to attack simulation, detection engineering, investigation, and incident response.

The project combined multiple enterprise security technologies to provide hands-on experience with log collection, endpoint monitoring, detection engineering, and security investigations.

---

# Key Technical Skills Developed

Throughout this project, I gained practical experience in:

## Cloud Infrastructure

- Deploying virtual machines in Vultr Cloud
- Configuring firewall groups
- Managing Virtual Private Cloud (VPC) networking
- Securing remote administration services

---

## Elastic Stack

Working with the Elastic Stack provided experience in:

- Elasticsearch administration
- Kibana configuration
- Fleet Server deployment
- Elastic Agent management
- Windows endpoint monitoring
- Log ingestion and visualization

---

## Endpoint Telemetry

Configuring Windows telemetry demonstrated the importance of collecting high-quality security data.

Key data sources included:

- Sysmon
- Microsoft Defender
- Windows Event Logs
- Elastic Agent

This telemetry formed the foundation for detection engineering and incident investigations.

---

## Detection Engineering

Creating custom detection rules improved my understanding of:

- KQL (Kibana Query Language)
- Indicators of Compromise (IOCs)
- Process creation monitoring
- Network activity analysis
- Event correlation
- Alert validation

---

## Adversary Simulation

Deploying Mythic C2 provided practical experience simulating attacker behaviour, including:

- Initial access
- Discovery
- Payload execution
- Command and Control
- Endpoint reconnaissance

This generated realistic telemetry that could be detected and investigated using Elastic Security.

---

## Incident Response

The project reinforced the importance of structured investigations.

Key activities included:

- Validating alerts
- Collecting evidence
- Identifying Indicators of Compromise
- Recommending remediation actions
- Documenting findings

---

# Challenges Encountered

Several technical challenges were encountered during the project.

These included:

- Fleet Server connectivity
- Elasticsearch networking
- Kibana configuration
- Windows firewall configuration
- Elastic Agent enrollment
- osTicket API integration
- Apache configuration
- Remote Desktop connectivity

Troubleshooting these issues significantly improved my understanding of enterprise infrastructure and security operations.

---

# Future Improvements

Although the Detection Lab successfully demonstrated the complete SOC workflow, several improvements are planned.

Future enhancements include:

- Complete Elastic → osTicket API integration
- Integrate VirusTotal for IOC enrichment
- Deploy Active Directory
- Expand attack simulations
- Create additional Elastic detection rules
- Implement Sigma rule support
- Automate alert enrichment
- Integrate SOAR workflows
- Develop additional dashboards for threat hunting

---

# Reflection

This project strengthened my understanding of how modern Security Operations Centers detect, investigate, and respond to cyber threats.

Beyond learning individual technologies, the project demonstrated how multiple security tools work together to provide complete visibility into endpoint activity.

Building the Detection Lab also highlighted the importance of documentation, troubleshooting, and continuous improvement when developing enterprise security solutions.

---

# Conclusion

The Detection Lab successfully demonstrates the complete SOC lifecycle:

- Infrastructure Deployment
- Endpoint Monitoring
- Attack Simulation
- Detection Engineering
- Threat Investigation
- Incident Response

The experience gained throughout this project has strengthened my technical skills in SIEM administration, endpoint security, detection engineering, and incident response, while providing a solid foundation for continued growth as a SOC Analyst.
