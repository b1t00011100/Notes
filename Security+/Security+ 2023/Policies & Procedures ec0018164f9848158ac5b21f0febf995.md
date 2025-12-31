# Policies & Procedures

### Policies & Procedures

- *Governance* provides a comprehensive security management framework.
- **Policies :** Defines the role of security in an organization and establishes the desired end state of the security program.
    - *Policies* are very broad
    - **Organizational Policies :** Provide general direction and goals, a framework to meet the business goals and define the roles, responsibilities and terms.
    - **System-Specific Policies :** Address the security needs of a specific technology, application, network, or computer system.
    - **Issue-Specific Policies :** Built to address a specific security issue, such as email privacy, employee termination procedures or other specific issues.
- **Policies may be *regulatory, advisory or informative.***
- **Standards** are used to implement a policy in an organization.
- **Baseline :** Created as reference points which are documented for use as a method of comparison during an analysis conducted in the future.
- *Guidelines* are used to recommended actions.
- **Procedures :** Detailed step-by-step instructions that are created to ensure personnel can perform a given action.

<aside>
💡 *Exam Tip* :

- **Policies are generic.**
- **Procedures are specific.**
</aside>

### Data Classifications

- **Data Classification :** Category based on the value to the organization and the sensitivity of the information if it were to be disclosed.
- **Sensitive Data :** Any information that can result in a loss of security, or loss of advantage to a company, if accessed by unauthorized persons.
- *Commercial businesses* and *the government* use different classification systems.
    - **Commercial Classifications**
        - **Public Data :** Has no impact to the company if released and is often posted in the open-source environment.
        - **Sensitive Data :** Might have a minimal impact if released.
        - **Private Data :** Contains data that should only be used within the organization.
        - **Confidential Data :** Highest Classification level that contains items such as trade secrets, intellectual property data, source code and other types that would seriously affect the business if disclosed.
    - **Government Classifications**
        - **Unclassified Data :** can be released to the public.
        - **Sensitive but Unclassified Data :** Items that wouldn’t hurt national security if released but could impact those whose data is contained in it.
        - **Confidential Data :** Data that could seriously affect the government if unauthorized disclosure were to happen.
        - **Secret Data :** Data that could seriously damage national security if disclosed.
        - **Top Secret Data :** Data that could gravely damage national security if it were known to those who are not authorized for this level of information.
- *Data should not be stored forever.*

### Data Ownership

- **Data Ownership :** The process of identifying the person responsible for the confidentiality, integrity, availability, and privacy of information assets.
- Roles in Data Ownership
    - **Data Owner :** A senior (executive) role with ultimate responsibility for maintaining the confidentiality, integrity, and availability of the information asset.
        - The Data Owner is responsible for labeling the asset and ensuring that it is protected with appropriate controls.
    - **Data Steward :** A role focused on the quality of the data and associated metadata.
    - **Data Custodian :** A role responsible for handling the management of the system on which the data assets are stored.
        - Example : System Administrator.
    - **Privacy officer :** A role responsible for the oversight of any PII/SPI/PHI assets managed by the company.

### PII & PHI

- **PHI — Protected Health Information**
- **PII — Personally Identifiable Information**
    - A piece of data that can be used either by itself or in combination with some other pieces of data to identify a single person.
    - Example : Full Name, Driver’s License, Date of Birth, etc.
- PII should be verified by the legal team.
- Following Laws were designed to help protect against the disclosure of data.
    - **Privacy Act of 1974 :** Affects U.S government computer systems that collects, stores, uses or disseminates personally identifiable information.
    - **Health Insurance Portability and Accountability ACT (HIPAA) :** Affects healthcare providers, facilities, insurance companies, and medical data clearing houses.
    - **Sarbanes-Oxley (SOX) :** Affects publicly-traded U.S corporations and requires certain accounting methods and financial reporting requirements. ****
    - **Gramm-Leach-Bliley Act (GLBA) :** Affects banks, mortgage companies, loan offices, insurance companies, investment companies and credit card providers.
    - **Federal Information Security Management Act(FISMA) of 2002 :** Requires each agency to develop, document and implement an agency-wide information systems security program to protect their data.
    - Payment Card Industry Data Security Standard (PCI DSS) is a contractual obligation or agreement.
    - **Help America Vote Act (HAVA) of 2002 :** Provides regulations that govern the security, confidentiality, and integrity of the personal information collected, stored, or processed during the election and voting process.

