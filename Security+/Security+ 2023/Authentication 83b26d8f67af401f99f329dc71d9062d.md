# Authentication

### Authentication

- **Multi—factor Authentication :** Use of two or more authentication factors to prove user’s identity.
- 5 basic factors of Authentication
    1. **Knowledge** - Password, Pin, etc.
    2. **Ownership** - Something in Possession that uniquely identifies them.
    3. **Characteristics** - something that a person is like a fingerprint scanner, Biometrics.
    4. **Location** - Where a person is.
    5. **Action** - Something that a user does.
- Usernames and password are only considered **single-factor authentication**.
- **Time-based One-Time Password (TOTP)** : A password is computed from a shared secret and current time.
- **HMAC-based One Time Password (HOTP)** : A password is computed from a shared secret and is synchronized between the client and the server.

### Authentication Models

- Models of Authentication
    - **Context-aware Authentication :** Process to check the user’s or system’s attributes or characteristics prior to allowing to connect.
    - **Single Sign-On Authentication** : A default user profile for each user is created and linked with all of the resources needed.
        - Compromised SSO credentials will lead to serious security breach.
    - **Federated Identity Management (FIdM)** : A single identity is created for a user and shared with all of the organizations in a federation.
    - **Cross-Certification** : Utilizes a web of trust between organizations where each one certifies others in the federation.
    - **Trusted Third-Party** : Organizations are able to place their trust in a single third-party (also called the bridge model).
    - **Security Assertion Markup Language (SAML)** : Attestation model built upon XML used to share federated identity management information between systems.
    - **OpenID** : An open standard and decentralized protocol that is used to authenticate users in a federated identity management system.

### 802.1x

- Standardized framework used for port-based authentication on wired and wireless networks.
- It utilized other mechanisms to do the real authentication
    - RADIUS (Remote Authentication Dialing User Service) : Centralized administration system for dial-up, VPN and wireless authentication that uses either ports 1812/1813(UDP) or 1645/1646(UDP).
    - TACACS+ (Terminal Access Controller access control system plus) : Cisco’s proprietary version of RADIUS that provides separate authentication and authorization functions over port 49(TCP).
- There are 3 roles for an authentication to occur under 802.1x
    - **Supplicant** : which is the device or user that’s requesting access to the network.
    - **Authenticator** : which is the device through which supplicant is attempting to access the network.
    - **Authentication Server** : which is the centralized server that performs the authentication.
- 802.1x can prevent rogue devices.
- 802.1x also allows to encapsulate the extensible authentication protocol (EAP)
- **Extensible Authentication Protocol (EAP)** : A framework of protocols that allows for numerous methods of authentication including passwords, digital certificated, and public key infrastructure.

### LDAP and Kerberos

- **Lightweight Directory Access Protocol (LDAP)** : A database used to centralize information about clients and objects on the network.
    - **LDAP Unencrypted : Port 389**
    - **LDAP Encrypted : Port 636**
- Microsoft created their own version of this which is **Active Directory(AD)**.
- **Kerberos** : An authentication protocol used by windows to provide for two-way (mutual) authentication using a system of tickets.
    - Port 88
    - A Domain Controller can be single point of failure of Kerberos.

### Remote Desktop Services

- **Remote Desktop Protocol (RDP)** : Microsoft’s proprietary protocol that allows administrators and users to remotely connect to another computer via a GUI.
    - RDP doesn’t provide authentication natively.
- **Virtual Network Computing (VNC)** : Cross-platform version of the Remote Desktop Protocol for remote user GUI access.
    - VNC requires a client, server and protocol be configured.
    - VNC : Port 5900

### Remote Access Services

- **PAP** - Password Authentication Protocol : Used to provide authentication but is not considered secure since it transmits the login credentials unencrypted.
- **CHAP** - Challenge Handshake Authentication Protocol : Used to provide authentication by using the user’s password to encrypt a challenge string of random numbers.
    - Microsoft’s version of CHAP is MS-CHAP
- **EAP** - Extensible Authentication Protocol - A framework of protocols that allows for numerous methods of authentication including passwords, digital certificated, and public key infrastructure.

### VPN

- Allows end users to create a tunnel over an untrusted network and connect remotely and securely back to the enterprise network.
- **VPN Concentrators** : Specialized hardware device that allows for hundreds of simultaneous VPN connections for remote workers.
- **Split tunneling** : A remote worker’s machine diverts internal traffic over the VPN but external traffic over their own internet connection.
    - Prevent split tunneling through proper configurations and network segmentations.

### Authentication Attacks

- **Spoofing :** Software-based attack where the goal is to assume the identity of a user, process, address or other unique identifier.
- **Man-in-the-Middle :** An attack where the attacker sits between two communicating hosts and transparently captures, monitors and relays all communication between the hosts.
- **Password Spraying :** Brute force attack in which multiple user accounts are tested with a dictionary of common passwords.
- **Credential Stuffing :** Brute force attack in which stolen user accounts names and passwords are tested against multiple websites.
- **Broken Authentication :** A software vulnerability where the authentication mechanism allows an attacker to gain entry.