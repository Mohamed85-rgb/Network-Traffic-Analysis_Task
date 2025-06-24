# Network-Traffic-Analysis_Task
🧾 Network Traffic Analysis Summary
Objective: Capture, filter, and analyze network traffic to identify normal vs suspicious behavior.

📷 Captured Screenshots
HTTP Browsing Activity

GET/POST requests to public sites with 200/301 responses

Screenshot 1: Normal HTTP packet breakdown (Wireshark filter: http)

DNS Query Analysis

Domain resolution for neverssl.com and others

Screenshot 2 & 3: DNS request/response with protocol breakdown (filter: dns)

Nmap SYN Scan Activity

Half-open connection attempts (Nmap style)

Screenshot 4: tcp.flags.syn == 1 && tcp.flags.ack == 0 revealing SYN flood pattern

Suspicious SSH Activity

Multiple SYN packets and sudden connection to port 22

Screenshot 5: Highlighted packets showing potential probe and session attempt

🧠 Observations
Normal traffic included DNS lookups and web browsing sessions.

Anomalous activity was observed in the form of:

Repeated SYN packets (indicative of port scans)

Sudden SSH connections (potential brute-force or enumeration attempts)

🛡️ Mitigations
Limit SSH access to known IPs and disable unused ports

Use firewalls to detect and throttle scan behavior

Monitor DNS and SYN packet surges for reconnaissance detection
