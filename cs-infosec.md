
# What cybersecurity and information security is

Essentially, cybersecurity is [security](safety-security.md), but applied to computers and their information, broadly called "assets". Since not all information in a computer is the same, some of that information is higher-priority than other information and needs more security.

- It's worth noting that the idea of cybersecurity broadens to "information security" or "infosec" when it deals with the people involved, while cybersecurity is the maintenance of the systems themselves.

To successfully protect information, you have to understand [the mind of a hacker](cs-infosec-pentest.md).

- That doesn't mean you need to [hack yourself](mind-creativity-hacking.md), but you *do* need to understand the criminal mentality of a hacker and how they tend to think.

Keeping computers safe can be complicated, so there are 3 major approaches to it:

1. Ad hoc based, which is essentially doing what [feels](mind-feelings.md) right at the time or vendor recommendations.
2. [Risk-bsaed](cs-infosec-riskmgmt.md), which involves assessing risks and acting on them.
3. [Compliance-based](cs-infosec-compliance.md), which involves making and following [standards](standards.md) and [rules](people-rules.md).
   - It's worth noting that compliance-based management is *also* risk-based, but more stringent and with dumb requirements that don't always apply to common sense.

Broadly, information security is built on the "CIA triad", which represents as confidentiality, integrity, and availability:

1. Confidentiality: only authorized users can access it
2. Integrity: the information hasn't been tampered with
3. Availability: the information can be accessed by authorized users

CIA, like the [project management triangle](mgmt-2_projects-theories.md), has tradeoffs:

- If you want something private and safe, it won't be easy to access.
- If you want something easy to access and private, it won't be easy to keep it safe.
- If you want something safe and easy to access, it won't be easy to keep it private.

There are several ways that information can be stolen or destroyed:

- Duplicating information, which is like theft but without any recognized loss by the owner until that information is used or accessed.
- Information is deleted or corrupted, either maliciously or unintentionally.
- Information is intentionally changed, often for the purpose of misleading or disruption.
- Permanently locking information off from accessing (such as a forgotten password).
- Information getting stolen, which is duplicating and then deleting information.

## Safety measures

It's critical to use some type of verification for a program, and there are [many elements](cs-infosec-authentication.md) for making it reliable and effective.

Further, [hardening your networks and OS](cs-infosec-hardening.md) is critical.

## Scanning software

The highest-risk [files](cs-files.md) for a computer to keep functioning (and thereby enforce [authentication](cs-infosec-authentication.md)) are core system files, so an [operating system](cs-os.md) has a constant need to track *any* changes to them.

A "firewall" is meant to stop hackers from accessing the computer in the first place. It's a set of rules that it applies to any data packets that pass through it. They are usually "stateful" now and often analyze the [application layer](cs-networks.md) for policy violations. Because of how complicated and interconnected networks have gotten, cybersecurity professionals debate quite a bit about how effective firewalls really are.

A much elaborate system than a firewall is called an IPS or IDS ("intrusion prevention/detection system") depending on how active the software protects you from the problem.

"Antivirus software" scans specific files or file systems to find malicious code. They can also scan emails or web hyperlinks.

Some malware/antivirus scanners are "persistent" (always running) and others have to be activated when you want to use them. Because the more robust effort that persistent scanners like Norton and McAfee have to do to verify *everything* the computer does, they're often a *huge* drain on resources and will cause everything to slow down.

Since AV software is sometimes notoriously difficult to remove (since the software often doesn't trust that you're removing it on purpose), many technicians joke that certain AV software are viruses of its own. In fact, AV software is often unnecessary bloatware that preys on users' fears, and [some of them are mine cryptocurrency at the users' expense](cs-bigtech.md).

## Memory security

Keeping the computer "known-good" is ideal, so maintaining the state of a working machine is the best way to keep the computer accessible.

- This means that, barring security updates, the best thing to do is to *not* install updates as soon as they release.
- For many systems, this may mean automatically turning off updates and then manually running them when you know you have time to revert the system if something breaks.

For the sake of protecting information, most of the components of a computer are perfectly fine if they are ever stolen:

- Peripherals without onboard long-term memory (e.g. [mice](cs-mouse.md), [keyboards](cs-keyboard.md), cheaper [printers](engineering-printers.md)).
- [CPUs](cs-cpu.md)
- Short-term [memory](cs-memory.md)

However, [long-term memory can be *highly* risky](cs-infosec-cysec-memory.md) if accessed or stolen. A hard drive possesses all the information a computer has (minus the [BIOS information](cs-boot.md)) as soon as the computer is turned off.

Either way, make sure you have all important information synchronized in real-time to another networked drive.

- If you can't, for whatever reason, have the data on a second drive altogether (and not simply a recovery partition).

Abide by the 3-2-1 [backup](cs-infosec-cysec-memory.md) rule:

- 3 copies of the data
- 2 different [storage media](cs-memory.md)
- 1 copy is off-site (just in case of theft or [disaster](hardship-disaster-1_short.md))

For heavier backup needs, the most common backup scheme is the Grandfather/Father/Son (GFS) approach:

1. Perform incremental backups every day to a "Son" media, maybe sometimes more than once a day, with the 5 days on a revolving rotation.
2. Every week (often Friday) there's a full backup to a "Father" media, with 5 of them for each of the weeks in a month.
3. At the end of the last working day of the month make a "Grandfather" media, with 12 of them for each month.
4. Each day, week, and month after the first uses the earliest backup for a new batch of media.

## Virtualization

One of the best ways to protect a computer from the outside is to operate as many programs as possible inside a [virtual environment](cs-distsys-vm.md). Some operating systems (like Qubes) are designed *entirely* around this concept.

## Decentralization

Keeping multiple redundant systems allows a safe solution in case anything is taken offline.

However, decentralization is *much* easier if the data doesn't change (such as with [torrenting](cs-distsys-p2p-torrent.md)).

Further, the attack vectors are multiplied in relation to the number of decentralized nodes. If there's any sort of [exploit](cs-infosec-exploits.md) on one node, the entire system could be at risk.

## The cybersecurity community

Cybersecurity is a community effort, and multiple organizations including the Open Web Application Security Project (OWASP) maintain tons of data and [standards](cs-standards.md) on Common Vulnerabilities and Exposures (CVE), as well as Common Weakness Enumeration (CWE).

## Dark web

Every domain of society has a [black market](money-economics.md), and the computer version of this is the "dark web".

Essentially, the internet isn't solely a collection of publicly accessible [websites](cs-browser.md). It also has many elements that are limited from standard consumption. For example, [torrents](cs-distsys-p2p-torrent.md) and [blockchain](cs-blockchain.md) sit within the internet, but not within a standard web browser experience.

### Tor

One option for maintaining anonymity is to use the [Tor browser](https://www.torproject.org/), which uses Tor (short for The Onion Router). It was originally a [fork](cs-software-versionctrl.md) of Firefox, and is a privacy-focused mode of web browsing. This has a limited scope compared to VPNs, but it operates as a type of parallel to typical web access.

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
