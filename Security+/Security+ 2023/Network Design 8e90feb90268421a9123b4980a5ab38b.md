# Network Design

### The OSI Model

- Used to explain network communications between a host and remote device over LAN or WAN.
    - **Physical Layer** : Represents the actual network cables and radio waves used to carry data over a network.
        - Data in form of **bits**.
    - **Data Link Layer** : Describes how a connection is established, maintained and transferred over the physical layer and uses physical addressing (MAC addresses).
        - Data in form of frames.
    - **Network Layer** : Uses logical address to route or switch information between hosts, the network and the internetworks.
        - Data in form of Packets.
    - **Transport Later** : Manages and ensures transmission of the packets occurs from a host to a destination using TCP or UDP.
        - Data in form of Segments(TCP) or Datagrams(UDP).
    - **Session Layer** : Manages the establishment, termination and synchronization of a session over the network.
    - **Presentation Layer** : Translates the information into a format that the sender and receiver both understand.
    - **Application Layer** : Layer from which the message is created, formed and originated.
        - Consists of high level protocols like **HTTP, SMTP** and **FTP.**

### Switches

- **Switches** are the combination evolution of hubs and bridges.
- **Switches** are subjected to three main types of attacks
    - **MAC Flooding :** Attempt to overwhelm the limited switch memory set aside to store the MAC addresses for each port.
        - Switches can fail-open when flooded and begin to act like a hub.
    - **MAC Spoofing :** Occurs when an attacker masks their own MAC address to pretend they have the MAC address of another device.
        - MAC Spoofing is often combined with an ARP spoofing attack.
    - **Physical Tampering :** Occurs when an attacker attempts to gain physical access.

### Routers

- Routers operate at Layer 3
- Used to connect two or more networks together to form a internetworks.
- Routers rely on a packet’s IP Addresses to determine the proper destination.
- **ACL (Access Control Lists)** : An ordered set of rules that a router uses to decide whether to permit or deny traffic based upon given characteristics.
- IP Spoofing is used to trick a router’s ACL.

### Network Zones

- Most network are separated into 3 different zones
    - **LAN**
    - **WAN**
    - **DMZ** **(De-Militarized Zone)** : Focused on providing controlled access to publicly available servers that are hosted within your organizational network.
- Any Confidential traffic should be processed to through a VPN.
- Sub zones can be created to provide additional protection for some servers.
- **Extranets** : Specialized type of DMZ that is created for your partner organization to access over a wide area of network.
- Intranets are used when only one company is involved.

### Jumpbox

- **Internet-Facing host** : Any host that accepts inbound connections from the internet.
- Everything behind the DMZ is invisible to the outside network.
- **Bastion Hosts** : Hosts or servers in the DMZ which are not configured with any services that run on the local network.
- To configure devices in the DMZ, a jumpbox is utilized.
- **Jumpbox** : A hardened server that provides access to other hosts within the DMZ.
- An administrator connects to the jumpbox and the jumpbox connects to hosts in the DMZ.
- The jumpbox and management workstation should only have the minimun required software to perform their job and be well hardened.

### Network Access Control

- Security technique in which devices are scanned to determine its current state prior to being allowed access onto a given network.
- if a device fails the inspection, it is placed into digital quarantine.