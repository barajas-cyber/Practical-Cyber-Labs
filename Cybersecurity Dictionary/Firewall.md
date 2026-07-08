# Firewall

**Category:** Network Security

**Last Updated:** July 2026

---

## Definition

A **firewall** is a security device or software application that monitors, filters, and controls network traffic entering or leaving a network based on a predefined set of security rules.

Firewalls are one of the first lines of defense in a network and help protect systems from unauthorized access while allowing legitimate communications.

---

## Primary Purpose

- Control inbound and outbound traffic
- Block unauthorized access
- Enforce security policies
- Segment networks
- Reduce the attack surface
- Log network activity

---

## Common Use Cases

- Protecting internal networks from the Internet
- Restricting access to sensitive systems
- Allowing only approved applications
- Blocking malicious IP addresses
- Controlling outbound traffic
- Creating secure network segments

---

## How It Works

Every packet entering or leaving the network is compared against a predefined rule set.

Typical firewall rules evaluate:

- Source IP Address
- Destination IP Address
- Source Port
- Destination Port
- Protocol (TCP, UDP, ICMP)
- Connection State
- Application (NGFW)

If the traffic matches an allowed rule, it is permitted.

If no rule matches, the traffic is typically denied.

---

## Common Deployment Locations

- Internet Edge
- Between Internal Network Segments
- Data Centers
- Cloud Environments
- Branch Offices
- Individual Endpoints (Host-Based Firewall)

---

## Advantages

- Blocks unauthorized network traffic
- Enforces security policies
- Provides network visibility
- Supports network segmentation
- Reduces attack surface

---

## Limitations

- Cannot stop every attack
- Requires proper rule configuration
- Does not replace endpoint security
- Misconfigured rules may expose systems

---

## Common Firewall Vendors

- Palo Alto Networks
- Cisco Secure Firewall
- Fortinet FortiGate
- Check Point
- Juniper
- Sophos
- pfSense
- OPNsense

---

## Related Concepts

- IDS
- IPS
- VPN
- WAF
- Network Segmentation
- Zero Trust
- ACL (Access Control Lists)
- NAT (Network Address Translation)

---

## Interview Notes

### What is a Firewall?

> A firewall is a security device or software application that monitors and filters network traffic according to predefined security rules. Its primary purpose is to allow legitimate traffic while blocking unauthorized or malicious communications.

---

## Official Resources

### NIST Computer Security Resource Center

https://csrc.nist.gov

### CISA

https://www.cisa.gov

### Cisco Secure Firewall

https://www.cisco.com/c/en/us/products/security/firewalls/index.html

### Palo Alto Networks

https://www.paloaltonetworks.com

---

## Personal Notes

Firewalls are typically the first security control that traffic encounters when entering or leaving a network. Modern enterprise environments often deploy multiple firewalls to separate network zones and implement a defense-in-depth strategy.
