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
- [Format Used in Every Entry](#format-used-in-every-entry)
- [Purpose of This Journal](#purpose-of-this-journal)

---

## About This Repo

This repo holds my collection of incident handler journal entries.  
Each entry comes from hands-on labs, alert simulations, Splunk analysis, Suricata rules, malware investigations, and general cybersecurity exercises.

Every entry follows the same structure so I can practice thinking and documenting like a SOC analyst. This journal acts as both a learning tool and a portfolio showcasing the security work I’ve completed.

---

## Tools Used Across Entries

- Splunk Enterprise  
- Splunk Cloud  
- Suricata  
- Wireshark  
- VirusTotal  
- Linux command line  
- Packet capture data  
- Hashing & IOC lookup tools  
- Authentication / system logs  
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


*(More entries coming soon.)*

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
- Additional notes  

---

## Purpose of This Journal

The goal of this journal is to track my progress as I learn cybersecurity and gain hands-on skills.  
This documentation helps me practice:

- analyzing logs  
- investigating alerts  
- understanding network traffic  
- writing clear, structured incident reports  
- thinking like a SOC analyst  

New entries will be added as I complete more labs, tools, and investigations.

