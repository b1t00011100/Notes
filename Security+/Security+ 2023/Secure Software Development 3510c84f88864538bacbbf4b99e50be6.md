# Secure Software Development

### Software Development Life Cycle

- **SDLC (Software Development Life Cycle)** : SDLC is an organized process of developing a secure application throughout the life of the project.
    - This process covers everything From idea to coding to deployment and even its retirement.
    - It is based on generic Waterfall model of development.
- **Agile Development** : Software development is performed in time-boxed or small increments to allow more adaptivity to change.
- **DevOps** : Software Development and information technology operations.

![several-consecutive-phases-of-the-classical-waterfall-model.webp](Secure%20Software%20Development/several-consecutive-phases-of-the-classical-waterfall-model.webp)

### Phases of SDLC

- Planning and Analysis
- Software/System Design
- Implementation
- Testing
- Integration
- Deployment
- Maintenance

### Principles of SDLC

- Developers should always remember confidentiality, integrity and availability.
- During **Testing phase**, it is important to ensure that there are no vulnerabilities.
    - This task is performed by developers and not security analysts.
    - Security analysts perform threat modeling, Threat Modeling helps prioritize vulnerability identification and patching.
- Good security is implemented in the analysis and implementation phases.
- **Least Privilege** : Users and processes should be run using least amount of access necessary to perform a given function.
- **Defense in Depth** : Layering of security controls is more effective and secure than relying on a single control.
- **Never Trust User Input** : Any Input that is received from a user should undergo input validation prior to allowing it to be utilized by an application.
- **Minimize Attack Surface** : Reduce the amount of code used by a program, eliminate unneeded functionality, and require authentication prior to running additional plugins.
- **Authenticity and Integrity** : Applications should be deployed using code signing to ensure the program is not changed inadvertently or maliciously prior to delivery to an end user.
- **Fail Securely** : Exception Handling should be carried throughout the code, so it will fail securely instead of crashing.
- **Fix Security Issues** : Vulnerabilities should correctly patched.
- **Rely on Trusted SDKs(Software Development Kit):** SDKs must come from trusted sources to ensure no malicious code is being added.

### Testing Methods

- **System Testing**
    - **Black Box Testing** : Occurs when a tester is not provided with any information about the system or program prior to conducting the test.
    - **White Box Testing** : Occurs when a tester is provided full details of a system including the source code, diagrams, and user credentials in order to conduct the test.
    - **Gray Box Testing** : Mixture white and black box testing. Tester is given very little information about the site.
- If a program is running and error occurs it is called **runtime error**.
- If a program fails to run because of the code it is known as **syntax error.**
- Runtime error occur frequently as tester is running it in real time environment.
- **Structure Exception Handling** (**SEH**): Provides control over what the application should do when faced with a runtime or syntax error.
- To make errors occur, Tester should provide the site with an erroneous input as an end user.
- Programs should use input validation when taking data from users.
- **Input Validations** : Applications verify that information received from a user matches a specific format or range of values.
- **Static Analysis** : Analysis of source code prior to running it.
- **Dynamic Analysis** : Analysis of a program while its running.
- **Fuzzing** : Injection of randomized data into a software program in an attempt to find system failures, memory leaks, error handling issues and improper input validation.

### Software Vulnerability and Exploits

- **Backdoors :** Code placed in computer programs to bypass normal authentication and other security mechanisms.
    - Backdoors are a poor coding practice and should not be utilized.
- **Directory Traversal :** Method of accessing unauthorized directories by moving through the directory structure on a remote server.
- **Arbitrary Code Execution :** Occurs when an attacker is able to execute or run commands on a victim computer.
    - **REMOTE CODE EXECUTION(RCE) :** Occurs when an attacker is able to execute or run commands on a remote computer.
    - The difference between ACE and REC is In, RCE attacker can run commands remotely such as through an interactive shell session or some kind of other attack.
- **Zero Day Attack :** Attack against a vulnerability that is unknown to the original developer or manufacturer.

### Buffer Overflows

- **Buffer Overflow** : Occurs when a process stores data outside the memory range allocated by the developer.
    - **Buffer** : A temporary storage area that a program uses to store data.
