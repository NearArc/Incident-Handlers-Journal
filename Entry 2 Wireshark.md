# Entry 2 | Wireshark Packet Capture Analysis

## Date
7/20/2025

## Description
Used Wireshark to inspect packet capture data during a simulated investigation involving normal browsing traffic between a local system and a web server. Practiced applying filters, analyzing protocols, and interpreting DNS, TCP, and ICMP packet details.

## Tools Used
- Wireshark

## The 5 W's

### Who caused the incident?
No malicious actor was involved. The activity represented normal user browsing behavior for training purposes.

### What happened?
A packet capture (.pcap) file was analyzed to review network traffic. The investigation focused on identifying:
- source and destination IP addresses  
- protocol types  
- DNS queries and responses  
- TCP payload and HTTP details  

### When did the incident occur?
During a hands-on lab exercise on 7/20/2025.

### Where did the incident happen?
Inside a cloud-based Windows virtual machine provided through the course environment.

### Why did the incident happen?
The purpose of the exercise was to practice:
- packet inspection  
- protocol analysis  
- filtering techniques  
- understanding how normal web traffic appears inside Wireshark  

This included DNS lookups, TCP handshake details, and HTTP requests.

## Additional Notes
- ICMP packets were identified as Echo Request traffic.  
- DNS traffic showed a query for *opensource.google.com* which resolved to **142.250.1.139**.  
- TCP packets included port 80 HTTP traffic with a TTL of 64, a frame length of 60 bytes, and a header length of 20 bytes.  
- Useful filters applied included:  
  - `ip.addr`  
  - `udp.port == 53`  
  - `tcp contains "curl"`  
- Gained experience navigating protocol subtrees including Frame, Ethernet II, IPv4, TCP, and DNS layers to understand how network traffic is structured.  
