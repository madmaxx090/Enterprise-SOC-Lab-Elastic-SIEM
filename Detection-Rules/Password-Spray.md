# Password Spray Detection

## Rule Name

Credential Access – Repeated Failed Logons Followed by Success

---

## Description

Detects password spraying attacks by identifying multiple failed authentication attempts followed by a successful login from the same source IP.

---

## KQL Query

```kql
event.code:4625 or event.code:4624
```

---

## Severity

High

---

## MITRE ATT&CK

| Tactic | Technique |
|---------|-----------|
| Credential Access | T1110.003 Password Spraying |
| Initial Access | T1078 Valid Accounts |

---

## Expected Detection

- Multiple Event ID 4625 records
- Followed by Event ID 4624
- Same attacker IP

---

## Validation

Validated during the simulated password spraying attack.

---

## Future Improvements

- Add threshold (≥5 failures)
- Time correlation (5–10 minutes)
- Reduce false positives
