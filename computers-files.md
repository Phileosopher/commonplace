
# What computer files are

Computer commands *could* distill down as [binary information](logic-cs.md) (and, in practice, you always *can* examine them inside [memory registers](computers-memory.md)) but that's absolutely tedious and difficult when you want to actually do something that *isn't* computer science.

So, instead of looking at information as a big long string of information, engineers grouped the computer's instructions into logical, clearly marked files.

From a logical standpoint, absolutely *everything* on a computer is abstracted as a type of file. This includes things that aren't technically files, such as tasks, programs, and external media like CDs.

Computer files can store just about anything:

- Instructions for how the [CPU](computers-cpu.md) will work with various inputs or outputs (also called a "driver").
- Instructions for routine things the [operating system](computers-os.md) must do frequently (like "refresh" the screen or check for new USB cables, also called a "process").
- Sets of instructions the user can choose to run that typically work with other files (also called a "program").
- Outputted logs ("log files") about how and when a computer did something or failed at it.
- Files the user actually saved themselves (like a text file or photo).
- Collections of any of the above (e.g., a CD disk image, a ZIP file).

Often, a file isn't exclusively one of the above:

- Files often contain instructions to make new files (such as installation programs).
- Some files are temporary and discarded after they're used.
- Most modern computer programs are collections of files that work back-and-forth between getting written to, then being read.

The category of whether a file is in "userland" or "system" isn't so clear, either. Accessing a log file, for example, is a bit of both.

When you first [boot](computers-boot.md) any computer, a few files are already running:

- Input file (stdin) - tracks what you're doing with the [keyboard](computers-keyboard.md) (and occasionally the [mouse](computers-mouse.md)).
- Output file (stdout) - feeds information to the [screen](engineering-screen.md)/[printer](engineering-printers.md)/[speakers](computers-speakersmic.md).
- Error file (stderr) - a database of [errors](computers-software-redesign.md) with reference codes that specify how things broke.

To make managing files easier at first glance, most files have a "header" with "metadata" about the file, such as the file type, file size, date last accessed, and date created.

