# Entry 4 | Large Scale Data Breach from Web Application Vulnerability

## Date
7/20/2025

## Description
Investigated a major data breach involving unauthorized access to over 50,000 customer records. The attacker exploited a web application weakness that allowed forced browsing and unauthorized viewing of sensitive information. This entry covers the attack method, timeline, impact, and remediation steps.

## Tools Used
- Web server access logs  
- Web application vulnerability scanner  
- Internal ticketing and alert system  
- On site investigation by the security team  

## The 5 W's

### Who caused the incident?
An unknown threat actor who discovered and exploited a vulnerability in the organization’s public e commerce web application.

### What happened?
The attacker modified order numbers in purchase confirmation URLs to access other customers’ information. This technique is known as forced browsing. Using this method, the attacker viewed and exfiltrated sensitive customer data including PII and financial details.  
After gaining access, the attacker contacted the company by email threatening to leak the data unless paid in cryptocurrency.

### When did the incident occur?
- Initial threat email: December 22, 2022 at 3:13 PM  
- Follow up extortion email: December 28, 2022 at 7:20 PM  
- Investigation period: December 28 through December 31, 2022  

### Where did the incident happen?
On the organization’s public facing e commerce platform, which had insufficient access control and URL validation.

### Why did the incident happen?
The web application failed to verify whether users were authorized to view specific order IDs. This lack of proper access control allowed the attacker to simply change the order number in the URL and access thousands of unrelated customer records.

## Additional Notes
- Estimated financial impact: $100,000  
- Attacker demanded ransom payments ranging from $25,000 to $50,000  
- More than 50,000 customer records were accessed  
- The company offered identity protection services to affected customers  
- Logs showed large scale sequential access to thousands of order records  

### Remediation Actions Taken
- Public disclosure of the breach  
- Full forensic review confirming the exploit method  
- Implemented secure URL access controls and authentication checks  
- Added allowlisting for sensitive endpoints  
- Scheduled frequent vulnerability scans and regular penetration testing  
