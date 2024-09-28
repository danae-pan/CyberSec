## Reconnaissance

The first phase of the threat lifecycle, where attackers search for vulnerabilities that they can exploit to attack targets. It consists of techniques that involve adversaries actively or passively gathering information to support their targeting efforts. Reconnaissance can be classified into active and passive types, which describe how the reconnaissance is being performed—either quietly (passive) or interactively (active).


### Passive Reconnaissance

This involves collecting information without directly interacting with the target. In passive reconnaissance, attackers rely on publicly available knowledge to gather data while minimizing the risk of detection. 

***Techniques & Tools***

- **Packet Sniffing**: Captures data packets to analyze network traffic (e.g., Wireshark).
- **Search Engine Dorking**: Uses specific search operators to uncover sensitive information indexed by search engines (e.g., Google Hacking Database).
- **Public Data Aggregation**: Collects information from publicly accessible databases like WHOIS, web registries, and financial records (e.g., Robtex).
- **Social Media Analysis**: Examines social media platforms to gather personal or organizational data (e.g., Maltego).
- **Archival Research**: Uses historical web content to find information that has been removed or modified (e.g., Wayback Machine).
- **Email Harvesting**: Collects email addresses from a target organization, often for use in spear phishing or other social engineering attacks (e.g., theHarvester).

### Active Reconnaissance

This involves an intrusive approach, actively interacting with the target to gather information by directly engaging with it. Active reconnaissance carries a higher risk of detection since it requires direct contact with the target systems.

***Techniques & Tools***

- **Social Engineering**: Involves manipulating individuals into revealing confidential information (e.g., Social Engineer Toolkit).
- **Port Scanning**: Identifies open ports and services running on websites or web applications (e.g., Nmap).
- **Network Mapping**: Reveals the target's network topology, connected devices, and communication protocols (e.g., Zenmap).
- **DNS Enumeration**:  Finds all DNS servers and associated records for a domain (e.g., DNSrecon).
- **OS Fingerprinting**: Identifies the operating system running on the target device (e.g., Xprobe2).
- **Vulnerability Scanning**: Detects vulnerabilities in a system to address them before attackers can exploit them (e.g., Nessus, OpenVAS).