A file can hold a *lot* of metadata, but not all metadata about that file is stored *inside* the file. It can often be contained in the operating system instead inside a [data structure](data-structures.md) (on Windows it's the master file table or MFT and Linux uses inodes).

File metadata often varies based on the file system, but it usually has at least most of the following:

- File [permissions](computers-cysec.md), as well as the file's owner, and "access control lists/entries" that indicate which users can do what (i.e., write/read/rename/delete)
- "Timestamps" for when it was created, when it was last accessed, and when the *metadata* was last changed
- Extended attribute metadata that may not comply with any preset standards
- Alternate data streams and forks, where the file can hold multiple different versions of mostly similar information
- Checksums/ECC that verify when transferring the information that it was safely copied

Depending on the file, metadata might be spread around the file, but it makes the most sense to keep metadata grouped where it will likely be used first (i.e., at the front).

Files can also contain all sorts of multimedia, and it can get a bit complicated. Most codecs for [music files](computers-speakersmic.md), for example, don't usually contain *only* music. An MP3, for example, will have plenty of text data about the performer, [licensing/copyright](legal-ip.md) information, song lyrics, and album photos. For [memory allocation](computers-programming.md) reasons of all the *possible* metadata, this can *really* pad out file sizes.

It's worth noting that there are often specific rules about what characters work in file names. All the alphabet is allowed, along with some special characters like commas, periods, and spaces. However, [regular expression](computers-programming.md) elements like "?" and "/" aren't allowed.

On older systems, using periods and spaces can *really* mess up a system, and on an unknown distributed system you don't always know how old everything is. Therefore, it's typically a good idea to get into the habit of using "_" instead of " ".

## File attributes

Most files have an extension that (usually) is an acronym that indicates what they are:

- text.txt
- MicrosoftWordDocument.doc
- OpenDocumentText.odt
- MicrosoftExcelDocument.xls
- OpenDocumentSpreadsheet.ods
- MPEG-1_or_MPEG-2_Audio_Layer_III.mp3
- Microsoft_Software_Installer.msi
- Executable_File.exe
- tarballfile_GZip.tar.gz

Some operating systems hide the known extensions, but you can typically rename the files to work with them differently (though it may not be encoded correctly anymore).

A file can be marked as read-only. This means the computer won't change the contents of the file until it's marked for writing into as wel.

To make file management safer for the non-tech user, files can be demarcated as hidden. This tells the file manager to not display them visually, though a savvy user can enable them at any time. Most core system files are marked as hidden or, sometimes, as a system file (i.e., SUPER-hidden).

Since [cloud storage](computers-distsys-cloud.md) became popular, some files can be labeled as a network resource instead of as a local one. While this can be profoundly convenient, it can confuse users who don't realize their files are *not* stored locally.

Depending on the location of the file, it isn't really in only 1 location on a disk. To manage an unknown amount of space, files tend to get stored more abstractly as multiple "blocks" whenever that file exceeds 1 block size:

- Block 1 - File 1 part a
- Block 2 - File 1 part b
- Block 3 - File 2
- Block 4 - File 1 part c

In the case above, File 1 is "fragmented" because not all the blocks are together.

- At one time, software such as Disk Defragmenter on [Windows](computers-os-windows.md) would defragment.
- [Linux](computers-os-unix.md) computers sidestepped this issue by placing the files at comparatively large distances from each other.
- Now, many [algorithms](computers-programming-algorithms.md) can predict fragmentation before it happens and accommodate it by either moving around blocks or writing to a different part of the disk.

Blocks can be any variety of [two-based](logic-cs.md) sizes, ranging from a few kilobytes upwards to multiple megabytes. These blocks may have certain abilities depending on the file system:

- Internal snapshotting/branching - maintaining multiple copies of that block
- [Encryption](encryption.md) and compression
- Deduplication - getting rid of duplicates, which can save money in [enterprise systems](computers-distsys-enterprise.md)
- Checksums/ECC that verify the block is safely encoded

Blocks, however, are a *further* abstraction from a different grouping called "sectors":

- Every block is usually made of more than one sector.
- However, except for a hardware problem with the disk, the operating system doesn't tend to work with sectors.

Most files don't *exactly* conform to block size, so there's almost always a block at the end of the file with some free space. For that reason, the size of the file is always a little smaller than the size of the disk space it occupies. In the case of many files, it can be a significant amount.

The blocks are assembled by the file system into larger [data structures](data-structures.md) called block groups, which can group indefinitely farther into even more elaborate structures. By using data structures instead of keeping it more straightforward, it cuts down on how much the CPU has to race back-and-forth across the memory system (and, naturally, extends the longevity of the media).

The file system may also have certain additional features for block management:

- Sparse files - the operating system organizes the blocks to be more efficient
- Block suballocation - uses empty disk space at the end of blocks to more efficiently use space, this often uses "read ahead" features to work correctly
- Extent - reserved space for future file writing
  - Preallocation - reserving space before it's actually needed
  - Delayed allocation - wait until the entire set of data to be written has accumulated, then make the best use of large and small files to fill in the blocks
  - Allocate-on-flush - re-allocating memory that was *not* used for future file writing only when that memory is actually needed
- Variable file block size - for managing multiple block sizes on one system
- Trim support - in [solid-state drives](computers-memory.md), writes all the unused data to 0 to prolong the life of the drive

Because of the way [algorithms](computers-programming-algorithms.md) write blocks, you can save a *lot* of disk space if you group similar information together *before* compressing it for archiving. This can heavily affect [compiling sizes](computers-programming.md) as well.

## File systems

There are three abstraction layers for file systems:

1. Physical file systems - the actual data stored on the disk, which involves device drivers managing partitions.
2. Virtual file systems - since not all file systems are the same, there needs to be a unified cross-platform connection that naturally translates across those various systems, which involves file system drivers to manage this interchange.
3. Logical file systems - A user-facing part of the file system, which involves simplifying the information down to things like EXECUTE, READ, WRITE, and DELETE for the upper layers.

File systems exist within various [standards](standards-computers.md), most of them based on the type of [operating system](computers-os.md) the computer uses. Some older file systems (e.g., FAT, FAT32) had a bad tendency to randomly lose data, and there are various file system features meant to make files safer and faster:

- Hard links - essentially, a fixed directory name for the file, most files *need* at least one of these.
- Symbolic links - aka symlinks, a representational name for a file located elsewhere that ends up saying "see [ACTUAL MEMORY LOCATION]".
- Journaling - keeping a record file in long-term memory of tasks the CPU still has to do, very useful if the task is interrupted and can't continue, can sometimes *only* journal the metadata, a critical part of [cybersecurity](computers-cysec.md).
- File change log - keeps a record of many changes to various files, can be localized to system files or apply to *all* files.
- Case-sensitivity - Some operating systems (like [Unix-based ones](computers-os-unix.md)) are case-sensitive ("file.txt" *isn't* "File.txt"), while others (like [Windows](computers-os-windows.md)) are not ("file.txt" is the same as "FiLe.TXt"). Occasionally, a case-insensitive file system will still *preserve* the case-sensitivity.
- XIP - execute in place, where a CPU can load a file directly from long-term storage instead of migrating it to RAM first.

Older file systems had a 4 GB limit, but newer ones have a 16 EB (1000 TB) limit.

As of the early 2020s the best general all-purpose cross-platform standard is exFAT, since it was made by and works well with Microsoft (as opposed to NTFS), but is cross-compatible with all other devices, though Linux's ext4 standard has value as well.

Logical file systems fit squarely in the domain of [good UX](engineering-design.md), and getting rid of them to allow text-based entry and output is why [CLI](computers-cli.md) is still fashionable for tech-savvy users.

## Hierarchical files

Naturally, a gigantic list of files can get *really* unwieldy, especially when 3 programs use the same file name, or when you want to separate system files and files you're working on.

To accommodate this, the most popular way to group files is with a "hierarchical file system". Like it sounds, hierarchical file systems put files inside imaginary boxes called "folders" which can indefinitely box inside other folders to create a hierarchy. Here's an example:

- \Users\Default\AppData\Local\Microsoft\Windows\WinX\Group1\file.txt

There are various hierarchical file systems ("exFat, ext2/3/4, jfs, gpfs etc.) which are each designed with different purposes in mind. The file system rules (and where to start the operating system's first programs) are stored in the [boot sector](computers-boot.md).

Another convenience of a hierarchical file system is that "moving" a file on the same disk is simply renaming the file path, which may mean changing a few [memory references](computers-memory.md) depending on the design of the hardware. This is why a drag-and-drop transfer can sometimes be instant. This, however, creates a [UX hangup](engineering-design.md) when moving across disks, since lots of data will take a while to transfer.

It's worth being aware of what a file is doing when you're copying, moving, and deleting:

- When you delete a file, the file is still there, but it gets marked for overwriting whenever the operating system needs more storage. Unless you actively use deletion software, [it'll still be there](computers-cysec-compliance.md) if the operating system never overwrites it.
- If you're copying a file *anywhere*, it's duplicating the code.
- If you're moving a file to the same drive, it's changing some references (and, depending on partitioning, copying and marking the code for deletion).
- If you're moving a file to a different drive, it's duplicating the code and then marking the original for deletion.
- Drag-and-drop with the mouse could mean *either* moving or copying depending on the [operating system](computers-os.md) and where it's going, so it's better to use the cut or copy keyboard shortcut and then the paste shortcut.

However, there are some limits to hierarchical files based on how many bits were allocated to the task. At one point, [memory](computers-memory.md) limits had a hard 256-character limit on the file. While this sounds like a lot, that character limit included the *folders* as part of that file name.

- C:\Users\Oh Boy My Grandson Got Me A Computer Hi Computer\Documents\Pictures\That one time when the boys took me and Aunt Gertrude to Disney World, this was right after my Morty passed\Splash Mountain 23 after the nice attendant helped me in but fell in.jp[ERROR]
- This gets worse if you're dealing with [cloud storage](computers-distsys-cloud.md) and [distributed systems](computers-distsys.md), and *especially* with [virtual machines](computers-distsys-vm.md).

## Database file systems

There's a less-frequent but important alternative file system that uses a [database](database.md) instead. However, while it could possibly *not* be hierarchical, it's essentially a top-level management system attached to a standard file system.

Most music players will use a database file system, and it allows easy navigation and sorting. But, it comes at the cost of versatility, so it doesn't work as a base-level OS file system.

## Partitions

Beyond the [boot sector](computers-boot.md), drives have "partitions" assigned for various purposes:

- Operating system partition - the main partition that holds all the information to run the computer.
- User data partition - optional storage for the user's data.
- Swap partition - optional extra memory allocated for when the RAM gets too full.
- Recovery partition - optional backup for restoring known-good system files.

Except for some forms of [virtualization](computers-distsys-vm.md), it's only sane to keep up to 1 operating system on 1 partition "volume". This evenly divides the tasks of an operating system in such a way that there's no conflict for what the CPU should do.

Volume management in [large-scale systems](computers-distsys.md) can become challenging. It can help to use a native logical volume management file system (e.g., LVM-ext4, Btrfs), or it can be done higher up in the [OS stack](computers-os.md) via [virtualization](computers-distsys-vm.md).

Partitions are grouped based on the operating system.

- In [Windows-based](computers-os-windows.md) systems, partitions are given arbitrary letters (C: as the first one because A: and B: were once for floppy disks, D:, E:, etc.).
- In [Unix-based](computers-os-unix.md) systems, they're grouped under specific folders (and accessible with the "df -h" command).
- They can be "mounted" automatically, or at the user's discretion.
- Further, partitions can be assigned to pretty much any folder the user wishes.

## Programs

Programs are specific types of files. They are special because they predominantly contain code meant to be "executed" by an operating system (hence the term "executable file"). Most programs need to be compiled from their original syntax, but some don't need compiling.

You can open any file in a text editor, though the parsing of the language may make it look weird, and the operating system may forbid opening certain files and output an error.
