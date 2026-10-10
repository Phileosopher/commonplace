
# The Apple operating system

Apple is a very different tech company than the other operating systems because it's the only company that somehow has maintained both an OS and the hardware it sits on.

- Most other companies (e.g., IBM) either became hardware-focused exclusively and gave the driver code to others.
- Google may be the closest to this, but they're somewhat cheating with Android OS because it's a version of [Linux](cs-os-unix.md).

One of the unique qualities about Apple is that it is *both* [monolithic and microkernel](cs-os.md). It also happens to be the only major [Big Tech](cs-bigtech.md) company from a long time ago that releases *both* hardware and the operating system with it.

The microkernel part of Apple is XNU (which stands for "XNU is Not Unix" because programmers like recursions), which consists of several components:

- Carnegie Mellon University's Mach kernel
- FreeBSD components
- IOKit, the C++ [API](cs-software.md) for writing drivers

Apple development is a bit risky for [software development](cs-software.md) because the company has a record of not caring for independent developers. As a *customer* Apple bends over backwards, and their in-house developers are great. But, it's better to be a [web developer](cs-software-webdev.md) or find another [operating system](cs-os.md) to build on, especially since Apple tries to set trends and constantly sunsets projects.
