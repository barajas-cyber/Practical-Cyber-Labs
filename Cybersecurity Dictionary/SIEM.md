# Security Information and Event Management (SIEM)

**Category:** Security Operations (SOC)

**Difficulty:** Beginner

**Last Updated:** July 2026

---

## Definition

A **Security Information and Event Management (SIEM)** platform is a centralized security solution that collects, normalizes, correlates, stores, and analyzes logs and security events from multiple systems across an organization.

A SIEM helps security teams detect threats, investigate incidents, and respond more efficiently by providing a single location to monitor security events.

---

## Primary Purpose

- Centralize log collection
- Correlate security events
- Detect suspicious activity
- Generate security alerts
- Support incident response
- Support threat hunting
- Meet compliance and auditing requirements

---

## Common Log Sources

A SIEM can collect logs from:

- Firewalls
- IDS / IPS
- Windows Event Logs
- Linux Syslog
- Active Directory
- VPNs
- Endpoint Detection & Response (EDR)
- Antivirus
- DNS Servers
- Web Servers
- Email Gateways
- Cloud Services (AWS, Azure, Microsoft 365)

---

## How It Works

A SIEM continuously collects logs from multiple systems and devices.

It then:

1. Normalizes the data into a common format.
2. Correlates events from different sources.
3. Detects suspicious patterns.
4. Generates alerts.
5. Stores logs for investigations and compliance.

Security analysts investigate alerts and determine whether they represent legitimate threats.

---

## Common Use Cases

- Detecting brute-force attacks
- Detecting privilege escalation
- Detecting malware infections
- Monitoring failed logins
- Identifying lateral movement
- Detecting suspicious PowerShell activity
- Investigating phishing incidents
- Compliance reporting

---

## Real-World Example

A user fails to log in to Active Directory 25 times within two minutes.

The firewall also reports multiple failed VPN login attempts from the same IP address.

The SIEM correlates both events and generates a high-priority alert for a potential brute-force attack.

A security analyst investigates the activity and determines whether additional containment actions are required.

---

## Advantages

- Centralized visibility
- Faster incident detection
- Correlates events across systems
- Supports compliance
- Improves threat hunting
- Reduces investigation time

---

## Limitations

- Requires proper tuning
- Can generate false positives
- Requires skilled analysts
- Storage requirements can be significant
- Licensing costs can be high

---

## Common Technologies

Commercial

- Microsoft Sentinel
- Splunk Enterprise Security
- IBM QRadar
- Google Chronicle
- Stellar Cyber Open XDR

Open Source

- Elastic Security
- Wazuh
- Security Onion

---

## Related Concepts

- SOC
- IDS
- IPS
- EDR
- XDR
- SOAR
- Threat Hunting
- Incident Response
- Log Management

---

## SIEM vs Log Management

| Log Management | SIEM |
|----------------|------|
| Stores logs | Stores and analyzes logs |
| Basic searching | Correlates events |
| Limited alerting | Advanced alerting |
| Primarily for storage | Detection, investigation, and response |

---

## Interview Notes

### What is a SIEM?

> A SIEM is a centralized platform that collects, correlates, and analyzes security logs from multiple systems. It helps security teams detect threats, investigate incidents, and respond more effectively by providing visibility across the enterprise.

---

## Official Resources

### NIST Computer Security Resource Center

https://csrc.nist.gov

### Microsoft Sentinel

https://learn.microsoft.com/azure/sentinel/

### Splunk

https://www.splunk.com

### Elastic Security

https://www.elastic.co/security

### IBM QRadar

https://www.ibm.com/products/qradar

---

## Personal Notes

A SIEM does not replace security tools such as firewalls, IDS, or EDR. Instead, it collects information from these tools and correlates events to provide a more complete picture of an organization's security posture.

One of the primary responsibilities of a SOC analyst or Security Engineer is triaging SIEM alerts to determine whether they represent true security incidents or false positives.
