
#  SSRF Lab 2: Cloud Metadata Exploitation

##  Objective
Exploit SSRF to access cloud metadata and simulate credential exposure.

---

##  Vulnerability Type
Server-Side Request Forgery (SSRF)

---

##  Lab Scenario

The application allows users to submit a URL that the server fetches and returns.

The server does not validate or restrict outgoing requests.

---

##  Exploitation Steps

1. Identify a URL input parameter
2. Modify the request to target metadata service:

http://169.254.169.254/latest/meta-data/

3. Enumerate available endpoints (if accessible):
   - /iam/
   - /iam/security-credentials/

4. Extract credentials (simulated in lab environment)

---

##  Important Note

The metadata endpoint (169.254.169.254) is:

- NOT accessible from a regular user browser
- ONLY accessible from within the server or cloud instance

This is why SSRF is required to exploit it.

---

##  Impact

- Exposure of cloud credentials
- Unauthorized API access
- Full infrastructure compromise
- Privilege escalation

---

##  Real-World Mapping

In real-world breaches:

- Attackers exploit SSRF vulnerabilities
- Target cloud metadata endpoints
- Retrieve IAM credentials
- Use credentials to access:
  - S3 buckets
  - databases
  - internal services

---

##  Incident Analysis

### What went wrong

- User input not validated
- No outbound request filtering
- Metadata service exposed
- No authentication required for metadata access (IMDSv1)

---

### Attack Flow

1. Attacker injects malicious URL
2. Server sends request to metadata endpoint
3. Metadata response returned to attacker
4. Attacker extracts credentials
5. Attacker pivots into cloud environment

---

##  Incident Response Actions

- Immediately rotate exposed credentials
- Enable metadata protection (IMDSv2)
- Block internal IP ranges
- Audit logs for suspicious activity
- Review IAM permissions

---

##  Mitigation

- Enforce IMDSv2 (AWS)
- Restrict access to 169.254.169.254
- Validate all user-supplied URLs
- Implement outbound request filtering
- Use Zero Trust architecture

---

##  Key Takeaway

SSRF vulnerabilities become critical when cloud metadata services are exposed, allowing attackers to gain full control over cloud environments.
