
# How permissions work

User account management is likely the most common and tedious part of [infosec](cs-infosec.md), but it's critical for the purpose of reliable [authentication](cs-infosec-authentication.md).

Users are defined by User and Group Identifiers (UIDs/GIDs), which are enumerated references to accounts. There used to only be 16-bit values (0-65535), but the identifiers are now 64 bits.

Beyond the UID, there's also a primary GID, which is only for that user alone. For simplicity, the default setting on many systems is for the UID and GID to be the same.

Above everything inside a computer is the superuser, or root, or system administrator, with UID 0. That account has unlimited access and control over the systems, including other users.

Beyond the user accounts, there are system accounts for programs to use:

- The UIDs are usually 1-99 or 500-100.
- They either have *no* dedicated userspace directory or the directory isn't under a standard userspace path.
- With rare exceptions, there's no valid login shell.
- Service accounts are typically made when services are installed and configured, and are mostly the same thing, but usually have a UID/GID over 1000.

While users are the conventional and common model for permissions, a few OS designs (e.g., Fuchsia) uses a capability-based concept for permissions.

- This means that instead of users holding a pile of permissions (e.g., user "bob" can read/write a file), it's built on capabilities defining those permissions (e.g., role "web browser" can read/write a file).

As far as how it's handled, data has various forms of classifications:

- First, it has a classification of severity:
  - Sensitive: highest classification, could damage the institution
  - Confidential: it might damage the institution
  - Private: the users could be damaged
  - Public: no risk of harm if it's used
- Further, the data's state has a classification as well:
  - Data in transit: the nature of it while transferring
  - Data at rest: the nature of it while being stored
  - Data in use: the data being actively processed
    - There really isn't much to protect data at this point

## Access control models

There are different models for managing access:

- Discretionary Access Control (DAC): give access according to the context (the default when there's no official policy)
- Role-Based Access Control (RBAC): define roles to designate controls
  - This is very effective in large organizations because it's just a matter of assigning roles once it's set up.
  - However, it takes some work to set up at the beginning, and any mistakes can create a *lot* of issues.
- Attribute-Based Access Control (ABAC): define qualities to designate controls
  - This is RBAC, but with specific contexts added
- Rule-Based Access Control (RuBAC): designate rules for controls
- Context-Based Access Control (RBAC): uses various contexts for controls
