
# Architecture

This directory contains the architectural diagrams for the **Enterprise SOC Lab**. These diagrams illustrate the overall design of the environment, the flow of security telemetry, the attack lifecycle, and the detection workflow implemented using the Elastic Stack.

---

## Contents

| Diagram | Description |
|----------|-------------|
| **Network-Diagram.png** | High-level network architecture showing the attacker, victim, Elastic components, and communication paths. |
| **Lab-Topology.png** | Virtual lab topology, including VMware Workstation, Windows 10, Kali Linux, and the host machine. |
| **Data-Flow.png** | End-to-end log collection pipeline from Windows Event Logs and Sysmon through Elastic Agent to Elasticsearch and Kibana. |
| **Attack-Flow.png** | Sequence of the simulated attack, including reconnaissance, enumeration, password spraying, authentication, and detection. |
| **Detection-Workflow.png** | Detection pipeline illustrating how telemetry is processed, analyzed, and transformed into security alerts. |

---

# Architecture Overview

The Enterprise SOC Lab was designed to simulate a small enterprise Security Operations Center (SOC) capable of collecting endpoint telemetry, detecting suspicious activity, and supporting threat hunting.

The environment consists of:

- Windows 11 host system
- VMware Workstation
- Kali Linux attacker machine
- Windows 10 victim endpoint
- Elastic Agent
- Fleet Server
- Elasticsearch
- Kibana
- Sysmon

---

# Log Collection Workflow

The Windows endpoint generates security telemetry through Windows Event Logs and Sysmon.

Elastic Agent collects this telemetry and securely forwards it to Elasticsearch.

Elasticsearch indexes the collected events, making them searchable within Kibana.

Security analysts can then:

- Monitor dashboards
- Investigate alerts
- Perform threat hunting using KQL
- Develop detection rules

---

# Attack Workflow

The simulated attack followed the sequence below:

1. Reconnaissance using Nmap
2. Network service discovery
3. SMB enumeration
4. Password spraying
5. Successful authentication
6. Detection using Elastic Security
7. Investigation using Kibana

---

# Detection Workflow

The detection process consists of five stages:

1. Endpoint telemetry collection
2. Log ingestion through Elastic Agent
3. Data indexing in Elasticsearch
4. Rule evaluation in Elastic Security
5. Alert generation and SOC investigation

---

# Technologies Used

| Category | Technology |
|----------|------------|
| Host OS | Windows 11 |
| Hypervisor | VMware Workstation |
| Attacker | Kali Linux |
| Victim | Windows 10 |
| Endpoint Monitoring | Sysmon |
| Log Collection | Elastic Agent |
| SIEM | Elastic Stack |
| Dashboard | Kibana |
| Threat Hunting | KQL |
| Detection Framework | Elastic Security |
| Attack Mapping | MITRE ATT&CK |


---

