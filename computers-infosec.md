
# What cybersecurity and information security is

Keeping computers safe can be complicated.

Essentially, cybersecurity is [security](safety-security.md), but applied to computers and their information, broadly called "assets". Since not all information in a computer is the same, some of that information is higher-priority than other information and needs more security.

- It's worth noting that the idea of cybersecurity broadens to "information security" or "infosec" when it deals with the people involved, while cybersecurity is the maintenance of the systems themselves.

To successfully protect information, you have to understand [the mind of a hacker](computers-infosec-pentest.md).

- That doesn't mean you need to [hack yourself](mind-creativity-hacking.md), but you *do* need to understand the criminal mentality of a hacker and how they tend to think.

Broadly, information security is built on the "CIA triad", which represents as confidentiality, integrity, and availability:

1. Confidentiality: only authorized users can access it
2. Integrity: the information hasn't been tampered with
3. Availability: the information can be accessed by authorized users

There are several ways that information can be stolen or destroyed:

- Duplicating information, which is like theft but without any recognized loss by the owner until that information is used or accessed.
- Information is deleted or corrupted, either maliciously or unintentionally.
- Information is intentionally changed, often for the purpose of misleading or disruption.
- Permanently locking information off from accessing (such as a forgotten password).
- Information getting stolen, which is duplicating and then deleting information.

Technology is usually safest when abiding by the CIA acronym:

- Confidentiality - the information only gets accessed by approved people/computers.
- Integrity - the information wasn't messed with or destroyed.
- Availability - the people/computers who want/need the information can get it.

More information means more risk, so it's wisest to destroy legitimately useless information whenever possible.

- Formatting and destroying unused disks is critical.
  - When formatting, clear the MBR as well (which can often be done through the "fdisk /MBR" command).
  - If you're not outright destroying the data, zero out all the data by clearing it with multiple passes. Traditionally, 7 passes was the standard, but that was when [storage](computers-memory.md) was magnetic hard drives, so it may not need that many.

Further, the more complexity in the system, the more risks inherent to the system, since it creates more [attack vectors](computers-infosec-pentest.md).

## Authentication

It's critical to use some type of verification for a program, and there are [many elements](computers-infosec-authentication.md) for making it reliable and effective.

## Network hardening

Making a [computer network](computers-networks.md) involves adding communication features between computers. By contrast, [network hardening](computers-infosec-cysec-network.md) involves *removing or disabling* all unnecessary features authorized users won't use.

### Specific network hardening tricks

If you're particularly paranoid, make sure to change your devices' MAC address, since that MAC has the origination and likely information about the firmware on it.

Have a burner browser to work with any suspicious situations.

- Even if you use privacy-minded things browser features (e.g. private windows, no cookies), some services will still detect other content in that browser.
- For this reason, have a "burner" browser that has absolutely nothing in it.
- Preferably, it should use a different framework (e.g., Firefox uses Gecko, Brave uses Chromium)

## Scanning software

The highest-risk [files](computers-files.md) for a computer to keep functioning (and thereby enforce [authentication](computers-infosec-authentication.md)) are core system files, so an [operating system](computers-os.md) has a constant need to track *any* changes to them.

A "firewall" is meant to stop hackers from accessing the computer in the first place. It's a set of rules that it applies to any data packets that pass through it. They are usually "stateful" now and often analyze the [application layer](computers-networks.md) for policy violations. Because of how complicated and interconnected networks have gotten, cybersecurity professionals debate quite a bit about how effective firewalls really are.

A much elaborate system than a firewall is called an IPS or IDS ("intrusion prevention/detection system") depending on how active the software protects you from the problem.

"Antivirus software" scans specific files or file systems to find malicious code. They can also scan emails or web hyperlinks.

Some malware/antivirus scanners are "persistent" (always running) and others have to be activated when you want to use them. Because the more robust effort that persistent scanners like Norton and McAfee have to do to verify *everything* the computer does, they're often a *huge* drain on resources and will cause everything to slow down.

