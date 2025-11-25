# Incident Handlers Journal

Cybersecurity journal documenting my investigations, SOC style entries, and hands-on analysis across different tools and scenarios.

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
Each entry comes from hands-on labs, simulated alerts, Splunk investigations, Suricata rules, malware checks, phishing analysis, and other cybersecurity exercises.

I use the same structure in every entry so I can practice thinking and writing like a SOC analyst. This repo is both a learning tool and a growing portfolio of my cybersecurity experience.

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

### Entry 1 – Ransomware at a Hospital  
A staff member opened a phishing email that deployed ransomware. Covers infection path, impact, and recommendations like better staff training and awareness.

### Entry 2 – Wireshark Packet Analysis  
Analyzed a web browsing PCAP. Looked at DNS queries, TCP handshake details, HTTP traffic, ICMP echo requests, and used filters to inspect specific protocol data.

### Entry 3 – VirusTotal Malicious File Investigation  
Investigated a suspicious spreadsheet with a hidden malicious payload. Used SHA256 hashing and VirusTotal to confirm malware and record IoCs. Recommended blocking indicators and reimaging the device.

### Entry 4 – Forced Browsing Data Breach  
Reviewed a major data breach caused by insecure URL access on an e-commerce site. Attackers accessed over 50,000 customer records. Includes remediation steps such as URL authentication, IDs, and vulnerability scanning.

### Entry 5 – Suricata Custom Rule Detection  
Created a custom Suricata rule to detect HTTP GET requests. Validated the rule with sample PCAP data and analyzed alerts in fast.log and eve.json using jq.

### Entry 6 – Splunk Cloud SSH Attack Analysis  
Analyzed secure.log data for repeated SSH brute force attempts against the root account on a mail server. Identified attack patterns and recommended SSH hardening.

*(More entries will be added as I complete them.)*

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

The goal of this journal is to track my progress as I learn cybersecurity.  
It helps me:

- practice analyzing logs  
- investigate alerts  
- understand network traffic  
- write clear incident reports  
- build real SOC analyst habits  

This repo grows as I complete new labs, tools, and investigations.

