# Perimeter Security

- Security devices focused on the boundary between the LAN and the WAN in your organization’s network.
- Perimeter security relies on several different devices.

### Firewalls

- Three types of firewalls
    - **Software** : run as a piece of software that run on a host or a server
    - **Hardware** : installed on a network
    - **Embedded firewalls** : work as a single function out of many on devices.
- **Packet Filtering** : Inspects each packet passing through the firewall accepts or rejects it based on the rules.
- **NAT Filtering** : Filters traffic based upon the ports being utilized and type of connection(UDP or TCP).
- **Circuit-Level Gateway** : Operates at the session layer and only inspects the traffic during the establishment of the initial session over TCP or UDP.
- **Explicit Allow** : Traffic is allowed to enter or leave the network because there is an ACL rule that specially allows it.
- **Implicit Deny** : Traffic is denied the ability to enter or leave the network because there is no specific rule that allows it.
- **Web Application Firewalls** : Firewall installed to protect your server by inspecting traffic being sent to a web application.
    - A WAF can prevent a XSS or SQL injection.

### Proxy Server

- A device that acts as a middle man between a device and a remote server.
- 4 Types of Proxies
    - **IP Proxy :** is used to secure a network by keeping its machines anonymous during web browser.
    - **Caching Proxy :** Attempts to serve client requests by delivering content from itself without actually contacting the remote server.
    - **Content Filter :** Used in organizations to prevent users from accessing  prohibited websites and other contents
    - **Web Security Gateway :** A go-between device that scans for viruses, filters unwanted content and performs data loss prevention functions.

### Honeypots and Honeynets

- Honeypots and Honeynets are used to attract and trap potential attackers.
- **Honeypot** : A single computer (or file, group of files, or IP range) that might be attractive to an attacker.
- **Honeynet** : A group of computers, servers, or networks used to attract an attacker.
- Honeypots are normally used in security research.

### Data Loss Prevention

- Systems designed to protect data by conducting content inspection of data being sent out of the network.
- DLP is used to ensure your private data remains secure.

### NIDS & NIPS

- **Network Intrusion Detection System** : Attempts to detect, log and alert on malicious network activities.
- NIDS use promiscuous mode to see all network traffic on a segment.
- **Network Intrusion Prevention System** : Attempts to remove, detain or redirect malicious traffic.
- NIPS should be installed in-line of the network traffic flow.

### Unified Threat Management

- Combination of network security devices and technologies to provide more defense in depth within a single device.