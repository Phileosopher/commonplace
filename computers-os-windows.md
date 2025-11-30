
# Microsoft Windows explained

Most people on the planet with a computer have at least heard of Microsoft Windows, but most people aren't aware of much more than its brand and [marketing](marketing.md).

## Licensing

It's important to understand how Microsoft made their money with Windows compared to the competition:

- Apple sold their operating system on their computers (meaning people bought the hardware *and* software).
- Nearly everything in [the Unix world](computers-os-unix.md) was [open-source](legal-ip-floss.md) (i.e., paying for service agreements or hardware more than software).
- Windows made money exclusively on their licenses to run their operating system.

A consumer buying a computer would ask if the computer had Windows, and either the manufacturer had Windows pre-installed with a Microsoft-approved license or the consumer had to buy and install it themselves. "Digital rights management" (DRM) was maintained with a specific license key on the sleeve of the installation disk. Now, the DRM is written right into the computer's motherboard.

This license arrangement meant that Windows made money when they were able to motivate people to upgrade, and the OS' design still holds true today. However, while the old upgrades were inherently superior (Windows 95 to 98, for example), it's been much easier since the 2010s to force people to upgrade by making the present operating system progressively worse via incremental updates.

## History

Before Windows was MS-DOS, a [command-line interface](computers-cli.md) released in 1981.

- MS-DOS rapidly became ubiquitous with personal computing because Microsoft's creator, Bill Gates, scored a nonexclusive [contract](people-contracts.md) with IBM.
- To IBM's misfortune, the contract meant Microsoft was [licensed](legal-ip-floss.md) to run MS-DOS on *anything* that could support it, and consumers didn't really care what computer it ran on as much as IBM thought they would.

Windows 1.0 was released in 1985, and ran as software on top of MS-DOS.

- Windows was more user-friendly by integrating use of the [computer mouse](computers-mouse.md) for *everything*.
- It was widely popular, and became the standard operating system on most computers for at least a few decades.

Microsoft Windows, up through Windows 3.1, was originally a blatant ripoff of [Mac OS](computers-os-apple.md), and copied most of the conveniences of Apple's [design](engineering-design.md). Since it was more affordable than Macintosh computers, and ran on almost anything, Windows was able to [dominate the operating system market](faang.md). Even in the 2020s, [Linux](computers-os-unix.md) has made some good contenders, but Windows is still the convention for most non-mobile personal computers.

Windows forked a version of Windows called Windows NT in 1993.

- It was designed for [commercial use](computers-distsys-enterprise.md) (i.e., multiple users across potentially multiple computes with tons of tracking).
- Most consumer users would *never* care for the features in Windows NT.
- Eventually, its title changed to Windows 2000, then Windows Server, and has been Windows Server ever since.

Windows 95 changed out its design from its 3.1 roots, since Microsoft didn't want a [lawsuit](faang.md) from Apple.

- Windows 95 had an industry-changing [interface](engineering-design.md) because it was the first OS to use a child-friendly setup.
- It used a Start menu in the bottom-left corner (named Start to provoke the user to act), and a visual desktop folder that displayed on the main screen. One of the running jokes for a while was that you had to select Start to shut down.
- It introduced a taskbar and notification area, which kept the active programs easily accessible and viewable.
- Instead of using MS-DOS, the computer could [boot](computers-boot.md) straight into Windows.
- Some utilities, like "Device Manager" and "Task Manager", were so useful and effective that they haven't changed *at all* in decades.
- The "killer apps" were in Microsoft Office: Word and Excel specifically (Excel originally being a ripoff of VisiCalc).
- One of Windows 95's quirky limitations was that it stored the time in a 32-bit register, so it only permitted 4,294,967,296 milliseconds of "uptime", which translates to roughly 49.7 days until it glitched out and crashed.

Windows 98 was a vast improvement of almost everything in Windows 95, but not much changed.

- It was more stable than Windows 95, but beyond some graphical improvements, was just about the same as Windows 95 internally.

Windows Me was an attempt to rush a consumer-based Windows NT to market, released in 2000.

- The OS ended up as nothing more than a visually polished Windows 95 with a hybrid [16/32-bit architecture](computers-cpu.md).
- It was meant as a holdover until Windows XP, and should have undergone more [debugging](computers-software-redesign.md).

The high point of Windows was indisputably with Windows XP, released in 2001.

- It was thoroughly stable, kept driver backups in case a device driver failed, had a Prefetch feature that preloaded the [RAM](computers-memory.md) with frequently accessed programs, and ran strictly on a 32-bit architecture.
- It borrowed heavily from Windows NT, and many [enterprise-grade](computers-distsys-enterprise.md) features were available inside the system.
- It was also "backwards-compatible" to other Windows software with Compatibility Mode.
- It also had multiple GUI updates that took advantage of the improved [graphics processing](engineering-graphics.md) from the early 2000s.
- While its mainstream support ended in 2009, it ended extended support in 2014, and 13 years is an *eternity* in technology terms.

Windows' [trend](trends.md) of improvement wobbled around, starting with Windows Vista, released in 2007.

- While Vista was mostly the same as XP, it added a Superfetch feature, which loaded *all* the RAM with readily accessible programs. This slowed down Windows to the point that every "power user" would get frustrated by it, and most people weren't willing to take the upgrade.

Windows 7, released in 2009, added some much-needed UI improvements, and fixed most of what what wrong with Windows Vista.

