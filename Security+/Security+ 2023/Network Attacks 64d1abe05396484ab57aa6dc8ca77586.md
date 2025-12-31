# Network Attacks

### Introduction

- Some of the Network Attacks :
1. Denial of Service
2. Spoofing
3. Hijacking
4. Replay
5. Transitive Attacks
6. DNS Attacks
7. ARP Poisoning

### Ports and Protocols

- **Port :** A Logical communication endpoint that exists on a computer or server.
    - **Inbound Port** : A logical Communication opening on a server that is listening for a connection from a client.
    - **Outbound Port** : A logical communication opening created on a client in order to call out to a server that is listening for a connection.
- Ports can be between 0 to 65535.
    - **Well Known Ports :** Ports 0 to 1023 are considered well-known and are assigned by the Internet Assigned Numbers Authority(IANA).
    - **Registered Ports** : Ports 1024 to 49151 are considered registered and are usually assigned to proprietary protocols.
    - **Dynamic Ports** : Ports 49152 to 65535 can be used by an application without being registered with IANA.
    
    ## Ports
    
    1. **FTP** - Port **21** - used to transfer files from host to host.
    2. **SSH, SCP & SFTP** - Port **22** - used to remotely administer network devices and systems. SCP is used for secure copy and SFTP for secure FTP.
    3. **Telnet** - Port **23** - Unencrypted method to remotely administer network devices.
    4. **SMTP** - Port **25** - used to send email over the internet.
    5. **DNS** - Port **52** - is used to resolve hostnames to IPs and IPs to hostnames.
    6. **TFTP** - Port **69** - Trivial FTP is used as a simplified version of FTP to put a file on a remote host, or get a file from a remote host.
    7. **HTTP** - Port **80** - used to transmit web page data to a client for unsecured web browsing.
    8. **Kerberos** - Port **88** - used for network authentication using a system of tickets within windows domain.
    9. **POP3** - Port **110** - used to receive email from a mail server.
    10. **NNTP** - Port **119** - used to transport Usenet articles.
    11. **RPC/DCOM-scm** - Port **135** - Remote Procedure Call is used to locate DCOM ports to request a service from a program on another computer on the network
    12. **NetBIOS** - Port **137-139** - used to conduct name querying, sending of data, and other function over a NetBIOS connection. 
    13. **IMAP** - Port **143** - used to receive email from a mail server with more features than POP3.
    14. **SNMP** - Port **161** - used to remotely monitor network devices.
    15. **SNMPTRAP** - Port **162** - used to send TRAP and InformRequests to the SNMP Manager on a network.
    16. **LDAP** - Port **389** - used to maintain directories of users and other objects.
    17. **HTTPS** - Port **443** - used to transmit web page data to a client over an SSL/TLS encrypted Connection.
    18. **SMB** - Port **445** - used to provide shared access to files and other resources on a network.
    19. **SMTP with SSL/TLS** - Port **465/587** - SMTP with an SSL and TLS secured connection.
    20. **Syslog** - Port **514** - used to conduct computer message logging, especially for routers and firewall logs.
    21. **LDAP SSL/TLS** - Port **636** - LDAP over an encrypted SSL/TLS connection.
    22. **iSCSI** - Port **860** - used for linking data storage facilities over IP.
    23. **FTPS** - Port **989/990** - FTP over an encrypted connection.
    24. **IMAP4 with SSL/TLS** - Port **993** - IMAP over an SSL/TLS encrypted connection.
    25. **POP3(TLS/SSL)** - Port **995** - POP3 using an encrypted connection.
    26. **Ms-sql-s** - Port **1433** - used to receive SQL database queries from clients.
    27. **RADIUS(alternative)** - Port **1645/1646** - used for authentication and authorization and accounting.
    28. **L2TP** - Port **1701** - Layer 2 Tunnel Protocol is used as an underlying VPN protocol but has no inherent security.
    29. **PPTP** - Port **1723 -** Point to Point Tunneling Protocol is an underlying VPN protocol with built-in security.
    30. **RADIUS** - Port **1812/1813** - used for authentication and authorization and accounting.
    31. **FCIP** - Port **3225** - used to encapsulate Fibre Channel frames within TCP/IP packets.
    32. **iSCSI Target** - Port **3260** - is a listening Port for a iSCSI targeted devices when linking data storage facilities over IP.
    33. **RDP** - Port **3389** - used to remotely view and control other windows systems via a GUI.
    34. **Diameter** - Port **3868** - more advanced AAA protocol that is a replacement for RADIUS.
    35. **Syslog over TLS** - Port **6514** - Syslog over a TLS encrypted connection.
    

