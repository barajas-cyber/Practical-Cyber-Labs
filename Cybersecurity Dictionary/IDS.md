# Intrusion Detection System (IDS)

> Monitors network or host activity for malicious or suspicious behavior and generates alerts. An IDS is a passive security control because it does not block traffic.

---

## Key Points

- Passive monitoring
- Detects suspicious activity
- Generates alerts
- Supports incident response
- Does not block traffic

---

## Types

### Network IDS (NIDS)

Monitors network traffic.

Examples:

- Suricata
- Snort
- Zeek

### Host IDS (HIDS)

Monitors activity on an endpoint.

Examples:

- Wazuh
- OSSEC

---

## Real-World Example

An attacker performs an Nmap scan.

The IDS detects the scan and generates an alert.

The SOC investigates the activity.

---

## IDS vs IPS

| IDS | IPS |
|-----|-----|
| Detects | Detects & Blocks |
| Passive | Active |
| Alerts | Prevents |
| Out-of-band | Inline |

---

## Interview Answer

> "An IDS is a passive monitoring solution that detects suspicious activity and generates alerts but does not block traffic."

---

## References

- NIST
- Suricata
- Snort
- MITRE ATT&CK
