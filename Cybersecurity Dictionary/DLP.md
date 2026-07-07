# Data Loss Prevention (DLP)

**Category:** Data Security

**Difficulty:** Beginner

**Last Updated:** July 2026

---

## Definition

**Data Loss Prevention (DLP)** is a security technology and set of policies designed to identify, monitor, and prevent the unauthorized disclosure, transmission, or loss of sensitive information.

DLP solutions help organizations protect confidential data by inspecting data **at rest**, **in transit**, and **in use**, enforcing policies that prevent accidental or intentional data leaks.

---

## Primary Purpose

- Protect sensitive information
- Prevent unauthorized data disclosure
- Detect accidental data leaks
- Prevent intentional data exfiltration
- Support regulatory compliance
- Monitor movement of confidential data

---

## Common Use Cases

- Blocking emails containing Social Security numbers
- Preventing uploads of confidential files to cloud storage
- Restricting copying sensitive files to USB devices
- Monitoring sensitive documents leaving the organization
- Protecting intellectual property
- Preventing insider threats

---

## How It Works

A DLP solution examines data as it is:

- Stored on systems (Data at Rest)
- Transmitted across networks (Data in Transit)
- Accessed or used by users (Data in Use)

It compares the data against predefined policies.

If sensitive information is detected, the DLP solution can:

- Block the action
- Encrypt the data
- Quarantine the file
- Notify security personnel
- Log the event
- Require user justification

---

## Types of DLP

### Network DLP

Monitors data moving across the network.

Examples:

- Email
- Web uploads
- FTP transfers
- Cloud applications

---

### Endpoint DLP

Protects data on user devices.

Examples:

- USB storage
- Local file copies
- Printing
- Clipboard
- Screen capture restrictions

---

### Cloud DLP

Protects information stored in cloud services.

Examples:

- Microsoft 365
- Google Workspace
- Dropbox
- SharePoint
- OneDrive

---

## Real-World Example

An employee attempts to email a spreadsheet containing customer Social Security numbers to a personal Gmail account.

The DLP solution detects the sensitive information based on company policy, blocks the email from being sent, logs the event, and notifies the security team for review.

---

## Advantages

- Protects confidential information
- Reduces insider threat risk
- Helps maintain regulatory compliance
- Prevents accidental disclosures
- Improves visibility into data movement

---

## Limitations

- Requires well-defined data classification
- Can generate false positives
- Requires continuous policy tuning
- Cannot prevent all insider threats
- May affect user productivity if overly restrictive

---

## Common Technologies

Commercial

- Microsoft Purview DLP
- Symantec Data Loss Prevention
- Forcepoint DLP
- Trellix DLP
- Digital Guardian
- Proofpoint DLP

Cloud

- Microsoft 365
- Google Workspace
- Microsoft Defender for Cloud Apps

---

## Related Concepts

- Data Classification
- Information Protection
- Insider Threat
- Encryption
- Zero Trust
- IAM
- Endpoint Security

---

## DLP vs Encryption

| DLP | Encryption |
|-----|------------|
| Monitors data | Protects data with cryptography |
| Prevents unauthorized sharing | Protects confidentiality |
| Enforces security policies | Makes data unreadable without a key |
| Can block transmissions | Does not prevent transmission |

---

## Interview Notes

### What is DLP?

> Data Loss Prevention (DLP) is a security solution that identifies, monitors, and protects sensitive information by preventing unauthorized disclosure, transmission, or loss. DLP helps organizations enforce security policies across endpoints, networks, email, cloud services, and other communication channels.

---

## Official Resources

### NIST Computer Security Resource Center

https://csrc.nist.gov

### Microsoft Purview DLP

https://learn.microsoft.com/purview/dlp-learn-about-dlp

### CISA

https://www.cisa.gov

### Microsoft Defender for Cloud Apps

https://learn.microsoft.com/defender-cloud-apps/

---

## Personal Notes

DLP is commonly used to protect Personally Identifiable Information (PII), financial records, healthcare data, intellectual property, and other sensitive business information. Modern DLP solutions integrate with email systems, cloud storage, endpoints, and collaboration platforms to prevent both accidental and intentional data loss.

A DLP solution is most effective when combined with data classification, encryption, least privilege, and user security awareness training.
