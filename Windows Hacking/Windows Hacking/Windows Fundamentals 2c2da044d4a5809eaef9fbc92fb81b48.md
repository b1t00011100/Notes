# Windows Fundamentals

### Windows Editions

- Windows XP
- Windows Vista
- Windows 7
- Windows 8
- Windows 10
- Windows 11

<aside>
💡

In Windows 11 Pro, you can enable BitLocker encryption which cannot be done in Windows 11 Home 

</aside>

---

## Intro to Windows

- The Windows OS is a complex product with many system files, utilities, settings, features, etc.

### The File system

- In modern versions of Windows, the file system used is NTFS. Before `NTFS (New Technology File System)`, there was `FAT16/FAT32 (File Allocation Table)` and `HPFS (High Performance File System)`.
- FAT Partitions are still seen today typically in USB devices, MicroSD cards, etc.
- NTFS addresses many of the limitations of the previous file systems; such as:
    - Supports files larger than 4GB
    - Set specific permissions on folders and files
    - Folder and file compression
    - Encryption
- Another feature of NTFS is ADS (Alternate Data Stream) which allows files to contain more than one stream of data.

### Windows / System 32 Folders

- The Windows folder (C:/Windows) is traditionally known as the folder which contains the Windows operating system.
- The folder doesn’t have to reside in the C drive necessarily.
- It can reside in any other drive and technically can reside in a different folder.
- This is where environment variables. more specifically system environment variables, comes into play. the system environment variable for the Windows directory is `%windir%`
- The System32 folder holds the important files that are critical for the operating system.

### Users

- User accounts can be one of two types on a typical local Windows system: Administrator & Standard User.
- The user account type will determine what actions the user can perform on that specific Windows system.
    - An administrator can make changes to the system: add users, delete users, modify groups, modify settings on the system, etc.
    - A Standard User can only make changes to folders/files attributed to the user & can’t perform system-level changes, such as install programs.
- Run the command `lusrmgr.msc` to view the Local User & Group Management tab.

### UAC

- A user doesn’t need to run with high (elevated) privileges on the system to run tasks that don’t require such privileges, such as surfing the Internet, working on a word document.
- This elevated privilege increases the risk of system compromise because it makes it easier for malware to infect the system.
- Consequently, since the user account can make changes to the system, the malware would run in the context of the logged-in user.
- UAC (User Account Control) was introduced to protect the local user with such privileges but doesn’t apply to the local admin account by default.
- Working of UAC - When a user with an account type of administrator logs into a system, the current session doesn’t run with elevated permissions, When an operation requiring higher-level privileges needs to execute, the user will be prompted to confirm if they permit the operation to run.

---

- The **System Configuration** utility (MSConfig) is for advanced troubleshooting, and its main purpose is to help diagnose startup issues.
- The **Computer Management (`compmgmt`)** utility has three primary sections :
    - System Tools
    - Storage
    - Services & applications

**System Tools**

- With **Task Scheduler**, we can create and manage common tasks that our computer will carry out automatically at the times we specify.
- A task can run an application, a script, etc., and tasks can be configured to run at any point. A task can run at log in or at log off. Tasks can also be configured to run on a specific schedule, for example, every five minutes.
- Event Viewer allows us to view events that have occurred on the computer. These records of events can be seen as an audit trail that can be used to understand the activity of the computer system. This information is often used to diagnose problems and investigate actions executed on the system.

**Storage**

- **Disk Management** is a system utility in Windows that enables you to perform advanced storage tasks. Some tasks are :
    - Set up a new drive
    - Extend a partition
    - Shrink a partition
    - Assign or change a drive letter (ex E:)

**Services and applications**

- WMI (Windows Management Instrumentation) allows scripting languages (such as VBScript or Windows Powershell) to manage Microsoft Windows personal computers and servers, both locally and remotely.
- Microsoft also provides a CLI to WMI called Windows Management Instrumentation Command-line (WMIC)

### System Information

- The system information `(msinfo32`) tool gathers information about computer and displays a comprehensive view of your hardware, system components, and software environment, which can be used to diagnose computer issues.
- System summary will display general technical specifications for the computer.
- Under Components, specific info about the hardware devices installed on the computer can be seen.
- Some sections dont show any info, but some sections do such as Display and input.
- In the Software Environment section, you can see information about software baked into the operating system and software you have installed.
- Other details are visible in this section as well, such as the Environment Variables and Network Connections.

### Resource Monitor

- Resource monitor (`resmon`) displays per-process and aggregate CPU, memory, disk, and network usage information, in addition to providing details about which processes are using individual file handles and modules.
- Advanced filtering allows users to isolate the data related to one or more processes (either application or service), start, stop, pause and resume services and close unresponsive applications from the user interface.

### Command Prompt

- The command prompt (`cmd`) is not the only way to interact with OS on windows, but on early systems, it was the sole way to interact with it.
- When the GUI was introduced, it allowed users to perform complex tasks with a few clicks of a button instead of entering commands in the command prompt.
- Even though the GUI is the primary way to interact with the OS, a computer can still interact via the command prompt

### Registry Editor

- The Windows Registry is a central hierarchical database used to store information necessary to configure the system for one or more users, applications, and hardware devices. The registry contains information that Windows continually references during operation.
- There are various ways to view/edit the registry. One way is to use the Registry Editor (`regedt32`).