### Denial of Service (DOS)

- Term used to describe many different types of attacks which attempt to make a computer or server’s resources unavailable.
    - **Flood Attacks** : attempts to send more packets to a single server or host than they can handle.
    - **Ping of Death :** An attack that sends an oversized and malformed packet to another computer or server.
    - **Teardrop Attack :** Attack that breaks apart packets into IP Fragments , modifies them with overlapping and oversized payloads and sends them to a victim machine.
    - **Permanent DoS :** Attack which exploits a security flaw to a permanently break a networking device by reflashing its firmware.
    - **Fork Bomb :** Attack that creates a large number of processes to use up the available processing power of a computer.
- **DDOS :** A group of compromised systems attack a single target simultaneously to create a Denial of Service.
- **DNS Amplification** : Attack which relies on the large amount of DNS information that is sent on response to a spoofed query on behalf of the victimized server.
- **Stopping A DDoS Attack**
    - **Blackholing or Sinkholing** : Identifies any attacking IP addresses and routes all their to a non-existent server through the null interface.
    - An IPS can prevent small scale DDoS attack.
    - Specialized security services cloud providers can stop DDoS attacks
        - Cloudflare
        - Akamai

### Spoofing

- Occurs when an attacker masquerades as another person by falsifying their identity.
- Anything that uniquely identifies a user or system can be spoofed.
- Proper Authentication is used to detect and prevent spoofing.

### Hijacking

- Exploitation of a computer session in an attempt to gain unauthorized access to data, services or other resources on a computer or server.
- There are 8 types of hijacking sessions that can be performed
    - **Session Theft :** Attacker guesses the session ID for a web session, enabling them to takeover the already authorized session of the client.
    - **TCP/IP hijacking :** Occurs when an attacker takes over a TCP session between two computers without the need of cookie or other host access.
    - **Blind hijacking :** Occurs when an attacker blindly injects data into the communication stream without being able to see if its successful or not.
    - **Clickjacking :** Attack that uses multiple transparent layers to trick a user into clicking on a button or link on a page when they were intending to click on the actual page.
    - **Man-in-the-Middle :** Attack that causes data to flow through the attackers computer where they can intercept or manipulate the data.
    - **Man-in-the-browser :** Occurs when an trojan infects a vulnerable web browser and modifies the web pages or transactions being done within the browser.
    - **Watering hole :** Occurs when malware is placed on a website that the attacker knows his potential victim would access.
    - **Cross-site Scripting**

### Replay Attack

- Network-based attack where a valid data transmission is fraudulently or maliciously rebroadcast, repeated or delayed.
- Multi-factor authentication can help prevent successful replay attacks.

### Transitive Attacks

- **Transitive Attacks** aren’t really an attack but more of a conceptual method.
- When an security is sacrificed in favor of more efficient operations, additional risks exists.
- $Transitive= A=B=C$

### DNS Attacks

- **DNS Poisoning :** Occurs when the name resolution information is modified in the DNS server’s cache.
    - If the cache is poisoned, then the user can be redirected to a malicious website.
- **Unauthorized Zone Transfers :** Occurs when an attacker requests replication of the DNS information to their systems for use in planning future attacks.
- **Altered Host files :** Occurs when an attacker modifies the host file to have the client bypass the DNS server and redirects them to an incorrect or malicious website.
- **Domain Name Kiting :** Attacks that exploits a process on the way a domain name is registered so that the domain name is kept in limbo and cannot be registered by an authenticated buyer.

### ARP Poisoning

- **ARP** : **A**ddress **R**esolution **P**rotocol
- Protocol for converting a IP address to MAC address.
- **ARP Poisoning** : Attack that exploits the IP address to MAC resolution in a network to steal, modify or redirect frames within the local area network.

[Only thing to remember for exam : RMF is made by NIST and its used in federal government systems.](Network%20Attacks/Only%20thing%20to%20remember%20for%20exam%20RMF%20is%20made%20by%20NIS%20b418aab0ad814396bf6f7e3553bbb6bb.md)