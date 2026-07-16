# Network Reconnaissance Detection

## Rule Name

Network Reconnaissance – High-Volume Connections from Single Source

## Status

Active

---

## Description

This rule detects high-volume network connection attempts originating from a single source IP. It is designed to identify reconnaissance activity such as Nmap port scanning.

---

## KQL Query

```kql
event.code:3 and agent.name:"DESKTOP-F4MMQ6V"
```

---

## Severity

Low

---

## MITRE ATT&CK

| Tactic | Technique |
|---------|-----------|
| Reconnaissance | T1595.001 Active Scanning |
| Discovery | T1046 Network Service Discovery |

---

## Expected Detection

- High number of Event ID 3 records
- Multiple destination ports
- Same source IP

---

## Validation

Successfully detected the Nmap scan performed during the attack simulation.

---

## Future Improvements

- Threshold-based detection
- Port aggregation
- Alert suppression
