# Network Segmentation

**Category:** Network Security

**Last Updated:** July 2026

---

## Definition

**Network Segmentation** is the practice of dividing a network into smaller, isolated segments or zones to improve security, performance, and management. Each segment can have its own security policies that control how devices communicate with one another.

By limiting communication between segments, organizations reduce the attack surface and make it more difficult for attackers to move laterally after compromising a system.

---

## Primary Purpose

- Reduce the attack surface
- Prevent lateral movement
- Improve network security
- Protect sensitive systems
- Improve network performance
- Support regulatory compliance
- Enforce Zero Trust principles

---

## How It Works

Instead of placing every device on one large network, organizations separate devices into logical or physical network segments.

Traffic between segments is controlled by security devices such as:

- Firewalls
- Next-Generation Firewalls (NGFWs)
- Access Control Lists (ACLs)
- VLANs
- Network Access Control (NAC)

Communication between segments is only allowed if it complies with organizational security policies.

---

## Common Network Segments

Examples include:

- User Workstations
- Servers
- Domain Controllers
- Finance Department
- Human Resources
- Guest Network
- Wireless Network
- VoIP Phones
- IoT Devices
- Security Cameras
- Data Center
- DMZ (Demilitarized Zone)

---

## Real-World Example

A company separates its network into multiple VLANs:

- Employee Workstations
- Finance Department
- Guest Wi-Fi
- Security Cameras
- Domain Controllers

Employees on the Guest Wi-Fi network are allowed Internet access but cannot communicate with internal servers or finance systems.

If an attacker compromises a guest device, network segmentation limits the attacker's ability to move into sensitive parts of the network.

---

## Advantages

- Limits lateral movement
- Improves security
- Reduces the impact of breaches
- Simplifies access control
- Supports regulatory compliance
- Improves network performance

---

## Limitations

- Requires careful planning
- More complex network management
- Misconfigured firewall rules may expose systems
- Requires ongoing maintenance

---

## Common Technologies

- VLANs
- Next-Generation Firewalls (NGFW)
- Access Control Lists (ACLs)
- Cisco Identity Services Engine (ISE)
- Aruba ClearPass
- VMware NSX (Microsegmentation)
- Azure Virtual Network (VNet)
- AWS Security Groups

---

## Related Concepts

- VLAN
- DMZ
- NAC
- Zero Trust
- Firewall
- Next-Generation Firewall (NGFW)
- ACL
- Microsegmentation

---

## Traditional Network vs Segmented Network

| Flat Network | Segmented Network |
|--------------|-------------------|
| All devices share one network | Devices are separated into security zones |
| Easier lateral movement | Limits lateral movement |
| Larger attack surface | Smaller attack surface |
| Minimal access control | Granular access control |
| Lower security | Higher security |

---

## Interview Notes

### What is Network Segmentation?

> Network segmentation is the practice of dividing a network into smaller security zones and controlling communication between those zones. It reduces the attack surface, limits lateral movement, and improves overall security by enforcing access controls between network segments.

---

## Official References

### National Institute of Standards and Technology (NIST)

https://csrc.nist.gov

---

### Cybersecurity and Infrastructure Security Agency (CISA)

https://www.cisa.gov

---

### NIST Zero Trust Architecture (SP 800-207)

https://csrc.nist.gov/pubs/sp/800/207/final

---

### Cisco Network Segmentation

https://www.cisco.com

---

### VMware NSX Microsegmentation

https://docs.vmware.com

---

## Personal Notes

Network segmentation is one of the most effective ways to limit the impact of a cyberattack. Even if an attacker successfully compromises one system, properly configured segmentation prevents unrestricted movement throughout the environment.

Segmentation is commonly implemented using VLANs, firewalls, ACLs, and NAC solutions and is a fundamental component of Zero Trust architecture.
