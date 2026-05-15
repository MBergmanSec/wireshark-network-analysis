Suspicious DNS \& HTTP Investigation



Project Overview

This investigation focused on analyzing suspicious DNS and HTTP traffic within a controlled Ubuntu virtual machine environment using Wireshark. The lab simulated automated HTTP communication, suspicious User-Agent strings, repeated beacon-style traffic, and DNS-to-HTTP correlation analysis to demonstrate foundational network investigation techniques.



Objectives

\- Analyze HTTP GET requests and responses

\- Identify suspicious User-Agent strings

\- Investigate repeated beacon-style communication

\- Correlate DNS resolution activity with HTTP traffic

\- Inspect packet-level metadata and TCP behavior

\- Practice traffic investigation workflows using Wireshark



Lab Environment

\- Host System: Windows 11

\- Virtualization: VMware Workstation

\- Guest OS: Ubuntu 64-bit

\- Analysis Tool: Wireshark

\- Network Interface: ens33



Tools Used

\- Wireshark

\- Ubuntu Terminal

\- curl

\- VMware Shared Folders



Analysis Performed

\- Captured HTTP traffic generated through curl commands

\- Inspected HTTP GET requests and HTTP 200 OK responses

\- Identified suspicious User-Agent values including:

&#x20; - Mozilla/5.0 EvilBot

&#x20; - BeaconClient/1.2

\- Analyzed repeated HTTP requests indicative of beaconing behavior

\- Investigated DNS AAAA queries and DNS response traffic

\- Correlated DNS resolution activity with subsequent HTTP communication

\- Reviewed TCP session metadata including PSH and ACK flags



Key Findings

\- Suspicious HTTP User-Agent strings were successfully identified within unencrypted HTTP traffic

\- Repeated HTTP communication patterns demonstrated simulated beaconing behavior

\- DNS requests for example.com directly correlated with later HTTP communication to resolved infrastructure IP addresses

\- Packet analysis confirmed successful TCP sessions containing transferred application-layer data

\- AAAA DNS queries demonstrated IPv6 resolution activity prior to HTTP communication



Skills Demonstrated

\- Packet analysis

\- HTTP protocol inspection

\- DNS traffic analysis

\- Traffic correlation

\- Behavioral analysis

\- User-Agent investigation

\- Beaconing detection fundamentals

\- TCP session interpretation

\- Wireshark filtering and navigation





Screenshot Descriptions



suspicious-user-agent-http.png

Inspection of suspicious HTTP traffic containing the modified User-Agent string "Mozilla/5.0 EvilBot". Packet analysis identified unencrypted HTTP communication over TCP port 80, including GET requests and application-layer metadata.



beaconclient-packet-analysis.png

Detailed inspection of repeated HTTP communication generated using the User-Agent "BeaconClient/1.2". Analysis included TCP session details, PSH/ACK flags, and successful application-layer data transfer.



repeated-beacon-requests.png

Observed repeated HTTP GET requests communicating with the same external infrastructure at recurring intervals, demonstrating simulated beaconing behavior commonly associated with automated communication patterns.



dns-http-correlation.png

Correlated DNS resolution activity with subsequent HTTP communication. Analysis identified AAAA DNS queries for example.com followed by communication with resolved infrastructure IP addresses.



Next Steps

\- Continue developing traffic correlation skills

\- Expand into HTTPS/TLS traffic analysis

\- Investigate JA3 and TLS fingerprinting concepts

\- Begin analyzing malicious PCAP samples from Malware-Traffic-Analysis.net

\- Practice identifying anomalous traffic patterns within larger packet captures