Since AV software is sometimes notoriously difficult to remove (since the software often doesn't trust that you're removing it on purpose), many technicians joke that certain AV software are viruses of its own. In fact, AV software is often unnecessary bloatware that preys on users' fears, and [some of them are mine cryptocurrency at the users' expense](computers-bigtech.md).

## Memory security

For the sake of protecting information, most of the components of a computer are perfectly fine if they are ever stolen:

- Peripherals without onboard long-term memory (e.g. [mice](computers-mouse.md), [keyboards](computers-keyboard.md), cheaper [printers](engineering-printers.md)).
- [CPUs](computers-cpu.md)
- Short-term [memory](computers-memory.md)

However, [long-term memory can be *highly* risky](computers-infosec-cysec-memory.md) if accessed or stolen. A hard drive possesses all the information a computer has (minus the [BIOS information](computers-boot.md)) as soon as the computer is turned off.

Either way, make sure you have all important information synchronized in real-time to another networked drive.

- If you can't, for whatever reason, have the data on a second drive altogether (and not simply a recovery partition).

Abide by the 3-2-1 [backup](computers-infosec-cysec-memory.md) rule:

- 3 copies of the data
- 2 different [storage media](computers-memory.md)
- 1 copy is off-site (just in case of theft or [disaster](hardship-disaster-1_short.md))

## Virtualization

One of the best ways to protect a computer from the outside is to operate as many programs as possible inside a [virtual environment](computers-distsys-vm.md). Some operating systems (like [Qubes](https://www.qubes-os.org/)) are designed *entirely* around this concept.

## Decentralization

Keeping multiple redundant systems allows a safe solution in case anything is taken offline.

However, decentralization is *much* easier if the information doesn't move around (such as with [torrenting](computers-distsys-p2p-torrent.md)).

Further, the attack vectors are multiplied in relation to the number of decentralized nodes. If there's any sort of [exploit](computers-infosec-exploits.md) on one node, the entire system could be at risk.

## Dark web

Every domain of society has a [black market](money-economics.md), and the computer version of this is the "dark web".

Essentially, the internet isn't solely a collection of publicly accessible [websites](computers-browser.md). It also has many elements that are limited from standard consumption. For example, [torrents](computers-distsys-p2p-torrent.md) and [blockchain](computers-blockchain.md) sit within the internet, but not within a standard web browser experience.

### Tor

One option for maintaining anonymity is to use the [Tor browser](https://www.torproject.org/), which uses Tor (short for The Onion Router). It was originally a [fork](computers-software-versionctrl.md) of Firefox, and is a privacy-focused mode of web browsing. This has a limited scope compared to VPNs, but it operates as a type of parallel to typical web access.

- The downside of this, however, is that there are *many* sketchy people using it for very bad activities (e.g., child pornography). If traced, you'd likely be associated with that activity.
- While it may even be profitable, running a Tor exit node can hold you [liable](legal-safety.md) for other people doing very [immoral](morality-evil.md) things.

The one difference between accessing a Tor and a VPN is that each of the hops is a new layer of encryption (which is why it's called an onion). With a VPN, the client computer sees the VPN host's IP address, and a Tor exit node operates the same way.

It's important, however, to not access Tor with a regular web browser, due to how slow it drags and what it needs for maintaining privacy:

- Disable JavaScript to avoid any tracking, since JS often gives clues on the browser and connection.
- Video should be disabled, given how utterly slow everything runs on the Tor network.
- All Tor exit IPs are publicly known, so be mindful if you're doing anything that's at all questionable.
- Tor has been compromised, so nothing is fully private on it anymore for someone who wants to find out.

Tor has received negative attention from vague popularized concepts about the "[dark web](mind-creativity-hacking.md)". While there *have* been drug deals, counterfeiting, and other illicit activity taking place over Tor, the urban myths have escalated to implying crowd-funded assassinations.

In all reality, there are likely more legitimate services from privacy-concerned individuals on the Onion Network than illegitimate ones.

Tor also serves as a useful tech admin tool, since you have access to multiple random IP addresses.

## More information

Tutorials and guides:

- [awesome-cyber-security-university](https://github.com/brootware/awesome-cyber-security-university)

Notes:

- [SecNotes](https://github.com/0xRar/SecNotes)
