# Attack Chain

The following attack chain was executed during the project.

```text
Kali Linux
      │
      ▼
Nmap Port Scan
      │
      ▼
SMB Enumeration
      │
      ▼
Password Spray
      │
      ▼
Successful Authentication
      │
      ▼
Elastic SIEM Detection
      │
      ▼
SOC Investigation
```

## Description

### Phase 1 – Reconnaissance

The attacker performed network reconnaissance using Nmap to identify exposed services.

MITRE:
- T1595.001
- T1046

---

### Phase 2 – Discovery

SMB shares were enumerated to identify accessible resources.

MITRE:
- T1135

---

### Phase 3 – Credential Access

A password spraying attack generated multiple failed logon events (4625) followed by a successful logon (4624).

MITRE:
- T1110.003

---

### Phase 4 – Initial Access

Successful authentication provided valid access to the target system.

MITRE:
- T1078

---

### Phase 5 – Detection

Elastic SIEM correlated Windows Event Logs and Sysmon telemetry to identify suspicious activity.
