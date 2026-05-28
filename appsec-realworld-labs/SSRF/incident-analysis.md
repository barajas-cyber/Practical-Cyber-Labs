
#  SSRF Incident Analysis (Real-World Perspective)

##  Attack Scenario

A web application allows users to submit a URL for preview.

The backend fetches the URL without validation.

---

##  What went wrong

- No validation on user-controlled input
- Server allowed outbound requests to internal services
- No network restrictions in place

---

##  Exploitation Flow

1. Attacker submits malicious URL:
   http://169.254.169.254/latest/meta-data/

2. Server makes request internally

3. Attacker retrieves:
   - IAM credentials
   - instance metadata

4. Attacker escalates privileges

---

##  Impact

- Cloud credential exposure
- Unauthorized access to infrastructure
- Potential full environment takeover

---

##  Incident Response Actions

- Identify suspicious outbound requests
- Block access to metadata endpoints
- Rotate exposed credentials
- Audit cloud permissions

---

##  Mitigation

- Restrict internal IP access
- Implement IMDSv2 (AWS)
- Validate all user-supplied URLs
- Use outbound firewall rules

---

##  Lesson Learned

SSRF vulnerabilities can lead to complete system compromise when cloud metadata services are exposed.
