
# Cloud computing

You can use a computer locally ("on-prem") or, with the power of the [internet](networks-cs.md), you can use it remotely.

If you use it remotely, your information is remotely accessible, or in the "cloud".

The simplest method of cloud storage involves simply synchronizing [files](computers-files.md). This can be one-way or both ways, and can be periodic or constant. Most cloud services (e.g.,Dropbox, OneDrive) are both ways and constant, since it's *darn* convenient across multiple computers.

For redundant storage with important computer files, it's a generally good idea to have "network-attached storage" (NAS), which typically keeps a backup of whatever is stored locally. It also can help to have "snapshots" of various points in the past, just in case there was a detected deletion that synchronized back to the NAS.

Further, cloud storage can be as-needed, where all the files are displayed for access but require download to properly use. This compromise saves local storage space while allowing full access to whatever is needed, presuming an [internet connection](networks-cs.md). For space reasons, most mobile device storage apps use this, but most desktop computer apps don't use it as of 2021 except OneDrive.

One of the most thorough and straightforward ways to remotely access apps and storage in a cloud environment is through a "virtual desktop environment" (VDI). To the user, it looks like a locally hosted [OS](computers-os.md), but is actually using an advanced form of a remote desktop [protocol](standards-computers.md) to access a [virtual machine](computers-distsys-vm.md).
