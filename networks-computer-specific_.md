
## IP Addresses

Modem IPv4 default (generally):

- 192.168.0.1
- 192.168.1.1
- 192.168.2.1
- 10.0.0.1
- 10.0.0.1

## Ports

Blocked ports:

| Port | Protocol/IP version | Description |
| 0 | TCP, IPv4/6 | Reserved port, not meant to be used, but has been abused |
| 25 | TCP SMTP, IPv4/6 | unsecured, [botnets](computers-cysec-pentest.md) use it for spam, use port 587 instead |
| 67 | UDP BOOTP/DHCP, IPv4 | gets IPv4 info from DHCP server and is vulnerable to attacks |
| 135-139 | TCP/UDP NetBIOS, IPv4/6 | allows file sharing over networks and bad permissions can give full access to a remote client |
| 161 | UDP SNMP, IPv4/6 | vulnerable to [DDoS attacks](computers-cysec-pentest.md) |
| 445 | TCP MS-DS/SMB, IPv4/6 | vulnerable to exploits/attacks/malware (e.g., Sasser/Nimda worms) |
| 520 | UDP RIP, IPv4 | vulnerable to malicious route updates, gives several attack possibilities |
| 547 | UDP DHCPv6, IPv6 | gets IPv6 info from DHCP server and is vulnerable to attacks |
| 1080 | TCP SOCKS, IPv4/6 | vulnerable to many things |
| 1900 | UDP SSDP, IPv4/6 | vulnerable to DoS attacks |

Standard internet ports:

| Service | TCP Port | UDP Port |
| DHCP | 67, 68, 135 |

 |
| DNS | 53, 139 | 53 |
| HTTP / HTTP-SSL | 80 / 443 |

 |
| IIS | 80 |

 |
| LDAP / LDAP-SSL | 389 / 636 |

 |
| NetBIOS | 139 | 138 |
| NTP | 123 |

 |
| RPC | 135, 1500, 2500 |

 |
| SNMP / SNMP Trap | 161 | 161 / 162 |
| Telnet / SSH, SFTP | 23 / 22 |

 |

File-specific ports

| Service | TCP Port | UDP Port |
| CIFS | 445 | 139, 445 |
| FTP / FTP-data / FTP over SSL / FTP over TLS | 21 / 20 |

 |
| File shares session | 139 |

 |
| TFTP | 69 |

 |
| MySQL | 3306 |

 |
| SQL | 53, 137 | 53, 135, 139, 1024-5000 |
| WebDAV, CalDAV / WebDAV(HTTPS), CalDAV (HTTPS) | 5005 / 5006 |

 |

Mail/chat-related ports:

| Service | TCP Port |
| SMTP / SMTP-SSL / SMTP-TLS | 25 / 465 / 587 |
| POP3 / POP3-SSL | 110 / 995 |
| IMAP / IMAP-SSL | 143 / 993 |
| NNTP / NNTP-SSL | 119 / 563 |
| IRC | 531 |
| X.400 | 102 |

Proprietary ports:

| Service | Vendor | TCP Port | UDP Port |
| Bonjour | Apple |

 | 5353 |
| iTunes Server | Apple | 3689 |

 |
| Macintosh File Services (AFP/IP) | Apple | 548 |

 |
| Microsoft Chat | Microsoft | 6665, 6667 |

 |
| Microsoft Message Queue | Microsoft | 135, 1801, 2101, 2103, 2105 | 1801, 3527 |
| Microsoft NetMeeting | Microsoft | 389, 1720, 1731 |

 |

[Authentication](computers-cysec-authentication.md) ports:

| Service | TCP Port | UDP Port |
| Kerberos | 88, 464, 543, 54, 2053 | 88, 464 |
| RADIUS |

 | 1812, 1812, 1645, 1646 |
| VPN - OpenVPN |

 | 1194 |
| VPN --- PPTP | 1723 |

 |
| VPN --- L2TP/IPSec |

 | 500, 1701, 4500 |
