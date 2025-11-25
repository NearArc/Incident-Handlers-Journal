# Entry 3 | Malicious File Investigation with VirusTotal

## Date
7/19/2025

## Description
Investigated an alert involving a suspicious file downloaded by an employee. The file contained a hidden malicious payload that executed when opened. Used SHA256 hashing and VirusTotal to gather indicators of compromise and confirm the file’s malicious nature.

## Tools Used
- VirusTotal  
- SHA256 hashing utility  
- Endpoint Detection and Response (EDR) alert system  

## The 5 W's

### Who caused the incident?
A threat actor who sent a phishing email containing a password protected Excel spreadsheet with a malicious payload embedded inside.

### What happened?
The employee opened the spreadsheet using the provided password in the phishing email. Once opened, the hidden payload ran on the system, triggering an EDR alert. The file was extracted, hashed using SHA256, and the hash was submitted to VirusTotal for analysis.

### When did the incident occur?
The email was opened at approximately 9:43 AM. The alert was received and investigated on 7/19/2025.

### Where did the incident happen?
On an employee workstation inside the internal network of a financial services company.

### Why did the incident happen?
The employee trusted the phishing email because the file was password protected, giving it a false sense of legitimacy. This reduced suspicion and led to the payload being executed.

## Additional Notes
- The SHA256 hash confirmed the file was a known malicious sample.  
- VirusTotal identified several IoCs including:  
  - malicious domains  
  - embedded macros  
  - connections to command and control (C2) servers  
- The incident was escalated to the level two SOC team for containment and further review.  

### Recommended Actions
- Block all identified malicious URLs, IPs, and domains at the firewall.  
- Re image the affected workstation to fully remove malware.  
- Conduct phishing awareness training for employees.  
- Review email filtering settings to prevent similar attachments from bypassing defenses.  
