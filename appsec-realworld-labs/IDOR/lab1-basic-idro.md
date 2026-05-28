
# 🧪 IDOR Lab 1: Basic Object Reference Manipulation

## 🎯 Objective
Demonstrate how changing object identifiers can expose unauthorized data.

---

## 🔍 Vulnerability Type
Insecure Direct Object Reference (IDOR)

---

## 🧠 Lab Scenario

The application allows users to access their profile using a URL like:

/profile?id=123

The server does not properly validate whether the user owns the requested resource.

---

## ⚙️ Exploitation Steps

1. Log in as a normal user
2. Intercept or modify the request:
   
   /profile?id=123 → /profile?id=124

3. Observe that another user's data is returned

---

## 💥 Impact

- Unauthorized access to user data
- Exposure of sensitive information
- Privacy violations

---

## 🌍 Real-World Mapping

In real-world applications, IDOR vulnerabilities often occur in APIs:

GET /api/user/1001

If no authorization is enforced, attackers can access:

GET /api/user/1002

This can expose:
- personal data
- financial records
- healthcare information

---

## 🚨 Incident Analysis

### What went wrong

- No server-side authorization checks
- Application trusted user input
- No validation of resource ownership

---

### Attack Flow

1. Attacker logs into account
2. Modifies object ID in request
3. Server returns unauthorized data
4. Attacker enumerates IDs for mass data access

---

### Incident Response Actions

- Disable affected endpoints temporarily
- Identify affected users
- Audit access logs
- Notify impacted users if sensitive data exposed

---

## 🛠 Mitigation

- Enforce server-side authorization
- Validate user ownership before returning data
- Use indirect references (UUIDs instead of sequential IDs)
- Implement RBAC or ABAC controls

---

## ✅ Key Takeaway

IDOR vulnerabilities are caused by missing authorization checks, allowing attackers to access data by simply modifying identifiers.
