
# Specific networking trivia

## IP Addresses

Modem IPv4 default (generally):

- 192.168.0.1
- 192.168.1.1
- 192.168.2.1
- 10.0.0.1
- 10.0.0.1

## Ports

### Blocked ports

0

- Protocol: TCP, IPv4/6
- Reserved port, not meant to be used, but has been abused

25

- Protocol: TCP SMTP, IPv4/6
- unsecured, [botnets](computers-cysec-pentest.md) use it for spam, use port 587 instead

67

- Protocol: UDP BOOTP/DHCP, IPv4
- gets IPv4 info from DHCP server and is vulnerable to attacks

135-139

- Protocol: TCP/UDP NetBIOS, IPv4/6
- allows file sharing over networks and bad permissions can give full access to a remote client

161

- Protocol: UDP SNMP, IPv4/6
- vulnerable to [DDoS attacks](computers-cysec-pentest.md)

445

- Protocol: TCP MS-DS/SMB, IPv4/6
- vulnerable to exploits/attacks/malware (e.g., Sasser/Nimda worms)

520

- Protocol: UDP RIP, IPv4
- vulnerable to malicious route updates, gives several attack possibilities

547

- Protocol: UDP DHCPv6, IPv6
- gets IPv6 info from DHCP server and is vulnerable to attacks

1080

- Protocol: TCP SOCKS, IPv4/6
- vulnerable to many things

1900

- Protocol: UDP SSDP, IPv4/6
- vulnerable to DoS attacks

### Standard internet service ports

DHCP

- TCP ports 67, 68, 135

DNS

- TCP ports 53, 139
- UDP port 53

HTTP / HTTP-SSL

- TCP ports 80 / 443

IIS

- TCP port 80

LDAP / LDAP-SSL

- TCP ports 389 / 636

NetBIOS

- TCP port 139
- UDP port 138

NTP

- TCP port 123

RPC

- TCP ports 135, 1500, 2500

SNMP / SNMP Trap

- TCP port 161
- UDP ports 161 / 162

Telnet / SSH, SFTP

- TCP ports 23 / 22

### File-specific ports

CIFS

- TCP port 445
- UDP ports 139, 445

FTP / FTP-data / FTP over SSL / FTP over TLS

- TCP ports 21 / 20

File shares session

- TCP port 139

TFTP

- TCP port 69

MySQL

- TCP port 3306

SQL

- TCP ports 53, 137
- UDP ports 53, 135, 139, 1024-5000

WebDAV, CalDAV / WebDAV(HTTPS), CalDAV (HTTPS)

- TCP ports 5005 / 5006

### Mail/chat-related ports

SMTP / SMTP-SSL / SMTP-TLS

- TCP ports 25 / 465 / 587

POP3 / POP3-SSL

- TCP ports 110 / 995

IMAP / IMAP-SSL

- TCP ports 143 / 993

NNTP / NNTP-SSL

- TCP ports 119 / 563

IRC

- TCP port 531

X.400

- TCP port 102

### Proprietary ports

| Service | Vendor | TCP Port | UDP Port |

Apple's Bonjour

- TCP port 5353

Apple's iTunes Server

- TCP port 3689

Apple's Macintosh File Services (AFP/IP)

- TCP port 548

Microsoft's MS Chat

- TCP ports 6665, 6667

Microsoft Message Queue

- TCP ports 135, 1801, 2101, 2103, 2105
- UDP ports 1801, 3527

Microsoft NetMeeting

- TCP ports 389, 1720, 1731

### [Authentication](computers-cysec-authentication.md) ports

Kerberos

- TCP ports 88, 464, 543, 54, 2053
- UDP ports 88, 464

RADIUS

- TCP ports 1812, 1812, 1645, 1646

VPN: OpenVPN

- TCP port 1194

VPN: PPTP

- TCP port 1723

VPN: L2TP/IPSec

- UDP ports 500, 1701, 4500

## Email-to-SMS

Step 1 - reverse lookup the carrier (e.g., [NumLookup](https://www.numlookup.com/))

Step 2 - email the carrier's SMS/MMS server (10-digit #, no dashes, no subject)

MNOs (mobile network operators, relatively straightforward)

- AT&T SMS - @txt.att.net
- AT&T MMS - [num]@mms.att.net
- Google Project Fi SMS/MMS - [num]@msg.fi.google.com
- Spectrum - [num]@mypixmessages.com
- Sprint SMS - [num]@messaging.sprintpcs.com
- Sprint MMS - [num]@pm.sprint.com
- T-Mobile SMS/MMS - [num]@tmomail.net
- U.S. Cellular SMS - [num]@email.uscc.net
- U.S. Cellular MMS - [num]@mms.uscc.net
- Verizon SMS - [num]@vtext.com
- Verizon MMS - [num]@vzwpix.com

MVNOs (mobile variable network operators, may need an MNO's geographically dependent gateway address)

- Boost Mobile SMS - [num]@sms.myboostmobile.com
- Boost Mobile MMS - [num]@myboostmobile.com
- Cricket Wireless SMS/MMS - [num]@mms.cricketwireless.net
- Republic Wireless SMS - [num]@text.republicwireless.com
- Straight Talk SMS - [num]@vtext.com
- Straight Talk MMS - [num]@mypixmessages.com
- Ting SMS - [num]@message.ting.com
- Tracfone SMS - [depends on underlying carrier]
- Tracfone MMS - [num]@mmst5.tracfone.com
- Virgin Mobile SMS - [num]@vmobl.com
- Virgin Mobile MMS - [num]@vmpix.com

A few things to note:

- SMS might glitch out or redirect to MMS server if you don't limit it to 160 chars.
- Some MNOs become MVNOs if the phone is geographically located elsewhere, so this isn't a foolproof system.
