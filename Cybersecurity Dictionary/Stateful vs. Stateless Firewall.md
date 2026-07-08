# Stateful vs. Stateless Firewalls

**Category:** Network Security

**Last Updated:** July 2026

---

## Overview

Firewalls inspect network traffic and determine whether it should be allowed or blocked based on security rules. One of the primary differences between firewalls is whether they are **stateful** or **stateless**.

A **stateless firewall** evaluates each packet independently without considering previous packets. A **stateful firewall** maintains a record of active network connections and uses that information to make more informed security decisions.

---

## Stateless Firewall

### Definition

A **stateless firewall** examines every packet individually based on predefined rules such as:

- Source IP Address
- Destination IP Address
- Source Port
- Destination Port
- Protocol

It does **not** remember previous packets or whether a connection has already been established.

### How It Works

Each packet is treated as an independent event.

Every packet must match an allow rule before it is forwarded.

### Advantages

- Fast processing
- Low memory usage
- Simple configuration
- Suitable for basic packet filtering

### Limitations

- No awareness of active sessions
- Less secure
- Cannot distinguish between legitimate and unsolicited traffic

---

## Stateful Firewall

### Definition

A **stateful firewall** tracks active network connections using a **state table**.

Instead of evaluating every packet independently, it determines whether a packet belongs to an existing, legitimate communication session.

### How It Works

When a new connection is established, the firewall records information such as:

- Source IP Address
- Destination IP Address
- Source Port
- Destination Port
- Protocol
- Connection State

Future packets belonging to that connection are automatically recognized and allowed without evaluating every firewall rule again.

### Advantages

- More secure
- Tracks established connections
- Reduces unnecessary rule processing
- Better protection against unsolicited traffic

### Limitations

- Requires additional memory
- More CPU intensive
- More complex than stateless firewalls

---

## Stateful vs. Stateless

| Stateless Firewall | Stateful Firewall |
|--------------------|-------------------|
| Examines each packet independently | Tracks active network connections |
| No memory of previous packets | Maintains a state table |
| Faster processing | More intelligent inspection |
| Basic packet filtering | Connection-aware filtering |
| Lower resource usage | Higher resource usage |
| Less secure | More secure |

---

## Real-World Example

A user opens a web browser and visits an HTTPS website.

### Stateless Firewall

Every packet exchanged between the client and the web server is evaluated independently against the firewall rules.

The firewall has no knowledge that the packets belong to the same session.

### Stateful Firewall

The firewall records the connection when it is established.

As additional packets are exchanged, the firewall verifies that they belong to an existing session before allowing them through.

---

## Common Technologies

### Stateless

- Basic Access Control Lists (ACLs)
- Traditional Packet Filtering Firewalls

### Stateful

- Cisco Secure Firewall
- Palo Alto Networks
- Fortinet FortiGate
- Check Point
- Juniper SRX
- pfSense
- OPNsense

---

## Related Concepts

- Firewall
- Packet Filtering
- Next-Generation Firewall (NGFW)
- Access Control Lists (ACLs)
- NAT
- IDS
- IPS

---

## Interview Notes

### What is the difference between a stateful and stateless firewall?

> A stateless firewall evaluates each packet independently using predefined rules such as IP addresses, ports, and protocols. It does not maintain information about previous packets or active sessions. A stateful firewall maintains a state table of active network connections and uses that information to determine whether packets belong to legitimate, established sessions. This makes stateful firewalls more secure and better suited for modern enterprise networks.

---

## Official Resources

### NIST Computer Security Resource Center

https://csrc.nist.gov

### Cisco Secure Firewall

https://www.cisco.com/c/en/us/products/security/firewalls/index.html

### Palo Alto Networks

https://www.paloaltonetworks.com

### Fortinet

https://www.fortinet.com

---

## Personal Notes

Most enterprise firewalls today are **stateful** by default. Modern **Next-Generation Firewalls (NGFWs)** build upon stateful inspection by adding application awareness, intrusion prevention (IPS), malware protection, user identity integration, URL filtering, and SSL/TLS inspection.

A useful way to think about firewall evolution is:

Packet Filtering Firewall (Stateless)
→ Stateful Inspection Firewall
→ Next-Generation Firewall (NGFW)
