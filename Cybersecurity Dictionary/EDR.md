# Endpoint Detection and Response (EDR)

**Category:** Endpoint Security

**Difficulty:** Beginner

**Last Updated:** July 2026

---

## Definition

**Endpoint Detection and Response (EDR)** is an endpoint security technology that continuously monitors endpoints such as desktops, laptops, and servers to detect, investigate, and respond to malicious activity.

Unlike traditional antivirus software, EDR provides real-time visibility into endpoint behavior and enables security teams to rapidly investigate and contain threats.

---

## Primary Purpose

- Monitor endpoint activity
- Detect malicious behavior
- Investigate security incidents
- Contain compromised devices
- Collect forensic evidence
- Support threat hunting

---

## Common Use Cases

- Detecting ransomware
- Detecting malware
- Detecting suspicious PowerShell execution
- Detecting credential theft
- Detecting privilege escalation
- Detecting lateral movement
- Isolating infected devices

---

## How It Works

An EDR agent is installed on each endpoint.

The agent continuously monitors system activity including:

- Running processes
- File modifications
- Registry changes
- Network connections
- User logins
- PowerShell execution
- Command-line activity

When suspicious behavior is detected, the EDR platform generates alerts and may automatically respond based on configured policies.

---

## Common Response Actions

- Isolate the endpoint
- Kill malicious processes
- Quarantine files
- Collect forensic evidence
- Block malicious hashes
- Alert security analysts
- Initiate automated response workflows

---

## Real-World Example

A user opens a malicious email attachment.

The malware launches PowerShell and attempts to download additional payloads.

The EDR detects the suspicious behavior, terminates the PowerShell process, isolates the workstation from the network, and alerts the Security Operations Center (SOC).

---

## Advantages

- Continuous endpoint monitoring
- Real-time detection
- Rapid containment
- Detailed forensic visibility
- Supports threat hunting
- Improves incident response

---

## Limitations

- Requires tuning
- Can generate false positives
- Requires endpoint agents
- Licensing costs can be significant

---

## Common Technologies

Commercial

- Microsoft Defender for Endpoint
- CrowdStrike Falcon
- SentinelOne
- VMware Carbon Black
- Trellix Endpoint Security

Open Source

- Wazuh
- Velociraptor (Forensics & Incident Response)

---

## Related Concepts

- Antivirus
- XDR
- SIEM
- SOAR
- Threat Hunting
- Incident Response
- Windows Event Logs

---

## Antivirus vs EDR

| Traditional Antivirus | EDR |
|----------------------|-----|
| Signature-based detection | Behavioral detection |
| Basic malware protection | Advanced detection & response |
| Limited visibility | Continuous endpoint visibility |
| Manual investigation | Integrated investigation tools |
| Limited response | Automated response capabilities |

---

## Interview Notes

### What is EDR?

> Endpoint Detection and Response (EDR) continuously monitors endpoints for malicious behavior, detects threats, and enables security teams to investigate and respond quickly. Unlike traditional antivirus software, EDR provides detailed visibility into endpoint activity and supports automated response actions.

---

## Official Resources

### MITRE ATT&CK

https://attack.mitre.org

### Microsoft Defender for Endpoint

https://learn.microsoft.com/defender-endpoint/

### CrowdStrike Falcon

https://www.crowdstrike.com

### SentinelOne

https://www.sentinelone.com

### NIST Computer Security Resource Center

https://csrc.nist.gov

---

## Personal Notes

EDR solutions are a critical component of modern endpoint security. They provide visibility into endpoint activity and allow security teams to rapidly contain threats by isolating compromised devices, collecting forensic evidence, and stopping malicious processes before attacks spread throughout the environment.

Many organizations integrate EDR with a SIEM and SOAR platform to improve incident detection, investigation, and automated response.
