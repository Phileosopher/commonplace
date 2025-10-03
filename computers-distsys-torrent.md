
# What torrenting and P2P is

[Intellectual property](legal-ip.md) is big money. People don't like their stuff getting copied. While it doesn't legitimately reflect the [original term](legal-crimes.md) (hijacking and committing violent acts in a remote area), the legal term for illegally or pseudo-legally copying IPs is known as "piracy".

The penalties for piracy are extremely steep, depending on the situation. We're often talking in the tens of thousands of dollars, with prison time often involved. The charges aren't anywhere *near* that scope for individual citizens who consume for personal use without money involved (often a simple misdemeanor instead of a felony), but depending on the situation someone can still get in serious trouble for simply downloading/copying copyright-protected media for a friend or family member.

Even with punitive measures that would drive any convict to prison and make them [indebted for life](slavery.md), most pirates get away with it, and there are *constant* new pirates joining, even with the clearly apparent risks of the decision.

As the [internet](computers-sofware-webdev.md) has grown, piracy has as well, and entails quite a few forms of computer information:

- [Software](computers-software.md)
- Copyrighted media such as music, movies, and books
- Databases, including [hacked data](computers-cysec-pentest.md)
- Trade secrets
- Software that specifically empowers piracy

## IP agnostic

To start with, computers don't naturally understand copyright-protection because they're not intuitive. Any person with a lick of common sense will feel something is wrong if another person handed them a briefcase stuffed with money sticking out the sides and white powder on it. In a digital sense, computers don't have that sort of intuition unless it was programmed to pay specific attention to it.

One of the ways computers track intellectual property is with "digital rights management" (DRM), which is essentially computer code designed to enforce IPs. It can sometimes mean a PDF can't be copied, an online multiplayer game can't go online, or software is severely hampered until the user enters a special code.

DRM is highly complicated, for several reasons:

1. Most [intellectual property](legal-ip.md) treats digital content as an extension of physical things, but in computers "moving" anything digitally is actually copy-then-delete. Giving a book to a friend isn't violating copyright, but is technically a violation by emailing it and not deleting the original copy. It's actually *less* work to violate copyright law digitally by sharing a song (copy a file) than doing it legally (copy a file and delete the original).
2. DRM often breaks the usability for the legitimate owners of the device, meaning users may be *forced* to [hack](hacking.md) their rightfully owned property.
3. Intellectual property lawyers are often not computer experts, so they aren't aware of #1 when they press charges.
4. Judges are often not computer experts, so they might enforce intellectual property lawyers' rights without being aware of #1.
5. The willpower of the hacking/"cracking" community mean very clever [hacks](hacking.md) come out shortly after media releases with DRM:
   - CDs had DRM preinstalled to prevent copying, until someone found out how to remove it by drawing a permanent marker around the edge of the CD.
   - Software keys to register a product are often hiding inside the source code or is a list from a database.
   - Hackers often reverse-engineer the source code, then rebuild the entire thing and release it as an unlocked version.
6. Further, if an IP-holder gets *too* oppressive with their rights management, for a variety of reasons they'll often see typical consumers pirate copies or use alternative products (e.g., [open-source](legal-ip-floss.md)).

## Moral vs. legal

The implications of piracy are controversial.

Proponents of enforcing anti-piracy laws are quick to say:

- They lose money for each copy that someone chooses to illegally download.
- The illegal copiers, if punished enough, will deter everyone else from illegally downloading.
- It's unethical that rights-holders can't make their full amount of rightfully-earned money off their property.

Opponents quickly respond:

- The money lost is negligible or nothing, since people weren't going to pay to consume that media anyway.
- There's no way to permanently suppress illegal distribution of content.
- It's unethical that individuals can't consume something that could positively improve their lives, especially when specific national laws suppress freedom to consume that media.

