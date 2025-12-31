# Security Applications and Devices

### Firewalls

- **Personal Firewalls (Host Based Firewalls):** Software applications that protects a single computer from unwanted internet traffic.
- **Operating system Firewalls :**
    - Windows - Windows Firewall
    - Mac OSX - PF (Packet Filtering) and IPFW (Internet Protocol Firewall)
    - Linux - Iptables

<aside>
💡 **Firewall Application**

Windows firewall command : *wf.msc*

Mac OSX : OSX 10.0 and Higher - PF | Older Versions - IPFW

Linux command : iptables  

</aside>

- Many Anti-Malware suites also contain software firewalls.

### **Intrusion Detection System (IDS)**

- HIDS(Host Based IDS) : Logging everything Suspicious (Log files, Audit files).
    
    ![Screenshot 2023-06-13 at 14-13-13 CompTIA Security Complete Training Course & Practice Exam.png](Security%20Applications%20and%20Devices/Screenshot_2023-06-13_at_14-13-13_CompTIA_Security_Complete_Training_Course__Practice_Exam.png)
    

- NIDS(Network Based IDS) : Monitoring Suspicious Network Traffic.
    
    ![Host-Intrusion-Detection-System-HIDS.webp](Security%20Applications%20and%20Devices/Host-Intrusion-Detection-System-HIDS.webp)
    
- Methods for system to alert on
    - Signature Based : A specific String of bytes that will trigger the alarm.
    - Anomaly Based : Analyzes the current traffic against an established baseline and triggers an alert if outside the statistical average.
    - Policy Based : Relies on specific declaration of the security policy.
- Types of Alerts
    - **True Positive :** Malicious activity is identified as an attack.
    - **True Negative :** Legitimate activity is identified as legitimate traffic.
    - **False Positive :** Legitimate activity is identified as an attack.
    - **False Negative :** Malicious activity is identified as legitimate traffic.
- IDS can only alert and log suspicious activity
- IPS (Intrusion Prevention system) : stops malicious activity from being executed.

### Pop up Blocking

- Most web-browsers have the ability to block Javascript created pop-ups
- Pop ups maybe need to enabled for certain function on a website
- Malicious attackers could purchase ads through various networks
- **Content Filters :** Blocking of external files containing JavaScript , images, or web pages from loading in a browser
- Ensure your browser and its extensions are updated regularly.

### Data Loss Prevention(DLP)

- Definition : Monitors the data of a system while in use , in transit , or at rest to detect attempts to steal the data.
- Data Loss Prevention systems :
    - Hardware or Software solutions
- **Endpoint DLP system :** Software-based client that monitors the data in use on a computer and can stop a files transfer or alert an admin of the occurrence
    - Very much like an IPS or IDS but focused on **DATA.**
    - DLP’s can be set to detection mode or prevention mode.
- **Network DLP system :** Software or hardware based solutions that is installed on the perimeter of the network to detect data in transit
- **Storage DLP system :** Software installed on servers in the datacenter to inspect the data at rest
- **Cloud DLP system :** Cloud software as a service that protects data being stored in cloud services

### Securing the BIOS

- Definition : Bios is a type of firmware which is software on a chip.
- BIOS : **B**asic **I**nput **O**utput **S**ystem - Firmware that provides the computer instructions for how to accept input and send output.
- **UEFI (Unified Extensible Firmware Interface) :** more updated and robust version of BIOS
- Steps for securing BIOS
    1. Flash The Bios : ensuring it has the most updated software.
    2. Use a BIOS password : protect the bios from changing configurations
    3. Configure the BIOS boot order 
    4. Disable external ports and devices 
    5. Enable the secure Boot option

### Securing Storage Devices

- Removable media comes in different formats
    - Floppy Disk
    - CD/DVD
    - External Hard Drive
    - Thumb Drive / USB
- You should always encrypt files on removable media
- **Removable Media Control :** Technical limitations placed on a system in regards to the utilization of USB Storage devices and other removable media.
- Create administrative controls such as policies
- **Network Attached Storages (NAS)** : Storage Devices that connect directly to your organization’s network
    - NAS Systems often implement RAID arrays to ensure high availability
- **SAN (Storage Area Network)** : Network Designed specifically to perform block storage functions that may consist of NAS devices
- Securing Network Storages
    1. Use Data Encryption
    2. Use proper Authentication
    3. Log NAS access

### Disk Encryption

- **Encryption scrambles data into unreadable information**
- Two types of Encryption
    
    <aside>
    💡 **Encryption software is most commonly used.**
    
    </aside>
    
    - **Hardware Based Encryption** :
        - Self-Encrypting Drive (SED) - Storage Device that performs whole disk encryption by using embedded hardware.
    - **Software Based Encryption**
        - Mac : Filevault
        - Windows : Bitlocker
- When using Bitlocker, A Hardware key is used which resides on motherboard called TPM(Trusted Platform Module).
- If Motherboard doesn’t have a TPM , External USB Drive is used as a key.
- **Advanced Encryption Standard (AES) :** Symmetric key Encryption that supports 128-bit and 256-bit keys.
- Encryption adds security but has lower performance.

 

### Endpoint Analysis

- **Endpoint Analysis** is used when conducting when monitoring, logging and analysis of endpoints
- **Endpoint** is simply any device that is connected to the network
- Endpoint Protection Tools
    - Anti-Virus(AV) : Software Capable of detecting and removing virus infections and other types of malware.
    - HIDS/HIPS : A type of IDS or IPS that monitors a computer system for unexpected behavior or drastic changes to the systems state on an endpoint. Intrusion Detection/Protection.
    - Endpoint Protection Platforms(EPP) : A software agent and monitoring system that performs multiple security tasks such as anti-virus, HIDS/HIPS, firewall, DLP and file encryption. Signature Based.
    - Endpoint detection response platforms(EDR) : A software agent that collects system data and logs for analysis by a monitoring system to provide early detection of threats. Anamoly Based.
    - User Entity Behavioral Analytics(UEBA) : A system that can provide automated identification of suspicious activity by user accounts and computer hosts . Heavily dependent on AI or Machine Learning.