# Hardening

- Act of Configuring an operating system securely by updating it, creating rules and policies to govern it, and removing unnecessary applications and services.
- Basically Optimizing and Maintaining OS.
- Minimize the theft risk by performing some hardening actions i.e Minimizing Vulnerabilities.

### Unnecessary Applications

- **Least Functionality :** Restricting Unnecessary Applications.
- Utilize a secure baseline image when adding new computers.
- SCCM : Microsoft’s System Center Configuration Management.

### Restricting Applications

- **Application Allowlisting  :** Only applications that are in the list are allowed to be run by the OS while all other applications are blocked.
- **Applications Blocklisting :** Any applications placed on the list will be prevented from running while all others will be permitted to run.
- Allowlisting and Blocklisting can be managed centrally.
- Any services that are unneeded should be disabled in the OS.

### Trusted Operating Systems(TOS)

- An **Operating System** that meets the requirements set forth by government and has multilevel Security.
    - Windows 7 and newer
    - Mac OS X 10.6 and newer
    - FreeBSD
    - Red Hat Enterprise Server
- An OS manufacturer should provide Patches to maintain a security.
- You need to identify Current OS version and build prior to it.

### Updates and Patches

- **Patches :** A Single problem-fixing piece of software for an operating system or application.
- Originally **Hotfix** can be installed without rebooting the system. ****
- But now **Patches** and **Hotfixes** are now used interchangeably by most manufacturers.
- **Categories Of Updates**
    - **Security Update :** Software code that is issued for a product-specific security-related vulnerability.
    - **Critical Update :** Software code for a specific problem addressing a critical, non-security bug in the software.
    - **Service Pack :** A tested, cumulative grouping of patches, hotfixes, security updates , critical updates and possibly some feature or design changes.
    - **Windows Update :** Recommended update to fix a noncritical problem that users have found, as well as to provide additional features or capabilities.
    - **Drivers Update :** Updated device driver to fix a security issue or add a feature to a supported piece of hardware.

### Patch Management

- Process of planning, testing, implementing and auditing of software patches.
- **Steps for Patch Management**
    1. **Planning** - Planning is creating policies, procedures and systems to track available patches and updates and check compatibility.
    2. **Testing -** Always test a patch prior to automating its deployment.
    3. **Implementing -** Manually or automatically deploy the patch to all your clients to implement it.
    4. **Auditing -** It’s important to audit the client’s status after patch deployment.
- Linux and OSX also have a built-in patch management systems.

### Group Policies

- set of rules or policies that can be applied to set of users or computers accounts within the operating systems.
- To access Group policy - In run - command: ‘**gpedit**’.
- Every Policy has certain rules , these rules can be like :
    - Password Complexity
    - Account Lockout Policy
    - Software restrictions
    - Application restrictions
- **Security Template** : A group of policies that can be loaded through one procedure.
- **Group Policy Objectives (GPOs) aid in the hardening of the operating system**
- **Baselining** : Process of measuring changes in the network, hardware, and software environment.
    - A Baseline establishes what is normal so you can find deviations.

### File Systems and Hard-drives

- Level of security of a system is effected by its file system type.
    - NTFS
    - FAT32
    - ext4
    - HFS+ (Hierarchical File System Plus)
    - APFS (Apple File System)
- **Windows systems can utilize NTFS or FAT32**
- **NTFS(New Technology File System)** : default file system for windows and is more secure because it supports logging, encryption, larger partition sizes, and larger file sizes than FAT32
- Linux systems should use ext4 and OSX should use the APFS.
- All hard drives eventually fail.
    - Things to delay this
        - Remove Temporary files by using disk cleanup.
        - Periodic System file checks.
        - Defragment your disks
        - Back up your data.
        - Use and practice restoration techniques.