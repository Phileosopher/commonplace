
https://www.maketecheasier.com/learn-linux-by-playing-games/

LOOK INTO ALPINE LINUX FOR SMALL PROJECT LINUX

One of the most prominent issues with the Unix-like OS (i.e., Linux) is that the scope of choice is FAR too vast. There are literally 10 distros for every need. The variety is nice when you're a tech enthusiast, but most people just want "something that installs and works". For that reason, I just recommend Ubuntu to random people, or its Kubuntu flavor if they like Windows.

NOTE: it's important to know the "family" of Linux you're in because there are often related solutions (e.g., Kubuntu/Ubuntu will pretty much work w/ most Debian-family things, but others may need other steps to get it done)
- It's not uncommon when troubleshooting:
    1. Search for "[specific proprietary] audio driver Ubuntu" online
    2. find a reference to one for Fedora with something that pops up an error on Ubuntu
    3. search for "[command] alternative in Ubuntu" online
    4. find a reference to the issue, but for network drivers
    5. run 2/3 of the commands on #5 that may apply
    6. run #2 but with the alternatives applicable to Ubuntu

freeCodeCamp dev quiz - Unix
- The Linux uniq command removes duplicate lines in a file, by default.
- wc -w in Linux counts words in a file
- Every file/directory in an Operating System like Linux or macOS (and every UNIX system in general) has an owner. The owner of a file can do everything with it. It can decide the fate of that file. The owner (and the root user) can change the owner to another user, too, using the chown command.
- Bash (short for Bourne Again SHell) is the most widely used shell, packaged by default for most Linux distributions
    - There are many different kind of shells available on Linux and macOS computers. A few of them that dominate the space are bash, csh, zsh, and fish.
- You create an empty file using the touch command, followed by the name of the file e.g. touch demo.txt
- The less command shows the content stored inside a file.
- Curl is a command-line tool that allows us to do HTTP requests from shell
- You create soft links using the -s option of ln. For example, ln -s
- Calling uname without any options will return the Operating System codename. The m option shows the hardware name and the p option prints the processor architecture name.
- To print all columns in a file you can use the awk command. The action you specify inside the curly braces is print $0.
- You can delete a folder using rmdir. That folder must be empty.
- Every time you run a command, it's memorized in the history. You can display all the history using the history command.
- GNU stands for "GNU's Not Unix"
- The "core" of Linux is the "kernel", which has critical things for everything else
- ps shows currently running processes

The tar command is used to create an archive, grouping multiple files in a single file, without compressing them

DIFFICULT BUT AWESOME:
Among Linux distributions, Gentoo. This distro will give you Stockholm Syndrome. Its installation isn't merely user unfriendly, it often borders on being downright user abusive, but once installed, it is guaranteed to deliver the absolute maximum level of performance your hardware is capable of providing, beyond what you had ever seen your hardware accomplish on any other operating system (with the possible exception of MenuetOS, but that system's written entirely in assembly code, which is sort of cheating).

CompTIA - Unix-likes
- A technician is using the YUM package manager to install software on Linux. What setup file format does YUM use? RPM
- A desktop owner is installing a new application on a macOS. What format would the setup file be? DMG
- [Linux uses a package manager, and Android/iOS are basically that but as "app stores"]
- What does Linux use to verify the authenticity of software packages obtained from an online source? A hash value

NOTE: "Linux Culture" section probably dovetails with FLOSS

## Distros

Distros Chart:

- MAKE A CHART OF THE LINUX DISTROS
    - e.g.
    - Ubuntu
        - A [bootloader]
        - B [???]
        - C [???]
        - D Unity environment
    - Kubuntu
        - …
        - D KDE environemnt

[(4) For everyday use, it seems like distros don't vary much : linux](https://www.reddit.com/r/linux/comments/u184ww/for_everyday_use_it_seems_like_distros_dont_vary/)

- Make sure to parse the comments re: the technical differences

BE CAREFUL W/ GRAPHENEOS, THEY'VE GONE WOKE

FreeBSD is an operating system used to power modern servers, desktops, and embedded platforms.

CalyxOS is Canada's, GrapheneOS got political

## Linux Commands

Idea: consider what it would take to make VERY simple syntax for the CLI (e.g., sudo dnf update -y && sudo dnf upgrade -y -> update now

## Linux Culture

[Cannot Play DVDs on Linux Mint - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/361520/cannot-play-dvds-on-linux-mint)
- the nature of Linux is that it'll make people smarter consumers, since they see DRM and other fudgery as it happens

[Explaining Why We Don't Endorse Other Systems - GNU Project - Free Software Foundation🆓](https://www.gnu.org/distros/common-distros.html)
- there's a type of "puritanism" oriented toward completely-free software/hardware/everything
- this drives a LOT of the culture, even at the risk of (alienating users)(UX)
