
# 🧪 XXE Lab 1: Basic File Disclosure

## 🎯 Objective
Demonstrate how XXE can be used to read local files on the server.

---

## 🔍 Vulnerability Type
XML External Entity (XXE)

---

## 🧠 Lab Scenario

The application accepts XML input and processes it without secure configuration.

The XML parser allows external entities.

---

## ⚙️ Exploitation Steps

1. Intercept request containing XML
2. Inject malicious XML payload:

<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]>
<user>
  <name>&xxe;</name>
</user>

3. Send request
4. Observe response including file contents

---

## 💥 Impact

- Read sensitive system files
- Expose application configuration
- Access secrets stored on server

---

## 🌍 Real-World Mapping

In real environments, attackers use XXE to read:

- configuration files
- API keys
- credential files

This can lead to deeper system compromise.

---

## 🚨 Incident Analysis

### What went wrong

- XML parser allowed external entities
- No input sanitization
- Sensitive files accessible

---

### Attack Flow

1. Attacker injects malicious XML
2. Server processes entity
3. Server reads local file
4. Data returned to attacker

---

### Incident Response Actions

- Disable vulnerable XML parsing feature
- Identify exposed data
- Rotate compromised credentials
- Patch application

---

## 🛠 Mitigation

- Disable external entities (XXE)
- Use secure XML parsers
- Validate input
- Avoid XML if not required

---

## ✅ Key Takeaway

XXE allows attackers to read sensitive files when XML parsing is not securely configured.
