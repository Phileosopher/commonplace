
# What an operating system is

The engineer who designs a general-purpose computer only has a vague idea of the kinds of stuff someone could do on that computer. They have no idea if the person who buys the computer will play games, send emails, or download adult entertainment.

Thus, a computer should be ready to handle *anything* that the person wants to do. The system that handles how everything operates is called an "operating system", or OS for short.

Altogether, the actual implementation of an OS is a keyboard (stdin or Channel 0) which sends processes to then present on a [screen](engineering-screen.md) (stdout or Channel 1).

- In one sense, it's the philosophical finish line for all [software development](cs-software.md).
- This always uses a [CPU](cs-cpu.md) with its [memory](cs-memory.md) cache, and most of time will output final work to hard drive memory. Errors can pass to a different output (stderr or Channel 2).
- Since it's an implementation, stdin and stdout can be redirected.

Because of their ubiquity, the most popular operating systems more-or-less set the [standards](cs-standards.md) for how *all* operating systems run:

- An Apple-proprietary OS called macOS. It had many great ideas (and has some of the best [UX](engineering-design.md) around), but has fallen in quality as of the early 2020s. It still comes on Apple desktops/laptops. It's based on Unix. Apple also has iOS for their mobile devices that was directly pulled from macOS.
- A Microsoft-proprietary OS called [Windows](cs-os-windows.md) that blatantly ripped off macOS dominated the market in the 1980s because it was affordable and ran on most computers. As of 2022, it still dominates the desktop/laptop PC market.
- An [open-source](legal-ip-floss.md) kernel of [Unix](cs-os-unix.md) called Linux. It has a vast variety of "distros", so it's a bit more open-ended.
- A Google-proprietary OS [built on Linux](cs-os-unix.md) called Android. It runs on most mobile devices that don't run iOS, though [lawsuits against Google's user data policies](cs-bigtech.md) may change that from their hold in the early 2020s.

## Kernel design

At the bottom of the OS is the kernel, which contains the drivers for the [hardware](cs-hardware.md).

There are two major approaches to OS design that represent a spectrum:

- A "microkernel" only manages what it has to: [CPU](cs-cpu.md), [memory](cs-memory.md), and IPC ("inter-process communication"). They are extremely portable and take up very little memory. Only specific processes run as "superuser". However, the hardware needs more "device drivers" to run peripherals, the processes will have to wait in line to get information, and the processes won't be able to access other processes.
- A "monolithic kernel" is also managing the CPU, memory, and IPC, but also includes managing the drivers, files, and "system calls". Everything runs in supervisor mode, and the OS takes more memory. However, it's faster, and the programs can easily handle hardware.

[Windows](cs-os-windows.md) and Mac are hybrid kernels that mix both of the architecture designs, while [Linux](cs-os-unix.md) is strictly monolithic.

In a broad sense, there are 6 layers to most operating systems, though this isn't a hard rule, and many layers merge together:

1. Hardware - deals with system "drivers" (such as the [screen](engineering-screen.md), [keyboard](cs-keyboard.md), [mouse](cs-mouse.md), [printer](engineering-printers.md), [scanner](cs-ocr.md), etc.).
2. Scheduling - manages the processes that pipe their way to the [CPU](cs-cpu.md).
3. [Memory](cs-memory.md) management - manages moving information back-and-forth between long-term storage and RAM.
4. Process management - prioritizes the various tasks based on multiple possible algorithms.
5. I/O buffer - keeps close track of what the user is inputting *and* what's getting outputted.
6. User programs - the myriad programs that run on top of everything else, typically according to the user's preference.

However, even with a shaved-down system where the layers are merged together will always have an outermost layer for user programs and an innermost layer for the hardware. Each of the layers will be able to access the things *below* it, but not above.

It's worth noting that most operating systems don't display everything they *can* do, since [design concepts](engineering-design.md) would make that experience too complicated for the average user. There's a constant tradeoff between boring [command-line interfaces](cs-cli.md) and [elaborate graphical interfaces](engineering-graphics.md).

Because tech-savvy people and tech-retarded people have completely different opinions on what constitutes a workable interface and [file arrangement](cs-files.md), there are a wide variety of interfaces to fit every need, with their own CPU labor costs involved.

## Disks

Managing partitions, disk images, defragmenting platter drives, trimming solid state drives, and auto-mounting drives are *all* standard features of most operating systems.

To maintain the file system, there is a delay between the request and the actual modification of the disk, so engineers designed a "journaling" file system to keep track of changes that haven't happened. The system keeps a circular log, which is a fixed-size buffer with a first-in first-out that allows the system to resume where it left off in an interruption like a power failure.

## Programs

A program is a set of instructions that the computer can run.

Beyond core programs necessary to keep the computer going (and are therefore broadly part of the operating system), there are two other kinds of programs:

- Utility programs that are non-essential but assist with the operating system (e.g., [antivirus](cs-infosec.md), disk scanners)
- Applications, which are what the user actually uses

When a program [creates variables and runs functions](cs-langs.md), the operating system can run allocate a memory stack for the program ("stack memory allocation"). Then, when the program ends, the operating system will deallocate that memory.

The other option is to store program memory in a heap with all the other programs ("heap memory allocation"). This is easier to make (and used to be the *only* way to run an operating system), but can cause memory leaks if the program's programmer forgot to release the memory before terminating the program.

