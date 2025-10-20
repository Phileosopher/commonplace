
[How to Boost Web Performance with Prefetching – Improve User Experience by Reducing Load Time](https://www.freecodecamp.org/news/boost-web-performance-with-prefetching/)

[What are Pre-Rendering and Hydration in Web Development? A Deep Dive for Devs](https://www.freecodecamp.org/news/what-are-pre-rendering-and-hydration-in-web-dev/)

[How to Create a Meme Generator Using HTML Canvas](https://www.freecodecamp.org/news/create-meme-generator-using-html-canvas/)

[Understanding Modern Development Frameworks: A Guide for Developers and Technical Decision-makers](https://www.freecodecamp.org/news/understanding-modern-development-frameworks-guide-for-devs/)

[How to Build Scalable Access Control for Your Web App [Full Handbook]](https://www.freecodecamp.org/news/how-to-build-scalable-access-control-for-your-web-app/)

[How to Reverse Engineer a Website – a Guide for Developers](https://www.freecodecamp.org/news/how-to-reverse-engineer-a-website/)

## 0oldformat

OLD FORMAT:
1. history
2. browsers
3. domains
4. SEO
5. maintenance
6. app/web design

NEW FORMAT - WEB DEV:
1. hardware
2. IP address
5. maintenance (but the bulk is at [software redesign])
6. app/web design (but the bulk is at [UX/UI] for the design part and [software design] for the coding part)
7. social network design (with the bulk of it going back to [groups large] and [game theory])

NEW FORMAT - BROWSERS
1. history of browsers
2. requests
3. web domains and DNS (spinoff of [networks] and [protocols])
4. web search and SEO (connected with [marketing])
5. web browser features (but the bulk is at [software design] for general matters and JS, [graphics] for CSS)
6. website design/structure

CSS -> Graphics
JS -> Lang Comparisons (w/ Web Dev earmark)
SEO -> marketing

NOTE: most of the content on trendless.tech/web-dev goes to trendless.tech/browser


NEW NEW FORMAT:

WEB DEV
    file transfer -> TS CLOUD
    web hosting -> TS DISTRIBUTED SYSTEMS
    domains <- NETWORKING + PROTOCOLS
    search engines:making
BROWSER
    sitebuilders
    cms
    css/html -> TS UX/UI
    Tor browser <- P2P/TORRENT
    aesthetics -> TS UX/UI + NAG DESIGN
    seo -> NAG MARKETING
    search engines:using
SOCIAL NETWORKS
    social media feed algo <- ALGORITHMS
    social network design <-> AUTHENTICATION + DATABASES

browser
    BROWSER
cms
    BROWSER
css
    GRAPHICS
file hosting
    CLOUD
file transfer
    CLOUD
html
    BROWSER
sitebuilders
    BROWSER
Tor browser
    BROWSER
web scraping and archiving
    WEB DEV

## maintenance

NOTE: ADD CLARITY THAT WEB MONITORING IS NECESSARY FOR CONTINUED WEB DEV

NOTE: CLARIFY HOW A GOOD WEB DEV ABSOLUTELY NEEDS VARIOUS SAAS TO SAVE ON SANITY

## messaging apps

[Welcome to Libera Chat | Hacker News](https://news.ycombinator.com/item?id=27207734)
[Welcome to Libera Chat | Libera Chat](https://libera.chat/news/welcome-to-libera-chat)
- NOTE: MAY BE TIED TO FREENODE, WITH A FLOSS COMMUNITY?

## server access

[Show HN: How did your computer reach my server? | Hacker News](https://news.ycombinator.com/item?id=38531604)
[How Did I Get Here?](https://how-did-i-get-here.net/)
- the routes are different from server->client vs. client->server

## web hosting

I hadn't thought of a significant risk from the service provider that comes through the word "unlimited":

1. If a website provides unlimited storage+domains+sites+bandwidth, they can't fulfill that promise in any literal sense.
2. To offset that promise, they sell the product at a premium to the 80% Pareto distribution who _won't_ use the promised service to the fullest of its ability (e.g., what [insurance companies](https://notageni.us/insurance/) do).
    - reductionist e.g., if 20% of the users burn up $100/month in hosting needs, and the other 80% burn up $1/month, they break even at $20.80, meaning they'll sell it at $30/month and come out ahead.
3. As long as _many_ people use the product without taking full advantage of the "unlimited" service, things are fine.
4. However, if for whatever reason more people use that unlimited service, the pricing will have to change.
5. But, it's not always easy to compete with pricing, since _other_ hosting providers are promising the same thing, and migrating a hosted system isn't anywhere _near_ as much trouble as building it.
6. None of the solutions are great, and someone will be unhappy. Prices go up, covered services goes down, they go out of business, or some horrifying combination of the three.

There are 2 good workarounds to this Bad Marketing Promise:

1. Put a general hard limit, which allows their risk assessment to factor the cost and never worry about changing promises later (e.g., [Cloudways](https://www.cloudways.com/)). You can basically do what everyone else does, but it keeps you honest and you won't ruin the customers' lives later.
2. Charge per-item, per-piece, at a _very_ low profit margin (e.g., [NearlyFreeSpeech.NET](https://www.nearlyfreespeech.net/)). This requires your customers to be abnormally tech-savvy.

## 404 pages

[The Financial Times' 404 page | Hacker News](https://news.ycombinator.com/item?id=28980927)
[Application Error](https://www.ft.com/3lJQa6w)

## bots

[Botspam apocalypse | Hacker News](https://news.ycombinator.com/item?id=32339314)
[Botspam Apocalypse @ marginalia.nu](https://www.marginalia.nu/log/61-botspam-apocalypse/)

## CORS

[Cache your CORS | Hacker News](https://news.ycombinator.com/item?id=32907234)
[Cache your CORS, for performance & profit](https://httptoolkit.com/blog/cache-your-cors/)

[You don't need that CORS request | Hacker News](https://news.ycombinator.com/item?id=29777145)
[You don't need that CORS request - Nick Olinger](https://www.nickolinger.com/blog/2021-08-04-you-dont-need-that-cors-request/)

[How to win at CORS | Hacker News](https://news.ycombinator.com/item?id=28861944)
[How to win at CORS - JakeArchibald.com](https://jakearchibald.com/2021/cors/)

[Developers don't understand CORS | Hacker News](https://news.ycombinator.com/item?id=20404578)
[Developers don't understand CORS - Chris Foster](https://fosterelli.co/developers-dont-understand-cors)

## curl

[Twenty-five years of curl | Hacker News](https://news.ycombinator.com/item?id=35225946)
[twenty-five years of curl | daniel.haxx.se](https://daniel.haxx.se/blog/2023/03/20/twenty-five-years-of-curl/)

[The curl quirk that exposed Burp Suite & Google Chrome: netsec](https://www.reddit.com/r/netsec/comments/124oq9m/the_curl_quirk_that_exposed_burp_suite_google)

[Memory safe 'curl' for a more secure internet | Hacker News](https://news.ycombinator.com/item?id=24729218)
[rust in curl with hyper | daniel.haxx.se](https://daniel.haxx.se/blog/2020/10/09/rust-in-curl-with-hyper/)

[Curl on 100 Operating Systems | Hacker News](https://news.ycombinator.com/item?id=38273999)
[curl on 100 operating systems | daniel.haxx.se](https://daniel.haxx.se/blog/2023/11/14/curl-on-100-operating-systems/)

[Andrew Morton](https://drewish.com/2010/03/29/using-curl-and-the-host-header-to-bypass-a-load-balancer/)
(2010) Using cURL and the host header to bypass a load balancer
command line tips & tricks

[How we applied fuzzing techniques to cURL | Hacker News](https://news.ycombinator.com/item?id=39562467)
[How we applied advanced fuzzing techniques to cURL | Trail of Bits Blog](https://blog.trailofbits.com/2024/03/01/toward-more-effective-curl-fuzzing/)

## domains - DNS

[Paul Vixie, creator of the DNS protocol](https://old.reddit.com/r/dontyouknowwhoiam/comments/lum331/paul_vixie_creator_of_the_dns_protocol/)

[cjdns](https://github.com/cjdelisle/cjdns)
Cjdns (Caleb James DeLisle's Network Suite)
is a networking protocol and reference implementation, founded on the ideology that networks should be easy to set up.
- IS IT A DNS PROTOCOL? OR IS IT A DIFFERENT PROTOCOL ENTIRELY?

[DNS over Wikipedia | Hacker News](https://news.ycombinator.com/item?id=40008383)
[aaronjanse/dns-over-wikipedia: Redirect `.idk` domains using Wikipedia](https://github.com/aaronjanse/dns-over-wikipedia)
- MAY GO INTO TB?

[Domain Name Purchase Agreements](https://www.ipwatchdog.com/business/domain-name-purchase-agreements)

[Proposed top-level domain string for private use: ".internal" | Hacker News](https://news.ycombinator.com/item?id=39152306)
[Proposed Top-Level Domain String for Private Use](https://www.icann.org/en/public-comment/proceeding/proposed-top-level-domain-string-for-private-use-24-01-2024)

[What DNS Is Not (2009) | Hacker News](https://news.ycombinator.com/item?id=39489427)
[What DNS Is Not - ACM Queue](https://queue.acm.org/detail.cfm?id=1647302)

[Cloudflare loses 22% of its domains in Freenom .tk shutdown | Hacker News](https://news.ycombinator.com/item?id=39725303)
[Cloudflare loses 22% of its domains in Freenom .tk shutdown | Netcraft](https://www.netcraft.com/blog/cloudflare-loses-22-of-its-domains-in-freenom-tk-shutdown/)

[Cloudflare, Apple, and others back a new way to make the Internet more private | Ars Technica](https://arstechnica.com/information-technology/2020/12/cloudflare-apple-and-others-back-a-new-way-to-make-the-internet-more-private)

[MagicDNS is generally available | Hacker News](https://news.ycombinator.com/item?id=33276601)
[MagicDNS is generally available](https://tailscale.com/blog/magicdns)

[Moving our Encrypted DNS servers to run in RAM | Hacker News](https://news.ycombinator.com/item?id=38217355)
[Moving our Encrypted DNS servers to run in RAM | Mullvad VPN](https://mullvad.net/en/blog/moving-our-encrypted-dns-servers-to-run-in-ram)

[.io considered harmful | Hacker News](https://news.ycombinator.com/item?id=38084572)
[.io considered harmful • beep.blog](https://www.beep.blog/io/)

[Facebook-owned sites were down | Hacker News](https://news.ycombinator.com/item?id=28748203)

[Prose.sh - A blog platform for hackers | Hacker News](https://news.ycombinator.com/item?id=32128013)
[discover prose -- prose.sh](https://prose.sh/)

[Internet Archive as a default host-of-record for startups | Hacker News](https://news.ycombinator.com/item?id=29639222)
[John Carmack on Twitter: "The Internet Archive struggles mightily to save content when services shut down, but it is often a panicky reactive process. I wonder if there could be a world where the IA acts as a default host-of-record for startups, with a super-easy CDN relationship such that the content \" / Twitter](https://web.archive.org/web/20211223021310/https://twitter.com/ID_AA_Carmack/status/1473327982605385735)

[Apple's whitelist of the 250k auto-completable domains in iOS | Hacker News](https://news.ycombinator.com/item?id=30903246)
[cdn.smoot.apple.com/static/autofill_tld_whitelist_url](https://cdn.smoot.apple.com/static/autofill_tld_whitelist_url)

[Whytheluckystiff's original domain back as an archive | Hacker News](https://news.ycombinator.com/item?id=32513020)
[_why's Estate](https://whytheluckystiff.net/)

[MarkMonitor left 60k domains for the taking | Hacker News](https://news.ycombinator.com/item?id=28351432)
[How MarkMonitor left >60,000 domains for the taking](https://ian.sh/markmonitor)

[Vivek Gite](https://www.cyberciti.biz/faq/howto-use-dig-to-find-dns-time-to-live-ttl-values/)
Dig Command Find Out TTL (Time to Live) Value For DNS Records

[Internet Assigned Numbers Authority](https://www.iana.org/)

[APNIC](https://www.apnic.net/)
[Wq.apnic.net/static/search.html](https://www.wq.apnic.net/static/search.html)

[What are effective backup strategies during DNS migration?](https://www.linkedin.com/comm/advice/0/what-effective-backup-strategies-during-dns-quo9f)

[A Google Cloud support engineer solves a tough DNS case | Hacker News](https://news.ycombinator.com/item?id=23235995)
[A Google Cloud support engineer solves a tough DNS case | Google Cloud Blog](https://cloud.google.com/blog/topics/inside-google-cloud/google-cloud-support-engineer-solves-a-tough-dns-case)

[The Disappearance of an Internet Domain](https://every.to/p/the-disappearance-of-an-internet-domain)

## domains - DNS alternatives

[The GNU Name System | Hacker News](https://news.ycombinator.com/item?id=32222360)
[GNUnet](https://www.gnunet.org/en/gns.html)

## domains - DNS - leak tests

[Make sure y'all do a DNS LEAK test frequently](https://old.reddit.com/r/Piracy/comments/ubsm0e/make_sure_yall_do_a_dns_leak_test_frequently/)

## domains - DNS lookup

[Rackspace](https://support.rackspace.com/how-to/nslookup-checking-dns-records-on-windows/)
Check DNS records on Windows with nslookup

## domains - DNS providers

[Former ICANN CEO is now co-CEO of the private equity firm that tried to buy .org | Hacker News](https://news.ycombinator.com/item?id=23878508)
[Fadi Chehadé is now co-CEO of Ethos Capital - Domain Name Wire | Domain Name News](https://domainnamewire.com/2020/07/16/fadi-chehade-is-now-co-ceo-of-ethos-capital/)

## domains - DNS - registrar

[FYI Namecheap is selling your e-mail or is compromised. : homelab](https://old.reddit.com/r/homelab/comments/116j7iq/fyi_namecheap_is_selling_your_email_or_is)

[Domain registrar Gandi gets bought out, removes free mailboxes | Hacker News](https://news.ycombinator.com/item?id=35080777)
[Paul Barker: "So, further to recent changes …" - A Social Front Organization](https://web.archive.org/web/20230309130738/https://social.afront.org/@pbarker/109993372907209176)

[BGP Meets Cat](https://labs.ripe.net/Members/cteusche/bgp-meets-cat)
after 3072 hours of manipulating BGP, Job Snijders has succeeded in drawing a Nyancat.

## domains - forums

[NamePros](https://www.namepros.com/)
Domain Forum

[DNForum](https://www.dnforum.com/)
Domain Forum

[GitHub - WebSnifferHQ/Domain-Name-Forums: A curated list of domain name related forums and discussion boards for domain name enthusiasts and professionals.](https://github.com/WebSnifferHQ/Domain-Name-Forums)

## domains - TLD

[Find a good available .com domain | Hacker News](https://news.ycombinator.com/item?id=31664440)
[Find a good available .com domain | Derek Sivers](https://sive.rs/com)

[How We Saved Dot Org | Hacker News](https://news.ycombinator.com/item?id=25521836)
[How We Saved .ORG: 2020 in Review | Electronic Frontier Foundation](https://www.eff.org/deeplinks/2020/12/how-we-saved-org-2020-review)

[Ask HN: Own .com for 7 years, a new company trademarked my name registered .NET | Hacker News](https://news.ycombinator.com/item?id=29521714)

[Premium .dev domain with Google costs $850 | Hacker News](https://news.ycombinator.com/item?id=33928399)
[Emir Karşıyakalı on Twitter: "As you know, domain extensions like .dev and .app are owned by Google. Last year, I bought the https://t.co/SWNLwhWO9l domain for one of our projects. When I tried to renew it this year, I was faced with a renewal price of $850 instead of the normal price of $12." / Twitter](https://web.archive.org/web/20230126171357/https://twitter.com/EmirKarsiyakali/status/1601373440979525632)

[The .zip TLD sucks | Hacker News](https://news.ycombinator.com/item?id=35920336)
[The .zip TLD sucks and it needs to be immediately revoked.](https://financialstatement.zip/)

[.ai | Hacker News](https://news.ycombinator.com/item?id=32804189)
[Offshore Information Services Ltd.](http://www.ai/?)

[Root Zone Database](https://www.iana.org/domains/root/db)

[ccTLD List](https://icannwiki.org/Country_code_top-level_domain#Current_ccTLDs)

## domains - URL

[url - what is difference between www vs www1, www2, www3 etc - Stack Overflow](https://stackoverflow.com/questions/4575814/what-is-difference-between-www-vs-www1-www2-www3-etc)

[Shortest URLs on the Internet | Hacker News](https://news.ycombinator.com/item?id=32801359)
[Shortest URLs on the Internet | James Williams](https://jameswillia.ms/posts/shortest-urls.html)

[What is the minimal possible UK address? | Hacker News](https://news.ycombinator.com/item?id=34995370)
[What is the Most Minimal UK Address Possible? | Vlad's Website](https://vladh.net/most-minimal-uk-address/)

[Cool URIs Don't Change (1998) | Hacker News](https://news.ycombinator.com/item?id=35015624)
[Hypertext Style: Cool URIs don't change.](https://www.w3.org/Provider/Style/URI)

[How to store your app's entire state in the url | Hacker News](https://news.ycombinator.com/item?id=34312546)
[scottantipa.com/store-app-state-in-urls](https://www.scottantipa.com/store-app-state-in-urls)

[Gail.com FAQ | Hacker News](https://news.ycombinator.com/item?id=34307705)
[gail.com FAQ](https://gail.com/)

[ELI5: How do some websites hijack my back button and keep me on their site until I've hit back two or three times? : explainlikeimfive](https://old.reddit.com/r/explainlikeimfive/comments/rgpduj/eli5_how_do_some_websites_hijack_my_back_button)

## endless requests

[How to waste bandwidth, battery power, and annoy sysadmins | Hacker News](https://news.ycombinator.com/item?id=40828203)
[How to waste bandwidth, battery power, and annoy sysadmins](https://rachelbythebay.com/w/2024/06/28/fxios/)

## fingerprinting

[Web fingerprinting is worse than I thought | Hacker News](https://news.ycombinator.com/item?id=35243355)
[Web fingerprinting is worse than I thought - Bitestring's Blog](https://www.bitestring.com/posts/2023-03-19-web-fingerprinting-is-worse-than-I-thought.html)

## Firebase

[Show HN: Firebase, a scalable real-time backend | Hacker News](https://news.ycombinator.com/item?id=3832877)
[Firebase | Google's Mobile and Web App Development Platform](https://firebase.google.com/)

[We're moving on from Firebase | Hacker News](https://news.ycombinator.com/item?id=33215770)
[Why we're moving away from Firebase](https://koptional.com/article/why-we%e2%80%99re-moving-away-from-firebase/)

## framebusting

[Let websites framebust out of native apps | Hacker News](https://news.ycombinator.com/item?id=32418679)
[Let websites framebust out of native apps | Holovaty.com](https://www.holovaty.com/writing/framebust-native-apps/)

## Gemini protocol

[What is this Gemini thing, and why am I excited about it? (2020) | Hacker News](https://news.ycombinator.com/item?id=28600436)
[What is this Gemini thing anyway, and why am I excited about it?](https://drewdevault.com/2020/11/01/What-is-Gemini-anyway.html)

## history

[World Wide Web (1991) | Hacker News](https://news.ycombinator.com/item?id=40177906)
[The World Wide Web project](https://info.cern.ch/hypertext/WWW/TheProject.html)

[Information mesh](http://infomesh.org/index)
[Information mesh](http://infomesh.org/)

## htaccess

[Jeff Starr](https://perishablepress.com/stupid-htaccess-tricks/)
Stupid .htaccess Tricks

[Jeff Starr](https://perishablepress.com/htaccess-cleanup/)
.htaccess Cleanup

## HTTP

[TIL: supermicro IPMI can attach virtual ISO images hosted on http/https, not just smb](https://old.reddit.com/r/selfhosted/comments/15zftzc/til_supermicro_ipmi_can_attach_virtual_iso_images/)

[The State of HTTP in 2022 | Hacker News](https://news.ycombinator.com/item?id=34201082)
[The state of HTTP in 2022](https://blog.cloudflare.com/the-state-of-http-in-2022/)

[Using HTTP Basic Auth in 2022 | Hacker News](https://news.ycombinator.com/item?id=29761728)
[Why I'm Using HTTP Basic Auth in 2022 | Joel Dare](https://joeldare.com/why-im-using-http-basic-auth-in-2022.html)

[HTTP/3 Is Fast | Hacker News](https://news.ycombinator.com/item?id=29563229)
[HTTP/3 is Fast - Request Metrics](https://requestmetrics.com/web-performance/http3-is-fast/)

[HTTP/2-exclusive threats caused by implementation flaws and RFC imperfections | Hacker News](https://news.ycombinator.com/item?id=28080097)
[HTTP/2: The Sequel is Always Worse | PortSwigger Research](https://portswigger.net/research/http2)

[HTML5 still doesn't replicate what mattered about Flash | Hacker News](https://news.ycombinator.com/item?id=25587765)
[Lars Doucet on X: "To this day, I am super mad at all the people who put for the codswallop that HTML5 was this perfect replacement for Flash. It's been 10 years since "Thoughts on Flash" was published and HTML5 STILL doesn't (in actual practice) replicate what mattered about Flash." / X](https://twitter.com/larsiusprime/status/1344404336252768257)

[HTTP/3 adoption is growing rapidly | Hacker News](https://news.ycombinator.com/item?id=37777050)
[Why HTTP/3 is eating the world | APNIC Blog](https://blog.apnic.net/2023/09/25/why-http-3-is-eating-the-world/)

[HTTP/2 Continuation Flood: Technical Details | Hacker News](https://news.ycombinator.com/item?id=39930919)
[HTTP/2 CONTINUATION Flood: Technical Details - nowotarski.info](https://nowotarski.info/http2-continuation-flood-technical-details/)

[CVE-2023-40547 - avoid incorrectly trusting HTTP headers | Hacker News](https://news.ycombinator.com/item?id=39132300)
[CVE-2023-40547 - avoid incorrectly trusting HTTP headers · rhboot/shim@0226b56](https://github.com/rhboot/shim/commit/0226b56513b2b8bd5fd281bce77c40c9bf07c66d)

[Server-sent events, WebSockets, and HTTP | Hacker News](https://news.ycombinator.com/item?id=30403438)
[Server-Sent Events, WebSockets, and HTTP](https://www.mnot.net/blog/2022/02/20/websockets)
[Server-Sent Events: an alternative to WebSockets | Hacker News](https://news.ycombinator.com/item?id=30312897)
[Server-Sent Events: the alternative to WebSockets you should be using - germano.dev](https://germano.dev/sse-websockets)

[Reliably Send an HTTP Request as a User Leaves a Page | Hacker News](https://news.ycombinator.com/item?id=30942555)
[Reliably Send an HTTP Request as a User Leaves a Page | CSS-Tricks - CSS-Tricks](https://css-tricks.com/send-an-http-request-on-page-exit/)

## HTTP - Go

[How I write HTTP services in Go after 13 years | Hacker News](https://news.ycombinator.com/item?id=39318867)
[How I write HTTP services in Go after 13 years | Grafana Labs](https://grafana.com/blog/2024/02/09/how-i-write-http-services-in-go-after-13-years/)

## HTTP - gRPC

[Why does gRPC insist on trailers? | Hacker News](https://news.ycombinator.com/item?id=32380769)
[Carl's Blog](https://carlmastrangelo.com/blog/why-does-grpc-insist-on-trailers)

## HTTP servers

[h5ai · modern HTTP web server index for Apache httpd, lighttpd, nginx and Cherokee · larsjung.de](https://larsjung.de/h5ai/)
[index powered by h5ai v0.29.2 (https://larsjung.de/h5ai/)](https://invalidvertex.com/soundcloud_backup)
[index powered by h5ai v0.29.2 (https://larsjung.de/h5ai/)](https://info.stylee32.net/)

## HTTPS

[API Shouldn't Redirect HTTP to HTTPS | Hacker News](https://news.ycombinator.com/item?id=40504756)
[Your API Shouldn't Redirect HTTP to HTTPS](https://jviide.iki.fi/http-redirects)

[Paul Calvano](https://discuss.httparchive.org/t/adoption-of-http-security-headers-on-the-web/1259)
(2018) Adoption of HTTP Security Headers on the Web

[Identifying Airtel middleboxes that censor HTTPS traffic | Hacker News](https://news.ycombinator.com/item?id=24626388)
[Identifying Airtel middleboxes that censor HTTPS traffic](https://web.archive.org/web/20231227063044/https://iamkush.me/sni-airtel/)

## instantmessengers - e2e

[Building end-to-end security for Messenger | Hacker News](https://news.ycombinator.com/item?id=38552789)
[Building end-to-end security for Messenger - Engineering at Meta](https://engineering.fb.com/2023/12/06/security/building-end-to-end-security-for-messenger/)

## instantmessengers - IRC and XDCC

[IRC is the only viable chat protocol (2022) | Hacker News](https://news.ycombinator.com/item?id=36918655)
[IRC is the Only Viable Chat Protocol](https://koshka.love/babel/irc-forever.html)

[IRC.org](http://www.irc.org/history_docs/TheGreatSplit.html)

[322: Pix Plz - explain xkcd](https://www.explainxkcd.com/wiki/index.php/322:_Pix_Plz)

[364: Responsible Behavior - explain xkcd](https://www.explainxkcd.com/wiki/index.php/364:_Responsible_Behavior)

## instantmessengers - Matrix protocol

[Germany's national healthcare system adopts Matrix for communication | Hacker News](https://news.ycombinator.com/item?id=27906336)
[Matrix.org - Germany's national healthcare system adopts Matrix!](https://matrix.org/blog/2021/07/21/germany-s-national-healthcare-system-adopts-matrix/)

[Element raises $30M to boost Matrix | Hacker News](https://news.ycombinator.com/item?id=27969624)
[Element raises $30M to boost Matrix | Matrix.org](https://web.archive.org/web/20210727070721/https://matrix.org/blog/2021/07/27/element-raises-30-m-to-boost-matrix)

[Matrix 2.0: The Future of Matrix | Hacker News](https://news.ycombinator.com/item?id=37599510)
[Matrix.org - Matrix 2.0: The Future of Matrix](https://matrix.org/blog/2023/09/matrix-2-0/)

[Matrix-webcam displays your webcam video feed in the console | Hacker News](https://news.ycombinator.com/item?id=33058242)
[GitHub - joschuck/matrix-webcam: Take your video conference from within the matrix.](https://github.com/joschuck/matrix-webcam)

## instantmessengers - MS Teams

[Ask HN: Why is Microsoft Teams still so bad? | Hacker News](https://news.ycombinator.com/item?id=32932137)

## instantmessengers - RCS

[Apple announces that RCS support is coming to iPhone next year | Hacker News](https://news.ycombinator.com/item?id=38293082)
[Apple announces that RCS support is coming to iPhone next year - 9to5Mac](https://9to5mac.com/2023/11/16/apple-rcs-coming-to-iphone/)

## instantmessengers - Signal

[Signal on Android: Images sent to wrong contacts | Hacker News](https://news.ycombinator.com/item?id=27950763)
[Images from another user displayed in message · Issue #10247 · signalapp/Signal-Android](https://github.com/signalapp/Signal-Android/issues/10247)

[No, Cellebrite Cannot "Break Signal Encryption" | Hacker News](https://news.ycombinator.com/item?id=25520481)
[Signal >> Blog >> No, Cellebrite cannot 'break Signal encryption.'](https://signal.org/blog/cellebrite-and-clickbait/)

[Help users in Iran reconnect to Signal | Hacker News](https://news.ycombinator.com/item?id=26026994)
[Signal >> Blog >> Help users in Iran reconnect to Signal](https://signal.org/blog/help-iran-reconnect/)

[You can change your number | Hacker News](https://news.ycombinator.com/item?id=30250215)
[Signal >> Blog >> You Can Change Your Number](https://signal.org/blog/change-number/)

[Signal Introduces Stories | Hacker News](https://news.ycombinator.com/item?id=33508536)
[Signal >> Blog >> Story Time](https://signal.org/blog/introducing-stories/)

[Snap Store administrators removed signal-desktop from Ubuntu Snap | Hacker News](https://news.ycombinator.com/item?id=33450806)
[What happened to signal-desktop? - snap - snapcraft.io](https://forum.snapcraft.io/t/what-happened-to-signal-desktop/32119)
[Install Cawbird Twitter Client for Linux using the Snap Store | Snapcraft](https://snapcraft.io/cawbird)

[Signal: You were the chosen one [video] | Hacker News](https://news.ycombinator.com/item?id=32244795)
[Signal: you were the chosen one! - media.ccc.de](https://media.ccc.de/v/mch2022-196-signal-you-were-the-chosen-one-)

[Removing SMS support from Signal Android (soon) | Hacker News](https://news.ycombinator.com/item?id=33179047)
[Signal >> Blog >> Removing SMS support from Signal Android (soon)](https://signal.org/blog/sms-removal-android/)

[Privacy is priceless, but Signal is expensive | Hacker News](https://news.ycombinator.com/item?id=38291427)
[Signal >> Blog >> Privacy is Priceless, but Signal is Expensive](https://signal.org/blog/signal-is-expensive/)

## instantmessengers - sms

["It's time for Apple to fix texting" | Hacker News](https://news.ycombinator.com/item?id=32399238)
[Apple can fix the messaging between Androids & iPhones | Android](https://www.android.com/get-the-message/)

[search Best way to pre-process text messages using Hadoop Stack Overflow](https://stackoverflow.com/questions/6543102/best-way-to-pre-process-text-messages-using-hadoop)

## instantmessengers - video

[Show HN: I built an app for when I talk too much in online meetings | Hacker News](https://news.ycombinator.com/item?id=32095592)
[Unblah - For those (like myself) who often talk too much, or too little, in meetings because they get nervous](https://unblah.me/)

## instantmessengers - XMPP

[XMPP, a comeback story | Hacker News](https://news.ycombinator.com/item?id=29256618)
[XMPP, A Comeback Story: A 20 Year Old Messaging Protocol For Robust, Private and Decentralized Communications](https://takebackourtech.org/xmpp-comeback/)

[Are we OMEMO yet? | Tracking the progress of OMEMO integration in XMPP clients.](https://omemo.top/)

## internet history

[The internet is held together with spit and baling wire | Hacker News](https://news.ycombinator.com/item?id=29353076)
[The Internet is Held Together With Spit & Baling Wire - Krebs on Security](https://krebsonsecurity.com/2021/11/the-internet-is-held-together-with-spit-baling-wire/)

[Only 90s Web Developers Remember This (2014) | Hacker News](https://news.ycombinator.com/item?id=39127433)
[Only 90s web developers remember this (2014) | Hacker News](https://news.ycombinator.com/item?id=29296003)
[Only 90s Web Developers Remember This](https://zachholman.com/posts/only-90s-developers/)

[A Brief History of the Internet - Who Invented It, How it Works, and How it Became the Web We Use Today](https://www.freecodecamp.org/news/brief-history-of-the-internet)

[Ask HN: Is it time to resurrect a Usenet clone? | Hacker News](https://news.ycombinator.com/item?id=36262821)

## IoT - ai

[Building a fully local LLM voice assistant to control my smart home | Hacker News](https://news.ycombinator.com/item?id=38985152)
[Building a fully local LLM voice assistant to control my smart home | John's Website](https://johnthenerd.com/blog/local-llm-assistant/)

## IoT

[My smart home 2021: A Home Assistant love story | Hacker News](https://news.ycombinator.com/item?id=30349767)
[My Smart Home 2021 | Joris Roovers](https://jorisroovers.com/posts/my-smart-home-2021/)

[IKEA sensors for doors and windows, motion, water leaks | Hacker News](https://news.ycombinator.com/item?id=38445745)
[Ikea debuts a trio of affordable smart home sensors - The Verge](https://www.theverge.com/2023/11/28/23977693/ikea-sensors-door-window-water-motion-price-date-specs)

[Hacking my "smart" toothbrush | Hacker News](https://news.ycombinator.com/item?id=36128617)
[Hacking my "smart" toothbrush - The Twenty Percent](https://kuenzi.dev/toothbrush/)

## IoT - security

[The S in IoT is for Security | Hacker News](https://news.ycombinator.com/item?id=26540007)
[The S in IOT is for Security - Purism](https://puri.sm/posts/the-s-in-iot-is-for-security/)

## IP - BGP

[GitHub - benjojo/bgp-battleships: Play battleships using BGP](https://github.com/benjojo/bgp-battleships?tab=readme-ov-file)
[Playing battleships over BGP](https://blog.benjojo.co.uk/post/bgp-battleships)
playing battleships over BGP.

## IPv4

[Who is squatting IPv4 addresses?](https://blog.benjojo.co.uk/post/ip-address-squatting)

[Czech republic sets IPv4 end date | Hacker News](https://news.ycombinator.com/item?id=39097314)
[Homepage - Konec IPv4](https://konecipv4.cz/en/)

[AWS to begin charging for public IPv4 addresses | Hacker News](https://news.ycombinator.com/item?id=36989798)
[New - AWS Public IPv4 Address Charge + Public IP Insights | AWS News Blog](https://aws.amazon.com/blogs/aws/new-aws-public-ipv4-address-charge-public-ip-insights/)

## IPv6

[Going IPv6 only](https://blog.brixit.nl/going-ipv6-only)

[40% of Google users now connect via IPv6 | Hacker News](https://news.ycombinator.com/item?id=31967221)
[IPv6 - Google](https://www.google.com/intl/en/ipv6/statistics.html)

[Engineer distributes resume via IPv6 traceroute | Hacker News](https://news.ycombinator.com/item?id=32609588)
[cv6.poinsignon.org | IPv6 Traceroute](https://web.archive.org/web/20220903153142/https://cv6.poinsignon.org/)

[Turn off IPv6 to Prevent Leaks](https://www.itechguides.com/disable-ipv6-windows-10/)

[IPv6 Internet is broken | Hacker News](https://news.ycombinator.com/item?id=33941324)
[IPv6 Internet Is Broken](https://adminhacks.com/broken-IPv6.html)

[Tell HN: IPv6-only still pretty much unusable | Hacker News](https://news.ycombinator.com/item?id=33894933)

[Tell HN: Hacker News now supports IPv6 | Hacker News](https://news.ycombinator.com/item?id=39099065)

## minimalist websites

[10kb Club](https://10kbclub.com/)

[250kb Club](https://250kb.club/)

[The 512KB Club](https://512kb.club/)
The 512KB Club
The internet has become a bloated mess. Massive JavaScript libraries, countless client-side queries and overly complex frontend frameworks are par for the course these days. [...] But we can make a difference - all it takes is some optimisation. [...] The 512KB Club is a collection of performance-focused web pages from across the Internet.
[kevquirk/512kb.club](https://github.com/kevquirk/512kb.club)

[1MB Club](https://1mb.club/)

## phones - VoIP

[Is VoIP dead?](https://old.reddit.com/r/networking/comments/15t7262/is_voip_dead/)

## QUIC

[QUIC is now RFC 9000 | Hacker News](https://news.ycombinator.com/item?id=27310349)
[QUIC is now RFC 9000 | Fastly](https://www.fastly.com/blog/quic-is-now-rfc-9000)

## spam comments

[Akismet to Turnstile - b3n.org](https://b3n.org/akismet-to-turnstile/)

## stacks - JAMstack

[JAMstack](https://jamstack.org/)
noun `’jam-stak’` : Modern web development architecture based on client-side JavaScript, reusable APIs, and prebuilt Markup.
The JAMstack is not about specific technologies. It’s a new way of building websites and apps that delivers better performance, higher security, lower cost of scaling, and a better developer experience.

[Introducing Cloudflare Pages: the best way to build JAMstack websites](https://blog.cloudflare.com/cloudflare-pages)

## stacks - MEAN

[Scott Davis](https://www.ibm.com/developerworks/web/library/wa-mean1/)
(2014) From LAMP to MEAN : Introducing the MEAN stack

## TCP

[Multipath TCP for Linux (2022) | Hacker News](https://news.ycombinator.com/item?id=40089609)
[MPTCP | Multipath TCP for Linux](https://www.mptcp.dev/)

[We need a replacement for TCP in the datacenter [pdf] | Hacker News](https://news.ycombinator.com/item?id=33401480)
[[2210.00714] It's Time to Replace TCP in the Datacenter](https://arxiv.org/abs/2210.00714)

[It's always TCP_NODELAY | Hacker News](https://news.ycombinator.com/item?id=40310896)
[It's always TCP_NODELAY. Every damn time. - Marc's Blog](https://brooker.co.za/blog/2024/05/09/nagle.html)

## the internet trend is dying

[The internet is already over (2022) | Hacker News](https://news.ycombinator.com/item?id=40899761)
[The internet is already over - by Sam Kriss](https://samkriss.substack.com/p/the-internet-is-already-over)

## unusual hosting

[This Blog is now hosted on a GPS/LTE modem | Hacker News](https://news.ycombinator.com/item?id=26669749)
[This blog is now hosted on a GPS/LTE modem](https://nns.ee/blog/2021/04/01/modem-blog.html)

[I'm hosting a website on a RAID0 of 30 floppy drives | Hacker News](https://news.ycombinator.com/item?id=32110662)
[Just a totally normal website](https://web.archive.org/web/20220715175852/https://totallynormalwebsite.ddns.net/)

[DIY Network/Server Rack](https://scottmckendry.tech/diy-network-rack)

[This blog is hosted on my Android phone | Hacker News](https://news.ycombinator.com/item?id=35944315)
[This page is hosted on my Android phone](https://web.archive.org/web/20230520092128/https://androidblog.a.pinggy.io/)

[This site is no longer solar powered for now | Hacker News](https://news.ycombinator.com/item?id=36177762)
[This Site is no longer Solar Powered... For Now | Andrew JV Powell](https://www.andrewjvpowell.com/articles/this-site-is-no-longer-solar-powered-for-now/)

[Show HN: Host a Website in the URL | Hacker News](https://news.ycombinator.com/item?id=37408150)
[🗜 omg it's a smolsite](https://smolsite.zip/UEsDBBQAAgAIAMYVIVfaTMb/VQIAANwDAAAKAAAAaW5kZXguaHRtbHVTUW+bMBB+Lr/ilq1i0wo4BGghJA/t9lBpk6Zpm6Y91cEOeAPMbCeEbv3vO0OjZdIK4mTuvvt8+vw5r0xTr5284pStc22Gmq+djWQD/HI2tPhRKrlrmVfIWqoMnm/HZ3laEg0teQY7Vb+cMWpoNiYCvS9fH5r64nxxg0voBTPVyp2HLlRclJXBdeLCXvD+Wh5WLgEC8xBsDrtavXIrY7osCPq+9/uFL1UZhIQQy+ueL94ibUdNBWzlvo/AT9MbjFEUQ4QxQrIYSOHHcWh5sRLbmKb7yCfhTQIxluIxJoB/kBTeBPbmHoJtTNMv+N03CVwVBKtRYpltHsbqE+QFAYv1LBhz3lj5H/mVZXdhK+p65Z6HC3bJYkanhCc7WggzoC5+9JhSu5qvXL7nrWTMDSYNrBy4mr1aOlvZGm9LG1EPGWjaak9zJfCsGqpK0WYo71V3WDoPTsFbwxUe8FlHGRNteVLrFLeFv+eLhx4S+y6ds6MLLol9lyf9IbHtZ4YfzNErU+rByYPJVXkweszJrbus4+brW+NqoKAbWWth+DOEzNeOk3frT5XQ0Fey5mArqIDRIFotGAdTcfj88R2iu0ewhEpqA4PcKY1O1BOmkE1D0aC1aNGf3c4AiqcGU+HEyIUbf7v9YLXlF3BNsSmJgLeFxC2EuQBsBYMy4A/QrRVsZi2p0ZPHgf170QWz7DiIwqvzAjAH3puv33+moGXDjzjckfGDb68bNEMtS+l3bYl4XlTyCeq7gpp/SX7DBifFQT2vV7QDcjdDgced82ASFhfTnXb+AFBLAQIeAxQAAgAIAMYVIVfaTMb/VQIAANwDAAAKAAAAAAAAAAEAAACkgQAAAABpbmRleC5odG1sUEsFBgAAAAABAAEAOAAAAH0CAAAAAA==)

[itty.bitty](https://itty.bitty.site/edit)

[Show HN: This page exists only if someone is looking at it | Hacker News](https://news.ycombinator.com/item?id=9531265)
[Ephemeral Hosting](http://ephemeralp2p.durazo.us/2bbbf21959178ef2f935e90fc60e5b6e368d27514fe305ca7dcecc32c0134838)

[A page with no code | Hacker News](https://news.ycombinator.com/item?id=34464951)
[The Page With No Code - Dan Q](https://danq.me/2023/01/11/nocode/)

[Most 16-year-olds don't have servers in their rooms | Hacker News](https://news.ycombinator.com/item?id=38710318)
[Most 16-year-olds don't have servers in their rooms](https://varun.ch/server)

[Deploy a website on imgur.com | Hacker News](https://news.ycombinator.com/item?id=28431716)
[EtherDream/web2img: Bundle web files into a single image](https://github.com/etherdream/web2img)
[Web2Img](https://etherdream.com/web2img/)

[Althttpd: Simple webserver in a single C file | Hacker News](https://news.ycombinator.com/item?id=27431910)
[Althttpd: The Althttpd Webserver](https://sqlite.org/althttpd/doc/trunk/althttpd.md)

[I made my blog solar-powered, then things escalated | Hacker News](https://news.ycombinator.com/item?id=35596959)
[I made my blog solar-powered, then things escalated](https://louwrentius.com/i-made-my-blog-solar-powered-then-things-escalated.html)

## urls

[You cannot simply publicly access private secure links, can you? | Hacker News](https://news.ycombinator.com/item?id=39630985)
[You can not simply publicly access private secure links, can you? | Vin01's Blog](https://vin01.github.io/piptagole/security-tools/soar/urlscan/hybrid-analysis/data-leaks/urlscan.io/cloudflare-radar%22/2024/03/07/url-database-leaks-private-urls.html)

[L(O*62).ONG: Make your URL longer | Hacker News](https://news.ycombinator.com/item?id=40543196)
[L(o*62).ong - Make your URL longer](https://loooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooo.ong/)

[Examples of Great URL Design (2023) | Hacker News](https://news.ycombinator.com/item?id=41243992)
[Examples of Great URL Design - Jim Nielsen’s Blog](https://blog.jim-nielsen.com/2023/examples-of-great-urls/)

[A deep dive into how linkers work (2008) | Hacker News](https://news.ycombinator.com/item?id=41316342)
[A ToC of the 20 part linker essay [LWN.net]](https://lwn.net/Articles/276782/)

## web components

[The Failed Promise of Web Components | Hacker News](https://news.ycombinator.com/item?id=24640151)
[The failed promise of Web Components • Lea Verou](https://lea.verou.me/blog/2020/09/the-failed-promise-of-web-components/)

[HTML Web Components | Hacker News](https://news.ycombinator.com/item?id=38251330)
[HTML Web Components - Jim Nielsen's Blog](https://blog.jim-nielsen.com/2023/html-web-components/)

## web dev community and culture

[High Scalability](http://highscalability.com/)
Building bigger, faster, more reliable websites
[High Scalability](http://highscalability.com/all-time-favorites/)
Here are some of the favorite posts on HighScalability...

[Jeff Huang](https://jeffhuang.com/designed_to_last/)
(2019) This Page is Designed to Last : A Manifesto for Preserving Content on the Web

[Where Have All the Websites Gone? | Hacker News](https://news.ycombinator.com/item?id=38923627)
[Where have all the websites gone?](https://www.fromjason.xyz/p/notebook/where-have-all-the-websites-gone/)

[My daughter (7 years old) used HTML to make a website | Hacker News](https://news.ycombinator.com/item?id=40992982)
[naya.lol/](https://naya.lol/)

[10% of the top million sites are dead | Hacker News](https://news.ycombinator.com/item?id=32110573)
[10% of the Top Million Sites are Dead · Craig Campbell](https://ccampbell.io/posts/10-percent-of-top-million-sites-are-dead/)

[The internet wants to be fragmented | Hacker News](https://news.ycombinator.com/item?id=34205828)
[The internet wants to be fragmented - by Noah Smith](https://www.noahpinion.blog/p/the-internet-wants-to-be-fragmented)

[I miss the programmable web (2021) | Hacker News](https://news.ycombinator.com/item?id=32284375)
[I Miss The Programmable Web](https://matt-rickard.com/the-programmable-web)

[Come back, c2.com, we still need you | Hacker News](https://news.ycombinator.com/item?id=35948268)
[Welcome Visitors](https://wiki.c2.com/)

[webdev](https://www.reddit.com/user/Romaixn/m/webdev/)
Web Developer Multireddit

[Tell HN: I let my 6-year-old daughter design my website | Hacker News](https://news.ycombinator.com/item?id=30344989)
[Kevin Basset | kevin.tw](https://kevin.tw/)

[Show HN: My wife is pregnant; naturally I made a baby-name app to prepare | Hacker News](https://news.ycombinator.com/item?id=29118785)
[Nom de Bébé](https://nomdebebe.app/)

[I made a mobile app for my significant other and she won't use it | Hacker News](https://news.ycombinator.com/item?id=26765128)
[I Made A Mobile App for my Significant Other (And She Doesn't Use It)](https://web.archive.org/web/20210411043203/https://jerseyfonseca.com/blogs/wewatch)

[Future Blues - Emily's Cowboy Bebop Page (1999) | Hacker News](https://news.ycombinator.com/item?id=35589124)
[3-2-1..Let's Jam! Emily's Cowboy Bebop Page](https://futureblues.com/)

[GitHub - gokulkrishh/awesome-web-newsletters: List of awesome web related newsletter to subscribe.](https://github.com/gokulkrishh/awesome-web-newsletters)

[Life in Weeks - Buster's Notes](https://busterbenson.com/life-in-weeks)
- CONSIDER DOING THIS?

## web dev community and culture - total freedom

[No More Medium - Build Your Own Site (2019) | Hacker News](https://news.ycombinator.com/item?id=28493431)
[No More Medium. Build Your Own Site, Please.](https://nomedium.dev/)

[Show HN: Switch from Medium to your own blog | Hacker News](https://news.ycombinator.com/item?id=20060549)
[mathieudutour/medium-to-own-blog: Switch from Medium to your own blog in a few minutes](https://github.com/mathieudutour/medium-to-own-blog)

[Everybody's Free (To Write Websites)](https://sarajoy.dev/blog/write-websites/)

[Show HN: AboutIdeasNow - search /about, /ideas, /now pages of 7k+ personal sites | Hacker News](https://news.ycombinator.com/item?id=39511714)
[About Ideas Now | Search 1000s of personal sites](https://aboutideasnow.com/)
[PersonalSit.es | Yes we got hot and fresh sites](https://personalsit.es/)
[GitHub - lindylearn/aboutideasnow: Find people to talk to or collaborate with by searching across the /about, /ideas and /now pages of 1000s of personal websites.](https://github.com/lindylearn/aboutideasnow)
- I have already submitted my site

## web dev

[Facts every web dev should know before they burn out and turn to painting | Hacker News](https://news.ycombinator.com/item?id=28895128)
[136 facts every web dev should know before they burn out and turn to landscape painting or nude modelling - Baldur Bjarnason](https://www.baldurbjarnason.com/2021/100-things-every-web-developer-should-know/)

[Web Development Reading List](https://wdrl.info/almanac/2017)
The 2017 Almanac : What happened in “News” in 2016?

[Web Development Reading List](https://wdrl.info/evergreen)
The Evergreen List : selection of resources that are important for a longer time.

[r/webdev](https://www.reddit.com/r/webdev/)
web development resources & news

[Karolina Szczur](https://medium.com/@fox/talk-the-state-of-the-web-3e12f8e413b3)
(2017) The State of the Web
A guide to impactful performance improvements

[Why is modern web development so complicated? | Hacker News](https://news.ycombinator.com/item?id=20637849)
[Why is modern web development so complicated? A long yet hasty explanation: Part 1! - vrk.dev](https://www.vrk.dev/2019/07/11/why-is-modern-web-development-so-complicated-a-long-yet-hasty-explanation-part-1/)

[The Best Motherfucking Website](https://thebestmotherfuckingwebsite.co/)
Your motherfucking websites got nothing compared to this beauty.
[This is still a motherfucking website.](http://bettermotherfuckingwebsite.com/)
[This is the best motherfucking website.](https://bestmotherfucking.website/)
[This is the final motherfucking website.](https://perfectmotherfuckingwebsite.com/)
[This is the best motherfucking website.](https://thebestmotherfucking.website/)
[MotherFuckingWebsite](http://motherfuckingwebsite.com/)
[EvenBetterMotherFuckingWebsite](https://evenbettermotherfucking.website/)
[TheBestMotherFuckingWebsite](https://thebestmotherfuckingwebsite.co/)

[Start a fucking blog | Hacker News](https://news.ycombinator.com/item?id=34231152)
[Start a Fucking Blog](https://startafuckingblog.com/)

[Don't Neglect the Fundamentals of Web Development [Tech Talk]](https://www.freecodecamp.org/news/learn-the-fundamentals-of-web-development)

[The baseline for web development in 2022](https://engineering.linecorp.com/en/blog/the-baseline-for-web-development-in-2022)

## web dev - performance improvement

[Jack Lenox](https://www.smashingmagazine.com/2019/01/save-planet-improving-website-performance/)
(2019) How Improving Website Performance Can Help Save The Planet

## web dev - semantic and microformats

[Let's talk about semantics](http://html5doctor.com/lets-talk-about-semantics/)

[HTML5 semantics from Smashing Magazine](http://www.smashingmagazine.com/2011/11/18/html5-semantics/)

[Metalog - the semantic web query/logical system](https://www.w3.org/RDF/Metalog/)

[The semantic web is now widely adopted | Hacker News](https://news.ycombinator.com/item?id=41307011)
[Being on The Semantic Web is easy, and, frankly, well worth the bother](https://csvbase.com/blog/13)

## web dev - templating

[A comprehensive list of most web templating engines](https://en.wikipedia.org/wiki/Comparison_of_web_template_engines)
(for comparison)

## web dev tricks

[Web developer tool secrets that shouldn't be secrets | Hacker News](https://news.ycombinator.com/item?id=29071700)
[Developer Tools secrets that shouldn't be secrets | Christian Heilmann](https://christianheilmann.com/2021/11/01/developer-tools-secrets-that-shouldnt-be-secrets/)

## web frameworks

[Biason::Julio::new();: "The untold history of web deve…" - Functional Café](https://functional.cafe/@juliobiason/111613996060167180)

## webhooks - IFTTT

[When "if" is not enough: Superpowers for IFTTT | by Philipp Ebneter | Medium](https://medium.com/@pebneter/when-if-is-not-enough-55b6e57d8742)

[Newest 'ifttt' Questions](https://stackoverflow.com/questions/tagged/ifttt)
[IFTTT (@IFTTT)](https://twitter.com/IFTTT)
[#IFTTT hashtag on Twitter](https://twitter.com/hashtag/IFTTT?src=hashtag_click)
[ifttt npm search](https://www.npmjs.com/search?q=ifttt)

## webhooks

[Give me /events, not webhooks | Hacker News](https://news.ycombinator.com/item?id=27823109)
[Give me /events, not webhooks](https://blog.sequin.io/events-not-webhooks/)

[Automate Your Life](https://automatelife.net/)

## web hosting - documents

[Serving my blog posts as Linux manual pages | Hacker News](https://news.ycombinator.com/item?id=39548410)
[Serving my blog posts as Linux manual pages | James' Coffee Blog](https://jamesg.blog/2024/02/29/linux-manual-pages/)

## web hosting

[I had a machine running for two weeks on the public cloud. Every few seconds there was an automated SSH login attempt. Here is the full list of usernames - some of which are quite curious. : netsec](https://old.reddit.com/r/netsec/comments/137heta/i_had_a_machine_running_for_two_weeks_on_the/)
[ssh-login-attempts-usernames · GitHub](https://gist.github.com/royra/35952b7bb1217e482a24d427848eefc2)

[Web Hosting Discussion Forums, Tutorials, Reviews & Services](https://forumweb.hosting/)

[Web Hosting Talk - The largest, most influential web hosting community on the Internet](https://www.webhostingtalk.com/)
Server Forum

[LowEndTalk](https://lowendtalk.com/)
Server Forum

[LowEndSpirit](https://lowendspirit.com/)
Server Forum

[OffshoreCorpTalk | Wealth & Tax Management](https://www.offshorecorptalk.com/)
Offshore Forum

[Webmaster Forum | WJunction - Webmaster Forum](https://www.wjunction.com/)
Web Master

## web hosting - optimizing resources

[7 watts idle - building a low powered server/NAS on Intel 12th/13th gen | Hacker News](https://news.ycombinator.com/item?id=38823514)
[7 watts idle on Intel 12th/13th gen: the foundation for building a low power server/NAS | mattgadient.com](https://mattgadient.com/7-watts-idle-on-intel-12th-13th-gen-the-foundation-for-building-a-low-power-server-nas/)

## web hosting servers - vps

[Privacy](https://old.reddit.com/r/selfhosted/comments/14njea1/privacy/)

[VPSBenchmarks](https://www.vpsbenchmarks.com/plans)

[How much can you get out of a $4 VPS? | Hacker News](https://news.ycombinator.com/item?id=34676186)
[How much can you really get out of a 4$ VPS?](https://alicegg.tech//2023/02/06/4dollar-vps.html)

## web hosting software - observability platform aka network monitor

[Grafana, Loki, and Tempo will be relicensed to AGPLv3 | Hacker News](https://news.ycombinator.com/item?id=26877528)
[Grafana, Loki, and Tempo will be relicensed to AGPLv3 | Grafana Labs](https://grafana.com/blog/2021/04/20/grafana-loki-tempo-relicensing-to-agplv3/)

[Monitoring Is a Pain | Hacker News](https://news.ycombinator.com/item?id=36469147)
[Monitoring is a Pain](https://matduggan.com/were-all-doing-metrics-wrong/)

## WebP

[WebP is so great except it's not (2021) | Hacker News](https://news.ycombinator.com/item?id=38653110)
[Engineering | WebP is so great… except it's not](https://eng.aurelienpierre.com/2021/10/webp-is-so-great-except-its-not/)

## web redesign

[What costs more, website redesign or a project from scratch? : webdev](https://old.reddit.com/r/webdev/comments/wprchj/what_costs_more_website_redesign_or_a_project)

[I regret my website redesign | Hacker News](https://news.ycombinator.com/item?id=32179563)
[I Regret My $46k Website Redesign · mtlynch.io](https://mtlynch.io/tinypilot-redesign/)

## WebRTC

[OBS merges WebRTC support | Hacker News](https://news.ycombinator.com/item?id=36273075)
[obs-webrtc: Add WHIP output & service · obsproject/obs-studio@851a8c2](https://github.com/obsproject/obs-studio/commit/851a8c216e14617fb523951839f3bdb240e85141)

## website - scrapers and archivers

[Web scraping for me, but not for thee | Hacker News](https://news.ycombinator.com/item?id=37264676)
[Web Scraping for Me, But Not for Thee (Guest Blog Post) - Technology & Marketing Law Blog](https://blog.ericgoldman.org/archives/2023/08/web-scraping-for-me-but-not-for-thee-guest-blog-post.htm)

[Web Scraping Is Vital to Democracy | Hacker News](https://news.ycombinator.com/item?id=25298697)
[Why Web Scraping Is Vital to Democracy - The Markup](https://themarkup.org/news/2020/12/03/why-web-scraping-is-vital-to-democracy)

[Scrape like the big boys | Hacker News](https://news.ycombinator.com/item?id=29117022)
[So you want to scrape like the big boys (2021) | Hacker News](https://news.ycombinator.com/item?id=40176738)
[incolumitas.com - So you want to Scrape like the Big Boys? 🚀](https://incolumitas.com/2021/11/03/so-you-want-to-scrape-like-the-big-boys/)

[Changedetection.io needs your help importing from distill.io and visualping! : selfhosted](https://old.reddit.com/r/selfhosted/comments/u9k1uz/changedetectionio_needs_your_help_importing_from)

[Ryanair wins screen scraping case against Booking.com in US court ruling | Hacker News](https://news.ycombinator.com/item?id=41031960)
[Ryanair wins case against Booking.com in US court](https://www.rte.ie/news/business/2024/0719/1460807-ryanair-wins-us-court-case-against-bookingcom/)

[Anyone got a contact at OpenAI. They have a spider problem | Hacker News](https://news.ycombinator.com/item?id=40001971)
[Anyone got a contact at OpenAI. They have a spider problem.](https://mailman.nanog.org/pipermail/nanog/2024-April/225407.html)

[Archiving URLs · Gwern.net](https://gwern.net/archiving)

[Avoiding bot detection: How to scrape the web without getting blocked? | Hacker News](https://news.ycombinator.com/item?id=29060272)
[niespodd/browser-fingerprinting: Analysis of Bot Protection systems with available countermeasures 🚿. How to defeat anti-bot system 👻 and get around browser fingerprinting scripts when scraping the web?](https://github.com/niespodd/browser-fingerprinting)

## website - scrapers and archivers - The Internet Archive

[Calculators now emulated at Internet Archive | Hacker News](https://news.ycombinator.com/item?id=34566139)
[A Calculated Move: Calculators Now Emulated at Internet Archive | Internet Archive Blogs](https://blog.archive.org/2023/01/29/a-calculated-move-calculators-now-emulated-at-internet-archive/)

## website - webpage monitor

[Tell HN: Thanks to thehodge and littlewarden.com, this site is up today | Hacker News](https://news.ycombinator.com/item?id=28472350)
[Monitor Domain & SSL Expiration, redirects and HTTP responses with Little Warden](https://littlewarden.com/)

## cache

[What is Pre-Caching? How to Increase Website Speed and Performance](https://www.freecodecamp.org/news/a-detailed-guide-to-pre-caching)

[What is Cached Data? What does Clear Cache Mean and What Does it Do?](https://www.freecodecamp.org/news/what-is-cached-data)

## full-stack

[GitHub - murffious/FullStackMastery-Resources: Resources to help full stack web developers master their craft](https://github.com/murffious/FullStackMastery-Resources)

[Full stack open](https://fullstackopen.com/en/)

## general web dev learning path

1: Introduction to Front End Development and HTML
- How the Web works: HTTP, packets, browsers, developer tools, etc.
- takes ~1 week

2: CSS & SFX
- Special effects using CSS3/Fonts (soon to be deprecated)
- From now on you should try to explore every cool site you see, inspecting its CSS and element distribution with your favorite browser inspection tool.
- Some of them are done right, some of them aren't
the point is you need a "hacker attitude" in order to steal the interesting parts and become versed in the ways of deconstructing someone else's design in order to find out how it works.
- takes ~1 week

3: Your first project - a quiz
- Semantics, Standards & Validation for HTML/CSS
- takes ~1-2 weeks

4: Real world problems
- (Photoshop 101) (to be disc.)
- We will now learn how to transform a Photoshop document into an HTML layout. That means you will need to grasp a basic understanding of Photoshop tools for selecting, measuring and properties, which will then help you structure your HTML and define your CSS styles.
- Please note that in all these tutorials you'll find mistakes. And you'll notice them only if you've paid close attention to the standards, semantics, usability and accessibility notions presented so far. When you do, please correct them as you see fit, or ask me whether something is correct or not.
- takes ~3 weeks

5: final project
- example workflow standards
  - git and HTML standards
- SASS magic
  - CSS is powerful, but not dynamic. To make it dynamic, you need SASS.
- templating basics
 - Until now, we've looked at static HTML and CSS projects and how to develop a working site. Now we'll take that to the next level, by exploring how to transform a static structure into a real, dynamic website, with real information stored in a database and dynamic structures for iterating, searching and navigating the site. These are all example templating engines or languages.You should read through at least a couple of them to understand the basic principles.

## guides - beginner - web dev

[Web Development for Beginners - A Curriculum | Hacker News](https://news.ycombinator.com/item?id=31299716)
[microsoft/Web-Dev-For-Beginners: 24 Lessons, 12 Weeks, Get Started as a Web Developer](https://github.com/microsoft/Web-Dev-For-Beginners)
[Web Dev for Beginners](https://microsoft.github.io/Web-Dev-For-Beginners/#/)
roadmap for becoming a "complete" front end (+ back end + devops etc.) developer

[What are the reference books to understand how internet works ?: computerscience](https://www.reddit.com/r/computerscience/comments/1254x23/what_are_the_reference_books_to_understand_how)

[Know it all](https://know-it-all.io/)
Web list that helps you track what you know and what you don't about web development.

## history

[Original WWW proposal is a Word for Macintosh 4 file from 1990, can we open it? | Hacker News](https://news.ycombinator.com/item?id=39357709)
[John Graham-Cumming's blog: The original WWW proposal is a Word for Macintosh 4.0 file from 1990, can we open it?](https://blog.jgc.org/2024/02/the-original-www-proposal-is-word-for.html)

## how the internet works
 
[How Does the Web Work? | The Odin Project](https://www.theodinproject.com/lessons/foundations-how-does-the-web-work)

## HTTP2

[HTTP/2 and HTTP/3 explained | Hacker News](https://news.ycombinator.com/item?id=39700443)
[HTTP/2 and HTTP/3 explained - AlexandreHTRB blog](https://alexandrehtrb.github.io/posts/2024/03/http2-and-http3-explained/)

[http2-explained](https://github.com/bagder/http2-explained)
a detailed document explaining and documenting HTTP/2.

[HTTP/2 in Action](https://www.manning.com/books/http2-in-action)
an excellent introduction to the new HTTP/2 standard.

## HTTP3

[HTTP/3 explained | Hacker News](https://news.ycombinator.com/item?id=19085534)
[English | HTTP/3 explained](https://http3-explained.haxx.se/en)

[http3-explained](https://github.com/bagder/http3-explained)
a document describing the HTTP/3 and QUIC protocols.

## HTTP

[Decrypting your own HTTPS traffic with Wireshark | Hacker News](https://news.ycombinator.com/item?id=30743141)
[Decrypting your own HTTPS traffic with Wireshark - Trickster Dev](https://www.trickster.dev/post/decrypting-your-own-https-traffic-with-wireshark/)

[An introduction to HTTP: everything you need to know](https://www.freecodecamp.org/news/http-and-everything-you-need-to-know-about-it)

[How HTTP Works and Why it's Important - Explained in Plain English](https://www.freecodecamp.org/news/how-the-internet-works)

[HTTP Networking in JavaScript -Handbook for Beginners](https://www.freecodecamp.org/news/http-full-course)

[HTTP vs HTTPS - What's the Difference?](https://www.freecodecamp.org/news/http-vs-https)

[Daniel Miessler](https://danielmiessler.com/study/http/)
A Security-focused HTTP Primer

[HTTPS](https://howhttps.works/)
[How HTTPS works](https://howhttps.works/why-do-we-need-https/)

## HTTPS

[Mediocre Engineer's Guide to HTTPS | Hacker News](https://news.ycombinator.com/item?id=40482799)
[Mediocre Engineer’s guide to HTTPS](https://devonperoutky.super.site/blog-posts/mediocre-engineers-guide-to-https)

[HTTPS in the real world](https://robertheaton.com/2018/11/28/https-in-the-real-world/)
great tutorial explain how HTTPS works in the real world.

## mobile web dev

[GitHub - elharony/google-mobile-web-specialist-certification-guide: If you are looking for becoming a Mobile Web Specialist by Google, this guide will be your best friend in your journey](https://github.com/elharony/google-mobile-web-specialist-certification-guide)

[GitHub - awesome-mws/udacity-mws-nd: A curated list of awesome resources for Udacity's MWS ND](https://github.com/awesome-mws/udacity-mws-nd)

## url vs uri

[Unveiling URI, URL, and URN | Hacker News](https://news.ycombinator.com/item?id=40689137)
[Unveiling URI, URL, and URN](https://blog.logto.io/unveiling-uri-url-and-urn/)

[Daniel Miessler](https://danielmiessler.com/study/url-uri/)
The Difference Between URLs and URIs

## web design in general

[The modern web design process: creating sitemaps and wireframes](https://webflow.com/blog/the-modern-web-design-process-creating-sitemaps-and-wireframes)

## web dev

[Free Web Development Bootcamp - Class Central](https://www.classcentral.com/report/webdev-bootcamp/)

[LandChad](https://landchad.net/)
Site Development Guide

[Agernic](https://www.agernic.com/)
Web Design Courses

[web.dev](https://web.dev/)
helps developers like you learn and apply the web's modern capabilities to your own sites and apps.

[Build an Accessible Web App with HTML, Sass, and JavaScript](https://www.freecodecamp.org/news/build-an-accessible-web-app-with-html-sass-and-javascript)

[developedbyed - YouTube](https://www.youtube.com/channel/UClb90NQQcskPUGDIXsQEz5Q)

[How to Learn Web Development in 2021 - a Web Developer Roadmap](https://www.freecodecamp.org/news/how-to-learn-web-dev-in-2021-roadmap)

[IliasHad/Developer-Tools-and-Resources: The Best Tools and Resources for developers](https://github.com/IliasHad/Developer-Tools-and-Resources)
[Developers Tools & Resources - All Tools and Resources For Developers In One Place](https://www.producthunt.com/products/developers-tools-resources#developers-tools-resources)

[illustrated.dev](https://illustrated.dev/)
Web development, illustrated.

[Bad Website Club](https://badwebsite.club/)

[The Odin Project - Web Development 101](https://www.theodinproject.com/courses/web-development-101)

[GitHub - nishi1401/WebD_Exploration_Cohort: This repo is a part of the Web Development Exploration Cohort by Lean In IGDTUW. The cohort is for selected mentees, but this repo can be a useful resource to anyone interested in getting started with Web Developement :)](https://github.com/nishi1401/WebD_Exploration_Cohort)

[Web Hosting Glossary](https://manage.accuwebhosting.com/knowledgebase/584/Web-Hosting-Glossary.html)

[Web Tools Directory: 20+ Free Tools to Improve your Website](https://www.websiteplanet.com/webtools/)
[How to Build a Website in 2023: Complete Step-by-Step Guide](https://www.websiteplanet.com)
Site Development Tools
[RedirectTracker](https://www.websiteplanet.com/webtools/redirected/)
Resolve link redirects with this redirect detective tool. Trace any link with 301, 302 redirects. Test where goes a URL with this free online tool. Get instant results now!

[GitHub - WebDevsCom/webDevsCom: All kinds of resources for Developers in one place.](https://github.com/WebDevsCom/webDevsCom)

[GitHub - Uvacoder/abc-webdev-resources](https://github.com/Uvacoder/abc-webdev-resources)

[GitHub - NowYouKnowProgramming/webdev-learning-materials: Don't waste time - the highest quality resource hub for web developers (and not only!)](https://github.com/NowYouKnowProgramming/webdev-learning-materials)

[GitHub - fabiocicerchia/dev-learning-path: Developer's Learning Path | List of great resources.](https://github.com/fabiocicerchia/dev-learning-path)

[Amishakumari544/Web-Dev-Helper: Developer Helper where you can find all resources related to open source and software developer resources](https://github.com/Amishakumari544/Web-Dev-Helper)

[autumnchris/resources-for-web-developers: An ongoing collective list of recommended resources for web developers. The vast majority of which are free, though some, however, are paid.](https://github.com/autumnchris/resources-for-web-developers)

[GitHub - feimosi/web-development-learning-resources: Resources to become a senior web developer](https://github.com/feimosi/web-development-learning-resources)

[GitHub - iamismile/web-dev-resources: The complete web development resources you ever need. More than 150+ resources for your web development.](https://github.com/iamismile/web-dev-resources)

[GitHub - ivqonsanada/awesome-web-developer: My Web Developer Awesome List](https://github.com/ivqonsanada/awesome-web-developer)

[GitHub - leocaseiro/Awesome-Online-Web-Development-Courses-List: The Definitive List of Online Web Development Courses](https://github.com/leocaseiro/Awesome-Online-Web-Development-Courses-List)

[GitHub - mdmarufsarker/Full-Stack-Web-Development-Resources: This resource is collected from HM Nayem's Full-stack Web Development](https://github.com/mdmarufsarker/Full-Stack-Web-Development-Resources)
[Full Stack Web Development Resources](https://mdmarufsarker.github.io/Full-Stack-Web-Development-Resources/)

[GitHub - bmorelli25/Become-A-Full-Stack-Web-Developer: Free resources for learning Full Stack Web Development](https://github.com/bmorelli25/Become-A-Full-Stack-Web-Developer)

[Best Udemy courses for learning Full Stack Web Development | by Brandon Morelli | codeburst](https://codeburst.io/best-udemy-courses-for-learning-full-stack-web-development-45e2bd3ec28b)

[GitHub - mguery/web-dev: Web Developer Tools and Resources](https://github.com/mguery/web-dev)

[GitHub - mtdvio/web-development-resources: A list of useful resources for Web Developers! Put it in your bookmarks and contribute something](https://github.com/mtdvio/web-development-resources)

[GitHub - myshov/awesome-mobile-web-development: All that you need to create a great mobile web experience](https://github.com/myshov/awesome-mobile-web-development)

[GitHub - sandip2224/Best-Web-Development-Resources: Curated list of awesome resources for developers.](https://github.com/sandip2224/Best-Web-Development-Resources)

[GitHub - UNO-Coders/Web-Development: Created this new Repository for Open Source Contribution for Beginners](https://github.com/UNO-Coders/Web-Development)

[GitHub - krishnadevz/OpensourceResources: Free opensource Learning Resources related to Web-Development A to Z](https://github.com/krishnadevz/OpensourceResources)

[GitHub - NARKOZ/guides: Design and development guides](https://github.com/NARKOZ/guides)

[Free Web Development Resources](https://markodenic.com/free-web-development-resources/)

## web dev - responsive design

[Learn Responsive Design](https://web.dev/learn/design/)

[FreeCodeCamp Responsive Web Design](https://www.freecodecamp.org/learn/2022/responsive-web-design/)

[Ethan Marcotte's articles on A List Apart](http://alistapart.com/author/emarcotte)
[responsive web design](http://alistapart.com/article/responsive-web-design)

[Luke Wroblewski's interesting presentations](http://www.lukew.com/presos/)

[Scaling User Interfaces](http://www.nngroup.com/articles/scaling-user-interfaces/)

[Creating a mobile-first responsive web design](http://www.html5rocks.com/en/mobile/responsivedesign/)

[Responsive Design is…](http://responsivedesign.is/)
[Am I Responsive](http://ami.responsivedesign.is/)
Responsive Design Checker

[Responsive Design Checker](http://responsivedesignchecker.com/)
Test how responsive your website design is with this free tool. Check if your website fits and adapts to mobile, tablet, and desktop screen sizes.

[RWD Tutorials](http://www.creativebloq.com/rwd/responsive-web-design-tutorials-71410085)

[Responsive Web Design - How to Make a Website Look Good on Phones and Tablets](https://www.freecodecamp.org/news/responsive-web-design-how-to-make-a-website-look-good-on-phones-and-tablets)

[Building a better responsive website](http://www.smashingmagazine.com/2013/03/05/building-a-better-responsive-website/)

[Screen Sizes | Viewport Sizes and Pixel Densities for Popular Devices](https://screensiz.es/)
Screen Size Database
[full list of devices and their resolutions](http://screensiz.es/about)

[Device agnostic breakpoints](http://www.smashingmagazine.com/2012/03/22/device-agnostic-approach-to-responsive-web-design/)

[State of the Web](http://www.zeldman.com/2011/12/29/state-of-the-web-of-apps-devices-and-breakpoints/)

[Natural responsive web design breakpoints](http://marcdrummond.com/responsive-web-design/2011/12/29/default-breakpoints-are-dead)

[Re-thinking breakpoints in responsive design](https://www.palantir.net/blog/re-thinking-breakpoints-responsive-design)

[Atomic Design | Brad Frost](https://bradfrost.com/blog/post/atomic-web-design/)
Atomic Web Design
[I have no idea what the hell I am doing](http://bradfrost.com/blog/post/i-have-no-idea-what-the-hell-i-am-doing/)

[Responsive Images tutorial on MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

[Complete guide to Media Queries](https://polypane.app/blog/the-complete-guide-to-css-media-queries/)

[HTML Responsive Web Design](https://www.w3schools.com/html/html_responsive.asp)

[How to Make a Website Responsive in Just 15 Minutes](https://1stwebdesigner.com/responsive-website-tutorial/)

## zip bombs

[Christian Haschek](https://blog.haschek.at/2017/how-to-defend-your-website-with-zip-bombs.html)
(2017) How to defend your website with ZIP bombs

## HTTP

[Extreme HTTP Performance Tuning | Hacker News](https://news.ycombinator.com/item?id=27226382)
[Extreme HTTP Performance Tuning: 1.2M API req/s on a 4 vCPU EC2 Instance | talawah.io](https://talawah.io/blog/extreme-http-performance-tuning-one-point-two-million/)

[HTTP headers for the responsible developer | Hacker News](https://news.ycombinator.com/item?id=19856419)
[HTTP headers for the responsible developer | Twilio](https://www.twilio.com/en-us/blog/a-http-headers-for-the-responsible-developer)

[HTTPWTF | Hacker News](https://news.ycombinator.com/item?id=26343577)
[HTTPWTF](https://httptoolkit.com/blog/http-wtf/)

[Marvin Pinto](https://disjoint.ca/til/2016/05/17/how-to-determine-the-file-size-of-a-remote-http-object/)
(2016) How to determine the file size of a remote HTTP object

## Apache mod_rewrite

[SSL Shopper](https://www.sslshopper.com/apache-redirect-http-to-https.html)
Apache Redirect HTTP to HTTPS using mod_rewrite

[Apache Docs](https://httpd.apache.org/docs/2.4/en/rewrite/remapping.html)
Redirecting and Remapping with mod_rewrite

## component library

[What is a Component Library? When to Build Your Own and When to Use Someone Else's](https://www.freecodecamp.org/news/what-is-a-component-library-when-to-build-your-own/)

## cron jobs

[Tom Ryder](https://sanctum.geek.nz/arabesque/cron-best-practices/)
(2016) Cron best practices

## curl

[--libcurl | Hacker News](https://news.ycombinator.com/item?id=39175873)
[Introduction - everything curl](https://everything.curl.dev/)

## Dat protocol

[Dat Protocol Foundation](https://dat.foundation)

[How the Dat Protocol Works | Hacker News](https://news.ycombinator.com/item?id=20363813)
[How Dat Works](https://web.archive.org/web/20190220035955/https://datprotocol.github.io/how-dat-works/)

## deploying websites

[How to Deploy Your Websites and Apps - User-Friendly Deployment Strategies](https://www.freecodecamp.org/news/how-to-deploy-websites-and-applications/)

## domains - DNS

[How DNS Works](https://howdns.works/)
[How DNS Works](https://www.youtube.com/watch?v=3eqEl6scOvw)
a fun and colorful explanation of how DNS works.

[Quickly set DNS servers of your Internet connection on Windows](https://www.nirsoft.net/utils/quick_set_dns.html)

[How to Stop and Prevent DNS Leaks - VPN Critic](https://vpncritic.com/how-to-stop-and-prevent-dns-leaks)

[Learning DNS in 10 Years | Hacker News](https://news.ycombinator.com/item?id=35870654)
[New talk: Learning DNS in 10 years](https://jvns.ca/blog/2023/05/08/new-talk-learning-dns-in-10-years/)

[Implement DNS in a Weekend | Hacker News](https://news.ycombinator.com/item?id=35916064)
[Implement DNS in a weekend](https://implement-dns.wizardzines.com/)

[Linux Troubleshooting 101 , 2016 Edition](https://krisbuytaert.be/blog/linux-troubleshooting-101-2016-edition/index.html)
everything is a DNS Problem...

[Understand DNS Propagation & Why it Takes so Long - SiteGround KB](https://www.siteground.com/kb/dns-propagation/)

[Unbound DNS Tutorial](https://calomel.org/unbound_dns.html)
a validating, recursive, and caching DNS server.

[Knot Resolver on Fedora](https://www.ctrl.blog/entry/knot-dns-resolver-tutorial.html)
how to get faster and more secure DNS resolution with Knot Resolver on Fedora.

[DNS Servers](https://zwischenzugs.com/2018/01/26/how-and-why-i-run-my-own-dns-servers/)
how (and why) i run my own DNS Servers.

[Christophe Vanlancker](https://carroarmato0.wordpress.com/2012/04/30/how-to-change-dns-in-dhcp-on-the-bbox2/)
(2012) How to change DNS in DHCP on the BBox2

[Daniel Miessler](https://danielmiessler.com/study/dns/)
A DNS Primer

[Michael Buckbee](https://blog.varonis.com/definitive-guide-to-dns-ttl-settings/)
Definitive Guide to DNS TTL Settings

## domains - DNS - DoH

[DNS-over-HTTPS](https://www.aaflalo.me/2018/10/tutorial-setup-dns-over-https-server/)
tutorial to setup your own DNS-over-HTTPS (DoH) server.

[dns-over-https](https://hacks.mozilla.org/2018/05/a-cartoon-intro-to-dns-over-https/)
a cartoon intro to DNS over HTTPS.

[Mozilla's DNS over HTTPs | Hacker News](https://news.ycombinator.com/item?id=22412409)
[The Facts: Mozilla's DNS over HTTPs (DoH) - Open Policy & Advocacy](https://blog.mozilla.org/netpolicy/2020/02/25/the-facts-mozillas-dns-over-https-doh/)

[Trusted Recursive Resolver - MozillaWiki](https://wiki.mozilla.org/Trusted_Recursive_Resolver)

## domains - DNSSEC

[DNSSEC](https://howdnssec.works/)

[What is DNS Security? | DNSSEC | Cloudflare](https://www.cloudflare.com/learning/dns/dns-security/)

## domains - URL

[The History of the URL](https://blog.cloudflare.com/the-history-of-the-url)

## Firebase

[GitHub - jthegedus/awesome-firebase: List of Firebase talks, tools, examples & articles! Translations in Contributions welcome!](https://github.com/jthegedus/awesome-firebase)

[How to Build a Google Docs Clone with React, Material UI, & Firebase](https://www.freecodecamp.org/news/build-a-google-docs-clone-with-react-and-firebase)

## GDPR

[Bozhidar Bozhanov](https://techblog.bozho.net/gdpr-practical-guide-developers/)
(2017) GDPR – A Practical Guide For Developers

## Gemini protocol

[Project Gemini](https://geminiprotocol.net/)

[GitHub - kr1sp1n/awesome-gemini: A collection of awesome things regarding the gemini protocol ecosystem.](https://github.com/kr1sp1n/awesome-gemini)

## global directory

[Global Directory Adventures](http://globaldir.arpa2.net)

## Gopher protocol

[The TCP/IP Guide - Gopher Protocol (Gopher)](http://www.tcpipguide.com/free/t_GopherProtocolGopher.htm)

## headers

[CSRF, CORS, and HTTP Security Headers Demystified | Hacker News](https://news.ycombinator.com/item?id=26984701)
[CSRF, CORS, and HTTP Security headers Demystified](https://blog.vnaik.com/posts/web-attacks.html)

## htaccess

[AskApache](https://www.askapache.com/htaccess/)
THE Ultimate .htaccess tutorial with 100's of Examples
This is a guide for using htaccess to the fullest.
[Htaccess Files from GitHub](https://www.askapache.com/htaccess-file/)

## HTTP - gRPC

[GitHub - grpc-ecosystem/awesome-grpc: A curated list of useful resources for gRPC](https://github.com/grpc-ecosystem/awesome-grpc)

## instantmessengers - IRC and XDCC

[XDCC Tutorial](http://theloadguru.com/xdcc-irc-beginners-guide/)
XDCC Downloading For Beginners: Do It Like A Pro!.

[guides/IRC.md at master · mayfrost/guides · GitHub](https://github.com/mayfrost/guides/blob/master/IRC.md)
[guides/VIDEO.md at master · mayfrost/guides · GitHub](https://github.com/mayfrost/guides/blob/master/VIDEO.md)

The IRC Rite of Passage
   /server -ssl irc.rizon.net 6697
      /join /g/punk
      /join /g/sec
      /join nfo

[XDCC](https://en.wikipedia.org/wiki/XDCC)
XDCC (Xabi DCC or eXtended DCC) - is a computer file sharing method which uses the Internet Relay Chat (IRC) - network as a host service.

[Internet Relay Chat Help](https://www.irchelp.org/)

[The Load Guru](http://theloadguru.com/how-to-get-started-with-xdcc/)
How To Get Started With XDCC

[The Load Guru](http://theloadguru.com/how-to-configure-mirc/)
How To Configure mIRC For Downloading

## instantmessengers

[How to build large-scale end-to-end encrypted group video calls | Hacker News](https://news.ycombinator.com/item?id=29570938)

## instantmessengers - XMPP

[IRC vs XMPP: Comparing Instant Messaging Protocol](https://www.cometchat.com/blog/irc-vs-xmpp-instant-messaging-protocol-comparison)

## IoT

[GitHub - microsoft/IoT-For-Beginners: 12 Weeks, 24 Lessons, IoT for All!](https://github.com/microsoft/IoT-For-Beginners)

[Troy Hunt: IoT Unravelled Part 1: It's a Mess... But Then There's Home Assistant](https://www.troyhunt.com/iot-unravelled-part-1-its-a-mess-but-then-theres-home-assistant)
[Troy Hunt: IoT Unravelled Part 2: IP Addresses, Network, Zigbee, Custom Firmware and Soldering](https://www.troyhunt.com/iot-unravelled-part-2-ip-addresses-network-zigbee-custom-firmware-and-soldering)
[Troy Hunt: IoT Unravelled Part 3: Security](https://www.troyhunt.com/iot-unravelled-part-3-security)
[Troy Hunt: IoT Unravelled Part 4: Making it All Work for Humans](https://www.troyhunt.com/iot-unravelled-part-4-making-it-all-work-for-humans)
[Troy Hunt](https://www.troyhunt.com/)
web security expert known for public education and outreach on security topics.

[GitHub - HQarroum/awesome-iot: A curated list of awesome Internet of Things projects and resources.](https://github.com/HQarroum/awesome-iot)

[GitHub - phodal/awesome-iot: Awesome IoT. A collaborative list of great resources about IoT Framework, Library, OS, Platform](https://github.com/phodal/awesome-iot)

## IoT_security

[GitHub - fkie-cad/awesome-embedded-and-iot-security: A curated list of awesome embedded and IoT security resources.](https://github.com/fkie-cad/awesome-embedded-and-iot-security)

[GitHub - nebgnahz/awesome-iot-hacks: A Collection of Hacks in IoT Space so that we can address them (hopefully).](https://github.com/nebgnahz/awesome-iot-hacks)

## IP

[What can you really do with someone's IP? : HowToHack](https://old.reddit.com/r/HowToHack/comments/v5tldl/what_can_you_really_do_with_someones_ip)

[Show HN: IP Guide - Info on IP addresses, Networks, and ASNs | Hacker News](https://news.ycombinator.com/item?id=38409164)
[IP Guide: Look up IP, Network, and ASN data](https://ip.guide/)

[There's more than one way to write an IP address (2019) | Hacker News](https://news.ycombinator.com/item?id=35744130)
[There's more than one way to write an IP address](https://ma.ttias.be/theres-more-than-one-way-to-write-an-ip-address/)

## IP - netcat

[Netcat - All you need to know | Hacker News](https://news.ycombinator.com/item?id=27973020)
[Netcat - All you need to know ::](https://blog.ikuamike.io/posts/2021/netcat/)

## link tags

[Preload, prefetch and other tags: what they do and when to use them](https://3perf.com/blog/link-rels)

## MVC framework

[MVC Framework Introduction - GeeksforGeeks](https://www.geeksforgeeks.org/mvc-framework-introduction/)

## rsync

[rsync - Wikipedia](https://en.wikipedia.org/wiki/Rsync)

[How does rsync work? | Hacker News](https://news.ycombinator.com/item?id=31958536)
[rsync, article 3: How does rsync work? (2022) - Michael Stapelberg](https://michael.stapelberg.ch/posts/2022-07-02-rsync-how-does-it-work/)

## speculative loading

[Speculative Loading can boost your WordPress site’s page speed](https://www.accuwebhosting.com/blog/speculative-loading-wordpress/?mc_cid=8e2445d623)

## stacks - FARM

[Use the FARM Stack to Develop Full Stack Apps](https://www.freecodecamp.org/news/use-the-farm-stack-to-develop-full-stack-apps/)

## stacks - JAMstack

[What is the JAMstack and how do I get started?](https://www.freecodecamp.org/news/what-is-the-jamstack-and-how-do-i-host-my-website-on-it)

[GitHub - BolajiAyodeji/awesome-jamstack: Curated list of resources: books, videos, articles, speaker decks, tools about using the Jamstack.](https://github.com/BolajiAyodeji/awesome-jamstack)

[automata/awesome-jamstack: Carefully curated list of awesome Jamstack resources](https://github.com/automata/awesome-jamstack)

## stacks - MERN

[MERN Stack Roadmap - How to Learn MERN and Become a Full-Stack Developer](https://www.freecodecamp.org/news/mern-stack-roadmap-what-you-need-to-know-to-build-full-stack-apps/)

[How to Build a MERN Stack To-Do App](https://www.freecodecamp.org/news/how-to-build-a-mern-stack-to-do-app/)

## streaming - webdav

[fstanis/awesome-webdav: A curated list of awesome apps that support WebDAV and tools related to it.](https://github.com/fstanis/awesome-webdav)

## TCP-IP

[Let's code a TCP/IP stack (2016) | Hacker News](https://news.ycombinator.com/item?id=27654182)
[Let's code a TCP/IP stack, 1: Ethernet & ARP](https://www.saminiir.com/lets-code-tcp-ip-stack-1-ethernet-arp/)
great stuff to learn network and system programming at a deeper level.

[The TCP/IP Guide - Table Of Contents](http://www.tcpipguide.com/free/t_toc.htm)

## TCP

[How to enable TCP BBR to improve network speed on Linux | TechRepublic](https://www.techrepublic.com/article/how-to-enable-tcp-bbr-to-improve-network-speed-on-linux/)

## urls

[Redd-Developer/howurls.work: Learn how URLs work by visually inspecting their structure.](https://github.com/Redd-Developer/howurls.work)

## web components - BEM

[GitHub - sturobson/BEM-resources: Just a repo full of BEM resources](https://github.com/sturobson/BEM-resources?tab=readme-ov-file)

## web dev - local-first

[Local-First Web Development | Hacker News](https://news.ycombinator.com/item?id=34857435)
[Local-First Web Development](https://localfirstweb.dev/)

## web dev - performance improvement

[GitHub - davidsonfellipe/awesome-wpo: A curated list of Web Performance Optimization. Everyone can contribute here!](https://github.com/davidsonfellipe/awesome-wpo)

## web dev - semantic and microformats

[Pursuing semantic value](http://adactio.com/journal/4999/)
(mandatory)

[Introduction to the semantic web](https://www.cambridgesemantics.com/blog/semantic-university/intro-semantic-web/)

[Semantic code: What? Why? How?](https://boagworld.com/dev/semantic-code-what-why-how/)

[Diving into HTML5](http://diveintohtml5.info/table-of-contents.html)

[Microformats primer - Sitepoint](https://www.sitepoint.com/microformats-meaning-markup/)
(mandatory)

[Get started with Microformats](http://microformats.org/wiki/get-started)

[Microformats v2](http://microformats.org/2014/03/05/getting-started-with-microformats2)

[GitHub - semantalytics/awesome-semantic-web: A curated list of various semantic web and linked data resources.](https://github.com/semantalytics/awesome-semantic-web)

## web dev - templating - angular

[AngularJS](https://docs.angularjs.org/guide/templates)

[AngularJS](https://docs.angularjs.org/tutorial/step_02)

[Single Page Apps with AngularJS Routing and Templating | DigitalOcean](https://www.digitalocean.com/community/tutorials/single-page-apps-with-angularjs-routing-and-templating)
(JS)

## webhooks - IFTTT

[IFTTT: If-This-Then-That FAQ](https://automatelife.net/ifttt-if-this-then-that-faq/)

[IFTTT An Introduction](https://www.c-sharpcorner.com/UploadFile/f55fd9/ifttt-an-introduction/)

[Fully automated location-based work hours log using IFTTT and Background Triggers](https://www.pushcut.io/guides/iftttwebhook.html)

## webhooks

[How to Configure Webhooks in GitHub? [Step-by-Step] - Magefan](https://magefan.com/blog/configure-webhooks-in-github)

[What is a Webhook?](https://ifttt.com/explore/what-is-a-webhook)

[IFTTT Webhook Integration: A Complete 7 Step Guide to Connect your Favourite Apps](https://hevodata.com/learn/ifttt-webhook/)

## web hosting servers - cloud seedboxes

[Seedbox Guide: Seedbox Providers Comparison](https://seedboxgui.de/)
Comparison tool to help you find the best fitting Seedbox.
[What is a seedbox?](https://seedboxgui.de/guides/what-is-a-seedbox/)

[Paying Money to Steal Movies & Music on the Internet](https://ryanlue.com/posts/2019-03-29-paying-money-to-steal-movies)

## web hosting servers

[Bulletproof Hosting](https://en.wikipedia.org/wiki/Bulletproof_hosting)

[Value-Added Resellers (VAR) - Overview, Brand Performance](https://corporatefinanceinstitute.com/resources/management/value-added-resellers-var)

## web hosting software

[aleron75/mageres: A list of useful Magento technical resources](https://github.com/aleron75/mageres)

[GitHub - run-as-root/awesome-magento2: Curated list of awesome Magento 2 Extensions, Resources and other Highlights](https://github.com/run-as-root/awesome-magento2)

## WebRTC

[Show HN: Learn how WebRTC actually works. A book on the protocols, not just APIs | Hacker News](https://news.ycombinator.com/item?id=24323589)
[Introduction | WebRTC for the Curious](https://webrtcforthecurious.com/)
[GitHub - webrtc-for-the-curious/webrtc-for-the-curious: WebRTC for the Curious: Go beyond the APIs](https://github.com/webrtc-for-the-curious/webrtc-for-the-curious)

[Everything You Ever Wanted to Know About WebRTC](https://blog.openreplay.com/everything-you-ever-wanted-to-know-about-webrtc)

## web security

[GitHub - qazbnm456/awesome-web-security: A curated list of Web Security materials and resources.](https://github.com/qazbnm456/awesome-web-security)
list of Web Security materials and resources.
a curated list of Web Security materials and resources.

## web server software

[GitHub - imthenachoman/How-To-Secure-A-Linux-Server: An evolving how-to guide for securing a Linux server.](https://github.com/imthenachoman/How-To-Secure-A-Linux-Server)

## website - scrapers and archivers

[How to Archive Open Source Materials](https://www.bellingcat.com/resources/how-tos/2018/02/22/archive-open-source-materials/)
Pro: Has institutional back, and is therefore likely to stick around for a long time.

[How I Built a Web Scraper with Beautiful Soup and Used it to Land My First Job](https://www.freecodecamp.org/news/how-i-used-a-side-project-to-land-a-job)

[GitHub - christian-bromann/awesome-selenium: A curated list of delightful Selenium resources.](https://github.com/christian-bromann/awesome-selenium)
[Web automation: Don't use Selenium, use Playwright | Hacker News](https://news.ycombinator.com/item?id=33537772)
[Web Automation: Don't Use Selenium, Use Playwright](https://new.pythonforengineers.com/blog/web-automation-dont-use-selenium-use-playwright/)
Selenium is an open source user acceptance testing tool for web applications. It allows you to simulate user actions by automating the browser via JavaScript.
Firefox browser plug-in called Selenium IDE. Selenium IDE allows you to record your interaction with a web application as a Selenium script, which you can play back through Selenium's TestRunner or through Selenium IDE itself. While this is useful when creating tests, it is invaluable if you need to automate your interaction with a web application.

[Web Scraping in Python - The Complete Guide | Hacker News](https://news.ycombinator.com/item?id=39442273)
[Web Scraping in Python - The Complete Guide | ProxiesAPI](https://proxiesapi.com/articles/web-scraping-in-python-the-complete-guide)

## website - scrapers and archivers - The Internet Archive

[Julia Geist](https://hackernoon.com/guide-to-handling-internet-archives-cdx-server-api-response-c469df5b81f4)
(2017) Guide to Handling Internet Archive’s CDX Server API Response. Examples:
 * `http://web.archive.org/cdx/search/cdx?limit=1&showResumeKey=true&url=<URL>`
 * `https://archive.org/wayback/available?timestamp=19010101010101&url=<URL>`

## website - scraping

[Web Scraping Tutorial](https://github.com/MorvanZhou/easy-scraping-tutorial)

[GitHub - iipc/awesome-web-archiving: An Awesome List for getting started with web archiving](https://github.com/iipc/awesome-web-archiving)

[GitHub - BruceDone/awesome-crawler: A collection of awesome web crawler,spider in different languages](https://github.com/BruceDone/awesome-crawler)
