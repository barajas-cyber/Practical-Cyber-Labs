# Network Access Control (NAC)

**Category:** Network Security

**Last Updated:** July 2026

---

## Definition

**Network Access Control (NAC)** is a security solution that controls which users and devices are allowed to connect to an organization's network. NAC verifies the identity, health, and security posture of a device before granting access to network resources.

By enforcing access policies, NAC helps prevent unauthorized users and non-compliant devices from accessing sensitive systems.

---

## Primary Purpose

- Control network access
- Authenticate users and devices
- Verify device security posture
- Enforce security policies
- Reduce unauthorized access
- Support Zero Trust architectures

---

## How It Works

Before granting network access, a NAC solution evaluates:

- User identity
- Device identity
- Device health
- Operating system compliance
- Antivirus status
- Endpoint Detection and Response (EDR) status
- Security certificates
- Device type

Based on predefined security policies, the NAC can:

- Allow access
- Deny access
- Restrict access
- Place the device into a quarantine VLAN
- Require remediation before granting access

---

## Authentication Methods

Common authentication methods include:

- IEEE 802.1X
- RADIUS
- Active Directory
- Microsoft Entra ID
- LDAP
- Digital Certificates

---

## Common Use Cases

- Employee laptops
- Guest Wi-Fi
- Bring Your Own Device (BYOD)
- Corporate desktops
- Servers
- Printers
- IP Phones
- IoT devices

---

## Real-World Example

An employee connects a personal laptop to the corporate network.

The NAC solution checks:

- Is the device registered?
- Is antivirus installed?
- Is the operating system up to date?
- Is disk encryption enabled?

Because the laptop is not compliant with company policy, the NAC places it into a quarantine VLAN where it can only access update servers until it meets security requirements.

---

## Advantages

- Prevents unauthorized network access
- Enforces security policies
- Improves endpoint visibility
- Supports regulatory compliance
- Reduces the risk of compromised devices
- Strengthens Zero Trust implementations

---

## Limitations

- Requires planning and policy development
- Can be complex to deploy
- May require endpoint agents
- Legacy devices may not fully support NAC

---

## Common Technologies

Commercial

- Cisco Identity Services Engine (ISE)
- Aruba ClearPass
- Fortinet FortiNAC
- Forescout Platform
- ExtremeControl

Open Source

- PacketFence

---

## Related Concepts

- Zero Trust
- IAM
- MFA
- Active Directory
- Microsoft Entra ID
- VPN
- EDR
- Network Segmentation

---

## NAC vs Firewall

| NAC | Firewall |
|-----|----------|
| Controls who can access the network | Controls network traffic |
| Evaluates user and device identity | Evaluates network packets |
| Verifies device compliance | Filters traffic based on security rules |
| Operates before network access is granted | Operates after devices are connected |

---

## Interview Notes

### What is Network Access Control (NAC)?

> Network Access Control (NAC) is a security solution that authenticates users and devices before allowing them to connect to a network. It evaluates identity and device compliance with security policies and can allow, deny, restrict, or quarantine devices based on organizational requirements.

---

## Official References

### National Institute of Standards and Technology (NIST)

https://csrc.nist.gov

---

### Cybersecurity and Infrastructure Security Agency (CISA)

https://www.cisa.gov

---

### Cisco Identity Services Engine (ISE)

https://www.cisco.com/c/en/us/products/security/identity-services-engine/

---

### Aruba ClearPass

https://www.arubanetworks.com/products/security/network-access-control/

---

### PacketFence

https://www.packetfence.org

---

## Personal Notes

NAC is often one of the first technologies used to enforce a **Zero Trust** security model. Instead of assuming that every device connected to the network is trusted, NAC continuously verifies that users and devices meet organizational security requirements before granting access.

Many organizations integrate NAC with Active Directory, Microsoft Entra ID, EDR solutions, and VLANs to automate access decisions and improve overall network security.
