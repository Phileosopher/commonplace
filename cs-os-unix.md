
# What Unix-likes are

"Linux" is a broad catch-all term to represent a variety of distributions ("distros"). Officially, the term is GNU/Linux because the Linux kernel mixes with GNU.

However, the demarcation between Linux/Windows/Apple isn't precise. Each operating system borrows *heavily* from the others, especially in the domain of [UX](engineering-design.md). In particular, GNU's system expands far into the realm of Windows-based operating systems, so it's not really an exclusive concept as much as [a FLOSS ideal](legal-ip-floss.md).

## History

Unix was an [operating system](cs-os.md) made by AT&T in 1969. However, AT&T was [monpolizing power](politics-monopolies.md) at the time (like [today's Big Tech](cs-bigtech.md)), so antitrust litigation prevented it from entering the computer industry. The company was forced to release the source code for free to anyone who asked. Many educational institutions (such as Berkeley) and businesses used Unix.

Later, once AT&T spun off Bell Labs, Bell was free to sell a proprietary license of Unix in 1984, but the damage to AT&T's potential hold on the market had already been done. Unix's source code was effectively public and legal to use.

In 1983, Richard Stallman created the GNU Project, which aimed to create an entire Unix-compatible software system made of nothing but [free software](legal-ip-floss.md). GNU stands for "GNU is Not Unix", which is a programmer joke about [recursions](cs-langs.md), and he wrote [the GNU Manifesto](https://www.gnu.org/gnu/manifesto) to rally support for a completely free operating system.

Many of the programs for a fully-functioning Unix "clone" were completed by the early 1990s ([libraries](cs-langs.md), [compilers](cs-langs-compilers.md), [text editors](cs-software-ide.md), a [command-line shell](cs-cli.md), and a [windowing system](engineering-graphics.md)). However, the lower-level elements like device drivers, daemons, and the kernel were incomplete.

In 1991, Linus Torvalds decided to make a free version of that kernel, then released it publicly on his university's internet forum. Since he posted it on a public forum and many other software developers saw its value, it ended up taking off *way* more than he expected, and it quickly outpaced adoption compared to *everything* else Unix-related.

One of the draws of Linux is that it's completely free compared to Unix and other proprietary systems like [Windows](cs-os-windows.md) or [Apple](cs-os-apple.md). That freedom gives a few built-in features:

- People tend to feel generally safer with it, since the operating system is a community-led project.
- When a distro is popular, [bugs](cs-software-redesign.md) are quickly dealt with, since there are many eyes on that project.
- If someone develops anything driven by that back-end, there's little to no risk of [coercive behavior](legal-ip-floss.md) later on.

The culture of Unix and Linux holds together with a philosophical framework driven around [the varying ideas that constitute software freedom](legal-ip-floss.md), and they represent in the [various distros](cs-os-unix-distros.md) that implement different purposes.

## Unix-likes

OS frameworks that originated from Unix all have a similar-enough experience to make the user [feel at home](engineering-design.md) when swapping back-and-forth between them, including using many of the same [commands](cs-cli.md). To that end, the broad catchall term is "Unix-likes", though many people simply say "Linux".

The most prevalent non-Linux Unix system right now is the family of BSD operating systems (e.g., FreeBSD, NetBSD, OpenBSD), but there are others like AIX, HP-UX, Iris, and Solaris.

Even [Apple](cs-os-apple.md) uses a BSD Unix framework, for both macOS and iOS, but its key difference is that it's a hybrid of a ["monolithic kernel" and "microkernel"](cs-os.md), while Linux is *strictly* a monolithic kernel.

## Usage

Linux is lightweight, so it's excellent for low-profile computers, and is even convenient to run off a flash drive.

However, unlike [Windows](cs-os-windows.md), Linux has *also* become more consistently reliable.

The largest failure within Linux is tied to its [UX](engineering-design.md). For the most part, its [GUI](engineering-graphics.md) commands convert to [console commands](cs-cli.md), meaning any sufficient experience with Linux often requires accessing a terminal. This creates [a learning curve beyond the aptitude of some people](computers.md).

## Kernel design

There is a hierarchy of processes based on parent processes that run further child processes.

- The first process is PID 1, which is more often than not systemd, which triggers almost everything else.

### Filesystem

/bin and /sbin store binaries and system binaries (bash, cat, chmod, ping, echo, etc.).

- /sbin/init is the first process Linux officially runs, though it usually links to systemd.

/boot stores the kernel itself as well as all the [boot-available](cs-boot.md) elements:

- config
- initrd: a RAM disk image that loads a temporary root filesystem into memory during startup
- System-map or System.map: memory address locations for kernel symbol names
- vmlinuz: the proper kernel in compressed format and usable with virtual memory

/proc is a virtual filesystem in memory that reflects running processes, kernel config, and system hardware.

- /proc/cpuinfo
- /proc/meminfo
- /proc/modules: lists modules loaded into the kernel
- /proc/sys: kernel config settings, classified into subdirectories
  - Most of them only contain 0 or 1 values, with a few exceptions

/dev gives device files/nodes for all connected hardware devices.

- Block devices have data read and written in blocks (e.g., [physical memory](cs-memory.md))
- Character devices read and write data sequentially, one character at a time (e.g., [keyboard](cs-keyboard.md))
- These can be distinguished in "ls -l" by b or c as the first letter
- There are also some other special files for specific [programming](cs-software.md) purposes:
  - /dev/zero outputs as many zeroes as needed
  - /dev/null discards all information sent to it
  - /dev/urandom generates pseudo-random numbers

/sys came from kernel 2.6 onward as an improvement on /proc/sys.

/var stores variable data that accumulates over time

- /var/log holds most system logs
  - These logs are rotated to avoid memory overuse
- /var/cache has "cached" program data.
- /var/lib has data that gets modified when programs are run.
- /var/lock has "lock files" that track resources getting used.
- /var/opt has variable data for installed "packages".
- /var/spool has tasks waiting to get processed (/var/spool/cron, /var/spool/cups, /var/spool/mail).
- /var/tmp has temporary files saved between reboots.

/etc stores system config files (fonts, hosts, services, timezone, machine-id, etc.):

- "x" represents shadow passwords.
- /etc/passwd
  - 7 colon-delimited fields with basic user information including [UID and GID](cs-infosec-permissions.md)
  - (username):(password):(UID):(GID):(GECOS):(homedirectory):(shellpath)
  - GECOS is a CSV list of user information, which stands for General Electric Comprehensive Operating System, and became a type of digital rolodex in the late 20th century.
  - The shell path is the shell program automatically launched when the user first logs in (usually /bin/bash).
- /etc/group
  - 4 colon-delimited fields with basic information about groups and members.
  - (groupname):x:(GID):(memberlist)
- /etc/shadow
  - 9 colon-delimited fields with [hashed](encryption.md) user passwords.
  - It's stored as [encrypted](encryption.md)
  - (username):(password):(datelastchanged):(minpasswordage):(maxpasswordage):(passwordwarningperiod):(passwordinactivityperiod):(accountexpirationdate):(reserved)
- /etc/gshadow
  - 4 colon-delimited fields.
  - (groupname):x:(groupadmins):(groupmembers)
  - The hashed group passwords are for temporary membership.
- /etc/sudoers
  - Who can use "sudo" and how, with /etc/sudoers.d supplementing info

/tmp has files that aren't expected to persist between invocations of a program.

- By contrast, /var/tmp should *not* clear between reboots.

/run contains runtime variable data such as .pid files.

- It used to be in /var/run, which sometimes symlinks to /run.

/usr is read-only, with both data and binaries.

- /usr/bin has most user commands.
- /usr/include has code files for the C language.
- /usr/lib has obj, bin, and lib files for coding and packages.
- /usr/local has local software (context-depending).
- /usr/share has unchanging data that everything uses.
  - /usr/share/man has manual pages.

/home is often organized separately (such as a separate drive partition or drive) and tends to have user data.

There are also others:

- /lib has libraries and kernel modules.
- /mnt has mount files for temporary file systems.
- /opt has optional software applications.
- /root is the "root user" directory.

## Permissions

There are 9 characters that represent read/write/execute permissions:

- drwxrwxrwt
- The first character indicates normal file (-), directory (d), symlink (l), socket (s), or character device (c)
- The next three triads are grouped for users, groups, and others respectively.
  - Read permissions (r)
  - Write permissions (w)
  - Execute permissions (x)
    - There is also a restricted deletion flag (sticky bit) to prevent deletion except by the owner (t)
    - There is also an Set GID (SGID) bit that grants the process resulting from execution the privileges of the file's group (s)
- This also can represent as octal values:
  1. Read = 4
  2. Write = 2
  3. Execute = 1
  4. The sum of the three represents the value:
     - e.g., "chmod 760 example.txt" makes full r/w/x on the owner, r/w on the group, and nothing on others.

## Configurations

Routine maintenance jobs use the cron utility.

- The syntax is straightforward:
  - MIN HR DOM MON DOW CMD
    - MIN: 0-59, minute to do the task
    - HR: 0-23, hour to do the task
    - DOM: 1-31, the day of the month
    - MON: 1-12, the month
    - DOW: 0-6, the weekday
    - CMD: the command to execute
    - Any of the fields with "*" mean to do it all the time regarding that element.
    - Multiple values are comma-separated with no space (e.g., 4,7).
    - Continuous values are dash-separated with no space (e.g., 09-18).
- There are other features:
  - @yearly/@monthly/@daily will do it at midnight of 1/1, the first of the month, or every day respectively.
  - @reboot once the machine has booted
  - MAIL="(user)" sends the output to a different user.
- You can only schedule every minute max, and not every second.
- Further, you can save your cron file, then run crontab on it instead of having to change it manually.

## More information

- [DistroWatch.com visual family tree of Linux distributions](https://distrowatch.com/dwres.php?resource=family-tree)
