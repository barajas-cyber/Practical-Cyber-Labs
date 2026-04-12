# Web Application Layout & Architecture

## Overview

Web applications are complex systems made up of multiple components, layers, and infrastructure models. Understanding how these pieces interact is critical for identifying vulnerabilities during penetration testing.

---

## Core Concepts

### 1. Infrastructure
Defines where components live:
- Servers
- Databases
- Hosting environment

---

### 2. Components
Defines what interacts:
- Client (browser)
- Server (backend)
- APIs / services

---

### 3. Architecture
Defines how everything connects:
- Communication between components
- Data flow
- Trust relationships

---

## Infrastructure Models

### Client-Server Model
- Client (browser) sends HTTP requests
- Server processes and responds

**Key Idea:**
> The attacker controls the client and manipulates requests.

---

### One Server (High Risk)
- Web app + database + logic all on one server

**Risks:**
- Single vulnerability → full system compromise
- Downtime affects everything

---

### Many Servers – One Database
- Multiple app servers connected to one database

**Benefits:**
- Partial segmentation
- Limits impact of compromise

---

### Many Servers – Many Databases
- Each application has its own database

**Benefits:**
- Strong isolation
- Better security and redundancy

---

## Web Application Components

### Client
- Browser (Chrome, Firefox)
- Executes JavaScript
- Sends HTTP requests

---

### Server
- Web server (Apache, Nginx)
- Application logic
- Database

---

### Services / APIs
- Microservices
- External integrations

---

### Serverless Functions
- Cloud-based execution (AWS Lambda, Azure Functions)

---

## Three-Tier Architecture

### 1. Presentation Layer
- UI (HTML, CSS, JavaScript)

**Common Attacks:**
- Cross-Site Scripting (XSS)

---

### 2. Application Layer
- Business logic
- Authentication & authorization

**Common Attacks:**
- Broken access control
- Logic flaws

---

### 3. Data Layer
- Database storage

**Common Attacks:**
- SQL Injection
- Data exposure

---

## Microservices

- Small independent services (e.g., login, payments)
- Communicate via APIs
- Stateless communication

**Benefits:**
- Scalability
- Flexibility
- Faster development

**Security Risks:**
- Exposed internal APIs
- Weak authentication between services
- Increased attack surface

---

## Serverless Architecture

- No traditional server management
- Runs on cloud platforms (AWS, Azure, GCP)

**Benefits:**
- Easy deployment
- Scalable

**Security Risks:**
- Misconfigured permissions (IAM)
- Exposed endpoints
- Poor access control

---

## Architecture Security

Not all vulnerabilities come from code:
> Many vulnerabilities are caused by poor design decisions.

---

### Example: Broken Access Control
- Users access admin functionality without permission

---

### Example: Poor Segmentation
- Compromising one component leads to full system access

---

## Attacker Mindset

When testing a web application, ask:

- Where is the database located?
- Is the application segmented?
- Are APIs exposed?
- Can I move between components?
- What does the server trust?

---

## Key Takeaway

Web application security is not just about code.

> Most real-world vulnerabilities come from:
- Poor architecture
- Weak trust boundaries
- Improper access control




# Front End vs Back End

## Overview

Web applications are divided into two main parts:

- Front End (Client-side)
- Back End (Server-side)

Understanding the difference is critical for identifying where vulnerabilities exist.

---

## Front End (Client-Side)

The front end is everything the user sees and interacts with in the browser.

### Technologies:
- HTML → structure
- CSS → design
- JavaScript → functionality

### Responsibilities:
- Display UI (text, buttons, forms)
- Handle user interaction
- Send requests to the server

### Key Idea:
> The front end runs in the browser and is fully visible to the attacker.

---

## Back End (Server-Side)

The back end handles all core functionality and runs on the server.

### Main Components:

#### 1. Back End Server
- Hosts the application
- OS (Linux, Windows)

#### 2. Web Server
- Handles HTTP requests
- Examples: Apache, NGINX, IIS

#### 3. Database
- Stores application data
- Examples: MySQL, PostgreSQL, MongoDB

#### 4. Frameworks
- Used to build applications
- Examples:
  - Laravel (PHP)
  - Django (Python)
  - Express (Node.js)

---

## Back End Responsibilities

- Process user requests
- Execute business logic
- Handle authentication
- Store/retrieve data
- Communicate with APIs

---

## Key Difference

| Front End | Back End |
|----------|--------|
| Visible to user | Hidden from user |
| Runs in browser | Runs on server |
| Handles UI | Handles logic + data |

---

## Security Implications

Even though the back end is not visible:
> It is still vulnerable to attacks.

### Example Attacks:
- SQL Injection → manipulate database queries
- Command Injection → execute OS commands
- File Inclusion → read server files

---

## Attacker Perspective

- You can see and modify front-end behavior
- You cannot see back-end code directly
- You attack the back end through requests

---

## Whitebox vs Blackbox Testing

### Whitebox Pentesting
- Full access to source code
- Can review logic directly

### Blackbox Pentesting
- No access to source code
- Test by interacting with the application

> Most bug bounty = Blackbox testing

---

## Common Developer Mistakes

- Trusting user input
- Storing passwords in plain text
- Weak authentication
- Not validating input
- Relying too much on client-side validation
- Using outdated components

---

## OWASP Top 10 (Important)

These are the most common web vulnerabilities:

1. Broken Access Control
2. Cryptographic Failures
3. Injection (SQL, Command)
4. Insecure Design
5. Security Misconfiguration
6. Vulnerable Components
7. Authentication Failures
8. Data Integrity Issues
9. Logging Failures
10. SSRF (Server-Side Request Forgery)

---

## Key Takeaway

- Front end = what you see  
- Back end = what you attack  

> Most vulnerabilities exist because the server trusts user input too much.




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
