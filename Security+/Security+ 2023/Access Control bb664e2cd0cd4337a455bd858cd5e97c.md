# Access Control

### Introduction

- Methods used to secure data and information by verifying a user has permissions to read, write, delete or otherwise modify it.

### Access Control Models

- **DAC (Discretionary Access Control) :** The access control policy is determined by the owner.
    - DAC is commonly used.
- **MAC (Mandatory Access Control) :** The access control policy is determined by the computer system.
    - MAC relies on security labels being assigned to every user (called a subject) and every file/folder/device or network connection (called an object).
    - Data labels creates trust levels for all subjects and objects.
- **RBAC (Role Based Access Control) :** An access model that is controlled by the system (like MAC) but utilized a set of data label to define the permission level.
    - Power Users is a role-based permission.
- **ABAC (Attribute-Based Access Control) :** An access model that is dynamic and context-aware using IF-THEN statements.

### Best Practices

- The access control policy is determined by the owner.
- **Implicit Deny :** All access to a resource should be denied by default and only be allowed when explicitly stated.
- **Explicit Deny :** Everything is allowed until you deny it.
- **Least Privilege** : Users are only given the lowest level of access needed to perform their job functions.
- **Separations of Duties** : Requires more than one person to conduct a sensitive task or operation.
    - Separation of duties can be implemented by a single user with a user and admin account.
- **Job Rotation** : Occurs when users are cycled through various jobs to learn the overall operations better, reduce their boredom, enhance their skill level, and most importantly, increase our security.

### Users and groups

- Computers can have multiple users and groups.
- **User Rights :** Permissions assigned to a given user.
- **Groups :** Collection of users based on common attributes (generally work roles).
- Permissions are broken down into read, write and execute in Linux.
- **Privilege Creep** : Occurs when a user get a additional permission over time as they rotate through different positions or roles.
- **User Access Recertification :** Process where each user’s rights and permissions are revalidated to ensure they are correct.

### Permissions

- **Permission Inheritance** : Permissions are inherited by default from the parent when a new folder is created.
    - Any permission added/removed from the parent folder will pass to the child by default too.
- **Propagation** : Occurs when permissions are passed to a subfolder from the parent through inheritance.

### User account Control

- **User Account Control (UAC) :** A security component in windows that keeps every user in standard user mode instead of acting like an administrative user.