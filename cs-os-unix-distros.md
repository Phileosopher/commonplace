
# The distros of Linux

Each GNU/Linux distro is configured and adapted to specific preferences or functions.

- A distro is simply a config that made sense for a software engineer and then got popular enough to gain traction in the community.

Broadly each distro comes from several possible families:

- The largest comes from Debian, which uses the package manager dpkg and deb packages.
- The second most common is from RHEL, which uses the package manager rpm and rpm packages.
- openSUSE also uses YaST with the zypper command line, and the packages are *entirely* version-specific.
- Arch is highly stripped-down, with not much except the kernel and the Pacman package manager.

Interestingly, many of the distros are actually designed as secondary mechanisms to solve [version control](cs-software-versionctrl.md) issues:

- Fedora Desktop is the means for Red Hat to test RHEL features.
- openSUSE is the means to publicly test SUSE features.

It's worth noting that, with enough time and patience, absolutely any distro can be converted to another distro's functionality.

- In fact, for educational reasons, you could simply [make it yourself from scratch](https://www.linuxfromscratch.org/).
- Further, enough [marketing](marketing.md) acumen to [gain adoption](people-trends.md) is enough to create a new GNU/Linux distro.

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
