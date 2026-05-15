\# User-Agent Investigation



\## Project Overview



This lab focused on analyzing HTTP User-Agent behavior and identifying differences between legitimate browser traffic, command-line HTTP clients, and suspicious automated communication patterns. Traffic was generated within an Ubuntu virtual machine and analyzed using Wireshark to simulate basic threat-hunting and behavioral investigation workflows.



\---



\## Objectives



\- Analyze HTTP GET requests and HTTP metadata

\- Compare browser-generated and command-line-generated traffic

\- Investigate User-Agent behavior within HTTP traffic

\- Simulate suspicious automated communication

\- Observe repetitive beaconing-style traffic patterns

\- Practice packet analysis and evidence collection using Wireshark



\---



\## Lab Environment



\- Host System: Windows 11

\- Virtualization Platform: VMware Workstation

\- Guest OS: Ubuntu 64-bit

\- Analysis Tool: Wireshark

\- Browser: Firefox

\- Network Interface: ens33



\---



\## Tools Used



\- Wireshark

\- Ubuntu Terminal

\- Firefox

\- curl

\- VMware Workstation



\---



\## Analysis Performed



\- Captured standard Firefox HTTP traffic

\- Inspected HTTP GET requests and User-Agent metadata

\- Generated HTTP traffic using curl

\- Compared browser traffic against command-line HTTP traffic

\- Created custom suspicious User-Agent strings

\- Simulated repeated HTTP beaconing behavior using bash loop automation

\- Investigated repetitive communication patterns and timing intervals

\- Collected packet captures and supporting evidence screenshots



\---



\## Key Findings



\### Browser Traffic Characteristics



Firefox-generated traffic contained:



\- detailed User-Agent metadata

\- multiple HTTP headers

\- browser-specific communication patterns



Observed traffic appeared consistent with normal human browsing behavior.



\### curl Traffic Characteristics



curl-generated traffic contained:



\- simplified HTTP requests

\- fewer HTTP headers

\- command-line User-Agent values



Traffic appeared more automated and machine-generated compared to browser activity.



\### Suspicious User-Agent Simulation



Custom User-Agent values including:



\- EvilBot-C2-Beacon



were injected into HTTP requests using curl to simulate suspicious or malware-like metadata often investigated during SOC and threat-hunting operations.



\### Beaconing Behavior



Repeated HTTP requests were generated using automated curl loop execution.



Observed characteristics included:



\- repetitive HTTP GET requests

\- identical destinations

\- repeated User-Agent values

\- predictable timing intervals

\- consistent communication patterns



These behaviors resembled low-level beaconing activity commonly associated with automated communication or command-and-control style traffic.



\---



\## Skills Demonstrated



\- HTTP traffic analysis

\- User-Agent investigation

\- Packet filtering and inspection

\- Behavioral traffic analysis

\- Beaconing detection fundamentals

\- DNS and TCP analysis

\- Linux command-line tooling

\- Wireshark investigation workflows

\- Evidence collection and documentation



\---



\## Evidence Collected



\### Screenshots



\#### normal-firefox-user-agent.png



Captured legitimate Firefox-generated HTTP traffic demonstrating standard browser metadata, detailed User-Agent values, and normal browser communication behavior.



\#### curl-user-agent.png



Inspected HTTP traffic generated using curl from the Linux command line. Traffic contained simplified HTTP requests and reduced metadata compared to browser-generated communication.



\#### suspicious-user-agent.png



Analyzed HTTP traffic containing the custom User-Agent string "EvilBot-C2-Beacon" generated using curl to simulate suspicious or malware-like metadata.



\#### repeated-http-beaconing-pattern.png



Observed repeated HTTP GET requests generated at predictable timing intervals using automated curl execution, demonstrating simulated beaconing-style communication behavior.



\---



\## Packet Captures



\- user-agent-investigation.pcapng

\- beaconing-simulation.pcapng



\---



\## Key Takeaways



\- Different tools generate unique network fingerprints

\- Automated traffic often appears repetitive and predictable

\- User-Agent metadata provides valuable investigative context

\- Human browsing behavior differs significantly from scripted traffic

\- Behavioral analysis is critical for identifying suspicious communication patterns

\- Traffic correlation improves investigative visibility during packet analysis

