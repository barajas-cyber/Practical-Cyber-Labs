
#  SSRF Lab 1: Internal Request Access

##  Objective
Demonstrate how SSRF can force a server to access internal resources.

---

##  Vulnerability Type
Server-Side Request Forgery (SSRF)

---

##  Lab Scenario

The application allows users to input a URL to fetch data.

The backend server processes the request and returns the response.

---

##  Exploitation Steps

1. Identify URL input parameter
2. Replace value with internal address:

http://localhost

or

http://127.0.0.1

3. Observe server response

---

##  Impact

- Access internal services
- Discover hidden endpoints
- Potential privilege escalation

---

##  Real-World Attack Mapping

In real environments, attackers move beyond localhost and target:

http://169.254.169.254/latest/meta-data/

 This endpoint is **only accessible from inside the server**, not from a browser.

If successful:
- attacker retrieves cloud credentials
- attacker gains access to infrastructure resources

---

##  Incident Analysis

### What went wrong
- Server trusted user input
- No outbound request filtering
- No network segmentation

---

### Attack flow

1. Attacker submits malicious URL
2. Server makes internal request
3. Sensitive data returned to attacker

---

### Response actions

- Block internal IP ranges
- Restrict outgoing requests
- Audit logs for unusual requests
- Rotate any exposed credentials

---

##  Mitigation

- Validate input URLs strictly
- Use allowlists for external requests
- Prevent access to internal IP ranges
- Protect metadata endpoints

---

## ✅ Key Takeaway

SSRF can turn a simple feature into a full system compromise if internal services are exposed.
``
