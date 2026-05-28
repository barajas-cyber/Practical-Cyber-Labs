
# 🧪 IDOR Lab 2: API-Based Data Exposure

## 🎯 Objective
Demonstrate how insecure APIs expose sensitive data through IDOR.

---

## 🔍 Vulnerability Type
Insecure Direct Object Reference (IDOR)

---

## 🧠 Lab Scenario

A REST API allows users to retrieve account data:

GET /api/orders?user_id=1001

The API does not verify if the requester owns the data.

---

## ⚙️ Exploitation Steps

1. Intercept API request
2. Modify parameter:

   user_id=1001 → user_id=1002

3. Send request
4. Observe response containing another user's data

---

## 💥 Impact

- Mass data exposure
- Access to financial transactions
- Potential account takeover

---

## 🌍 Real-World Mapping

Many real-world breaches occur due to broken access control in APIs:

- Attackers enumerate IDs
- Extract large volumes of user data
- Sell or abuse sensitive information

---

## 🚨 Incident Analysis

### What went wrong

- API lacked authorization enforcement
- ID-based access control missing
- No rate limiting to prevent enumeration

---

### Attack Flow

1. Attacker identifies API endpoint
2. Modifies user_id parameter
3. Extracts multiple user records
4. Automates attack for bulk data extraction

---

### Incident Response Actions

- Block offending IPs
- Review API logs for abuse patterns
- Limit access to endpoints
- Apply throttling and monitoring

---

## 🛠 Mitigation

- Implement strict authorization checks
- Use access tokens tied to user identity
- Avoid exposing direct object references
- Add rate limiting and monitoring

---

## ✅ Key Takeaway

APIs are a major attack surface for IDOR vulnerabilities, especially when access control is not enforced.
