
# Windows vs. Unix

Even though the interface of Linux *can* look quite a bit like Windows (especially with distros like [Zorin OS](https://zorin.com)), there are many differences under the hood between the operating systems.

## Portability and licensing

Windows 10 takes about 30-60 GB of storage space depending on God knows what, while Linux takes <1-20 GB of storage space depending on the distro.

Windows has a recovery drive that only installs a licensed copy on a motherboard that came from the manufacturer with Windows (and used to be an installation CD). Linux has a fully-functional OS that runs from a flash drive and can install itself to local storage.

To install Windows on an unlicensed system, it either requires a cracked or restricted version of Windows. By contrast, Linux runs everywhere.

Most of the time, a Linux config can be reduced to makefiles and dotfiles. By contrast, a Windows config often requires a pile of .exe files and documentation about any specific configurations.

As far as processing requirements, Linux can run on a potato (maybe literally), while Windows needs a modern computer.

## Security

Windows uses a microkernel arrangement, so security has a lot to do with how secure each application is.

By contrast, Linux is a monolithic kernel, where the kernel is heavily scrutinized by many developers.

Overall, Linux is therefore more secure, but the people who run Linux are also relatively more tech-savvy, making it more secure in that sense as well.

## Files and case-sensitivity

The kernel in Windows interprets what the file is based on the file extension. By contrast, Unix-likes ignore the file extension and look at the content and permissions to determine how to work with it.

The files and commands in Linux are case-sensitive, while Windows isn't:

- In Windows, "FileNaMe.txT" and "filename.txt" are the same, but Linux treats those differently.

## Licensing

While Windows is a completely proprietary license, Linux is free.

This can be a dramatically different situation when you go [large-scale](cs-distsys-enterprise.md), but the entire file system reflects that distinction.

## Organization

Windows labels the hard drive as C: (going way back to when the A: and B: drives were floppy disk drives), and labels subsequent drives (like CD drives or flash drives) as D:, E:, etc. Linux, on the other hand, puts all the drives under the /dev folder.

Windows' folder organization is pretty straightforward:

- C:\Windows contains all the Windows-specific system files.
- C:\Program Files is where all the programs live, with Program Files (x86) for all the older programs.
- C:\Users has all the user-based data, such as documents and many settings.

On the other hand, [Linux' file system](cs-os-unix.md) is based on the logical flow of the software developer who wrote the code, with many files and folders sitting everywhere in the folder tree for a variety of purposes.

## Versions

Windows has very clear-cut versions:

- Windows 7
- Windows 8
- Windows 8.1
- Windows 10
- Windows 11

There are other types of Windows OS (such as Windows NT), but it's relatively straightforward, with permutations and updates coming as Service Packs (e.g., SP1) or standard [versioning numbers](cs-software-versionctrl.md).

Linux, on the other hand, has [a variety of distros](cs-os-unix-distros.md) that each serve specific roles, and the kernel version is the only thing that advances sequentially, with each distro having their own [versioning system](cs-software-versionctrl.md).

Nothing really binds Linux distros together as the same OS very much except the kernel (though different versions of the same distro have quite a bit in common), whereas Windows versions are predictably interoperable, with the OS making most software at least *somewhat* backwards-compatible.

## Software and updates

While the distro may vary, the pre-installed tools for Windows are inferior to Linux's initial setup. There are also many more options available for Linux.

Getting a new Windows program is a specific process:

1. Have the installation media, or download the .exe/msi file from the website directly.
2. Run the installation program, which Windows will unpack.
   - If it's a portable program, you can simply run it as-is.
3. You can now use the program at your leisure.
4. If you need to update, download the new version and install, which will be a complete rewrite of the old program.

The upside is that it's easy to understand for downloading. The downside is that updates (such as [security updates](cs-infosec.md)) require the user to pay attention unless it's specifically a Microsoft-supported product (like Microsoft Office).

The best way to get a Linux program is a little more involved at the beginning:

1. Search for the software inside the package manager, which varies on the distro, and you can download any that you want.
   - You can download any package manager you want, if that package manager isn't to your liking (e.g., APKPure instead of Google Play Store)
   - Alternately, if you know the name of the program, you can simply run "sudo [PackageManagerName] install" from a [terminal](cs-cli.md).
   - If the software isn't there, install the relevant software repositories you need.
2. You can now use the program at your leisure.
3. If you need to update, run "sudo [PackageManagerName] update". To upgrade to the next [version](cs-software-versionctrl.md) (e.g., 1.7 to 1.8), run "sudo [PackageManagerName] upgrade". This will only update the relevant files that need updating.

While Linux is more work to get the dependencies set up, it's safer because security updates are rolled out as part of the update process.

As far as backwards compatibility goes, Linux is almost always prepared to run old software, while Windows often requires some workarounds. Ironically, Mac often simply doesn't run older software.

## Privacy

While some distros do track users, Windows *always* tracks user data.

Linux also gives the option to observe everything that happens in the system, while Windows' services and network calls are often opaque.

## Optimization

Windows' task automation usually involves downloading software or, in a more advanced capacity, programming in [VB.NET](cs-langs-specific-basic.md) or [C#](cs-langs-specific-c#.md).

By contrast, almost everything in Linux works with shell scripts, especially [bash](cs-cli-specific-bash.md).

The GUI is also more customizable in Linux, with the ability to swap out any desktop environment you prefer. Windows requires third-party apps to force the changes you want.

This compounds at scale, and most Windows experiences involve lots of clicking, while most Linux experiences involve dropping to [terminals](cs-cli.md).

## Other general tips

Here are a few tips to avoid making awful mistakes while using Linux:

- If there's any stock software the OS came with (such as a [file manager](cs-files.md) or software-based [keyboard](cs-keyboard.md)), *do not uninstall it*. If you want something new, simply install the new one and use it.
- Don't bother trying to run a common Windows-based software that has a Linux alternative (e.g., Microsoft Office). You *can* use the Windows-based interface (called "Wine"), but you'll usually have a better time with a Linux-based alternative if the software is even remotely popular.
- Most of the Linux-based [UI](engineering-design.md) lacks polish, but does the job relatively well. You'll find much more satisfaction if you observe the features those things have that proprietary software *doesn't* have.
- Websearch frequently what you don't know. Your lack of knowledge isn't new, and there's usually an answer somewhere about it, and Linux gives legitimately meaningful error messages.

Most "original equipment manufacturers" (OEMs) that come with [Windows](cs-os-windows.md) do *not* consider that you'd want to install Linux or dual-boot.

- Usually, you'll first need to find a way into the BIOS, disable Secure Boot, then boot from a USB drive.
  - Microsoft has been very slow and ineffective at supporting Linux on their hardware, so their Secure Boot and Trusted Platform Module (TPM) false-positives Linux as malware.
- If you're dual-booting, you may need to select your OS from the boot menu *every time*.
- It's usually GRUB, since UEFI bootloaders are locked-down by Microsoft.
  - Ironically, the alleged security that comes with UEFI is *not* as reliable as Microsoft or Intel claim.

Dual-booting is *very* cool because it's the best of both worlds, but it comes with downsides and risks:

- You need to be sure you have enough [long-term storage](cs-memory.md) to hold both OS distros, along with room for applications.
  - Since the drives are using different journaling systems (NTFS vs ext4 usually), the user files may not be accessible from both OS.
- Linux bootloaders are intelligent enough to detect Windows, but Windows is *not* programmed to track a Linux partition. For that reason, install Linux *after* Windows to ensure they're both accessible.
- The [time](standards-datetime.md) between Linux and Windows is fiddly.
  - Essentially, the CMOS battery tracks the hardware time, and the OS takes that time when it boots and makes it the system time.
  - The computer time [standard](cs-standards.md) uses UTC, then offsets it for the time zone (e.g., UTC -7:00).
  - Windows assumes the hardware time is already offset, while Linux assumes the time is UTC.
  - This means that, depending on how the systems are configured, you will frequently see one of the OS offset by that much time.
  - The answer is to manually configure the system to pull the time from the internet or to reconfigure either Windows or Linux to not adjust the time.
  - This would normally be a minor annoyance, but can dramatically affect [authentication](cs-infosec-authentication.md) if the certificate requires a timestamp and [cloud synchronization](cs-distsys-cloud.md) by overwriting more recent files with older ones.
