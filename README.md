# Incident Handlers Journal

Cybersecurity journal documenting my investigations, SOC style entries, and hands-on analysis across different tools and scenarios. This repo grows as I complete new labs, incidents, and training exercises.

---

## Badges

![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Security](https://img.shields.io/badge/Focus-Cybersecurity-blue)
![Learning](https://img.shields.io/badge/Learning-In%20Progress-orange)

---

## Table of Contents

- [About This Repo](#about-this-repo)
- [Tools Used Across Entries](#tools-used-across-entries)
- [Entry Summaries](#entry-summaries)
- [LetsDefend Alert Summary](#letsdefend-alert-summary)
- [Format Used in Every Entry](#format-used-in-every-entry)
- [Purpose of This Journal](#purpose-of-this-journal)

---

## About This Repo

This repo holds my collection of incident handler journal entries.  
Each entry comes from hands-on labs, alert simulations, Splunk analysis, Suricata rules, malware investigations, LetsDefend SOC alerts, and general cybersecurity exercises.

Every entry follows the same structure so I can practice thinking and documenting like a SOC analyst. This journal acts as both a learning tool and a portfolio showcasing the security work I’ve completed.

---

## Tools Used Across Entries

- Splunk Enterprise  
- Splunk Cloud  
- LetsDefend  
- ANY.RUN malware sandbox  
- Suricata  
- Wireshark  
- VirusTotal  
- Linux command line  
- Packet capture data  
- Hashing & IOC lookup tools  
- URL analysis tools  
- Malware sandboxing tools  
- Authentication / system logs  
- Proxy logs  
- SIEM alerts  
- Endpoint activity review  
- IOC review  
- C2 traffic analysis  
- Quarantine and cleanup verification  
- Malware alerts  
- EDR alerts  

---

## Entry Summaries

### [Entry 1 – Ransomware at a Hospital](Entry%201%20Ransomware.md)
A staff member opened a phishing email that deployed ransomware. The entry covers the infection path, early response attempts, and training recommendations.

### [Entry 2 – Wireshark Packet Analysis](Entry%202%20Wireshark.md)
Analyzed a packet capture showing normal browsing traffic. Reviewed DNS lookups, TCP handshakes, ICMP packets, and HTTP traffic using filters to isolate important details.

### [Entry 3 – VirusTotal Malicious File Investigation](Entry%203%20VirusTotal.md)
Investigated a suspicious spreadsheet containing a hidden payload. Used SHA256 hashing and VirusTotal to confirm malware and collect indicators of compromise.

### [Entry 4 – Forced Browsing Data Breach](Entry%204%20DataBreach.md)
Reviewed a major data breach caused by insecure URL access on an e-commerce site. Attackers retrieved more than fifty thousand customer records by altering order numbers.

### [Entry 5 – Suricata Custom Rule Detection](Entry%205%20Suricata.md)
Built a custom Suricata rule to detect HTTP GET traffic. Validated the rule with sample PCAP data and analyzed the alerts inside fast log and eve json.

### [Entry 6 – Splunk Cloud SSH Attack Analysis](Entry%206%20Splunk%20Buttercup%20Games.md)
Investigated over three hundred failed SSH login attempts targeting the root account on a mail server. Used Splunk searches to identify brute force patterns and recommended SSH hardening steps.

### [Entry 7 – LetsDefend SOC119 Proxy Malicious Executable File Detected](Entry%207%20LetsDefend%20SOC119%20Proxy%20Alert.md)
Investigated a medium severity proxy alert involving a suspected malicious executable file. Used the LetsDefend playbook to analyze the URL address and determine whether the activity was actually malicious. The case was closed as a false positive because no malicious behavior was found.

### [Entry 8 – LetsDefend SOC109 Emotet Malware Detected](Entry%208%20LetsDefend%20SOC109%20Emotet%20Malware.md)
Investigated a medium severity Emotet malware alert. Reviewed malware related indicators, analyzed the malware, checked for possible C2 related activity, and verified whether the malware was quarantined or cleaned. The case was closed as a true positive.

### [Entry 9 – LetsDefend SOC104 Malware Detected](Entry%209%20LetsDefend%20SOC104%20Malware%20Detected.md)
Handled a high severity malware alert involving endpoint `10.15.15[.]18`, user `AdamPRD`, suspicious outbound communication to `92.63.8[.]47`, and a downloaded file named `Invoice.exe`. After sandboxing the URL and file with malware analysis tools such as ANY.RUN, the activity was identified as malicious and linked to Maze ransomware. The endpoint was contained for remediation.

*(More entries coming soon.)*

---

## LetsDefend Alert Summary

| Entry | Severity | Date Closed | Event Time | Rule Name | Event ID | Type | Result | Action |
|---|---|---|---|---|---|---|---|---|
| Entry 7 | Medium | May 1, 2026, 10:18 PM | March 21, 2021, 1:02 PM | SOC119 Proxy Malicious Executable File Detected | 83 | Proxy | False Positive | Analyzed the URL address and found nothing malicious |
| Entry 8 | Medium | May 1, 2026, 9:23 PM | March 22, 2021, 9:06 PM | SOC109 Emotet Malware Detected | 85 | Malware | True Positive | Analyzed the malware, reviewed possible C2 related activity, and checked whether the malware was quarantined or cleaned |
| Entry 9 | High | April 28, 2026, 3:26 PM | December 1, 2020, 10:23 AM | SOC104 Malware Detected | 36 | Malware | True Positive | Sandboxed the suspicious URL and file, confirmed Maze ransomware behavior, and contained the endpoint |

---

## LetsDefend Case Details

### Entry 7 – SOC119 Proxy Malicious Executable File Detected

| Field | Value |
|---|---|
| Severity | Medium |
| Date closed | May 1, 2026, 10:18 PM |
| Event time | March 21, 2021, 1:02 PM |
| Event ID | 83 |
| Type | Proxy |
| Rule | SOC119 Proxy Malicious Executable File Detected |
| Result | False Positive |
| Playbook step completed | Analyze URL Address |
| Analyst note | Nothing malicious |

This case involved a proxy alert for a suspected malicious executable file. I reviewed the URL address connected to the alert and checked whether the activity showed signs of malware delivery, suspicious file download behavior, or confirmed malicious indicators.

After reviewing the available evidence, the case was closed as a false positive because nothing malicious was found. This entry shows the importance of validating alerts instead of assuming every suspicious rule name means a confirmed compromise.

### Entry 8 – SOC109 Emotet Malware Detected

| Field | Value |
|---|---|
| Severity | Medium |
| Date closed | May 1, 2026, 9:23 PM |
| Event time | March 22, 2021, 9:06 PM |
| Event ID | 85 |
| Type | Malware |
| Rule | SOC109 Emotet Malware Detected |
| Result | True Positive |
| Playbook steps completed | Analyze Malware, Check if the malware is quarantined or cleaned |
| Analyst note | No analyst note was entered in the platform |

This case involved a malware alert related to possible Emotet activity. I reviewed the malware related indicators, analyzed the malware evidence, and checked whether the malware was quarantined or cleaned.

The alert was closed as a true positive. This case helped me practice malware triage, IOC review, C2 investigation logic, and post detection response verification.

### Entry 9 – SOC104 Malware Detected

| Field | Value |
|---|---|
| Severity | High |
| Date closed | April 28, 2026, 3:26 PM |
| Event time | December 1, 2020, 10:23 AM |
| Event ID | 36 |
| Type | Malware |
| Rule | SOC104 Malware Detected |
| Result | True Positive |
| Endpoint | 10.15.15[.]18 |
| User | AdamPRD |
| External IP | 92.63.8[.]47 |
| File name | Invoice.exe |
| Malware family | Maze ransomware |

This case involved a high severity malware alert from the SIEM. Endpoint `10.15.15[.]18`, used by `AdamPRD`, was observed communicating with external IP address `92.63.8[.]47`. The communication was allowed and involved the endpoint downloading a suspicious file named `Invoice.exe`.

The suspicious file was downloaded from:

`hxxps://files-ld.s3.us-east-2.amazonaws.com/f83fb9ce6a83da58b20685c1d7e1e546.zip`

After sandboxing the URL and file with malware analysis tools such as ANY.RUN, the activity was confirmed as malicious and linked to Maze ransomware. The endpoint was contained for remediation and follow up with the user.

---

## Format Used in Every Entry

- Date  
- Entry number  
- Description  
- Tools used  
- The Five W's  
  - Who caused it  
  - What happened  
  - When it happened  
  - Where it happened  
  - Why it happened  
- Investigation notes  
- Result  
- Action taken  
- Additional notes  

---

## Purpose of This Journal

The goal of this journal is to track my progress as I learn cybersecurity and gain hands-on skills.  
This documentation helps me practice:

- analyzing logs  
- investigating alerts  
- understanding network traffic  
- reviewing malware detections  
- using malware sandboxing tools  
- reviewing IOCs  
- checking C2 related activity  
- documenting proxy and endpoint activity  
- verifying quarantine and cleanup status  
- writing clear, structured incident reports  
- thinking like a SOC analyst  

New entries will be added as I complete more labs, tools, and investigations.
