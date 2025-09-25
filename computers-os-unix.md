
# What Unix-likes are

"Linux" is a broad catch-all term to represent a variety of distributions ("distros"). Officially, the term is GNU/Linux because the Linux kernel mixes with GNU.

However, the demarcation between Linux/Windows/Apple isn't precise. Each operating system borrows *heavily* from the others, especially in the domain of [UX](engineering-design.md). In particular, GNU's system expands far into the realm of Windows-based operating systems, so it's not really an exclusive concept as much as [a FLOSS ideal](legal-ip-floss.md).

## History

Unix was an [operating system](computers-os.md) made by AT&T in 1969. However, AT&T was [monpolizing power](politics-monopolies.md) at the time (like [today's FAANG](faang.md)), so antitrust litigation prevented it from entering the computer industry. The company was forced to release the source code for free to anyone who asked. Many educational institutions (such as Berkeley) and businesses used Unix.

Later, once AT&T spun off Bell Labs, Bell was free to sell a proprietary license of Unix in 1984, but the damage to AT&T's potential hold on the market had already been done. Unix's source code was effectively public and legal to use.

In 1983, Richard Stallman created the GNU Project, which aimed to create an entire Unix-compatible software system made of nothing but [free software](legal-ip-floss.md). GNU stands for "GNU is Not Unix", which is a [programmer joke](humor-cs.md) about [recursions](computers-programming-basics.md), and he wrote [the GNU Manifesto](https://www.gnu.org/gnu/manifesto) to rally support for a completely free operating system.

Many of the programs for a fully-functioning Unix "clone" were completed by the early 1990s ([libraries](computers-programming-basics.md), [compilers](computers-compilers.md), [text editors](computers-software-ide.md), a [command-line shell](computers-cli.md), and a [windowing system](engineering-graphics.md)). However, the lower-level elements like device drivers, daemons, and the kernel were incomplete.

In 1991, Linus Torvalds decided to make a free version of that kernel, then released it publicly on his university's internet forum. Since he posted it on a public forum and many other software developers saw its value, it ended up taking off *way* more than he expected, and it quickly outpaced adoption compared to *everything* else Unix-related.

One of the draws of Linux is that it's completely free compared to Unix and other proprietary systems like [Windows](computers-os-windows.md) or [Apple](computers-os-apple.md). That freedom gives a few built-in features:

- People tend to feel generally safer with it, since the operating system is a community-led project.
- When a distro is popular, [bugs](computers-software-redesign.md) are quickly dealt with, since there are many eyes on that project.
- If someone develops anything driven by that back-end, there's little to no risk of [coercive behavior](legal-ip-floss.md) later on.

The culture of Unix and Linux holds together with a philosophical framework driven around [the varying ideas that constitute software freedom](legal-ip-floss.md).

## Distros

Each GNU/Linux distro is configured and adapted to specific preferences or functions.

Many of them are designed as one-size-fits-all desktop environment:

- [Ubuntu](https://ubuntu.com/) (off of [Debian](https://www.debian.org/))
- [Fedora](https://getfedora.org/)

A few are designed as a *very* general-purpose OS, mostly because they don't have many features built-in, meaning that only power users can set them up correctly:

- [Arch Linux](https://archlinux.org/)

Some are designed to *really* cater to new Linux users:

- [Zorin OS](https://zorin.com/) for Windows users

A few are for [PenTesting](computers-cysec-pentest.md):

- [Kali Linux](https://www.kali.org/)
- [Pentoo](https://pentoo.ch/)

A handful make Linux into a portable media center:

- [Kodi](https://kodi.tv/)

A few others were made for [computer security](computers-cysec.md):

- [Qubes](https://www.qubes-os.org/) uses [virtualization](computers-distsys-vm.md)
- [Tails](https://tails.boum.org/) uses [anonymity](computers-cysec.md)

Some are designed to be lower-profile or portable:

- [Linux Mint](https://linuxmint.com/)
- [Puppy Linux](https://puppylinux.com/)

There are a couple media-based OS designed to *only* run from portable media:

- [Knoppix](https://www.knopper.net/knoppix/index-en.html)

Many of them honor the GNU philosophy directly, which means any non-[FLOSS](legal-ip-floss.md) software won't work with the system:

- [Devuan](https://www.devuan.org/)

Others are meant for [enterprise-grade work](computers-distsys-enterprise.md):

- [Apache HTTP Server](https://httpd.apache.org/)
- [SUSE Linux](https://www.suse.com/)
- [Red Hat Enterprise Linux (RHEL)](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux)

Some are designed for specific hardware:

- [libreCMC](https://librecmc.org/) for an all-in-one embedded OS
- [Raspbian](https://www.raspbian.org/) for the [Raspberry Pi](computers-embedded.md)
- [Android](https://www.android.com/) for [Google](faang.md)-based phones
- [Chrome OS](https://www.google.com/chromebook/chrome-os/) is a browser-based OS for Google Chromebooks
- [Steam OS](https://store.steampowered.com/steamos/) powers Steam gaming platform machines
- [antiX](https://antixlinux.com/) is designed specifically to run well on older computers

If you have the patience and time, as well as the [marketing](marketing.md) acumen to [gain adoption](trends.md), you could make your *own* GNU/Linux distro.

- In fact, for educational reasons, you could simply [make it yourself from scratch](https://www.linuxfromscratch.org/).

It's worth noting that FreeBSD is *not* Linux, though they have *many* similarities:

- FreeBSD gives a kernel, device drivers, user utilities, and documentation. Linux only gives a kernel and device drivers, then expects other software to do the rest.
- The license for FreeBSD technically gives more freedom compared to Linux, including the ability for people to profit off the licensing.

## The distro hierarchy

Many of the distros have a thriving community that are *very* supportive. Most of the derelict distros are often downstream from larger distros that got better than their parent distros.

To elaborate, most distros are "forked" from other distros, as this non-exhaustive chart demonstrates, with the popular distros in bold:

- Clear Linux OS
- CRUX
  - **Arch Linux** (inspired by CRUX)
    - Chakra
    - EndeavourOS
    - Hyperbola
    - **Manjaro Linux**
    - Parabola
    - ArchBang
- Corel Linux
  - Xandros
- Softlanding Linux System (SLS)
  - Slackware
    - Dragora (inspired by Slackware)
    - openSUSE
    - Porteus
    - Salix OS
    - SUSE Linux Enterprise
    - Novell Open Enterprise Server
    - VectorLinux
    - Puppy Linux (inspired)
    - Zenwalk
  - **Debian** (inspired by Slackware)
    - CrunchBang Linux
    - Debian Edu
    - Deepin
    - Devuan
    - Grml
    - Kali Linux
    - Knoppix
    - Damn Small Linux
      - Tiny Core Linux (inspired)
    - MEPIS
    - antiX
    - Netrunner
    - Parrot OS
    - PureOS (for Purism devices)
    - SolydXK
    - SparkyLinux
    - SteamOS (for the Steam gaming platform)
    - Tails
    - TurnKey
    - **Ubuntu**
    - Bodhi
    - Canaima
    - Elementary OS
    - Freespire
    - Kodi
      - OpenELEC
    - Linspire
    - Linux Lite
    - **Linux Mint**
    - Pop! OS
    - Trisquel
    - Zentyal
    - **Zorin OS**
    - Univention Corporate Server
- Enoch Linux
  - Gentoo Linux
    - Chrome OS (for Google Chromebooks)
    - Pardus
    - Pentoo
    - Sabayon Linux
- Red Hat Linux
  - **Fedora**
    - BLAG
    - Korora
    - Qubes OS
    - Red Hat Enterprise Linux (RHEL)
    - AlmaLinux
    - CentOS
      - ClearOS
    - Oracle Linux
    - Scientific Linux
  - Mandriva
    - ALT Linux
    - ROSA
    - Mageia
    - OpenMandriva Lx
    - PCLinuxOS
  - Rocks Cluster Distribution
- **FreeBSD**
  - Void Linux (partly inspired by FreeBSD)
- LEAF Project (for embedded systems)
  - Alpine Linux
- Sorcerer
  - Source Mage

It's a wasted effort to cover all the inspirations for each distro, since they borrow ideas from each other *constantly*. It's also not worth time here to cover all the distros, since [other people have done that](https://distrowatch.com/dwres.php?resource=family-tree).

## Unix-likes

OS frameworks that originated from Unix all have a similar-enough experience to make the user [feel at home](engineering-design.md) when swapping back-and-forth between them, including using many of the same [commands](computers-cli.md). To that end, the broad catchall term is "Unix-likes".

[Apple](computers-os-apple.md) also uses a Unix framework, for both MacOS and iOS, but its key difference is that it's a hybrid of a ["monolithic kernel" and "microkernel"](computers-os.md), while Linux is *strictly* a monolithic kernel.

Apple's microkernel is XNU (which stands for "XNU is Not Unix" because programmers like recursions), which consists of several components:

- Carnegie Mellon University's Mach kernel
- FreeBSD components
- IOKit, the C++ [API](computers-software-design.md) for writing drivers

## Usage

Linux is lightweight, so it's excellent for low-profile computers, and is even convenient to run off a flash drive.

However, unlike [Windows](computers-os-windows.md), Linux has *also* become more consistently reliable.

The largest failure within Linux is tied to its [UX](engineering-design.md). For the most part, its [GUI](engineering-graphics.md) commands convert to [console commands](computers-cli.md), meaning any sufficient experience with Linux often requires accessing a terminal. This creates [a learning curve beyond the aptitude of some people](computers.md).

## Additional reading

- [DistroWatch.com visual family tree of Linux distributions](https://distrowatch.com/dwres.php?resource=family-tree)
