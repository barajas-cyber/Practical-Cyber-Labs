# Intrusion Detection System (IDS)

**Category:** Network Security

**Last Updated:** July 2026

---

## Definition

An **Intrusion Detection System (IDS)** is a security solution that continuously monitors network traffic or host activity to detect malicious or suspicious behavior. When potential threats are identified, the IDS generates alerts for security personnel to investigate.

Unlike an Intrusion Prevention System (IPS), an IDS **does not block or modify traffic**. Its primary purpose is to provide visibility into security events and support incident detection and response. :contentReference[oaicite:0]{index=0}

---

## Primary Purpose

- Detect malicious activity
- Monitor network traffic and host events
- Generate security alerts
- Improve network visibility
- Support incident response
- Assist with threat hunting and forensic investigations

---

## How It Works

An IDS inspects network traffic or endpoint activity and compares it against known attack signatures or behavioral baselines.

When suspicious activity is detected, the IDS:

1. Detects the event.
2. Generates an alert.
3. Records the event in logs.
4. Sends the alert to security analysts or a SIEM for investigation.

Because an IDS is a **passive** security control, it does not block the traffic.

---

## Types of IDS

### Network Intrusion Detection System (NIDS)

Monitors network traffic flowing across the network.

**Examples**

- Suricata
- Snort
- Zeek

---

### Host Intrusion Detection System (HIDS)

Monitors activity occurring on an individual endpoint or server.

Examples include:

- File integrity monitoring
- Registry monitoring
- Log monitoring
- Process monitoring

**Examples**

- Wazuh
- OSSEC

---

## Detection Methods

### Signature-Based Detection

Compares activity against a database of known attack signatures.

**Advantages**

- Highly accurate for known attacks
- Low false positive rate

**Limitations**

- Cannot detect unknown threats
- Requires frequent signature updates

---

### Anomaly-Based Detection

Compares activity against a baseline of normal behavior and alerts when significant deviations occur.

**Advantages**

- Can detect unknown attacks
- Useful for identifying zero-day threats

**Limitations**

- Higher false positive rate
- Requires tuning

---

## Common Use Cases

- Detecting port scans
- Detecting brute-force attacks
- Detecting malware communications
- Detecting command-and-control (C2) traffic
- Detecting lateral movement
- Detecting exploit attempts
- Monitoring critical network segments

---

## Real-World Example

An attacker performs an Nmap scan against a company's web server.

The IDS identifies multiple connection attempts across sequential ports and generates an alert indicating a potential reconnaissance or port scanning activity.

The traffic is not blocked, but the Security Operations Center (SOC) is notified so analysts can investigate.

---

## Advantages

- Provides network visibility
- Detects suspicious activity
- Supports incident response
- Assists with threat hunting
- Supports forensic investigations
- Does not interfere with legitimate traffic

---

## Limitations

- Cannot stop attacks
- Requires continuous monitoring
- May generate false positives
- Requires regular tuning and maintenance

---

## Common Technologies

### Open Source

- Suricata
- Snort
- Zeek
- Security Onion

### Commercial

- Cisco Secure IDS
- Palo Alto Networks Threat Prevention
- Trellix Network Security
- Trend Micro Deep Discovery

---

## Related Concepts

- IPS (Intrusion Prevention System)
- SIEM
- EDR
- XDR
- SOAR
- Threat Hunting
- Network Security Monitoring (NSM)
- Incident Response

---

## IDS vs IPS

| IDS | IPS |
|-----|-----|
| Detects attacks | Detects and blocks attacks |
| Passive monitoring | Active protection |
| Generates alerts | Generates alerts and blocks traffic |
| Out-of-band deployment | Inline deployment |

---

## Interview Notes

### What is an IDS?

> An Intrusion Detection System (IDS) is a passive security solution that monitors network traffic or host activity for malicious behavior. When suspicious activity is detected, it generates alerts for investigation but does not block or modify the traffic.

---

## Official References

### NIST

**Guide to Intrusion Detection and Prevention Systems (SP 800-94)**

:contentReference[oaicite:1]{index=1}

---

### NIST Glossary

:contentReference[oaicite:2]{index=2}

---

### Suricata Documentation

:contentReference[oaicite:3]{index=3}

---

### MITRE ATT&CK

:contentReference[oaicite:4]{index=4}

---

### Snort Documentation

:contentReference[oaicite:5]{index=5}

---

## Personal Notes

Most organizations deploy an IDS using a **SPAN (Mirror) Port** or a **Network TAP** so it can inspect copies of network traffic without interrupting communications.

In modern Security Operations Centers (SOCs), IDS alerts are commonly forwarded to a SIEM where they are correlated with logs from firewalls, endpoints, Active Directory, VPNs, and other security tools to improve threat detection and investigation.