There's not much scientific information about money lost on IPs, but the EU *did* try to suppress [a 300-page scientific study](https://felixreda.eu/wp-content/uploads/2017/09/displacement_study.pdf) that indicates that the only time [IP](legal-ip.md)-holders lose money is when it's a new release. This does make sense, since media typically becomes easy to acquire (and also part of the public consciousness to where it's not as [in-demand](economics.md)) proportionally to how long it has been published.

This doesn't change the current legality of intellectual property, though. There are specific clauses such as fair use that permit educational purposes and parody, and many varieties of more lenient IPs exist for people who don't feel driven to the severely confining scope of copyright (e.g., [creative commons](legal-ip.md), [LGPL](legal-ip-floss.md)).

## P2P protocols

Before going into the technical side of it, it's worth understanding how "peer-to-peer" (P2P) [protocols](standards-computers.md) work:

- Instead of conventional networking protocols with a client/host relationship, P2P is designed where every network node is *both* a host *and* a client.
- Information disseminates across every engaged computer in that network (which very often happens to be the internet), and the only way to stop the flow of information is to take down *every* computer that has that information.
- P2P protocols typically hold an entire network together with a "magnet link", which sends out a communication to the other computers that share that magnet link. If they have the same magnet link, they'll share information.
- Magnet links can be quickly and easily converted into a [hash](encryption.md) for quickly referencing the information across the internet.

There are [many P2P protocols](https://en.wikipedia.org/wiki/List_of_P2P_protocols), but the most popular [network protocol](networks-computer.md) for P2P, by far, is the BitTorrent protocol. "Torrenting" operates on a relatively straightforward system:

1. A computer (typically a "tracker") hosts a "magnet link" as a .torrent file, which specifies a [hash](encryption.md) that a BitTorrent "client" can open.
2. That magnet link refers to one of the clients, which has an authoritative set of complete data.
3. The protocol parses the sending data into packets, then checks whether those packets are available elsewhere.
4. Any other user can use a different BitTorrent client to download the data, or "leech" it. It may be sequential, but is often in no particular order. While downloading, it'll also seed data.
5. At any time afterward, any user that downloads data can *also* upload their own packets, or "seed" that set of data.
6. The blocks are prioritized by their lowest availability within other computers on that network.
   - The emphasis on sending the lowest-available is part of the reason BitTorrent is so difficult to shut down.
7. If other BitTorrent clients have that same magnet link enabled, they'll *also* upload/download the data, with multiple other clients at once.
8. Even if a client goes offline, the packet-based transfer means it can resume precisely where it left off.
9. When there are enough clients seeding, the content has a torrent "swarm", and is pretty much impossible to take down without destroying *all* the [network connections](networks-computer.md) of those computers at once. Enabling a "distributed hash table" (DHT) in the client can magnify user interactions after the initial leeching.

The most popular group that manages torrents is the Pirate Bay. They continue to stick around because they never legally hold content, but constantly hold the hashes that point *to* the content that other people hold. It's a legal technicality that keeps them around.

P2P creates several legal hurdles:

1. Information on the internet easily travels across international boundaries all the time, making certain local national laws ineffective.
2. It's logistically impossible to press charges against *every* person who owns a computer on a vast network.

## Trackers

Some sites, such as thePirateBay, host public "trackers", where anyone can download and share content, and they typically have more leechers and fewer seeders, as well as risks of [malware](computers-cysec-malware.md), [crypto miners](computers-blockchain.md), or third-party [DRM](legal-ip.md).

By contrast, private trackers require a membership. Generally, members must contribute back by uploading data proportionally to the amount they consume from the tracker. To incentivize more uploading, the tracker managers will often provide half-leech or (more often) freeleech content, which allows users to download content without affecting their ratio.

Most private trackers [specialize](jobs-specialization.md) in older, non-mainstream content, which is far less likely to lead to an [intellectual property](legal-ip.md) suit/enforcement.

- They tend to usually distribute higher-quality content
- They'll usually zoom in on specific domains (e.g., movies, TV shows, music, animation).
- They also typically hire staff who test whether the content is [malware](computers-cysec-malware.md) before seeding it.
- Further, they'll frequently take content requests for other available media.

The only way to join private trackers is through a well-established reputation on specific invite forums, which often includes uploading new content in some capacity. The content can then be shared indefinitely via a [hosted](computers-distsys-cloud.md) "seedbox" or temporarily via a "debrid". The entire community is *very* close-knit, and tracker managers frequently ban people who abuse the system or [exploit it](hacking.md) via invites.

The chances of finding [malware](computers-cysec-malware.md) on a public tracker is *much* higher, as well as the odds of being monitored by a government intelligence agency.

## How P2P persists

To start with, many times the pirating groups find ways to navigate *around* existing laws:

- It's illegal to share intellectual property, but it's not necessarily illegal to *point* to things that illegally share intellectual property.
- Not all nations respect intellectual property law, or to the same effect, and the geographical location of the hosting computer is typically who has jurisdiction over that region.

Contrary to the public perspective of everything running through torrents, all of this file-sharing is maintained through a scattered and constantly shifting variety of semi-exclusive social media:

- Public forums on [social media](networks-social.md) (e.g. Reddit)
- Hosted web forums
- Text messaging groups (e.g., Telegram)
- Chat services (e.g., Discord)
- Various other [protocols](standards-computers.md) (e.g., Usenet)
- "Bots" and "scripts" that automate everything
- Public websites and folders that allow direct download.

Pirated content travels through a type of [supply chain](logistics.md) from its original availability to mass dissemination:

1. Warez scene groups - aka scene, relatively small groups of people crack software and directly release "ripped" media content and cracked "warez".
   - They're typically the most tech-savvy group, and live by [*very* strict community guidelines](https://scenerules.org/) that floats close to the [protocol standards](standards-computers.md).
   - Their hacking is often perfectly legal, though their *distribution* often isn't, and they tend to not release their content to P2P protocols because it would expose their IP address.
   - As they release content (aka pre's), they'll update a pre-database to let the community know.
   - They'll often re-release fixed or improved versions of their efforts (aka repacks).
2. Top sites - high-powered servers that use [FTP](standards-computers.md) to send large amounts of files.
   - They'll typically require a ratio of certain upload/download requirements, which ensures that content stays redundant across multiple hosts even when a government shuts down one of them.
   - They tend to have very strict requirements and specific sections for various purposes (e.g., Europe-only video games).
3. Couriers/"racers" - individuals who trade content between pirated sites.
   - They typically will honor the rules, and will download/upload content among top sites.
   - Alongside FTP, they'll use an IRC [sub-protocol](standards-computers.md) called XDCC to upload large files, often on [compromised computers](computers-cysec-pentest.md).
   - They'll often damage the bona fide nature of internet services: exploiting free-tier disposable cloud storage, using web domains.
   - Many of *them* will share their content to torrents for pretty much everyone else to use.
4. Average people - individuals who simply want a free or non-DRM version of media/software.
   - Since software is executable, most [malware](computers-cysec-malware.md) for many people comes bundled within public torrents.
   - For the most part, if a user simply [virus scans](computers-cysec.md) any downloaded content, they won't get any malware.

## The ongoing battle

While governments often take down indexing for pirated addresses, hosting, and seeders, the name will simply move around (e.g., AmazingTorrents.com becomes AmazingTorrents.li, and eventually AmazinTorrens.ru).

- The only way they can take down the system entirely is to criminally prosecute *everyone* who pirates content, which is both prohibitively expensive and often unlawful according to many nations' constitutions.
- It's often not as difficult to criminally prosecute people making money off their efforts (i.e., by charging them with tax evasion), or for transferring illegal content (e.g., child pornography), but most situations are simply civil IP disputes.

In short, piracy is a portion of the never-ending arms race within the larger domain of [cybersecurity](computers-cysec.md). Every site torn down is only a fraction of where the content is available.

- Any formal efforts to suppress it will, like every other aspect of [human nature](people-rules.md), drive it underground.
- The implementation of circumventing the law is constantly changing to respond to the situation ([IP](legal-ip.md)-disrespecting government, endless rapidly-deployed [websites](computers-sofware-webdev.md), [new decentralized protocols](standards-computers.md), [new network infrastructure](networks-computer.md)).
- The piracy community, however, sees the legislative moves as a type of challenge to overcome, and they're *constantly* changing tactics, with endless temporary [storage](computers-memory.md) and [decentralization](computers-distsys.md) for just about everything.
- In fact, the only way to sufficiently crush internet piracy is to employ a single, worldwide [government](politics-systems.md) that micromanages [human freedoms](people-boundaries.md).

There's no way to fully prevent [intellectual property](legal-ip.md) violations, since it only takes a few (typically young) people on the internet devoted to uploading content. The only solution to avoid the fight while also making a living is to [release the content for free](legal-ip-floss.md).

The controversy of torrenting has become almost a mainstay of society:

1. As long as [large organizations wish to exert power](groups-large.md), and [the law honors it](people-rules.md), they will try to shut piracy down.
2. However, law enforcement only abates the wave, and never successfully shuts anything down completely.
3. New technologies give the public even *more* power. The decentralized BitTorrent protocol, for example, has inspired [blockchain](computers-blockchain.md), which now competes as a strange de facto alternative to [government-issued currency](economics.md).

Many software entrepreneurs and executives [aren't particularly aware](trends.md) of the mindset of pirates, and it creates a few odd arrangements:

1. Particularly freedom-loving software developers will open the doors wide-open for [complete software freedom](legal-ip-floss.md), which will attract piracy-based users. This may include free [network use](networks-computer.md), free [storage](computers-memory.md), or [free hosting](computers-sofware-webdev.md).
2. If they're not careful, that [risk exposure](safety-riskmgmt.md) will make them stand out as the go-to piracy solution, drawing in more users in that community. If they don't diversify their [marketing](marketing.md), they'll become [notorious](image.md) for piracy-based activities.
3. Eventually, government authorities will approach those developers, typically either requesting key information about users or to deactivate/delete content. The situation forces them into an ultimatum:
   - Give that information or act on behalf of the government, and receive the public resentment of the piracy world.
   - Withhold that information or resist taking down content, and get flagged by that government for noncompliance.
4. From the point that they've taken a side, their software company has now become a [politicized instrument](politics-conservativeliberal.md), either towards that government or towards a libertarian-leaning mentality.
5. This situation can become *much* more complicated with respect to a nation that changes political parties frequently (e.g., USA).

## Piracy is publicly useful

The natural design of DRM is to prevent complete use of a product. Sometimes, this can mean the product is *completely* unusable, especially if the company goes out of business and no longer maintains the necessary [authentication](computers-cysec-authentication.md) measures for that DRM.

In those situations, a pirated copy is the *only* way to access "legacy" software. Without a previously pirated copy, that software from years ago may become impossible to access.

To that end, piracy can often allow libraries and archivists to historically preserve software that would otherwise have expired and become lost to permanent [encryption](encryption.md).

## P2P isn't just piracy

Beyond torrenting, P2P has other implementations:

- General file-sharing has many uses in a P2P environment, such as with [open-source software](legal-ip-floss.md).
- If the file-sharing is encrypted, it can become P2P [cloud storage](computers-distsys-cloud.md).
- If the files can update fast enough, P2P can be useful for [web hosting](computers-sofware-webdev.md).
- P2P banking would mean decentralized monetary management, which has become a major use for [cryptocurrency](computers-blockchain.md).
