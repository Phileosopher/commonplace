
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

[Apple AirTags draining battery of devices close by | Hacker News](https://news.ycombinator.com/item?id=30632568)
[Annoying Technology](https://annoying.technology/posts/d9d6d289a06def25/)
- wireless networks are VERY annoying, in almost every domain: [security], reliability, speed, etc.

## 5G

[Telcos are barely done rolling out 5G networks - and they're already talking about '5.5G'](https://www.cnbc.com/2024/03/04/telcos-are-barely-done-rolling-out-5g-networks-and-theyre-already-talking-about-5point5g.html)

## AT protocol

[The AT protocol is the most obtuse crock of shit | Hacker News](https://news.ycombinator.com/item?id=35881170)
[Sam :verified:: "Fucking Christ the @protocol is the most obtuse c…" - Urbanists.Social](https://urbanists.social/@sam/110339902538138997)

## BGP

[Grave flaws in BGP Error handling | Hacker News](https://news.ycombinator.com/item?id=37305800)
[Grave flaws in BGP Error handling](https://blog.benjojo.co.uk/post/bgp-path-attributes-grave-error-handling)

## bluetooth

[Bluetooth remains an 'unusually painful' technology after two decades | Hacker News](https://news.ycombinator.com/item?id=32162131)
[Why Bluetooth remains an 'unusually painful' technology after two decades | CNN Business](https://www.cnn.com/2022/07/10/tech/bluetooth-technology-headache/index.html)

[Android's new Bluetooth stack rewrite (Gabeldorsh) is written with Rust | Hacker News](https://news.ycombinator.com/item?id=26647981)
[gd/rust - platform/system/bt - Git at Google](https://web.archive.org/web/20210331054656/https://android.googlesource.com/platform/system/bt/+/master/gd/rust/)

## cellular architecture

[Slack's migration to a cellular architecture | Hacker News](https://news.ycombinator.com/item?id=37274871)
[Slack's Migration to a Cellular Architecture - Slack Engineering](https://slack.engineering/slacks-migration-to-a-cellular-architecture/)

## dotplan

[.plan | Hacker News](https://news.ycombinator.com/item?id=29248368)
[.plan files | finger @plan.cat](https://plan.cat/)

## email

[A deep dive into email deliverability in 2024 | Hacker News](https://news.ycombinator.com/item?id=39888383)
[A Deep Dive into Email Deliverability in 2024](https://www.xomedia.io/blog/a-deep-dive-into-email-deliverability/)

[Kobold letters: HTML emails are a risk | Hacker News](https://news.ycombinator.com/item?id=39928558)
[Kobold letters - Lutra Security](https://lutrasecurity.com/en/articles/kobold-letters/)

[An Ode to Apple's Hide My Email | Hacker News](https://news.ycombinator.com/item?id=30979563)
[An Ode to Apple's Hide My Email](https://empty.coffee/an-ode-to-apples-hide-my-email/)

[Gmail having issues | Hacker News](https://news.ycombinator.com/item?id=25435916)
[Google Workspace Status Dashboard](https://www.google.com/appsstatus/dashboard/#hl=en&v=issue&sid=1&iid=a8b67908fadee664c68c240ff9f529ab)

[Email a Dumpster Fire | Hacker News](https://news.ycombinator.com/item?id=25201798)
[Email a dumpster fire | H.E.R.L.](https://web.archive.org/web/20201124191949/https://hey.science/dumpster-fire/)

[Hijacking Email with Cloudflare Email Routing | Hacker News](https://news.ycombinator.com/item?id=32331781)
[Hijacking email with Cloudflare Email Routing | Albert Pedersen](https://albertpedersen.com/blog/hijacking-email-with-cloudflare-email-routing/)

[Falsehoods programmers believe about email | Hacker News](https://news.ycombinator.com/item?id=32671959)
[Code: Falsehoods programmers believe about email](https://beesbuzz.biz/code/439-Falsehoods-programmers-believe-about-email)

[JMAP - a modern email open standard | Hacker News](https://news.ycombinator.com/item?id=36127703)
[JSON Meta Application Protocol Specification (JMAP)](https://jmap.io/)

[Email addresses are not good 'permanent' identifiers for accounts | Hacker News](https://news.ycombinator.com/item?id=38823817)
[Chris's Wiki :: blog/tech/EmailAddressesBadPermanentIDs](https://utcc.utoronto.ca/~cks/space/blog/tech/EmailAddressesBadPermanentIDs)

[Gmail and Yahoo's 2024 inbox protections and what they mean for email programs | Hacker News](https://news.ycombinator.com/item?id=38935048)
[Gmail And Yahoo Inbox Requirements & What They Mean For Senders | Mailgun](https://www.mailgun.com/blog/deliverability/gmail-and-yahoo-inbox-updates-2024/)

[GNU Anubis - GNU Project - Free Software Foundation (FSF)🆓](https://www.gnu.org/software/anubis)

[Lavabit](https://lavabit.com/)
Those guys are back and they are now developing their own mail protocol for secure communication.
[lavabit](https://github.com/lavabit/pahoehoe)
is a free and fast VPN service that respects and protects your privacy.

[Autocrypt 1.1.0 documentation](https://autocrypt.org)

[Barracuda urges replacing, not patching, its email security gateways | Hacker News](https://news.ycombinator.com/item?id=36274525)
[Barracuda Urges Replacing - Not Patching - Its Email Security Gateways - Krebs on Security](https://krebsonsecurity.com/2023/06/barracuda-urges-replacing-not-patching-its-email-security-gateways/)

[Trey Harris](http://www.ibiblio.org/harris/500milemail.html)
The case of the 500-mile email

[Stop Microsoft users sending 'reactions' to email by adding a postfix header | Hacker News](https://news.ycombinator.com/item?id=40978073)
[Attempting to stop Microsoft users sending 'reactions' to email from me by adding a postfix header](https://neilzone.co.uk/2024/07/attempting-to-stop-microsoft-users-sending-reactions-to-email-from-me-by-adding-a-postfix-header/)

## email spam

[Google is apparently struggling to contain an ongoing spam attack | Hacker News](https://news.ycombinator.com/item?id=38738619)
[Google Search Overwhelmed By Massive Spam Attack](https://www.searchenginejournal.com/google-search-overwhelmed-by-massive-spam-attack/504527/)

[A Plan for Spam](https://paulgraham.com/spam.html)

[Charlie Stross: "Some thoughts on spam: 1. Rig…" - The Wandering Shop](https://wandering.shop/@cstross/111952879603531914)

[Discord took no action against server that coordinated costly Mastodon spam attacks | TechCrunch](https://techcrunch.com/2024/02/21/discord-took-no-action-against-server-that-coordinated-costly-mastodon-spam-attacks/)

[A little trick to spam the spammers (2021) | Hacker News](https://news.ycombinator.com/item?id=32242581)
[misc.l3m.in/txt/spam.txt](https://misc.l3m.in/txt/spam.txt)

[Spam blacklisting is out of control | Hacker News](https://news.ycombinator.com/item?id=30222736)
[SPAM blacklisting is out of control](https://blog.roastidio.us/posts/spam_blacklists_are_out_of_control/)

[How to stop junk mail | Hacker News](https://news.ycombinator.com/item?id=31625472)
[How To Stop Junk Mail | Consumer Advice](https://consumer.ftc.gov/articles/how-stop-junk-mail)

## email - spf dkim and dmarc

[Learn and Test DMARC | Hacker News](https://news.ycombinator.com/item?id=37729964)
[See how DMARC, SPF, and DKIM work interactively | Hacker News](https://news.ycombinator.com/item?id=29869266)
[Learn and Test DMARC](https://www.learndmarc.com/)

## email validators

[Why don't we do email verification in reverse? | Hacker News](https://news.ycombinator.com/item?id=32537565)
[Why don't we do email verification in reverse?](https://blog.yossarian.net/2022/08/20/Why-dont-we-do-email-verification-in-reverse)

## ethernet

[Ethernet Is Still Going Strong After 50 Years | Hacker News](https://news.ycombinator.com/item?id=38302283)
[Ethernet is Still Going Strong After 50 Years - IEEE Spectrum](https://spectrum.ieee.org/ethernet-ieee-milestone)

[How engineers at Digital Equipment Corp. saved Ethernet | Hacker News](https://news.ycombinator.com/item?id=39968382)
[How Engineers at Digital Equipment Corp. Saved Ethernet - IEEE Spectrum](https://spectrum.ieee.org/how-dec-engineers-saved-ethernet)

[So good, it works on barbed wire (2001) | Hacker News](https://news.ycombinator.com/item?id=40456621)
[So Good, it works on Barbed Wire](https://www.sigcon.com/Pubs/edn/SoGoodBarbedWire.htm)

[Bob Metcalfe wins Turing Award | Hacker News](https://news.ycombinator.com/item?id=35258877)
[A.M. Turing Award](https://amturing.acm.org/?2023)

[Show HN: I made an Ethernet transceiver from logic gates | Hacker News](https://news.ycombinator.com/item?id=34035628)
[Ethernet transceiver | Ivan's blog](https://web.archive.org/web/20221218070132/https://imihajlov.tk/blog/posts/eth-to-spi/)

[Google opens Falcon, a reliable low-latency hardware transport, to the ecosystem | Hacker News](https://news.ycombinator.com/item?id=37922948)
[Introducing Falcon: a reliable low-latency hardware transport | Google Cloud Blog](https://cloud.google.com/blog/topics/systems/introducing-falcon-a-reliable-low-latency-hardware-transport)

## FCC regulation

[FCC votes to limit prison telecom charges | Hacker News](https://news.ycombinator.com/item?id=41005181)
[Worth Rises — FCC VOTES UNANIMOUSLY TO SIGNIFICANTLY LOWER PHONE AND VIDEO COMMUNICATION COSTS AFTER DECADES OF EXPLOITATION BY PRISON TELECOMS](https://worthrises.org/pressreleases/2024/7/18/fcc-votes-unanimously-to-significantly-lower-phone-and-video-communication-costs-after-decades-of-exploitation-by-prison-telecoms)

## fiber optic cabling

[Wiring my home with fiber | Hacker News](https://news.ycombinator.com/item?id=33393540)
[Wiring my home with Fiber - Stefan Schüller](https://sschueller.github.io/posts/wiring-a-home-with-fiber/)

[My upgrade to 25 Gbit/s Fiber To The Home | Hacker News](https://news.ycombinator.com/item?id=31134534)
[My upgrade to 25 Gbit/s Fiber To The Home (2022) - Michael Stapelberg](https://michael.stapelberg.ch/posts/2022-04-23-fiber7-25gbit-upgrade/)

[Utah Locals Are Getting Cheap 10 Gbps Fiber Thanks to Local Governments | Hacker News](https://news.ycombinator.com/item?id=40373931)
[Utah Locals Are Getting Cheap 10 Gbps Fiber Thanks To Local Governments | Techdirt](https://www.techdirt.com/2024/05/15/utah-locals-are-getting-cheap-10-gbps-fiber-thanks-to-local-governments/)

[Cicadas are so loud, fiber optic cables can 'hear' them | Hacker News](https://news.ycombinator.com/item?id=38500065)
[Cicadas Are So Loud, Fiber Optic Cables Can 'Hear' Them | WIRED](https://www.wired.com/story/cicadas-are-so-loud-fiber-optic-cables-can-hear-them/)

[Power over fiber | Hacker News](https://news.ycombinator.com/item?id=38865518)
[F4GRX SÃ©bastien: "Wow. Did you know this? There …" - chaos.social](https://chaos.social/@f4grx/111697027153656114)

## high-speed internet

[The pain of not having high speed @ AskWoody](https://www.askwoody.com/2024/the-pain-of-not-having-high-speed/)

## ICQ

[ICQ will stop working from June 26 | Hacker News](https://news.ycombinator.com/item?id=40467625)
[ICQ](https://icq.com/desktop/en#windows)

## IoT protocols

[Recently I broke off my IoT traffic and I want to share my new network setup. : homelab](https://old.reddit.com/r/homelab/comments/qge280/recently_i_broke_off_my_iot_traffic_and_i_want_to)

## L4S

[Low Latency, Low Loss, and Scalable Throughput (L4S) Internet Service: RFC 9330 | Hacker News](https://news.ycombinator.com/item?id=38597744)
[RFC 9330 - Low Latency, Low Loss, and Scalable Throughput (L4S) Internet Service: Architecture](https://datatracker.ietf.org/doc/rfc9330/)

## language server protocol

[Langserver.org](https://langserver.org/)
is a community-driven site, maintained by Sourcegraph, to track development progress of LSP-compatible language servers and clients.
The Language Server protocol is used between a tool (the client) and a language smartness provider (the server) to integrate features like auto complete, go to definition, find all references and alike into the tool

## LDAP

[Tyler](https://tylersguides.com/articles/backup-restore-openldap/)
(2016) How To Backup and Restore OpenLDAP

## network monitor

[What are the security monitoring can accomplish these scanning and detection? : AskNetsec](https://old.reddit.com/r/AskNetsec/comments/spyttt/what_are_the_security_monitoring_can_accomplish)

[Ask HN: What do you monitor on your servers? | Hacker News](https://news.ycombinator.com/item?id=41240379)

## network proxy - Envoy

[Some Envoy basics](https://jvns.ca/blog/2018/10/27/envoy-basics/)

## network research

[LBNL's Network Research Group](https://ee.lbl.gov/)
home page of the Network Research Group (NRG).

## Nostr protocol

[Nostr, a simple protocol for decentralizing social media that has a chance of working](https://nostr.com)
[GitHub - nostr-protocol/nostr: a truly censorship-resistant alternative to Twitter that has a chance of working](https://github.com/nostr-protocol/nostr)

## port scanning

[Why Is This Website Port Scanning Me? | Hacker News](https://news.ycombinator.com/item?id=23246170)
[Why is This Website Port Scanning me](https://nullsweep.com/why-is-this-website-port-scanning-me/)

[GitHub - RustScan/RustScan: The Modern Port Scanner](https://github.com/RustScan/RustScan)
find all open ports faster than Nmap.

[adminsub.net](https://www.adminsub.net/tcp-udp-port-finder)

## RS-232

[The RS-232 protocol [video] | Hacker News](https://news.ycombinator.com/item?id=33482166)
[The RS-232 protocol - YouTube](https://www.youtube.com/watch?v=AHYNxpqKqwo)

## rss

[We don't have official RSS feed support for now, but we're working on a solution | Hacker News](https://news.ycombinator.com/item?id=38598983)
[Feeds  |  Chrome for Developers](https://developer.chrome.com/feeds)

[Use RSS for privacy and efficiency (2021) | Hacker News](https://news.ycombinator.com/item?id=33469271)
[Use RSS for privacy and efficiency :: rsapkf.org](https://rsapkf.org/weblog/rss)

[This is the year of the RSS reader? | Hacker News](https://news.ycombinator.com/item?id=34105572)
[This is the year of the RSS reader. (Really!) - Nieman Journalism Lab](https://www.niemanlab.org/2022/12/this-is-the-year-of-the-rss-reader-really/)

[Style your RSS feed | Hacker News](https://news.ycombinator.com/item?id=36401854)
[Style your RSS feed](https://darekkay.com/blog/rss-styling/)

[I Miss RSS | Hacker News](https://news.ycombinator.com/item?id=29814921)
[I Miss RSS - Billy Wilcosky](https://wilcosky.com/2022/09/18/i-miss-rss/)

[RSS is wonderful | Hacker News](https://news.ycombinator.com/item?id=28967540)
[RSS is Wonderful · Quakkels.com](https://quakkels.com/posts/rss-is-wonderful/)

[I Still Use RSS | Hacker News](https://news.ycombinator.com/item?id=26014344)
[Why I Still Use RSS](https://atthis.link/blog/2021/rss.html)

[An example of why RSS is useful and important | Hacker News](https://news.ycombinator.com/item?id=30387879)
[An example of why RSS is useful and important - Chris Hardie's Tech and Software Blog](https://tech.chrishardie.com/2022/rss-useful-important/)

[The reallysimple project](http://reallysimple.org)

## standard setters

[IEEE Xplore Digital Library](https://ieeexplore.ieee.org/Xplore/home.jsp)

[I may be the only evil (bit) user on the internet (2015) | Hacker News](https://news.ycombinator.com/item?id=36330116)
[I may be the only evil (bit) user on the internet](https://blog.benjojo.co.uk/post/evil-bit-RFC3514-real-world-usage)

[Mike Crittenden](https://critter.blog/2021/04/23/you-have-to-standardize-before-you-can-standardize/)
(2021) You have to standardize before you can standardize

## TCP

[Cloning a Laptop over NVMe TCP | Hacker News](https://news.ycombinator.com/item?id=39676767)
[Cloning a laptop over NVME TCP](https://copyninja.in/blog/clone_laptop_nvmet.html)

## telephone

[Anonymous public voicemail inbox | Hacker News](https://news.ycombinator.com/item?id=39910119)
[After the Beep](https://afterthebeep.tel/)

## UDP

[How much secure is my UDP based network protocol? : crypto](https://old.reddit.com/r/crypto/comments/12yg97k/how_much_secure_is_my_udp_based_network_protocol/)

## UnifiedPush

[UnifiedPush: A decentralized, open-source push notification protocol | Hacker News](https://news.ycombinator.com/item?id=34094497)
[UnifiedPush: a decentralized, open-source push notification protocol | F-Droid - Free and Open Source Android App Repository](https://f-droid.org/2022/12/18/unifiedpush.html)

## Willow protocol

[Willow Protocol | Hacker News](https://news.ycombinator.com/item?id=39026791)
[Willow Specifications - Willow](https://willowprotocol.org/)

## wireless protocols

[Apache Mynewt](https://mynewt.apache.org)

[The Wi-Fi only works when it's raining | Hacker News](https://news.ycombinator.com/item?id=39896371)
[The Wi-Fi only works when it's raining](https://predr.ag/blog/wifi-only-works-when-its-raining/)

[Alexa, what is my wifi password? | Hacker News](https://news.ycombinator.com/item?id=35399590)
[Dragon863 - "Alexa, what is my wifi password?"](https://dragon863.github.io/blog/alexa.html)

[416: Zealous Autoconfig - explain xkcd](https://www.explainxkcd.com/wiki/index.php/416:_Zealous_Autoconfig)

[UniFi Express | Hacker News](https://news.ycombinator.com/item?id=38504027)
[UniFi Express - Ubiquiti](https://ui.com/cloud-gateways/wifi-integrated/express)

## YAML

[Why are we templating YAML? (2019) | Hacker News](https://news.ycombinator.com/item?id=39101828)
[Why the fuck are we templating yaml? | lbr.](https://leebriggs.co.uk/blog/2019/02/07/why-are-we-templating-yaml)

[YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- note: somehow connects w/ IRC

[YAML (YAML Ain't Markup Language)](http://yaml.org/)
[GitHub - yaml/yaml: YAML language and community information](https://github.com/yaml/yaml)

[The Yaml document from hell | Hacker News](https://news.ycombinator.com/item?id=34351503)
[The yaml document from hell](https://ruudvanasseldonk.com/2023/01/11/the-yaml-document-from-hell)

[That's a Lot of YAML | Hacker News](https://news.ycombinator.com/item?id=37687060)
[🚨🚨 That's a lot of YAML 🚨🚨](https://noyaml.com/)

[I accidentally used YAML.parse instead of JSON.parse and it worked | Hacker News](https://news.ycombinator.com/item?id=30052128)
[Paul Kuruvilla - I accidentally used YAML.parse instead of JSON.parse, and it... worked?](https://rohitpaulk.com/articles/accidentally-used-yaml-instead-of-json)

[GitHub - nasbench/SIGMA-Resources: Resources To Learn And Understand SIGMA Rules](https://github.com/nasbench/SIGMA-Resources)

## ARP

[Gratuitous ARP - Definition and Use Cases - Practical Networking .net](https://www.practicalnetworking.net/series/arp/gratuitous-arp)

## DHCP

[ISC's Knowledgebase](https://kb.isc.org/docs/using-this-knowledgebase)
you'll find some general information about BIND 9, ISC DHCP, and Kea DHCP.
[Index of /](https://ftp.isc.org/)

[dhcpcanon - DHCP anonymity profile — dhcpcanon 0.8.5 documentation](https://dhcpcanon.readthedocs.io/en/latest/)

## email

[How to Add Email Avatar for Different Mailbox Providers | Blog Selzy](https://selzy.com/en/blog/email-avatar)

[How to prevent email spoofing, using an unholy combination of silly standards | Hacker News](https://news.ycombinator.com/item?id=28192269)
[I figured out how DMARC works, and it almost broke me | Simon Andrews](https://simonandrews.ca/articles/how-to-set-up-spf-dkim-dmarc)

[email - What is the difference between ports 465 and 587? - Stack Overflow](https://stackoverflow.com/questions/15796530/what-is-the-difference-between-ports-465-and-587)

[GitHub - izmaelmag/awesome-emails: List of tools, articles and videos about email design and development](https://github.com/izmaelmag/awesome-emails)

[GitHub - jonathandion/awesome-emails: An awesome list of resources to build better emails.](https://github.com/jonathandion/awesome-emails)

[Use plaintext email](https://useplaintext.email/)
How-To Use plaintext Email

[Coding Archives | Campaign Monitor](https://www.campaignmonitor.com/resources/browse/topic/coding/)

## email - spf dkim and dmarc

[Understanding SPF, DKIM, and DMARC: A Simple Guide | Hacker News](https://news.ycombinator.com/item?id=40708476)
[nicanorflavier/spf-dkim-dmarc-simplified: Email security is a key part of internet communication. But what are SPF, DKIM, and DMARC, and how do they work? This guide will explain it all in simple terms to make these concepts clearer.](https://github.com/nicanorflavier/spf-dkim-dmarc-simplified)

## ethernet

[How 1500 bytes became the MTU of the internet](https://blog.benjojo.co.uk/post/why-is-ethernet-mtu-1500)
great story about the Maximum Transmission Unit.

## network analysis

[GitHub - briatte/awesome-network-analysis: A curated list of awesome network analysis resources.](https://github.com/briatte/awesome-network-analysis)

## network monitoring

[Daniel Miessler](https://danielmiessler.com/blog/security-how-to-monitor-your-network-connections/)
Security: How To Monitor Your Network Connections

[Julia Evans](https://jvns.ca/blog/2017/07/05/linux-tracing-systems/)
(2017) Linux tracing systems & how they fit together

## ping

[How does Linux NAT a ping? | Hacker News](https://news.ycombinator.com/item?id=37455621)
[how does linux nat a ping?](https://devnonsense.com/posts/how-does-linux-nat-a-ping/)

## port forwarding

[How To Set Up Port Forwarding - Port Forward](https://screenshots.portforward.com/)

## port listening

[What does it mean to listen on a port? | Hacker News](https://news.ycombinator.com/item?id=30323865)
[Paul Butler - What does it mean to listen on a port?](https://paulbutler.org/2022/what-does-it-mean-to-listen-on-a-port/)

## remote access - VNC

[Virtual Network Computing - Wikipedia](https://en.wikipedia.org/wiki/Virtual_Network_Computing)

## rss

[How to Create an RSS Feed for Your Site From Scratch](https://www.makeuseof.com/tag/how-to-create-an-rss-feed-for-your-site-from-scratch)

[XML RSS](https://www.w3schools.com/xml/xml_rss.asp)

[RSS tutorial: building and using a feed, step by step.](https://www.xul.fr/en-xml-rss.html)

[How to generate an RSS feed for your blog](https://www.contentful.com/blog/2021/03/05/generate-blog-rss-feed-with-javascript-and-netlify/)

[How to Set up an RSS Feed in 2022: Food for Thought](https://www.cloudwards.net/how-to-set-up-an-rss-feed/#setting-up-an-rss-feed)

## signal processing

[Signal Processing and Systems in Programming - Guide for Beginners](https://www.freecodecamp.org/news/signal-processing-and-systems-in-programming/)

## sms

[Messages in iCloud: How to Extract Full Content Including Media Files, Locations and Documents | ElcomSoft blog](https://blog.elcomsoft.com/2018/11/messages-in-icloud-how-to-extract-full-content-including-media-files-locations-and-documents)

## telephone protocols

[Why did old phone numbers start with letters? (2015) | Hacker News](https://news.ycombinator.com/item?id=37342925)
[Why Did Old Phone Numbers Start With Letters?](https://www.mentalfloss.com/article/61116/why-did-old-phone-numbers-start-letters)

## YAML

[Animosity](https://github.com/Animosity/CraftIRC/wiki/Complete-idiot%27s-introduction-to-yaml)
Complete idiot's introduction to yaml
