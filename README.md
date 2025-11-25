# Incident-Handlers-Journal
Cybersecurity incident journal with documented investigations, SOC style entries, and analysis across multiple tools.
# Incident Handlers Journal

This repo holds my collection of incident handler journal entries. Each entry comes from hands on labs, simulated alerts, Splunk investigations, Suricata rules, malware checks, phishing analysis, and other cybersecurity exercises. I use a consistent structure for every entry to build good habits and learn how to think and write like a SOC analyst.

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
  - [Entry 1 – Ransomware at a Hospital](#entry-1--ransomware-at-a-hospital)
  - [Entry 2 – Wireshark Packet Analysis](#entry-2--wireshark-packet-analysis)
  - [Entry 3 – VirusTotal Malicious File Investigation](#entry-3--virustotal-malicious-file-investigation)
  - [Entry 5 – Forced Browsing Data Breach](#entry-5--forced-browsing-data-breach)
  - [Entry 6 – Suricata Custom Rule Detection](#entry-6--suricata-custom-rule-detection)
  - [Entry 7 – Splunk Cloud SSH Attack Analysis](#entry-7--splunk-cloud-ssh-attack-analysis)
  - [Entry 8 – Splunk SSH Brute Force Dashboard](#entry-8--splunk-ssh-bruteforce-dashboard)
- [Format Used in Every Entry](#format-used-in-every-entry)
- [Purpose of This Journal](#purpose-of-this-journal)

---

## About This Repo

This journal is a record of the cybersecurity incidents, investigations, and analyses I have completed. I document everything using the five W format so I can break down each situation clearly and understand the reasoning behind it. The entries come from different tools, different types of attacks, and different security situations.

This repo acts as both a learning tool and a portfolio of my work as I continue to build experience in cybersecurity.

---

## Tools Used Across Entries

- Splunk Enterprise  
- Splunk Cloud  
- Wireshark  
- VirusTotal  
- Suricata  
- Linux command line  
- Hashing and IOC lookup tools  
- Packet capture data  
- Authentication and system logs  
- EDR alerts  

---

## Entry Summaries

### Entry 1 – Ransomware at a Hospital
A staff member opened a phishing email that deployed ransomware. The entry covers the initial impact, the suspected infection path, and early containment thoughts. Includes training recommendations for staff in high-risk environments like hospitals.

### Entry 2 – Wireshark Packet Analysis
Examined a web browsing packet capture. Looked at DNS, TCP handshake details, HTTP traffic, ICMP packets, and used filters to isolate important data. Learned how to read layered network communication.

### Entry 3 – VirusTotal Malicious File Investigation
Analyzed a suspicious spreadsheet file containing a hidden payload. Used SHA256 hashing and VirusTotal to confirm malware, identify IoCs, and recommend containment actions such as blocking domains and reimaging the device.

### Entry 5 – Forced Browsing Data Breach
Investigated a large-scale data breach caused by insecure URL handling in an e-commerce site. Attackers accessed over 50,000 customer records by modifying order numbers. Entry includes remediation steps such as URL authentication, public disclosure, and vulnerability scanning.

### Entry 6 – Suricata Custom Rule Detection
Created a custom Suricata rule to detect HTTP GET traffic. Validated the rule using sample packet capture data. Used jq to parse eve.json logs, confirm alert signatures, and track flow IDs. Learned how IDS rules trigger and log activity.

### Entry 7 – Splunk Cloud SSH Attack Analysis
Reviewed secure.log data showing over 300 failed SSH login attempts against the root account on a mail server. Used Splunk Cloud searches to identify patterns and recommend better SSH hardening.

### Entry 8 – Splunk SSH Brute Force Dashboard
Built a full Splunk dashboard showing top attacking IPs, usernames, invalid user attempts, time charts, and message breakdowns. Verified that no successful logins occurred. This entry demonstrates SIEM analysis and visualization skills.

---

## Format Used in Every Entry

- Date  
- Entry number  
- Description of what happened  
- Tools used  
- The five W's  
  - Who caused it  
  - What happened  
  - When it happened  
  - Where it happened  
  - Why it happened  
- Additional notes  

---

## Purpose of This Journal

The purpose of this journal is to track my progress as I learn cybersecurity. It helps me build experience in analyzing logs, investigating alerts, understanding network activity, and writing clear incident summaries. It also acts as a portfolio showing how I approach and document real security problems.

New entries will be added as I complete more labs, tools, and investigations.

