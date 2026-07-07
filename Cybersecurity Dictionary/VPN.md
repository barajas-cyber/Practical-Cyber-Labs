# Virtual Private Network (VPN)

**Category:** Network Security

**Difficulty:** Beginner

**Last Updated:** July 2026

---

## Definition

A **Virtual Private Network (VPN)** is a security technology that creates an encrypted tunnel between a user's device and a trusted network over an untrusted network, such as the Internet. This encrypted connection protects the confidentiality and integrity of data while allowing authorized users to securely access internal resources.

---

## Primary Purpose

- Secure remote access
- Encrypt network communications
- Protect sensitive data in transit
- Connect remote offices
- Reduce exposure on public networks
- Support secure work-from-home environments

---

## Common Use Cases

- Remote employees accessing corporate resources
- Secure access to internal file servers
- Connecting branch offices together
- Protecting traffic on public Wi-Fi
- Secure administration of servers

---

## How It Works

A VPN establishes an encrypted tunnel between a VPN client and a VPN server.

All network traffic sent through the VPN is encrypted before leaving the user's device and decrypted once it reaches the destination network.

This prevents attackers from viewing or modifying data while it travels across the Internet.

---

## Types of VPN

### Remote Access VPN

Allows individual users to securely connect to an organization's internal network.

**Examples**

- Employees working from home
- IT administrators managing servers remotely

---

### Site-to-Site VPN

Connects two or more networks together over the Internet.

**Examples**

- Headquarters connected to a branch office
- Corporate office connected to a cloud environment

---

## VPN Protocols

### IPsec

Provides encryption and authentication at the network layer.

Commonly used for:

- Site-to-site VPNs
- Enterprise remote access

---

### SSL/TLS VPN

Uses web technologies to establish secure remote connections.

Commonly used for:

- Remote workforce
- Browser-based VPN access

---

### WireGuard

A modern VPN protocol designed for simplicity, high performance, and strong cryptography.

---

### OpenVPN

An open-source VPN solution widely used in enterprise and commercial environments.

---

## Real-World Example

An employee working from home needs access to internal file shares and Active Directory resources.

The employee launches the company's VPN client, authenticates with Multi-Factor Authentication (MFA), and establishes an encrypted tunnel to the corporate firewall. Once connected, the employee can securely access internal resources as if they were physically in the office.

---

## Advantages

- Encrypts data in transit
- Enables secure remote work
- Protects users on public Wi-Fi
- Supports secure administration
- Protects sensitive communications

---

## Limitations

- Can introduce additional latency
- Requires proper authentication
- Misconfigurations may expose internal resources
- Performance depends on Internet connectivity

---

## Common Technologies

- Cisco AnyConnect
- Palo Alto GlobalProtect
- Fortinet FortiClient
- OpenVPN
- WireGuard
- Microsoft Always On VPN

---

## Related Concepts

- Firewall
- MFA
- Zero Trust
- Network Security
- Encryption
- Remote Access

---

## Interview Notes

### What is a VPN?

> A Virtual Private Network (VPN) creates an encrypted tunnel between a client and a trusted network, allowing users to securely access internal resources over untrusted networks such as the Internet.

---

## Official Resources

### NIST

https://csrc.nist.gov

### NIST SP 800-77 Revision 1
Guide to IPsec VPNs

https://csrc.nist.gov/publications/detail/sp/800-77/rev-1/final

### Cisco VPN Technologies

https://www.cisco.com/c/en/us/products/security/vpn-endpoint-security-clients/index.html

### OpenVPN

https://openvpn.net

### WireGuard

https://www.wireguard.com

---

## Personal Notes

VPNs are commonly used to provide secure remote access for employees and administrators. Most enterprise VPN deployments integrate with Active Directory or Entra ID and require Multi-Factor Authentication (MFA) before allowing access to internal resources.
