# Intrusion Detection System (IDS)

**Category:** Network Security

**Last Updated:** July 2026

---

## Definition

An **Intrusion Detection System (IDS)** is a security technology that continuously monitors network traffic or host activity for malicious or suspicious behavior. It analyzes traffic using signatures, anomaly detection, or behavioral analysis and generates alerts when potential threats are identified.

Unlike an **Intrusion Prevention System (IPS)**, an IDS is considered a **passive security control** because it **does not block or modify network traffic**. Its primary function is to detect suspicious activity and notify security personnel for investigation.

---

## Primary Purpose

- Detect malicious network or host activity
- Monitor security events
- Generate alerts for suspicious behavior
- Improve network visibility
- Support incident response
- Assist with threat hunting
- Provide forensic evidence during investigations

---

## How It Works

An IDS monitors network traffic or endpoint activity and analyzes it using one or more detection methods.

When suspicious activity is detected, the IDS:

1. Detects the event.
2. Generates an alert.
3. Logs the activity.
4. Sends the alert to security analysts or a SIEM platform for investigation.

Because an IDS operates **out-of-band**, it observes traffic without interrupting or modifying communications.

---

## Types of IDS

### Network Intrusion Detection System (NIDS)

A Network IDS monitors traffic flowing across the network.

Examples:

- Suricata
- Snort
- Zeek

Common deployment methods:

- SPAN (Mirror) Port
- Network TAP

---

### Host Intrusion Detection System (HIDS)

A Host IDS monitors activity occurring on an individual endpoint or server.

Examples include monitoring:

- System logs
- Registry changes
- File integrity
- Running processes
- User activity

Examples:

- Wazuh
- OSSEC

---

## Detection Methods

### Signature-Based Detection

Compares observed activity against a database of known attack signatures.

**Advantages**

- Accurate for known attacks
- Low false positive rate

**Limitations**

- Cannot detect previously unknown attacks
- Requires frequent signature updates

---

### Anomaly-Based Detection

Establishes a baseline of normal activity and alerts when significant deviations occur.

**Advantages**

- Can detect zero-day attacks
- Detects unknown threats

**Limitations**

- Higher false positive rate
- Requires tuning and baseline learning

---

## Common Use Cases

- Detecting port scans
- Detecting brute-force attacks
- Detecting malware communications
- Detecting command-and-control (C2) traffic
- Detecting lateral movement
- Detecting exploit attempts
- Monitoring critical network infrastructure

---

## Real-World Example

An attacker performs an Nmap scan against an organization's web server.

The IDS detects multiple connection attempts across sequential ports and generates an alert indicating a possible reconnaissance or port scan.

The traffic is not blocked because the IDS is passive, but the Security Operations Center (SOC) receives the alert and begins investigating the activity.

---

## Advantages

- Continuous monitoring
- Improved network visibility
- Detects suspicious activity
- Supports incident response
- Assists with forensic investigations
- Does not interrupt legitimate traffic

---

## Limitations

- Does not block attacks
- Requires continuous monitoring
- May generate false positives
- Requires tuning and maintenance

---

## Common Technologies

### Open Source

- Suricata
- Snort
- Zeek
- Security Onion

### Commercial

- Cisco Secure Firewall IDS/IPS
- Palo Alto Networks Threat Prevention
- Trellix Network Security
- Trend Micro Deep Discovery

---

## Related Concepts

- Intrusion Prevention System (IPS)
- Security Information and Event Management (SIEM)
- Endpoint Detection and Response (EDR)
- Extended Detection and Response (XDR)
- Security Orchestration, Automation, and Response (SOAR)
- Threat Hunting
- Network Security Monitoring (NSM)
- Incident Response

---

## IDS vs IPS

| IDS | IPS |
|-----|-----|
| Detects attacks | Detects and blocks attacks |
| Passive | Active |
| Generates alerts | Generates alerts and prevents attacks |
| Out-of-band deployment | Inline deployment |
| Does not modify traffic | Can block or drop malicious traffic |

---

## Interview Notes

### What is an IDS?

> An Intrusion Detection System (IDS) is a passive security solution that monitors network traffic or host activity for malicious or suspicious behavior. When suspicious activity is detected, it generates alerts so security personnel can investigate. Unlike an IPS, it does not block or modify network traffic.

---

## Official References

### National Institute of Standards and Technology (NIST)

**Guide to Intrusion Detection and Prevention Systems (IDPS) - NIST SP 800-94**

https://csrc.nist.gov/pubs/sp/800/94/final

**NIST Computer Security Resource Center**

https://csrc.nist.gov

---

### Cybersecurity and Infrastructure Security Agency (CISA)

https://www.cisa.gov

---

### MITRE ATT&CK Framework

https://attack.mitre.org

---

### Suricata Documentation

https://docs.suricata.io

---

### Snort Documentation

https://docs.snort.org

---

### Zeek Documentation

https://docs.zeek.org

---

## Personal Notes

Most enterprise IDS solutions are deployed using a **SPAN (Mirror) Port** or a **Network TAP**, allowing them to inspect copies of network traffic without interrupting communications.

Modern Security Operations Centers (SOCs) commonly forward IDS alerts to a **SIEM**, where they are correlated with firewall logs, Windows Event Logs, VPN logs, EDR telemetry, Active Directory events, and other security data sources.

An IDS is an important component of a **defense-in-depth** strategy. While it does not stop attacks, it provides visibility into suspicious activity and enables security teams to investigate potential threats before they escalate.
