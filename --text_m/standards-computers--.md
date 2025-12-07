
## Email Authentication

Another important technical aspect is email verification and authentication, especially if you are using a custom domain.

How does a provider such as Gmail confirm that the email has legitimately come from your organization and not someone pretending to be you?

There are a couple of security steps you can take to ensure that your emails are delivered while spoofed emails are not.

- Sender Policy Framework (SPF): You can use an SPF setting to validate that the mail server is authorized to send emails from your email domain. SPF is enabled via a `TXT` record in your domain settings. The content of that record will depend on the system you are using to send those emails.
- DomainKeys Identified Mail (DKIM): You can use DKIM to assert that the email message has not been modified in transit from the sending server to the receiving server. DKIM records are set up in your domain settings either as a `TXT` record or a `CNAME` record, depending on your provider. These records will indicate the public encryption/decryption keys.
- Domain Message Authentication, Reporting, and Conformance (DMARC): The final step, after enabling SPF and DKIM, is to set up a DMARC record. The DMARC record tells email providers what to do if an email from your domain fails SPF or DKIM, where to send delivery reports, and how often to apply the DMARC policy. A DMARC record is added as a `TXT` record to your domain settings, as `_dmarc.yourdomain.tld`.

## protocol history

there was a Great Baltimore Fire of 1904
- (check specifics)
- the NYC FD used a differently-sized coupling, meaning their fire trucks were useless
- this motivated the industry to create a set of unified standards

## protocols are messy

