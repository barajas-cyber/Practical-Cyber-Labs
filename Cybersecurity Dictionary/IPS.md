# Intrusion Prevention System (IPS)

**Category:** Network Security

**Difficulty:** Beginner

**Last Updated:** July 2026

---

## Definition

An **Intrusion Prevention System (IPS)** is a security technology that continuously monitors network traffic for malicious or suspicious activity and **automatically blocks, drops, or prevents** attacks before they reach their intended target.

Unlike an Intrusion Detection System (IDS), an IPS is an **active security control** because it operates inline with network traffic and can take immediate action to stop malicious activity.

---

## Primary Purpose

- Detect malicious activity
- Prevent attacks before they reach systems
- Block known exploits
- Reduce the attack surface
- Protect network resources
- Support defense-in-depth strategies

---

## Common Use Cases

- Blocking SQL Injection attacks
- Preventing Cross-Site Scripting (XSS)
- Blocking malware communications
- Preventing brute-force attacks
- Blocking known exploit signatures
- Preventing command-and-control (C2) traffic
- Protecting critical servers

---

## How It Works

An IPS sits **inline** with network traffic, meaning all traffic passes through the device before reaching its destination.

It analyzes packets using signature-based, behavioral, or anomaly-based detection techniques. If malicious activity is detected, the IPS can automatically:

- Drop malicious packets
- Block the connection
- Reset TCP sessions
- Block the source IP address
- Generate alerts for the SOC

---

## Detection Methods

### Signature-Based Detection

Compares traffic against known attack signatures.

**Advantages**

- High accuracy
- Low false positive rate

**Limitations**

- Cannot detect unknown attacks
- Requires frequent signature updates

---

### Anomaly-Based Detection

Identifies behavior that deviates from normal network activity.

**Advantages**

- Can detect zero-day and unknown attacks

**Limitations**

- Higher false positive rate
- Requires tuning and baseline learning

---

## Real-World Example

An attacker attempts an SQL Injection attack against a company's public web application.

The IPS detects the malicious payload, blocks the request before it reaches the web server, logs the event, and sends an alert to the Security Operations Center (SOC).

The attacker never reaches the application.

---

## Advantages

- Automatically blocks attacks
- Protects systems in real time
- Reduces manual intervention
- Prevents many known exploits
- Improves overall network security

---

## Limitations

- Can block legitimate traffic if improperly configured
- Requires regular signature updates
- May introduce network latency
- Requires continuous tuning

---

## Common Technologies

### Open Source

- Suricata (IPS Mode)
- Snort (IPS Mode)

### Commercial

- Palo Alto Networks Next-Generation Firewall
- Cisco Secure Firewall
- Fortinet FortiGate
- Check Point Quantum
- Juniper Networks

---

## Related Concepts

- IDS (Intrusion Detection System)
- Next-Generation Firewall (NGFW)
- SIEM
- Threat Hunting
- Network Security Monitoring
- Incident Response

---

## IDS vs IPS

| IDS | IPS |
|------|-----|
| Passive | Active |
| Detects attacks | Detects and blocks attacks |
| Generates alerts | Generates alerts and prevents attacks |
| Out-of-band deployment | Inline deployment |
| Does not modify traffic | Can block or drop malicious traffic |

---

## Interview Notes

### What is an IPS?

> An Intrusion Prevention System (IPS) is an inline security solution that monitors network traffic for malicious activity and automatically blocks or prevents attacks before they reach their destination. Unlike an IDS, an IPS actively protects the network by taking immediate action against detected threats.

---

## Official Resources

### NIST

https://csrc.nist.gov

### Cisco Secure Firewall

https://www.cisco.com/c/en/us/products/security/firewalls/index.html

### Suricata Documentation

https://docs.suricata.io

### Snort Documentation

https://docs.snort.org

### MITRE ATT&CK

https://attack.mitre.org

---

## Personal Notes

An IPS is commonly deployed **inline** between the firewall and the internal network so it can inspect and block malicious traffic before it reaches protected systems.

Many modern **Next-Generation Firewalls (NGFWs)** include IPS functionality as part of a broader security platform, combining firewall, application awareness, intrusion prevention, and threat intelligence into a single solution.
