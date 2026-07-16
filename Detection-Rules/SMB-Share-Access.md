
# SMB Administrative Share Access

## Rule Name

Administrative Share Access Following Authentication

---

## Description

Detects access to Windows administrative shares after successful authentication.

---

## KQL Query

```kql
event.code:5140 or event.code:5145
```

---

## Severity

Medium-High

---

## MITRE ATT&CK

| Tactic | Technique |
|---------|-----------|
| Discovery | T1135 Network Share Discovery |
| Lateral Movement | Administrative Share Access |

---

## Requirement

Windows Security Auditing for Event IDs 5140 and 5145 must be enabled.

---

## Future Improvements

- Correlate with successful logons
- Correlate with Password Spray rule
