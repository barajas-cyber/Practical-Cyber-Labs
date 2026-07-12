# Web Application Firewall (WAF)

**Category:** Network Security

**Last Updated:** July 2026

---

# Definition

A **Web Application Firewall (WAF)** is a security solution that monitors, filters, and blocks malicious HTTP and HTTPS traffic between clients and web applications. Unlike traditional firewalls, which primarily protect networks, a WAF is designed to protect web applications from attacks targeting the application layer (Layer 7 of the OSI model).

A WAF helps defend against common web application attacks such as SQL Injection (SQLi), Cross-Site Scripting (XSS), Cross-Site Request Forgery (CSRF), file inclusion attacks, and other threats identified by the OWASP Top 10.

---

# Primary Purpose

- Protect web applications from attacks
- Inspect HTTP and HTTPS traffic
- Block malicious requests before they reach the application
- Reduce the attack surface
- Improve application security
- Support regulatory compliance (PCI DSS, HIPAA, etc.)

---

# How It Works

A WAF sits between the client and the web application, inspecting every HTTP and HTTPS request before it reaches the web server.

When a request is received, the WAF evaluates:

- HTTP Headers
- URLs
- Cookies
- Query Parameters
- Request Body
- File Uploads
- HTTP Methods
- User Behavior

If malicious activity is detected, the WAF can:

1. Block the request.
2. Log the event.
3. Generate an alert.
4. Rate-limit requests.
5. Challenge the client (CAPTCHA).
6. Redirect or deny access.

---

# Types of WAF

## Network-Based WAF

Installed as a hardware appliance within the organization's network.

### Advantages

- High performance
- Low latency
- Full control

### Limitations

- Expensive
- Requires on-premises infrastructure

---

## Host-Based WAF

Runs directly on the web server or application.

### Advantages

- Highly customizable
- Deep integration with the application

### Limitations

- Consumes server resources
- More administrative overhead

---

## Cloud-Based WAF

Delivered as a cloud service.

### Advantages

- Easy deployment
- Automatic updates
- Scalable
- Lower maintenance

### Limitations

- Less customization
- Dependent on the service provider

---

# Common Attacks a WAF Can Mitigate

- SQL Injection (SQLi)
- Cross-Site Scripting (XSS)
- Local File Inclusion (LFI)
- Remote File Inclusion (RFI)
- Command Injection
- Directory Traversal
- HTTP Protocol Violations
- Malicious Bots
- API Abuse
- Some Cross-Site Request Forgery (CSRF) attacks

---

# Common Use Cases

- Public websites
- Customer portals
- Online banking
- E-commerce websites
- Healthcare applications
- Government portals
- APIs
- Login pages

---

# Real-World Example

A company hosts an online customer portal.

An attacker attempts a SQL Injection attack using the following payload:

```sql
' OR 1=1 --
```

The WAF inspects the incoming HTTP request, recognizes the SQL Injection signature, blocks the request, logs the event, and generates an alert for the Security Operations Center (SOC).

The malicious request never reaches the web application or database.

---

# Advantages

- Protects web applications
- Blocks common web attacks
- Improves visibility into web traffic
- Helps meet compliance requirements
- Can provide virtual patching
- Reduces application risk

---

# Limitations

- Cannot replace secure coding practices
- Requires tuning
- May generate false positives
- Cannot prevent every attack
- Limited protection against business logic flaws

---

# Common Technologies

## Commercial

- Cloudflare WAF
- AWS WAF
- Microsoft Azure Web Application Firewall
- F5 Advanced WAF
- Imperva WAF
- Akamai App & API Protector

## Open Source

- ModSecurity
- NAXSI

---

# Related Concepts

- Firewall
- Next-Generation Firewall (NGFW)
- Intrusion Prevention System (IPS)
- Reverse Proxy
- Secure SDLC
- API Security
- OWASP Top 10

---

# Firewall vs WAF

| Traditional Firewall | Web Application Firewall |
|----------------------|--------------------------|
| Protects networks | Protects web applications |
| Operates primarily at Layers 3 & 4 | Operates at Layer 7 |
| Filters IP addresses, ports, and protocols | Filters HTTP and HTTPS requests |
| Protects servers and networks | Protects websites and APIs |

---

# WAF vs NGFW

| WAF | NGFW |
|-----|------|
| Protects web applications | Protects the entire network |
| Inspects HTTP/HTTPS traffic | Inspects all network traffic |
| Focuses on Layer 7 attacks | Protects Layers 3–7 |
| Defends against OWASP Top 10 | Includes IPS, application awareness, malware detection, VPN, and more |

---

# Interview Notes

## What is a WAF?

> A Web Application Firewall (WAF) is a security solution that protects web applications by inspecting HTTP and HTTPS traffic for malicious requests. It helps prevent attacks such as SQL Injection, Cross-Site Scripting (XSS), and other OWASP Top 10 vulnerabilities before they reach the application.

---

## Official References

### OWASP

https://owasp.org/www-community/Web_Application_Firewall

---

### OWASP Top 10

https://owasp.org/www-project-top-ten/

---

### National Institute of Standards and Technology (NIST)

https://csrc.nist.gov

---

### Cybersecurity and Infrastructure Security Agency (CISA)

https://www.cisa.gov

---

### AWS WAF Documentation

https://docs.aws.amazon.com/waf/

---

### Microsoft Azure Web Application Firewall

https://learn.microsoft.com/azure/web-application-firewall/

---

### Cloudflare WAF

https://developers.cloudflare.com/waf/

---

### ModSecurity

https://modsecurity.org

---

## Personal Notes

A WAF is specifically designed to protect web applications—not entire networks. It should be considered an additional layer of security that complements secure software development practices.

Organizations commonly deploy WAFs in front of public-facing web applications and APIs to inspect HTTP/HTTPS traffic, block common web attacks, and provide visibility into attempted exploitation.

A WAF is most effective when used alongside secure coding practices, vulnerability management, regular penetration testing, and continuous monitoring through SIEM and XDR platforms.
