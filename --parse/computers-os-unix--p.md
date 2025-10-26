
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

[F-Droid - alternative to Google Play store | Hacker News](https://news.ycombinator.com/item?id=30506413)
[F-Droid - Free and Open Source Android App Repository](https://f-droid.org/en/)
- Check the comments for tools

The tar command is used to create an archive, grouping multiple files in a single file, without compressing them

DIFFICULT BUT AWESOME:
Among Linux distributions, Gentoo. This distro will give you Stockholm Syndrome. Its installation isn't merely user unfriendly, it often borders on being downright user abusive, but once installed, it is guaranteed to deliver the absolute maximum level of performance your hardware is capable of providing, beyond what you had ever seen your hardware accomplish on any other operating system (with the possible exception of MenuetOS, but that system's written entirely in assembly code, which is sort of cheating).

[MenuetOS](http://menuetos.net/)

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

## 128-bit systems

[The road to Zettalinux | Hacker News](https://news.ycombinator.com/item?id=32950988)
[The road to Zettalinux [LWN.net]](https://lwn.net/Articles/908026/)

## applications

[A new wave of Linux applications | Hacker News](https://news.ycombinator.com/item?id=30364337)
[A new wave of Linux applications](https://tuxphones.com/convergent-linux-phone-apps/)

## binary tools

[Binutils - GNU Project - Free Software Foundation🆓](https://www.gnu.org/software/binutils)

## bin folder

[Alexander Blagoev](http://ablagoev.github.io/linux/adventures/commands/2017/02/19/adventures-in-usr-bin.html)
(2017) Adventures in /usr/bin and the likes

## bin

[Understanding the bin, sbin, usr/bin, usr/sbin split (2010) | Hacker News](https://news.ycombinator.com/item?id=31336396)
[Understanding the bin, sbin, usr/bin , usr/sbin split](http://lists.busybox.net/pipermail/busybox/2010-December/074114.html)

## building a unix clone

[Writing a Unix clone in about a month | Hacker News](https://news.ycombinator.com/item?id=40467297)
[Writing a Unix clone in about a month](https://drewdevault.com/2024/05/24/2024-05-24-Bunnix.html)

## commands - bash

[Bash - GNU Project - Free Software Foundation🆓](https://www.gnu.org/software/bash)
is an sh-compatible shell that incorporates useful features from the Korn shell and C shell.
[GNU Bash manual - GNU Project - Free Software Foundation🆓](https://www.gnu.org/software/bash/manual/)

[I wrote a TUI file manager in pure bash](https://old.reddit.com/r/linux/comments/14zf9ee/i_wrote_a_tui_file_manager_in_pure_bash/)

["Exit traps" can make your Bash scripts more robust and reliable (2013) | Hacker News](https://news.ycombinator.com/item?id=36400465)
[How "Exit Traps" Can Make Your Bash Scripts Way More Robust And Reliable](http://redsymbol.net/articles/bash-exit-traps/)

[Bash functions are better than I thought | Hacker News](https://news.ycombinator.com/item?id=29058140)
[Cuddly, Octo-Palm Tree: Bash functions are better than I thought](https://cuddly-octo-palm-tree.com/posts/2021-10-31-better-bash-functions/)

[Escaping strings in Bash using !:q | Hacker News](https://news.ycombinator.com/item?id=24659282)
[Escaping strings in Bash using !:q | Simon Willison's TILs](https://til.simonwillison.net/bash/escaping-a-string)

[Detecting the use of "curl | bash" server side (2016) | Hacker News](https://news.ycombinator.com/item?id=34145799)
[Detecting the use of "curl | bash" server side | Application Security](https://web.archive.org/web/20240311094552/https://www.idontplaydarts.com/2016/04/detecting-curl-pipe-bash-server-side/)

[Tell HN: Bash.org is no more | Hacker News](https://news.ycombinator.com/item?id=38950721)

[Bash Debugging | Hacker News](https://news.ycombinator.com/item?id=39568728)
[bash debugging](https://wizardzines.com/comics/bash-debugging/)

[Sandra Henry-Stocker](http://www.computerworld.com/article/3015657/linux/changing-how-bash-behaves.html)
Changing how bash behaves

[Aaron Maxwell](http://redsymbol.net/articles/unofficial-bash-strict-mode/)
Use the Unofficial Bash Strict Mode (Unless You Looove Debugging).
:star:
[some bash tips when dealing with bash strict mode](https://gist.github.com/Integralist/0fc25edb5d9ceeae74cc)

[Quickshiftin](https://quickshiftin.com/blog/2014/01/template-method-pattern-bash/)
(2014) Template method pattern in BASH

[Sam Rowe](http://samrowe.com/wordpress/advancing-in-the-bash-shell/)
Advancing in the Bash Shell

[GreyCat's Wiki](http://mywiki.wooledge.org/BashFAQ)
BASH Frequently Asked Questions
These are answers to frequently asked questions on channel #bash on the [irc.libera.chat](https://libera.chat/) IRC network
[GreyCat](http://mywiki.wooledge.org/BashFAQ/082)
Why is `$(...)` preferred over `...` (backticks)?

[Ian Miell](https://zwischenzugs.com/2019/05/11/seven-surprising-bash-variables/)
(2019) Seven Surprising Bash Variables

[Ian Miell](https://zwischenzugs.com/2018/10/12/eleven-bash-tips-you-might-want-to-know/)
(2018) Eleven bash Tips You Might Want to Know

[GreyCat](http://mywiki.wooledge.org/BashWeaknesses)
BashWeaknesses : There are certain things BASH is not very good at.

[Bazyli Brzóska](https://invent.life/project/bash-infinity-framework)
(2015) Bash Infinity Framework

[Tim Visee](https://timvisee.com/blog/elegant-bash-conditionals/)
(2021) Elegant bash conditionals

[Mulle kybernetiK](https://www.mulle-kybernetik.com/modern-bash-scripting/)
(2022) Modern Bash (Zsh) Scripting

[ps aux written in bash without forking | Hacker News](https://news.ycombinator.com/item?id=41097241)
[GitHub - izabera/ps](https://github.com/izabera/ps)

## commands - chmod

[Alan Franzoni](https://www.franzoni.eu/chmod-and-the-capital-x/)
(2015) chmod and the capital X
This is one very, very, very interesting piece of ancient wisdom.

## commands - dd

[The cult of dd (2017) | Hacker News](https://news.ycombinator.com/item?id=33324704)
[The Cult of DD](https://eklitzke.org/the-cult-of-dd)

[Useless Use of "dd" (2015) | Hacker News](https://news.ycombinator.com/item?id=31474710)
[Useless Use Of dd - Vidar's Blog](https://www.vidarholen.net/contents/blog/?p=479)

## commands - epoll

[Linux: What Can You Epoll? | Hacker News](https://news.ycombinator.com/item?id=33299650)
[Linux: What can you epoll? · Graham King](https://darkcoding.net/software/linux-what-can-you-epoll/)

## commands - htop

[Today I learned htop shows wine programs with their "windows file paths" : linux](https://old.reddit.com/r/linux/comments/tprh6u/today_i_learned_htop_shows_wine_programs_with)

## commands - last

[Vivek Gite](https://www.cyberciti.biz/faq/linux-unix-last-command-examples/)
Linux / Unix: last Command Examples

## commands - man

[Why does man print "gimme gimme gimme" at 00:30? (2017) | Hacker News](https://news.ycombinator.com/item?id=27994194)
[date - Why does man print "gimme gimme gimme" at 00:30? - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/405783/why-does-man-print-gimme-gimme-gimme-at-0030)

## commands

[Unix command line conventions over time | Hacker News](https://news.ycombinator.com/item?id=31293032)
[Unix command line conventions over time](https://blog.liw.fi/posts/2022/05/07/unix-cli/)

[Silver Moon](http://www.binarytides.com/linux-fun-commands/)
20 amusing Linux commands to have fun with the terminal

[Vivek Gite](https://www.cyberciti.biz/faq/linux-list-network-interfaces-names-command/)
(2018) Linux Show / Display Available Network Interfaces

[Sandra Henry-Stocker](http://www.computerworld.com/article/3069981/linux/the-linux-command-that-you-should-never-say-out-loud.html)
thefuck : The Linux command that you should never say out loud

[SathiyaMoorthy](https://www.thegeekstuff.com/2010/06/at-atq-atrm-batch-command-examples/)
(2010) Understand at, atq, atrm, batch Commands using 9 Examples

## commands - mkdir+find

[`find` + `mkdir` is Turing complete | Hacker News](https://news.ycombinator.com/item?id=41115941)
[Randomly updated](https://ogiekako.vercel.app/blog/find_mkdir_tc)

## commands - mmap

[Why mmap is faster than system calls (2019) | Hacker News](https://news.ycombinator.com/item?id=25701959)
[Why mmap is faster than system calls | by Alexandra (Sasha) Fedorova | Medium](https://sasha-f.medium.com/why-mmap-is-faster-than-system-calls-24718e75ab37)

[Use mmap with care | Hacker News](https://news.ycombinator.com/item?id=19805675)
[Use mmap With Care - News - Sublime HQ](https://www.sublimetext.com/blog/articles/use-mmap-with-care)

## commands - mv

[Renaming files with mv without typing the name two times | Hacker News](https://news.ycombinator.com/item?id=22859935)
[Rename files in linux / bash using mv command without typing the full name two times](https://gist.github.com/premek/6e70446cfc913d3c929d7cdbfe896fef)

[Vivek Gite](https://www.cyberciti.biz/faq/linuxunix-move-file-starting-with-a-dash/)
(2010) Linux/UNIX: Move File Starting With A Dash

## commands - ncat

[Pradeep Kumar](https://www.linuxtechi.com/nc-ncat-command-examples-linux-systems/)
(2017) 10 useful ncat (nc) Command Examples for Linux Systems

## commands - netstat

[Ravi Saive](https://www.tecmint.com/20-netstat-commands-for-linux-network-management/)
20 Netstat Commands for Linux Network Management

## commands - occ

[Nextcloud Issuing OCC Commands without installing sudo](https://blog.lukebtaylor.com/posts/nextcloud-issuing-occ-commands-without-installing-sudo/)

## commands - rm

[Stack Exchange](https://unix.stackexchange.com/questions/68523/find-and-remove-large-files-that-are-open-but-have-been-deleted)
Find and remove large files that are open but have been deleted

## commands - sudo

[The first stable release of a memory safe sudo implementation | Hacker News](https://news.ycombinator.com/item?id=38161016)
[The First Stable Release of a Memory Safe sudo Implementation - Prossimo](https://www.memorysafety.org/blog/sudo-first-stable-release/)

[Sudo for Windows | Hacker News](https://news.ycombinator.com/item?id=39305452)
[Introducing Sudo for Windows! - Windows Command Line](https://devblogs.microsoft.com/commandline/introducing-sudo-for-windows/)

[the best sudo replacement | Hacker News](https://news.ycombinator.com/item?id=34454165)
[🥺: the best sudo replacement - Xe Iaso](https://xeiaso.net/blog/xn--ts9h/)

[Use TouchID to Authenticate Sudo on macOS | Hacker News](https://news.ycombinator.com/item?id=32611340)
[Use TouchID to Authenticate sudo on macOS - Digitaino IT](https://it.digitaino.com/use-touchid-to-authenticate-sudo-on-macos/)

[Laszlo Pusztai](http://www.laszlopusztai.net/2012/12/05/hdiutil-requires-sudo-for-readwrite/)
(2012) hdiutil Requires sudo for Read/Write

## commands - systemd

[LKML: Christopher Barry: OT: Open letter to the Linux World](https://lkml.org/lkml/2014/8/12/459)

[Chris Siebenmann](https://utcc.utoronto.ca/~cks/space/blog/linux/SystemdCrashAndMore)
(2014) The bad side of systemd: two recent systemd failures

## commands - tcpdump

[DayDreamer](http://daydreamer66.blogspot.be/2014/06/rhel-how-can-non-root-users-can-run.html)
(2014) RHEL: How can non-root users can run tcpdump or Wireshark or use libpcap

[Julia Evans](https://jvns.ca/blog/2016/03/16/tcpdump-is-amazing/)
(2016) tcpdump is amazing

[Steve Howard](http://appcrawler.com/wordpress/2012/08/01/tcpdump-to-see-oracle-errors/)
(2012) tcpdump to see Oracle errors

[Oleg Muravskiy](https://texnoblog.wordpress.com/2010/04/17/using-tcpdump/)
(2010) Using tcpdump to see HTTP requests and responses

[Working all day](http://workrobot.com/sysadmin/security/tcpdump_expressions.html)
TCPDUMP expressions

[Daniel Miessler](https://danielmiessler.com/study/tcpflags/)
How to Remember Your TCP Flags

## commands - termutils

[Termutils - GNU Project - Free Software Foundation (FSF)🆓](https://www.gnu.org/software/termutils)

## desktop environment - antix linux

[antiX Linux - Proudly anti-fascist "antiX Magic" in an environment suitable for old and new computers.](https://antixlinux.com/)

## desktop environment - gnome

[GNOME - Simple, beautiful, elegant.](https://www.gnome.org)
[Index of /](https://ftp.gnome.org/)
[Index of /](https://download.gnome.org/)
[Technical Blog of Richard Hughes - Blog about geeky stuff](https://blogs.gnome.org/hughsie)

[Material Shell - A modern desktop interface for GNOME | Hacker News](https://news.ycombinator.com/item?id=24491091)
[Material Shell - A new desktop experience](https://material-shell.com/)

[A patent lawsuit against GNOME | Hacker News](https://news.ycombinator.com/item?id=21071699)
[A patent lawsuit against GNOME [LWN.net]](https://lwn.net/Articles/800516/)

[GNOME has no thumbnails in the file picker and my toilets are blocked | Hacker News](https://news.ycombinator.com/item?id=25719796)
[Gnome has no thumbnails in the file picker and my toilets are blocked (2021) | Hacker News](https://news.ycombinator.com/item?id=31778490)
[GNOME has no thumbnails in the file picker (and my toilets are blocked)](https://jayfax.neocities.org/mediocrity/gnome-has-no-thumbnails-in-the-file-picker)

[How much faster are the Gnome 46 terminals? | Hacker News](https://news.ycombinator.com/item?id=39966918)
[Just How Much Faster Are the GNOME 46 Terminals? | Ivan Molodetskikh's Webpage](https://bxt.rs/blog/just-how-much-faster-are-the-gnome-46-terminals/)

## desktop environment - gnome+wayland

[Tell HN: Gnome on Wayland Is Amazing | Hacker News](https://news.ycombinator.com/item?id=30750710)

## desktop environment - gtk

[The end of the nice GTK button | Hacker News](https://news.ycombinator.com/item?id=30795846)
[The end of the nice GTK button](https://blog.brixit.nl/the-end-of-the-nice-gtk-button/)

[New Renderers for GTK | Hacker News](https://news.ycombinator.com/item?id=39172377)
[New renderers for GTK - GTK Development Blog](https://blog.gtk.org/2024/01/28/new-renderers-for-gtk/)

## desktop environment - i3

[i3 (window manager) - Wikipedia](https://en.wikipedia.org/wiki/I3_(window_manager))

## desktop environment - kde

[Revisiting KDE | Hacker News](https://news.ycombinator.com/item?id=34390655)
[Jack's Blog - Revisiting KDE](https://jackevansevo.github.io/revisiting-kde.html)

[The KDE desktop gets an overhaul with Plasma 6 | Hacker News](https://news.ycombinator.com/item?id=39548088)
[The KDE desktop gets an overhaul with Plasma 6 [LWN.net]](https://lwn.net/Articles/963851/)

[Debian KDE: Right Linux distribution for professional digital painting in 2024 | Hacker News](https://news.ycombinator.com/item?id=40533319)
[Debian 12 KDE Plasma: The right GNU/Linux distribution for professional digital painting in 2024. Reasons and complete installation guide. - David Revoy](https://www.davidrevoy.com/article1030/debian-12-kde-plasma-2024-install-guide)

## desktop environment - kera desktop

[Kera Desktop: open-source, cross-platform, web-based desktop environment | Hacker News](https://news.ycombinator.com/item?id=36260589)
[Kera Desktop](https://desktop.kerahq.com/)

## desktop environment - lumina

[Features of Lumina :: Lumina Desktop Environment](https://lumina-desktop.org/features/)

## desktop environment

[Linux Desktop Environments System Usage | Hacker News](https://news.ycombinator.com/item?id=33951719)
[2022 Linux Desktop Environments System Usage (Gnome, KDE, XFCE, LXQT, Cinnamon, Mate)](https://itvision.altervista.org/linux-desktop-environments-system-usage.html)

[9 Best Linux Desktop Environments to Optimize Your Experience - Geekflare](https://geekflare.com/best-linux-desktop-environments/)

## desktop environment - wayland

[Wayland](https://wayland.freedesktop.org)

[Firefox Wayland: fractional-scale-v1 support merged](https://old.reddit.com/r/linux/comments/15sh2yi/firefox_wayland_fractionalscalev1_support_merged/)

[An X11 apologist tries Wayland | Hacker News](https://news.ycombinator.com/item?id=32891313)
[An X11 Apologist Tries Wayland](https://artemis.sh/2022/09/18/wayland-from-an-x-apologist.html)

[I'm tired of this anti-Wayland horseshit | Hacker News](https://news.ycombinator.com/item?id=26001179)
[I'm tired of this anti-Wayland horseshit](https://web.archive.org/web/20231223232401/https://drewdevault.com/2021/02/02/Anti-Wayland-horseshit.html)

## distros - 0 multiple

[Lightweight Linux Distributions For Older PCs](https://www.freecodecamp.org/news/lightweight-linux-distributions-for-your-pc/)

## distros - Alpine Linux

[index | Alpine Linux](https://www.alpinelinux.org/)

[Alpine Linux in the Browser (2020) | Hacker News](https://news.ycombinator.com/item?id=34371073)
[JSLinux](https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192)
[Fabrice Bellard's Home Page](https://bellard.org/)
[BPG Image format](https://bellard.org/bpg/)

## distros - Android - forks - LineageOS

[LineageOS](https://lineageos.org/)
LineageOS, one of the biggest an well maintained alternative to Google's AOSP. Google apps (short: gapps)
can be optionally installed.

[LineageOS 19 | Hacker News](https://news.ycombinator.com/item?id=31166346)
[Changelog 26 - Tailored Twelve, Audacious Automotive, Neat Networking, Devoted Developers - LineageOS - LineageOS Android Distribution](https://lineageos.org/Changelog-26/)

[How to deGoogle LineageOS in 2019 : privacy](https://old.reddit.com/r/privacy/comments/cldrym/how_to_degoogle_lineageos_in_2019/)

## distros - Android - forks

[Secure Android - CopperheadOS - Copperhead](https://copperhead.co/android/)

[DeprecatedPortingToAndroid10 - Replicant](https://redmine.replicant.us/projects/replicant/wiki/DeprecatedPortingToAndroid10)

[Replicaant](https://replicant.us/)
replicant is a fully free Android distribution running on several devices, a free software mobile operating system putting the emphasis on freedom and privacy/security.

## distros - Android

[Android 14 adds support for using your smartphone as a webcam | Hacker News](https://news.ycombinator.com/item?id=37603467)
[Android 14 Adds Support for Using Your Smartphone as a Webcam](https://www.esper.io/blog/android-14-adds-support-for-using-your-smartphone-as-a-webcam)

[Android 14 introduces cellular connectivity security features | Hacker News](https://news.ycombinator.com/item?id=37055479)
[Google Online Security Blog: Android 14 introduces first-of-its-kind cellular connectivity security features](https://security.googleblog.com/2023/08/android-14-introduces-first-of-its-kind.html)

[Google has a secret browser hidden inside the settings | Hacker News](https://news.ycombinator.com/item?id=36478206)
[Google has a secret browser hidden inside the settings - Matan-h](https://matan-h.com/google-has-a-secret-browser-hidden-inside-the-settings/)
[Google has another secret browser | Hacker News](https://news.ycombinator.com/item?id=39226754)
[Google has another secret browser - Matan-h](https://matan-h.com/another-secret-browser)

[The Samsung Galaxy S23's bloated Android build somehow uses 60GB of storage | Hacker News](https://news.ycombinator.com/item?id=34682225)
[Bloatware pushes the Galaxy S23 Android OS to an incredible 60GB [Updated] | Ars Technica](https://arstechnica.com/gadgets/2023/02/the-samsung-galaxy-s23s-bloated-android-build-somehow-uses-60gb-of-storage/)

## distros - Arch Linux - Archcraft

[Archcraft : Home](https://archcraft.io/)
[Archcraft : Home](https://archcraft-os.github.io/)

## distros - Arch Linux - ArcoLinux

[ArcoLinux | ArcoLinux](https://www.arcolinux.info/)

## distros - Arch Linux - Artix

[Anarchy](https://artixlinux.org/)

## distros - Arch Linux - BlackArch

[BlackArch](https://blackarch.org/)
is an Arch Linux-based penetration testing distribution for penetration testers.

## distros - Arch Linux

[Migrating Arch Linux's packaging infrastructure to GitLab](https://about.gitlab.com/blog/2023/09/11/migrating-arch-linux-packaging-infrastructure-gitlab/)

[Graphing the packages on my laptop (Arch). Nodes are packages=~1900, Edges are dependency relation=~7700. High-res SVG in the comments.](https://old.reddit.com/r/linux/comments/16awoz3/graphing_the_packages_on_my_laptop_arch_nodes_are/)

[Wife's Debian PC driving me nuts...](https://old.reddit.com/r/archlinux/comments/165j4vy/wifes_debian_pc_driving_me_nuts/)

[Show HN: Twitch Installs Arch Linux - A cooperative text-based horror game | Hacker News](https://news.ycombinator.com/item?id=10477721)
[Twitch Installs Arch Linux](https://web.archive.org/web/20151030092759/https://www.twitchinstalls.com/)

[I'm surprised by Arch stability : archlinux](https://old.reddit.com/r/archlinux/comments/ttw3oi/im_surprised_by_arch_stability)

[Startup time : archlinux](https://old.reddit.com/r/archlinux/comments/u1oo5g/startup_time)

[Using the same Arch Linux installation for a decade | Hacker News](https://news.ycombinator.com/item?id=32483979)
[Using the Same Arch Linux Installation for a Decade](https://meribold.org/2022/08/16/same-arch-linux-installation-for-a-decade/)

[arch linux](https://www.archlinux.org/)
[arch linux](https://web.archive.org/web/20210102182957/https://www.archlinux.org/)
[ArchWiki](https://wiki.archlinux.org/)
my favourite linux distro

## distros - Arch Linux - Obscurix

[Obscurix](https://obscurix.github.io/)

## distros - Arch Linux - Peux OS

[Home Peux OS](https://peux-os.netlify.app/)

## distros - Asahi and Apple

[Apple Helps Asahi Linux | Hacker News](https://news.ycombinator.com/item?id=29591578)
[Hector Martin on Twitter: "Looks like Apple changed the requirements for Mach-O kernel files in 12.1, breaking our existing installation process... and they *also* added a raw image mode that will never break again and doesn't require Mach-Os. And people said they wouldn't help. This is intended for us."](https://web.archive.org/web/20220326234421/https://twitter.com/marcan42/status/1471799568807636994)

## distros - Asahi

[Asahi Linux: Linux on Apple Silicon project | Hacker News](https://news.ycombinator.com/item?id=25649719)
[Asahi Linux](https://asahilinux.org/)

[Paving the Road to Vulkan on Asahi Linux | Hacker News](https://news.ycombinator.com/item?id=35233479)
[Paving the Road to Vulkan on Asahi Linux - Asahi Linux](https://asahilinux.org/2023/03/road-to-vulkan/)

[OpenGL 3.1 on Asahi Linux | Hacker News](https://news.ycombinator.com/item?id=36212674)
[OpenGL 3.1 on Asahi Linux - Asahi Linux](https://asahilinux.org/2023/06/opengl-3-1-on-asahi-linux/)

[The Quest for Netflix on Asahi Linux | Hacker News](https://news.ycombinator.com/item?id=35081510)
[The Quest for Netflix on Asahi Linux | Blog](https://www.da.vidbuchanan.co.uk/blog/netflix-on-asahi.html)

[Asahi Linux goes from Apple Silicon port project to macOS bug hunters | Hacker News](https://news.ycombinator.com/item?id=38101328)
[Asahi Linux finds macOS bug that leaves machines unbootable • The Register](https://www.theregister.com/2023/11/01/asahi_linux_mac_black_screen/)

[Apple GPU drivers now in Asahi Linux | Hacker News](https://news.ycombinator.com/item?id=33891197)
[Apple GPU drivers now in Asahi Linux - Asahi Linux](https://asahilinux.org/2022/12/gpu-drivers-now-in-asahi-linux/)

[Asahi Linux alpha release | Hacker News](https://news.ycombinator.com/item?id=30729212)
[The first Asahi Linux Alpha Release is here! - Asahi Linux](https://asahilinux.org/2022/03/asahi-linux-alpha-release/)

## distros - AttifyOS

[AttifyOS](https://github.com/adi0x90/attifyos)
Linux distro for pentesting IoT devices.

## distros - Backtrack Linux

[BackTrack Linux - Penetration Testing Distribution](https://www.backtrack-linux.org)

## distros - Batocera

[batocera.linux](https://batocera.org/)

## distros - Bedrock Linux

[Bedrock Linux](https://bedrocklinux.org/)

## distros - Bottlerocket

[Bottlerocket - Minimal, immutable Linux OS with verified boot | Hacker News](https://news.ycombinator.com/item?id=37626731)
[Bottlerocket](https://bottlerocket.dev/)

## distros - BSD - DragonFly BSD

[DragonFlyBSD: DragonFly BSD](https://www.dragonflybsd.org/)
[DragonFly On-Line Manual Pages : vkernel(7)](https://www.dragonflybsd.org/cgi/web-man?command=vkernel&section=7)
[Index of /~marino](https://www.dragonflybsd.org/~marino/)

## distros - BSD - FreeBSD

[The FreeBSD Project](https://www.freebsd.org)

[Index of /~ssouhlal/](https://people.freebsd.org/~ssouhlal)

[FreeBSD optimizations used by Netflix to serve video at 800Gb/s [pdf] | Hacker News](https://news.ycombinator.com/item?id=33449297)
[EuroBSD 2022 - euro2022.pdf](https://people.freebsd.org/~gallatin/talks/euro2022.pdf)

[Serving Netflix Video at 400Gb/s on FreeBSD [pdf] | Hacker News](https://news.ycombinator.com/item?id=28584738)
[EuroBSD 2021 - euro2021.pdf](https://people.freebsd.org/~gallatin/talks/euro2021.pdf)

[Technical reasons to choose FreeBSD over GNU/Linux (2020) | Hacker News](https://news.ycombinator.com/item?id=32369189)
[Technical reasons to choose FreeBSD over GNU/Linux](https://unixdigest.com/articles/technical-reasons-to-choose-freebsd-over-linux.html)

[Why would someone choose FreeBSD over Linux?](https://unix.stackexchange.com/questions/14489/why-would-someone-choose-freebsd-over-linux)

[FreeBSD on Firecracker | Hacker News](https://news.ycombinator.com/item?id=37253035)
[FreeBSD on Firecracker | USENIX](https://www.usenix.org/publications/loginonline/freebsd-firecracker)

[FreeBSD spends 7% of its boot time running a bubblesort on its SYSINITs | Hacker News](https://news.ycombinator.com/item?id=36002574)
[Colin Percival on X: "When the FreeBSD kernel boots in Firecracker (1 CPU, 128 MB RAM), it now spends 7% of its time running a bubblesort on its SYSINITs. O(N^2) can bite hard when you're sorting over a thousand items. Time to replace the bubblesort with something faster." / X](https://twitter.com/cperciva/status/1659558311920914432)

[FreeBSD replaces bubblesort with mergesort on SYSINTs | Hacker News](https://news.ycombinator.com/item?id=37205053)
[Colin Percival on X: "FreeBSD (HEAD) no longer spends time running a bubblesort on its SYSINITs. We're now running a mergesort which is ~100x faster: https://t.co/1F8Yodedh3" / X](https://twitter.com/cperciva/status/1693127769901969772)

[anyone using bsd : HowToHack](https://old.reddit.com/r/HowToHack/comments/11dxp65/anyone_using_bsd)

[FreeBSD Portsnap](https://www.daemonology.net/portsnap)

[FreeBSD Update](https://www.daemonology.net/freebsd-update)

[Depenguinator](https://www.daemonology.net/depenguinator)

[FreeBSD Journal](https://issue.freebsdfoundation.org/publication/?m=33057&l=1&view=issuelistBrowser)
it is a great list of periodical magazines about FreeBSD and other important things.

[The NetBSD Project](https://www.netbsd.org/)

## distros - BSD - FreeBSD - forks

[RavynOS - Finesse of macOS, freedom of FreeBSD | Hacker News](https://news.ycombinator.com/item?id=32492514)
[Airyx OS | Hacker News](https://news.ycombinator.com/item?id=28068542)
[ravynOS - Finesse of macOS. Freedom of FreeBSD.](https://ravynos.com/)

## distros - BSD - FreeBSD - HelloSystem

[HelloSystem: A graphical OS built on FreeBSD | Hacker News](https://news.ycombinator.com/item?id=37262857)
[hello - helloSystem documentation](https://hellosystem.github.io/docs/)

## distros - BSD - FreeBSD - SecBSD

[SecBSD](https://www.secbsd.org/)

## distros - BSD - GhostBSD

[A simple, elegant desktop BSD Operating System | GhostBSD](https://ghostbsd.org/)

## distros - BSD

[John Lasseter drew the BSD daemon logo | Hacker News](https://news.ycombinator.com/item?id=39030991)
[The Director of "Toy Story" also drew the BSD Daemon logo](https://www.jacobelder.com/2024/01/17/director-of-toy-story-also-drew-bsd-daemon.html)

[MidnightBSD](https://www.midnightbsd.org/)

[NomadBSD](https://www.nomadbsd.org/)

## distros - BSD - OpenBSD

[John Carmack is reading and contributing to OpenBSD source code | Hacker News](https://news.ycombinator.com/item?id=23224584)
['Code changes for clarity' - MARC](https://marc.info/?l=openbsd-tech&m=158965652915344&w=2)

[OpenBSD/arm64 on Apple M1 systems | Hacker News](https://news.ycombinator.com/item?id=30734527)
['OpenBSD/arm64 on Apple M1 systems' - MARC](https://marc.info/?l=openbsd-arm&m=164768992119719&w=2)

[If you're happy with OpenBSD, probably any computer is good enough | Hacker News](https://news.ycombinator.com/item?id=34666305)
[If you're happy with OpenBSD, probably any computer is good enough.](https://web.archive.org/web/20230927180134/http://muezza.ca/thoughts/openbsd_imac_g4/)

[OpenBSD Release Songs | Hacker News](https://news.ycombinator.com/item?id=38919862)
[OpenBSD: Release Songs](https://www.openbsd.org/lyrics.html)

[OpenBSD 7.5 | Hacker News](https://news.ycombinator.com/item?id=39938072)
[OpenBSD 7.5](https://www.openbsd.org/75.html)

[OpenBSD KDE Plasma Desktop | Hacker News](https://news.ycombinator.com/item?id=38915759)
[OpenBSD KDE Plasma Desktop · rsadowski.de](https://rsadowski.de/posts/2024-01-09-openbsd-kde/)

[GitHub - slicer69/doas: A port of OpenBSD's doas which runs on FreeBSD, Linux, NetBSD, and illumos](https://github.com/slicer69/doas)

[We have reached OpenBSD of Theseus | Hacker News](https://news.ycombinator.com/item?id=41332342)
['CVS: cvs.openbsd.org: src' - MARC](https://marc.info/?l=openbsd-cvs&m=172443408727088&w=2)

## distros - CAINE

[CAINE](https://www.caine-live.net/page5/page5.html)

## distros - CalyxOS

NOTE: CALYX IS THE CANADIAN GOVT
[CalyxOS - De-Googled Android Alternative | Hacker News](https://news.ycombinator.com/item?id=28090024)
[CalyxOS](https://calyxos.org/)

## distros - CasaOS

[CasaOS A simple, easy-to-use, elegant open-source home cloud system](https://www.casaos.io/)

## distros - CentOS and Rocky Linux

[CentOS Project shifts focus to CentOS Stream | Hacker News](https://news.ycombinator.com/item?id=25345428)
[[CentOS-announce] CentOS Project shifts focus to CentOS Stream](https://lists.centos.org/pipermail/centos-announce/2020-December/048208.html)

[Rocky Linux: A CentOS replacement by the CentOS founder | Hacker News](https://news.ycombinator.com/item?id=25445725)
[rocky-linux/rocky: Rocky Linux is a community enterprise Operating System designed to be 100% bug-for-bug compatible with Enterprise Linux created in response to the effective discontinuation of CentOS.](https://github.com/rocky-linux/rocky)
[Rocky Linux](https://rockylinux.org/)

[Michael Heap](https://michaelheap.com/build-centos-5-generic-rpm-on-centos-6/)
Build CentOS 5 generic RPM on CentOS 6

## distros - ChimeraOS

[ChimeraOS: Instantly turn any PC into a gaming console | Hacker News](https://news.ycombinator.com/item?id=37052875)
[ChimeraOS](https://chimeraos.org/)
Gaming Focused OS

[Chimera Linux | Hacker News](https://news.ycombinator.com/item?id=38667503)
[Chimera Linux](https://chimera-linux.org/)

## distros - CSI Linux

[CSI Linux – A Complete Cyber Forensics Platform](https://csilinux.com/)

## distros - DahliaOS

[GitHub - dahliaOS/brand: dahliaOS brand assets](https://github.com/dahliaOS/brand)

## distros - Damn Small Linux

[Damn Small Linux 2024 | Hacker News](https://news.ycombinator.com/item?id=39215846)
[DSL 2024 Information](https://www.damnsmalllinux.org/)

## distros - Debian

[Debian celebrates 30 years | Hacker News](https://news.ycombinator.com/item?id=37160580)
[Debian Celebrates 30 years! - Bits from Debian](https://bits.debian.org/2023/08/debian-turns-30.html)

[Index of /](https://ftp.se.debian.org/)

[Brand-new Linux release, which I'm calling the Debian Linux Release (1993) | Hacker News](https://news.ycombinator.com/item?id=37147617)
[wiki.debian.org/DebianHistory?action=AttachFile&do=get&target=Debian-announcement-1993.txt](https://wiki.debian.org/DebianHistory?action=AttachFile&do=get&target=Debian-announcement-1993.txt)

[Debian's Which Hunt | Hacker News](https://news.ycombinator.com/item?id=29026623)
[Debian's which hunt [LWN.net]](https://lwn.net/Articles/874049/)

[Debian 11 | Hacker News](https://news.ycombinator.com/item?id=28180074)
[Release Notes for Debian 11 (bullseye), 64-bit PC](https://www.debian.org/releases/bullseye/amd64/release-notes/)

[Debian Running on Rust Coreutils | Hacker News](https://news.ycombinator.com/item?id=26396798)
[Debian running on Rust coreutils](https://sylvestre.ledru.info/blog/2021/03/09/debian-running-on-rust-coreutils)

[Debian 12 "Bookworm" | Hacker News](https://news.ycombinator.com/item?id=36269934)
[Debian -- News -- Debian 12 "bookworm" released](https://www.debian.org/News/2023/20230610)

[If you're not using Debian, what are you using and why? : selfhosted](https://old.reddit.com/r/selfhosted/comments/16vovjo/if_youre_not_using_debian_what_are_you_using_and/)

[Why is Debian the way it is? | Hacker News](https://news.ycombinator.com/item?id=37809276)
[Why is Debian the way it is?](https://blog.liw.fi/posts/2023/debian-reasons/)

[How I tripped over the Debian weak keys vulnerability | Hacker News](https://news.ycombinator.com/item?id=39976225)
[Brane Dump: How I Tripped Over the Debian Weak Keys Vulnerability](https://www.hezmatt.org/~mpalmer/blog/2024/04/09/how-i-tripped-over-the-debian-weak-keys-vuln.html)

[Mobian](https://mobian-project.org/)

[Septor](https://septor.sourceforge.io/)

## distros - Debian - Devuan

[Welcome to devuan.org | Devuan GNU+Linux Free Operating System](https://www.devuan.org/)

## distros - Debian - Kicksecure

[Kicksecure - Secure by Default Operating System](https://www.kicksecure.com/)

[Whonix - Superior Internet Privacy](https://www.whonix.org/)
Use Tor to encrypt your Internet traffic
[Speculative Tor Attacks - Whonix](https://www.whonix.org/wiki/Speculative_Tor_Attacks)
[Leak Tests](https://www.whonix.org/wiki/Dev/Leak_Tests)
Leak Tests
[Things NOT to Do](https://www.whonix.org/wiki/DoNot)
[Whonix](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion/)

## distros - Debian - Nitrux

[Nitrux - #YourNextOS - A Linux for Everyone](https://nxos.org/)

## distros - Debian - Subgraph OS

[Subgraph](https://subgraph.com/)
[Subgraph OS](https://subgraph.com/sgos)

## distros - Debian vs Ubuntu

[Wow Debian is so much better than Ubuntu Server: selfhosted](https://www.reddit.com/r/selfhosted/comments/11jvm48/wow_debian_is_so_much_better_than_ubuntu_server)

## distros - Deft

[Deft Linux](https://deftlinux.net)

## distros - DORA

[axlshear/dora-osint-vm](https://github.com/axlshear/dora-osint-vm)

## distros - Dracos

[Dracos Linux](https://dracos-linux.org)

## distros - DSLinux

[DSLinux - Linux for the Nintendo DS | Hacker News](https://news.ycombinator.com/item?id=37826357)
[DSLinux - Linux for the Nintendo DS](https://www.dslinux.org/)

## distros - Elementary OS

[The thoughtful, capable, and ethical replacement for Windows and macOS ⋅ elementary OS](https://elementary.io)

[Elementary OS 6 Odin | Hacker News](https://news.ycombinator.com/item?id=28130560)
[elementary OS 6 Odin Available Now ⋅ elementary Blog](https://blog.elementary.io/elementary-os-6-odin-released/)

[Elementary OS is imploding | Hacker News](https://news.ycombinator.com/item?id=30611748)
[elementary OS is imploding - by Bryan Lunduke](https://lunduke.substack.com/p/elementary-os-is-imploding)

## distros - Elive

[Elive - Fast, Beautiful and Powerful OS](https://www.elivecd.org)
Elive is a very optimized linux, it works very fast in old computers, feature a unique experience and beautiful desktop with tons of features for daily use

## distros - -e-

/e/

[Review of /e/ - Android-based alternative for mobile phones | Hacker News](https://news.ycombinator.com/item?id=32414215)
[/e/ OS Review on Murena Teracube 2e · The New Leaf Journal](https://thenewleafjournal.com/review-of-e-an-android-alternative-for-mobile-phones/)

## distros - EndeavourOS

[EndeavourOS - A terminal-centric distro with a dynamic and friendly community in its core](https://endeavouros.com/)

## distros - Essence

[Essence: Desktop operating system built from scratch | Hacker News](https://news.ycombinator.com/item?id=29950740)
[Essence: A desktop OS built from scratch, for control and simplicity | Hacker News](https://news.ycombinator.com/item?id=37671419)
[Essence](https://nakst.gitlab.io/essence)

## distros - Fedora

[Fedora Workstation](https://getfedora.org/)
Fedora Workstation is a secure, reliable, and user-friendly Linux distribution developed by the Fedora Project.

[I don't understand Fedora Silverblue... : Fedora](https://old.reddit.com/r/Fedora/comments/x3ehf8/i_dont_understand_fedora_silverblue)

[The Fedora Project Remains Community Driven | TheEvilSkeleton](https://theevilskeleton.gitlab.io/2022/09/30/the-fedora-project-remains-community-driven.html)

[Mark my words fedora is the future : Fedora](https://old.reddit.com/r/Fedora/comments/11ekg1z/mark_my_words_fedora_is_the_future)

[Fedora Security Lab](https://labs.fedoraproject.org/security/download/index.html)

[Fedora Spins](https://spins.fedoraproject.org)

[Index of /lookaside](https://src.fedoraproject.org/lookaside/)

[Fedora Silverblue/Kinoite or Regular Fedora : r/Fedora](https://www.reddit.com/r/Fedora/comments/u6se13/fedora_silverbluekinoite_or_regular_fedora/)

[Fedora](https://mirrors.fedoraproject.org/mirrorlist?repo=epel-6&arch=x86_64)
Fedora Mirrors list for EPEL-6 and arch x86_64
[Fedora Mirror Manager](https://admin.fedoraproject.org/mirrormanager/)

## distros - Fuchsia OS

[A Kernel Hacker Meets Fuchsia OS | Hacker News](https://news.ycombinator.com/item?id=31497827)
[A Kernel Hacker Meets Fuchsia OS | Alexander Popov](https://a13xp0p0v.github.io/2022/05/24/pwn-fuchsia.html)

[Fuchsia Workstation | Hacker News](https://news.ycombinator.com/item?id=30827210)
[Build Workstation  |  Fuchsia](https://web.archive.org/web/20230605122610/https://fuchsia.dev/fuchsia-src/development/build/build_workstation)

## distros - GalliumOS

[GalliumOS - A fast and lightweight Linux distro for ChromeOS devices](https://galliumos.org/)

## distros - Gentoo

[Gentoo goes Binary | Hacker News](https://news.ycombinator.com/item?id=38804135)
[Gentoo goes Binary! - Gentoo Linux](https://www.gentoo.org/news/2023/12/29/Gentoo-binary.html)

[gentoo download | SourceForge.net](https://sourceforge.net/projects/gentoo)

[Gentoo Portage Overlays News](https://gpo.zugaina.org/)

[Funtoo](https://www.funtoo.org/Welcome)
[Funtoo articles (Linux)](http://www.funtoo.org/Category:Articles)

## distros - Gentoo - Pentoo

[Pentoo](https://www.pentoo.ch/)
is a security-focused livecd based on Gentoo.

## distros - Gentoo - Redcore Linux

[Home | Redcore Linux Project](https://redcorelinux.org/)

## distros - Gentoo - TinHat

[Tinhat](https://sourceforge.net/projects/tinhat)
[Tin Hat](http://tinhat233xymse34.onion/)

## distros - GoboLinux

[GoboLinux | Hacker News](https://news.ycombinator.com/item?id=26002251)
[Gobolinux : Redefining Linux filesystem hierarchy | Hacker News](https://news.ycombinator.com/item?id=29714825)
[GoboLinux - the alternative Linux distribution](https://www.gobolinux.org/)

## distros - GrapheneOS

[Graphene OS has made some allegations AGAINST Microg on Twitter. Is it true?](https://old.reddit.com/r/MicroG/comments/qn8xan/graphene_os_has_made_some_allegations_against/)

[GrapheneOS finds Bluetooth memory corruption via ARM MTE | Hacker News](https://news.ycombinator.com/item?id=39668053)
[GrapheneOS: "Our hardware memory tagging su…" - GrapheneOS Mastodon](https://grapheneos.social/@GrapheneOS/112066872276203917)

## distros - Guix

[Guix Workflow Language | Guix Workflow Language](https://guixwl.org)

[GNU Guix transactional package manager and distribution - GNU Guix🆓](https://guix.gnu.org)
[Cuirass - GNU Guix🆓](https://guix.gnu.org/en/cuirass)

[I Love Arch, but GNU Guix Is My New Distro | Hacker News](https://news.ycombinator.com/item?id=29264888)
[I Love Arch But Gnu Guix Is My New Distro](https://boilingsteam.com/i-love-arch-but-gnu-guix-is-my-new-distro/)

## distros - Haiku OS

[Home | Haiku Project](https://www.haiku-os.org)

[Haiku R1/beta4 | Hacker News](https://news.ycombinator.com/item?id=34109349)
[R1/beta4 - Release Notes | Haiku Project](https://www.haiku-os.org/get-haiku/r1beta4/release-notes/)

## distros - Homebrew

[Homebrew 3.0 | Hacker News](https://news.ycombinator.com/item?id=26035787)
[3.0.0 - Homebrew](https://brew.sh/2021/02/05/homebrew-3.0.0/)

[Homebrew 4.0.0 | Hacker News](https://news.ycombinator.com/item?id=34817222)
[4.0.0 - Homebrew](https://brew.sh/2023/02/16/homebrew-4.0.0/)

[Our audit of Homebrew | Hacker News](https://news.ycombinator.com/item?id=41114839)
[Our audit of Homebrew | Trail of Bits Blog](https://blog.trailofbits.com/2024/07/30/our-audit-of-homebrew/)

## distros - Horizon Linux

[Horizon Linux: arm64 Linux patched to run programs for the Nintendo Switch | Hacker News](https://news.ycombinator.com/item?id=32464955)
[kentjhall/horizon-linux: arm64 Linux patched to run programs for the Nintendo Switch's Horizon OS](https://github.com/kentjhall/horizon-linux)

## distros - Hubris

[Hubris - A small operating system for deeply-embedded computer systems | Hacker News](https://news.ycombinator.com/item?id=29390751)
[Hubris and Humility / Oxide](https://oxide.computer/blog/hubris-and-humility)
[Servers as they should be - shipping early 2022 | Hacker News](https://news.ycombinator.com/item?id=27294471)
[Oxide Computer Company](https://oxide.computer/)

## distros - illumos

[illumos](https://illumos.org/)

[Helios: A distribution of Illumos powering the Oxide Rack | Hacker News](https://news.ycombinator.com/item?id=39178521)
[oxidecomputer/helios: Helios: Or, a Vision in a Dream. A Fragment.](https://github.com/oxidecomputer/helios)

## distros - Kali Linux

[Kali Linux 2023.1 introduces 'Purple' distro for defensive security | Hacker News](https://news.ycombinator.com/item?id=35156764)
[Home · Wiki · Kali Linux / kali-purple / Documentation · GitLab](https://gitlab.com/kalilinux/kali-purple/documentation/-/wikis/home)

[Kali Linux](https://www.kali.org/)
Linux distribution used for Penetration Testing, Ethical Hacking and network security assessments.
[Index of /](https://cdimage.kali.org/)

## distros - Lightwhale

[I've made a single-purpose Linux distro](https://old.reddit.com/r/linux/comments/159mktm/ive_made_a_singlepurpose_linux_distro/)

## distros - Linux Mint

[Linux Mint drops Ubuntu Snap packages | Hacker News](https://news.ycombinator.com/item?id=23771847)
[Linux Mint drops Ubuntu Snap packages [LWN.net]](https://lwn.net/Articles/825005/)

[Kids find a security flaw in Linux Mint by mashing keys | Hacker News](https://news.ycombinator.com/item?id=25843874)
[Screensaver lock by-pass via the virtual keyboard · Issue #354 · linuxmint/cinnamon-screensaver](https://github.com/linuxmint/cinnamon-screensaver/issues/354)

## distros - linux vs bsd

[We're migrating many of our servers from Linux to FreeBSD | Hacker News](https://news.ycombinator.com/item?id=30057549)
[Why we're migrating (many of) our servers from Linux to FreeBSD -](https://it-notes.dragas.net/2022/01/24/why-were-migrating-many-of-our-servers-from-linux-to-freebsd/)

[Show HN: Porting OpenBSD Pledge() to Linux | Hacker News](https://news.ycombinator.com/item?id=32096801)
[Porting OpenBSD pledge() to Linux](https://justine.lol/pledge/)

## distros - Maemo

[Maemo Leste - Maemo Leste](https://maemo-leste.github.io)

## distros - Maestro

[Maestro: A Linux-compatible kernel in Rust | Hacker News](https://news.ycombinator.com/item?id=38852360)
[llenotre/maestro: Unix-like kernel written in Rust](https://github.com/llenotre/maestro)
[Luc Lenôtre - Blog](https://blog.lenot.re/)

## distros - Manjaro

[[HowTo] become a Manjaro power user when you're a wizard at Windows but a N00b at Manjaro/Linux - Contributions/Tutorials - Manjaro Linux Forum](https://forum.manjaro.org/t/howto-become-a-manjaro-power-user-when-youre-a-wizard-at-windows-but-a-n00b-at-manjaro-linux/13646#other-tips-and-tricks-16)

[Manjaro](https://manjaro.org/)

## distros

[Best Linux distros of 2023 | TechRadar](https://www.techradar.com/best/best-linux-distros)

[Best Linux Distros for Kids in 2023: Prepare the Young Ones for the Future](https://www.blackdown.org/best-linux-distros-for-kids)

[11 Best Linux Gaming Distributions in 2023](https://itsfoss.com/linux-gaming-distributions/)

## distros - Minix

[Minix - Wikipedia](https://en.wikipedia.org/wiki/Minix)

## distros - MOFO Linux

[MOFO Linux | Anti Censorship Linux](https://mofolinux.com/)
Linux OS that protects privacy/avoids censorship

## distros - MX Linux

[MX Linux - Midweight Simple Stable Desktop OS](https://mxlinux.org/)

## distros - NethServer

[NethServer - operating system for the Linux enthusiast](https://www.nethserver.org/)

## distros - NixOS

[NixOS RFC 136 approved: A plan to stabilize the new CLI and Flakes incrementally | Hacker News](https://news.ycombinator.com/item?id=37105524)
[[RFC 0136] A plan to stabilize the new CLI and Flakes incrementally by Ericson2314 · Pull Request #136 · NixOS/rfcs](https://github.com/NixOS/rfcs/pull/136)

[The Curse of NixOS | Hacker News](https://news.ycombinator.com/item?id=30057287)
[Wesley Aptekar-Cassels | The Curse of NixOS](https://blog.wesleyac.com/posts/the-curse-of-nixos)

[Our Roadmap for Nix | Hacker News](https://news.ycombinator.com/item?id=32374113)
[Our roadmap for Nix - Tweag](https://www.tweag.io/blog/2022-08-04-tweag-and-nix-future/)

[The NixOS Foundation's Call to Action: S3 Costs Require Community Support | Hacker News](https://news.ycombinator.com/item?id=36173020)
[The NixOS Foundation's Call to Action: S3 Costs Require Community Support - Announcements - NixOS Discourse](https://discourse.nixos.org/t/the-nixos-foundations-call-to-action-s3-costs-require-community-support/28672)

[NixOS Reproducible Builds: minimal ISO successfully independently rebuilt | Hacker News](https://news.ycombinator.com/item?id=38057591)
[NixOS Reproducible Builds: minimal installation ISO successfully independently rebuilt - Announcements - NixOS Discourse](https://discourse.nixos.org/t/nixos-reproducible-builds-minimal-installation-iso-successfully-independently-rebuilt/34756)

[Nixos-unstable's ISO_minimal.x86_64-Linux is 100% reproducible | Hacker News](https://news.ycombinator.com/item?id=27573393)
[Nixos-unstable's iso_minimal.x86_64-linux is 100% reproducible! - Development - NixOS Discourse](https://discourse.nixos.org/t/nixos-unstable-s-iso-minimal-x86-64-linux-is-100-reproducible/13723)

[Nix: Taming Unix with Functional Programming | Hacker News](https://news.ycombinator.com/item?id=32355327)
[Nix - taming Unix with functional programming - Tweag](https://www.tweag.io/blog/2022-07-14-taming-unix-with-nix/)

[~ehmry/sigil - sourcehut git](https://git.sr.ht/~ehmry/sigil)

## distros - Oasis

[Oasis - a small, statically-linked Linux system | Hacker News](https://news.ycombinator.com/item?id=39142748)
[Oasis: Small statically-linked Linux system | Hacker News](https://news.ycombinator.com/item?id=32458744)
[oasislinux/oasis: a small statically-linked linux system](https://github.com/oasislinux/oasis)

## distros - OmniOS

[OmniOS Community Edition](https://omnios.org/)

## distros - Oracle Solaris

[Oracle Solaris 11 | Oracle](https://www.oracle.com/solaris/solaris11)

## distros - Parrot Security OS

[Parrot Security OS](https://www.parrotsec.org/)
cyber security GNU/Linux environment.
[Parrot Security](https://twitter.com/ParrotSec)
[Index of /](https://archive.parrotsec.org/)

[Parrot Security OS - Online in the Cloud](https://www.onworks.net/os-distributions/special-os/free-parrot-security-os-online)

## distros - Plan 9

[Plan 9 from Bell Labs in Cyberspace | Hacker News](https://news.ycombinator.com/item?id=26554539)
[Plan 9 from Bell Labs in Cyberspace! - Nokia Bell Labs](https://www.bell-labs.com/institute/blog/plan-9-bell-labs-cyberspace/)

## distros - POP! OS

[5 Years of Pop_OS | Hacker News](https://news.ycombinator.com/item?id=33294448)
[Celebrating 5 Years of Pop!_OS - System76 Blog](https://blog.system76.com/post/celebrating-5-years-of-pop_os)

[System76 Developing "Cosmic" Desktop Environment | Hacker News](https://news.ycombinator.com/item?id=26798080)
[system76 on Tumblr: COSMIC to Arrive in June Release of Pop!_OS 21.04](https://www.tumblr.com/system76/648371526931038208/cosmic-to-arrive-in-june-release-of-popos-2104)

[System76 Open Firmware | Hacker News](https://news.ycombinator.com/item?id=35431119)
[GitHub - system76/firmware-open: System76 Open Firmware](https://github.com/system76/firmware-open)

[System76's coreboot open firmware manages to disable Intel ME for Raptor Lake | Hacker News](https://news.ycombinator.com/item?id=36166649)
[Major Updates for System76 Open Firmware! - System76 Blog](https://blog.system76.com/post/major-updates-for-system76-open-firmware-june-2023/)

[Exploring System76's New Rust Based Desktop Environment | Hacker News](https://news.ycombinator.com/item?id=29924803)
[Exploring System76's New Rust Based Desktop Environment | Devloop](https://web.archive.org/web/20230521195236/https://blog.edfloreshz.dev/articles/linux/system76/rust-based-desktop-environment/)

[HP Dev One Laptop with Pop_OS | Hacker News](https://news.ycombinator.com/item?id=31453125)
[HP Dev One | Home Page](https://hpdevone.com/)

## distros - POP! OS vs Mac

[Switching from macOS to Pop_OS | Hacker News](https://news.ycombinator.com/item?id=29950152)
[Switching from macOS to Pop!_OS - System76 Support](https://support.system76.com/articles/switch-from-macos-to-popos/)

## distros - Postmarket OS

[postmarketOS // real Linux distribution for phones](https://postmarketos.org)

## distros - PureOS

[PureOS](https://www.pureos.net/)

## distros - Qubes OS

[Qubes OS: A reasonably secure operating system | Qubes OS](https://www.qubes-os.org)
a security-oriented OS that uses Xen-based virtualization.
[QUBES OS](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion/)

## distros - Raspbian

[FrontPage - Raspbian](https://www.raspbian.org)

## distros - ReactOS

[Front Page | ReactOS Project](https://reactos.org/)

## distros - Red Hat (RHEL)

NOTE: THIS MIXES WITH TT NPO

[SUSE is forking RHEL | Hacker News](https://news.ycombinator.com/item?id=36678079)
[SUSE Preserves Choice in Enterprise Linux by Forking RHEL with a $10+ Million Investment | SUSE](https://www.suse.com/news/SUSE-Preserves-Choice-in-Enterprise-Linux/)

[Announcing Open-sourced & Community-Driven RHEL Fork by CloudLinux](https://blog.cloudlinux.com/announcing-open-sourced-community-driven-rhel-fork-by-cloudlinux)

[Red Hat Customer Portal](https://access.redhat.com/solutions/504583)
Package not available to the client systems after rhnpush

[Red Hat Customer Portal](https://access.redhat.com/solutions/8036)
How to re-register the system with Red Hat Network (RHN) Classic or Red Hat Satellite?

[Red Hat Customer Portal](https://access.redhat.com/documentation/en-US/Red_Hat_Network_Satellite/5.0/html/Channel_Management_Guide/Channel_Management_Guide-Uploading_Packages_to_SAT-Using_the_RHNPUSHapplication.html)
Using the RHN Push application

[Red Hat Customer Portal](https://access.redhat.com/solutions/737373)
Satellite 5.6: unable to register RHEL 7 client system due to rhn-setup package not included in Minimal installation

## distros - Red Hat (RHEL) - Oracle Linux

[Oracle](https://www.oracle.com/linux)

[Oracle Linux - Wikipedia](https://en.wikipedia.org/wiki/Oracle_Linux)

[Oracle Linux: A better alternative to CentOS](https://linux.oracle.com/switch/centos/)

## distros - Redox

[Redox - Your Next(Gen) OS - Redox - Your Next(Gen) OS](https://www.redox-os.org/)

## distros - Ripple

[unfathomable software](https://src.unfathomable.blue)

## distros - Security Onion

[Security Onion](https://securityonion.net/)
Linux distro for intrusion detection, enterprise security monitoring, and log management.

## distros - SerenityOS

[SerenityOS](https://serenityos.org/)
[GitHub - SerenityOS/serenity: The Serenity Operating System](https://github.com/SerenityOS/serenity)

[SerenityOS demo at Handmade Seattle 2021 [video] | Hacker News](https://news.ycombinator.com/item?id=29270776)
[Media | Handmade Cities](https://handmadecities.com/media/)

[The 4th Year of SerenityOS | Hacker News](https://news.ycombinator.com/item?id=33151658)
[The 4th year of SerenityOS](https://serenityos.org/happy/4th/)

[SerenityOS Browser now passes the Acid3 test | Hacker News](https://news.ycombinator.com/item?id=30853392)
[Andreas Kling on X: "The SerenityOS Browser now passes the Acid3 test! 🥳🐞🌍 AFAIK we're the first new open source browser to reach this milestone since the test originally came out. This has been a team effort over the last couple of weeks, and I'm so proud of everyone who contributed! 🤓❤️ https://t.co/Vw8GkHWSaj" / X](https://twitter.com/awesomekling/status/1508953394836353024)

[SerenityOS: A remarkable achievement for a small project • The Register](https://www.theregister.com/2022/03/31/serenityos)

[How I make a living working on SerenityOS | Hacker News](https://news.ycombinator.com/item?id=33386163)
[How I make a living working on SerenityOS - Andreas Kling - I like computers!](https://awesomekling.github.io/How-I-make-a-living-working-on-SerenityOS/)
[I quit my job to focus on SerenityOS full time | Hacker News](https://news.ycombinator.com/item?id=27317655)
[I quit my job to focus on SerenityOS full time - Andreas Kling - I like computers!](https://awesomekling.github.io/I-quit-my-job-to-focus-on-SerenityOS-full-time/)

[andreas kling](https://awesomekling.github.io/)
the author of serenityos' blog
[Excellence is a habit, but so is failure | Hacker News](https://news.ycombinator.com/item?id=36628356)
[Excellence is a habit, but so is failure - Andreas Kling - I like computers!](https://awesomekling.github.io/Excellence-is-a-habit-but-so-is-failure/)

[I'm forking Ladybird and stepping down as SerenityOS BDFL | Hacker News](https://news.ycombinator.com/item?id=40560768)
[I'm forking Ladybird and stepping down as SerenityOS BDFL](https://awesomekling.substack.com/p/forking-ladybird-and-stepping-down-serenityos)

## distros - Serpent OS

[Home | Serpent OS](https://www.serpentos.com/)
[Serpent OS · GitHub](https://github.com/serpent-os)

## distros - skiftOS

[skiftOS](https://skiftos.org/)

## distros - Slackware

[Slackware](http://www.slackware.com/)
the most "Unix-like" Linux distribution.

## distros - SteamOS

[I forked SteamOS for my living room PC | Hacker News](https://news.ycombinator.com/item?id=38823101)
[How I forked SteamOS for my living room PC - iliana.fyi](https://iliana.fyi/blog/build-your-own-steamos-updates/)

[Steam Top 50 Games: Over 70% now work on Linux | Hacker News](https://news.ycombinator.com/item?id=28492227)
[Out of the Top Fifty Games on Steam, 70% Work on Linux](https://boilingsteam.com/out-of-the-top-50-games-70-work-on-linux-now/)

[Linux surpasses the Mac among Steam gamers | Hacker News](https://news.ycombinator.com/item?id=36993968)
[Linux surpasses the Mac among Steam gamers | Ars Technica](https://arstechnica.com/gadgets/2023/08/linux-surpasses-the-mac-among-steam-gamers/)

[ProtonDB | Gaming know-how from the Linux and Steam Deck community](https://www.protondb.com/)

## distros - Tails

[Tails is a portable OS that protects against surveillance and censorship | Hacker News](https://news.ycombinator.com/item?id=37509560)
[Tails - Home](https://tails.net/)

[Tails](https://tails.boum.org)
a live system that aims to preserve your privacy and anonymity.
[Tails](https://tails.boum.org/index.en.html)
Tails is a live system that aims to preserve your privacy and anonymity

## distros - Tiny Core Linux

[Tiny Core Linux is the smallest Linux distribution on the market with a big heart](https://www.techrepublic.com/article/tiny-core-linux-is-the-smallest-linux-distribution-on-the-market-with-a-big-heart/)

[Tiny Core Linux 13.0 is a full Linux desktop in 22 MB | Hacker News](https://news.ycombinator.com/item?id=31977164)
[Tiny Core Linux 13.0 is a full Linux desktop in 22 MB #Linux - Adafruit Industries - Makers, hackers, artists, designers and engineers!](https://blog.adafruit.com/2022/02/11/tiny-core-linux-13-0-is-a-full-linux-desktop-in-22-mb-linux/)

## distros - Trisquel

[Trisquel GNU/Linux - Run free!](https://trisquel.info/en)

## distros - Tsurugi Linux

[Tsurugi Linux | Digital Forensics, Osint and malware analysis Linux Distribution](https://tsurugi-linux.org/)

## distros - Ubuntu - Backbox

[Backbox Linux](https://www.backbox.org/)
penetration test and security assessment oriented Ubuntu-based Linux distribution.

## distros - Ubuntu - Kodachi

[Kodachi](https://www.digi77.com/linux-kodachi)

## distros - Ubuntu - MATE

[Ubuntu MATE | For a retrospective future](https://ubuntu-mate.org/)

## distros - Ubuntu

[Ubuntu 20.04 LTS' snap obsession has snapped me off of it | Hacker News](https://news.ycombinator.com/item?id=24383276)
[Ubuntu 20.04 LTS' snap obsession has snapped me off of it - Uncertain Jatan](https://web.archive.org/web/20201101012448/https://personal.jatan.space/2020/09/05/ubuntu-snap-obsession-has-snapped-me-off-of-it/)

[Ubuntu 22.10 Kinetic Kudu | Hacker News](https://news.ycombinator.com/item?id=33275206)
[Canonical releases Ubuntu 22.10 Kinetic Kudu | Ubuntu](https://ubuntu.com/blog/canonical-releases-ubuntu-22-10-kinetic-kudu)

[Ubuntu Looking at Applying Low-Latency Optimizations to Its Generic Kernel | Hacker News](https://news.ycombinator.com/item?id=39173229)
[Ubuntu Looking At Applying Low-Latency Optimizations To Its Generic Kernel - Phoronix](https://www.phoronix.com/news/Ubuntu-Low-Lat-Generic-Kernel)

[Ask Ubuntu on Stack Exchange](https://askubuntu.com/questions/631077/problem-with-deluge-no-incoming-connection)
Problem with Deluge: “no incoming connection!”

## distros - Ubuntu - Rhino Linux

[I'm a pro Linux user, and this distribution is one of the most unique I've tried | ZDNET](https://www.zdnet.com/article/im-a-pro-linux-user-and-this-distribution-is-one-of-the-most-unique-ive-tried/)

## distros - Ubuntu - Vanilla OS

[Vanilla OS](https://vanillaos.org/)

## distros - Venom Linux

[Venom Linux](https://venomlinux.org/)

## distros - Void Linux

[GitHub - void-linux/void-packages: The Void source packages collection](https://github.com/void-linux/void-packages)
[Enter the void](https://voidlinux.org/)

## drivers

[A Linux Evening | Hacker News](https://news.ycombinator.com/item?id=34013195)
[A Linux evening](https://fabiensanglard.net/a_linux_evening/index.html)

## drivers - sex toys

[Empathy for the user having sex with your software | Hacker News](https://news.ycombinator.com/item?id=41021029)
[Butts Are Difficult | buttplug.io](https://docs.buttplug.io/docs/dev-guide/intro/buttplug-ethics/)

## drivers - speakers-mic

[AlsaProject](https://alsa-project.org/wiki/Main_Page)

## eBPF

[How io_uring and eBPF Will Revolutionize Programming in Linux | Hacker News](https://news.ycombinator.com/item?id=25222243)
[How io_uring and eBPF Will Revolutionize Programming in Linux - ScyllaDB](https://www.scylladb.com/2020/05/05/how-io_uring-and-ebpf-will-revolutionize-programming-in-linux/)

[New Relic to open-source Pixie's eBPF observability platform | Hacker News](https://news.ycombinator.com/item?id=25375170)
[Accelerating the Pixie community with New Relic | Pixie Labs Blog](https://web.archive.org/web/20210123201131/https://blog.pixielabs.ai/pixie-new-relic/)

## file system

[Vivek Gite](https://www.cyberciti.biz/faq/how-do-i-find-the-largest-filesdirectories-on-a-linuxunixbsd-filesystem/)
How Do I Find The Largest Top 10 Files and Directories On a Linux / UNIX / BSD?

[Michael Kwaku Aboagye](https://opensource.com/article/18/1/securing-linux-filesystem-tripwire)
(2018) Securing the Linux filesystem with Tripwire

## file system - xfs

[Those Using The XFS File-System Will Want To Avoid Linux 6.3 For Now: archlinux](https://www.reddit.com/r/archlinux/comments/13stqod/those_using_the_xfs_filesystem_will_want_to_avoid)

## firmware - libcdio

[GNU Compact Disc Input and Control Library (libcdio)🆓](https://www.gnu.org/software/libcdio)

## firmware

[LVFS: Home](https://fwupd.org)

[GitHub - linuxhw/hw-probe: Probe for hardware, check operability and find drivers](https://github.com/linuxhw/hw-probe)

[Linux Touchpad Like MacBook Update: Touchpad Gestures Now Shipping | Hacker News](https://news.ycombinator.com/item?id=29555822)
[Linux Touchpad like Macbook Update: Touchpad Gestures Now Shipping 🚢 - GitClear](https://www.gitclear.com/blog/linux_touchpad_update_december_2021)

## firmware - vcdimager

[GNU VCDImager - GNU Project - Free Software Foundation (FSF)🆓](https://www.gnu.org/software/vcdimager)

## GNU kernel

[GNU Hurd🆓](https://www.gnu.org/software/hurd)

[gnumach🆓](https://www.gnu.org/software/hurd/microkernel/mach/gnumach.html)

## linux bastion host

[Vivek Gite](https://www.cyberciti.biz/faq/linux-bastion-host/)
(2009) Configure Linux As Bastion Host

## linux blogs

[Red Hat Blog](https://www.redhat.com/en/blog)
Official Red Hat Blog

[Red Hat Enterprise Linux Blog](http://rhelblog.redhat.com/)
latest information on Red Hat's IT infrastructure products, offerings, and solutions

## linux conferences

[Red Hat Events](https://www.redhat.com/en/events)
Conferences, online events, on-demand webinars, and more

[OpenStack Summit](https://www.openstack.org/videos/)
All Videos archives

## linux culture

[Linux has achieved a 3% desktop market share | Hacker News](https://news.ycombinator.com/item?id=36676103)
[After 30 Years, Linux Finally Hits 3% Market Share](https://linuxiac.com/linux-hits-3-percent-market-share/)

[Linux Journal Is Back | Hacker News](https://news.ycombinator.com/item?id=24559589)
[Linux Journal is Back | Linux Journal](https://www.linuxjournal.com/content/linux-journal-back)

[The Unix Magic Poster | Hacker News](https://news.ycombinator.com/item?id=27029196)
[Jan-Piet Mens :: The Unix Magic poster](https://jpmens.net/2021/04/09/the-unix-magic-poster/)

[Valve is a wonderful upstream contributor to Linux and the open-source community | Hacker News](https://news.ycombinator.com/item?id=37612127)
[Valve Is A Wonderful Upstream Contributor To Linux & The Open-Source Community - Phoronix](https://www.phoronix.com/news/Valve-Upstream-Everything-OSS)

[I got robbed of my first kernel contribution | Hacker News](https://news.ycombinator.com/item?id=37671991)
[How I got robbed of my first kernel contribution - Ariel Miculas - Software Engineer at Cisco](https://ariel-miculas.github.io/How-I-got-robbed-of-my-first-kernel-contribution/)

[ARM64 Linux Workstation | Hacker News](https://news.ycombinator.com/item?id=35014677)
[Jason Eckert's Website and Blog](https://jasoneckert.github.io/myblog/ultimate-linux-arm64-workstation/)

[The SCO lawsuit, 20 years later | Hacker News](https://news.ycombinator.com/item?id=35012313)
[The SCO lawsuit, 20 years later [LWN.net]](https://lwn.net/Articles/924577/)

[Despite just 5.8% sales, over 38% of bug reports come from the Linux community (2021) | Hacker News](https://news.ycombinator.com/item?id=38392931)
[Despite having just 5.8% sales, over 38% of bug reports come from Linux | Hacker News](https://news.ycombinator.com/item?id=28978086)
[Despite having just 5.8% sales, over 38% of bug reports come from the Linux community : gamedev](https://old.reddit.com/r/gamedev/comments/qeqn3b/despite_having_just_58_sales_over_38_of_bug/)

[5 reasons why I love coding on Linux | Opensource.com](https://opensource.com/article/21/2/linux-programming)

[456: Cautionary - explain xkcd](https://www.explainxkcd.com/wiki/index.php/456:_Cautionary)

[349: Success - explain xkcd](https://www.explainxkcd.com/wiki/index.php/349:_Success)

[149: Sandwich - explain xkcd](https://www.explainxkcd.com/wiki/index.php/149:_Sandwich)

[278: Black Hat Support - explain xkcd](https://www.explainxkcd.com/wiki/index.php/278:_Black_Hat_Support)

[424: Security Holes - explain xkcd](https://www.explainxkcd.com/wiki/index.php/424:_Security_Holes)

[340: Fight - explain xkcd](https://www.explainxkcd.com/wiki/index.php/340:_Fight)

[323: Ballmer Peak - explain xkcd](https://www.explainxkcd.com/wiki/index.php/323:_Ballmer_Peak)

[UNIX / Platform - TV Tropes](https://tvtropes.org/pmwiki/pmwiki.php/Platform/UNIX)

[Enlightenmentware | Hacker News](https://news.ycombinator.com/item?id=40419856)
[Enlightenmentware](https://mmapped.blog/posts/28-enlightenmentware.html)

[Geek Flare](https://geekflare.com/category/web-infrastructure/unix/)
general Unix articles, tips, tools for managing web infrastructure

[Steven J. Vaughan-Nichols ](http://www.zdnet.com/article/linus-linux-torvalds-gives-security-developers-guidance/)
Linus 'Linux' Torvalds gives security developers guidance

[nixCraft](https://www.cyberciti.biz/)
linux tips, hacks, tutorials and ideas
:star:

[Red Hat](https://www.youtube.com/channel/UC9CjkhQp1jX8Hbtbg6OZ9dw)
Red Hat Summit Youtube Channel

[nixCraft - Linux Tips, Hacks, Tutorials, And Ideas In Blog](https://www.cyberciti.biz/)
linux and unix tutorials for new and seasoned sysadmin.

[Cat-v.org Random Contrarian Insurgent Organization](https://cat-v.org/)
A _contrarian_ tech group

## linux culture vs faang

[Xbox Cloud throttles performance if user agent is Linux | Hacker News](https://news.ycombinator.com/item?id=31985605)
[Quality on linux : xcloud](https://old.reddit.com/r/xcloud/comments/vrfmuz/quality_on_linux/)

[Everyone seems to forget why GNOME and GNOME 3 and Unity happened | Hacker News](https://news.ycombinator.com/item?id=32257412)
[liam_on_linux | Everyone seems to forget why GNOME and GNOME 3 and Unity happened](https://liam-on-linux.dreamwidth.org/85359.html)

## linux culture vs hardware - apple m

[Serial adapter/reboot controller for Apple M1/M2 | Hacker News](https://news.ycombinator.com/item?id=37298506)
[Serial adapter / reboot controller for Apple M1/M2 from aaafnraa on Tindie](https://www.tindie.com/products/aaafnraa/serial-adapter-reboot-controller-for-apple-m1m2/)

[Native Linux GPU Driver for Apple M1 | Hacker News](https://news.ycombinator.com/item?id=33019316)
[Asahi Lina / 朝日リナ // @lina@vt.social on X: "✨🎊🎉IT WORKS!!!!🎉🎊✨ 🦀🐧🍎🔻🧊🇼👩🔥🦊⚙️ GNOME runs!! Firefox works!! You can watch YouTube, play Neverball, run KDE apps, and more!! No crashes!!!🎉🎉 On a native Linux GPU driver for Apple M1!!🚀 Check out the mini stream where I show it off!!! ▶️https://t.co/g0R1JZI6Pe" / X](https://twitter.com/LinaAsahi/status/1575343067892051968)

[Linux M1 GPU driver passes 99% of the dEQP-GLES2 compliance tests | Hacker News](https://news.ycombinator.com/item?id=33288706)
[Asahi Lina / 朝日リナ // @lina@vt.social on X: "🎉🎉🎉 My Linux M1 GPU driver passes &gt;99% of the dEQP-GLES2 compliance tests!!!!! 🎉🎉🎉 Most of this is thanks to @alyssarzg's prior work on macOS, but now I can replicate it on Linux! ^^ https://t.co/BTI4AIUTkC" / X](https://twitter.com/linaasahi/status/1583444549648543744)

[KDE runs on the Apple M2 with full GPU acceleration | Hacker News](https://news.ycombinator.com/item?id=33744598)
[Asahi Lina (朝日リナ) // nullptr::live: "✨ KDE runs on the Apple M2!!!!…" - VT Social](https://vt.social/@lina/109405566112910885)

[M1 Pro 14" MacBook Pro Running KDE Plasma 5 on Arch Linux ARM | Hacker News](https://news.ycombinator.com/item?id=29197509)
[Hector Martin on Twitter: "Say hi to an M1 Pro 14" MacBook Pro running KDE Plasma 5 on Arch Linux ARM! Notch compatible! I made NVMe work today and decided it's time to properly install a distro ;)… https://t.co/gL5HjXjZ0f"](https://web.archive.org/web/20211110174438/https://twitter.com/marcan42/status/1458473546225577987)

[Asahi Linux for M1 Macs: progress report for September 2021 | Hacker News](https://news.ycombinator.com/item?id=28762744)
[Progress Report: September 2021 - Asahi Linux](https://asahilinux.org/2021/10/progress-report-september-2021/)
[Asahi Linux for Apple M1 progress report, August 2021 | Hacker News](https://news.ycombinator.com/item?id=28180135)
[Progress Report: August 2021 - Asahi Linux](https://asahilinux.org/2021/08/progress-report-august-2021/)

[Dissecting the Apple M1 GPU, part I | Hacker News](https://news.ycombinator.com/item?id=25673631)
[Rosenzweig - Dissecting the Apple M1 GPU, part I](https://rosenzweig.io/blog/asahi-gpu-part-1.html)
[Dissecting the Apple M1 GPU, Part II | Hacker News](https://news.ycombinator.com/item?id=25873887)
[Rosenzweig - Dissecting the Apple M1 GPU, part II](https://rosenzweig.io/blog/asahi-gpu-part-2.html)
[Dissecting the Apple M1 GPU, Part III | Hacker News](https://news.ycombinator.com/item?id=26858053)
[Rosenzweig - Dissecting the Apple M1 GPU, part III](https://rosenzweig.io/blog/asahi-gpu-part-3.html)
[Dissecting the Apple M1 GPU, Part IV | Hacker News](https://news.ycombinator.com/item?id=27019249)
[Rosenzweig - Dissecting the Apple M1 GPU, part IV](https://rosenzweig.io/blog/asahi-gpu-part-4.html)

[The first conformant M1 GPU driver | Hacker News](https://news.ycombinator.com/item?id=37224042)
[Rosenzweig - The first conformant M1 GPU driver](https://rosenzweig.io/blog/first-conformant-m1-gpu-driver.html)

[Conformant OpenGL 4.6 on the M1 | Hacker News](https://news.ycombinator.com/item?id=39371669)
[Rosenzweig - Conformant OpenGL 4.6 on the M1](https://rosenzweig.io/blog/conformant-gl46-on-the-m1.html)

[Apple Silicon M1: A Developer's Perspective | Hacker News](https://news.ycombinator.com/item?id=25238608)
[Apple Silicon M1: A Developer's Perspective | steipete's blog](https://steipete.com/posts/apple-silicon-m1-a-developer-perspective/)

[Initial M1 support merged into Linux SoC tree | Hacker News](https://news.ycombinator.com/item?id=26746983)
[Merge branch 'arm/apple-m1' into for-next - kernel/git/soc/soc.git - Unnamed repository; edit this file 'description' to name the repository.](https://git.kernel.org/pub/scm/linux/kernel/git/soc/soc.git/commit/?h=for-next&id=0d5fe4b31785b732b71e764b55cda5c8d6e3bbbf)

[Linux 6.2: The first mainstream Linux kernel for Apple M1 chips arrives | Hacker News](https://news.ycombinator.com/item?id=34873357)
[Linux 6.2: The first mainstream Linux kernel for Apple M1 chips arrives | ZDNET](https://www.zdnet.com/article/linux-6-2-the-first-mainstream-linux-kernel-for-apple-m1-chips-arrives/)

## linux culture vs hardware

[GNU Parallel - GNU Project - Free Software Foundation🆓](https://www.gnu.org/software/parallel)
Execute Commands/Scripts in Parallel using Multiple Computers
GNU parallel is a shell tool for executing jobs in parallel using one or more computers.

[GNU Pth - The GNU Portable Threads🆓](https://www.gnu.org/software/pth)

[SHMM Shared Memory Manager - GNU Project - Free Software Foundation🆓](https://www.gnu.org/software/shmm)

## linux gaming

[Valve's Proton Has Brought 6000 Windows Games to Linux So Far | Hacker News](https://news.ycombinator.com/item?id=22922774)
[Proton Has Brought About 6000 Games to Linux So Far](https://boilingsteam.com/proton-brought-about-6000-games-to-linux-so-far/)

[Celebrating 6 years since Valve announced Steam Play Proton for Linux | Hacker News](https://news.ycombinator.com/item?id=41316999)
[Celebrating 6 years since Valve announced Steam Play Proton for Linux | GamingOnLinux](https://www.gamingonlinux.com/2024/08/celebrating-6-years-since-valve-announced-steam-play-proton-for-linux/)

## linux - handwriting-ocr

[Pens and Tablets for Linux | Hacker News](https://news.ycombinator.com/item?id=30874256)
[Wacom Leads the Way with Pens and Tablets for Linux](https://web.archive.org/web/20230322165327/https://community.wacom.com/eu/enterprise/wacom-leads-the-way-with-pens-and-tablets-for-linux/)

## linux kernel

["Fast Kernel Headers" Tree -v1: Eliminate the Linux Kernel's "Dependency Hell" | Hacker News](https://news.ycombinator.com/item?id=29777048)
[[PATCH 0000/2297] [ANNOUNCE, RFC] "Fast Kernel Headers" Tree -v1: Eliminate the Linux kernel's "Dependency Hell" [LWN.net]](https://lwn.net/ml/linux-kernel/YdIfz+LMewetSaEB@gmail.com/)

[Linux Kernel RNG is now Blake2 instead of SHA1 and 3x faster | Hacker News](https://news.ycombinator.com/item?id=29742977)
[Filippo Valsorda @filippo.abyssdomain.expert on X: "Damn. @zx2c4 has been the Linux random driver maintainer for like a hot minute, and /dev/[u]random is now 100% SHA-1 free and 370% faster. Amazing. https://t.co/qh5eh0L9lN https://t.co/CuQD8pDrIg" / X](https://twitter.com/FiloSottile/status/1476698207413493766)

[Moving the Linux Kernel to Modern C | Hacker News](https://news.ycombinator.com/item?id=30459634)
[Moving the kernel to modern C [LWN.net]](https://lwn.net/Articles/885941/)

[Linux 5.19 | Hacker News](https://news.ycombinator.com/item?id=32303592)
[Linux 5.19 [LWN.net]](https://lwn.net/Articles/903033/)

[Linux Kernel 6.0 | Hacker News](https://news.ycombinator.com/item?id=33062252)
[Kernel 6.0 released [LWN.net]](https://lwn.net/Articles/910087/)

## linux news

[NetWorld](https://www.networkworld.com/)
[Security news, trend analysis and opinion](https://www.networkworld.com/category/security)
Linux News

[LinuxJournal](https://www.linuxjournal.com/)
Linux News

[9to5Linux](https://9to5linux.com/)
Linux News

[Phoronix](https://phoronix.com/)
Linux News

[LXer](http://lxer.com/)
Linux News

[TuxURLs](https://tuxurls.com/)
Linux News

[The Linux Foundation](https://www.youtube.com/channel/UCfX55Sx5hEFjoC3cNs6mCUQ)
The Linux Foundation Youtube Channel

[/r/linux](https://www.reddit.com/r/linux/)
discussions & news about linux on reddit

[Tux Machines](http://www.tuxmachines.org/)
a community-driven public service/news site which has been around for over a decade and primarily focuses on GNU/Linux

[DistroWatch](http://distrowatch.com/)
news and reviews of open source operating systems, with focus on Linux and BSD
[Security @ Distrowatch](http://distrowatch.com/search.php?category=Security)
Website dedicated to talking about, reviewing, and keeping up to date with open source operating systems.
http://distrowatch.org

## linux os

[Sandra Henry-Stocker](http://www.computerworld.com/article/3152772/linux/17-unix-tricks-for-a-happy-2017.html)
17 Unix tricks for a happy 2017

[TuxRadar](http://www.tuxradar.com/content/more-linux-tips-every-geek-should-know)
More Linux tips every geek should know

[TuxRadar](http://www.tuxradar.com/content/linux-tips-every-geek-should-know)
Linux tips every geek should know
:star:

[Al Williams](https://hackaday.com/2017/03/10/linux-fu-keeping-things-running/)
(2017) Linux-Fu: Keeping Things Running

[How we found and fixed an eBPF Linux kernel vulnerability | Hacker News](https://news.ycombinator.com/item?id=41189971)
[A deep dive into CVE-2023-2163: How we found and fixed an eBPF Linux Kernel Vulnerability - Google Bug Hunters](https://bughunters.google.com/blog/6303226026131456/a-deep-dive-into-cve-2023-2163-how-we-found-and-fixed-an-ebpf-linux-kernel-vulnerability)

## linux personal computers

[Poll: What's the best laptop for Linux these days? | Hacker News](https://news.ycombinator.com/item?id=34180508)

[Rant: Year of Linux on the desktop | Hacker News](https://news.ycombinator.com/item?id=34206055)
[Rant: year of Linux on the desktop](https://blog.liw.fi/posts/2022/goalposts/)

[The $8 Linux Computer | Hacker News](https://news.ycombinator.com/item?id=34024914)
[The Little Engineer That Could: The $8 linux computer (part 1.)](https://thelittleengineerthatcould.blogspot.com/2022/12/the-8-linux-computer.html)

[Running a Unix-like OS on a home-built CPU with a home-built C compiler (2020) | Hacker News](https://news.ycombinator.com/item?id=33761419)
[Running a Unix-like OS on a home-built CPU with a home-built C compiler | Hacker News](https://news.ycombinator.com/item?id=24680109)
[How we ran a Unix-like OS (Xv6) on our home-built CPU with our home-built C compiler | Fueled by Coffee](https://fuel.edby.coffee/posts/how-we-ported-xv6-os-to-a-home-built-cpu-with-a-home-built-c-compiler/)

[Linux on the laptop works so damn well that it's boring | Hacker News](https://news.ycombinator.com/item?id=32964519)
[Linux On The Laptop Works So Damn Well That It's Boring | by Clive Thompson | Medium](https://clivethompson.medium.com/linux-on-the-laptop-works-so-damn-well-that-its-boring-29014b347941)

[Lenovo ThinkPad P1 Gen3 Review - with Linux | Hacker News](https://news.ycombinator.com/item?id=31231968)
[Lenovo ThinkPad P1 Gen3 Review (with Linux) | Ernestas](https://ernestas.me/lenovo-thinkpad-p1-gen3)

## linux phones

[Do you really want Linux phones | Hacker News](https://news.ycombinator.com/item?id=26574731)
[Do you really want Linux phones](https://blog.brixit.nl/do-you-really-want-linux-phones/)

[Will Linux phones stay around this time? | Hacker News](https://news.ycombinator.com/item?id=27010556)
[LINMOB.net - Will Linux Phones stay around this time?](https://linmob.net/will-linux-phones-stay-around-this-time/)

[Lindroid | Hacker News](https://news.ycombinator.com/item?id=40705574)
[Erfan Abdi ➐ on X: "So finally today i can talk about this, most of you already know but I'll explain in thread🧵 Project: Lindroid✨✨ https://t.co/5TAnyqIfg6" / X](https://x.com/Khode_Erfan/status/1802331845633212554)

## linux pipelines

[The Beauty of Unix Pipelines | Hacker News](https://news.ycombinator.com/item?id=23420786)
[The beauty of Unix pipelines](https://prithu.dev/posts/unix-pipeline/)

[How fast are Linux pipes anyway? | Hacker News](https://news.ycombinator.com/item?id=31592934)
[How fast are Linux pipes anyway? (2022) | Hacker News](https://news.ycombinator.com/item?id=37782493)
[How fast are Linux pipes anyway?](https://mazzo.li/posts/fast-pipes.html)

## linux pipes

[Linux Pipes Are Slow | Hacker News](https://news.ycombinator.com/item?id=41348844)
[Linux Pipes are Slow | Quentin Santos](https://qsantos.fr/2024/08/25/linux-pipes-are-slow/)

## linux servers and sysops

[Reclaiming the lost art of Linux server administration | Hacker News](https://news.ycombinator.com/item?id=30118273)
[Reclaiming the lost art of Linux server administration | Pietro Rea](https://pietrorea.com/2022/01/28/reclaiming-the-lost-art-of-linux-server-administration/)

## linux tracing

[Give me 15 minutes and I'll change your view of Linux tracing](https://www.brendangregg.com/blog/2016-12-27/linux-tracing-in-15-minutes.html)

## linux vs apple

[Things I can't do on macOS which I can do on Ubuntu (2020) | Hacker News](https://news.ycombinator.com/item?id=31165505)
[Things I can't do on MacOS which I can do on Ubuntu - Terence Eden's Blog](https://shkspr.mobi/blog/2020/04/things-i-cant-do-on-macos-which-i-can-do-on-ubuntu/)

[More developers use Linux than Mac, according to 2022 StackOverflow survey | Hacker News](https://news.ycombinator.com/item?id=34163874)
[More Developers Use Linux than Mac, Report Shows - OMG! Linux](https://www.omglinux.com/devs-prefer-linux-to-mac-stackoverflow-survey/)

[I switched from macOS to Linux after 15 years of Apple | Hacker News](https://news.ycombinator.com/item?id=28320404)
[How I switched from macOS to Linux after 15 years of Apple](https://markosaric.com/linux/)

[Moving from Macbook to Linux | Hacker News](https://news.ycombinator.com/item?id=25163685)
[The Year of the Linux Desktop](https://monadical.com/posts/moving-to-linux-desktop.html)

[Fed up with the Mac, I spent six months with a Linux laptop | Hacker News](https://news.ycombinator.com/item?id=26677035)
[Carlos Fenollosa - Blog](https://cfenollosa.com/blog/fed-up-with-the-mac-i-spent-six-months-with-a-linux-laptop-the-grass-is-not-greener-on-the-other-side.html)

[Impressions from a first-time Mac user | Hacker News](https://news.ycombinator.com/item?id=30993350)
[Impressions from a first-time Mac user | Logan Marchione](https://loganmarchione.com/2022/04/impressions-from-a-first-time-mac-user/)

[Have an old iPad lying around? You might be able to make it run Linux soon | Hacker News](https://news.ycombinator.com/item?id=31624185)
[Have an old iPad lying around? You might be able to make it run Linux soon | Ars Technica](https://arstechnica.com/gadgets/2022/06/developers-get-linux-up-and-running-on-old-ipad-air-2-hardware/)

[We got Linux on the iPhone, iPad and other idevices | Hacker News](https://news.ycombinator.com/item?id=31679293)
[Linux on A7-A8X - Konrad Dybcio](https://konradybcio.pl/linuxona7/)

## memory management

[zswap - ArchWiki](https://wiki.archlinux.org/title/Zswap)

## mempool

[MemPool - GNU Project - Free Software Foundation🆓](https://www.gnu.org/software/mempool)

[The Linux kernel's inability to gracefully handle low memory pressure | Hacker News](https://news.ycombinator.com/item?id=20620545)
[LKML: "Artem S. Tashkinov": Let's talk about the elephant in the room - the Linux kernel's inability to gracefully handle low memory pressure](https://lkml.org/lkml/2019/8/4/15)

[Introduction to memory management - Memory Management Reference 4.0 documentation](https://www.memorymanagement.org/mmref/index.html)

## misc files

[Miscfiles - GNU Project - Free Software Foundation🆓](https://www.gnu.org/software/miscfiles)

## package manager - dnf

[Vultr](https://www.vultr.com/docs/use-dnf-to-manage-software-packages-on-centos-7)
Use DNF To Manage Software Packages On CentOS 7

## package manager

[package management - Where are my installed applications? - Ask Ubuntu](https://askubuntu.com/questions/9024/where-are-my-installed-applications)

[What NPM should do to stop a new colors attack | Hacker News](https://news.ycombinator.com/item?id=29877745)
[research!rsc: What NPM Should Do Today To Stop A New Colors Attack Tomorrow](https://research.swtch.com/npm-colors)

[GitHub - TekWizely/bingo: The missing package manager for golang binaries (its homebrew for "go install")](https://github.com/TekWizely/bingo)

[KDE and GNOME seeks $100k to turn Flathub into a Store for the Linux desktop | Hacker News](https://news.ycombinator.com/item?id=34916644)
[oss-virtual-incubator/proposals/flathub-linux-app-store.md at main · PlaintextGroup/oss-virtual-incubator[ARCHIVED]](https://github.com/PlaintextGroup/oss-virtual-incubator/blob/main/proposals/flathub-linux-app-store.md)

[New F-Droid repository format for faster and smaller updates | Hacker News](https://news.ycombinator.com/item?id=35002983)
[New repository format for faster and smaller updates | F-Droid - Free and Open Source Android App Repository](https://f-droid.org/2023/03/01/new-repo-format-faster-smaller-updates.html)

[50% of new NPM packages are spam | Hacker News](https://news.ycombinator.com/item?id=35370728)
[One In Two New Npm Packages Is SEO Spam Right Now](https://blog.sandworm.dev/one-in-two-new-npm-packages-is-seo-spam-right-now)

[KDE publishes the new "KDE for developers" page, where you can find advice on and links to tools, frameworks and libraries that will help you build powerful and cool-looking apps using KDE technologies: linux](https://www.reddit.com/r/linux/comments/13v0lxk/kde_publishes_the_new_kde_for_developers_page)

[Ask Ubuntu](https://askubuntu.com/questions/79665/keep-only-essential-packages)
Keep only essential packages

## package manager - nix

[Nix: An idea whose time has come | Hacker News](https://news.ycombinator.com/item?id=30384121)
[Nix: An Idea Whose Time Has Come | Revelry](https://revelry.co/insights/development/nix-time/)

[GitHub - ryantm/nixpkgs-update: Updating nixpkgs packages since 2018](https://github.com/ryantm/nixpkgs-update)

[Mattia Gheda](https://ghedam.at/15490/so-tell-me-about-nix)
(2020) So, tell me about Nix

[Adrian Hesketh](https://adrianhesketh.com/2020/07/03/mac-setup-with-nix-darwin/)
(2020) Using Nix to set up my new Mac

## package manager - rpm

[Stack Overflow](https://stackoverflow.com/questions/8076471/how-to-know-the-value-of-built-in-macro-in-rpm)
How to know the value of built-in macro in RPM?

[Packagecloud blog](https://blog.packagecloud.io/eng/2015/05/11/building-rpm-packages-with-mock/)
(2015) Building RPM packages with mock

[Christian Stankowic](https://www.stankowic-development.net/?p=7900&lang=en)
CentOS 7 and the incorrect dist RPM macro

[Gavin Carr](http://www.openfusion.net/linux/mocking_rpms)
Mocking RPMs on CentOS with Mock by Fedora

## package manager - yum

[Vivek Gite](https://www.cyberciti.biz/faq/centos-redhat-fedora-yum-lock-package-version-command/)
CentOS / RHEL: Yum Lock Package Version At a Particular Version

[Linux Stack Exchange](https://unix.stackexchange.com/questions/259640/how-to-use-yum-to-get-all-rpms-required-for-offline-use)
How to use yum to get all RPMs required, for offline use?

[Red Hat Customer Portal](https://access.redhat.com/solutions/10154)
How to use yum to download a package without installing it

[CentOS Wiki](https://wiki.centos.org/TipsAndTricks/YumAndRPM)
Yum and RPM Tips and Tricks

[Computer Hope](https://www.computerhope.com/unix/yum.htm)
yum command help + examples

[David Newcomb](http://www.bigsoft.co.uk/blog/2012/01/06/rpmdb-unable-to-join-the-environment)
(2012) yum install failing on `rpmdb: unable to join the environment` or `db3 error(11) from dbenv->open: Resource temporarily unavailable`. Do the followings:

```bash
rm -rf /var/lib/rpm/__db*
rpm --rebuilddb
```

[Benjamin Cane](https://bencane.com/2013/12/23/yum-plugins-verifying-packages-and-configurations-with-yum-verify/)
(2013) Yum Plugins: Verifying packages and configurations with Yum Verify

## realtime preemption

[The real realtime preemption end game | Hacker News](https://news.ycombinator.com/item?id=38290145)
[The real realtime preemption end game [LWN.net]](https://lwn.net/Articles/951337/)

## rust support

[Linux Rust Support | Hacker News](https://news.ycombinator.com/item?id=27746130)
[[PATCH 00/17] Rust support - ojeda](https://lore.kernel.org/lkml/20210704202756.29107-1-ojeda@kernel.org/)

[Supporting Linux kernel development in Rust | Hacker News](https://news.ycombinator.com/item?id=24334731)
[Supporting Linux kernel development in Rust [LWN.net]](https://lwn.net/Articles/829858/)

[Linus Torvalds on Rust support in kernel | Hacker News](https://news.ycombinator.com/item?id=26831841)
[LKML: Linus Torvalds: Re: [PATCH 00/13] [RFC] Rust support](https://lkml.org/lkml/2021/4/14/1099)

[An RFC that adds support for Rust to the Linux kernel | Hacker News](https://news.ycombinator.com/item?id=26812047)
[LKML: ojeda@kernel ...: [PATCH 00/13] [RFC] Rust support](https://lkml.org/lkml/2021/4/14/1023)

[Linus Torvalds: Rust for the Kernel Could Possibly Be Merged for Linux 5.20 | Hacker News](https://news.ycombinator.com/item?id=31848499)
[Linus Torvalds: Rust For The Kernel Could Possibly Be Merged For Linux 5.20 - Phoronix](https://www.phoronix.com/news/Rust-For-Linux-5.20-Possible)

[Rust support in the Linux kernel | Hacker News](https://news.ycombinator.com/item?id=29485465)
[LKML: Miguel Ojeda: [PATCH 00/19] Rust support](https://lkml.org/lkml/2021/12/6/461)

## selinux

[SELinux](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/5/html/deployment_guide/ch-selinux)
provides a flexible Mandatory Access Control (MAC) system built into the Linux kernel.

[SELinux is unmanageable; just turn it off if it gets in your way | Hacker News](https://news.ycombinator.com/item?id=31176138)
[SELinux is unmanageable; just turn it off if it gets in your way | Ctrl blog](https://www.ctrl.blog/entry/selinux-unmanageable.html)

[SELinux Project](https://github.com/SELinuxProject)

[SELinux Wiki](https://selinuxproject.org/page/Main_Page)

[Fedora](https://fedoraproject.org/wiki/SELinux)

## swear words

[words in the kernel](https://www.vidarholen.net/contents/wordcount/)
[words in the kernel](https://web.archive.org/web/20210102182957/https://www.vidarholen.net/contents/wordcount/)
occurences of words within the linux kernel. crap is said more times than shit surprisingly

## system layer - config files

[Mcron - GNU Project - Free Software Foundation🆓](https://www.gnu.org/software/mcron)

## system layer - copy files

[Cpio - GNU Project - Free Software Foundation (FSF)🆓](https://www.gnu.org/software/cpio)

## system layer - executing programs and services

[GNU PIES - Program Invocation and Execution Supervisor🆓](https://www.gnu.org.ua/software/pies)

[The Shepherd - GNU Project - Free Software Foundation🆓](https://www.gnu.org/software/shepherd)

[Swbis - GNU Project - Free Software Foundation (FSF)🆓](https://www.gnu.org/software/swbis)

[userv - user services client and daemon🆓](https://www.gnu.org/software/userv)

[Xlogmaster - GNU Project - Free Software Foundation (FSF)🆓](https://www.gnu.org/software/xlogmaster)

[Non Session Manager vs New Session Manager | Hacker News](https://news.ycombinator.com/item?id=27789952)
[Linux Audio is Dead | Non](https://archive.is/3Tggt)

[Nq - A simple Unix job queue system | Hacker News](https://news.ycombinator.com/item?id=25920517)
[leahneukirchen/nq: Unix command line queue utility](https://github.com/leahneukirchen/nq)

[Libuv - Linux: io_uring support | Hacker News](https://news.ycombinator.com/item?id=36106196)
[linux: introduce io_uring support by bnoordhuis · Pull Request #3952 · libuv/libuv](https://github.com/libuv/libuv/pull/3952)

## system layer - libreboot

[GNU+Linux laptops with Libreboot preinstalled, based on coreboot | Hacker News](https://news.ycombinator.com/item?id=35496651)
[Minifree Ltd - Linux/BSD preinstalled laptops with Libreboot BIOS replacement](https://minifree.org/)

## system layer

[NLnet; Structuring the System Layer with Dataspaces](https://nlnet.nl/project/Dataspaces)

## text manipulation

[Coreutils - GNU core utilities🆓](https://www.gnu.org/software/coreutils)
[Decoded: GNU Coreutils (2018) | Hacker News](https://news.ycombinator.com/item?id=37439535)
[Decoded: GNU coreutils - MaiZure's Projects](https://maizure.org/projects/decoded-gnu-coreutils/)

## the spirit of linux

[Keep Linux Open and Free-We Can't Afford Not To](https://old.reddit.com/r/linux/comments/14vws22/keep_linux_open_and_freewe_cant_afford_not_to/)

[urbit.org](https://urbit.org/)

## unix signals

[Should you be scared of Unix signals? (2016) | Hacker News](https://news.ycombinator.com/item?id=37899098)
[Should you be scared of Unix signals?](https://jvns.ca/blog/2016/06/13/should-you-be-scared-of-signals/)

## WebSockets

[Show HN: A Unixy approach to WebSockets | Hacker News](https://news.ycombinator.com/item?id=9050970)
[websocketd](http://websocketd.com/)

## wireless drivers

[Remembering Larry Finger, who made Linux wireless work | Hacker News](https://news.ycombinator.com/item?id=40812695)
[Larry Finger made Linux wireless work and brought others along to learn | Ars Technica](https://arstechnica.com/gadgets/2024/06/larry-finger-linux-wireless-hero-was-a-persistent-patient-coder-and-mentor/)

## break-fix

[Show HN: SadServers - Test your Linux troubleshooting skills | Hacker News](https://news.ycombinator.com/item?id=33344142)
[SadServers - Troubleshooting Linux Servers](https://sadservers.com/)

## build a linux computer

[Eight Virtues Personal Computers - Linux Personal Computers](https://pc.eightvirtues.com/)

## commands

[The Linux Command Handbook - Learn Linux Commands for Beginners](https://www.freecodecamp.org/news/the-linux-commands-handbook)

[Top Linux Command Line Courses Online - Updated [February 2023] | Udemy](https://www.udemy.com/topic/linux-command-line)

[Switching From Windows to Nix or a Newbie to Linux 20 Useful Commands for Linux Newbies](https://www.tecmint.com/useful-linux-commands-for-newbies)
[TecMint](https://www.tecmint.com/)
the ideal Linux blog for Sysadmins & Geeks.

[50 Most Frequently Used UNIX/Linux Commands (With Examples)](https://www.thegeekstuff.com/2010/11/50-linux-commands)

[Basic (but) Useful Linux Commands | Bodhi LinuxBasic (but) Useful Linux Commands | Bodhi Linux](https://www.bodhilinux.com/w/basic-but-useful-linux-commands)

[How to Search for Files from the Linux Command Line](https://www.freecodecamp.org/news/how-to-search-for-files-from-the-linux-command-line)

[How to Create Your Own Commands in Linux](https://www.freecodecamp.org/news/how-to-create-your-own-command-in-linux)

[GameShell: A game to learn or teach the Unix shell | Hacker News](https://news.ycombinator.com/item?id=31502917)
[phyver/GameShell: a game to learn (or teach) how to use standard commands in a Unix shell](https://github.com/phyver/GameShell)

[LinuxCommand.org: Learn The Linux Command Line. Write Shell Scripts.](https://linuxcommand.org/)
An excellent place to learn the command line and Bash shell scripting.

[How to Search Files Effectively in the Linux Terminal - Advanced Guide](https://www.freecodecamp.org/news/how-to-search-files-effectively-in-linux)

[How to Use Your Linux Terminal as a Calculator - Mathematical Expression Solver](https://www.freecodecamp.org/news/solve-your-math-equation-on-terminal)

## components of linux

["Linux" Isn't Just Linux: 8 Pieces of Software That Make Up Linux Systems](https://www.howtogeek.com/177213/linux-isnt-just-linux-8-pieces-of-software-that-make-up-linux-systems)

## distros - 0 multiple

[I created a chart showing how long some of the still active independent Linux distros have been around : linux](https://old.reddit.com/r/linux/comments/rfigw0/i_created_a_chart_showing_how_long_some_of_the)

[Ubuntu vs Debian vs Fedora vs Arch vs Linux Mint | DevDungeon](https://www.devdungeon.com/content/ubuntu-vs-debian-vs-fedora-vs-arch-vs-linux-mint)

[List of Linux distributions - Wikipedia](https://en.m.wikipedia.org/wiki/List_of_Linux_distributions#Debian-based)

## linux certifications

[Linux Certification](https://www.lpi.org/our-certifications/lpic-1-overview)

[Best Linux and Cloud Training Certification Pricing | Linux Academy](https://acloudguru.com/pricing)

[UNIX and Linux Essentials| Solaris 11 Administration | Oracle Solaris | Operating Systems | Training| Oracle](https://education.oracle.com/oracle-it-infrastructure-learning-subscription/ls_50041)

[UNIX and Linux Essentials| Solaris 11 Administration | Oracle Solaris | Operating Systems | Training| Oracle](https://education.oracle.com/pls/web_prod-plq-dad/db_pages.getpage?get_params=dc%3AD76989%2Cclang%3AEN&page_id=609)

[Introduction to Linux (LFS101) Linux Foundation Training](https://training.linuxfoundation.org/training/introduction-to-linux)

## linux history

[The early days of Linux | Hacker News](https://news.ycombinator.com/item?id=35557848)
[The early days of Linux [LWN.net]](https://lwn.net/Articles/928581/)

[Exploring the Internals of Linux v0.01 | Hacker News](https://news.ycombinator.com/item?id=37101588)
[Exploring the internals of Linux v0.01 - seiya.me](https://seiya.me/blog/reading-linux-v0.01)

[A Way Out for A.out | Hacker News](https://news.ycombinator.com/item?id=30792059)
[A way out for a.out [LWN.net]](https://lwn.net/Articles/888741/)

## linux kernel

[Linux Kernel Teaching | Hacker News](https://news.ycombinator.com/item?id=22564665)
[Linux Kernel Teaching - The Linux Kernel documentation](https://linux-kernel-labs.github.io/refs/heads/master/index.html)

[The Linux Kernel Module Programming Guide | Hacker News](https://news.ycombinator.com/item?id=35782630)
[The Linux Kernel Module Programming Guide](https://sysprog21.github.io/lkmpg/)
[GitHub - sysprog21/lkmpg: The Linux Kernel Module Programming Guide (updated for 5.x kernels)](https://github.com/sysprog21/lkmpg)

[Putting the "You" in CPU | Hacker News](https://news.ycombinator.com/item?id=36823605)
[Intro | Putting the "You" in CPU](https://cpu.land/)

[A Heavily-Commented Linux Kernel Source Code [pdf] | Hacker News](https://news.ycombinator.com/item?id=19225268)
[Wayback Machine](https://web.archive.org/web/20190328210534/http://www.oldlinux.org/download/ECLK-5.0-WithCover.pdf)

[Interactive Map of Linux Kernel | Hacker News](https://news.ycombinator.com/item?id=37490623)
[Interactive map of Linux kernel](https://makelinux.github.io/kernel/map/)

[Linux Kernel Teaching - The Linux Kernel documentation](https://linux-kernel-labs.github.io/refs/heads/master/index.html)
a collection of lectures and labs Linux kernel topics.

## linux os

[What's in a Linux executable?](https://fasterthanli.me/series/making-our-own-executable-packer/part-1)

[Linux from Scratch with Training Wheels | Hacker News](https://news.ycombinator.com/item?id=28820602)
[LFS-TW - Phil's Blog](https://philsyme.net/lfs-tw/)

[Welcome to Linux From Scratch!](https://linuxfromscratch.org)
a project that provides you with step-by-step instructions for building your own custom Linux system, entirely from source code.

[Home | Linux Journey](https://linuxjourney.com/)
Linux & CLI Crash Course

[Linux Guide and Hints](https://linuxguideandhints.com/)
tutorials on system administration in Fedora and CentOS.

[Linux Tutorial](https://linuxsurvival.com/linux-tutorial-introduction)

[Linux Insides | Hacker News](https://news.ycombinator.com/item?id=31377904)
[Introduction · Linux Inside](https://0xax.gitbooks.io/linux-insides/content/)

[sirredbeard/awesome-unix: All the UNIX and UNIX-Like: Linux, BSD, macOS, Illumos, 9front, and more.](https://github.com/sirredbeard/Awesome-UNIX)

[wiredhackers/Learn-Linux: A dedicated list of free resources to learn Linux](https://github.com/wiredhackers/Learn-Linux)

[mikeroyal/Linux-Guide: Linux Guide. Learn about Linux Hardware vendors, Linux in the Cloud, Desktop Environments, Window Mangers, Linux Distributions, Linux Security, Graphics (AMD/NVIDIA/Intel ARC), and Software Apps.](https://github.com/mikeroyal/Linux-Guide)

[Gaurav Kumar Gupta](http://www.gauravkgupta.com/ten-best-cheat-sheets-first-time-linux-admins/)
Ten Of The Best Cheat Sheets For First Time Linux Admins

[Howtoforge](http://www.howtoforge.com/howtos)
Linux tutorials by tag : Excellent tutorials on many different subjects.

[Alexander Kuleshov aka 0xAX](https://github.com/0xAX/linux-insides/blob/master/SUMMARY.md)
Linux insides : A little bit about a linux kernel

[Binh Nguyen](http://www.tldp.org/LDP/Linux-Dictionary/html/index.html)
(2004) Linux Dictionary

[Sandra Henry-Stocker](http://www.computerworld.com/article/3066941/linux/administering-unix-systems-like-your-mom-taught-you.html)
Administering Unix systems like your mom taught you

[aleksandar-todorovic/awesome-linux](https://github.com/aleksandar-todorovic/awesome-linux)
list of awesome resources that make Linux awesome

[The Linux Kernel Module Programming Guide | Hacker News](https://news.ycombinator.com/item?id=41083972)
[The Linux Kernel Module Programming Guide](https://sysprog21.github.io/lkmpg/)

## linux servers and sysops

[Linux SysOps Handbook - Linux SysOps Handbook](https://abarrak.gitbook.io/linux-sysops-handbook)

[The Debian Administrator's Handbook](https://www.debian.org/doc/manuals/debian-handbook)

[The Apache Cassandra Beginner Tutorial](https://www.freecodecamp.org/news/the-apache-cassandra-beginner-tutorial)

## projects

[Getting better at Linux with mini-projects | Hacker News](https://news.ycombinator.com/item?id=26002335)
[Getting Better at Linux With 10 Mini-Projects](https://carltheperson.com/posts/10-things-linux/)

## unix

[The Unix-Haters Handbook (1994) [pdf] | Hacker News](https://news.ycombinator.com/item?id=31417690)
[ugh.book - ugh.pdf](https://web.mit.edu/~simsong/www/ugh.pdf)

[I summarized my understanding of Linux systems | Hacker News](https://news.ycombinator.com/item?id=39701358)
[lsc4719/MyViewOfLinuxSystems](https://github.com/lsc4719/MyViewOfLinuxSystems)
THIS MAY BE ABSOLUTELY AMAZING!!

[Xv6, a simple Unix-like teaching operating system | Hacker News](https://news.ycombinator.com/item?id=40613126)
[6.1810 / Fall 2023](https://pdos.csail.mit.edu/6.828/2023/xv6.html)

[Jeffrey Paul](https://sneak.berlin/20191011/stupid-unix-tricks/)
(2019) Stupid Unix Tricks

[Eric Steven Raymond](https://www.catb.org/~esr/writings/unix-koans/)
Rootless Root: The Unix Koans of Master Foo

## advanced unix programming

[CS631 - Advanced Programming in the Unix Environment | Hacker News](https://news.ycombinator.com/item?id=33140795)
[Advanced Programming in the UNIX Environment](https://stevens.netmeister.org/631/)

## awk_sed

### Chart of similar operations with sed and awk

#### string

sed "s/from/to/"        awk '{sub("from","to"); print}'

sed "s/from/to/g"       awk '{gsub("from","to"); print}'

sed "s/from/to/3"       awk '{$0=gensub("from","to",3); print}'

#### regex

sed "s/reg.*$/_&_/"     awk '{sub(/reg.*$/, "_&_"); print}'

sed "s/reg[ex]/YY/g"    awk '{gsub(/reg[ex]/, "YY"); print}'

sed "s/reg[ex]/ZZ/4"    awk '{$0=gensub(/reg[ex]/, "ZZ", 4); print}'

### awk variable "var"

sed "s/bang/boom/"      awk -v var="bang" '{sub(var,"boom");print}'

sed "s/.*=/equ/5"       awk -v var=".*=" '{$0=gensub(var,"equ",5);print}'

### DOS variable "XY" with awk variable "z"

[DOSPROMPT] C:\path> set xy=bangg*

sed "s/%XY%/boom/"     awk -v z="%XY" '{sub(z,"boom"); print}'

sed "s/%XY%/boom/g"    awk -v z="%XY" '{gsub(z,"boom"); print}'

sed "s/%XY%/boom/5"    awk -v z="%XY" '{$0=gensub(z,"boom",5); print}'

### interval expression, \{M,N\}

sed "s/fo\{3,8\}/bar/"   awk --re-interval '{sub(/fo{3,8}/, "bar");print}'

sed "s/fo\{3,8\}/bar/g"

               awk --re-interval -v a="fo{3,8}" '{gsub(a,"bar");print}'
       or
               awk --re-interval -v a="fo\{3,8\}" '{gsub(a,"bar");print}'

### DOS variable "HI", awk variable "j" with interval expression

[DOSPROMPT] C:\path> set hi=Whe\{2,7\}!*

sed "s/%hi%/Zow!/"     awk --re-interval -v j="%hi" '{sub(j,"Zow!"); print}'

sed "s/%hi%/Zow!/g"    awk --re-interval -v j="%hi" '{gsub(j,"Zow!");print}'

[DOSPROMPT] C:\path> REM ... using a disk file ...
[DOSPROMPT] C:\path> echo {$0=gensub(j,"Zow!",5); print} >myfile.awk

sed "s/%hi%/Zow!/5"    awk --re-interval -v j="%hi" -f myfile.awk

--
compiled by Eric Pement
on 03/20/2001 07:11pm

[end-of-file]

## commands - sed and awk

[F'Awk Yeah!](https://posts.specterops.io/fawk-yeah-advanced-sed-and-awk-usage-parsing-for-pentesters-3-e5727e11a8ad)
advanced sed and awk usage (Parsing for Pentesters 3).

## commands - systemd

[Systemd through the eyes of a musl distribution maintainer | Hacker News](https://news.ycombinator.com/item?id=38889156)
[systemd through the eyes of a musl distribution maintainer - The Cat Fox Life](https://catfox.life/2024/01/05/systemd-through-the-eyes-of-a-musl-distribution-maintainer/)

## embedded linux

[So you want to build an embedded Linux system? | Hacker News](https://news.ycombinator.com/item?id=24800037)
[So you want to build an embedded Linux system? - Jay Carlson](https://jaycarlson.net/embedded-linux/)

## AppImage

[How to Use AppImage in Linux [Complete Guide]](https://itsfoss.com/use-appimage-linux/)

## cleaning the system

[How to Clean Your Ubuntu Machine](https://www.w3docs.com/snippets/linux/how-to-clean-your-ubuntu-machine.html)

## linux culture

[Unix philosophy - Wikipedia](https://en.wikipedia.org/wiki/Unix_philosophy)

## linux file system

[The Linux Directory Structure, Explained](https://www.howtogeek.com/117435/htg-explains-the-linux-directory-structure-explained)

[An introduction to the Linux /etc/fstab file | Enable Sysadmin](https://www.redhat.com/sysadmin/etc-fstab)

## linux os

[What is Linux? - Linux.com](https://www.linux.com/what-is-linux)

[The Difference Between Linux and GNU/Linux](https://www.lifewire.com/what-is-linux-2201940)

[Introduction to Linux](https://www.freecodecamp.org/news/introduction-to-linux)

[Linux for Hackers - Basics for Cybersecurity Beginners](https://www.freecodecamp.org/news/linux-basics)

[Why is Linux so much "faster"?: linux](https://www.reddit.com/r/linux/comments/13pszur/why_is_linux_so_much_faster)

[Linux Survival | Where learning Linux is easy](https://linuxsurvival.com/)

[Howtoforge Linux Tutorials.](https://www.howtoforge.com/)

[Learn Linux: 10 Free and Best Courses to Learn Linux for Beginners - DEV Community](https://dev.to/javinpaul/5-free-courses-to-learn-linux-for-beginners-367f)

[Guide: Migrating to Linux in 2019 : linux_gaming](https://old.reddit.com/r/linux_gaming/comments/9oqq3w/guide_migrating_to_linux_in_2019/)

## posix compliance

[POSIX - Wikipedia](https://en.wikipedia.org/wiki/POSIX)

## app management

[Linux command to restart application](https://stackoverflow.com/questions/11395565/linux-command-to-restart-application)

## config files

[How to Back Up and Migrate Your Linux Configuration Files](https://www.howtogeek.com/194342/how-to-back-up-and-migrate-your-linux-configuration-files/)

[AskF5 Support](https://support.f5.com/csp/article/K12213214)
Overview of colored status icons in the Configuration utility

## desktop environment - display manager

[software installation - What is gdm3, kdm, lightdm? How to install and remove them? - Ask Ubuntu](https://askubuntu.com/questions/829108/what-is-gdm3-kdm-lightdm-how-to-install-and-remove-them#829110)

## desktop environment - gnome

[GitHub - Kazhnuz/awesome-gnome: A curated list of awesome apps, extensions, modules, themes and tools for the Gnome Desktop Environment.](https://github.com/Kazhnuz/awesome-gnome)

[GitHub - sonnyp/Workbench: Learn and prototype with GNOME technologies](https://github.com/sonnyp/Workbench)

## desktop environment

[How to Install and Use Another Desktop Environment on Linux](https://www.howtogeek.com/193129/how-to-install-and-use-another-desktop-environment-on-linux/)

[Category:Free desktop environments - Wikipedia](https://en.wikipedia.org/wiki/Category:Free_desktop_environments)

[Category:Free windowing systems - Wikipedia](https://en.wikipedia.org/wiki/Category:Free_windowing_systems)

## desktop environment - x

[Category:Free X window managers - Wikipedia](https://en.wikipedia.org/wiki/Category:Free_X_window_managers)

## device drivers

[How to List Your Computer's Devices From the Linux Terminal](https://www.howtogeek.com/426199/how-to-list-your-computers-devices-from-the-linux-terminal)

[Linux Device Drivers, Third Edition [LWN.net]](https://lwn.net/Kernel/LDD3/)

## eBPF

[GitHub - zoidyzoidzoid/awesome-ebpf: A curated list of awesome projects related to eBPF.](https://github.com/zoidyzoidzoid/awesome-ebpf)
a curated list of awesome projects related to eBPF.

## file permissions

[Linux chmod and chown - How to Change File Permissions and Ownership in Linux](https://www.freecodecamp.org/news/linux-chmod-chown-change-file-permissions)

[Linux Permissions - How to Find Permissions of a File](https://www.freecodecamp.org/news/linux-permissions-how-to-find-permissions-of-a-file)

## fork

[Fork() is evil; vfork() is goodness; afork() would be better; clone() is stupid | Hacker News](https://news.ycombinator.com/item?id=30502392)
[fork() is evil; vfork() is goodness; afork() would be better; clone() is stupid](https://gist.github.com/nicowilliams/a8a07b0fc75df05f684c23c18d7db234)

## hardening

[+PROTECTING LINUX AT KERNEL LEVEL WHY AND HOW](https://hardenedvault.net/blog/2023-07-09-protecting-linux-kernel-why-how/)

## immutable linux systems

[Introduction to Immutable Linux Systems | Hacker News](https://news.ycombinator.com/item?id=37551474)
[Solene'% : Introduction to immutable Linux systems](https://dataswamp.org/~solene/2023-07-12-intro-to-immutable-os.html)

## initramfs

[GitHub - LaszloGombos/awesome-initramfs: awesome initramfs](https://github.com/LaszloGombos/awesome-initramfs)

## linux on chromebook

[Complete Guide to Installing Linux on Chromebook](https://itsfoss.com/install-linux-chromebook/)

## lvm

[server - What is LVM and what is it used for? - Ask Ubuntu](https://askubuntu.com/questions/3596/what-is-lvm-and-what-is-it-used-for)

[Linux LVM | How LVM works in Linux with Examples?](https://www.educba.com/linux-lvm)

## makefiles

[Chris Wellons](http://nullprogram.com/blog/2017/08/20/)
(2017) A Tutorial on Portable Makefiles

## making Linux apps

[Make Apps for Linux | Hacker News](https://news.ycombinator.com/item?id=38583399)
[Make a Linux App](https://makealinux.app/)

## os maintenance

[What Kind of Maintenance Do I Need to Do On My Linux PC?](https://lifehacker.com/what-kind-of-maintenance-do-i-need-to-do-on-my-linux-pc-5817282)

## package manager - apt

[Linux apt command help and examples](https://www.computerhope.com/unix/apt.htm)

[[Tutorial] Apt-get & Aptitude & dpkg : jailbreak](https://old.reddit.com/r/jailbreak/comments/6mgou6/tutorial_aptget_aptitude_dpkg/)

[Using apt-get Commands In Linux [Complete Beginners Guide]](https://itsfoss.com/apt-get-linux-guide/)

[The Ultimate Guide to Apt and Apt-Get Commands - Make Tech Easier](https://www.maketecheasier.com/ultimate-guide-apt-and-apt-get-commands/)

## package manager

[How does apt render its fancy progress bar? | Hacker News](https://news.ycombinator.com/item?id=28850036)
[mdk.fr - How APT does its fancy progress bar](https://mdk.fr/blog/how-apt-does-its-fancy-progress-bar.html)

[Linux package managers: dnf vs apt | Opensource.com](https://opensource.com/article/21/7/dnf-vs-apt)

## package manager - nix

[Mattia Gheda](https://ghedam.at/15978/an-introduction-to-nix-shell)
(2020) An introduction to nix-shell
nix-shell allows you to define development environments for pretty much any language in a consistent way, it makes also easy to support different versions of the same language!

[Mathias Polligkeit](https://www.mathiaspolligkeit.de/dev/exploring-nix-on-macos/)
(2020) Dev Environment Setup With Nix on MacOS

## package manager - rpm

[Senthil Kumar aka SK](https://www.ostechnix.com/download-rpm-package-dependencies-centos/)
(2016) How To Download A RPM Package With All Dependencies In CentOS

## running services

[How to List All Running Services in Linux | RoseHosting](https://www.rosehosting.com/blog/how-to-list-all-services-in-linux/)

## selinux

[SELinux Game](http://selinuxgame.org/index.html)
learn SELinux by doing. Solve Puzzles, show skillz.

[Daniel J Walsh](https://opensource.com/business/13/11/selinux-policy-guide)
Your visual how-to guide for SELinux policy enforcement

## sysctl

[Linux network performance parameters | Hacker News](https://news.ycombinator.com/item?id=37403799)
[leandromoreira/linux-network-performance-parameters: Learn where some of the network sysctl variables fit into the Linux/Kernel network flow.](https://github.com/leandromoreira/linux-network-performance-parameters)
where some of the network sysctl variables fit into the Linux/Kernel network flow.

## tar archive

[The tar archive format, and why GNU tar extracts in quadratic time | Hacker News](https://news.ycombinator.com/item?id=32206579)
[The tar archive format, its extensions, and why GNU tar extracts in quadratic time - Mort's Ramblings](https://mort.coffee/home/tar/)

## unix pipes

[The Unix Pipe Card Game | Hacker News](https://news.ycombinator.com/item?id=41047110)
[The UNIX Pipe Card Game](https://punkx.org/unix-pipe-game/)

## user management

[Jack Wallen](https://www.linux.com/learn/intro-to-linux/2017/12/how-manage-users-groups-linux)
(2017) How to Manage Users with Groups in Linux

[Ian Maddox](https://cloudplatform.googleblog.com/2018/01/12-best-practices-for-user-account.html)
(2018) 12 best practices for user account, authorization and password management

## commands - bash

[Bashcrawl: Learn Linux commands by playing a simple text adventure | Hacker News](https://news.ycombinator.com/item?id=28819387)
[slackermedia / bashcrawl · GitLab](https://gitlab.com/slackermedia/bashcrawl)

[Pure Bash Bible | Hacker News](https://news.ycombinator.com/item?id=21013150)
[GitHub - dylanaraps/pure-bash-bible: A collection of pure bash alternatives to external processes.](https://github.com/dylanaraps/pure-bash-bible)

[Pure Sh Bible | Hacker News](https://news.ycombinator.com/item?id=35765707)
[GitHub - dylanaraps/pure-sh-bible: A collection of pure POSIX sh alternatives to external processes.](https://github.com/dylanaraps/pure-sh-bible)

[Run Commands, the 'rc' in '.bashrc' | Hacker News](https://news.ycombinator.com/item?id=20853214)
[RUNCOM - Wikipedia](https://en.wikipedia.org/wiki/Run_commands)

[How to write idempotent Bash scripts | Hacker News](https://news.ycombinator.com/item?id=20375197)
[How to write idempotent Bash scripts](https://arslan.io/2019/07/03/how-to-write-idempotent-bash-scripts/)

[Bash Scripting Tutorial - Linux Shell Script and Command Line for Beginners](https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners)

[Command Line for Beginners - How to Use the Terminal Like a Pro [Full Handbook]](https://www.freecodecamp.org/news/command-line-for-beginners)

[BashGuide - Greg's Wiki](https://mywiki.wooledge.org/BashGuide)
[GreyCat's Wiki](http://mywiki.wooledge.org/BashGuide/Practices)
BASH Guide / practices for people doing Unix shell scripting or system administration

[GitHub - awesome-lists/awesome-bash: A curated list of delightful Bash scripts and resources.](https://github.com/awesome-lists/awesome-bash)

[Idnan/bash-guide](https://github.com/Idnan/bash-guide)
A guide to learn bash + some tips

[bash-handbook](https://github.com/denysdovhan/bash-handbook)
for those who wanna learn Bash.

[The Bash Hackers Wiki](https://wiki.bash-hackers.org/start)
hold documentation of any kind about GNU Bash.
[Terminal codes (ANSI/VT100) introduction [Bash Hackers Wiki]](http://wiki.bash-hackers.org/scripting/terminalcodes)

[The Bash Guide](https://guide.bash.academy/)

[Bash-oneliner: A collection of handy Bash one-liners and terminal tricks | Hacker News](https://news.ycombinator.com/item?id=31250275)
[onceupon/Bash-Oneliner: A collection of handy Bash One-Liners and terminal tricks for data processing and Linux system maintenance.](https://github.com/onceupon/Bash-Oneliner)
[Bash-Oneliner | A collection of handy Bash One-Liners and terminal tricks for data processing and Linux system maintenance.](https://onceupon.github.io/Bash-Oneliner/)
[GitHub repository](https://github.com/onceupon/Bash-Oneliner)

[FLOZz' MISC](http://misc.flogisoft.com/bash/tip_colors_and_formatting)
Bash tips: Colors and formatting

[Nicola Paolucci](https://developer.atlassian.com/blog/2015/02/ten-tips-for-wonderful-bash-productivity/)
(2015) Ten tips for wonderful bash productivity

[blockloop.io](https://www.blockloop.io/mastering-bash-and-terminal)
Mastering Bash and Terminal

[Bhaskar Karambelkar](https://dev.to/bhaskar_vk/bash-shell-tricks)
(2017) Bash Shell Tricks

[The Goose-bearing bash shell](https://goosebearingbashshell.github.io/2016/11/12/how-to-get-your-ip-address-from-the-command-line.html)
(2016) How to get your IP address from the command line. TLDR;
type `curl ident.me` to know your public ip

[progrium/bashstyle](https://github.com/progrium/bashstyle)
Let's do Bash right! Collection of Best practices acquired from experience for Bash

[Buddy Reno](https://medium.freecodecamp.com/bash-shortcuts-to-enhance-your-git-workflow-5107d64ea0ff)
Bash Shortcuts to Enhance Your Git Workflow

[Jakub Koziol](https://pragmaticcoders.com/blog/bash-tips-and-tricks/)
(2018) Bash tips & tricks: good and not-so-good bash practices

[Valentin Bajrami](https://www.redhat.com/sysadmin/stupid-bash-tricks)
(2020) Stupid Bash tricks: History, reusing arguments, files and directories, functions, and more
Here are five great tips and tricks for the Bash shell that you can use at your Linux terminal today.

[Bash Pitfalls](https://mywiki.wooledge.org/BashPitfalls)
common errors that Bash programmers make. Each example is flawed in some way.

[Bash Hackers Wiki](https://wiki.bash-hackers.org/scripting/obsolete)
obsolete and deprecated syntax

## commands - bind

[bind/](https://dev.w3.org/cvsweb/bind)

## commands - cksum

[What is Checksum? How to Check if a File was Modified Using the cksum Command in Linux](https://www.freecodecamp.org/news/file-last-modified-in-inux-how-to-check-if-two-files-are-same)

## commands - cp

[Scott Rippee](http://www.hypexr.org/linux_scp_help.php)
Example syntax for Secure Copy (scp)

## commands - htop

[Htop Explained | Hacker News](https://news.ycombinator.com/item?id=21414882)
[htop explained | peteris.rocks](https://peteris.rocks/blog/htop/)
explanation of everything you can see in htop/top on Linux.
(2017) htop explained

[htop](https://github.com/hishamhm/htop)
interactive text-mode process viewer for Unix systems. It aims to be a better 'top'.

[htop an interactive process viewer](https://htop.dev/)

## commands - ls

[The Linux LS Command - How to List Files in a Directory + Option Flags](https://www.freecodecamp.org/news/the-linux-ls-command-how-to-list-files-in-a-directory-with-options/)

## commands - lsof

[Sandra Henry-Stocker](http://www.computerworld.com/article/3121790/linux/making-troubleshooting-with-lsof-easier.html)
Unix tips: Making troubleshooting with lsof easier.
[Unix commands: Troubleshooting with lsof](http://www.computerworld.com/article/3119775/linux/troubleshooting-with-lsof.html)

[Lakshmanan Ganapathy](https://www.thegeekstuff.com/2012/08/lsof-command-examples)
(2012) 15 Linux lsof Command Examples (Identify Open Files)

[Daniel Miessler](https://danielmiessler.com/study/lsof/)
An lsof Primer

## commands - mkdir+cd

[Erlend Hamberg](https://hamberg.no/erlend/posts/2013-01-18-mkcd.html)
(2013) use mkcd (mkdir + cd)

## commands - mkdir

[Lori Kaufman](https://www.howtogeek.com/275069/how-to-create-multiple-subdirectories-with-one-linux-command/)
(2016) How to Create Multiple Subdirectories with One Linux Command

## commands - nmap

[Vivek Gite](https://www.cyberciti.biz/networking/nmap-command-examples-tutorials/)
(2018) Top 32 Nmap Command Examples For Sys/Network Admins

## commands - oc

[Jorge Tudela Gonzales De Riancho](https://blog.openshift.com/oc-command-newbies/)
(2018) The oc Command for Newbies

## commands - sed

[Useful sed scripts and patterns | Hacker News](https://news.ycombinator.com/item?id=29196221)
[adrianlarion/useful-sed: Useful sed scripts & patterns.](https://github.com/adrianlarion/useful-sed)

[The Basics of Using the Sed Stream Editor to Manipulate Text in Linux | DigitalOcean](https://www.digitalocean.com/community/tutorials/the-basics-of-using-the-sed-stream-editor-to-manipulate-text-in-linux)

[GNU sed - GNU Project - Free Software Foundation🆓](https://www.gnu.org/software/sed)

## commands - shred

[How to Securely Erase a Disk and File using the Linux shred Command](https://www.freecodecamp.org/news/securely-erasing-a-disk-and-file-using-linux-command-shred)

## commands - ss

[Silver Moon](http://www.binarytides.com/linux-ss-command/)
10 examples of Linux ss command to monitor network connections

## commands - sudo

[OSXDaily](http://osxdaily.com/2017/11/22/use-touch-id-sudo-mac/)
(2017) How to Use Touch ID to Authenticate sudo on Mac OS

## commands - systemd

[Systemd by Example | Hacker News](https://news.ycombinator.com/item?id=30071240)
[systemd by example - the systemd playground](https://systemd-by-example.com/)

[CertDepot](https://www.certdepot.net/rhel7-get-started-systemd/)
(2018) RHEL7: How to get started with Systemd.

## commands - tar

[Linux tar Command - How to Compress Files in Linux](https://www.freecodecamp.org/news/how-to-compress-files-in-linux-with-tar-command)

## commands - tcpdump

[Pradeep Kumar](https://www.linuxtechi.com/capture-analyze-packets-tcpdump-command-linux/)
(2018) How to capture and analyze packets with tcpdump command on Linux

[Daniel Miessler](https://danielmiessler.com/study/tcpdump/)
A tcpdump Tutorial and Primer with Examples

[Steven Iveson](http://packetpushers.net/masterclass-tcpdump-interpreting-output/)
Masterclass – Tcpdump – Interpreting Output

[Narad Shrestha](https://www.tecmint.com/12-tcpdump-commands-a-network-sniffer-tool/)
12 Tcpdump Commands – A Network Sniffer Tool

[Edoceo](http://edoceo.com/cli/tcpdump)
tcpdump examples

[rationallyPARANOID](https://rationallyparanoid.com/articles/tcpdump.html)
Tcpdump usage examples

## sed1line

```sed
USEFUL ONE-LINE SCRIPTS FOR SED (Unix stream editor)        Dec. 29, 2005
Compiled by Eric Pement - pemente[at]northpark[dot]edu        version 5.5

Latest version of this file (in English) is usually at:
   http://sed.sourceforge.net/sed1line.txt
   http://www.pement.org/sed/sed1line.txt

This file will also available in other languages:
  Chinese     - http://sed.sourceforge.net/sed1line_zh-CN.html
  Czech       - http://sed.sourceforge.net/sed1line_cz.html
  Dutch       - http://sed.sourceforge.net/sed1line_nl.html
  French      - http://sed.sourceforge.net/sed1line_fr.html
  German      - http://sed.sourceforge.net/sed1line_de.html
  Italian     - http://sed.sourceforge.net/sed1line_it.html
  Portuguese  - http://sed.sourceforge.net/sed1line_pt-BR.html
  Spanish     - http://sed.sourceforge.net/sed1line_es.html

FILE SPACING:

 # double space a file
 sed G

 # double space a file which already has blank lines in it. Output file
 # should contain no more than one blank line between lines of text.
 sed '/^$/d;G'

 # triple space a file
 sed 'G;G'

 # undo double-spacing (assumes even-numbered lines are always blank)
 sed 'n;d'

 # insert a blank line above every line which matches "regex"
 sed '/regex/{x;p;x;}'

 # insert a blank line below every line which matches "regex"
 sed '/regex/G'

 # insert a blank line above and below every line which matches "regex"
 sed '/regex/{x;p;x;G;}'

NUMBERING:

 # number each line of a file (simple left alignment). Using a tab (see
 # note on '\t' at end of file) instead of space will preserve margins.
 sed = filename | sed 'N;s/\n/\t/'

 # number each line of a file (number on left, right-aligned)
 sed = filename | sed 'N; s/^/     /; s/ *\(.\{6,\}\)\n/\1  /'

 # number each line of file, but only print numbers if line is not blank
 sed '/./=' filename | sed '/./N; s/\n/ /'

 # count lines (emulates "wc -l")
 sed -n '$='

TEXT CONVERSION AND SUBSTITUTION:

 # IN UNIX ENVIRONMENT: convert DOS newlines (CR/LF) to Unix format.
 sed 's/.$//'               # assumes that all lines end with CR/LF
 sed 's/^M$//'              # in bash/tcsh, press Ctrl-V then Ctrl-M
 sed 's/\x0D$//'            # works on ssed, gsed 3.02.80 or higher

 # IN UNIX ENVIRONMENT: convert Unix newlines (LF) to DOS format.
 sed "s/$/`echo -e \\\r`/"            # command line under ksh
 sed 's/$'"/`echo \\\r`/"             # command line under bash
 sed "s/$/`echo \\\r`/"               # command line under zsh
 sed 's/$/\r/'                        # gsed 3.02.80 or higher

 # IN DOS ENVIRONMENT: convert Unix newlines (LF) to DOS format.
 sed "s/$//"                          # method 1
 sed -n p                             # method 2

 # IN DOS ENVIRONMENT: convert DOS newlines (CR/LF) to Unix format.
 # Can only be done with UnxUtils sed, version 4.0.7 or higher. The
 # UnxUtils version can be identified by the custom "--text" switch
 # which appears when you use the "--help" switch. Otherwise, changing
 # DOS newlines to Unix newlines cannot be done with sed in a DOS
 # environment. Use "tr" instead.
 sed "s/\r//" infile >outfile         # UnxUtils sed v4.0.7 or higher
 tr -d \r <infile >outfile            # GNU tr version 1.22 or higher

 # delete leading whitespace (spaces, tabs) from front of each line
 # aligns all text flush left
 sed 's/^[ \t]*//'                    # see note on '\t' at end of file

 # delete trailing whitespace (spaces, tabs) from end of each line
 sed 's/[ \t]*$//'                    # see note on '\t' at end of file

 # delete BOTH leading and trailing whitespace from each line
 sed 's/^[ \t]*//;s/[ \t]*$//'

 # insert 5 blank spaces at beginning of each line (make page offset)
 sed 's/^/     /'

 # align all text flush right on a 79-column width
 sed -e :a -e 's/^.\{1,78\}$/ &/;ta'  # set at 78 plus 1 space

 # center all text in the middle of 79-column width. In method 1,
 # spaces at the beginning of the line are significant, and trailing
 # spaces are appended at the end of the line. In method 2, spaces at
 # the beginning of the line are discarded in centering the line, and
 # no trailing spaces appear at the end of lines.
 sed  -e :a -e 's/^.\{1,77\}$/ & /;ta'                     # method 1
 sed  -e :a -e 's/^.\{1,77\}$/ &/;ta' -e 's/\( *\)\1/\1/'  # method 2

 # substitute (find and replace) "foo" with "bar" on each line
 sed 's/foo/bar/'             # replaces only 1st instance in a line
 sed 's/foo/bar/4'            # replaces only 4th instance in a line
 sed 's/foo/bar/g'            # replaces ALL instances in a line
 sed 's/\(.*\)foo\(.*foo\)/\1bar\2/' # replace the next-to-last case
 sed 's/\(.*\)foo/\1bar/'            # replace only the last case

 # substitute "foo" with "bar" ONLY for lines which contain "baz"
 sed '/baz/s/foo/bar/g'

 # substitute "foo" with "bar" EXCEPT for lines which contain "baz"
 sed '/baz/!s/foo/bar/g'

 # change "scarlet" or "ruby" or "puce" to "red"
 sed 's/scarlet/red/g;s/ruby/red/g;s/puce/red/g'   # most seds
 gsed 's/scarlet\|ruby\|puce/red/g'                # GNU sed only

 # reverse order of lines (emulates "tac")
 # bug/feature in HHsed v1.5 causes blank lines to be deleted
 sed '1!G;h;$!d'               # method 1
 sed -n '1!G;h;$p'             # method 2

 # reverse each character on the line (emulates "rev")
 sed '/\n/!G;s/\(.\)\(.*\n\)/&\2\1/;//D;s/.//'

 # join pairs of lines side-by-side (like "paste")
 sed '$!N;s/\n/ /'

 # if a line ends with a backslash, append the next line to it
 sed -e :a -e '/\\$/N; s/\\\n//; ta'

 # if a line begins with an equal sign, append it to the previous line
 # and replace the "=" with a single space
 sed -e :a -e '$!N;s/\n=/ /;ta' -e 'P;D'

 # add commas to numeric strings, changing "1234567" to "1,234,567"
 gsed ':a;s/\B[0-9]\{3\}\>/,&/;ta'                     # GNU sed
 sed -e :a -e 's/\(.*[0-9]\)\([0-9]\{3\}\)/\1,\2/;ta'  # other seds

 # add commas to numbers with decimal points and minus signs (GNU sed)
 gsed -r ':a;s/(^|[^0-9.])([0-9]+)([0-9]{3})/\1\2,\3/g;ta'

 # add a blank line every 5 lines (after lines 5, 10, 15, 20, etc.)
 gsed '0~5G'                  # GNU sed only
 sed 'n;n;n;n;G;'             # other seds

SELECTIVE PRINTING OF CERTAIN LINES:

 # print first 10 lines of file (emulates behavior of "head")
 sed 10q

 # print first line of file (emulates "head -1")
 sed q

 # print the last 10 lines of a file (emulates "tail")
 sed -e :a -e '$q;N;11,$D;ba'

 # print the last 2 lines of a file (emulates "tail -2")
 sed '$!N;$!D'

 # print the last line of a file (emulates "tail -1")
 sed '$!d'                    # method 1
 sed -n '$p'                  # method 2

 # print the next-to-the-last line of a file
 sed -e '$!{h;d;}' -e x              # for 1-line files, print blank line
 sed -e '1{$q;}' -e '$!{h;d;}' -e x  # for 1-line files, print the line
 sed -e '1{$d;}' -e '$!{h;d;}' -e x  # for 1-line files, print nothing

 # print only lines which match regular expression (emulates "grep")
 sed -n '/regexp/p'           # method 1
 sed '/regexp/!d'             # method 2

 # print only lines which do NOT match regexp (emulates "grep -v")
 sed -n '/regexp/!p'          # method 1, corresponds to above
 sed '/regexp/d'              # method 2, simpler syntax

 # print the line immediately before a regexp, but not the line
 # containing the regexp
 sed -n '/regexp/{g;1!p;};h'

 # print the line immediately after a regexp, but not the line
 # containing the regexp
 sed -n '/regexp/{n;p;}'

 # print 1 line of context before and after regexp, with line number
 # indicating where the regexp occurred (similar to "grep -A1 -B1")
 sed -n -e '/regexp/{=;x;1!p;g;$!N;p;D;}' -e h

 # grep for AAA and BBB and CCC (in any order)
 sed '/AAA/!d; /BBB/!d; /CCC/!d'

 # grep for AAA and BBB and CCC (in that order)
 sed '/AAA.*BBB.*CCC/!d'

 # grep for AAA or BBB or CCC (emulates "egrep")
 sed -e '/AAA/b' -e '/BBB/b' -e '/CCC/b' -e d    # most seds
 gsed '/AAA\|BBB\|CCC/!d'                        # GNU sed only

 # print paragraph if it contains AAA (blank lines separate paragraphs)
 # HHsed v1.5 must insert a 'G;' after 'x;' in the next 3 scripts below
 sed -e '/./{H;$!d;}' -e 'x;/AAA/!d;'

 # print paragraph if it contains AAA and BBB and CCC (in any order)
 sed -e '/./{H;$!d;}' -e 'x;/AAA/!d;/BBB/!d;/CCC/!d'

 # print paragraph if it contains AAA or BBB or CCC
 sed -e '/./{H;$!d;}' -e 'x;/AAA/b' -e '/BBB/b' -e '/CCC/b' -e d
 gsed '/./{H;$!d;};x;/AAA\|BBB\|CCC/b;d'         # GNU sed only

 # print only lines of 65 characters or longer
 sed -n '/^.\{65\}/p'

 # print only lines of less than 65 characters
 sed -n '/^.\{65\}/!p'        # method 1, corresponds to above
 sed '/^.\{65\}/d'            # method 2, simpler syntax

 # print section of file from regular expression to end of file
 sed -n '/regexp/,$p'

 # print section of file based on line numbers (lines 8-12, inclusive)
 sed -n '8,12p'               # method 1
 sed '8,12!d'                 # method 2

 # print line number 52
 sed -n '52p'                 # method 1
 sed '52!d'                   # method 2
 sed '52q;d'                  # method 3, efficient on large files

 # beginning at line 3, print every 7th line
 gsed -n '3~7p'               # GNU sed only
 sed -n '3,${p;n;n;n;n;n;n;}' # other seds

 # print section of file between two regular expressions (inclusive)
 sed -n '/Iowa/,/Montana/p'             # case sensitive

SELECTIVE DELETION OF CERTAIN LINES:

 # print all of file EXCEPT section between 2 regular expressions
 sed '/Iowa/,/Montana/d'

 # delete duplicate, consecutive lines from a file (emulates "uniq").
 # First line in a set of duplicate lines is kept, rest are deleted.
 sed '$!N; /^\(.*\)\n\1$/!P; D'

 # delete duplicate, nonconsecutive lines from a file. Beware not to
 # overflow the buffer size of the hold space, or else use GNU sed.
 sed -n 'G; s/\n/&&/; /^\([ -~]*\n\).*\n\1/d; s/\n//; h; P'

 # delete all lines except duplicate lines (emulates "uniq -d").
 sed '$!N; s/^\(.*\)\n\1$/\1/; t; D'

 # delete the first 10 lines of a file
 sed '1,10d'

 # delete the last line of a file
 sed '$d'

 # delete the last 2 lines of a file
 sed 'N;$!P;$!D;$d'

 # delete the last 10 lines of a file
 sed -e :a -e '$d;N;2,10ba' -e 'P;D'   # method 1
 sed -n -e :a -e '1,10!{P;N;D;};N;ba'  # method 2

 # delete every 8th line
 gsed '0~8d'                           # GNU sed only
 sed 'n;n;n;n;n;n;n;d;'                # other seds

 # delete lines matching pattern
 sed '/pattern/d'

 # delete ALL blank lines from a file (same as "grep '.' ")
 sed '/^$/d'                           # method 1
 sed '/./!d'                           # method 2

 # delete all CONSECUTIVE blank lines from file except the first; also
 # deletes all blank lines from top and end of file (emulates "cat -s")
 sed '/./,/^$/!d'          # method 1, allows 0 blanks at top, 1 at EOF
 sed '/^$/N;/\n$/D'        # method 2, allows 1 blank at top, 0 at EOF

 # delete all CONSECUTIVE blank lines from file except the first 2:
 sed '/^$/N;/\n$/N;//D'

 # delete all leading blank lines at top of file
 sed '/./,$!d'

 # delete all trailing blank lines at end of file
 sed -e :a -e '/^\n*$/{$d;N;ba' -e '}'  # works on all seds
 sed -e :a -e '/^\n*$/N;/\n$/ba'        # ditto, except for gsed 3.02.*

 # delete the last line of each paragraph
 sed -n '/^$/{p;h;};/./{x;/./p;}'

SPECIAL APPLICATIONS:

 # remove nroff overstrikes (char, backspace) from man pages. The 'echo'
 # command may need an -e switch if you use Unix System V or bash shell.
 sed "s/.`echo \\\b`//g"    # double quotes required for Unix environment
 sed 's/.^H//g'             # in bash/tcsh, press Ctrl-V and then Ctrl-H
 sed 's/.\x08//g'           # hex expression for sed 1.5, GNU sed, ssed

 # get Usenet/e-mail message header
 sed '/^$/q'                # deletes everything after first blank line

 # get Usenet/e-mail message body
 sed '1,/^$/d'              # deletes everything up to first blank line

 # get Subject header, but remove initial "Subject: " portion
 sed '/^Subject: */!d; s///;q'

 # get return address header
 sed '/^Reply-To:/q; /^From:/h; /./d;g;q'

 # parse out the address proper. Pulls out the e-mail address by itself
 # from the 1-line return address header (see preceding script)
 sed 's/ *(.*)//; s/>.*//; s/.*[:<] *//'

 # add a leading angle bracket and space to each line (quote a message)
 sed 's/^/> /'

 # delete leading angle bracket & space from each line (unquote a message)
 sed 's/^> //'

 # remove most HTML tags (accommodates multiple-line tags)
 sed -e :a -e 's/<[^>]*>//g;/</N;//ba'

 # extract multi-part uuencoded binaries, removing extraneous header
 # info, so that only the uuencoded portion remains. Files passed to
 # sed must be passed in the proper order. Version 1 can be entered
 # from the command line; version 2 can be made into an executable
 # Unix shell script. (Modified from a script by Rahul Dhesi.)
 sed '/^end/,/^begin/d' file1 file2 ... fileX | uudecode   # vers. 1
 sed '/^end/,/^begin/d' "$@" | uudecode                    # vers. 2

 # sort paragraphs of file alphabetically. Paragraphs are separated by blank
 # lines. GNU sed uses \v for vertical tab, or any unique char will do.
 sed '/./{H;d;};x;s/\n/={NL}=/g' file | sort | sed '1s/={NL}=//;s/={NL}=/\n/g'
 gsed '/./{H;d};x;y/\n/\v/' file | sort | sed '1s/\v//;y/\v/\n/'

 # zip up each .TXT file individually, deleting the source file and
 # setting the name of each .ZIP file to the basename of the .TXT file
 # (under DOS: the "dir /b" switch returns bare filenames in all caps).
 echo @echo off >zipup.bat
 dir /b *.txt | sed "s/^\(.*\)\.TXT/pkzip -mo \1 \1.TXT/" >>zipup.bat

TYPICAL USE: Sed takes one or more editing commands and applies all of
them, in sequence, to each line of input. After all the commands have
been applied to the first input line, that line is output and a second
input line is taken for processing, and the cycle repeats. The
preceding examples assume that input comes from the standard input
device (i.e, the console, normally this will be piped input). One or
more filenames can be appended to the command line if the input does
not come from stdin. Output is sent to stdout (the screen). Thus:

 cat filename | sed '10q'        # uses piped input
 sed '10q' filename              # same effect, avoids a useless "cat"
 sed '10q' filename > newfile    # redirects output to disk

For additional syntax instructions, including the way to apply editing
commands from a disk file instead of the command line, consult "sed &
awk, 2nd Edition," by Dale Dougherty and Arnold Robbins (O'Reilly,
1997; http://www.ora.com), "UNIX Text Processing," by Dale Dougherty
and Tim O'Reilly (Hayden Books, 1987) or the tutorials by Mike Arst
distributed in U-SEDIT2.ZIP (many sites). To fully exploit the power
of sed, one must understand "regular expressions." For this, see
"Mastering Regular Expressions" by Jeffrey Friedl (O'Reilly, 1997).
The manual ("man") pages on Unix systems may be helpful (try "man
sed", "man regexp", or the subsection on regular expressions in "man
ed"), but man pages are notoriously difficult. They are not written to
teach sed use or regexps to first-time users, but as a reference text
for those already acquainted with these tools.

QUOTING SYNTAX: The preceding examples use single quotes ('...')
instead of double quotes ("...") to enclose editing commands, since
sed is typically used on a Unix platform. Single quotes prevent the
Unix shell from intrepreting the dollar sign ($) and backquotes
(`...`), which are expanded by the shell if they are enclosed in
double quotes. Users of the "csh" shell and derivatives will also need
to quote the exclamation mark (!) with the backslash (i.e., \!) to
properly run the examples listed above, even within single quotes.
Versions of sed written for DOS invariably require double quotes
("...") instead of single quotes to enclose editing commands.

USE OF '\t' IN SED SCRIPTS: For clarity in documentation, we have used
the expression '\t' to indicate a tab character (0x09) in the scripts.
However, most versions of sed do not recognize the '\t' abbreviation,
so when typing these scripts from the command line, you should press
the TAB key instead. '\t' is supported as a regular expression
metacharacter in awk, perl, and HHsed, sedmod, and GNU sed v3.02.80.

VERSIONS OF SED: Versions of sed do differ, and some slight syntax
variation is to be expected. In particular, most do not support the
use of labels (:name) or branch instructions (b,t) within editing
commands, except at the end of those commands. We have used the syntax
which will be portable to most users of sed, even though the popular
GNU versions of sed allow a more succinct syntax. When the reader sees
a fairly long command such as this:

   sed -e '/AAA/b' -e '/BBB/b' -e '/CCC/b' -e d

it is heartening to know that GNU sed will let you reduce it to:

   sed '/AAA/b;/BBB/b;/CCC/b;d'      # or even
   sed '/AAA\|BBB\|CCC/b;d'

In addition, remember that while many versions of sed accept a command
like "/one/ s/RE1/RE2/", some do NOT allow "/one/! s/RE1/RE2/", which
contains space before the 's'. Omit the space when typing the command.

OPTIMIZING FOR SPEED: If execution speed needs to be increased (due to
large input files or slow processors or hard disks), substitution will
be executed more quickly if the "find" expression is specified before
giving the "s/.../.../" instruction. Thus:

   sed 's/foo/bar/g' filename         # standard replace command
   sed '/foo/ s/foo/bar/g' filename   # executes more quickly
   sed '/foo/ s//bar/g' filename      # shorthand sed syntax

On line selection or deletion in which you only need to output lines
from the first part of the file, a "quit" command (q) in the script
will drastically reduce processing time for large files. Thus:

   sed -n '45,50p' filename           # print line nos. 45-50 of a file
   sed -n '51q;45,50p' filename       # same, but executes much faster

If you have any additional scripts to contribute or if you find errors
in this document, please send e-mail to the compiler. Indicate the
version of sed you used, the operating system it was compiled for, and
the nature of the problem. To qualify as a one-liner, the command line
must be 65 characters or less. Various scripts in this file have been
written or contributed by:

 Al Aab                   # founder of "seders" list
 Edgar Allen              # various
 Yiorgos Adamopoulos      # various
 Dale Dougherty           # author of "sed & awk"
 Carlos Duarte            # author of "do it with sed"
 Eric Pement              # author of this document
 Ken Pizzini              # author of GNU sed v3.02
 S.G. Ravenhall           # great de-html script
 Greg Ubben               # many contributions & much help
```

## tcpdump_advanced_filters

```
Sebastien Wains <sebastien -the at sign- wains -dot- be>
https://www.wains.be

###################################################################

This page is NO LONGER UPDATED and might contain mistakes and typos.

It is kept around because this link has been published in books and blogs.

Please check the updated link:

https://blog.wains.be/2007/2007-10-01-tcpdump-advanced-filters/

###################################################################

Notes :

I usually always specify the interface from which to listen.. that's the -i option you will always see in the examples.
Indeed, I have tested each rule on my laptop over the wireless adapter which is eth1.

Feel free to contact me for comments, suggestions or for reporting mistakes.
I know I'm usually terrible at explaining stuff, so let me know if something is not clear.

I'll try to keep this document updated with new useful rules.


Before I begin with advanced filters, let's review the basic syntax of tcpdump

Basic syntax :
==============

Filtering hosts :
-----------------

- Match any traffic involving 192.168.1.1 as destination or source
# tcpdump -i eth1 host 192.168.1.1

- As soure only
# tcpdump -i eth1 src host 192.168.1.1

- As destination only
# tcpdump -i eth1 dst host 192.168.1.1


Filtering ports :
-----------------

- Match any traffic involving port 25 as source or destination
# tcpdump -i eth1 port 25

- Source
# tcpdump -i eth1 src port 25

- Destination
# tcpdump -i eth1 dst port 25


Network filtering :
-------------------

# tcpdump -i eth1 net 192.168
# tcpdump -i eth1 src net 192.168
# tcpdump -i eth1 dst net 192.168


Protocol filtering :
--------------------

# tcpdump -i eth1 arp
# tcpdump -i eth1 ip

# tcpdump -i eth1 tcp
# tcpdump -i eth1 udp
# tcpdump -i eth1 icmp


Let's combine expressions :
---------------------------

Negation    : ! or "not" (without the quotes)
Concatanate : && or "and"
Alternate   : || or "or" 

- This rule will match any TCP traffic on port 80 (web) with 192.168.1.254 or 192.168.1.200 as destination host
# tcpdump -i eth1 '((tcp) and (port 80) and ((dst host 192.168.1.254) or (dst host 192.168.1.200)))'

- Will match any ICMP traffic involving the destination with physical/MAC address 00:01:02:03:04:05
# tcpdump -i eth1 '((icmp) and ((ether dst host 00:01:02:03:04:05)))'

- Will match any traffic for the destination network 192.168 except destination host 192.168.1.200
# tcpdump -i eth1 '((tcp) and ((dst net 192.168) and (not dst host 192.168.1.200)))'


Advanced header filtering :
===========================

Before we continue, we need to know how to filter out info from headers

proto[x:y] 		: will start filtering from byte x for y bytes. ip[2:2] would filter bytes 3 and 4 (first byte begins by 0)
proto[x:y] & z = 0 	: will match bits set to 0 when applying mask z to proto[x:y]
proto[x:y] & z !=0 	: some bits are set when applying mask z to proto[x:y]
proto[x:y] & z = z 	: every bits are set to z when applying mask z to proto[x:y]
proto[x:y] = z 		: p[x:y] has exactly the bits set to z


Operators : >, <, >=, <=, =, !=


This may not be clear in the first place but you'll find examples below involving these.


Of course, it is important to know what the protocol headers look like before diving into more advanced filters.


IP header
---------

	0                   1                   2                   3   
	0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|Version|  IHL  |Type of Service|          Total Length         |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|         Identification        |Flags|      Fragment Offset    |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|  Time to Live |    Protocol   |         Header Checksum       |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|                       Source Address                          |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|                    Destination Address                        |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|                    Options                    |    Padding    | <-- optional
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|                            DATA ...                           |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+

I'll consider we are only working with the IPv4 protocol suite for these examples.

In an ideal world, every field would fit inside one byte. This is not the case, of course.

Are IP options set ?
--------------------

Let's say we want to know if the IP header has options set. We can't just try to filter out the 21st byte
because if no options are set, data start at the 21st byte. We know a "normal" header is usually 20 bytes 
(160 bits) long. With options set, the header is longer than that. The IP header has the header 
length field which we will filter here to know if the header is longer than 20 bytes.

	+-+-+-+-+-+-+-+-+
	|Version|  IHL  |
	+-+-+-+-+-+-+-+-+

Usually the first byte has a value of 01000101 in binary.

Anyhow, we need to divide the first byte in half...

0100 = 4 in decimal. This is the IP version.
0101 = 5 in decimal. This is the number of blocks of 32 bits in the headers. 5 x 32 bits = 160 bits or 20 bytes.

The second half of the first byte would be bigger than 5 if the header had IP options set.

We have two ways of dealing with that kind of filters.

1. Either try to match a value bigger than 01000101. This would trigger matches for IPv4 traffic with IP options set, 
   but ALSO any IPv6 traffic !

In decimal 01000101 equals 69.

Let's recap how to calculate in decimal.

0 : 0		\
1 : 2^6 = 64	 \ First field (IP version)
0 : 0		 /
0 : 0		/
-
0 : 0		\
1 : 2^2 = 4	 \ Second field (Header length)
0 : 0		 /
1 : 2^0 = 1	/

64 + 4 + 1 = 69

The first field in the IP header would usually have a decimal value of 69.
If we had IP options set, we would probably have 01000110 (IPv4 = 4 + header = 6), which in decimal equals 70.

This rule should do the job :
# tcpdump -i eth1 'ip[0] > 69'

Somehow, the proper way is to mask the first half/field of the first byte, because as mentionned earlier, 
this filter would match any IPv6 traffic.

2. The proper/right way : "masking" the first half of the byte

0100 0101 : 1st byte originally
0000 1111 : mask (0xf in hex or 15 in decimal). 0 will mask the values while 1 will keep the values intact.
=========
0000 0101 : final result

You should see the mask as a power switch. 1 means on/enabled, 0 means off/disabled.

The correct filter :

In binary
# tcpdump -i eth1 'ip[0] & 15 > 5'

or 

In hexadecimal
# tcpdump -i eth1 'ip[0] & 0xf > 5'

I use hex masks.

Recap.. That's rather simple, if you want to :
- keep the last 4 bits intact, use 0xf (binary 00001111)
- keep the first 4 bits intact, use 0xf0 (binary 11110000)


DF bit (don't fragment) set ?
-----------------------------

Let's now trying to know if we have fragmentation occuring, which is not desirable. Fragmentation occurs 
when a the MTU of the sender is bigger than the path MTU on the path to destination.

Fragmentation info can be found in the 7th and 8th byte of the IP header.

	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|Flags|      Fragment Offset    |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+

Bit 0: 	reserved, must be zero
Bit 1: 	(DF) 0 = May Fragment, 1 = Don't Fragment.
Bit 2: 	(MF) 0 = Last Fragment, 1 = More Fragments.

The fragment offset field is only used when fragmentation occurs.

If we want to match the DF bit (don't fragment bit, to avoid IP fragmentation) :

The 7th byte would have a value of :
01000000 or 64 in decimal

# tcpdump -i eth1 'ip[6] = 64'


Matching fragmentation ?
------------------------

- Matching MF (more fragment set) ? This would match the fragmented datagrams but wouldn't match the last 
  fragment (which has the 2nd bit set to 0).
# tcpdump -i eth1 'ip[6] = 32'

The last fragment have the first 3 bits set to 0... but has data in the fragment offset field.

- Matching the fragments and the last fragments
# tcpdump -i eth1 '((ip[6:2] > 0) and (not ip[6] = 64))'

A bit of explanations :
"ip[6:2] > 0" would return anything with a value of at least 1
We don't want datagrams with the DF bit set though.. the reason of the "not ip[6] = 64"

If you want to test fragmentation use something like :
ping -M want -s 3000 192.168.1.1


Matching datagrams with low TTL
-------------------------------

The TTL field is located in the 9th byte and fits perfectly into 1 byte.
The maximum decimal value of the TTL field is thus 255 (11111111 in binary).

This can be verified :
$ ping -M want -s 3000 -t 256 192.168.1.200
ping: ttl 256 out of range

	+-+-+-+-+-+-+-+-+
	|  Time to Live |
	+-+-+-+-+-+-+-+-+

We can try to find if someone on our network is using traceroute by using something like this on the gateway :
# tcpdump -i eth1 'ip[8] < 5'


Matching packets longer than X bytes
------------------------------------

Where X is 600 bytes

# tcpdump -i eth1 'ip[2:2] > 600'


More IP filtering
-----------------

We could imagine filtering source and destination addresses directly in decimal addressing.
We could also match the protocol by filtering the 10th byte.

It would be pointless anyhow, because tcpdump makes it already easy to filter out that kind of info.


TCP header
----------

	0                   1                   2                   3   
	0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|          Source Port          |       Destination Port        |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|                        Sequence Number                        |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|                    Acknowledgment Number                      |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|  Data |       |C|E|U|A|P|R|S|F|                               |
	| Offset|  Res. |W|C|R|C|S|S|Y|I|            Window             | 
	|       |       |R|E|G|K|H|T|N|N|                               |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|           Checksum            |         Urgent Pointer        |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|                    Options                    |    Padding    |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
	|                             data                              |
	+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+

- Matching any TCP traffic with a source port > 1024
# tcpdump -i eth1 'tcp[0:2] > 1024'

- Matching TCP traffic with particular flag combinations

The flags are defined in the 14th byte of the TCP header.

	+-+-+-+-+-+-+-+-+
	|C|E|U|A|P|R|S|F|
	|W|C|R|C|S|S|Y|I|
	|R|E|G|K|H|T|N|N|
	+-+-+-+-+-+-+-+-+

In the TCP 3-way handshakes, the exchange between hosts goes like this :

1. Source sends SYN 
2. Destination answers with SYN, ACK 
3. Source sends ACK

- If we want to match packets with only the SYN flag set, the 14th byte would have a binary 
  value of 00000010 which equals 2 in decimal.
# tcpdump -i eth1 'tcp[13] = 2'

- Matching SYN, ACK (00010010 or 18 in decimal)
# tcpdump -i eth1 'tcp[13] = 18'

- Matching either SYN only or SYN-ACK datagrams
# tcpdump -i eth1 'tcp[13] & 2 = 2'

We used a mask here. It will returns anything with the ACK bit set (thus the SYN-ACK combination as well)

Let's assume the following examples (SYN-ACK)

00010010 : SYN-ACK packet
00000010 : mask (2 in decimal)
--------
00000010 : result (2 in decimal)

Every bits of the mask match !

- Matching PSH-ACK packets
# tcpdump -i eth1 'tcp[13] = 24'

- Matching any combination containing FIN (FIN usually always comes with an ACK so we either 
  need to use a mask or match the combination ACK-FIN)
# tcpdump -i eth1 'tcp[13] & 1 = 1'

- Matching RST flag
# tcpdump -i eth1 'tcp[13] & 4 = 4'

Actually, there's an easier way to filter flags :
# tcpdump -i eth1 'tcp[tcpflags] == tcp-ack'

- Matching all packages with TCP-SYN or TCP-FIN set : 
# tcpdump 'tcp[tcpflags] & (tcp-syn|tcp-fin) != 0


By looking at the TCP state machine diagram (http://www.wains.be/pub/networking/tcp_state_machine.jpg)
we can find the different flag combinations we may want to analyze.

Ideally, a socket in ACK_WAIT mode should not have to send a RST. It means the 3 way handshake has not completed.
We may want to analyze that kind of traffic.


Matching SMTP data :
--------------------

I will make a filter that will match any packet containing the "MAIL" command from SMTP exchanges.

I use something like http://www.easycalculation.com/ascii-hex.php to convert values from ASCII to hexadecimal.

"MAIL" in hex is 0x4d41494c

The rule would be :

# tcpdump -i eth1 '((port 25) and (tcp[20:4] = 0x4d41494c))'

It will check the bytes 21 to 24. "MAIL" is 4 bytes/32 bits long.. 

This rule would not match packets with IP options set.

This is an example of packet (a spam, of course) :

# tshark -V -i eth0 '((port 25) and (tcp[20:4] = 0x4d41494c))'
Capturing on eth0
Frame 1 (92 bytes on wire, 92 bytes captured)
    Arrival Time: Sep 25, 2007 00:06:10.875424000
    [Time delta from previous packet: 0.000000000 seconds]
    [Time since reference or first frame: 0.000000000 seconds]
    Frame Number: 1
    Packet Length: 92 bytes
    Capture Length: 92 bytes
    [Frame is marked: False]
    [Protocols in frame: eth:ip:tcp:smtp]
Ethernet II, Src: Cisco_X (00:11:5c:X), Dst: 3Com_X (00:04:75:X)
    Destination: 3Com_X (00:04:75:X)
        Address: 3Com_X (00:04:75:X)
        .... ...0 .... .... .... .... = IG bit: Individual address (unicast)
        .... ..0. .... .... .... .... = LG bit: Globally unique address (factory default)
    Source: Cisco_X (00:11:5c:X)
        Address: Cisco_X (00:11:5c:X)
        .... ...0 .... .... .... .... = IG bit: Individual address (unicast)
        .... ..0. .... .... .... .... = LG bit: Globally unique address (factory default)
    Type: IP (0x0800)
Internet Protocol, Src: 62.163.X (62.163.X), Dst: 192.168.X (192.168.X)
    Version: 4
    Header length: 20 bytes
    Differentiated Services Field: 0x00 (DSCP 0x00: Default; ECN: 0x00)
        0000 00.. = Differentiated Services Codepoint: Default (0x00)
        .... ..0. = ECN-Capable Transport (ECT): 0
        .... ...0 = ECN-CE: 0
    Total Length: 78
    Identification: 0x4078 (16504)
    Flags: 0x04 (Don't Fragment)
        0... = Reserved bit: Not set
        .1.. = Don't fragment: Set
        ..0. = More fragments: Not set
    Fragment offset: 0
    Time to live: 118
    Protocol: TCP (0x06)
    Header checksum: 0x08cb [correct]
        [Good: True]
        [Bad : False]
    Source: 62.163.X (62.163.X)
    Destination: 192.168.X (192.168.XX)
Transmission Control Protocol, Src Port: 4760 (4760), Dst Port: smtp (25), Seq: 0, Ack: 0, Len: 38
    Source port: 4760 (4760)
    Destination port: smtp (25)
    Sequence number: 0    (relative sequence number)
    [Next sequence number: 38    (relative sequence number)]
    Acknowledgement number: 0    (relative ack number)
    Header length: 20 bytes
    Flags: 0x18 (PSH, ACK)
        0... .... = Congestion Window Reduced (CWR): Not set
        .0.. .... = ECN-Echo: Not set
        ..0. .... = Urgent: Not set
        ...1 .... = Acknowledgment: Set
        .... 1... = Push: Set
        .... .0.. = Reset: Not set
        .... ..0. = Syn: Not set
        .... ...0 = Fin: Not set
    Window size: 17375
    Checksum: 0x6320 [correct]
        [Good Checksum: True]
        [Bad Checksum: False]
Simple Mail Transfer Protocol
    Command: MAIL FROM:<wguthrie_at_mysickworld--dot--com>\r\n
        Command: MAIL
        Request parameter: FROM:<wguthrie_at_mysickworld--dot--com>


Matching HTTP data :
--------------------

Let's make a filter that will find any packets containing GET requests
The HTTP request will begin by :

GET / HTTP/1.1\r\n (16 bytes counting the carriage return but not the backslashes !)

If no IP options are set.. the GET command will use the byte 20, 21 and 22
Usually, options will take 12 bytes (12nd byte indicates the header length, which should report 32 bytes). 
So we should match bytes 32, 33 and 34 (1st byte = byte 0).

Tcpdump is only able to match data size of either 1, 2 or 4 bytes, we will take the following ASCII 
character following the GET command (a space)

"GET " in hex : 47455420
 
# tcpdump -i eth1 'tcp[32:4] = 0x47455420'


Matching HTTP data (exemple taken from tcpdump man page) : 

# tcpdump -i eth1 'tcp port 80 and (((ip[2:2] - ((ip[0]&0xf)<<2)) - ((tcp[12]&0xf0)>>2)) != 0)'

          +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
ip[2:2] = |          Total Length         |
	  +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+

	+-+-+-+-+-+-+-+-+
ip[0] =	|Version|  IHL  |
	+-+-+-+-+-+-+-+-+

	     +-+-+-+-+-+-+-+-+
ip[0]&0xf =  |# # # #|  IHL  | <-- that's right, we masked the version bits with 0xf or 00001111 in binary
	     +-+-+-+-+-+-+-+-+

          +-+-+-+-+
	  |  Data |
tcp[12] = | Offset|
	  |       |
	  +-+-+-+-+

So what we are doing here is "(IP total length - IP header length - TCP header length) != 0"

We are matching any packet that contains data.


We are taking the IHL (total IP lenght


Matching other interesting TCP things :
---------------------------------------

SSH connection (on any port) : 
We will be looking for the reply given by the SSH server.
OpenSSH usually replies with something like "SSH-2.0-OpenSSH_3.6.1p2".
The first 4 bytes (SSH-) have an hex value of 0x5353482D.

# tcpdump -i eth1 'tcp[(tcp[12]>>2):4] = 0x5353482D'

If we want to find any connection made to older version of OpenSSH (version 1, which are insecure and subject to MITM attacks) : 
The reply from the server would be something like "SSH-1.99.."

# tcpdump -i eth1 '(tcp[(tcp[12]>>2):4] = 0x5353482D) and (tcp[((tcp[12]>>2)+4):2] = 0x312E)'

Explanation of >>2 can be found below in the reference section.


UDP header
----------

  0      7 8     15 16    23 24    31  
 +--------+--------+--------+--------+ 
 |     Source      |   Destination   | 
 |      Port       |      Port       | 
 +--------+--------+--------+--------+ 
 |                 |                 | 
 |     Length      |    Checksum     | 
 +--------+--------+--------+--------+ 
 |                                   | 
 |              DATA ...             |
 +-----------------------------------+                 

Nothing really interesting here.

If we want to filter ports we would use something like :
# tcpdump -i eth1 udp dst port 53


ICMP header
-----------

See different ICMP messages :
http://img292.imageshack.us/my.php?image=icmpmm6.gif

We will usually filter the type (1 byte) and code (1 byte) of the ICMP messages.

Here are common ICMP types :

  0	Echo Reply				 [RFC792]
  3	Destination Unreachable			 [RFC792]
  4	Source Quench			 	 [RFC792]
  5	Redirect				 [RFC792]
  8	Echo					 [RFC792]
 11	Time Exceeded				 [RFC792]

We may want to filter ICMP messages type 4, these kind of messages are sent in case of congestion of the network.
# tcpdump -i eth1 'icmp[0] = 4'


If we want to find the ICMP echo replies only, having an ID of 500. By looking at the image with all the ICMP packet description
we see the ICMP echo reply have the ID spread across the 5th and 6th byte. For some reason, we have to filter out with the value in hex.

# tcpdump -i eth0 '(icmp[0] = 0) and (icmp[4:2] = 0x1f4)'


References
----------

tcpdump man page : http://www.tcpdump.org/tcpdump_man.html
Conversions : http://easycalculation.com/hex-converter.php
Filtering HTTP requests : http://www.wireshark.org/tools/string-cf.html
Filtering data regardless of TCP options : http://www.wireshark.org/lists/wireshark-users/201003/msg00024.html

Just in case the post disappears, here's a copy of the last URL :

From: Sake Blok <sake@xxxxxxxxxx>
Date: Wed, 3 Mar 2010 22:42:29 +0100
Or if your capturing device is capable of interpreting tcpdump style filters (or more accurately, BPF style filters), you could use:

tcp[(((tcp[12:1] & 0xf0) >> 2) + 8):2] = 0x2030

Which in English would be: 
- take the upper 4 bits of the 12th octet in the tcp header ( tcp[12:1] & 0xf0 )
- multiply it by four ( (tcp[12:1] & 0xf0)>>2 ) which should give the tcp header length
- add 8 ( ((tcp[12:1] & 0xf0) >> 2) + 8 ) gives the offset into the tcp header of the space before the first octet of the response code
- now take two octets from the tcp stream, starting at that offset ( tcp[(((tcp[12:1] & 0xf0) >> 2) + 8):2]  )
- and verify that they are " 0" ( = 0x2030 )

Of course this can give you false positives, so you might want to add a test for "HTTP" and the start of the tcp payload with:

tcp[((tcp[12:1] & 0xf0) >> 2):4] = 0x48545450

resulting in the filter:

tcp[((tcp[12:1] & 0xf0) >> 2):4] = 0x48545450 and tcp[(((tcp[12:1] & 0xf0) >> 2) + 8):2] = 0x2030

A bit cryptic, but it works, even when TCP options are present (which would mess up a fixed offset into the tcp data).

Cheers,
Sake


The end ? 
---------

Please send more useful recipes !
```

## distros - Android

[GitHub - mikeroyal/Android-Guide: Android Guide](https://github.com/mikeroyal/Android-Guide)

[GitHub - it-shark-pro/mobile-android: Materials about development for Android](https://github.com/it-shark-pro/mobile-android)

[GitHub - Kingbond470/Android-Resource: To Speed Up Your App Development](https://github.com/Kingbond470/Android-Resource)

[GitHub - OpenSouce-LNMIIT/Android-Development-Resources: Learning resources for android development](https://github.com/OpenSouce-LNMIIT/Android-Development-Resources)

[GitHub - wahibhaq/ultimate-resources-android-devs: Compiled & Curated List of Resources for Android Developers](https://github.com/wahibhaq/ultimate-resources-android-devs)

[Android Tutorial => Getting started with Android](https://riptutorial.com/android)

## distros - Arch Linux

[mikeroyal/Arch-Linux-Guide: Arch Linux Guide](https://github.com/mikeroyal/Arch-Linux-Guide)

[i dont have ethernet, how can i install arch without internet?](https://old.reddit.com/r/archlinux/comments/15m7sbl/i_dont_have_ethernet_how_can_i_install_arch/)

[Should You Install Arch Linux? 10 Reasons for Arch-Based Distros](https://www.makeuseof.com/tag/reasons-install-arch-linux)

[The Arch Linux Handbook - Learn Arch Linux for Beginners](https://www.freecodecamp.org/news/how-to-install-arch-linux)

[GitHub - PandaFoss/Awesome-Arch: A complete list of Arch-based projects](https://github.com/PandaFoss/Awesome-Arch)

## distros - BSD - FreeBSD

[Resources for Newbies](https://www.freebsd.org/projects/newbies/)

[FreeBSD jail - Wikipedia](https://en.wikipedia.org/wiki/FreeBSD_jail)

## distros - BSD

[GitHub - SaintFenix/Awesome-BSD-Ports-Programs-And-Projects: A Repo Detailing BSD Ports, Programs, and Projects.](https://github.com/SaintFenix/Awesome-BSD-Ports-Programs-And-Projects)

## distros - BSD - OpenBSD

[OpenBSD](https://www.openbsd.org/)
multi-platform 4.4BSD-based UNIX-like operating system.
[OpenBSD PF: User's Guide](https://www.openbsd.org/faq/pf)

## distros - Fedora

[GUIDE: How packages get from Fedora to you, and where to look for news! : Fedora](https://old.reddit.com/r/Fedora/comments/wle02w/guide_how_packages_get_from_fedora_to_you_and)

## distros - Fuchsia OS

[GitHub - mikeroyal/Fuchsia-Guide: Fuchsia Guide](https://github.com/mikeroyal/Fuchsia-Guide)

## distros - Gentoo

[install gentoo wiki](https://wiki.installgentoo.com/index.php/Main_Page)
[install gentoo wiki](https://web.archive.org/web/20210102182957/https://wiki.installgentoo.com/index.php/Main_Page)
the /g/ wiki

[Babbies First Linux - InstallGentoo Wiki](https://wiki.installgentoo.com/wiki/Babbies_First_Linux#What_does_.2Fg.2F_use.3F)
[Babbies First Linux - InstallGentoo Wiki](https://wiki.installgentoo.com/index.php/Babbies_First_Linux)

## distros - Guix

[GitHub - techenthusiastsorg/awesome-guix: Awesome list of resources about GNU Guix](https://github.com/techenthusiastsorg/awesome-guix)

## distros - Kali Linux

[How to Install Kali Linux on Your Computer](https://www.freecodecamp.org/news/how-to-install-kali-linux)

## distros - Linux Mint

[mikeroyal/Linux-Mint-Guide: Linux Mint Guide](https://github.com/mikeroyal/Linux-Mint-Guide)

## distros - NixOS

[Zero to Nix, an unofficial, opinionated, gentle introduction to Nix | Hacker News](https://news.ycombinator.com/item?id=34490376)
[Zero to Nix](https://zero-to-nix.com/)

## distros - RHEL

[RedHat](https://developers.redhat.com/)
Development Tutorials

[Learn User Management in RHEL: A Comprehensive Guide](https://www.freecodecamp.org/news/learn-user-management-in-rhel-a-comprehensive-guide/)

## distros - Sailfish

[Sailfish 4 | Hacker News](https://news.ycombinator.com/item?id=28313750)
[Sailfish OS fourth generation - Sailfish OS](https://sailfishos.org/)

## distros - SE Linux

[How to Secure Linux Servers with SE Linux](https://www.freecodecamp.org/news/securing-linux-servers-with-se-linux)

## distros - Simula One

[Show HN: Simula One - Portable Linux VR Computer | Hacker News](https://news.ycombinator.com/item?id=30440828)
[SimulaVR Store](https://shop.simulavr.com/)

[SimulaVR Has Been Subpoenaed by Meta Platforms, Inc | Hacker News](https://news.ycombinator.com/item?id=33108050)
[SimulaVR](https://simulavr.com/blog/subpoenaed-by-meta/)

## distros - Snakeware

[Snakeware - Linux distro with Python userspace inspired by Commodore 64 | Hacker News](https://news.ycombinator.com/item?id=33003245)
[GitHub - joshiemoore/snakeware: A free Linux distro with a Python-based userspace](https://github.com/joshiemoore/snakeware)

## distros - Spectrum

[Spectrum, a step towards usable secure computing](https://spectrum-os.org)

## distros - Ubuntu

[Enterprise Open Source and Linux | Ubuntu](https://ubuntu.com)

[GitHub - mikeroyal/Perfect-Ubuntu-Guide: Ubuntu Guide. Learn about getting your Ubuntu Desktop/Server ready for development. Including Ubuntu Security, Graphics (AMD/NVIDIA/Intel ARC), and Software Apps.](https://github.com/mikeroyal/Perfect-Ubuntu-Guide)

[How to get root on Ubuntu 20.04 by pretending nobody's /home | Hacker News](https://news.ycombinator.com/item?id=25053238)
[How to get root on Ubuntu 20.04 by pretending nobody's /home | GitHub Security Lab](https://securitylab.github.com/research/Ubuntu-gdm3-accountsservice-LPE/)

[Install Ubuntu on a Chromebook | Ubuntu](https://ubuntu.com/tutorials/install-ubuntu-on-chromebook#1-overview)

## distros - Zorin OS

[GitHub - mikeroyal/Zorin-OS-Guide: Zorin OS Guide](https://github.com/mikeroyal/Zorin-OS-Guide)
