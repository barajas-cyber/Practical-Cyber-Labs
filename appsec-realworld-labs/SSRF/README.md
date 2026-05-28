

# 🌐 SSRF (Server-Side Request Forgery)

## 🔍 What is SSRF?

SSRF allows an attacker to make requests from the server to internal or external systems.

---

## 💥 Why it matters

- Access internal APIs
- Reach localhost services
- Expose cloud metadata (AWS, GCP)
- Potential full infrastructure compromise

---

## 🧠 Real-World Scenario

An attacker exploits a vulnerable URL parameter to make the server send requests to:

http://169.254.169.254/latest/meta-data/

This allows extraction of cloud credentials.

---

## 🛠 Mitigation Strategies

- Block internal IP ranges
- Use allowlists for outbound requests
- Disable access to metadata endpoints
- Implement IMDSv2 (AWS)

---

## 📂 Labs

- Basic SSRF
- SSRF to internal services
- SSRF to cloud metadata
``
