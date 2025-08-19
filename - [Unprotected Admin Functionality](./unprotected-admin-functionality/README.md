# Unprotected Admin Functionality Lab  

This repository documents my completion of the **Unprotected Admin Functionality** lab from PortSwigger Web Security Academy. The lab demonstrates how an unprotected administrative interface can be discovered and exploited. The goal is to delete the user "carlos".  

---

## Objectives  
- Discover the hidden admin panel by analyzing application files.  
- Access the admin interface without authentication.  
- Delete the user "carlos" to complete the lab.  

---

## Tools & Environment  
- PortSwigger Web Security Academy lab environment  
- Burp Suite or a web browser for accessing URLs  
- Web browser (Chrome)  

---

## Steps Taken  

1. Inspect "robots.txt"  
   Accessed "https://<lab-domain>/robots.txt". Noticed a line like "Disallow: /administrator-panel" that revealed the path to the admin interface.  

2. Navigate to Admin Panel  
   In the browser’s address bar, replaced "robots.txt" with "/administrator-panel". This loaded the admin interface without requiring login.  

3. Exploit the Admin Interface  
   Located and deleted the user "carlos" using the available functionality.  

---

## Results  
- Successfully discovered the admin panel via "robots.txt".  
- Accessed the interface without authentication or authorization checks.  
- Deleted the user "carlos", completing the lab.  

---

## Key Takeaways  
- Relying on security through obscurity (like hiding admin URLs) is ineffective.  
- Admin functionalities should always be protected by authentication and proper access control.  
- Files like "robots.txt" can inadvertently expose sensitive endpoints. Always audit them.  

---

## Mitigation Suggestions  
- Require authentication for all admin endpoints.  
- Avoid naming or disclosing admin paths in public files like "robots.txt".  
- Monitor and log access to sensitive routes and alert on suspicious activity.