- Over 85% data breaches were caused by Buffer Overflows.
- **Smash the Stack :** Occurs when an attacker fills up the buffer with NOP(Non Operation Instruction) so that the return address may hit a NOP and continue on until it finds the attackers code to run.
- **Address Space Layout Randomization** : Method used by programmers to randomly arrange the different address spaces used by program or process to prevent buffer overflow exploits.

<aside>
💡 Buffer Overflow attempt to put more data into memory than it is designed to hold.

</aside>

### XSS and XSRF

- Types of Web applications vulnerabilities are known as **Cross Site Scripting and Cross-site request forgery.**
- **Cross-Site Scripting(XSS) :** Occurs when an attacker embeds malicious scripting commands on a trusted website.
    - During a cross-scripting attack, the victim is the user, not the website
- Three types of Cross Scripting attack
    - **Stored/Persistent :** Attempts to get data provided by the attacker to be saved on the web server by the victim.
    - **Reflected :** Attempts to have a non-persistent effect activated by a victim clicking a link on the site.
    - **DOM-based : Document Object Model based** - Attempt to exploit the victim’s web browser and often called client side cross-scripting attack.
- Prevent XSS with output encoding and proper input validation.
- **Cross Site Request Forgery (XSRF/CSRF)** : Occurs when an attacker forces a user to execute actions on a webserver for which they are already authenticated.
- Prevent XSRF with tokens, encryption, XML file scanning, and cookie verification.

### SQL Injection

- **SQL** : **S**tructured **Q**uery **L**anguage is the way web server connects to their database server to ask for information.
- **SQL Injection** : Attack consisting of the insertion or injection of an SQL query via input data from the client to a web application.
- **Injection Attack** : Insertion of additional information or code through data input from a client to an application.
    - Most common Injections :
        - SQL
        - HTML
        - XML
        - LDAP
- Most common are SQL injections
- SQL injections is prevented through input validation and using least privilege when accessing a database.
- Syntax : `‘ or 1=1`

### XML Vulnerabilities

- XML : Extensible Markup Language used for web applications for authentication and authorizations and for other types of data exchange and uploading.
- XML data submitted without encryption or input validation is vulnerable to spoofing , request forgery and injection of arbitrary code.
- Some of the xml exploits
    - **XML Bomb (Billion Laughs Attack)** : XML encodes entities that expand to exponential sizes, consuming memory on the host and potentially crashing it. like a Denial of Service Attack
    - **XML External Entity (XXE)** : An attack that embeds a request for a local resource. like a File Inclusion
- To prevent XML Vulnerabilities from being exploited, use proper input validation.

### Race Conditions

- A Software Vulnerability when the resulting outcome from execution processes is directly dependent on the order and timing of certain events, and those events fail to execute in the order and timing intended by the developer.
- A race condition vulnerability is found where multiple threads are attempting to write a variable or object at the same memory location.
- **Dereferencing** : A software Vulnerability that occurs when the code attempts to remove the relationship between a pointer and the thing it points to.
- Race Conditions are difficult to detect and mitigate.
- This can also be used against databases and file-Systems.
- **Time of Check to Time to Use (TOCTTOU)** : The potential Vulnerability that occurs when there is a change between when an app checked a resource and when the app used the resource.
- Ways to Prevent Race Conditions and TOCTTOU :
    1. Develop applications to not process things sequentially if possible.
    2. Implement a locking mechanism to provide app with exclusive access.

### Design Vulnerabilities

- **Vulnerabilities** often arise from the general design of the software code.
- Three main types
- **Insecure Components :** Any code that is used or invoked outside the main program development process.
    - Code Reuse
    - Third-Party Library
    - Software Development Kit (SDKs)
- **Insufficient Logging and Monitoring :** Any program that does not properly record or log detailed enough information for an analyst to perform an job.
    - Logging and Monitoring must support your use case and answer who, what, when, where and how.
- **Weak or default Configurations :** Any program that used ineffective credentials or configurations, or one in which the defaults have not been changed for security.
    - Many applications choose to simply run as root or as a local admin.
    - Permissions may be too permissive on files or directories due to weak configurations.