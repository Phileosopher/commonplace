
## Protection

MAKE SURE TO CONSIDER [INSURANCE]

it's worth noting the security/efficiency tradeoff

- a cysec policy that's too constricting will prevent people from ever getting work done (e.g., can't even view a powerpoint file from a flash drive and can't send it via email)

[F*ck Cybersecurity : cybersecurity](https://old.reddit.com/r/cybersecurity/comments/12aumfx/fck_cybersecurity/)

- The comments indicate it well:
- Your mission isn't to safeguard assets. Your mission is to help bring cyber risk in line with company policy. If you advise X, Y and Z because A and they say no because B, you document it and go get a Coke.
- There's something very wrong about corporate awfulness, and that's cysec for you.

## Tentative Sections

- Honeypot
- Managed Security Services
- Forensics
- Recovery
- Destruction

## clever exploit detection

[Tesla has used space characters in internal emails to identify leaks | Hacker News](https://news.ycombinator.com/item?id=33621562)
[Nico H on X: "@GergelyOrosz Since people are asking https://t.co/iOgDvVl3Ge" / X](https://twitter.com/pnikosis/status/1592823543498436611)

[Detecting unauthorized physical access with beans, lentils and colored rice (2021) | Hacker News](https://news.ycombinator.com/item?id=31897530)
[dys2p](https://dys2p.com/en/2021-12-tamper-evident-protection.html)

[Operation Gunman - how the Soviets bugged IBM typewriters (2015) | Hacker News](https://news.ycombinator.com/item?id=31965969)
[Selectric bug](https://www.cryptomuseum.com/covert/bugs/selectric/)

## DFIR

[@sansforensics](https://twitter.com/sansforensics)
the world's leading Digital Forensics and Incident Response provider.

[Home Page](https://www.dfir.training/)

## malware analysis

[Searching samples – Max Kersten](https://maxkersten.nl/binary-analysis-course/obtaining-samples/searching-samples/)

## threat actors

[GitHub: Widespread Injection Vulnerabilities in Actions | Hacker News](https://news.ycombinator.com/item?id=24980187)
[2070 - GitHub: Widespread injection vulnerabilities in Actions - project-zero](https://bugs.chromium.org/p/project-zero/issues/detail?id=2070&can=2&q=&colspec=ID%20Type%20Status%20Priority%20Milestone%20Owner%20Summary&cells=ids)

### threat detection

[Spy camera detection using smartphone time-of-flight sensors | Hacker News](https://news.ycombinator.com/item?id=29267168)
[LAPD | Proceedings of the 19th ACM Conference on Embedded Networked Sensor Systems](https://dl.acm.org/doi/10.1145/3485730.3485941)

[GitHub - levlesec/lockup: A proof-of-concept Android application to detect and defeat some of the Cellebrite UFED forensic toolkit extraction techniques.](https://github.com/levlesec/lockup)

[How to Find Hidden Cameras and Spy Gear | Hacker News](https://news.ycombinator.com/item?id=18926264)
[How to Find Hidden Cameras and Spy Bugs (The Professional Way) - Sentel Tech Security](https://web.archive.org/web/20190826071818/https://www.senteltechsecurity.com/blog/post/how-to-find-hidden-cameras/)

### profiling

[GitHub - curated-intel/Threat-Actor-Profile-Guide: The Threat Actor Profile Guide for CTI Analysts](https://github.com/curated-intel/Threat-Actor-Profile-Guide)

### naming conventions

[Microsoft shifts to a new threat actor naming taxonomy | Microsoft Security Blog](https://www.microsoft.com/en-us/security/blog/2023/04/18/microsoft-shifts-to-a-new-threat-actor-naming-taxonomy/)
[Microsoft Security](https://www.microsoft.com/en-us/security/default.aspx)

## incident response / blue team

[GitHub - fabacab/awesome-cybersecurity-blueteam: A curated collection of awesome resources, tools, and other shiny things for cybersecurity blue teams.](https://github.com/fabacab/awesome-cybersecurity-blueteam)

[GitHub - meirwah/awesome-incident-response: A curated list of tools for incident response](https://github.com/meirwah/awesome-incident-response)

[A-poc/BlueTeam-Tools: Tools and Techniques for Blue Team / Incident Response](https://github.com/A-poc/BlueTeam-Tools)

[What is an Incident Response Plan? Step by Step Guide and Examples | CompTIA](https://www.comptia.org/blog/security-awareness-training-incident-response-plans)

[LetsDefend](https://letsdefend.io/)
Blue team training platform.

[Phishing Incident Response Automation | Phish Report](https://phish.report)

## memory destruction

[Securely Wipe Disks and Delete Files](https://brainfucksec.github.io/securely-wipe-disks-and-delete-files)

[Senthil Kumar aka SK](https://www.ostechnix.com/securely-permanently-delete-data-linux/)
(2017) How To Securely And Permanently Delete Your Data In Linux

[nixCraft 🐧: "Compliance is the root of all …" - Mastodon](https://mastodon.social/@nixCraft/112084612189308888)

[Need a hard drive destroyed. Is this good enough? : pcmasterrace](https://old.reddit.com/r/pcmasterrace/comments/1bslktz/need_a_hard_drive_destroyed_is_this_good_enough/)

### Morgan Stanley Lost Some Hard Drives - Matt Levine

Don't throw out your computers
Well here's my new financial heist movie script. A big bank has a lot of computers that keep track of its customers' accounts. It periodically buys new computers to do a better job of keeping track of those accounts. When it does that, it hires a moving company to cart away all of the old computers. The moving company makes a few extra bucks by selling the old computer hardware to, I don't know, scrappy small technology businesses that are happy to have the bank's slightly outdated hardware. Ideally the bank, or the moving company, would delete all the data on the computers first, but that takes time and time is money and sometimes they forget.
So what you do is, you set up a scrappy small tech business as a cover, and you go to the bank's moving company's computer sale and buy all the computers, and then you turn them on and get all of the bank's customers' account information, and then you steal their money. Okay, having written this all out, I guess it is a boring heist movie, never mind. Still:

    The Securities and Exchange Commission today announced charges against Morgan Stanley Smith Barney LLC (MSSB) stemming from the firm's extensive failures, over a five-year period, to protect the personal identifying information, or PII, of approximately 15 million customers. MSSB has agreed to pay a $35 million penalty to settle the SEC charges.
    The SEC's order finds that, as far back as 2015, MSSB failed to properly dispose of devices containing its customers' PII. On multiple occasions, MSSB hired a moving and storage company with no experience or expertise in data destruction services to decommission thousands of hard drives and servers containing the PII of millions of its customers. Moreover, according to the SEC's order, over several years, MSSB failed to properly monitor the moving company's work. The staff's investigation found that the moving company sold to a third party thousands of MSSB devices including servers and hard drives, some of which contained customer PII, and which were eventually resold on an internet auction site without removal of such customer PII. While MSSB recovered some of the devices, which were shown to contain thousands of pieces of unencrypted customer data, the firm has not recovered the vast majority of the devices.

Great stuff. If you find a 2016-vintage Morgan Stanley computer on EBay and crack it open to find customer information, I guess you can … do … something with that? I don't know. Here, from the SEC complaint, is what one guy did:

    On October 25, 2017, nearly a year after the completion of the 2016 Data Center Decommissioning, MSSB received an email from an IT consultant in Oklahoma ("Consultant"). In that email, Consultant informed MSSB that he had purchased hard drives from an online auction site and that he had access to MSSB's data on those devices. In that email, Consultant informed MSSB that "[y]ou are a major financial institution and should be following some very stringent guidelines on how to deal with retiring hardware. Or at the very least getting some kind of verification of data destruction from the vendors you sell equipment to." MSSB eventually repurchased the hard drives in Consultant's possession.

Somehow the SEC neglects to mention how much Morgan Stanley paid him for those hard drives. How much would you charge Morgan Stanley for the hard drives in this situation? I do not want to give you legal advice, and I think that you would want to get some legal advice before trying this, but I think if you offered these hard drives to Morgan Stanley for, say, $100,000 each, they might pay you? Is there a bug bounty program for, you know, you threw out the wrong hard drive? They paid the SEC $35 million; there is money in the budget for this sort of thing.
The rest of the complaint is full of suggestive hints at the scale of Morgan Stanley's after-the-fact garbage hunt:

    In late 2017, MSSB launched an investigation into the disposition of the devices that were part of the 2016 Data Center Decommissioning project and determined that Moving Company had also delivered the 8,000 back-up tapes removed from one of the data centers to IT Corp B. MSSB emailed IT Corp B on January 19, 2018 asking whether IT Corp B could "confirm the disposition of …3k lbs of tapes." IT Corp B responded: "I can confirm that we did send this load of tapes for secure waste to energy incineration. Although that lot # is not the lot # we used. They were processed 'Confidential Material' in June of 2016." MSSB's basis for believing that these tapes were in fact destroyed without any unauthorized access to customer PII and consumer report information hinges on this email. MSSB has no other verification or 5 documentation that these tapes were destroyed.
    In June 2021, MSSB obtained another fourteen of the missing hard drives from a downstream purchaser. Based on forensic analysis of these hard drives, thirteen of the devices contained a total of at least 140,000 pieces of customer PII. The vast majority of the hard drives from the 2016 Data Center Decommissioning remain missing. …
    MSSB has identified an international shipping project that may have involved Moving Company. MSSB can state only that "documents suggest" that Moving Company transported 18-36 unspecified devices to a storage location in New York City. It was contemplated that those devices would be shipped internationally to Europe, potentially by Moving Company. 

Possibly thousands of ancient Morgan Stanley storage devices, all over the globe, possibly full of customer data, possibly useful for nefarious purposes. Probably not; there is no suggestion that anyone did anything at all nefarious with any of these things, and also not much suggestion that you could do anything particularly bad. (You're not supposed to hand out customers' "personal identifying information" to random hackers, but there's no suggestion that it was, like, account passwords.) 
More from
Bloomberg opinion
When Immigration Hypocrisy Landed on Martha's Vineyard
LinkedIn's Future Is a Joke
I Paid Off Student Loans But Support Relief for Those Who Can't
Don't Let the Crypto Winter Go to Waste
In recent years it has been popular for investment bank executives to say that they were becoming tech companies: They were hiring developers, building apps, talking about big data. This is a good thing to say, I suppose, insofar as being a tech company means that you can make large profits without putting too much of your own balance sheet at risk, that you can scale rapidly, that you can compete with Silicon Valley for employees.
But there is also an old-school understanding of investment banking in which it is a business of implicit knowledge, of personal connections, that the value that a good banker can add can't be reduced to an algorithm. There is a tension there. If banks are tech companies then they will invest in good consistent electronic communication tools that create good searchable records. If banking is a business of personal connections, then bankers will ignore those tools and text clients on their personal cell phones because that feels more personal. Morgan Stanley got fined $200 million for that this summer. You are supposed to use the official communication tools.
Similarly, if banking is a business of implicit knowledge, go ahead and throw out the old hard drives; what's important is the knowledge in the hearts and minds of the bankers. If banking is a data business, you should probably wipe the hard drives before you throw them out.

## memory recovery

[First word discovered in unopened Herculaneum scroll by CS student | Hacker News](https://news.ycombinator.com/item?id=37857417)
[First word discovered in unopened Herculaneum scroll by 21yo computer science student | Vesuvius Challenge](https://scrollprize.org/firstletters)

[A disk so full, it couldn't be restored | Hacker News](https://news.ycombinator.com/item?id=39925186)
[A disk so full, it couldn't be restored - Six Colors](https://sixcolors.com/post/2024/03/a-disk-so-full-it-couldnt-be-restored/)

[Retrieving 1TB of data from a faulty drive with the help of woodworking tools | Hacker News](https://news.ycombinator.com/item?id=37160783)
[John Graham-Cumming's blog: Retrieving 1TB of data from a faulty Seagate Firecuda 530 drive with the help woodworking tools](https://blog.jgc.org/2023/08/retrieving-1tb-of-data-from-faulty.html)

### file recovery

[Undeleting a file overwritten with mv - pretix - behind the scenes - Behind the scenes of pretix, your friendly open source ticketing system from next door. Might contain traces of technology and business.](https://behind.pretix.eu/2020/11/28/undelete-flv-file)

[Recover a corrupt video file: techsupport](https://www.reddit.com/r/techsupport/comments/12hu6ye/recover_a_corrupt_video_file)

### forensics

[Digital Forensics Tips](https://digitalforensicstips.com/)
Includes blog posts about using AWS to further OSINT capability. Very useful.

## on-call

[alicegoldfuss/oncall-handbook](https://github.com/alicegoldfuss/oncall-handbook)
Tips and tricks for getting through on-call

[Pat Cable](https://blog.threatstack.com/balancing-security-and-your-on-call-rotation-using-deputize)
Balancing Security and Your On-Call Rotation Using Deputize

## notifying users

[Apple alerts users in 92 nations to mercenary spyware attacks | Hacker News](https://news.ycombinator.com/item?id=40002987)
[Apple alerts users in 92 nations to mercenary spyware attacks | TechCrunch](https://techcrunch.com/2024/04/10/apple-warning-mercenary-spyware-attacks/)

## security audits

[Infrastructure audit completed by Radically Open Security | Hacker News](https://news.ycombinator.com/item?id=37060654)
[Infrastructure audit completed by Radically Open Security | Mullvad VPN](https://mullvad.net/en/blog/2023/8/9/infrastructure-audit-completed-by-radically-open-security)

## security countermeasures

[D3FEND Matrix | MITRE D3FEND™](https://d3fend.mitre.org/)
A knowledge graph of cybersecurity countermeasures

## security overreach

[The Insecurity Industry | Hacker News](https://news.ycombinator.com/item?id=27965746)
[We Need To Talk About The Insecurity Industry](https://edwardsnowden.substack.com/p/ns-oh-god-how-is-this-legal)

[Interview with CEO of rsync.net: "no firewalls and no routers" | Hacker News](https://news.ycombinator.com/item?id=26504287)
[Console Newsletter - The best tools for developers](https://console.dev/interviews/rsync-john-kozubik)

## security regulations

[New SEC rule for publicly-traded firms and cybersecurity](https://old.reddit.com/r/cybersecurity/comments/15a954w/new_sec_rule_for_publiclytraded_firms_and/)

[What not to write on your security clearance form (1988) | Hacker News](https://news.ycombinator.com/item?id=34437937)
[What Not To Write On Your Security Clearance Form](https://milk.com/wall-o-shame/security_clearance.html)

[I am now in charge of a new cybersecurity department (only me). I am looking for suggestions as to what my first 3-6 months should look like. : cybersecurity](https://old.reddit.com/r/cybersecurity/comments/11gnjaj/i_am_now_in_charge_of_a_new_cybersecurity)

## management doesn't care

[Tired of management not caring about cybersecurity](https://old.reddit.com/r/cybersecurity/comments/159krj7/tired_of_management_not_caring_about_cybersecurity/)

[In FAA and across federal government, outdated software needs fixing - CSMonitor.com](https://www.csmonitor.com/Business/2023/0117/Bringing-US-up-to-code-How-outdated-software-has-become-a-safety-issue)

## managed security services

[Managed Security Services Recommendation : AskNetsec](https://old.reddit.com/r/AskNetsec/comments/tjhaf1/managed_security_services_recommendation)

## finding a pentest company

[Tips for Choosing a Pentesting Company](https://thehackernews.com/2022/10/tips-for-choosing-pentesting-company.html)
