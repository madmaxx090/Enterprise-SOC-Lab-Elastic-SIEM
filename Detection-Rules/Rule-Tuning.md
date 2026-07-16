
# Rule Tuning

## Objective

Reduce false positives while maintaining high detection accuracy.

---

## Current Challenges

- Large number of alerts generated during network scanning.
- Single-event detections create unnecessary analyst workload.

---

## Recommended Improvements

- Threshold-based detections
- Correlation between multiple event types
- Time-window analysis
- Source IP aggregation
- Alert suppression

---

## Example Improvements

| Rule | Improvement |
|------|-------------|
| Network Reconnaissance | Aggregate destination ports |
| Password Spray | Require multiple failures before success |
| SMB Share Access | Correlate with authentication events |

---

## Expected Outcome

Improved detection fidelity, reduced alert fatigue, and more efficient SOC investigations.
