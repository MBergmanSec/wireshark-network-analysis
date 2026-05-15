\# Wireshark Network Analysis Lab — Session Notes V3



\## Objective



Simulate repetitive automated HTTP communication and investigate beaconing-style traffic patterns using Wireshark.



\---



\## Activities Performed



\* Captured HTTP traffic generated through automated curl requests

\* Used bash loop automation to create repeated outbound HTTP requests

\* Inspected HTTP GET requests and HTTP 200 OK responses

\* Analyzed request timing intervals and repeated communication behavior

\* Investigated automated traffic patterns using Wireshark filters

\* Saved packet captures and evidence screenshots



\---



\## Tools Used



\* Wireshark

\* Ubuntu Linux VM

\* curl

\* Bash scripting

\* VMware



\---



\## Beaconing Simulation Overview



Automated HTTP traffic was generated using repeated curl requests with controlled timing intervals.



Command used:



for i in {1..10}; do curl http://example.com; sleep 5; done



This generated:



\* repeated HTTP GET requests

\* repeated HTTP 200 OK responses

\* predictable communication intervals

\* repeated User-Agent values

\* consistent destination traffic



\---



\## Findings



Observed traffic demonstrated characteristics commonly associated with automated communications and low-level beaconing behavior.



Key observations:



\* communication occurred at regular intervals

\* identical HTTP requests were repeatedly generated

\* same destination IPs were repeatedly contacted

\* User-Agent values remained unchanged across requests

\* traffic appeared predictable and machine-generated



Timing analysis showed repeated requests occurring approximately every five seconds.



\---



\## Analyst Observations



Human browsing behavior is generally inconsistent and irregular. Automated traffic often appears repetitive and predictable.



Repeated traffic patterns combined with identical metadata may indicate:



\* scripts

\* scheduled tasks

\* automated monitoring

\* malware beaconing

\* command-and-control check-ins



This exercise demonstrated how timing analysis and behavioral traffic inspection can help identify suspicious automation.



\---



\## Skills Demonstrated



\* HTTP traffic analysis

\* Behavioral traffic analysis

\* Wireshark filtering

\* Timing interval inspection

\* Automated traffic identification

\* Linux command-line usage

\* Bash loop automation

\* Evidence collection and documentation



\---



\## Evidence Collected



\### Screenshot



\## repeated-http-beaconing-pattern.png



Simulated automated HTTP communication using repeated curl requests to generate predictable outbound traffic patterns. Observed repeated HTTP GET requests, identical User-Agent values, and consistent timing intervals between requests. This exercise demonstrated how repetitive communication behavior may resemble low-level beaconing activity commonly investigated during SOC analysis and threat hunting operations.



\---



\## Key Takeaways



\* Automated traffic often follows predictable timing patterns

\* Repeated destinations and identical requests may indicate beaconing activity

\* Behavioral analysis is critical during threat hunting and SOC investigations

\* User-Agent inspection combined with timing analysis provides valuable investigative context

\* Wireshark can be used to identify repetitive communication behavior and automation patterns



