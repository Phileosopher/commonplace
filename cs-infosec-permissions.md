
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
