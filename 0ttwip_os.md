
The engineer who designs a general-purpose computer only has a vague idea of the kinds of stuff someone could do on that computer. They have no idea if the person who buys the computer will play games, send emails, or download adult entertainment.

Thus, a computer should be ready to handle *anything* that the person wants to do. The system that handles how everything operates is called an "operating system", or OS for short.

Because of their ubiquity, the most popular operating systems more-or-less set the standards for how *all* operating systems run:

- An Apple-proprietary OS called MacOS. It had many great ideas (and has some of the best [UX](design-uxui.md) around), but has fallen in quality as of the early 2020's. It still comes on Apple desktops/laptops. It's based on Unix. Apple also has iOS for their mobile devices that was directly pulled from MacOS.
- A Microsoft-proprietary OS called [Windows](computers-os-windows.md) that blatantly ripped off MacOS dominated the market in the 1980's because it was affordable and ran on most computers. As of 2022, it still dominates the desktop/laptop PC market.
- An [open-source](legal-ip-floss.md) kernel of [Unix](computers-os-unix.md) called Linux. It has a vast variety of "distros", so it's a bit more open-ended.
- A Google-proprietary OS built on Linux called Android. It runs on most mobile devices that don't run iOS, though [lawsuits against Google's user data policies](faang.md) may change that from their hold in the early 2020's.

## Kernel design

There only two major approaches to OS design, but they all sit on a spectrum between two philosophies.

- A "microkernel" only manages what it has to: [CPU](computers-cpu.md), [memory](computers-memory.md), and IPC ("inter-process communication"). They are extremely portable and take up very little memory. Only specific processes run as "superuser". However, the hardware needs more "device drivers" to run peripherals, the processes will have to wait in line to get information, and the processes won't be able to access other processes.
- A "monolithic kernel" is also managing the CPU, memory, and IPC, but also includes managing the drivers, files, and "system calls". Everything runs in supervisor mode, and the OS takes more memory. However, it's faster, and the programs can easily handle hardware.

[Windows](computers-os-windows.md) and Mac are hybrid kernels that mix both of the architecture designs, while [Linux](computers-os-unix.md) is strictly monolithic.

In a broad sense, there are 6 layers to most operating systems, though this isn't a hard rule, and many layers merge together:

1. Hardware - deals with system "drivers" (such as the [screen](computers-screen.md), [keyboard](computers-keyboard.md), [mouse](computers-mouse.md), [printer](computers-printers.md), [scanner](computers-ocr.md), etc.).
2. Scheduling - manages the processes that pipe their way to the [CPU](computers-cpu.md).
3. [Memory](computers-memory.md) management - manages moving information back-and-forth between long-term storage and RAM.
4. Process management - prioritizes the various tasks based on multiple possible algorithms.
5. I/O buffer - keeps close track of what the user is inputting *and* what's getting outputted.
6. User programs - the myriad programs that run on top of everything else, typically according to the user's preference.

However, even with a shaved-down system where the layers are merged together will always have an outermost layer for user programs and an innermost layer for the hardware. Each of the layers will be able to access the things *below* it, but not above.

It's worth noting that most operating systems don't display everything they *can* do, since [design concepts](design-uxui.md) would make that experience too complicated for the average user. There's a constant tradeoff between boring [command-line interfaces](computers-cli.md) and [elaborate graphical interfaces](graphics.md).

Because tech-savvy people and tech-retarded people have completely different opinions on what constitutes a workable interface and [file arrangement](computers-files.md), there are a wide variety of interfaces to fit every need, with their own CPU labor costs involved.

## Programs

A program is a set of instructions that the computer can run.

When a program [creates variables and runs functions](programming-basics.md), the operating system can run allocate a memory stack for the program ("stack memory allocation"). Then, when the program ends, the operating system will deallocate that memory.

The other option is to store program memory in a heap with all the other programs ("heap memory allocation"). This is easier to make (and used to be the *only* way to run an operating system), but can cause memory leaks if the program's programmer forgot to release the memory before terminating the program.

Whenever a program is running, it creates at least one task in the operating system (a "process"). Some processes only start when the user interacts with it, but many processes (such as the clock) run *constantly* on a rhythm in the background.

Each process starts *from* a [file](computers-files.md), but many processes write *to* files or call *other* processes. Processes can "pipeline" data to another process and grab more input data. Since *all* the processes are pipelining, the entire computer can look a bit like a factory assembly line.

There are many default programs built into most general-purpose operating systems:

- A disk management system that mounts and manages partitions.
- A file management system that allows for file access, reading, writing, moving, and deleting, which likely will need to also optimize those files in the long-term.
- Translation [protocols](standards-computers.md) that convert information into different formats for various needs.
- A program that monitors and displays other running programs:
  - Windows - press CTRL+SHIFT+ESC (or CTRL+ALT+DEL if it's an old version of Windows)
  - Linux - type "top" from a terminal (or quickly upgrade to htop with "sudo [usually apt or dnf] install htop")
  - Mac - access via Launchpad->Other->Activity Monitor or the Dock's Application/Utilities/Activity Monitor
- Notifications to indicate events from the system or relevant updated information from across a [network](networks-computer.md).
- A shortcut system that allows quick access to programs, documents, and various scripts. In a [console-based GUI](computers-cli.md), quick-reference help documentation on the commands and their syntax.
- A "clipboard" system that allows copying something, then pasting it somewhere else.
- To prevent [malicious actors](computers-cysec-pentest.md), a built-in scanner/verification process to [authenticate](computers-cysec-authentication.md) the validity of a program that's about to run.

## GUI

Most programs can activate with commands. While the information once outputted through a [printer](computers-printers.md), the OS now typically displays a [GUI](graphics.md) ("graphical user interface") on a [screen](computers-screen.md).

We take *many* [GUI features](design-uxui.md) for granted in most consumer operating systems:

- A context menu button, either by long-press, right-clicking, or clicking while pressing a function key.
- A panel/taskbar that shows currently open programs.
- A list of available programs, often [searchable](programming-algorithms.md).
- Default folders for documents, pictures, videos, and a visual "desktop" for easy access to files.
- Automatic file associations (e.g., .doc files open with Microsoft Word).
- The ability to download/copy and install/run new programs and device drivers that don't come with the OS.
- Personal customization features for background wallpaper, colors, mouse pointers, folder view settings, etc.
- Detecting newly plugged-in hardware (e.g., scanner, keyboard, game controller) along with activating *functional* default device drivers for them (which takes a lot more work than it sounds).
- Somewhere where programmers and IT technicians can view [system error logs](computers-software-redesign.md).

## Development

Designing "native" OS [GUI-based](graphics.md) applications is a headache compared to [web apps](computers-webdev.md). Each operating system has its own [specific knowledge](understanding.md). Most of that knowledge is built around various methods to get software even working correctly. Plus, each proprietary OS (such as Apple) has an approval process that makes it even more complicated (e.g., App Store).