Whenever a program is running, it creates at least one task in the operating system (a "process"). Some processes only start when the user interacts with it, but many processes (such as the clock) run *constantly* on a rhythm in the background.

Each process starts *from* a [file](cs-files.md), but many processes write *to* files or call *other* processes. Processes can "pipeline" data to another process and grab more input data. Since *all* the processes are pipelining, the entire computer can look a bit like a factory assembly line.

### Utility software

Keeping an OS running well requires several support software, which are usually installed alongside the OS itself.

There are many default programs built into most general-purpose operating systems:

- File management system that allows for file access, reading, writing, moving, and deleting, which likely will need to also optimize those files in the long-term
- System monitoring and log viewer
- Disk management system that mounts and manages partitions
- Memory information software, such as disk space usage
- Disk defragmenter (for [older hard drives](cs-memory.md))
- Translation [protocols](cs-standards.md) that convert information into different formats for various needs
- A program that monitors and displays other running programs:
  - Windows - press CTRL+SHIFT+ESC (or CTRL+ALT+DEL if it's an old version of Windows)
  - Linux - type "top" from a terminal (or quickly upgrade to htop with "sudo [usually apt or dnf] install htop")
  - Mac - access via Launchpad->Other->Activity Monitor or the Dock's Application/Utilities/Activity Monitor
- Notifications to indicate events from the system or relevant updated information from across a [network](cs-networks.md)
- A "clipboard" system that allows copying something, then pasting it somewhere else

### Desktop uses

Since non-tech people are less attentive than tech people to what the computer is doing or what they should do, most consumer computers need some extra utility programs:

- A shortcut system that allows quick access to programs, documents, and various scripts. In a [console-based GUI](cs-cli.md), quick-reference help documentation on the commands and their syntax
- To prevent [malicious actors](cs-infosec-pentest.md), a built-in scanner/verification process to [authenticate](cs-infosec-authentication.md) the validity of a program that's about to run

#### GUI

Most programs can activate with commands. While the information once outputted through a [printer](engineering-printers.md), the OS now typically displays a [GUI](engineering-graphics.md) ("graphical user interface") on a [screen](engineering-screen.md).

We take *many* [GUI features](engineering-design.md) for granted in most consumer operating systems:

- A context menu button, either by long-press, right-clicking, or clicking while pressing a function key.
- A panel/taskbar that shows currently open programs, the date and time, and some common controls.
- A list of available programs, often [searchable](cs-langs-algorithms.md).
- Default folders for documents, pictures, videos, and a visual "desktop" for easy access to files.
- A dock for commonly used programs.
- Automatic file associations (e.g., .doc files open with Microsoft Word).
- The ability to download/copy and install/run new programs and device drivers that don't come with the OS.
- Personal customization features for background wallpaper, colors, mouse pointers, folder view settings, etc.
- Detecting newly plugged-in hardware (e.g., scanner, keyboard, game controller) along with activating *functional* default device drivers for them (which takes a lot more work than it sounds).
- Somewhere where programmers and IT technicians can view [system error logs](cs-software-redesign.md).

All these GUI features packaged together create a "desktop environment", which constitutes the basis for how most users interpret their experience with a computer.

#### What the user actually wants

For most typical people, they expect some software automatically, so most OS automatically come with it to avoid any nuisance:

- [Web browser](cs-browser.md), which is about 99% of a computer's use for most people
- Text editor
- [Text character](cs-keyboard.md) selector
- Basic calculator
- Basic timer/alarm
- Image viewer
- Multimedia player (e.g., VLC)
  - While the software often comes pre-installed with at least some [media codecs](engineering-graphics.md), they usually need extra installation as well.
- Basic painting and image editing program
- Office suite software (e.g., LibreOffice):
  - Word processor
  - Spreadsheet manager
  - Presentation software
  - [Vector](engineering-graphics.md) drawing
  - [Database](database.md) manager
  - [Mathematical formula](math.md) editor
- Document viewer (e.g., PDFs)

Further, many users have a variety of common needs:

- Email client
- Audio editor (e.g., Audacity)
- Advanced image management (e.g., GIMP, Krita, Inkscape)
- 3D modeling (e.g., Blender)
- Batch image management (e.g., ImageMagick)

However, for any general-purpose computer, the user should be free to add more software. This can represent through several options:

- Software that accesses a central repository of more software (i.e., app store, package repository)
- The ability to install software separately, which is sometimes called "sideloading" if it's outside a standardized central repository.

### Server uses

There's no reason to add extra resources to an OS when it's a server, especially at scale. for this reason, GUIs are conspicuously absent from many servers, where everything is done via [CLI](cs-cli.md).

While a server can serve just about anything, there are a few standard server applications for most use cases:

- Web server for [the internet](cs-software-webdev.md):
  - HTTP server: send [web browser](cs-browser.md) content
  - DHCP server: map computers to IPs
  - DNS server: map IPs to domains
- [Database](database.md) server
- [File](cs-files.md) server
- [Print](engineering-printers.md) server

## Development

Designing "native" OS [GUI-based](engineering-graphics.md) applications is a headache compared to [web apps](cs-sofware-webdev.md). Each operating system has its own [specific knowledge](mind-understanding.md). Most of that knowledge is built around various methods to get software even working correctly. Plus, each proprietary OS (such as Apple) has an approval process that makes it even more complicated (e.g., App Store).
