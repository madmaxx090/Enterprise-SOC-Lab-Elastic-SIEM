# Techniques

## T1595.001 – Active Scanning

### Description

The attacker scanned the target system using Nmap to identify active services.

### Evidence

- Event Code 3
- Sysmon Network Connections
- Elastic Detection Rule

---

## T1046 – Network Service Discovery

### Description

Open services were identified during reconnaissance.

### Evidence

- Sysmon Event ID 3
- Elastic Discover
- Kibana Dashboards

---

## T1135 – Network Share Discovery

### Description

SMB shares were enumerated to identify accessible resources.

### Evidence

- SMB Enumeration
- Administrative Shares

---

## T1110.003 – Password Spraying

### Description

Multiple failed authentication attempts were followed by a successful login.

### Evidence

- Windows Event ID 4625
- Windows Event ID 4624

---

## T1078 – Valid Accounts

### Description

Successful authentication using valid credentials.

### Evidence

- Event ID 4624
- Elastic Security Investigation
