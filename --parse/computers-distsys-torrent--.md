
## need more research

merges with several other things:
1. TT P2P/Torrent
2. Hacking?
3. Protocols?

## Private Trackers

NOTE: CLARIFY WHAT SCENE RELEASES ARE
PRIVATE TRACKERS ARE ALL DOMAIN-SPECIFIC

## redistribution

[gd-utils](https://github.com/roshanconnor123/gd-utils)
[Bypass-GDrive](https://yuudrive.me/tools/bypass-gdrive)
[nenokkadine/GD-Utils: This repo is just for heroku deployment of GD-Utils](https://github.com/nenokkadine/GD-Utils)
Google Drive Limit Bypass
- THERE ARE ALL SORTS OF HACKY WAYS TO TAKE ADVANTAGE OF FREE ACCOUNTS
- BY USING FREE ACCOUNTS, THERE'S LESS PAPER TRAIL FROM CARD PAYMENTS

## 00 TT Torrent - ISP Complaints

The following is not meant to be an in-depth explanation of the logistics involved in relationships between internet service providers and copyright parties, but rather a simple overview of answers to common inquiries regarding piracy and the importance of privacy.

### Copyright infringement complaints

#### Will I receive a letter/complaint from my ISP for downloading `x` or browsing a pirate site?

Browsing a pirate website will not get you in any sort of trouble by your ISP.

In regards to downloading, it depends on the country in which you live, but this guide is mainly intended for USA/Canada-based users since that is reddit's primary userbase. In some countries, like Germany, you are likely to be hit with a sizeable fine if you are caught pirating, so stay away from torrents completely if you live there.

If you are downloading via torrents (ie. Torrenting, through the use of a bittorrent client or other torrent-based application like Popcorn Time, or Showbox -To disable torrent functionality from Showbox, look through its settings), then yes, you will be caught. Being part of a torrent swarm at all means you are at risk of getting a copyright notice.

Otherwise, downloading through other means, such as direct downloads/DDL (ie. downloading from cloud storage like google drive or mega.nz, or file hosts such as zippyshare, or other centralized downloads, irc, usenet, etc.), would not get you caught. DDL is a blanket term used for any sort of direct connection between you and a single other server. Basically, if the download is done via HTTP, FTP (either through your browser or a download manager), you will not be caught.

Downloading a `.torrent` file from a website does not classify as torrenting, as that occurs through an HTTP download. Browsing a torrent site also will not trigger complaints from your ISP. Continue reading below for an explanation.

#### How does my ISP know what I am downloading and why is it only torrents that are the culprit for copyright infringement letters?

ISPs are not the ones who monitor your downloading habits for the purpose of punishing you -An ISP would not have any stake in trying to bust their users for acts of piracy on their own accord. If an ISP cared about your piracy habits, they would simply block access to pirate websites instead of constantly monitoring their users for acts of piracy. The blame lies with copyright trolls, parties that monitor the distribution of copyrighted material and use "mass copyright litigation to extract settlements from individuals". The only type of piracy that these groups can monitor are torrents since the technology is inherently open -a torrent tracker will broadcast the IPs of the peers who are present in that swarm to the other peers, as a means of reporting which pieces of the file(s) each peer has for the purpose of distribution (ie. user A has piece `x` and user B is missing piece `x`, therefore user A will now upload to user B). As a result, copyright trolls can easily join a swarm and log all of the IPs present in that swarm. These groups will then complain to the ISPs who own the IPs they logged, and in turn, the ISPs are expected forward the complaint to the account holder but in most cases, the ISP is not obligated to share the personal details of the account holder to the copyright protection group and will only forward their complaints and threaten to shut off your internet, while other times they merely serve as an educational warning. In some countries, like Germany, you are liable to be fined a hefty sum of money for copyright infringement.

When you download from a web server, on which the only peers involved are you and the server (as opposed to torrenting, where there are many peers), then only you and the server operator will know what is being downloaded if the server is SSL encrypted  (when visiting a webpage, SSL encryption is denoted by https in the URL, as opposed to just http). If your connection to the server is not SSL encrypted, then your ISP can easily know what is being downloaded. They won't do this, however, as they have no reason to -ISPs are not responsible for monitoring the downloading of pirated material.

#### Am I less likely to receive a copyright complaint from my ISP if I don't upload?

The "uploading is illegal, downloading is not" reasoning most people give for why only torrents get you caught is a myth. Downloading copyrighted content is still illegal, though uploading (sharing) of copyrighted content is a more serious act. However, this doesn't mean that uploading is the sole culprit in receiving complaints from your ISP -joining a torrent swarm at all will mean that your IP is liable to be logged and reported by copyright trolls. Even if uploading was the sole culprit for receiving copyright complaints, setting a ratio limit of 0 in your torrent client would do nothing to prevent copyright complaints, since torrents will naturally attempt to upload to other peers at any point during the download process and no proper torrent client (excludes Chinese clients like Xunlei Thunder) allows users to limit their upload speed to 0. If DDLs could be as easily monitored as torrent swarms, you would be getting copyright infringement complaints concerning their use as well.

#### How can I avoid getting copyright infringement complaints?

You have several options:

1. If you're going to download via torrents, use a VPN. A VPN creates a secure network connection over a public network such as the internet and encrypts your traffic. Your ISP will continue to know that you are consuming bandwidth, but to their eyes, your traffic will be encrypted. Your real IP will be hidden, so any server/network you connect to will only see your VPN's assigned IP address. A paid VPN is recommended, as there are no good free ones -such free VPNs will likely collect data from you, be too slow to bother with, or do not allow torrent traffic in the first place. Many VPNs can be as cheap as 3 USD/month, if you buy in bulk.

VPNs are not infallible, however, as your connection to them may sometimes fail. That is why some VPN providers offer a 'killswitch' function, which will disable all network activity on your computer if your connection to the VPN drops. If your VPN provider does not offer such functionality, you may consider switching to a torrent client that offers an in-built killswitch, like qBittorrent [(Here is a guide on how to accomplish this)](https://www.ghacks.net/2016/03/23/qbittorrent-block-transfers-vpn-disconnect/).

Note 1: Also keep in mind that some websites will throw a fit if you are connected to a VPN. Connecting to netflix will fail if you are behind a VPN; your banking institutions, including paypal, will raise a flag on your account and likely lock it due to suspicious login activity.

Note 2: qBitorrent has a setting called anonymous mode. It can cause many connectivity issues, essentially killing your ability to connect to peers: [[Reddit thread] qBittorrent has a "Anonymous Mode" ... Is this at a beneficial if I'm already using a VPN?](https://web.archive.org/web/20140128050529/http://www.reddit.com/r/torrents/comments/1vqt9b/qbittorrent_has_a_anonymous_mode_which_as_i)

Note 3: Many torrent clients offer a `force encryption` option. This does not hide your IP from the torrent swarm. It only attempts to mask your torrenting activity from your ISP, such that they do not become aware that you are transferring data through torrents. This setting aims to prevent ISPs from throttling your torrent transfers. Your IP will still be entered into the swarm, and any anti-piracy suit who chooses to enter the swarm can do so easily and log your IP. It is not a substitute for a VPN.

2. Rent a seedbox. A seedbox is a remote server that is set up with torrenting in mind -the server will handle all torrenting so your own IP will never have a chance of entering any torrent swarm. Once the server completes the torrent, you can download the content to your own computer through FTP or HTTP(S), both different types of direct downloads. It is extremely unlikely for your ISP to monitor your FTP transfers. Regardless, your seedbox provider should offer SSH access (your data transfers will be encrypted) if you are worried about your ISP snooping in on your data transfers.

3. Using a private tracker in conjunction with either of the above solutions is also advised. Copyright trolls go after low hanging fruit such as public trackers (thepiratebay, extratorrent, rarbg), which have millions of daily users and are therefore the prime target. By using a private tracker you are diminishing the likelihood of receiving an infringement letter, however, it is still not impossible.

4. Download using DDL (direct download) methods, such as google drive, mega, zippyshare, etc. DDL is a blanket term used for any sort of direct connection between you and a single other server. Such transfers could take the form of HTTP, ftp, etc.

5. Download from usenet. Check the [/r/usenet wiki](/r/usenet/wiki) for more info. Usenet is especially great for Movie and TV content and many usenet providers will provide SSL-encrypted downloads, allowing for greater peace of mind.

#### I just got a letter/email from my ISP about copyright infringement, what happens now?

The repercussions for pirating content vary by country. What may just be a mere *educational warningin one country, may lead to the suspension/termination of your internet service in another country. Your ISP may have outlined the repercussions in the letter/email you received. As an example, the UK-based ISPs, Sky and Virgin, deliver educational emails to copyright violators. Virgin is ambiguous about repurcissions whereas Sky has explicitly mentioned that violations will not result in service suspension. US-based ISPs are also likely to terminate your service if you get too many repeated complaints for copyright infringement - [the number of warnings before termination of service is supposedly 6.](https://sg.news.yahoo.com/six-strikes-explained-us-readies-piracy-warning-system-145127585.html) For more information regarding repercussions, your letter/email most likely states it, if not, refer to your ISP's ToS.

Furthermore, you shouldn't worry about being prosecuted for downloading pirated material. When people speak of being prosecuted for distribution of copyrighted content, they refer to the parties that make the pirated material available to begin with, such as streaming/torrent/pirate site operators. There are cases where the average joe can get into legal trouble for distribution, and those are cases that are referred to as example cases. One such case would be streaming pirated material to your fanbase on twitch, where people know your face and likely know your full real name, and copyright holders would want to prosecute these personalities to make an example out of them. Simple, every-day acts of piracy are not prosecuted, as they do not have any worth to the copyright holders, example-wise or monetary-wise (they would lose more money in lawyer fees than they'd get from you in a settlement).

The typical response to a copyright infringement letter is to just ignore it, move on with your day and follow the above advice on preventing further notices. If your internet has been shut down by your ISP, call them and ask what you can do to restore service, but never admit fault.

Again, keep in mind that different countries will have different laws regarding what the punishment should be. In certain countries, like Germany, you are likely to be hit with a sizable fine for copyright infringement. [Read this](https://www.reddit.com/r/Piracy/comments/fbf5so/fine_for_downloading_movie/) if you live in Germany and have received letter indicating that you will be fined.

#### I got caught pirating and my ISP has instructed me to delete the pirated material from my hard drive. Should I?

No, you don't need to. Your ISP cannot tell what's on your hard drive or not. As long as you follow the above advice on preventing further copyright infringement notices, you should be all set.

## 00 TT Torrent - Laws

[Senate Votes to Allow FBI to Look at Your Web Browsing History Without a Warrant](https://www.vice.com/en_us/article/jgxxvk/senate-votes-to-allow-fbi-to-look-at-your-web-browsing-history-without-a-warrant)

[Burn, drown, or smash your phone: Forensics can extract data anyway](https://www.zdnet.com/article/burn-drown-or-smash-your-phone-forensics-can-extract-data-anyway/)

[A new bill could punish web platforms for using end-to-end encryption](https://www.theverge.com/2020/1/31/21116788/earn-it-act-section-230-lindsey-graham-draft-bill-encryption)

[French court rules that Steam's ban on reselling used games is contrary to European law](https://www.polygon.com/2019/9/19/20874384/french-court-steam-valve-used-games-eu-law)

[MEPs approve sweeping changes to copyright law](https://www.theguardian.com/media/2019/mar/26/meps-approve-sweeping-changes-to-copyright-law-european-copyright-directive)

[The Legalities of Linking](https://www.lifewire.com/legalities-of-linking-3468972)

[EU court says linking to copyrighted material isn't illegal](https://www.engadget.com/2016/04/08/eu-court-linking-copyrighted-content-is-legal/)

[New EU Piracy Watchlist Targets Key Pirate Sites and Cloudflare](https://torrentfreak.com/new-eu-piracy-watchlist-targets-key-pirate-sites-and-cloudflare-181210/)

[Domain Registrar Can be Held Liable for Pirate Site, Court Rules](https://torrentfreak.com/domain-registrar-can-be-held-liable-for-pirate-site-court-rules-181224/)

[Reporting When Pirate Releases Hit The Internet is Apparently Illegal Now](https://torrentfreak.com/reporting-when-pirate-releases-hit-the-internet-is-apparently-illegal-now-190101/)

[Swiss Copyright Law: Downloading Stays Legal, No Site Blocking](https://torrentfreak.com/swiss-copyright-law-downloading-stays-legal-no-site-blocking/)

[Web Sheriff](https://en.wikipedia.org/wiki/Web_Sheriff)

[List of websites blocked in the United Kingdom](https://en.wikipedia.org/wiki/List_of_websites_blocked_in_the_United_Kingdom)

[Who Watches the Watchmen: Exploring Complaints on the Web](https://arxiv.org/abs/1902.05796)

## anonymity and piracy are connected

[Reddit: IP Address Disclosure Puts User Anonymity At Risk * TorrentFreak](https://torrentfreak.com/reddit-ip-address-disclosure-puts-user-anonymity-at-risk-240124/)

## cracks community

[Retro cracking and art underground | Defacto2](https://defacto2.net/)
Retro NFOs
[Defacto2](https://defacto2.net/welcome)

## deterrence can work

[Malware Threats Can Be An Effective Anti-Piracy Strategy, Research Suggests * TorrentFreak](https://torrentfreak.com/malware-threats-can-be-an-effective-anti-piracy-strategy-research-suggests-231130/)

[Pirate Site Blocking Boosts Legal Consumption, Research Finds * TorrentFreak](https://torrentfreak.com/pirate-site-blocking-boosts-legal-consumption-research-finds-240216/)

[Premier League IPTV Piracy Clickbait Reaches New Low, But Will Go Lower * TorrentFreak](https://torrentfreak.com/premier-league-iptv-piracy-clickbait-reaches-new-low-but-will-go-lower-240323/)

[Despite 155 Piracy Incidents in Cinemas, Pirates Suffer Worst Year Since 2012 * TorrentFreak](https://torrentfreak.com/despite-155-piracy-incidents-in-cinemas-pirates-suffer-worst-year-since-2012-240417/)

[DoodStream's 'Proprietors' Struggle to Comply With Hollywood Injunction * TorrentFreak](https://torrentfreak.com/doodstreams-proprietors-struggle-to-comply-with-hollywood-injunction-240607/)

## different reasons for piracy

[It's easier and faster to pirate an e-book, than it is to buy it | Hacker News](https://news.ycombinator.com/item?id=34172506)

['Expensive' Streaming Services Are a Key Reason for Americans to 'Pirate' * TorrentFreak](https://torrentfreak.com/expensive-streaming-services-are-a-key-reason-for-americans-to-pirate-240424/)

## dmca battles

[Roblox 'Weight Lifting Sim' Dev Gains Muscle From DMCA Counter-Notice * TorrentFreak](https://torrentfreak.com/roblox-weight-lifting-sim-dev-gains-muscle-from-dmca-counter-notice-240211/)

## game piracy

[GitHub - privateersclub/wiki: The most comprehensive game piracy wiki on the internet.](https://github.com/privateersclub/wiki)

## history

[Redfox Disappearance Puts a Spotlight on Defiant StreamFab * TorrentFreak](https://torrentfreak.com/redfox-disappearance-puts-a-spotlight-on-defiant-streamfab-240610/)

## huge piracy takedowns

[BitTorrent Tracker Blocks Thousands of 'Infringing' Hashes * TorrentFreak](https://torrentfreak.com/bittorrent-tracker-blocks-thousands-of-infringing-hashes-240103/)

['Movie-web' Domain Shut Down By Hollywood Complaint * TorrentFreak](https://torrentfreak.com/movie-web-domain-shut-down-by-hollywood-complaint-240224/)

[How Seized Firesticks in a Plastic Bag Opened Up a Pirate Rabbit Hole * TorrentFreak](https://torrentfreak.com/how-seized-firesticks-in-a-plastic-bag-opened-up-a-pirate-rabbit-hole-240107/)

[Kim Dotcom Expects New Raid & Bail Revocation After "Secret Orders" Issued in U.S. * TorrentFreak](https://torrentfreak.com/kim-dotcom-expects-new-raid-bail-revocation-after-secret-orders-issued-in-u-s-240513/)

[Motion Picture Association Statement on Conviction of Jetflicks Operators - Alliance for Creativity and Entertainment](https://www.alliance4creativity.com/statement/motion-picture-association-statement-on-conviction-of-jetflicks-operators/)

## I2P

[GitHub - mikalv/awesome-i2p: A curated list of awesome I2P implementations, libraries, resources, projects, and shiny things. I2P is an anonymous overlay network - a network within a network. It is intended to protect communication from dragnet surveillance and monitoring by third parties such as ISPs.](https://github.com/mikalv/awesome-i2p)

## IPFS

[IPFS Powers the Distributed Web](https://ipfs.tech/)

[IPFS Support in Brave | Hacker News](https://news.ycombinator.com/item?id=25836886)
[IPFS Support in Brave | Brave](https://brave.com/ipfs-support/)

[Show HN: Encrypt and upload files to IPFS from browser | Hacker News](https://news.ycombinator.com/item?id=38038662)

[HTTP is obsolete - it's time for the distributed, permanent web (2015) | Hacker News](https://news.ycombinator.com/item?id=28897373)
[HTTP is obsolete. It's time for the distributed, permanent web](https://ipfs.io/ipfs/QmNhFJjGcMPqpuYfxL62VVB9528NXqDNMFXiqN5bgFYiZ1/its-time-for-the-permanent-web.html)

[I moved my blog from IPFS to a server | Hacker News](https://news.ycombinator.com/item?id=39208673)
[Why I Moved My Blog from IPFS to a Server | Neiman's Blog](https://neimanslab.org/2024-01-31/why-i-moved-my-blog-ipfs-to-server.html)

## IPTV and m3u

[IPTV Community](https://iptv.community/)
Technology and IPTV discussion website, useful for finding an IPTV provider/reseller.

## ISPs and piracy

[Received a Piracy Warning From Your ISP? Here's What to Do * TorrentFreak](https://torrentfreak.com/received-a-piracy-warning-from-your-isp-heres-what-to-do-181007/)

## nulled scripts

[language agnostic - what does "nulled script" mean? - Stack Overflow](https://stackoverflow.com/questions/6350303/what-does-nulled-script-mean)

## p2p community

[P2Pcollab](https://p2pcollab.net/)

[Public Spaces.net](https://publicspaces.net/)

[FileSharing Talk](https://filesharingtalk.com/forum.php)
P2P Forum

[Aether](https://getaether.net/)
P2P Ephemeral Public Communities

[organize:howto [CryptoParty.]](https://www.cryptoparty.in/organize/howto)

## piracy has a glamorous streak

[Maggie Stiefvater](http://maggie-stiefvater.tumblr.com/post/166952028861/ive-decided-to-tell-you-guys-a-story-about)
a story about piracy by a book writer

[YoHoHo Asks GitHub to Take 'Pirated' Pirate-Themed Games Offline * TorrentFreak](https://torrentfreak.com/yohoho-asks-github-to-take-pirated-pirate-themed-games-offline-240710/)

[Peter Sunde - Wikipedia](https://en.wikipedia.org/wiki/Peter_Sunde)

## piracy is hard to fight

[Netflix: Piracy is difficult to compete against and growing rapidly | Hacker News](https://news.ycombinator.com/item?id=39254807)
[Netflix: Piracy is Difficult to Compete Against and Growing Rapidly * TorrentFreak](https://torrentfreak.com/netflix-piracy-is-difficult-to-compete-against-and-growing-rapidly-240204/)

[IPTV Anti-Piracy Threats May Increase Male Motivation to Pirate By 30% * TorrentFreak](https://torrentfreak.com/iptv-anti-piracy-threats-may-increase-male-motivation-to-pirate-by-30-240202/)

[You Wouldn't Steal an Episode of the 'Pirate Bay' TV Series? * TorrentFreak](https://torrentfreak.com/you-wouldnt-steal-an-episode-of-the-pirate-bay-tv-series-240310/)

[Telegram Block Averted For Now But Escalating Threat is Far From Over * TorrentFreak](https://torrentfreak.com/telegram-block-averted-for-now-but-escalating-threat-is-far-from-over-240329/)

[Pirate IPTV Investigations Are Expensive, Time-Consuming & Prone to Misfire * TorrentFreak](https://torrentfreak.com/pirate-iptv-investigations-are-expensive-time-consuming-prone-to-misfire-240405/)

['IP House' Takes Global IP & Anti-Piracy Protection to a New Level * TorrentFreak](https://torrentfreak.com/ip-house-takes-global-ip-anti-piracy-protection-to-a-new-level-240508/)

[Nintendo's DMCA Operation Continues With Lockpick, Kezplez-nx Takedowns * TorrentFreak](https://torrentfreak.com/nintendos-dmca-operation-continues-with-lockpick-kezplez-nx-takedowns-240508/)

[IMDb Struggles with Persistent Movie 'Piracy' Problem * TorrentFreak](https://torrentfreak.com/imdb-struggles-with-persistent-movie-piracy-problem-240514/)

[VPN, DNS, Give Up, or Go Legal: Aussies' Reactions to Pirate Site-Blocking in 2023 * TorrentFreak](https://torrentfreak.com/vpn-dns-give-up-or-go-legal-aussies-reactions-to-pirate-site-blocking-in-2023-240515/)

[YouTube Ripper Seeks IP-Addresses of 'Threatening' & 'DMCA-Abusing' Competitors * TorrentFreak](https://torrentfreak.com/youtube-ripper-seeks-ip-addresses-of-threatening-and-dmca-abusing-competitors-240517/)

[Court Rejects Law Firm's Bid to Directly Obtain BitTorrent Users' Identities * TorrentFreak](https://torrentfreak.com/court-rejects-law-firms-bid-to-directly-obtain-bittorrent-users-identities-240522/)

[Serie A Legal Action Claims Cloudflare Helps Pirates Evade Piracy Shield * TorrentFreak](https://torrentfreak.com/serie-a-legal-action-claims-cloudflare-helps-pirates-evade-piracy-shield-240528/)

[FBI Carries Out Fresh Round of Z-Library Domain Name Seizures * TorrentFreak](https://torrentfreak.com/fbi-carries-out-fresh-round-of-z-library-domain-name-seizures-240530/)

[Court Denies Filmmakers' Renewed Attempt to Get Redditors' IP Addresses * TorrentFreak](https://torrentfreak.com/court-denies-filmmakers-renewed-attempt-to-get-redditors-ip-addresses-240530/)

[€5.3m Pirate IPTV Network 'Dismantled' By Spanish Police is Still Streaming * TorrentFreak](https://torrentfreak.com/e5-3m-pirate-iptv-network-dismantled-by-spanish-police-is-still-streaming-240602/)

[Nintendo Hits 127 Switch Piracy Tutorial Repos After 'Cracking' URL Encryption * TorrentFreak](https://torrentfreak.com/nintendo-hits-127-switch-piracy-tutorial-repos-after-cracking-url-encryption-240604/)

[Organized Crime Unit Arrest Suspected Sky TV Pirate - What About His Users? * TorrentFreak](https://torrentfreak.com/organized-crime-unit-arrest-suspected-sky-tv-pirate-what-about-his-users-240605/)

[Google "Profits From Pirated Textbooks" Publishers' Lawsuit Claims * TorrentFreak](https://torrentfreak.com/google-profits-from-pirated-textbooks-publishers-lawsuit-claims-240610-240610/)

[Pirate Site Blocking Agency Reveals How and Why Pirates Circumvent Blocking * TorrentFreak](https://torrentfreak.com/pirate-site-blocking-agency-reveals-how-and-why-pirates-circumvent-blocking-240503/)

[Biggest IPTV Piracy Trial in U.S. History Underway and Already Controversial * TorrentFreak](https://torrentfreak.com/biggest-iptv-piracy-trial-in-u-s-history-underway-and-already-controversial-240612/)

[French court orders Google, Cloudflare, Cisco to poison DNS to stop piracy | Hacker News](https://news.ycombinator.com/item?id=40693451)
[Google, Cloudflare & Cisco Will Poison DNS to Stop Piracy Block Circumvention * TorrentFreak](https://torrentfreak.com/google-cloudflare-cisco-will-poison-dns-to-stop-piracy-block-circumvention-240613/)

[South Korean telecom company attacks torrent users with malware | Hacker News](https://news.ycombinator.com/item?id=40805099)
[South Korean telecom company attacks customers with malware — over 600,000 torrent users report missing files, strange folders, and disabled PCs | Tom's Hardware](https://www.tomshardware.com/tech-industry/cyber-security/south-korean-telecom-company-attacks-torrent-users-with-malware-over-600000-people-report-missing-files-strange-folders-and-disabled-pcs)
[South Korean ISP 'Infected' Torrenting Subscribers with Malware * TorrentFreak](https://torrentfreak.com/south-korean-isp-infected-torrenting-subscribers-with-malware-240625/)

[Kim Dotcom Can't Prevent NZ Govt. Sending Hard Drives & Passwords to FBI * TorrentFreak](https://torrentfreak.com/kim-dotcom-cant-prevent-nz-govt-sending-hard-drives-passwords-to-fbi-240628/)

[Anna's Archive Faces Millions in Damages and a Permanent Injunction | Hacker News](https://news.ycombinator.com/item?id=40908878)
[Anna's Archive Faces Millions in Damages and a Permanent Injunction * TorrentFreak](https://torrentfreak.com/annas-archive-faces-millions-in-damages-and-a-permanent-injunction-240708/)

[U.S. Universities Warn Students about Limewire and Kazaa... in 2024 * TorrentFreak](https://torrentfreak.com/u-s-universities-warn-students-about-limewire-and-kazaa-in-2024-240707/)

[3x new books added to the Pirate Library Mirror | Hacker News](https://news.ycombinator.com/item?id=32972923)
[3x new books added to the Pirate Library Mirror (+24TB, 3.8 million books) - Anna's Blog](https://annas-blog.org/blog-3x-new-books.html)

[What Killed Fmovies? Death By a 1000 Cuts, One Killer Blow, Or Possibly Both * TorrentFreak](https://torrentfreak.com/what-killed-fmovies-death-by-a-1000-cuts-one-killer-blow-or-possibly-both-240719/)

[Jacek Karpińśki, the computer genius the communists couldn't stand (2017) | Hacker News](https://news.ycombinator.com/item?id=41072026)
[The Computer Genius the Communists Couldn’t Stand | Article | Culture.pl](https://culture.pl/en/article/jacek-karpinski-the-computer-genius-the-communists-couldnt-stand)

[Ad Blocking Infringes Copyright? Ancient Sony Cheat Lawsuit May Prove Pivotal * TorrentFreak](https://torrentfreak.com/ad-blocking-infringes-copyright-ancient-sony-cheat-lawsuit-may-prove-pivotal-240729/)

[Kim Dotcom's extradition to the U.S. given green light by New Zealand | Hacker News](https://news.ycombinator.com/item?id=41254989)
[Kim Dotcom's Extradition to the U.S. Given Green Light By New Zealand * TorrentFreak](https://torrentfreak.com/kim-dotcoms-extradition-to-the-u-s-given-green-light-by-new-zealand-240815/)

[Billion Dollar Music Piracy Lawsuit Against Optimum is Over, Permanently * TorrentFreak](https://torrentfreak.com/billion-dollar-music-piracy-lawsuit-against-optimum-is-over-permanently-2400816/)

[NVIDIA: Copyrighted Books Are Just Statistical Correlations to Our AI Models * TorrentFreak](https://torrentfreak.com/nvidia-copyrighted-books-are-just-statistical-correlations-to-our-ai-models-240617/)

[17-year-old student exposes Germany's 'secret' pirate site blocklist | Hacker News](https://news.ycombinator.com/item?id=41328784)
[17-Year-old Student Exposes Germany's 'Secret' Pirate Site Blocklist * TorrentFreak](https://torrentfreak.com/17-year-old-student-exposes-germanys-secret-pirate-site-blocklist-240822/)

['Bonus' Episode of 'House of the Dragon' Comes With a Nasty Surprise for Pirates * TorrentFreak](https://torrentfreak.com/bonus-episode-of-house-of-the-dragon-comes-with-a-nasty-surprise-for-pirates-240825/)

[Pssst... Want to Snitch on Sellers of Pirate Streaming Services? * TorrentFreak](https://torrentfreak.com/pssst-want-to-snitch-on-sellers-of-pirate-streaming-services-240826/)

[Operation Redirect: Police Anti-Malware Action Protects Music & Pirates * TorrentFreak](https://torrentfreak.com/operation-redirect-police-anti-malware-action-protects-music-pirates-240830/)

## piracy is hard to fight - piracy shield

[Google: Piracy Shield Has Legal Limits, Anti-Piracy Chief: Think Ethics, Do More * TorrentFreak](https://torrentfreak.com/google-piracy-shield-has-legal-limits-anti-piracy-chief-think-ethics-do-more-240212/)

["Perfect" Piracy Shield & Propaganda: Blocking Blunders Branded "Fake News" * TorrentFreak](https://torrentfreak.com/fake-news-propaganda-props-up-piracy-shield-errors-dismissed-as-lies-240225/)

[Piracy Shield Source Code & Internal Documentation Leak Online TorrentFreak](https://torrentfreak.com/piracy-shield-source-code-internal-documentation-leak-online-240326/)

## piracy news

[TorrentFreak](https://torrentfreak.com/)
Piracy News

[TechGiga](https://www.techgiga.net/)
Piracy News

[/r/piracy](https://www.reddit.com/r/Piracy/)
piracy on reddit
:star:

[ShareMania.US](http://sharemania.us/)
(_insecure_) HDTV, HD Music Videos, 1080i, 720p, Live, TV Shows.

[SB-Innovation - Leecher Mod Source #1](https://www.sb-innovation.de/forum.php)
Tracker Forum

## piracy takedowns have consequences

[Fun Fact: I own porn I can't watch | Hacker News](https://news.ycombinator.com/item?id=34628996)
[Foone Turing - FUN FACT: I own porn I can't watch.](https://foone.tumblr.com/post/705446706461949953/hello-hacker-news-never-post-me-on-your-site-ever)

[Bungie's Vow to Relentlessly Pursue 'Anonymous' Cheaters Was No Bluff * TorrentFreak](https://torrentfreak.com/bungies-vow-to-relentlessly-pursue-anonymous-cheaters-was-no-bluff-240605/)

[Operation Anime Phase 2: New Anti-Piracy Crackdown Executed in Brazil * TorrentFreak](https://torrentfreak.com/operation-anime-phase-2-new-anti-piracy-crackdown-executed-in-brazil-240428/)

[Nintendo Takedown Wipes "Rhythm Heaven" Remix Tool & 250+ Forks Off GitHub * TorrentFreak](https://torrentfreak.com/nintendo-takedown-wipes-rhythm-heaven-remix-tool-and-250-forks-from-github-240619/)

[Austrian ISPs Block Cloudflare IP addresses after apparent court order | Hacker News](https://news.ycombinator.com/item?id=32630757)
[LIWEST Netzsperren](https://netzsperre.liwest.at/)

[Supreme Court Blow: ISP Bill Payers Aren't Piracy Police or Instantly Liable * TorrentFreak](https://torrentfreak.com/supreme-court-blow-isp-bill-payers-arent-piracy-police-or-instantly-liable-240704/)

## software piracy

[DirtyWarez](https://forum.dirtywarez.com/)

[Novanon](https://novanon.net/)

## the principle of ownership

[If buying isn't owning, piracy isn't stealing | Hacker News](https://news.ycombinator.com/item?id=38579899)
[Pluralistic: "If buying isn't owning, piracy isn't stealing" (08 Dec 2023) - Pluralistic: Daily links from Cory Doctorow](https://pluralistic.net/2023/12/08/playstationed/#tyler-james-hill)

[We need to talk about digital ownership](https://www.citationneeded.news/we-need-to-talk-about-digital-ownership/)

['Adam Ruins Everything' Star Suggests BitTorrent as an Option to Watch the Series * TorrentFreak](https://torrentfreak.com/adam-ruins-everything-star-suggests-bittorrent-as-an-option-to-watch-the-series-240605/)
- it becomes a problem when the creator hates IP regulations

[Cheaper Prices Reduce Indirect Visits to Pirate Sites, Research Finds * TorrentFreak](https://torrentfreak.com/cheaper-prices-reduce-indirect-visits-to-pirate-sites-research-finds-240609/)
- people pay what they feel gives value, at the rate they want to pay
- PWYW fixes the entire thing, or maybe a Vickery auction

[Internet Archive forced to remove 500k books after publishers' court win | Hacker News](https://news.ycombinator.com/item?id=40754229)
[Internet Archive forced to remove 500,000 books after publishers’ court win | Ars Technica](https://arstechnica.com/tech-policy/2024/06/internet-archive-forced-to-remove-500000-books-after-publishers-court-win/)

[488: Steal This Comic - explain xkcd](https://www.explainxkcd.com/wiki/index.php/488:_Steal_This_Comic)

[Taking Pirated Copies Offline Can Benefit Book Sales, Research Finds * TorrentFreak](https://torrentfreak.com/taking-pirated-copies-offline-can-benefit-book-sales-research-finds-240804/)

## torrent client - go

[Building a BitTorrent client from the ground up in Go (2020) | Hacker News](https://news.ycombinator.com/item?id=33495328)
[Building a BitTorrent client from the ground up in Go | Jesse Li](https://blog.jse.li/posts/torrent/)

## torrent client - rtorrent

[rTorrent Community wiki](https://github.com/rtorrent-community/rtorrent-community.github.io/wiki)
GitHub wiki for rTorrent.

## TorrentFreak (RSS)

[Movie Companies Take DMCA Subpoena ‘Shortcut’ Dispute to Court of Appeals – TorrentFreak](https://torrentfreak.com/movie-companies-take-dmca-subpoena-shortcut-dispute-to-court-of-appeals-240916/)

[Fake Streams 'Save' Premier League Pirates, Security Tips Can Save More * TorrentFreak](https://torrentfreak.com/fake-streams-save-premier-league-pirates-security-tips-can-save-more-240917/)
[ISPs Back Cox's Supreme Court Petition to Counter "Extortionate" Piracy Liability Pressure * TorrentFreak](https://torrentfreak.com/isps-back-coxs-supreme-court-petition-to-counter-extortionate-piracy-liability-pressure-240917/)

[Pirating "The Pirate Bay" TV Series is Ironically Difficult (Updated) * TorrentFreak](https://torrentfreak.com/pirating-the-pirate-bay-tv-series-is-ironically-difficult-241108/)

[IFPI: Stream-Ripping Fuels Generative AI From Which Existential Threats Emerge * TorrentFreak](https://torrentfreak.com/ifpi-stream-ripping-fuels-generative-ai-from-which-existtential-threats-emerge-241229/)

[MAME Devs Spent 628 Years Cracking Protection on 712 Retro Games * TorrentFreak](https://torrentfreak.com/mame-devs-spent-628-years-cracking-protection-on-712-retro-games-250118/)

[Pirate Libraries Are Forbidden Fruit for AI Companies. But at What Cost? * TorrentFreak](https://torrentfreak.com/pirate-libraries-are-forbidden-fruit-for-ai-companies-but-at-what-cost-250131/)

[Ad-Funded Piracy's 'Biggest Open Secret' Revealed By Researcher * TorrentFreak](https://torrentfreak.com/ad-funded-piracys-biggest-open-secret-revealed-by-researcher-250308/)

## torrent hosting

[Shutting down my legal torrent site after 17 years | Hacker News](https://news.ycombinator.com/item?id=35639370)
[Legit Torrents - Legal Torrents, Free Media](https://www.legittorrents.info/)

## torrent search engine - private trackers

[What are private trackers and how to get started](https://www.reddit.com/r/Piracy/wiki/guides/private_trackers)

[Private trackers - InstallGentoo Wiki](https://wiki.installgentoo.com/index.php/Private_trackers)

[A Simple Guide To A Better Ratio](https://www.reddit.com/r/trackers/comments/fthja/a_simple_guide_to_a_better_ratio/)
A good tracker requires you to upload what you download. This guide explains many of the methods involved with keeping on top of this sometimes difficult task.

[Frequently Asked Questions : trackers](https://old.reddit.com/r/trackers/comments/51ay9n/frequently_asked_questions/)

## usenet

[r/usenet - Usenet Discussion](https://old.reddit.com/r/usenet/)
A thriving community dedicated to helping users old and new understand and use Usenet.
[Getting started with usenet /r/usenet wiki](https://www.reddit.com/r/usenet/wiki/index)
[r/Usenet wiki: indexers](https://www.reddit.com/r/Usenet/wiki/indexers)
[Indexer List](https://www.reddit.com/r/usenet/wiki/indexers#wiki_free_membership_sites)
Information about /r/Usenet's favourite indexing services.
[Usenet Invite Requests and Offers](https://old.reddit.com/r/UsenetInvites/)
requests and offers for Usenet indexers.

[NZBLNK™ specification](https://nzblnk.info/)
The NZBLNK™ URI scheme defines the format of NZBLNK™ links to identify binary Usenet content and supplies some extra information to handle that content correct (similar to magnet links, but for NZBs).

## widevine

["Widevine Dump": Leaked Code Downloads HD Video from Disney+, Amazon, and Netflix | Hacker News](https://news.ycombinator.com/item?id=29702110)
['Widevine Dump": Leaked Code Downloads HD Video from Disney+, Amazon, and Netflix * TorrentFreak](https://torrentfreak.com/widevine-dump-leaked-code-downloads-hd-video-from-disney-amazon-and-netflix-211227/)

## AwesomeP

### Background Information

 [Wikipedia "File sharing" category](https://en.wikipedia.org/wiki/Category:File_sharing)
Wikipedia's full list of file-sharing related articles.

### Contents

 VPNs
  * VPN Guides and Tutorials
  * VPN Subscription Services
  * Self-hosted VPNs
 Browser Extensions
 Userscripts
 Password Vaults
 Antivirus
 Privacy
  * Windows 10 Privacy
 Email
 Operating Systems
 Decentralised Networks
 Domain Names
 Torrenting
  * Trackers
    * Private Trackers
    * Semi-Private Trackers
    * Public Trackers
  * Tracker Aggregators
  * Tracker Proxies
  * Tracker Invites
  * Torrent Clients
  * * Deluge
    * rTorrent
    * WebTorrent Clients
  * autodl-irssi
  * Seedboxes
    * Web-based Cloud Seedboxes
    * Seedbox Hosting Providers
    * Seedbox Setup Tools and Guides
  * Tracker Frameworks
 Usenet
  * Usenet Providers
  * Usenet Indexers
    * Usenet Indexing Software
    * Paid Indexers
    * Free Indexers
  * Usenet Clients
 Direct Downloads
  * Download Managers
  * DDL Tools
  * Custom Google Search Engines
  * FTP Indexers
  * DDL Search Engines and Crawlers
  * DDL Link Sites
  * Premium Link Generators
  * Premium Link Hosts
  * Open Directories
  * Streaming Sites
    * HD Streaming
    * Big Media Libraries
    * TV
    * Anime
    * Cartoons
    * Sports Streaming
    * Specialty Sites
    * Openload Hosts
 Media Centre Applications
 Stremio
 Plex
  * Plex Plugins
  * Plex Requests
  * Plex Scripts and Tools
  * Plex Shares
  * Plex Transcoding
  * Plex Logging and Metrics
  * Plex Clients
 Kodi
 Gaming
  * Repacks
  * ROMs
  * Console Games
  * Homebrew and Custom Firmware
 Music
  * Music Streaming
  * Music Downloading
  * Spotify
  * iTunes
 Software
 Ebooks
 Magazines
 Academic Papers and Material
 Textbooks
 Courses and Tutorials
 Audiobooks
 Comicbooks
 Manga
 Documentaries
 Fonts, Icons and Graphics
 Automation
  * TV Automation
  * Movie Automation
  * Music Automation
  * Subtitles Automation
 P2P Networks
 Ripping, Transcoding, Converting, Encoding
 Cloud Storage
 File Renaming and Tagging
 Mobile Apps
  * Streaming Apps
  * Torrent Apps
  * APKs
 Discord Servers
 IPTV and DVR
  * Acestreams
 IRC
  * IRC Clients
  * IRC Networks
  * IRC Search Engines
 DC++
 Full Movies On
 Piracy Blogs and News
 Content Discovery
  * PreDB Sites
    [Urban Dictionary: predb](https://www.urbandictionary.com/define.php?term=predb)
    Urban Dictionary definition.

 Dashboards and Homepages
 Proxy Sites
 File Sharing Tools
 Stream Synchronisation
 Telegram Piracy
 Miscellaneous

---

it's worth noting that the piracy community is COMPLETELY indiscriminate

- there's a bit of an anarchic vibe to it all

## How to block Ads and Trackers for free on iOS, MAC OS & Android

iOS 14+

  Visit [AhaDNS Blitz](https://blitz-setup.ahadns.com/) using Safari.

  Tick all the options you want.

  After selecting the options click on Download Apple mobileconfig button.

  Click allow when the pop up appears.

  Go to Settings > General > VPN, DNS & Device Management.

  Click on Downloaded Profile.

  Click on AhaDNS Blitz.

  Click on Install.

  Enter passcode if you have.

  Click Next.

  Click Install.

  Click Install when the popup appears.

  Enjoy System wide ad blocking on iOS!

Android

  Visit [AhaDNS Blitz](https://blitz-setup.ahadns.com/) using any browser.

  Tick all the options you want.

  After selecting the options click on Copy URL button.

Or you can use our URL https://blitz.ahadns.com/1:1.4.7.8.17

  Download [Nebulo DNS](https://play.google.com/store/apps/details?id=com.frostnerd.smokescreen&hl=en&gl=US) app.

  Open app.

  Select DNS over HTTPS.

  Click on server button.

  Click on add server.

  Enter the copied URL from bullet point 3 of this guide.

  Disable battery optimization for Nebulo app in Android settings.

  Make sure to enable always on for Nebulo in Android VPN settings.

  Enjoy System wide ad blocking on Android!

MAC OS

  The steps for Mac OS are similar to iOS.

  Press "Allow" if asked to allow download of mobileconfig file above.

  Double-click the downloaded mobileconfig file.

  You should now get a pop-up telling you to review the profile in System Preferences.

  Go to System Preferences → Profiles.

  Enable the downloaded profile.

  Done! You're now using encrypted DNS over HTTPS in all your networks.

## general piracy guides

[The Complete Guide to Building Your Own Personal Streaming Service Powered by Docker and Plex](https://www.reddit.com/r/Piracy/comments/ma1hlm/the_complete_guide_to_building_your_own_personal/)
Guide by u/WhereIsYourMind

[GitHub - hijoput4/RealPiracy: FAL (Frequently Asked Links) list so you stop asking these everywhere. It covers 99% your internet needs.](https://github.com/hijoput4/RealPiracy)

[pirate-haven.github.io/](https://pirate-haven.github.io/)

[redacted Interview Prep - Welcome](https://interviewfor.red/en/index.html)

[Reddit](https://www.reddit.com/r/Piracy/comments/6583hl/piracy_megathread_v20/)
Piracy Megathread on reddit

[How to become a pirate archivist | Hacker News](https://news.ycombinator.com/item?id=33240701)
[How to become a pirate archivist - Anna's Blog](https://annas-blog.org/blog-how-to-become-a-pirate-archivist.html)

[Champagne Piracy Wiki - Champagne.](https://champagne.pages.dev/)

[SnakeWarez](https://pilssken.neocities.org/warez/)
Pirate Links

[Home • Wiki](https://megathread.pages.dev/)
Pirate Links

## history

[Napster sparked a file-sharing revolution 25 years ago | Hacker News](https://news.ycombinator.com/item?id=40545436)
[Napster Sparked a File-Sharing Revolution 25 Years Ago * TorrentFreak](https://torrentfreak.com/napster-sparked-a-file-sharing-revolution-25-years-ago-250601/)

## naming


### How do I correctly archive my files? (PC)

If you put files onto MEGA or any other file site without first .rar'ing them and changing their name, they'll most likely be deleted very quickly. Here's how to protect your files correctly:

    Use WinRAR

    You can use alternatives (7-Zip and Win-Zip are popular) but this guide will specifically address WinRAR.

    Using 7-Zip will create .7z files. Newer versions of WinRAR can open these but some older versions cannot and may cause headaches for the community.
    Right click on the file or folder (depending on the type of file you're archiving) and select "Add to archive..."
    First, change the "Archive name" to something inconspicuous.

    Many users title their archives something clever having to do with the file or just the initials of the file.

    Community.S02E03.rar is NOT an acceptable archive name, for example.

    Please keep your file names discreet and your archives password protected for the safety of the site and yourself.
    Next, click the "Advanced" tab and selected the "Set password..." option.

    This is where you will type the password for the file. Now select the box titled "Encrypt file names".

    This makes sure you cannot see the files inside the archive without first entering the password.
    If your file is large (1GB+), you may want to split it into multiple files so users can more easily download it. MEGA seems to have some trouble uploading and downloading large files. Select a file size that works well for you.

    Under the "Split to volumes, size", input your desired file size. Be sure to select the correct unit for your file size (usually MB).
    Click "OK" and you should be good to go.
    If you click "Mode" you can change this to "Fastest". This changes the compression mode.

    Most files (movies and music) don't allow for much compression so your rar file size is going to be almost the same size as the original file.

    Clicking "Fastest" should decrease the time your computer spends archiving the files.
    If you do choose to break your file up into multiple parts, your file will be made with the same file name, each appended with a different part number.

    For example: O12-7.part1.rar, O12-7.part2.rar

    All part files will need to be present before the file can be fully extracted.

How do I correctly archive my files? (MacOS)

Use LueRAR2 or BetterZip
Do my files need to be password protected?

Yes. Archiving files without a password allows the possibility of people outside the site gaining access to your files. If they find something they like, they may link it on a more public platform. This may cause the file to get flagged and in turn, your MEGA account to get flagged. It's another layer of security and it takes so little time to add, it's not worth not doing it.
What should the password on my file be?

## p2p networks

[mafintosh/awesome-p2p: List of great p2p resources](https://github.com/mafintosh/awesome-p2p)

## Piracy-Rules

### /r/Piracy Rules

#### 1. Submissions must be related to the discussion of digital piracy

1a. No low effort submissions such as sharing seeding ratio screenshots are permitted.

#### 2. No spam, trading, selling, or blatant self-promotion posts

2a. No begging for invites to private sites, requesting for others to download content for you, requesting activation keys, etc.

2b. No dealing "cracked" (read: stolen) accounts or request for sites that do so

2c. Any monetary services are not allowed.

#### 3. Do not request for specific pirated titles (ie. a specific movie, book title, software title, etc.); do not link to pirated content. [Why?](https://www.reddit.com/r/piracy/wiki/subfaq)

3a. You may ask generalized questions such as "Where can I find 4K movies, children's books, sci-fi books, etc.". You may not name a specific work's title in your content request.

3b. Do not link to specific pirated media. You may link to the top level of a site, eg. <https://1337x.to> but never to a specific pirated release, eg. <http://1337x.to/specific-movie-torrent>

3c. Do not encourage rule breaking by asking which specific title someone is looking for when they make a request

#### 4. Redundant questions that have been previously answered will be removed

Do a custom search via google, example: `where to find cracked apps site:reddit.com/r/piracy`

#### 5. Do not direct-message moderators for help with your issues. Either message the mod team if relevant, or make a post on the sub as normal

Set the recipient as /r/piracy to message the mod team instead of direct-messaging a particular mod

## Privatebin

[Free Books : Download & Streaming : eBooks and Texts : Internet Archive](https://archive.org/details/texts)
(Public domain books only)

[Balder Ex-Libris](https://balderexlibris.com/)

Guides & Megathreads:

[Guide: The idiot proof guide to downloading ebooks off IRC. With Pictures and everything! : Piracy](https://old.reddit.com/r/Piracy/comments/2oftbu/guide_the_idiot_proof_guide_to_downloading_ebooks/)

[Apprentice Alf's Blog | Everything you ever wanted to know about DRM and ebooks, but were afraid to ask.](https://apprenticealf.wordpress.com/)
(Info about DRMs)

Search engines:

Finding books using Google without a custom search engine (for easier to find books):

Use this format:
[title]:[type]
Or
The most common e-book types are .pdf, .epub, and .mob (in that order)

## 00 TT Torrent - How To Proxy 'Any' Website Using Cloudflare Workers

  1. _Sign_ up on <https://www.cloudflare.com/> if not already.
  2. _Click_ on workers tab.
  3. _Choose_ a subdomain where you would like to see your workers.
such as [zyx.subdomain.workers.dev](http://zyx.subdomain.workers.dev)
here zyx will be replaced by your future worker names.
the subdomain will stay same
  4. _After_ selecting subdomain click on create a service/worker.
  5. _Name_ your new worker anything you want.
  6. _Click_ create.
  7. _Click_ quick edit.
  8. _Click_ next.
  9. _Delete_ existing code.
  10. _Paste_ the following code there.

   async function handleRequest(request) {
  const url = new URL(request.url)
  if (url.hostname in ORIGINS) {
const target = ORIGINS[url.hostname]
url.hostname = target
return fetch(url.toString(), request)
  }
  return fetch(request)
}
addEventListener('fetch', event => {
  event.respondWith(handleRequest(event.request))
})
const ORIGINS = {
  '1337x.subdomain.workers.dev': '1337x.to'
}

> Replace 1337x with whatever you named your new worker.
>
> Replace [1337x.to](http://1337x.to) with the website you want to be proxied.
>
> Don't enter <https://1337x.to/>
>
> Only [1337x.to](http://1337x.to)
>
>
>

   BOOM you can access your proxied website at [1337x.subdomain.workers.dev](http://1337x.subdomain.workers.dev)

Enjoy and cheers!

Not all websites can be proxied. Either because the websites don't want to be proxied or because can't be proxied through cloudflare workers or because cloudflare itself doesn't support them.

Leaving some sample workers. Feel free to use them.

<https://1337x.unban.workers.dev>

<https://scrolller.unban.workers.dev>

## DC++

NOTE: WILL PROBABLY NEED TO MAKE A NOD TO THIS AND IRC

[Direct Connect (protocol)](https://en.wikipedia.org/wiki/Direct_Connect_(protocol))
Wikipedia page describing Direct Connect.

[DC++](https://en.wikipedia.org/wiki/DC%2B%2B)
Wikipedia page describing DC++

## encoding and ripping

[AHD's Encoding Guide](https://encoding-guide.neocities.org/)
An in-depth guide on video encoding.

[Audio ripping guides](https://captainrookie.com/)

[Video Encoding Guides](https://sometimes-archives-things.github.io/archived-things/)
Learn how to Encode Videos

[Simple x264 Encoding Guide for Handbrake](https://sometimes-archives-things.github.io/archived-things/ptp_guides/Simple-x264-Encoding-Guide-for-Handbrake-\(Mar-13\).html)

[The HANDJOB Guide to BluRay Encodes for Mac \(Beginner Friendly\)](https://sometimes-archives-things.github.io/archived-things/ptp_guides/The-HANDJOB-Guide-to-BluRay-Encodes-for-Mac-\(Beginner-Friendly\).html)

[Basic HANDJOB encoding guide](https://sometimes-archives-things.github.io/archived-things/ptp_guides/The-HANDJOB-Guide.html)

[Full encoding and Ripping Archive](https://sometimes-archives-things.github.io/archived-things/)

## How To Deploy A Mirror Bot On Heroku Using CLI

PRERQUISTIES GETTING CREDENTIALS.JSON

  Visit the [Google Cloud Console](https://console.developers.google.com/apis/credentials)

  Make sure you're using the right google account, if you're not, change it first. After that, press Create Project.

!https://i.ibb.co/qR898VX/437855c1a33e2960574c8-1.png

  Name it whatever and press Create (This is using edu mail here so the organization is present. If you're using normal gmail, just set the organization to No organization).

!https://i.ibb.co/qrLGg4w/1d2616afab1d4f4f17241-2.png

  Go to the OAuth Consent tab

  Press external, and press Create

  Fill app name whatever you want

  Fill User support email and developer contact information with your google account, and ignore other configs. Press Save and Continue.

!https://i.ibb.co/t2fQJdJ/b0771f7a256a3cdac402b-3.png

!https://i.ibb.co/MpJTK1q/9d16b42d6115cd06eb88c-7.png

  Skip the scopes step

  Add your google account as tester, press Save and Continue.

!https://i.ibb.co/kGpmxf1/26cb4c6c8d7698a0acd0b-4.png

  Press back to dashboard

  Press Credentials tab > Create Credentials > OAuth client ID.

!https://i.ibb.co/pLDbcfZ/f7aa5ad039c5411b22a45-5.png

  Select Desktop and name it whatever you want

  This will appear, download it.

!https://i.ibb.co/g7BRP17/bacb6937e4fa55c242bc5-6.png

  Rename the downloaded file to credentials.json

PRERQUISTIES GETTING TOKEN.PICKLE

  Visit [Google API page](https://console.developers.google.com/apis/library)

  Search for drive

  Press Google Drive API and enable it.

  Install Python from [here](https://www.python.org/downloads/windows/)

Use the Windows installer (64-bit)

  Install GIT from [here](https://git-scm.com/download/win)

Use the 64-bit Git for Windows Setup.

  Install Heroku CLI from [here](https://cli-assets.heroku.com/heroku-x64.exe)

Make sure to add both Python and GIT to PATH during the installation. The option is present during installation. Just remember to select it.

  Create a folder called BOTS on your PC.

  Navigate to File Explorer address bar while you are inside the folder.

  Delete existing entry.

  Type cmd and hit enter.

  This will open a CMD prompt window.

  Type pip install google-api-python-client google-auth-httplib2 google-auth-oauthlib and hit enter.

  Copy and paste git clone https://github.com/anasty17/mirror-leech-telegram-bot mirrorbot/ && cd mirrorbot

  This will clone the repo and make a folder on your PC called mirrorbot.

  Copy the credentials.json file which you had generated and downloaded earlier and paste it into the mirrorbot folder.

  Go back to CMD window which is opened and type python3 generate_drive_token.py and hit enter.

  It will show you a URL. Copy the URL and paste it inside a browser and open it.

  Follow the steps inside browser and accept everything.

  You'll get your authorization code. Copy that and paste inside terminal and press enter.

!https://i.ibb.co/Mpr9DXb/b06c5e6547aadf8b88a3d-10.png

  Your token.pickle will be generated and can be found inside mirrorbot folder.

PRERQUISTIES GENERATING SERVICE ACCOUNTS

  To generate service accounts, go back to CMD and paste the following and hit enter.

1
2

python -m pip install progress
python3 gen_sa_accounts.py --quick-setup 1 --new-only

  Copy the link and open it in a new tab, connect it to your google account, and paste the authorization code you just got.

!https://i.ibb.co/gyP35kt/1086509163ef4057cdc45-12.png

  You're bound to get this error since it's the first time you're making service accounts with that google account. Copy the link after Enabling it by visiting and opening it in a new tab.

!https://i.ibb.co/j4XpxZh/ee52ba6628d28f4a4f785-13.png

  Enable it.

!https://i.ibb.co/61XtmgD/1f2c4f47a8c2a411de9d7-14.png

  To generate service accounts, go back to CMD and paste the following and hit enter.

1

python3 gen_sa_accounts.py --quick-setup 1 --new-only

  Wait and you'll get an accounts folder with all the service accounts credentials files. It is recommended to add all the service accounts to a Google Group. You can then add the google group to your team drive which you will be using for the mirror bot.

  Open the config.env file inside mirrorbot folder with Notepad and insert your values.

Namely:

  BOT TOKEN The Telegram Bot Token that you got from [@BotFather](https://t.me/BotFather).

  GDRIVE FOLDER ID The folder ID where you will be storing the mirrored files. It is the thing which comes after folders/ in a Google Drive URL. Here the folder ID will be 1XBSIksifdei322xxxxxxx <https://drive.google.com/drive/u/0/folders/1XBSIksifdei322xxxxxxx>

  OWNER ID The Telegram User ID (not username) of the Owner of the bot. Get it from [userinfobot](https://t.me/userinfobot)

  TELEGRAM_API This is to authenticate your Telegram account for downloading Telegram files. You can get this from <https://my.telegram.org>.

  TELEGRAM_HASH This is to authenticate your Telegram account for downloading Telegram files. You can get this from <https://my.telegram.org>.

  AUTHORIZED_CHATS Fill user_id and chat_id of groups/users you want to authorize. Separate them by space. Get it from [userinfobot](https://t.me/userinfobot)

  SUDO_USERS Fill user_id of users whom you want to give sudo permission. Separate them by space.

  BASE_URL_OF_BOT For Heroku fill <https://yourappname.herokuapp.com>

  SEARCH_API_LINK Search api app link. Get your api from deploying this [repository](https://github.com/Ryuk-me/Torrent-Api-py).

[MEGA](../../NOTES/mega.md)

 Here is how your config.env should look like, with your values filled where necessary:

```
 1
 2
 3
 4
 5
 6
 7
 8
 9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85
86
87
88
89
90

# REQUIRED CONFIG
BOT_TOKEN = ""
GDRIVE_FOLDER_ID = ""
OWNER_ID =
DOWNLOAD_DIR = "/usr/src/app/downloads"
DOWNLOAD_STATUS_UPDATE_INTERVAL = 5
AUTO_DELETE_MESSAGE_DURATION = 20
IS_TEAM_DRIVE = "True"
TELEGRAM_API =
TELEGRAM_HASH = ""
# OPTIONAL CONFIG
DATABASE_URL = ""
AUTHORIZED_CHATS = ""
SUDO_USERS = ""
IGNORE_PENDING_REQUESTS = "False"
USE_SERVICE_ACCOUNTS = "True"
INDEX_URL = ""
STATUS_LIMIT = "4"
STOP_DUPLICATE = ""
CMD_INDEX = ""
UPTOBOX_TOKEN = ""
TORRENT_TIMEOUT = "900"
EXTENTION_FILTER = ""
INCOMPLETE_TASK_NOTIFIER = "True"
# Update
UPSTREAM_REPO = ""
UPSTREAM_BRANCH = ""
# Leech
TG_SPLIT_SIZE = ""
AS_DOCUMENT = ""
EQUAL_SPLITS = ""
CUSTOM_FILENAME = ""
# qBittorrent
BASE_URL_OF_BOT = ""
SERVER_PORT = ""
WEB_PINCODE = ""
QB_SEED = ""
# Rss
RSS_DELAY = ""
RSS_COMMAND = ""
RSS_CHAT_ID = ""
USER_STRING_SESSION = ""
# Pivate Files
ACCOUNTS_ZIP_URL = ""
TOKEN_PICKLE_URL = ""
MULTI_SEARCH_URL = ""
YT_COOKIES_URL = ""
NETRC_URL = ""
# Mega
MEGA_API_KEY = ""
MEGA_EMAIL_ID = ""
MEGA_PASSWORD = ""
# Shortener
SHORTENER = ""
SHORTENER_API = ""
# GDTOT COOKIE
CRYPT = ""
# Size Limits
TORRENT_DIRECT_LIMIT = ""
ZIP_UNZIP_LIMIT = ""
CLONE_LIMIT = ""
MEGA_LIMIT = ""
STORAGE_THRESHOLD = ""
# Buttons
VIEW_LINK = ""
BUTTON_FOUR_NAME = ""
BUTTON_FOUR_URL = ""
BUTTON_FIVE_NAME = ""
BUTTON_FIVE_URL = ""
BUTTON_SIX_NAME = ""
BUTTON_SIX_URL = ""
# Torrent Search
SEARCH_API_LINK = ""
SEARCH_LIMIT = ""
SEARCH_PLUGINS = '["https://raw.githubusercontent.com/qbittorrent/search-plugins/master/nova3/engines/piratebay.py",
   "https://raw.githubusercontent.com/qbittorrent/search-plugins/master/nova3/engines/legittorrents.py",
   "https://raw.githubusercontent.com/qbittorrent/search-plugins/master/nova3/engines/limetorrents.py",
   "https://raw.githubusercontent.com/qbittorrent/search-plugins/master/nova3/engines/torrentscsv.py",
   "https://raw.githubusercontent.com/qbittorrent/search-plugins/master/nova3/engines/zooqle.py",
   "https://raw.githubusercontent.com/qbittorrent/search-plugins/master/nova3/engines/eztv.py",
   "https://raw.githubusercontent.com/MaurizioRicci/qBittorrent_search_engines/master/kickass_torrent.py",
   "https://raw.githubusercontent.com/MaurizioRicci/qBittorrent_search_engines/master/yts_am.py",
   "https://raw.githubusercontent.com/MadeOfMagicAndWires/qBit-plugins/master/engines/linuxtracker.py",
   "https://raw.githubusercontent.com/MadeOfMagicAndWires/qBit-plugins/master/engines/nyaasi.py",
   "https://raw.githubusercontent.com/LightDestory/qBittorrent-Search-Plugins/master/src/engines/ettv.py",
   "https://raw.githubusercontent.com/LightDestory/qBittorrent-Search-Plugins/master/src/engines/glotorrents.py",
   "https://raw.githubusercontent.com/LightDestory/qBittorrent-Search-Plugins/master/src/engines/thepiratebay.py",
   "https://raw.githubusercontent.com/nindogo/qbtSearchScripts/master/magnetdl.py",
   "https://raw.githubusercontent.com/khensolomon/leyts/master/yts.py"]'

  After editing the config.env and adding your values do Ctrl+S to save the file.

  Go back to the open CMD window.

  Now copy/paste git checkout heroku and hit enter.

  Now copy/paste git add . -f and hit enter.

  Now copy/paste the following two lines and hit enter.

1
2

git config --global user.email "any random email address"
git config --global user.name "any random name"

  Now copy/paste git commit -m token and hit enter.

  Now copy/paste heroku login and hit enter.

Follow the on screen instructions.

  Now copy/paste heroku create --region us YOURAPPNAME and hit enter.

Replace YOURAPPNAME with whatever you will like your mirrorbot app on heroku to be called.

  Now copy/paste heroku git:remote -a YOURAPPNAME and hit enter.

Replace YOURAPPNAME with the heroku app name you picked in previous step.

  Now copy/paste heroku stack:set container and hit enter.

  Now copy/paste git push heroku heroku:master -f and hit enter.

YOUR BOT SHOULD BE DEPLOYED SHORTLY!

BOT COMMANDS TO BE SENT TO [@BotFather](https://t.me/BotFather)

  Use /setcommands

 1
 2
 3
 4
 5
 6
 7
 8
 9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32

mirror Mirror
qbmirror Mirror torrent using qBittorrent
clone Copy file/folder to Drive
watch Mirror yt-dlp supported link
status Get Mirror Status message
search Search for torrents with API
stats Bot Usage Stats
cancel Cancel a task
cancelall Cancel all tasks
count Count file/folder of Drive
restart Restart the Bot
zipmirror Mirror and upload as zip
unzipmirror Mirror and extract files
qbzipmirror Mirror torrent and upload as zip using qb
qbunzipmirror Mirror torrent and extract files using qb
leech Leech
zipleech Leech and upload as zip
unzipleech Leech and extract files
qbleech Leech torrent using qBittorrent
qbzipleech Leech torrent and upload as zip using qb
qbunzipleech Leech torrent and extract using qb
zipwatch Mirror yt-dlp supported link as zip
leechwatch Leech through yt-dlp supported link
leechzipwatch Leech yt-dlp support link as zip
leechset Leech settings
setthumb Set thumbnail
list Search files in Drive
del Delete file/folder from Drive
log Get the Bot Log
shell Run commands in Shell
ping Ping the Bot
help All cmds with description
```

## IPFS

[IPFS Distributed Web](https://en.wikipedia.org/wiki/InterPlanetary_File_System)
Peer-to-peer distributed file system that seeks to connect all computing devices with the same system of files.

[GitHub - ipfs/awesome-ipfs: Community list of awesome projects, apps, tools, pinning services and more related to IPFS.](https://github.com/ipfs/awesome-ipfs)
IPFS Resource Index

[Luke Gloege, Ph.D.](https://betterprogramming.pub/a-guide-to-hosting-websites-on-ipfs-d2efad40ed3)
(2022) A Guide to Hosting Websites on IPFS
How to host a site on the Inter-Planetary File System

## IPTV and m3u

[Latest M3U Playlist URL Free And How To Use Them Easily](https://www.techtoreview.com/top-picks/m3u-playlist-url.html)

## jailbreaking apple - activator

[Here's some Activator Action workflows for those with jailbroken devices. Requires Activator to be installed from Cydia.](https://old.reddit.com/r/workflow/comments/3p3qn0/heres_some_activator_action_workflows_for_those/)

[[Discussion] What clever activator actions do you have setup? : jailbreak](https://old.reddit.com/r/jailbreak/comments/54u6w8/discussion_what_clever_activator_actions_do_you/)

[[Question] Running commands in Activator : jailbreak](https://old.reddit.com/r/jailbreak/comments/44u56d/question_running_commands_in_activator/)

[[Question] What's wrong with my activate command / Activator ? Can someone with some programming experience have a look. : jailbreak](https://old.reddit.com/r/jailbreak/comments/4zl9r9/question_whats_wrong_with_my_activate_command/)

[[Discussion] Learning Shell commands to do more with activator : jailbreak](https://old.reddit.com/r/jailbreak/comments/53hjdm/discussion_learning_shell_commands_to_do_more/)

[[Question] How to run an app in background with activator command when the device is locked? : jailbreak](https://old.reddit.com/r/jailbreak/comments/50mudn/question_how_to_run_an_app_in_background_with/)

## jailbreaking apple

[How to jailbreak iOS 9.3.3 with Pangu [tutorial]](http://www.idownloadblog.com/2016/07/24/how-to-jailbreak-ios-9-3-3-pangu)

[How to tweak your iPhone, iPad or iPod Touch without jailbreaking | CONATH](http://conath.me/2016/01/tweak-iphone-without-jailbreaking)

[What is the jailbreak for iOS 9.3.3 actually doing? - Part 1 - Nettitude Labs](https://labs.nettitude.com/blog/what-is-the-jailbreak-for-ios-9-3-3-actually-doing-part-1)

[Jailbreak-Update-zz/jailbreak-update.github.io: This is a dedicated repository for jailbreak and other iPhone related projects.](https://github.com/Jailbreak-Update-zz/jailbreak-update.github.io)

[Danniez/cydia: Cydia is an alternative to Apple's App Store for "jailbroken" devices, at this time including iPhones, iPads, and iPod Touches, specializing in the distribution of all that is not an "app".](https://github.com/Danniez/cydia)

[Arcane is a simple script designed to backdoor iOS packages (iphone-arm) and create the necessary resources for APT repositories.](https://hakin9.org/arcane-is-a-simple-script-designed-to-backdoor-ios-packages-iphone-arm-and-create-the-necessary-resources-for-apt-repositories/)

[Control iOS From the Command Line](https://www.technorms.com/25404/control-ios-from-command-line)

[[Tutorial] Executing terminal commands, with Filza and without a Mobile Terminal. : jailbreak](https://old.reddit.com/r/jailbreak/comments/pfafuq/tutorial_executing_terminal_commands_with_filza/)

## remove music drm

[How to Remove DRM From iTunes Movies and TV Shows](https://www.howtogeek.com/291612/how-to-remove-drm-from-itunes-movies-and-tv-shows/)
HowToGeek article on how to use TunesKit and Requiem.

## How To Sideload Unlimited Apps/IPAs Which Never Expire NO JAILBREAK [iOS 14 15.4.1 Only]

JAILED PERMASIGNED APP INSTALLER iOS 14 15.4.1

An app has been released which allows you to install or sideload unlimited IPA's and the best thing is they will never expire unlike with AltStore and Sideloadly.

[TrollStore Release Post On Reddit](https://old.reddit.com/r/jailbreak/comments/x44cpj/free_release_trollstore_jailed_permasigned_app/)

[CyPwn](https://ipa.cypwn.xyz/)
Get IPA's here as well.

[Get IPA's/Apps to install using TrollStore here!](https://ipa.cypwn.xyz/trollstore/)
TrollStore specific apps.

[GitHub Releases](https://github.com/opa334/TrollStore/releases)

[Telegram Channel for IPAs #1](https://t.me/iapps_ipa)

[Telegram Channel for IPAs #2](https://t.me/Ed0ardoo)

[Anonfiles mirror of TrollInstaller 1.1](https://anonfiles.com/Xai0u5A4y2/TrollInstaller_ipa)

  Install Trollinstaller via services like
  [AltStore](https://altstore.io/)
  [Sideloadly](https://sideloadly.io/)
  etc.

  Open Trollinstaller, click on "Install" Button & wait for it to be finished.

  If your phone reboots here, go back to previous step.

  An alert should pop up when TrollStore installed successfully, click close and the app should exit.

  If TrollStore is on home screen, start it. If not, then reboot and it should appear afterwards. Then start it.

  Go into the settings tab, hit "Install ldid" so TrollStore can install unsigned apps.

  Tap "Install Persistence Helper" and choose a system app you don't need to use (e.g. Tips or Home) in the list that appears.

  Optional : You now may delete "Trollinstaller" app if you see "TrollStore" on your homepage.

  Next download or save an iPA file to be sideloaded on you iDevice.

Very Important

Save your iPA file in the "On My iPhone/iPad etc." storage and not in "iCloud Drive". Failing to do this step will probably result in failed iPA installation.

  Install the iPA Package by Opening the Share Sheet, and opening the file in "TrollStore".

  Profit.

Some cr@cked Cydia Repos:

[ReJail](https://rejail.ru/)

[HackYouriPhone](http://repo.hackyouriphone.org/)
[Julioverne](https://julio.hackyouriphone.org)
iOS Jailbreaking Tools
[How to add HackYouriPhone Repo in Cydia](http://repo.hackyouriphone.org/add)

[PandaHelper](https://apt.pandahelp.vip/)

## specific installation instructions

[Protecting yourself when downloading pirated content Guide concerning copyright infringement complaints](https://www.reddit.com/r/Piracy/wiki/faq/isp_complaints)

[How to install and activate Windows 10  Includes LTSB/LTSC](https://www.reddit.com/r/Piracy/wiki/guides/win10upgrade_activation)

[How to install and activate Office](https://old.reddit.com/r/Piracy/wiki/guides/office_activation)

[4K HDR Movies: A pirate's Guide](https://www.reddit.com/r/Piracy/comments/hvcozj/4k_hdr_movies_a_pirates_guide/)
Guide by u/lasttycoon

[Unlimited free Sirius XM for your car](https://www.reddit.com/r/Piracy/comments/c9bsz7/unlimited_free_sirius_xm_for_your_car/)
Guide by u/Itswillyferret

|[How to install Spectrasonics Omnisphere 2 [Windows Guide]](https://www.reddit.com/r/Piracy/comments/8khu8q/how_to_install_spectrasonics_omnisphere_2_windows/) | u/Kiicki | May 18, 2018 | Dec 5, 2018 |

## torrent client - rtorrent

[rTorrent Docs](https://rtorrent-docs.readthedocs.io/en/latest/)
Comprehensive manual and user guide for the rTorrent bittorrent client.

[rTorrent ArchWiki Page](https://wiki.archlinux.org/index.php/RTorrent)
Detailed article to answer most common questions about rTorrent.

## torrent

[BitTorrent - Wikipedia](https://en.wikipedia.org/wiki/BitTorrent)

[Build your own BitTorrent | Hacker News](https://news.ycombinator.com/item?id=37941075)
[Build your own BitTorrent | CodeCrafters](https://app.codecrafters.io/courses/bittorrent/overview)

## usenet

[Usenet](https://en.wikipedia.org/wiki/Usenet)
Usenet is a worldwide distributed discussion system available on computers.

[Usenet newsgroup](https://en.wikipedia.org/wiki/Usenet_newsgroup)
A Usenet newsgroup is a repository usually within the Usenet system, for messages posted from many users in different locations using the Internet.

[A Quick Guide to Choosing a Usenet Provider : usenet](https://old.reddit.com/r/usenet/comments/a7ffm7/a_quick_guide_to_choosing_a_usenet_provider/)
