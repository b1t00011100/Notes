# Security Protocols

### S/MIME

- **Secure/Multipurpose Internet Mail Extension (S/MIME) :** A standard that provides cryptographic security for electronic messaging.
    - Basically, Encryption for email.
- It provides
    - **Authentication**
    - **Integrity**
    - **Non-repudiation**
- S/MIME can encrypt emails and their contents *… including malware*.

### SSL & TLS

- SSL and TLS are the backbone of web security.
- **Secure Socket Layer (SSL) and Transport Layer Security (TLS) :** Cryptographic protocols that provide secure Internet communication for web browsing, instant messaging, email, VoIP and many other services.
- SSL was last updated in 1996 with SSLv3, its really old.
- Instead now everyone uses TLS.
- TLSv1.3 is the latest version of TLS.
- **Downgrade Attack :** A protocol is tricked into using a lower quality version of a higher quality version.

### SSH

- **Secure Shell (SSH) :** A protocol that can create a secure channel between two computers or network devices to enable one device to control the other device.
- SSH requires a server (daemon) to be run on one device and a client on the other.
- SSH - Port 22
- SSH 2.0 uses Diffie-Hellman key exchange and MACs(Message Authentication Codes).

### VPN Protocols

- **Virtual Private Networks** : A secure connection between two or more computers or device that are not on the same private network.
- VPN Protocols :
    - **Point-to-Point Tunneling Protocol (PPTP)** : A protocol that encapsulates PPP packets and ultimately sends data as encrypted traffic.
        - PPTP : Port 123
        - PPTP can use CHAP-based authentication, making it vulnerable to attacks.
    - **Layer 2 Tunneling Protocol (L2TP)** : A connection between two or more computers or device that are not on the same private network
        - L2TP is usually paired with IPSec to provide security.
        - L2TP : Port 1701
    - **IPSec** : A TCP/IP protocol that authenticates and encrypts IP packets and effectively securing communications between computers and devices using this protocol.
        - IPSec provides confidentiality(encryption), integrity(hashing) and authentication (Key exchange).
        - **Internet Key Exchange (IKE)** : Method used by IPSec to create a secure tunnel by encrypting the connection between authenticated peers.
        - **Security Association :** Establishment of secure connections and shared security information using certificates or cryptographic keys.
        - **Authentication Header :** Protocol used in IPSec that provides integrity and authentication.
        - **Encapsulating Security Payload (ESP) :** Provides integrity, confidentiality and authenticity of packets by encapsulating and encrypting them.
    - IPSec can be operated in 2 modes
        - **Transport Mode :** Host-to-Host transport mode Only uses encryption of the payload of an IP packet but not its header.
            - Transport mode is used for transmission between hosts on a private network.
        - **Tunnel Mode :** A network tunnel is created which encrypts the entire IP packet (payload and header).
            - Tunnel mode is used for transmission between networks.