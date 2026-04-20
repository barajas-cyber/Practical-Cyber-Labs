# 🔐 SSRF Defense Bypass Techniques (Circumventing SSRF Protections)  - notes for ssrf with blacklist-based input filters 

## 📌 Overview

Applications often implement defenses to prevent **Server-Side Request Forgery (SSRF)** by restricting which URLs a server can request. However, these defenses are frequently **incomplete or improperly implemented**, allowing attackers to **circumvent (bypass)** them.

SSRF defenses typically rely on:

* Blacklisting internal IPs (e.g., `127.0.0.1`, `localhost`)
* Allowlisting trusted domains
* Validating URL structure (string-based checks)

These approaches can often be bypassed due to **inconsistent URL parsing, weak validation logic, or improper DNS handling**.

---

## 🔥 Common SSRF Bypass Techniques

---

## 🔹 1. Alternative IP Address Representations

Many filters block:

```text
127.0.0.1
localhost
```

However, attackers can represent the same IP in alternative formats:

```text
127.0.0.1       → standard
2130706433      → decimal
017700000001    → octal
0x7f000001      → hexadecimal
127.1           → shorthand
```

👉 These resolve to the same loopback address but may bypass string-based filters.

---

## 🔹 2. Domain Name Resolution (DNS Rebinding / Controlled Domains)

Instead of directly using a blocked IP:

```text
http://127.0.0.1/admin
```

An attacker can use a domain that resolves to it:

```text
http://attacker-controlled-domain.com/admin
```

Where:

```text
attacker-controlled-domain.com → 127.0.0.1
```

### 🧪 In PortSwigger Labs:

```text
spoofed.burpcollaborator.net → 127.0.0.1
```

👉 This bypasses filters that only check for literal IP strings.

---

## 🔹 3. URL Encoding and Obfuscation

Filters may fail to normalize input before validation.

Examples:

```text
http://127.0.0.1/admin
http://127.0.0.1%2fadmin
http://127.0.0.1/%61dmin   (URL-encoded path)
```

Case variation may also bypass filters:

```text
HTTP://127.0.0.1
hTTp://127.0.0.1
```

---

## 🔹 4. Open Redirect Exploitation

If a server allows requests to trusted domains:

```text
http://trusted.com
```

An attacker can use an open redirect:

```text
http://trusted.com/redirect?url=http://127.0.0.1/admin
```

👉 The application validates `trusted.com`, but the request is redirected to an internal resource.

---

## 🔹 5. Protocol Switching

Applications may restrict certain protocols:

```text
http://
```

Attackers may try:

```text
https://
ftp://
gopher://
file://
```

👉 Some back-end systems support additional protocols that can be abused.

---

## 🔹 6. Redirect Handling Variations

Different HTTP redirect codes behave differently:

```text
301 → permanent redirect
302 → temporary redirect
307/308 → preserve HTTP method
```

👉 Some applications validate the initial request but fail to validate redirected destinations.

---

## 🧠 Root Cause of These Bypasses

Most SSRF bypasses exploit:

```text
✔ Improper input validation
✔ Inconsistent URL parsing
✔ Failure to resolve and validate DNS results
✔ Trusting user-controlled input
```

---

## 🔥 Key Takeaway

```text
SSRF defenses often fail because they validate how a URL LOOKS, not where it actually RESOLVES.
```

---

## 📚 References (Legitimate Sources)

### 🔗 OWASP SSRF Overview

https://owasp.org/www-community/attacks/Server_Side_Request_Forgery

### 🔗 OWASP Top 10 (SSRF – A10:2021)

https://owasp.org/Top10/A10_2021-Server-Side_Request_Forgery_(SSRF)/

### 🔗 PortSwigger SSRF Documentation

https://portswigger.net/web-security/ssrf

### 🔗 PortSwigger SSRF Bypass Techniques

https://portswigger.net/web-security/ssrf#bypassing-common-ssrf-defenses

### 🔗 RFC 3986 (URL Parsing Standard)

https://datatracker.ietf.org/doc/html/rfc3986

### 🔗 DNS Rebinding Explanation (OWASP)

https://owasp.org/www-community/attacks/DNS_Rebinding

---

## 🧠 Final Insight

```text
Effective SSRF defense requires validating BOTH:
1. The URL structure
2. The resolved destination (IP address and network location)
```

---