- It was a stable and workable operating system again.
- However, as of 2025, it is the last high-quality Windows that didn't require a vastly more powerful computer than the operating system's minimum recommended specifications.
- They also ended long-term support for it, meaning that [Ubuntu](computers-os-unix.md) is a better option for a low-spec computer.

Mobile devices were becoming more ubiquitous, and Microsoft tried to build Windows 8 to merge the mobile/desktop experience as an all-in-one solution, released in 2012.

- The system was filled with horrible [UX](engineering-design.md) mistakes: getting rid of the familiar Start menu, mapping the mouse to the swipe features that a touchscreen usually had, using stock photography without any labels, and burying extremely common tasks 4-5 menus deep.
- It was such a terrible system that Microsoft released a free upgrade to a fixed version called Windows 8.1 that was a bit more like Windows 7.

By this point, consumers had lost most of their desire to get a new version of Windows. There was no reason to try the new one.

- In an attempt at restoring faith in consumers, Microsoft released Windows 10 in 2015 for free to anyone who had Windows 7, 8, or 8.1.
- Windows 10 was, effectively, an inferior version of Windows 7.
- By the time Windows 10 came around, the only major licensing profit Microsoft could glean was from the OEMs ("original equipment manufacturers").

Windows 11 didn't do much to add to the experience, and wasn't met with much fanfare in 2021.

- Microsoft added interface elements that made it look more like macOS.
- On the back-end, Windows 11 was Windows 10 that sent more user data, which has been [trending away from acceptable](faang.md) for many people.

## .NET

On the development side, one of the most significant portions of Windows comes through the .NET framework. It's a Microsoft-specific framework that builds features and elements for an ever-increasing variety of [programming languages](computers-languages.md).

.NET also has its uses on Linux and Mac, but since it *is* Microsoft, the .NET framework is inextricably married to Windows. It's a good framework generally, though it's very much [proprietary](legal-ip-floss.md).

ASP.NET was designed to expand .NET into [web apps](computers-sofware-webdev.md) by using the C# language instead of JavaScript. Developers have mixed opinions about it: it's trying to create a fire-and-forget set of solutions, but particularly intelligent [software designers](computers-software.md) will find it irritating.

## Updates

Windows Update was once a useful feature. It released patches that [fixed bugs](computers-software-redesign.md).

However, around the time Windows Phone was released in 2010, Microsoft shifted their approach:

- Before, they had a gigantic room with every type of computer on the market in it, and rolled out an update to visually watch what would happen.
- To cut costs, Microsoft replaced that department with Windows Phone, then used [virtualization](computers-distsys-vm.md) from then on to track any issues before sending it out.
- This caused a catastrophic set of Windows updates in the early 2010s.

Since then, Windows updates have become staggered, and release a bit like vaccines or prescription drugs:

1. Release the updates to a small percentage of the computers (maybe 1-2%), many of them being part of the Windows Insider program.
2. Watch what happens for a month or two by reading bug reports sent back. "Roll back" any changes if those computers crash.
3. Roll out to a larger percentage of the computers (possibly 10-30%).
4. Watch what happens, which will presumably be about the same issues but with more conspicuous "edge cases".
5. Roll that update out to all the computers, while continuously monitoring for any future bugs.

This makes the computer updates reliable-enough, effectively over 99%, with a minimal chance of any computer crashing.

## Not broken doesn't mean fixed

Operating systems need constant [redesign](computers-software-redesign.md) to stay current to the changes in technology. They have to accommodate better [memory](computers-memory.md), more streamlined [programming languages](computers-languages.md), and [UX improvements](engineering-design.md).

At the same time, updating takes time and money. Most PCs have come pre-installed with Windows, so the executives who run Microsoft don't necessarily need to work at creating an ideal user experience, unless everyone were to leave for [Linux](computers-os-unix.md).

Windows became the dominant OS for a very long time. It is now so popular that people use it strictly out of convention.

So, since Windows 7, most of the Windows experience has gone downhill. The system has gotten buggier, UX improvements are often *worse* than their predecessors, and the operating system has slowly devolved into near-unreliability.

Further, Windows 11 now demonstrates their primary profit motive comes less from bringing a meaningful user experience than from [collecting user data](faang.md).

However, for anyone who finds Windows irritating enough, Linux has reached a state of maturity where it is now universally better than Windows. In fact, many Windows-based [software emulation](computers-distsys-vm.md) through Linux (typically via the Wine software) is *better* than running it natively on Windows!

## Not broken

At the same time, Windows isn't inherently defective.

- The built-in Windows Defender [antivirus software](computers-cysec.md) is well-designed, and none of the other antivirus software products are particularly necessary if you're [avoiding dodgy websites and not running malicious software](safety-computers.md).
- All the programs will run, even when various dumb processes create tremendous memory overhead.

It's relatively easy to tweak and improve the Windows OS to make it run more efficient, even if the interface often requires odd UI gymnastics and registry tweaks to pull off:

- Turn off all privacy settings that may send user data to Microsoft.
- Harden Windows' built-in antivirus: Windows Defender.

Of course, since it's proprietary, and Microsoft doesn't make too much money off it, Windows may fade in the coming decades. Windows XP's source code was supposedly leaked online, but it's completely possible that it was a subversive effort directly from Microsoft (alongside Windows Subsystem for Linux, or WSL) to offload the operating system's maintenance to the [open-source community](legal-ip-floss.md).
