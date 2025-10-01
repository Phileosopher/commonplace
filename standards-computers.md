
# How computer standards are set

Beyond the typical need for [standards](standards.md) represented in most large industries, computers, computers are too dumb to recognize slight variants on a data transfer.

Engineers representing all the largest organizations, therefore, must constantly meet to make *highly* precise agreed-upon standards to accommodate the stupidity of computers.

This isn't to say that slang and dialects don't adapt in the human development of new technologies. In fact, it's frequently the case that figuring out *why* most standards are named what they are quickly becomes a deep dive into a technical history lesson.

## Standard-setters

Here are some of the more notable organizations that set computer-related standards (as of 2021), with some of their more notable contributions.

General:

- [ANSI](https://www.ansi.org/) (American National Standards Institute)
- [AIIM](https://www.aiim.org/) (Association for Information and Image Management)
- [ASAM](https://www.asam.net/) (Association for Standardisation of Automation and Measuring Systems)
- [ISO](https://www.iso.org/home.html) (international Organization of Standards)
  - [List of ISO's publicly available standards](https://standards.iso.org/ittf/PubliclyAvailableStandards/)
- [IEC](https://www.iec.ch/homepage) (International Electrotechnical Commission)
- [IEEE](https://www.ieee.org/) (Institute of Electrical and Electronics Engineers)
  - [IEEE SA](https://standards.ieee.org/) (IEEE Standards Association)
  - [IEEE 802.11](https://ieee802.org/11/) - WLAN standards (i.e., WiFi)
- [OMG](https://www.omg.org/) (Object Management Group)
- [OSGi Alliance](https://www.osgi.org/) (Open Services Gateway) - Java-specific

Computer manufacturing:

- [Accellera](https://www.accellera.org/)
- [Ecma International](https://www.ecma-international.org/) (European Computer Manufacturers Association)
- [NEMA](https://www.nema.org/) (National Electrical Manufacturers Association)

Open-source:

- [The Open Group](https://www.opengroup.org/)

Internet/networks:

- [ARIB](https://www.arib.or.jp/english/) (Association of Radio Industries and Businesses) - Japan-specific
- [ATIS](https://www.atis.org/) (Alliance for Telecommunications Industry Solutions) - USA-specific
- [CCSA](https://www.ccsa.org.cn/english/) (China Communications Standards Association) - China-specific
- [ETSI](https://www.etsi.org/) (European Telecommunications Standards Institute) - Europe-specific
- [IETF](https://www.ietf.org/) (Internet Engineering Task Force)
  - [RFC 3339 - Date and Time on the Internet: Timestamps](https://tools.ietf.org/html/rfc3339)
- [ITU](https://www.itu.int/en/Pages/default.aspx) (International Telecommunications Union)
- [OCF](https://openconnectivity.org/) (Open Connectivity Foundation) - specifically for IoT
- [OIF](https://www.oiforum.com/) (Optical Internetworking Forum)
- [TIA](https://tiaonline.org/) (Telecommunications Industry Association)
- [TM Forum](https://www.tmforum.org/)
- [TSDSI](https://tsdsi.in/) (Telecommunications Standards Development Society, India) - India-specific
- [TTC](https://www.ttc.or.jp/) (Telecommunication Technology Committee) - Japan-specific

Wireless/radio:

- CISPR (International Special Committee on Radio Interference) - part of the IEC
- [OMA](https://omaspecworks.org/) (Open Mobile Alliance)

Internet - web content:

- [DCMI](https://dublincore.org/) (Dublin Core Metadata Initiative)
- [IPTC](https://iptc.org/) (International Press Telecommunications Council)
- [OASIS](https://www.oasis-open.org/) (Organization for the Advancement of Structured Information Standards)
- [W3C](https://www.w3.org/) (World Wide Web Consortium)
- [XMPP Standards Foundation](https://xmpp.org/)

Internet - media content:

- [DDEX](https://ddex.net/) (Digital Data Exchange) - for music
- [SMPTE](https://www.smpte.org/) (Society of Motion Picture and Television Engineers)

Internet - cybersecurity:

- [Liberty Alliance Project](http://www.projectliberty.org/)

Storage:

- [CFA](https://www.compactflash.org/) (CompactFlash Association)
- [SDA](https://www.sdcard.org/) (SD Association)
- [SNIA](https://www.snia.org/) (Storage Networking Industry Association)

Screen/printer:

- [CIE](https://cie.co.at/) (International Commission on Illumination)

Audio:

- [AES](https://www.aes.org/) (Audio Engineering Society)

GPS/satellites:

- [CCSDS](https://public.ccsds.org/) (Consultative Committee for Space Data Systems)
- [OGC](https://www.ogc.org/) (Open Geospatial Consortium)

Distributed systems and large-scale technology:

- [DMTF](https://www.dmtf.org/) (Distributed Management Task Force)
- [OGF](https://www.ogf.org/) (Open Grid Forum)

Other:

- [GS1](https://www.gs1.org/) - standardized the barcode

## Protocols/standards

[Many networking standards](https://en.wikipedia.org/wiki/Lists_of_network_protocols) are thoroughly fixed as protocols. Many of them operate specifically on a port number, but some don't use specific ports.

Very often, the [spirit of freedom](legal-ip-floss.md) comes through protocols. Platforms are proprietary, but protocols allow a broader interoperability between various computers, programs, and tasks.

Cabling:

- USB - Universal Serial Bus, a standard swappable cable for most computers designed to be as near-universal as possible:
  - USB Type A - the most frequently seen form factor, rectangular port that only inserts one way
    - First standardized in 1990's
    - Supports USB 1.1, USB 2, and USB 3.x
  - USB 3.0 - a direct update to USB Type A and therefore typically backwards compatible, indicated by blue on the connector
  - USB Type B - rectangular form factor with tapered ends on one side, less frequently used (e.g., [printers](engineering-printers.md), [scanners](computers-ocr.md)) and typically is Type A on the cable's other side
  - USB Mini - small form factor typically for smaller devices (e.g., [cameras](engineering-camera.md), [scanners](computers-ocr.md)), largely deprecated for USB Micro
  - USB Micro - the smallest form factor typically used for lower-power technology (e.g., cellphones), largely depreciated for USB Type C
  - USB Type C - symmetrical, comparatively newer form factor
  - USB Micro B - one male plug with two separate odd-shaped female connectors, typically for steady data transfer
- Category 5 - more specifically, Cat5e is the most standard cabling for networked computers, but can go as low as Cat3 or up to and beyond Cat7
- SFP - Small Form factor Pluggable, a standard for [large-scale servers](computers-distsys-enterprise.md)

Network identification:

- ARP and RARP - address resolution protocol and (reverse) for IPv4, find out the MAC address from an IP address and vice versa, can be proxy (as a response) or gratuitous (as an unsolicited response)
- NDP - neighbor discovery protocol, ARP for IPv6
- CIDR - classless inter-domain routing, a system of demarcating classes of IPv4 addresses
- DHCP - dynamic hosting control protocol, assigns IP addresses automatically, a *huge* part of maintaining networks
  - APIPA - automatic private IP addressing, the fallback for when DHCP fails on IPv4
  - SLAAC - stateless address auto configuration, an alternative for DHCP on IPv6
- DNS - domain name system, access a server that links a URL with an IP address
- IP - internet protocol, find an IP address of a computer

Network routing and status:

- Ethernet - the only surviving LAN ("Local Area Network") protocol, designed in the mid-1970's
- RIP - routing information protocol, counts the number of "hops" to determine the shortest network path
- SNMP - simple network management protocol, keep track of relevant network information
- ICMP - internet control message protocol, to send error messages about a specific IP address

File and information transfer:

- FTP and FTPS - file transfer protocol (and secured version), send files
- HTTP - hyper-text transfer protocol, send hyper-text across the internet
  - WebDAV - web distributed authoring and versioning, an extension to HTTP that allows the content to be both read *and* written (e.g., typing content into a web form)
- L2TP - Layer 2 tunneling protocol, a core component of VPNs

Streaming file and information transfer:

- IGMP - internet group management protocol, to multicast to specific IP addresses
- RPC - remote procedure call, remotely request another computer to run a service
- TCP - transmission control protocol, safely send data across the internet
- UDP - user datagram protocol, quickly send data across the internet (it doesn't check it afterward)

Message transfer protocols:

- SMS - short message service, which is completely unencrypted and maxes out at 160 characters
- MMS - multimedia message service, which allows a photo/video and 1,000 characters
- Signal - an unencrypted, highly secure protocol
- RSS - really simple syndication, a straightforward time-based feed of content that permits built-in media and hyperlinks
- IRC - internet relay chat, a real-time text-based chat system
  - DCC - direct client-to-client, a sub-protocol for file transfer via IRC
  - XDCC - eXtended DCC or Xabi DCC, an expanded version of DCC for large files

Email-specific protocols:

- POP3 - post office protocol v3, receive emails and delete the original
- IMAP - internet message access protocol, receive and synchronize copies of emails
- SMTP - simple mail transfer protocol, send emails

[Console/terminal](computers-cli.md) data protocols:

- Telnet - remotely access an unencrypted command-line interface

[Mobile](engineering-radio.md) carrier protocols:

- GSM - global system for mobile communications, a European standard on the 900-1800 MHz band that the whole world uses (though the US uses the 1900 MHz band which makes its phones incompatible without dual-band hardware).
- CDMA - code division multiple access, high-quality [proprietary](legal-ip-floss.md) WWII-era protocol that gives full-band data to multiple connections at once by splitting the code into small pieces
- WLL - wireless in local loop, a LAN protocol
- GPRS - general packet radio services, the standard for 2G and 3G data services

Some protocols are [encryption-specific](encryption.md):

- TLS - transport layer security, which has succeeded secure socket layer (SSL), and tends to use other encryption primitives like AES
- PGP - pretty good privacy, encrypts and authenticates mail messages
- SSH - secure shell, remotely access an encrypted command-line interface (i.e., Telnet but encrypted)
- HTTPS - hyper-text transfer protocol secured, send hyper-text across the internet (i.e., HTTP with SSL/TLS)
- WEP - wireless encrypted protocol, a compromised network standard for wireless signals, has been compromised
- WPA/WPA2/WPA3 - Wi-Fi protected access, the network standard for wireless signals
- Some protocols verify email [domains](computers-sofware-webdev.md) for validity, such as DMARC (Domain-based Message Authentication, Reporting and Conformance)

Synchronizing a network across time zones, while also accounting for (relatively) severe latency, daylight savings time, differences in altitude (since time travels slower when moving faster due to Einstein's relativity), and differences between conventions makes [timezones insanely difficult to keep track of](https://gist.github.com/timvisee/fcda9bbdff88d45cc9061606b4b923ca). It uses the Network Time Protocol (NTP) just to keep track, and it has *two* different standards: [IETF's RFC 3339](https://tools.ietf.org/html/rfc3339) and [ISO's 8601](https://www.iso.org/iso-8601-date-and-time-format.html). They have overlap, [but not entirely](https://ijmacd.github.io/rfc3339-iso8601/).

It's worth noting most of the above protocols have very specific network "ports" they work through.

Most computer design specifications must abide by certain compliance standards to work correctly. While it's often possible to [hack](hacking.md) them, those standards are often there for a safety reason.

There are many standards about how to setup cabling arrangements as well:

- Horizontal cabling and cabling runs which travel long-distance.
- Structured cabling for nearby systems, like twisted-pair and optical cabling.
- Arrangements for wireless technologies' power output, which considers their range and materials that the signals are passing through.

## Additional reading

[Fun with IP address parsing](https://blog.dave.tf/post/ip-addr-parsing/)

[All About USB-C: Illegal Adapters](https://hackaday.com/2022/12/27/all-about-usb-c-illegal-adapters/)

[Email explained from first principles](https://explained-from-first-principles.com/email/)
