# Entry 5 | Suricata Custom Rule Detection and Alert Analysis

## Date
7/20/2025

## Description
Configured and ran Suricata with a custom detection rule to trigger alerts from a sample packet capture. Reviewed both fast.log and eve.json outputs to confirm that the rule worked and to extract useful network telemetry from the alerts.

## Tools Used
- Suricata  
- sample.pcap  
- custom.rules  
- fast.log  
- eve.json  
- jq (JSON parsing tool)  

## The 5 W's

### Who caused the incident?
There was no real threat actor. This was a simulated lab designed to test IDS detection behavior for HTTP GET traffic.

### What happened?
A custom Suricata rule was written to detect outbound HTTP GET requests from the home network to external IPs. The rule was applied to a packet capture file, prompting Suricata to generate alerts. These alerts were reviewed to analyze the captured traffic and confirm that the rule triggered as expected.

### When did the incident occur?
During a lab session on 7/20/2025 while processing the sample.pcap file.

### Where did the incident happen?
Inside a Linux based virtual lab environment using Suricata from the terminal.

### Why did the incident happen?
The purpose of the rule was to match HTTP GET traffic. This type of rule mirrors how analysts detect suspicious outbound traffic such as scanning, beaconing, data exfiltration, or other abnormal web activity.

## Additional Notes
- Custom rule used:  
  `alert http $HOME_NET any -> $EXTERNAL_NET any (msg:"GET on wire"; flow:established,to_server; content:"GET"; http_method; sid:12345; rev:3;)`  
- fast.log confirmed alerts showing HTTP GET traffic from `172.21.224.2` to `142.250.1.139` on port 80.  
- jq was used to parse eve.json fields including:
  - timestamp  
  - flow_id  
  - alert.signature  
  - proto  
  - dest_ip  
- Verified alert signature was "GET on wire".  
- Verified the last event destination IP was `142.250.1.102`.  
- Verified alert severity was `3`.  
- Successfully correlated multiple alerts using the same flow_id to follow a single communication flow.  
