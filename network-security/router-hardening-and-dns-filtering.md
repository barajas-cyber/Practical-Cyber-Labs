# Router Hardening and DNS Filtering

## Overview
This guide provides practical steps to secure a home or small business network and restrict access to malicious and inappropriate content, including adult websites.

---

## Threat Overview

Unsecured networks can expose users to:

- Malicious websites  
- Phishing attacks  
- Adult content  
- Unsafe browsing behavior  

This is especially important for:

- Families  
- Small businesses  
- Guest networks  

---

## Router Hardening Steps

### 1. Change Default Credentials

- Log into your router (e.g., `192.168.0.1`)  
- Change:
  - Admin username  
  - Admin password  

> ⚠️ Default credentials are publicly known and easily exploited.

---

### 2. Update Router Firmware

- Check for firmware updates  
- Apply the latest version  

✔ Fixes known vulnerabilities  
✔ Improves overall security  

---

### 3. Disable Remote Management

- Turn OFF:
  - Remote access (WAN access to router)  

✔ Prevents external attackers from accessing your network  

---

### 4. Configure Secure Wi-Fi

- Use:
  - WPA2 or WPA3 encryption  
- Disable:
  - WPS (Wi-Fi Protected Setup)  

✔ Prevents unauthorized access  

---

## DNS Filtering (Content Blocking)

### Option A — Cisco Umbrella (Recommended)

Use the following DNS servers:

208.67.222.222
208.67.220.220


✔ Blocks:
- Adult content  
- Malware  
- Phishing domains  

---

### Option B — OpenDNS Family Shield

208.67.222.123
208.67.220.123



✔ Automatically blocks:
- Pornography  
- Proxy sites  
- Unsafe content  

---

## Enforcing DNS Filtering

- Configure DNS settings at the router level  
- Block outbound DNS traffic (port 53) except for approved DNS servers  

> ⚠️ Some devices use DNS over HTTPS (DoH), which may bypass filtering.

---

## Network Segmentation

### Create a Guest Network

- Separate:
  - Business devices  
  - Guest devices  

✔ Reduces risk if a device is compromised  

---

## Monitoring and Maintenance

Regularly:

- Review connected devices  
- Check router logs  
- Apply firmware updates  

---

## Business Value

This configuration helps:

- Protect employees and families  
- Reduce risk of malware infections  
- Enforce safe browsing policies  
- Improve overall network security  

---

## Real-World Use Case

Ideal for:

- Small businesses (e.g., HVAC companies like A&B Heating & Cooling)  
- Homes with children  
- Offices with shared Wi-Fi  

---

## Key Takeaway

Security is not just about blocking attacks — it is about controlling access.

By combining:

- Router hardening  
- DNS filtering  

You create a safer and more controlled network environment.
