# SSRF - Basic Backend System

## Objective
Exploit a Server-Side Request Forgery (SSRF) vulnerability to access internal resources.

## Tools Used
- Burp Suite (Proxy, Repeater)

## Steps
1. Intercept the request in Burp Suite
2. Identify the parameter that fetches a URL
3. Send request to Repeater
4. Modify the URL to:
   http://localhost/admin
5. Observe response and access admin panel
6. Delete user "Carlos"

## Result
Successfully accessed internal admin functionality and performed unauthorized action.

## Impact
- Internal services exposed
- Unauthorized admin access
- Potential data manipulation

## Mitigation
- Validate user input strictly
- Block internal IP ranges (127.0.0.1, localhost)
- Use allowlists for outbound requests
- Disable unnecessary internal endpoints exposure
