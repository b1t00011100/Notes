# Supply Chain Management

### Supply Chain Assessment

- Authentication of products.
- Secure working in an unsecure environment involves mitigating the risks of the supply chain.
- An organization must ensure that the operation of every element (hardware, firmware, driver, OS, and application) is consistent and tamper resistant to establish a trusted computing environment.
- **Due Diligence :** A legal principle identifying a subject has used best practice or reasonable care when setting up, configuring and maintaining a system.
    - Properly resourced cybersecurity program
    - Security assurance and risk management processes
    - Product support life-cycle
    - Security controls for confidential data
    - Incident response and forensics assistance
    - General and historical company information
- Due Diligence should apply to contractors and suppliers
- **Trusted Foundry :** A microprocessor manufacturing utility that is part of a validated supply chain (one where hardware and software does not deviate from its documented function)
    - Trusted foundry is operated by the Department of Defense(DOD/US Military).
- **Hardware Source Authenticity** : The process of ensuring that hardware is produced tamper-free from trustworthy suppliers.

### Root of Trust

- **Hardware Root of Trust :** A cryptographic module embedded within a computer system that can endorse trusted execution and attest to boot settings and metrics.
- A hardware root of trust is used to scan boot metrics and OS files to verify their signature, which we can then use to sign a digital report.
- **Hardware Security Module (HSM) :** An appliance for generating and storing cryptographic keys that is less susceptible to tampering and insider threats than software-based storage.
- **Anti Tamper** : Methods that make it difficult for an attacker to alter the authorized execution of software.

### Trusted Firmware

- A **Firmware exploit** gives an attacker an opportunity to run any code at the highest level of CPU Privilege.
- **UEFI :** A type of  system firmware providing support for 64-bit CPU operation at boot, full GUI and mouse operation at boot and better boot security.
- **Secure Boot :** A UEFI feature that prevents processes from executing during the boot operation.
- **Measured Boot :** A UEFI feature that gathers secure metrics to validate the boot process in an attestation report.(Analysis of Boot)
- **Attestation :** A claim that the data presented in the report is valid by digitally signing it using the TPM’s private key.
- **eFUSE :** A means for software or firmware to permanently alter the state of a transistor on a computer chip.
- **Trusted Firmware Updates :** A firmware update that is digitally signed by the vendor and trusted by the system before installation.
- **Self Encrypting Drvies :** A disk drive where the controller can automatically encrypt data that is written to it.

### Secure Processing

- A mechanism for ensuring the confidentiality, integrity and availability of software code and data as it is executed in volatile memory.
- **Processor Security Extension** : Low-level CPU changes and instructions that enable secure processing.
- **Trusted Execution** : The CPU’s security extensions invoke a TPM and secure boot attestation to ensure that a trusted operating system is running.
- **Secure enclave** : The extension allow a trusted process to create an encrypted container for sensitive data.
- **Automatic Execution** : Certain operations that should only be performed once or not at all such as initializing a memory location.
- **Bus Encryption** : Data is encrypted by an application prior to being placed on the data bus.