### Legal Requirements

- Any type of information or asset should consider how a compromise of that information can threaten the three core security attributes of the CIA triad.
- **Privacy V/S Security**
    - Security Controls focus on the CIA attributes of the processing system.
    - **Privacy :** A data governance requirement that arises when collecting and processing personal data to ensure the rights of the subject’s data.
- **Legal Requirements** will affect your corporate governance and policies in regards to privacy of your user’s data.
- **General Data Protection Regulation (GDPR) :** Personal data cannot be collected, processed or retained without the individual’s informed consent.
    - GDPR also provides the right for a user to withdraw consent, to inspect, amend or erase data held about them.
    - GDPR requires data breach information within 72 hours.

### Privacy Technologies

- **Deidentification :** Methods and technologies that remove identifying information from data before it is distributed.
    - Deidentification is often implemented as part of database design.
    - *Topics in Deidentification*
        - **Data Masking :** A deidentification method where generic or placeholder labels are substituted for real data while preserving the structure or format of the original data.
        - **Tokenization :** A deidentification method where a unique token is substituted for real data.
        - **Aggregation/Banding :** A deidentification technique where data is generalized to protect the individuals involved.
        - **Reidentification :** An attack that combines a deidentified dataset with other data sources to discover how secure the deidentification method used is.

### Security Policies

- Privacy Policies govern the labelling and handling of data.
- **Acceptable Use Policy (AUP) :** Defines the rules that restrict how a computer, network, or other systems may be used.
- **Change Management Policy :** Defines the structured way of changing the state of a computer system, network or IT procedure.
- **Separation of Duties** is a preventive type of administrative control.
- **Dual Control** is when two admins do a two different duties.
- **Split Knowledge** is when two people have half of the knowledge to do something.
- **Job Rotation :** Different users are trained to perform the tasks of the same position to help prevent and identify fraud that could occur if only one employee had the job.
- **Onboarding & Offboarding Policies :** Dictates what type of things need to be done when an employee is hired, fired, or quits.
- Terminated employees are often not cooperative.
- Concepts to be kept in mind while writing policies.
    - **Due Diligence :** Ensuring that IT infrastructure risks are known and managed properly.
    - **Due Care :** Mitigates actions that an organization takes to defend against the risks that have been uncovered during due diligence.
    - **Due Process :** A legal term that refers to how an organization must respect and safeguard personnel’s rights.
        - Due Process protects citizens from their government and companies from lawsuits.

### User Education

- **Security Awareness Training :** Used to reinforce to users the importance of their help in securing the organization’s valuable resources.
    - User security awareness training has the best return on investment.
- **Security Training :** Used to teach the organization’s personnel the skills they need to perform their job in a more secure manner.
- **Security Education** is generalized training (like *Security*+)

### Vendor Relationships

- **NDA (Non-Disclosure Agreement) :** Agreement between two parties that defines what data is considered confidential and cannot be shared outside of the relationship.
    - *NDAs are a binding contract.*
- **MOU (Memorandum of Understanding) :** A non-binding agreement between two or more organizations to detail an intended common line of action, *like a formal Version of Gentleman’s Agreement*
- **SLA (Service-Level Agreement) :** An agreement concerned with the ability to support and respond to problems within a given timeframe and continuing to provide the agreed upon level of service to the user.
- **ISA (Interconnection Security Agreement) :** An agreement for the owners and operators of the IT systems to document what technical requirements each organizations must meet.
- **BPA (Business Partnership Agreement) :** Conducted between two business partners that establishes the conditions of their relationships.
    - *A BPA can also include security requirements.*

