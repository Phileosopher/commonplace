
# The features of a Unix-based OS, moving upward

[All operating systems have similar features](cs-os.md), but Unix-style architecture has some unique distinctions.

To accommodate the monolithic kernel's design, Linux uses preemptive multitasking, which allocates a specific amount of time to each task before giving another task a chance. This prevents one task from dominating and ultimately freezing the computer if it was badly programmed.

Beyond this, to add functionality, there must be a package manager:

- Debian family installs .deb files with dpkg, or apt (advanced package tool) for higher-level work.
- RHEL family installs .rpm packages with rpm (formerly yum).
- openSUSE family uses YaST with the zypper [CLI](cs-cli.md) to unpack it.
- Arch family uses pacman, which is designed for extreme update micromanagement.

## Superuser

Many of the instructions online will have "$" or "#" at the beginning of the command.

- Don't enter it, since "#" means simply running the command and "$" means running it as "sudo"

You will frequently need to enter sudo at the beginning of any system process.

- This is "superuser do", and requires you enter your password to authenticate [the highest permission possible on the computer](cs-infosec-authentication.md).

## Filesystems

Unix abides by the Filesystem Hierarchy Standard (FHS), which indicates various file conditions (e.g., static vs variable, whether it can be reproduced across a [network](cs-networks.md))

To [encrypt](encryption.md) a device, Linux uses Linux Unified Key Setup (LUKS) to run dm-crypt, which is part of the kernel itself.

There isn't one singular way to manage files, either. Hard links are representational as the canon, non-negotiable link and therefore must exist on the same file system. Symbolic links (or "symlinks") are simply referring to another file by name.

## Package manager

There are a few mainstream package managers to choose from, though like everything else in Linux there's a bazillion alternatives:

- Debian's, with deb files
- YUM/RPM (for RHEL package manager), with rpm files
- Pacman, which uses tar.gz files

## Desktop environment

Due to the [open-source nature](legal-ip-floss.md) of Linux, there are *many* desktop environments, with their own "opinionated" way of doing things:

- GNOME is the most common and borrows heavily from the Mac, with the GTK toolkit written in [C](cs-langs-specific-c.md). However, many people have had issues with it since it focused on mobile-first and used the Unity design.
- KDE is also common and uses the Qt library, written in [C++](cs-langs-specific-cpp.md) borrows from Windows, though it's far more "modular" than Windows ever was.

### What the user actually wants

The applications available on Linux are manifold, especially in a well-supported desktop environment.

- With the exception of some [Big Tech software](cs-bigtech.md) like Microsoft Word or Apple Safari, most things have supported packages on Linux these days.
- Even when that software *isn't* available, there are usually at least a few equivalent [FLOSS](legal-ip-floss.md) alternatives with a different name.
