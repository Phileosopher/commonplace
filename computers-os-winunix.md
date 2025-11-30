
# Windows vs. Unix

Even though the interface of Linux *can* look quite a bit like Windows (especially with distros like [Zorin OS](https://zorin.com)), there are many differences under the hood between the operating systems.

## Portability

Windows 10 takes about 30-60 GB of storage space, while Linux takes <1-20 GB of storage space depending on the distro.

Windows has a recovery drive that only installs a licensed copy on a motherboard that came from the manufacturer with Windows (and used to be an installation CD). Linux has a fully-functional OS that runs from a flash drive and can install itself to local storage.

## Case-sensitive

The files and commands in Linux are case-sensitive, while Windows isn't:

- In Windows, "FileNaMe.txT" and "filename.txt" are the same, but Linux treats those differently.

## Licensing

While Windows is a completely proprietary license, Linux is free.

This can be a dramatically different situation when you go [large-scale](computers-distsys-enterprise.md), but the entire file system reflects that distinction.

## Organization

Windows labels the hard drive as C: (going way back to when the A: and B: drives were floppy disk drives), and labels subsequent drives (like CD drives or flash drives) as D:, E:, etc. Linux, on the other hand, puts all the drives under the /dev folder.

Windows' folder organization is pretty straightforward:

- C:\Windows contains all the Windows-specific system files.
- C:\Program Files is where all the programs live, with Program Files (x86) for all the older programs.
- C:\Users has all the user-based data, such as documents and many settings.

On the other hand, Linux' file system is based on the logical flow of the software developer who wrote the code, with many files and folders sitting everywhere in the folder tree for a variety of purposes.

- /bin is the essential "binaries" for user commands (bash, cat, chmod, ping, echo, etc.).
- /sbin are essential system binaries (fdisk, fsck, getty, halt, etc.).
- /etc has system configuration files (fonts, hosts, services, timezone, machine-id, etc.).
- /usr is read-only, with both data and binaries.
  - /usr/bin has most user commands.
  - /usr/include has code files for the C language.
  - /usr/lib has obj, bin, and lib files for coding and packages.
  - /usr/local has local software (context-depending).
  - /usr/share has unchanging data that everything uses.
    - /usr/share/man has manual pages.
- /var has variable data files.
  - /var/cache has "cached" program data.
  - /var/lib has data that gets modified when programs are run.
  - /var/lock has "lock files" that track resources getting used.
  - /var/log has "log files".
  - /var/opt has variable data for installed "packages".
  - /var/spool has tasks waiting to get processed (/var/spool/cron, /var/spool/cups, /var/spool/mail).
  - /var/tmp has temporary files saved between reboots.
- /home is often organized separately (such as a separate drive partition or drive) and tends to have user data.
- Others:
  - /lib has libraries and kernel modules.
  - /mnt has mount files for temporary file systems.
  - /opt has optional software applications.
  - /proc has process/kernel information files.
  - /root is the home directory for the "root user".

## Versions

Windows has very clear-cut versions:

- Windows 7
- Windows 8
- Windows 8.1
- Windows 10
- Windows 11

There are other types of Windows OS (such as Windows NT), but it's relatively straightforward, with permutations and updates coming as Service Packs (e.g., SP1) or standard [versioning numbers](computers-software-versionctrl.md).

Linux, on the other hand, has [a variety of distros](computers-os-unix.md) that each serve specific roles, and the kernel version is the only thing that advances sequentially, with each distro having their own [versioning](computers-software-versionctrl.md).

Nothing really binds Linux distros together as the same OS very much until you get down to the kernel (though different versions of the same distro have quite a bit in common), whereas Windows versions are predictably interoperable, with the OS making most software at least *somewhat* backwards-compatible.

## Programs

Getting a new Windows program is a specific process:

1. Have the installation media, or download the .exe/msi file from the website directly.
2. Run the installation program, which Windows will unpack.
   - If it's a portable program, you can simply run it as-is.
3. You can now use the program at your leisure.
4. If you need to update, download the new version and install, which will be a complete rewrite of the old program.

The upside is that it's easy to understand for downloading. The downside is that updates (such as [security updates](computers-cysec.md)) require the user to pay attention unless it's specifically a Microsoft-supported product (like Microsoft Office).

The best way to get a Linux program is a little more involved at the beginning:

1. Search for the software inside the package manager, which varies on the distro, and you can download any that you want.
   - You can download any package manager you want, if that package manager isn't to your liking (e.g., APKPure instead of Google Play Store)
   - Alternately, if you know the name of the program, you can simply run "sudo [PackageManagerName] install" from a [terminal](computers-cli.md).
   - If the software isn't there, install the relevant software repositories you need.
2. You can now use the program at your leisure.
3. If you need to update, run "sudo [PackageManagerName] update". To upgrade to the next [version](computers-software-versionctrl.md) (e.g., 1.7 to 1.8), run "sudo [PackageManagerName] upgrade". This will only update the relevant files that need updating.

While Linux is more work to get the dependencies set up, it's safer because security updates are rolled out as part of the update process.

As far as backwards compatibility goes, Linux is almost always prepared to run old software, while Windows often requires some workarounds. Ironically, Mac often simply doesn't run older software.

## Linux tips

As of this writing, Windows still dominates the majority of the PC market. Here are a few tips to avoid making awful mistakes while using Linux:

- If there's any stock software the OS came with (such as a [file manager](computers-files.md) or software-based [keyboard](computers-keyboard.md)), *do not uninstall it*. If you want something new, simply install the new one and use it.
- Don't bother trying to run a common Windows-based software that has a Linux alternative (e.g., Microsoft Office). You *can* use the Windows emulator (called "Wine"), but you'll usually have a better time with a Linux-based alternative if the software is even remotely popular.
- Most of the Linux-based [UI](engineering-design.md) lacks polish, but does the job relatively well. You'll find much more satisfaction if you observe the features those things have that proprietary software *doesn't* have.
- Websearch frequently what you don't know. Your lack of knowledge isn't new, and there's usually an answer somewhere about it.

Most "original equipment manufacturers" (OEMs) that come with [Windows](computers-os-windows.md) do *not* consider that you'd want to install Linux or dual-boot. Usually, you'll first need to find a way into the BIOS, then boot from a USB drive. If you're dual-booting, you may need to select your OS from the boot menu *every time*.
