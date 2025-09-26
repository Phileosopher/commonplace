
# How a computer boots itself up

NOTE: To get hands-on with the BIOS, pressing manufacturer-contextual Esc/F2/F10 repeatedly while the computer is starting will typically bring you to the interface for the BIOS of most computers. Sometimes it's a different key, but there's always something to get you there.

Computers have evolved over the years to the point that an [operating system](computers-os.md) is a standard feature. But, before the operating system even starts, there are a few elements that must activate first:

1. Power goes to the motherboard.
2. The motherboard performs a power-on self test (POST).
3. Load the "firmware", which is called a BIOS (basic input-output system) in older computers. This is a *very* basic fully-functioning operating system designed to let tech-savvy users manage the rudimentary elements of the computer.
4. Identify the boot device. This was once a floppy disk that had the [operating system](computers-os.md) directly on it to load to RAM before swapping to other programs, but is now typically a hard drive (or sometimes a supplementary flash drive).
5. The BIOS checks the beginning of the disk for MBR code ("master boot record").
6. The MBR loads code from the boot sector of the active partition.
7. The boot sector of the partition loads code that starts the [operating system](computers-os.md) itself.

In that context, older hard drives had a relatively straightforward arrangement:

1. An MBR is at the beginning of the drive that describes what's on the drive, a bit like a Table of Contents in a book.
2. Primary partitions, which can hold an operating system, and can only be up to 2 terabytes in size.
3. Extended partitions, which are an abstraction of *another* drive that serve as a logical drive (i.e., an abstraction) of their own.

An MBR is made of 512 bytes and has several components inside it:

1. 446 bytes of master boot code that gives instructions about what's elsewhere on the disk and how it's [encrypted and encoded](encryption.md).
2. 64 bytes for a "disk partition table", which is a [database](database.md) of primary partitions. Each primary partition is 16 bytes, so you can only have up to 4 per disk without recursively [hacking](hacking.md) the primary/extended partition system.
3. A 2 byte boot signature at the end, which *must* be unique to that disk or the operating system will have a disk signature collision. Disk signature collisions most frequently happen when a disk is completely copied, then mounted on the same device.

It's worth noting that resizing and moving partitions is *not* trivial, as opposed to [virtual drives](computers-distsys-vm.md) that have arbitrarily-set sizes:

- When you want to resize partitions, have a plan for shrinking the size of any partitions you want to free up. The computer takes a long time to do this, and if any process is interrupted the partition will likely be corrupted and the data will be lost.
- To move partitions around, it means manually copying and then deleting partitions. It's a set of long processes that can also lose data.
- If the MBR is ever corrupted, it is *not* easy to rebuild the information in it.

## History

BIOS was around for a long time, so long ago that it was originally written in 16-bit code (the standard for 1981, while 64-bit code became standard by the mid-2000s). It added many extensions, such as ACPI (advanced configuration and power interface), but didn't get upgraded for a *long* time.

In the mid-1990's, Intel designed the new standard of EFI (extended firmware interface) to replace the BIOS with some much-needed improvements to make operating systems more scalable and redundant. However, this wasn't really adopted until there was a Microsoft/AMD/Intel/PC manufacturer agreement with the UEFI (unified extended firmware interface):

1. Power goes to the motherboard.
2. Load the UEFI, which is a BIOS with a better interface and significantly more options.
   - Everything is centralized under the UEFI, whereas the BIOS had various controllers that it only partially interacted with.
3. Load the boot manager into memory and run either an OS loader or the [OS kernel](computers-os.md).

Once UEFI came around, they redesigned how hard drives store information with GPT (GUID partition table), which rebuilt the framework of the drive itself:

1. Protective MBR in LBA 0, which was designed to prevent legacy MBR-based tools from overwriting a GPT-based drive. This usually outputs weird errors when using MBR tools.
2. The primary GPT header in LBA 1 stores the primary GUID partition table header, which creates database code that defines a partition table.
3. Partition entries in LBA 2 through LBA 33
   - each partition entry has the following:
     - The starting memory location of that partition.
     - The size of that partition.
     - A 32-bit cyclic redundancy check (CRC32) [checksum](computers-cysec-authentication.md).
   - While there are 32 entries, there could be more, which makes it a *very* scalable situation, as well as getting rid of the need for extended or logical drives.
4. The partitions themselves in LBA 34 onward.
5. Backup partition entries in LBA -33 through LBA -2, just in case they fail.
6. Backup primary GPT header in LBA -1, just in case it fails.

## GPT vs. MBR

The existence of a backup GPT header and partition entries is the reason why GPT is inherently safer than simply MBR.

At the same time, MBR is on more computers, especially old ones.

Most older operating systems (or ones that use legacy code) will only work on MBR computers. But, newer operating systems are often backwards-compatible.

In practical terms, it really doesn't matter unless you're buying a computer, since it's a motherboard configuration. The advantage of UEFI, though, is that it has CSM (compatibility support module), which makes it backwards-compatible with an MBR system.

Either way, while you can often mess around with the operating system without doing much damage, it's equally easy to brick a computer if you interrupt firmware updates to a BIOS *or* UEFI motherboard.

## Cybersecurity

One interesting aspect is that a BIOS/UEFI is a base-level stripped-down operating system meant for simple tasks. This means that there is a *lot* of legacy [code](computers-software.md) in there, and it's ridiculously slow with respect to clock cycles. If you ever wonder why booting takes a while after you press the power button, it's because the manufacturers don't care to delete the 99% of code that's irrelevant.

This *does* represent a [cybersecurity risk](computers-cysec-pentest.md), which is why UEFI's Secure Boot can sign the boot with a [cryptographic key](encryption.md), and why Windows computers tend to use Trusted Platform Module (TPM). It's possible (and a good idea) to harden Linux computers with Secure Boot.

## Bootloader

There's a very particular difference between a boot loader and a boot manager. A boot loader is selecting a menu of options, while a boot manager allows for other interface decisions (such as a system scan). EFI-based computers simply treat them both as programs, though older BIOS-based systems need boot loaders. The line is blurry, but is important to clarify.

On an MBR disk, there's a gap just after the MBR and before the first system partition. This permits a boot loader to exist in that gap for the user to select a [partition](computers-files.md) (and, naturally, an [operating system](computers-os.md) on it).

However, some boot loaders (like GRUB) load additional boot loaders into that area to allow recursive booting (that is, a bootloader that boots up a bootloader). At *that* point, you'll see an operating system's logo. Without it, the operating system would run without user selection involved based on the MBR boot.

With GPT systems, the first sector is blocked off to error out legacy systems that use it, then use LBA 1 to boot from the primary GPT header. In a Linux system, you can access the EFI system partition (ESP) at /sys/firmware/efi, with the [file](computers-files.md) having a .efi extension.

## Features

Booting isn't always so straightforward. Instead, in an [enterprise](computers-distsys-enterprise.md) situation you can use a remote-access boot command with a pre-boot execution environment (PXE):

1. The computer lets the [DHCP](standards-computers.md) server know that it's doing a PXE boot.
2. The DHCP server sends back the IP address and filename of the boot image.
3. The computer contacts the PXE boot server and asks for it.
4. The PXE server sends the boot image through TFTP.

## File management

The operating system will use a variety of files, which will have different arrangements depending on [how the file system is designed](computers-files.md).
