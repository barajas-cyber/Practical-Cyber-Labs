
# 🔎 IDOR Incident Analysis (Real-World Perspective)

## 🧠 Attack Scenario

An application exposes user data through predictable object identifiers.

No authorization check is performed when accessing resources.

---

## ⚠️ What went wrong

- Missing access control
- Trusting user-supplied identifiers
- No validation of resource ownership

---

## 💥 Exploitation Flow

1. Attacker logs into system
2. Identifies predictable IDs
3. Modifies requests to access other users' data
4. Extracts sensitive information

---

## 🚨 Impact

- Data leakage
- Privacy violations
- Regulatory consequences (PII exposure)

---

## 🛠 Incident Response Actions

- Identify affected endpoints
- Restrict access immediately
- Perform forensic analysis on logs
- Notify affected users if necessary

---

## ✅ Mitigation

- Enforce server-side authorization
- Validate access on every request
- Use role-based access controls
- Avoid predictable identifiers

---

## 📚 Lesson Learned

Broken access control is one of the most common and critical vulnerabilities in modern applications.
