# Virtualization

- Creation of Virtual resource
    - You can virtualize many things like servers, laptops, hard drives and even an entire network.
    - Most common use of Virtualization is Virtual Machines(VMs)
        - **Virtual Machine** is a container for an emulated computer that runs an entire OS.
        - VM types: System or Processor
        - **System VM** : Complete platform designed to replace an entire physical computer and includes a full desktop/server OS.
        - **Processor VM** : Designed to run a single application like a virtualized web browser or a simple web server.
- **Virtualization** continues to rise in order to reduce the physical requirements for data centers.

### Hypervisor

- Manages the distribution of the physical resources of a host machine(server) to the virtual machine being run
- Two types of hypervisors
    - Type I (bare metal)
    - Type II (host based)
    - **Type I hypervisors are more efficient then Type II**.
- Third type of Virtualization becoming popular nowadays,
    - **Application Container-Based Virtualization :** A Single operating system kernel is shared across multiple VMs but each has its own space for programs and data.
    - Containerization allows for rapid and efficient deployment of distributed applications.

### Threats to VMs

- **VM escape :** An attack that allows an attacker to break out of a normally isolated VM by interacting directly with the hypervisor.
- **Data remnants :** Contents of a virtual machine that exist as deleted files on a cloud-based server after deprovisioning of a virtual machine.
- **Privilege Escalation**
- **Live VM Migration :** When a VM is moved from one server to another.

### Securing VMs

- Securing VMs uses many of the same security measures as a physical server.
- Ensuring each VM has a good Anti Virus installed.
- Patches to be installed up-to-date.
- Limit Connectivity between the virtual machine and the host.
- If VM gets affected with malware, every other machine on that hypervisor should remain secure but if the VMs share a common resource this breaks the isolation.
- Remove any Unnecessary pieces of virtual hardware from Virtual Machine.
- Using Proper patch management is important to keeping your guest’s operating system secure.
- **Virtualization Sprawl** : Occurs when VMs are created, used and deployed without proper management or oversight by the system admins.
- Enable Encryption on the files that host VMs.