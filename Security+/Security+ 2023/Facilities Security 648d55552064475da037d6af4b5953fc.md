# Facilities Security

### Fire Suppression

- **Fire Suppression :** Process of controlling and/or extinguishing fires to protect an organization’s employees, data, equipment and buildings.
- 3 Types of Fire Suppression
    - **Handheld Fire Suppression Systems - Fire Extinguishers.**
        - Fires are broken down in 5 Classes : ***A,B,C,D,K***
            - **Class A** : Ordinary Combustibles : wood, paper, rubber, fabrics and many plastics. - For this an **Water-Based Extinguisher** to be used.
                - Water-Based Extinguishers should not be used in server rooms.
            - **Class B** : Flammable Gases or Liquids - an **Dry chemical agent or CO2 Extinguisher** to be used.
            - **Class C** : Fires involving Live Electrical Equipment - CO2 Based Extinguisher.
            - **Class D** : Combustibles metals or Combustible Metal Alloys - **Extinguisher with a yellow decagon** on it to be used.
            - **Class K** : Fire in Cooking Appliance that involves Combustible Cooking Media : Vegetable or Animal Oils and Fats - **Extinguisher with a Black Hexagon** on them to be used.
    - **Sprinklers Fire Suppression System**
        - **Wet Pipe** : Pipes are filed with water all the way to the sprinkler head and are just waiting for the bulb to be melted or broken.
        - **Dry Pipe** : Pipes are filled with pressurized air and only push water into the pipes when needed to combat the fire.
        - A **Pre-Action sprinkler system** will activate when heat or smoke is detected.
    - **Special Hazard Protection**
        - Clean Agent System : Fire Suppression system that relies upon gas(HALON,FM-200 or C02) instead of water to extinguish a fire.

### HVAC

- **H**eating, **V**entilation, and **A**ir **C**onditioning
- Humidity should be kept around 40%.
- HVAC systems may be connected to ICS(Industrial Control Systems) and SCADA(Supervisory Control and Data Aquisition System) networks.

### Shielding

- To reduce EMI in cables, STP should be used.
- **Shielded Twisted Pair (STP)** adds a layer of shielding inside the cable.
- HVAC should also be shielded as its a large motor or large generator.
- **Faraday Cage** : Shielding installed around an entire room that prevents electromagnetic energy and radio frequencies from entering or leaving the room.
- **TEMPEST** : U.S Government standards for the level of shielding required in a building to ensure emissions and interference cannot enter or exit the facility.
    - **TEMPEST** Facilities are also resistant to EMPs(Electromagnetic Pulses).

### Vehicular Vulnerabilities

- Vehicles connect numerous subsystems over a controller area network(CAN).
- **Controller Area Network** : A digital serial data communications used within vehicles.
- The primary external interface is the **Onboard Diagnostics(OBD-II)** module.
- How the attacker gets into the CAN bus :
    - Attach the exploit to OBD-II
    - Exploit over onboard cellular
    - Exploit over onboard WiFi

### IoT Vulnerabilities

- **Internet of Things** : A group of objects that are connected to the wider Internet by using electronic components.
- Most smart devices use an embedded version of Linux or Android as their OS.
- Devices must be secured and updates when new vulnerabilities are found.

### Embedded System Vulnerabilities

- **Embedded Systems** : A computer system that is designed to perform a specific dedicated function.
- **Embedded systems** are considered static environments where frequent changes are not made or allowed.
- Embedded systems have very little support for identifying and correcting security issues.
- **Programmable Logic Controller(PLC)** : A type of computer designed for deployment in an industrial or outdoor setting that can automate and monitor mechanical systems.
- **PLC** can be patched and reprogrammed to fix vulnerabilities.
- **System-on-Chip(SoC)** : A processor that integrates the platform functionality of multiple logical controllers onto a single chip.
- **SoC** are power efficient and used with embedded systems.
- **Real-Time Operating Systems** : A type of OS that prioritizes deterministic execution of operations to ensure consistent response for time-critical tasks.
- **Embedded systems** typically cannot tolerate reboots or crashes and must have response times that are predictable to within microsecond tolerances.
- **Field Programmable Gate Array (FPGA)** : A processor that can be programmed to perform a specific function by a customer rather than at the time of manufacture.
- End customer can configure the programming logic to run a specific application instead of using an ASIC (Application Specific Integrated Circuit).

### ICS and SCADA vulnerabilities

- **Operational Technology(OT)** : A communication network designed to implement an industrial control system rather than data networking.
- Industrial systems prioritize availability and integrity over confidentiality.
- This is based on AIC triad.
- **Industrial Control Systems (ICS)** : A network that manages embedded devices.
- **ICS** is used for electrical power stations, water suppliers, health services, telecommunications, manufacturing and defense needs.
- **Fieldbus** : Digital serial data communications used in operational technology networks to link PLC.
- **Human Machine Interface (HMI)** : Input and Output controls on a PLC to allow a user to configure and monitor the system.

<aside>
💡 ICS manages the process automation by linking together PLCs using a fieldbus to make changes in the physical world (values, motors, etc)

</aside>

- **Data Historian** : Software that aggregates and catalogs data from multiple sources within an industrial control systems.
- **Supervisory Control and Data Aquisition (SCADA)** : A type of industrial control system that manages large-scale, multiple site devices and equipment spread over a geographic region.
    - When you talk about ICS u look at a single plant and with SCADA multiple plants.
- **SCADA** typically run as software on ordinary computers to gather data from and manage plant devices and equipment with embedded PLCs.
- **MODBUS** : a Communication protocol used in operational technology networks.
- **Modbus** gives control servers and SCADA hosts the ability to query and change the configuration of each PLC.

### Mitigating Vulnerabilities

- Four Key controls for mitigating vulnerabilities in specialized systems
1. Establish administrative control over Operational Technology networks by recruiting staff and relevant expertise
2. Implement the minimum network links by disabling unnecessary link, service and protocols.
3. Develop and test a patch management program for Operational Technology networks. 
4. Perform regular audits of logical and physical access to systems to detect possible vulnerabilities and intrusions.

### Premise System Vulnerabilities

- Systems used for building automation and physical access security.
- Many system designs allow the monitoring to be accessible from the corporate data network or even directly from the internet.
- **Building Automation Systems (BAS)** : Components and protocols that facilitate and centralized configuration and monitoring of mechanical and electrical systems within offices and data centers.
- Vulnerabilities of BAS
    - Process and memory vulnerabilities in PLC.
    - Plaintext credentials or keys in application code.
    - Code injections via web user interface.
- Denial of Service conditions could be caused by affecting building automation systems like HVAC.
- **Physical Access Control System (PACS)** : Components and protocols that facilitate the centralized configurations and monitoring of security mechanisms within offices and data centers.