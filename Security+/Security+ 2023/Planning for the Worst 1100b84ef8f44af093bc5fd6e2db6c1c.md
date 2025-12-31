# Planning for the Worst

### Planning for the Worst

- It is done by R**edundancy** & **Disaster Recovery Planning.**
- **Redundancy** usually refers to when you have something extra or unnecessary.
- Redundancy helps ensure fault-tolerance to continue operations.
- **Single Point of Failure :** The individual elements, objects, or parts of a system that would cause the whole system to fail if they were to fail.

### Redundant Power

- **Redundant Power Supply :** An enclosure that provides two or more complete power supplies.
- A *redundant power* supply mitigates a single point of failure.
- Issues with power source :
    - **Surges :** An unexpected increase in the amount of voltage provided.
    - **Spikes :** A short transient in voltage that can be due to a short circuit, tripped circuit breaker, power outage, or lightning strike.
    - **Sags :** An unexpected decrease in the amount of voltage provided.
    - **Brownouts :** Occurs when the voltage drops low enough that it typically causes the lights to dim and can cause a computer to shut-off.
    - **Blackouts :** Occurs when there is a total loss of power for a prolonged period.

### Backup Power

- **Uninterruptible Power Supply (UPS)** : Combines the functionality of a surge protector with that of a battery backup.
- **Backup Generator :** An emergency power system used when there is an outage of the regular electric grid power.
- There are mainly 3 types of generator
    - **Portable gas-engine**
    - **Permanently installed**
    - **Battery-inverter**

### Data Redundancy

- **Redundant Arrays of Independent Disks (RAID)** : Allows the combination of multiple physical hard disks into a single logical hard disk drive that is recognized by the operating system.
    - **RAID 0 :** Provides data striping across multiple disks to increase performance.
    - **RAID 1 :** Provides redundancy by mirroring the data identically on two hard disks.
    - **RAID 5 :** Provides redundancy by striping data and parity data across the disk drives.
    - **RAID 6 :** Provides redundancy by striping and double parity data across the disk drives.
    - **RAID 10 :** Creates a striped RAID of two mirrored RAIDs (combines RAID 1 & RAID 0).
- RAID can be classified as :
    - **Fault-resistant :** Protects against the loss of the array’s data if a single disk fails.(RAID 1 or RAID 5)
    - **Fault-tolerant :** Protects against the loss of the array’s data if a single component fails. (RAID 1, RAID 5, RAID 6)
    - **Disaster-tolerant :** Provides two independent zones with full access to the data. (RAID 10).
- RAID provides *redundancy* and high *availability*.

### Network Redundancy

- Focused on ensuring that the network remains up.
- Having redundant ports for backup.

### Server Redundancy

- **Cluster :** Two or more servers working together to perform a particular job function.
    - **Failover Cluster :** A secondary server can take over the function when the primary one fails.
    - **Load-balancing Cluster :** Servers are clustered in order to share resources such as CPU, RAM, and hard disks.

### Redundant Sites

- Backup workstations.
- They can classified in 3 different Categories
    - **Hot Site :** A near duplicate of the original site of the organization that can be up and running within minutes.
    - **Warm Site :** A site that has computers, phones, and servers but they might require some configuration before users can start working.
    - **Cold Site :** A site that has tables, chairs, bathrooms, and possibly some technical items like phones and network cabling.

### Data Backup

- Maintaining a good backup is crucial to disaster recovery.
- They are differentiated in 3 types
    - **Full :** All of the contents of a drive are backed up.
    - **Incremental :** Only conducts a backup of the contents of a drive that have changed since the last full or incremental backup.
    - **Differential :** Only conducts a backup of the contents of a drive that has changed since the last full backup.
- Differential backup take more time to create but less time to restore.

### Tape Rotations

- **10 Tape Rotation :** Each tape is used once per day for two weeks and then the entire set is reused.
- **Grandfather-Father-Son :** Three sets of backup tapes are defined as the son (daily), the father (weekly) and the grandfather (monthly).
- **Towers of Hanoi :** Three sets of backup tapes that are rotated in a more complex manner.
- **Snapshot Backup :** Type of backup primarily used to capture the entire operating system image including all applications and data.
    - Snapshots are also commonly used with virtualized systems.

### Disaster Recovery Planning

- **Disaster Recovery Planning :** The development of an organized and in-depth plan for problems that could affect the access of data or the organization’s building.
- **Disaster Recovery Plan (DRP)** should be written down.
    - Contact Information
    - Impact Determination
    - Recovery Plan
    - Business Continuity Plan (BCP)
    - Copies of Agreements
    - Disaster Recovery Exercises
    - List of Critical Systems and Data

### Business Impact Analysis

- **Business Impact Analysis (BIA) :** A systematic activity that identifies organizational risks and determines their effect on ongoing, mission critical operations.
- *Business impact analysis* is governed by metrics that express system availability.
- Factors when we talk about metrics
    - **Maximum Tolerable Downtime :** The longest period of time a business can be inoperable without causing irrevocable business failure.
        - Each business process can have its own MTD, such as
            - Range of Minutes - Critical Functions
            - 24 Hours - Urgent Functions
            - 7 Days - Normal Functions
        - MTD sets the upper limit on the recovery time that system and asset owner need to resume operations.
    - **Recovery Time Objective :** The length of time it takes after an event to resume normal business operations and activities.
    - **Work Recovery Time :** The length of time in addition to the RTO of individual systems to perform reintegration and testing of a restored or upgraded system following an event.
    - **Recovery Point Objective :** The longest period of time that an organization can tolerate lost data being unrecoverable.
        - RPO is focused on how long you can be without your data.
- Designing your disaster recovery and continuity of operations plans requires an understanding of your availability and reliability levels.
- Disasters can be caused by internal and external forces.
- **Mean Time To Repair (MTTR) :** Measure the average time it takes to repair a network device when it breaks.
- **Mean Time Between Failures (MTBF) :** Measures the average time between failures of a device.