### Disposal Policies

- Asset disposal occurs whenever a system is no longer needed.
- **Degaussing :** Exposes the hard drive to a powerful magnetic field which in turn causes previously-written data to be wiped from the drive.
- **Purging (Sanitizing) :** Act of removing data in such a way that it cannot be reconstructed using any known forensics techniques.
- **Clearing :** Removal of dat with a certain amount of assurance that it cannot be reconstructed.
- Data remnants are a big security concern.
- Possible reuse of the device will influence the disposal method.
- While writing Disposal Policies, Following steps should be followed.
    - Define which equipment will be disposed of
    - Determine a storage location until disposal
    - Analyze equipment to determine disposal - reuse, resell or destruction.
    - Sanitize the device and remove all its data.
    - Throw away, recycle or resell the device.

### IT Security Frameworks

- **Frameworks** are used as a basis for *policies*, *procedures* and *standards*.
- **Sherwood Applied Business Security Architecture (SABSA)** is a risk-driven architecture.
- **Control Objectives for information and Related Technology (COBIT) :** A security framework that divides IT into four domains : Plan and Organize, Acquire and Implement, Deliver and Support, and Monitor and Evaluate.
- **NIST SP 800-53** is a security control framework developed by the Dept. of Commerce.
- **ITIL** is the de facto standard for IT service management.

### Key Frameworks

- **Central for Internet Security (CIS) :** Consensus-developed secure configuration guidelines for hardening (benchmarks) and prescriptive, prioritized and simplified sets of cybersecurity best practices.
- **Risk Management Framework (RMF) :** A process that integrates security and risk management activities into the system development life cycle through an approach to security control selection and specification that considers effectiveness, efficiency, and constraints due to applicable laws, directives, Executive Orders, policies, standards, or regulations.
    - Only thing to remember for exam : RMF is made by NIST and its used in federal government systems.
- **Cybersecurity Framework (CSF) :** A set of industry standards and best practices created by NIST to help organizations manage cybersecurity risks.
- **ISO** is the **International Organization for Standardization.**
- **ISO 27001 :** An international standard that details requirements for establishing, implementing and continually improving an information security management system (ISMS). ****
    - ISO 27001 is the basic procedure for cybersecurity and an international standard.
- **ISO 27002 :** An international standard that provides best practice recommendations on information security controls for use by those responsible for initiating, implementing or maintaining information security management systems (ISMS).
- **ISO 27701 :** An international standard that acts as a privacy extension to the ISO 27001 to enhance the existing information Security Management Systems (ISMS) with additional requirements in order to establish, implement, maintain and continually improve a Privacy Information Management System (PIMS).
- **ISO 31000 :** An international standard for enterprise risk management that provides a universally recognized paradigm for practitioners and companies employing risk management processes to replace the myriad of existing standards, methodologies and paradigms that differed between industries, subject matters and regions.

<aside>
💡 ISO Frameworks in Brief :-

ISO 27001 - information Systems

ISO 27002 - controls to Protect those systems.

ISO 27701 - adding privacy on top of that

</aside>

- **System and Organization Controls (SOC) :** A suite of reports produced during an audit which is used by service organizations to issue validated reports of internal controls over those information systems to the users of those services.
    - **SOC 2 -** Trust Services Criteria.
    - **Type II -** Addresses the operational effectiveness of the specified controls over a period of time (usually 9-12 months).
- **Cloud Security Alliance’s Cloud Control Matrix :** Designed to provide fundamental security principles to guide cloud vendors and to assist prospective cloud customers in accessing the overall security risk of a cloud provider.
- **Cloud Security Alliance’s Reference Architecture :** A methodology and a set of tools that enable security architects, enterprise architects and risk management professionals to leverage a common set of solutions that fulfill their common needs to be able to assess where their internal IT and their cloud providers are in terms of security capabilities and to plan a roadmap to meet the security needs of their business.