# Basics

- **Information Security** : Act of Protecting Data from Unauthorized Access.
- **Information System Security** : Act of Protecting the Systems that hold the Data.

## CIA Triad

- **Confidentiality** - Encryption.
- **Integrity** - Modification without proper authorization.
- **Availability** - Information able to be accessed when needed.
    
    ![384.png](Basics/384.png)
    

## AAA of Security

- **Authentication** : When a persons Identity is established with proof.
    - 5 methods of Authentication
        - Something you know : Username and Password
        - Something you are : Fingerprint or Retina scan
        - Something you have : Token or Drivers License
        - Something you do : Way someone speaks or Signature
        - Somewhere you are : Location Factor Based on GPS
- **Authorization** : When a person is given access to certain data or certain areas of Building
- **Accounting :** Tracking of Data , Computer Usage and Network Resources

<aside>
💡 Note -

**Non Repudiation** : Occurs when you know user has taken an action.

**Log File** : Large Text Document which keeps track of all sorts of things.

</aside>

- Security Threats
    - 4 Main Categories
        - **Malware** : Short hand for Malicious Software e . g - Viruses, Worms, Rootkits, Trojan Horses, Spyware, etc.
        - **Unauthorized access** : Occurs when an computer data is accessed without owner consent.
        - **System Failure** : Occurs when a system crashes or an individual application fails.
        - **Social Engineering :** Act of Manipulating Users into revealing confidential information or performing other detrimental actions.
        
        <aside>
        💡 Phishing : Form of Social Engineering using technical capacity.
        
        </aside>
        
        ### Mitigating Threats (Reducing Risk)
        
        - 3 Basic Categories for mitigating threats
            - **Technical Controls :** Encryption , Smart Cards , etc.
            - **Physical Controls :** Alarms systems , Surveillance Cameras , etc.
            - **Administrative Controls or Managerial Controls :** Protocols, Policies , etc.
                - Protocols :
                    - Procedural Protocols : Protocols which you carry out on your own.
                    - Legal or Regulatory Protocols : legal or protocols that you are obliged to do because of LAW.
        
        ### Hackers
        
        - Types of **Hackers :**
            - **White Hats / Ethical Hacker or Penetration Tester :** Non Malicious Hackers who attempt to break into a Company’s system at their request.
            - **Black Hats :** Malicious Hackers who break into computer systems or networks with unauthorized access.
            - **Grey Hats :** Hackers without any affiliation to a company that attempts to break into a company’s network and risk breaking the law.
            - **Blue Hats :** Freelance Penetration Tester / Ethical Hacker.
            - **Elite :** Hackers who find vulnerabilities and exploit them before anyone else does.
            
            <aside>
            💡 Note -
            
            - Grey Hat Hackers do not have to malicious intent for breaking in they just do it for the challenge unlike Black Hats
            </aside>
            
            - **Script Kiddies :** Have limited Skill and run other people’s exploits and tools.
        
        ### Threat Actors
        
        - **Script Kiddies :** Have limited Skill and run other people’s exploits and tools. They are also called Baby Hackers.
        - **Hacktivists :** Hackers who are driven by cause such as Social change , Political agendas and Terrorism. Till now, the well-known Hacktivist group is Anonymous.
        - **Organized Crime :**  Hackers who are a part of crime group that is well funded and highly sophisticated. ****
        - **Advanced Persistent Threats (APT) :** Highly trained and funded group of hackers (Often by Nation states) with covert and open source intelligence at their disposal.
        
        ### Threat Intelligence and Sources
        
        - Timeliness
        - Relevancy
        - Accuracy
        - Confidence Levels
        
        <aside>
        💡 Information sources : US CERT, UK’s NCSC, AT & T SECURITY (OTX) , MISP, Virus Total, Spamhaus, SANS ISC Suspicious Domain.
        
        </aside>
        
        - **Open Source Intelligence (OSINT) -** Methods of obtaining information about a person or organization through public records, websites and Social Media.
        
        ### Threat Hunting
        
        - It is a Cybersecurity technique designed to detect presence of threats that have not been discovered by security Monitoring.
        - Steps :
        1. **Establishing a Hypothesis** : Deriving a Hypothesis by recognizing potential threats.
        2. **Profiling Threat actors and Activities :** Relying on Hypothesis , and Thinking about intruders and their objectives.
        - Threat Hunting relies on tools developed for regular security monitoring and incident response.
        - SIEM - Security Information and Event Management system.
        - TTP - Tactics, Techniques and Procedures
        
        ### Attack Frameworks
        
        - Types of Attack Frameworks are :
            - **Lockheed Martin Kill Chain :** A model developed by Lockheed Martin that describes the stages by which a threat actor progresses a network intrusion.
                - The Model :
                    - **Reconnaissance** - Understanding the network by mainly passive ways.
                    - **Weaponization** :  Duplicates a payload load that will enable the exploit.
                    - **Delivery** : Transmit the weaponized code to the target environment.
                    - **Exploitation** : Execution of weaponized code on the target system.
                    - **Installation** : Enables the weaponized code to run a remote access tool and achieve persistence on the target system.
                    - **Command and Control (C2)** : After establishing remote access tools, it controls the remote access tool and download additional tools the progress the attack
                    - **Actions on objectives** : The attacker typically uses the access he has achieved to covertly collect information from the target systems and transfer it to a remote system(data exfiltration) or achieve other goals or motives.
                - **MITRE ATT&CK Framework**
                    - A knowledge base maintained by the MITRE Corporation for listing and explaining specific adversary tactics, techniques, and common knowledge or procedures (attack.mitre.org)
                    - The **pre-ATT&CK tactics matrix** aligns to the reconnaissance and weaponization phases of the kill chain
                - **Diamond model of intrusion analysis**
                    - A framework for analyzing Cybersecurity intrusions and incidents by exploring relationships between four core features :
                        - **Adversary**
                        - **Capability**
                        - **Infrastructure**
                        - **Victim**