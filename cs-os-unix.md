
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

Even [Apple](cs-os-apple.md) uses a Unix framework, for both macOS and iOS, but its key difference is that it's a hybrid of a ["monolithic kernel" and "microkernel"](cs-os.md), while Linux is *strictly* a monolithic kernel.

## Usage

Linux is lightweight, so it's excellent for low-profile computers, and is even convenient to run off a flash drive.

However, unlike [Windows](cs-os-windows.md), Linux has *also* become more consistently reliable.

The largest failure within Linux is tied to its [UX](engineering-design.md). For the most part, its [GUI](engineering-graphics.md) commands convert to [console commands](cs-cli.md), meaning any sufficient experience with Linux often requires accessing a terminal. This creates [a learning curve beyond the aptitude of some people](computers.md).

## Linux tips

Here are a few tips to avoid making awful mistakes while using Linux:

- If there's any stock software the OS came with (such as a [file manager](cs-files.md) or software-based [keyboard](cs-keyboard.md)), *do not uninstall it*. If you want something new, simply install the new one and use it.
- Don't bother trying to run a common Windows-based software that has a Linux alternative (e.g., Microsoft Office). You *can* use the Windows-based interface (called "Wine"), but you'll usually have a better time with a Linux-based alternative if the software is even remotely popular.
- Most of the Linux-based [UI](engineering-design.md) lacks polish, but does the job relatively well. You'll find much more satisfaction if you observe the features those things have that proprietary software *doesn't* have.
- Websearch frequently what you don't know. Your lack of knowledge isn't new, and there's usually an answer somewhere about it.

Most "original equipment manufacturers" (OEMs) that come with [Windows](cs-os-windows.md) do *not* consider that you'd want to install Linux or dual-boot. Usually, you'll first need to find a way into the BIOS, then boot from a USB drive. If you're dual-booting, you may need to select your OS from the boot menu *every time*.

## More information

- [DistroWatch.com visual family tree of Linux distributions](https://distrowatch.com/dwres.php?resource=family-tree)
