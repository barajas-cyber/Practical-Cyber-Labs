
# XXE (XML External Entity)

## 🔍 What is XXE?

XXE is a vulnerability that allows attackers to exploit XML parsers to read local files or perform SSRF.

---

##  Why it matters

- Read sensitive files (/etc/passwd)
- Access internal services
- Chain into SSRF attacks

---

##  Real-World Scenario

An attacker uploads malicious XML:

<!ENTITY xxe SYSTEM "file:///etc/passwd">

The server processes it and exposes system files.

---

##  Mitigation Strategies

- Disable external entity processing
- Use secure XML parsers
- Validate and sanitize input
- Avoid unnecessary XML usage

---

##  Labs

- Basic XXE
- File disclosure
- XXE → SSRF chain

