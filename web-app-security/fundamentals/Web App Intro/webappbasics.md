# Real-World Web Application Attacks

## SQL Injection (SQLi)
- Exploits unsafe handling of user input in database queries
- Can be used to:
  - Extract sensitive data
  - Dump user credentials
  - Access internal systems

### Real-World Impact
- Extract Active Directory usernames
- Perform password spraying on VPN or email portals

---

## File Inclusion (LFI/RFI)
- Allows reading server files or executing code

### Real-World Impact
- Read source code
- Discover hidden endpoints
- Potential remote code execution (RCE)

---

## Unrestricted File Upload
- Upload functionality allows any file type

### Real-World Impact
- Upload malicious scripts (e.g., web shell)
- Gain full control of the server

---

## Insecure Direct Object Reference (IDOR)
- Accessing resources by modifying IDs (e.g., user IDs)

### Example
/user/701 → change to → /user/702

### Real-World Impact
- Access other users’ data
- Modify accounts without authorization

---

## Broken Access Control
- System fails to properly enforce permissions

### Example
POST request:
username=bjones&password=Welcome1&roleid=3

Modify role ID to 0 or 1:
roleid=0 or 1 → become admin

### Real-World Impact
- Privilege escalation
- Full admin access

---

## Attacker Mindset (IMPORTANT)

Attackers ask:
"What happens if I change this value?"

- Change IDs
- Change roles
- Modify requests
- Upload unexpected files

---

## Key Takeaway

Most vulnerabilities happen because:
👉 The server trusts user input too much