[FFmpeg is getting multithreaded transcoding pipelines | Hacker News](https://news.ycombinator.com/item?id=38160703)
[FFmpeg on X: "The most powerful video transcoder in the world is getting better with multithreaded transcoding pipelines. Find out more in the patchset below: https://t.co/oiuy2GJ7wq" / X](https://twitter.com/FFmpeg/status/1721275669336707152)
- protocols are messy and can often need regular updating

## subnetting

I have a system. Really. It takes 15 minutes and a whiteboard. "Double and half"

I have non-networking people subnetting in their head. I taught a few security people to do it and had them show it off to unwitting network engineers. Works on IPv6 too.

I have taught experienced network engineers and they were annoyed that they have been doing it inefficiently for years. I should YouTube it.

Edit. /23 is one bit away from /24. /24 is a block of 256. Double and half. Forget the unusable first/last address.

Double. /23 is a block of 512. Now figure out the ranges.

Half. You need two /24 to make a /23. You have to gather them in two, and you must choose a boundary. 0 2 4 6

Range. Think of the dotted decimal like a car odometer. 192.168.(factor of two). 192.168.0.0/23 is 192.168.0.0 through 192.168.0.255 AND 192.168.1.0 on through to 192.168.1.255

/22 is four /24. Count by fours 192.168.0.0 through 192.168.3.255.

/21 is eights. 8,16,24,32,40,48,56,64. 192.168.32.0 to 192.168.39.255 - that last address is easy to find because it is one less than the start of the next range at 192.168.40.0.

/25 is half. /24 is 256. /25 is 128. Count by 128. 192.168.0.0 to 192.168.0.127 is the first block. The other is 192.168.0.128 to 192.168.0.255

Take that and apply it to any 8 bit range in the mask.

10.0.0.0/7 is double 10/8. You're combining 10/8 and the next block up, which is 11.0.0.0/8. Count by twos. Range is 10.0.0.0 to 11.255.255.255.

10.0.0.0/9 is half of 10/8. 10/8 is 10.0.0.0 to 10.255.255.255. Half? Second octet is 256 so half is 128. Two ranges. 10.0.0.0 to 10.127.255.255 and 10.128.0.0 to 10.255.255.255.

That works when you start at mask values 0 8 16 24 and 32. /32 is a host route. /31 is two up addresses. /30 is four.

0/0 is all addresses. First octet is all 256 values. 0/1 is class A. Half of all ipv4. Half of 256 is 128. 0.0.0.0 through 127.255.255.255.

Now figure out the range for CGN 100.64/10 - 100.64.0.0 through 100.127.255.255. Start at /8 or /16. It works either way. 16 is easier but involves more counting on fingers. What is 100.64/15? /14? Keep going.

## Tor protocol

[Tor](https://www.torproject.org/)
Tor is free software and an open network that helps you defend against traffic analysis.

:::caution - I'm not responsible for the links, domains, it's content or if the provided `.onion` links are really the ones advertised. It's impossible for me as individual person to check every single page every second and monitor it's content.

Also be very carefull of scams. you can find the links to some scam sites on [`torss7t3bxd3qsxn.onion`](http://torss7t3bxd3qsxn.onion/)

note Something to consider [Judge Recommends to Deny Summary Judgment Against Tor Exit Node Operator in Piracy Case](https://torrentfreak.com/judge-recommends-to-deny-summary-judgment-against-tor-exit-node-operator-in-piracy-case-190907/)
TorrentFreak

caution [Bittorrent over Tor isn't a good idea](https://blog.torproject.org/bittorrent-over-tor-isnt-good-idea)
Tor Blog

info - If you suspect your access to the Tor network is being blocked, you may want to use bridges.

You can get latest Tor bridges from [bridges.torproject.org](https://bridges.torproject.org/)

tip - Just replace .onion with .onion.ws or any other domain made available by volounteers [Tor2web](https://www.tor2web.org/) operators.

Example: `http://archivecaslytosk.onion/ => http://archivecaslytosk.onion.ws/`

This connects you with Tor2web, which then talks to the onion service via Tor and relays the response back to you.

WARNING: Tor2web only protects publishers, _not readers_. As a reader installing Tor Browser will give you much greater anonymity than using Tor2web. Using Tor2web trades off security for convenience and usability.

## URLs to try from your LAN

In these examples, 1.2.3.4 represents the [LAN side IP address](https://www.computerworld.com/article/2474776/network-security/find-the-ip-address-of-your-home-router.html) of the router.

In June 2020 we learned that 79 different Netgear devices [shared the same flaw](https://blog.grimm-co.com/2020/06/soho-device-exploitation.html). A bad guy can learn the exact model and firmware of a Netgear router using a URL like
   [https://1.2.3.4/currentsetting.htm](https://1.2.3.4/currentsetting.htm)
and customize an exploit specifically for that router. If you have a Netgear router, try this URL. If it returns information about your router, look for the most recent firmware. Hopefully, it will have been released after June 2020. At the time when the flaw was made public (June 15, 2020) Netgear had done nothing regarding a fix.

In October 2019 we learned of [10 D-Link routers](https://kb.cert.org/vuls/id/766427/) with critical flaws that will not be fixed. If you have any of these D-Link routers, don't bother testing, just get a new router: DIR-655, DIR-866L, DIR-652, DHP-1565, DIR-855L, DAP-1533, DIR-862L, DIR-615, DIR-835 and the DIR-825. For confirmation, CERT has a [Proof of Concept](https://kb.cert.org/artifacts/cve-2019-16920.html) web page that will disconnect a vulnerable D-Link router from the Internet for a minute.

In January 2019 we learned of two [information disclosure bugs](https://badpackets.net/over-9000-cisco-rv320-rv325-routers-vulnerable-to-cve-2019-1653/) in some Cisco routers. More details are on the Bugs page. If the URL below shows details about your Cisco router, that is bad. A public/WAN side version of this is auto-generated on the [Shodan](https://routersecurity.org/shodan.php) page.
   [https://1.2.3.4/cgi-in/config.exp](https://1.2.3.4/cgi-in/config.exp)
   [https://1.2.3.4/cgi-bin/export_debug_msg.exp](https://1.2.3.4/cgi-bin/export%5C%5C_debug%5C%5C_msg.exp)

As per Scott Helme's 2014 [description of his BrightBox router](https://scotthelme.co.uk/ee-brightbox-router-hacked/), try the URL below, where 1.2.3.4 is the IP address of your router. A good result returns nothing but an error message. Here is a [sample](https://scotthelme.co.uk/wp-content/uploads/2014/01/cgi-status-js.png) of a bad result.
   [https://1.2.3.4/cgi/](https://1.2.3.4/cgi/) cgi_status.js

In December 2016, Pedro Ribeiro reported on [flaws in the Netgear WNR2000](https://seclists.org/fulldisclosure/2016/Dec/72) router. If you own a Netgear router, it can't hurt to check for information leakage with the URL below. It may leak the device serial number.
   [https://1.2.3.4/](https://1.2.3.4/) BRS_netgear_success.html

Many Netgear routers had a security flaw in December 2016 (see [here](https://www.computerworld.com/article/3151097/security/updates-and-more-on-the-netgear-router-vulnerability.html)
and [here](https://www.computerworld.com/article/3148680/networking/easily-exploited-netgear-router-flaw-discovered.html) for more). The command below tests a Netgear router. If this results in a web page with the word "Vulnerable", then the [router is vulnerable](https://www.heise.de/security/meldung/Netgear-Luecke-dramatischer-als-angenommen-erste-Sicherheits-Updates-3569299.html). Netgear has issued fixes for all vulnerable routers.
  [https://www.routerlogin.net](https://www.routerlogin.net/) /cgi-bin/;echo$IFS'Vulnerable'

This issue with port 32764 is explained above in the [TCP Ports to Test](https://routersecurity.org/testrouter.php#TCPport32764) section.
   [https://1.2.3.4:32764](https://1.2.3.4:32764/)

In September 2017, security firm Embedi found port 19541 [open on many D-Link routers](https://embedi.com/blog/enlarge-your-botnet-top-d-link-routers-dir8xx-d-link-routers-cruisin-bruisin). It responds to commands such as one to reboot the router. They did not find any way to close the port. The default IP address is 192.168.0.1 but the router may also respond to dlinkrouter.local.
   [https://1.2.3.4:19541](https://1.2.3.4:19541/)

## wireless networks

NOTE: make ref to radio and clarify the bands

also include the bands for walkie talkies and CB
