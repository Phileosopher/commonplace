
# How network hardening works

For the most part, network hardening revolves around removing features and adding layers of obfuscation.

- The removed features generally remove attack vectors.
- The obfuscation is to enhance privacy through anonymity.

## Signed certificates

There are some "certificate authorities", which are organizations that issue signed certificates to known-good websites.

- These websites will have a "lock" symbol in the top left next to the URL.

Be careful navigating anything unsigned (which will be [HTTP instead of HTTPS](standards-computers.md)).

- While *consuming* information is fine from those websites, your best assumption is that everything *entered* on that website is effectively public knowledge.

## Blocking transfer

Most computer security policies manage specific portions of what the computer interacts with:

- Blocking specific ports that will likely send particular unwanted [protocols](standards-computers.md).
- Blocking [networks](computers-networks.md) that may be insecure.
- Blocking certain forms of code that may run on system files or read user-made documents.

Disable *any* unused ports:

- IP ports
- Physical ports like USB, Ethernet, cameras, microphones, etc. (including the built-in ones)
- Wireless ports
- Any hardware or peripherals you don't use

Many internet [protocols](standards-computers.md) are unsecure (e.g., Telnet), so disabling them cuts down the risk of "network sniffing".

Disable all internet router features that won't be used:

- IPv6
- Remote Web Administration
- Bluetooth
- Wi-Fi
- Universal Plug n Play (UPnP) has been compromised for a while.
- WPS (Wi-Fi Protected Setup) involves joining a wireless network by pressing a button on the router and entering an 8-digit pit, but hackers were able to [brute force](mind-creativity-hacking.md) that PIN as of 2011.
- Turn gateway devices to Bridge mode unless they're the means of connecting to the internet.

## End-to-end encryption (E2E)

One of the most important aspects of keeping a network safe is to have "end-to-end [encryption](encryption.md)" (E2E). This doesn't simply mean the network transfers information securely or that it stores it securely, but that *every* step of the transaction is securely handling the information. This requires awareness of each stage of the network transfer and computer's use of the information, and what keeps data safe.

## Domain name servers (DNS)

One of the easiest forms of [network](computers-networks.md) hardening involves sending "DNS" requests to a safe [DNS server](computers-browser-domains.md).

- You *can* easily set up your own DNS server, but it's worth researching to find a good one elsewhere, at least as a backup if yours fails. Otherwise, you won't get on the internet at all!

By running "DoH" (DNS over HTTPS), the computer will look up its DNS through a secure HTTPS network port instead of HTTP.

If you're not using a Bluetooth device (such as a fitness wristband or headset) shut it off. In a public place, Bluetooth devices are relatively easy to hack.

## Proxy servers and virtual private networks (VPN)

To manage information across an unsecured network (such as the internet), some software can arrange to encrypt files before they transfer, thereby creating a "virtual private network" (VPN).

A VPN ("virtual private network") will "tunnel" to another computer by sending encrypted information that the other computer can decrypt, with nobody else able to decode the information if it's intercepted.

It's worth noting that an SSH tunnel with a proxy is a de facto VPN connection.

*Always* use them on public networks (such as Wi-Fi) and make it a habit to use them for all sensitive activities (like buying things), and it should (as of right now) have at least AES-256 encryption.

There are multiple types of VPN protocol:

- OpenVPN uses specific client software to set up, secure if it's set up correctly, and can be used on any TCP/UDP port.
- WireGuard is newer than OpenVPN, far more secure than OpenVPN, and performs better, though hasn't been adopted as much as OpenVPN because of how much work OpenVPN takes to set up. Unfortunately, some vendors (like Apple) have problems with the app even if the protocol works well.
- IPSec is a suite of network protocols that works natively with many [operating systems](computers-os.md), so it doesn't need third-party apps. It encrypts the entire packet with an [authentication](computers-infosec-authentication.md) header (AH) and an encapsulating security protocol (ESP) that seals the information.
  - Cisco and Microsoft partnered in 2005 to create Internet Key Exchange version 2 (IKEv2), which improved in speed, security, stability, CPU use, and re-connectivity compared to other VPNs at the time.
  - A [leaked NSA presentation](https://web.archive.org/web/20141229051901/http://www.spiegel.de/media/media-35529.pdf) implies that L2TP and IKE were compromised, but it's hard to tell for sure.
- PPTP (Point-to-Point Tunneling Protocol) is one of the oldest protocols, but it's outdated and *not* secure.
- SSTP (Secure Socket Tunneling Protocol) is a Microsoft-specific protocol, but it isn't widely used.
- Apple has talked about an iCloud+ VPN as of 2021, but it's not strictly a VPN because it's more of an Apple onion router using the [Tor](computers-sofware-webdev.md) protocol, where Apple provides a first hop and an unknown provider provides the second.

Generally, VPNs are more secure with UDP, but more reliable with TCP.

## Wi-Fi

Wireless networks are a *huge* vulnerability because they weren't designed to be secure. All wireless routers are effectively hubs: *everyone* in range gets all the information, which is often [unencrypted](encryption.md).

- Password-protect your home/work networks (preferably with WPA2-AES [encryption](encryption.md), but do *not* use the much older WEP or WPS).
- Always, *always* use a VPN over a public network.
- Try to avoid doing highly important things (like banking) on public networks.

[Hackers](mind-creativity-hacking.md) can hit public Wi-Fi networks with a "man-in-the-middle attack" by using the same [SSID](computers-networks.md) as the public network. Pay close attention to which network you're logging into, and never check the box to automatically connect to a public Wi-Fi network.
