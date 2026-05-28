
# 🔓 IDOR (Insecure Direct Object Reference)

## 🔍 What is IDOR?

IDOR occurs when an application exposes internal object references without proper authorization checks.

---

## 💥 Why it matters

- Access other users' data
- Expose sensitive information
- Account takeover scenarios

---

## 🧠 Real-World Scenario

An API endpoint:

/api/user/123

If authorization is not checked, an attacker can access:

/api/user/124

---

## 🛠 Mitigation Strategies

- Enforce server-side authorization
- Validate user ownership
- Use indirect object references (UUIDs)
- Implement RBAC/ABAC

---

## 📂 Labs

- Basic IDOR
- API IDOR
- Privilege escalation

