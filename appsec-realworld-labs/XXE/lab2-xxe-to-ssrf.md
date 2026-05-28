
# 🧪 XXE Lab 2: XXE to SSRF (Chaining Attack)

## 🎯 Objective
Demonstrate how XXE can be used to perform Server-Side Request Forgery (SSRF).

---

## 🔍 Vulnerability Type
XML External Entity (XXE) → SSRF

---

## 🧠 Lab Scenario

The application processes XML input and allows external entity resolution.

The XML parser can fetch external URLs.

---

## ⚙️ Exploitation Steps

1. Intercept XML request
2. Inject payload:

<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "http://169.254.169.254/latest/meta-data/"> ]>
<data>&xxe;</data>

3. Send request
4. Observe server making request to internal endpoint

---

## ⚠️ Important Note

The endpoint:
http://169.254.169.254

- Cannot be accessed from browser
- Can be accessed by vulnerable server

---

## 💥 Impact

- Internal network access
- Cloud metadata exposure
- Credential leakage

---

## 🌍 Real-World Mapping

Attack chain:

1. XXE vulnerability discovered
2. Used to trigger SSRF
3. SSRF targets metadata service
4. Attacker retrieves credentials
5. Attacker escalates access

---

## 🚨 Incident Analysis

### What went wrong

- XML parser allowed external URL fetching
- No network restrictions
- Metadata service exposed

---

### Attack Flow

1. Attacker injects XML entity
2. Server fetches remote resource
3. Internal service accessed
4. Sensitive response returned

---

### Incident Response Actions

- Disable external entity resolution
- Restrict outbound requests
- Monitor unusual traffic
- Secure metadata endpoints

---

## 🛠 Mitigation

- Disable external entities
- Use XML validation
- Restrict outbound network traffic
- Implement Zero Trust principles

---

## ✅ Key Takeaway

XXE can be chained into SSRF, turning a file-read vulnerability into a full infrastructure compromise.
