
Keeping computers safe can be complicated.

Essentially, cybersecurity is [security](https://notageni.us/security/), but applied to computers and their information, broadly called "assets". Since not all information in a computer is the same, some of that information is higher-priority than other information and needs more security.

Broadly, there are several ways information can be stolen or destroyed:

- Duplicating information, which is like theft but without any realized loss by the owner until the information is used.
- Information is deleted or corrupted, either maliciously or unintentionally.
- Information is intentionally changed, often for the purpose of misleading or disruption.
- Permanently locking information off from accessing (such as a forgotten password).
- Information getting stolen, which is duplicating and then deleting information.

Technology is usually safest when abiding by the CIA acronym:

- Confidentiality - the information only gets accessed by approved people/computers.
- Integrity - the information wasn't messed with or destroyed.
- Availability - the people/computers who want/need the information can get it.

Cybersecurity professionals use human rules ("policies") and computer rules ("permissions") to create "protection rings" around computer information or technology, which are are layers of security. The x86 protection rings, for example:

- Ring 0 - core operating system files
- Ring 1 - drivers for important hardware
- Ring 2 - drivers for not-as-important hardware
- Ring 3 - applications

If you want extra security, tell the computer to use 2 or 3 "factors" to "authenticate" the user instead of just one:

- Something you know - e.g., a password
- Something you have - e.g., a mobile phone or social media account
- Something you are - e.g., a fingerprint or retina scan

* * * * *

## Backups

The easiest way to protect computer information from being lost is to keep regular, consistent backups of everything. That way, if anything fails, you can revert to a "known good" configuration or set of files.

A backup can be cold or hot storage:

- A synchronized "hot storage" backup a long distance away, just in case your house is hit by a flood or tornado.
- A sporadically synchronized "cold storage", to hold known-good information indefinitely without a synchronization overwriting it.

A hard drive will eventually fail, and more quickly if it's consumer-grade. For a lasting backup, pay very close attention to "write tolerance" and "over-provisioning" to see how long that drive will last.

To prevent a lightning strike or power outage from destroying hardware, get an "uninterruptible power supply" (UPS). A power strip can stop surges, but a UPS will also give enough time to save any important work before powering off the computer.

* * * * *

## Authentication

It's critical to use some type of verification for a program, and there are [many elements](/authentication/) for making it reliable and effective.

Most operating system security consists of sequential layers of authentication. More authentication factors means more complexity.

* * * * *

## Network hardening

Making a network secure includes *many* inter-related and comparatively smaller tasks.

### Blocking transfer

Most computer security policies manage specific portions of what the computer interacts with:

- Blocking specific ports that will likely send particular unwanted [protocols](/protocols/).
- Blocking [networks](/networks/) that may be insecure.
- Blocking certain forms of code that may run on system files or read user-made documents.

Disable *any* unused ports:

- IP ports
- Physical ports like USB, Ethernet, cameras, microphones, etc. (including the built-in ones)
- Wireless ports
- Any hardware or peripherals you don't use

Many internet [protocols](/protocols/) are unsecure (e.g., Telnet), so disabling them cuts down the risk of "network sniffing".

Disable internet router features that won't be used:

- IPv6
- Remote Web Administration
- Bluetooth
- Wi-Fi
- Universal Plug n Play (UPnP) has been compromised for a while.
- WPS (Wi-Fi Protected Setup) involves joining a wireless network by pressing a button on the router and entering an 8-digit pit, but hackers were able to [brute force](/hacking/) that PIN as of 2011.
- Turn gateway devices to Bridge mode unless they're the means of connecting to the internet.

### E2E

One of the most important aspects of keeping a network safe is to have "end-to-end [encryption](/encryption/)" (E2E). This doesn't simply mean the network transfers information securely or that it stores it securely, but that *every* step of the transaction is securely handling the information. This requires awareness of each stage of the network transfer and computer's use of the information, and what keeps data safe.

### DNS

One of the easiest forms of [network](/networks/) hardening involves sending "DNS" requests to a safe DNS server.

- You *can* easily set up your own DNS server, but it's worth researching to find a good one elsewhere, at least as a backup if yours fails. Otherwise, you won't get on the internet at all!

By running "DoH" (DNS over HTTPS), the computer will look up its DNS through a secure HTTPS network port instead of HTTP.

If you're not using a Bluetooth device (such as a fitness wristband or headset) shut it off. In a public place, Bluetooth devices are relatively easy to hack.

### VPN

To manage information across an unsecured network (such as the internet), some software can arrange to encrypt files before they transfer, thereby creating a "virtual private network" (VPN).

A VPN ("virtual private network") will "tunnel" to another computer by sending encrypted information that the other computer can decrypt, with nobody else able to decode the information if it's intercepted.

*Always* use them on public networks (such as Wi-Fi) and make it a habit to use them for all sensitive activities (like buying things), and it should (as of right now) have at least AES-256 encryption.

There are multiple types of VPN protocol:

- OpenVPN uses specific client software to setup, secure if it's set up correctly, and can be used on any TCP/UDP port.
- WireGuard is newer than OpenVPN, far more secure than OpenVPN, and performs better, though hasn't been adopted as much as OpenVPN because of how much work OpenVPN takes to setup. Unfortunately, some vendors (like Apple) have problems with the app even if the protocol works well.
- IPSec is a suite of network protocols that works natively with many [operating systems](/os/), so it doesn't need third-party apps. It encrypts the entire packet with an [authentication](/authentication/) header (AH) and an encapsulating security protocol (ESP) that seals the information.
  - Cisco and Microsoft partnered in 2005 to create Internet Key Exchange version 2 (IKEv2), which improved in speed, security, stability, CPU use, and re-connectivity compared to other VPNs at the time.
  - A [leaked NSA presentation](https://web.archive.org/web/20141229051901/http://www.spiegel.de/media/media-35529.pdf) implies that L2TP and IKE were compromised, but it's hard to tell for sure.
- PPTP (Point-to-Point Tunneling Protocol) is one of the oldest protocols, but it's outdated and *not* secure.
- SSTP (Secure Socket Tunnneling Protocol) is a Microsoft-specific protocol, but it isn't widely used.
- Apple has talked about an iCloud+ VPN as of 2021, but it's not strictly a VPN because it's more of an Apple onion router using the [Tor](/web-dev/) protocol, where Apple provides a first hop and an unknown provider provides the second.

Generally, VPNs are more secure with UDP, but more reliable with TCP.

### Wi-Fi

Wireless networks are a *huge* vulnerability because they weren't designed to be secure. *Everyone* in range gets all the information, which is often [unencrypted](/encryption/):

- Password-protect your home/work networks (preferably with WPA2-AES, but *don't* use the much older WEP or WPS).
- Always, *always* use a VPN over a public network.
- Try to avoid doing highly important things (like banking) on public networks.

[Hackers](/hacking/) can hit public WiFi networks with a "man-in-the-middle attack" by using the same [SSID](/networks/) as the public network. Pay close attention to which network you're logging into, and never check the box to automatically connect to a public WiFi network.

* * * * *

## Scanning software

The highest-risk [files](/files/) in a computer are core system files, so an [operating system](/os/) has a constant need to track *any* changes to them.

A "firewall" is meant to stop hackers from accessing the computer in the first place. It's a set of rules that it applies to any data packets that pass through it. They are usually "stateful" now and often analyze the [application layer](/networks/) for policy violations. Because of how complicated and interconnected networks have gotten, cybersecurity professionals debate quite a bit about how effective firewalls really are.

A much elaborate system than a firewall is called an IPS or IDS ("intrusion prevention/detection system") depending on how active the software protects you from the problem.

"Antivirus software" scans specific files or file systems to find malicious code. They can also scan emails or web hyperlinks.

Some malware/antivirus scanners are "persistent" (always running) and others have to be activated when you want to use them. Because the more robust effort that persistent scanners like Norton and McAfee have to do to verify *everything* the computer does, they're often a *huge* drain on resources and will cause everything to slow down.

Since AV software is sometimes notoriously difficult to remove (since the software often doesn't trust that you're removing it on purpose), many technicians joke that certain AV software are viruses of its own. In fact, AV software is often unnecessary bloatware that preys on users' fears, and [some of them are mine cryptocurrency at the users' expense](/faang/).

* * * * *

## Memory security

For the sake of protecting information, most of the components of a computer are perfectly fine if they are ever stolen:

- Peripherals without onboard long-term memory (e.g. [mice](/mouse/), [keyboards](/keyboard/), cheaper [printers](/printer/)).
- [CPUs](/cpu/)
- Short-term [memory](/memory/)

However, long-term memory can be *highly* risky. A hard drive possesses all the information a computer has (minus the [BIOS information](/boot/)) as soon as the power gets turned off.

The severity of hard drive security has created a popular convention that memory must be wiped multiple times for the information to be perfectly safe. Popular myths have been 7 passes, or even as many as 35 passes. While this may be true for magnetic drives (like the older platter hard disks or floppy disks), this isn't necessarily true for other drives (like optical disks or electrically-stored memory like USB/SSD).

The best memory security is to have an [encrypted](/encryption/) OS, then simply delete everything once (or more if it's magnetic storage), and make sure the information can't be migrated to another storage (i.e., limit access to files via USB peripherals, external media, and network).

If you're particularly concerned over a hard drive you're throwing out, permanently destroy it by running a power drill through the hardware.

Of course, this protects the drive from *other* people stealing it, but you still have to maintain data integrity and redundancy. This is where you'll need a [RAID configuration](/memory/).

* * * * *

## Virtualization

One of the best ways to protect a computer from the outside is to operate as many programs as possible inside a [virtual environment](/vm/). Some operating systems (like [Qubes](https://www.qubes-os.org/)) are designed *entirely* around this concept.

* * * * *

## Tor

One alternative to maintaining anonymity is to use the [Tor browser](https://www.torproject.org/), which uses Tor (short for The Onion Router). It was originally a fork of Firefox, and is a privacy-focused mode of web browsing. This has a limited scope compared to VPNs, but it operates as a type of parallel to typical web access.

The one difference between accessing a Tor and a VPN is that each of the hops is a new layer of encryption (which is why it's called an onion). With a VPN, the client computer see's the VPN host's IP address, and a Tor exit node operates the same way.

It's important, however, to not access Tor with a regular web browser, due to how slow it drags and what it needs for maintaining privacy:

- Disable JavaScript to avoid any tracking, since JS often gives clues on the browser and connection.
- Video should be disabled, given how utterly slow everything runs on the Tor network.
- All Tor exit IPs are publicly known, so be mindful if you're doing anything that's at all questionable.
- Tor has been compromised, so nothing is fully private on it anymore for someone who wants to find out.

Tor has received negative attention from vague popularized concepts about the "[dark web](/hacking/)". While there *have* been drug deals, counterfeiting, and other illicit activity taking place over Tor, the urban myths have escalated to implying crowd-funded assassinations.

In all reality, there are likely more legitimate services from privacy-concerned individuals on the Onion Network than illegitimate ones.

Tor also serves as a useful tech admin tool, since you have access to multiple random IP addresses.
