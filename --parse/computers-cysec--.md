
NOTE: THIS IS TL;DR CYBERSECURITY
- the Security page will be more complete
- focus on basic aspects of what non-tech people want to know

PRINCIPLE THAT MAY GO TO SECURITY OR CYSEC, MAYBE GIS
- One way to protect against invasion is to have multiple barriers, with degrees of safety for each
- e.g., subsidiary corporations that can get sued without the parent company being affected
- e.g., city walls in layers toward the government center
- e.g., multiple firewalls with different encryptions each layer

if you're particularly paranoid, make sure to change your devices' MAC address, since that MAC has the origination and likely information about the firmware on it

Have a burner browser
- Even if you use privacy-minded things in a browser (e.g. private windows, no cookies), some services detect this.
- For this reason, have a "burner" browser that has absolutely nothing in it
- Preferably, it should use a different framework (e.g., Firefox uses Gecko, so use Chromium w/ Brave)

Identity theft protection
- On average, it takes 800 hours to resolve identity fraud.
    - Good protection services will assign a counselor to clean up the mess.
- Don't get ID theft protection that only monitors credit reports.
    - Several popular services like [Credit Karma](https://www.creditkarma.com/) will monitor credit for free.
- identity theft insurance can often be part of the ID theft protection package - https://www.cnbc.com/select/id-theft-insurance/

With peer-to-peer payments (P2P), you can transfer money to someone from your bank account, debit card, or credit card using a website or mobile app such as Zelle, Cash App, PayPal, or Venmo. P2P payments can also include your financial institution's apps, such as Schwab Mobile. While P2P payments are popular and convenient, understanding the risks can help you avoid becoming a victim of scams and fraud.

How do scams and fraud differ?
Fraud involves someone accessing your account without your permission and completing unauthorized transactions. A scam involves being tricked into authorizing a transaction or sending a payment. It's important to remember the difference, as the same protections do not always apply to both.

In general, be VERY vigilant about the information you enter, and consider how it makes any sense to get used
Do NOT enter your credit card info into something just because they need to "verify your age"
You don't need to "make a login" for a public site like wikipedia
those logins will often ask for extra information, much of which you shouldn't give away freely

The reason this is a big issue, EVEN IF THE COMPANY IS LEGITIMATE, is because your personal information is as safe as that company's server is safe from getting hacked
i.e., it can happen to anyone who wasn't paying attention to 1 setting in a computer somewhere and 1 teenage/incel found it

NOTE: when making any purchase online, MAKE ABSOLUTELY SURE that you're seeing the "lock" symbol in the top left
(must research what that actually means, I'm presuming a certified certificate)

FROM NORDVPN TEST
- Wifi:
    - secure password
    - disable SSID on router
    - WPA2/WPA3 encryption
    - enable MAC address filtering on router
- Password security???
- Malware causes:
    - opening random downloaded files
    - clicking on unknown links
    - visiting suspicious sites
    - opening emails from unknown sources
- IoT problems
    - no encryption
    - no-password access
    - no standards/regulation on many things
    - discreet audio/video recording

What information could do
- With your passport number, someone could:
    - Book an international flight as you
    - Apply for anything that requires proof of identity documentation with the government, e.g. Working with children check
    - Activate a SIM card (and so get an internet connection that's traceable to you, not them, hiding them from the government)
    - Create a fake physical passport from a template, with the correct passport number (which they then use to cross a border, open a bank account, or anything)
- with a password, soemoene could
- login to that particular computer (if 2FA wasn't enabled
- login to ANY other site that had the same password/email combo

CySec hardening concepts
- Disable/remove Native VLAN
- Check for redirects and diversions
    - #62* redirect
    - _#21# diversions_
    - _##002# remove redirections_
- _Packet analyzer for phones_
    - _##197328640#_#
    - UMTS RR Information (cell ID#)
    - MM Info > Serving PLMN (area code)
    - Netmonitor website (OpenCellID, e.g.)
- Record all relevant information
    - IMEIs of all devices #06#

Dial *67 in North America to make calls labeled as anonymous

We can apply obfuscation in our own lives by using practices and technologies that make use of it, including:
- The secure browser Tor, which (among other anti-surveillance technologies) muddles our Internet activity with that of other Tor users, concealing our trail in that of many others.
- The browser plugins TrackMeNot and AdNauseam, which explore obfuscation techniques by issuing many fake search requests and loading and clicking every ad, respectively.
- The browser extension Go Rando, which randomly chooses your emotional "reactions" on Facebook, interfering with their emotional profiling and analysis.
- Playful experiments like Adam Harvey's "HyperFace" project, finding patterns on textiles that fool facial recognition systems - not by hiding your face, but by creating the illusion of many faces.

Web content is frequently insecure because it's often a hybrid of secure AND insecure elements
- this is especially egregious with web forms, which can send insecure content EVEN WHEN IT'S A HTTPS SITE!

Plan for a catastrophic laptop crash, with either a USB drive or a recovery partition.

[Gen Z falls for online scams more than their boomer grandparents do : technology](https://old.reddit.com/r/technology/comments/16rdi9s/gen_z_falls_for_online_scams_more_than_their/)
- the best cure for tech safety is experience

CYSEC TIP:
Post-it note/sticker over built-in camera

## privacy

NOTE: will connect to other non-TS page?

Privacy and complete freedom are inversely connected
- if everyone has privacy, there's the opportunity for injustice
- if everyone has freedom, there's technically no privacy
 
article on how there needs to be a tech version of attorney/client, doctor/patient privilege
- basically, there's too much [power] in the hands of these geeks that there must be a legally bound implicit standardized agreement
- without this, any random person can steal any information they want because copying computer information is EASIER than moving it

[Privacy is the most important concept of our time | Hacker News](https://news.ycombinator.com/item?id=24661271)
[Why Privacy Is the Most Important Concept of Our Time - In Re](https://inre.me/why-privacy-is-the-most-important-concept-of-our-time/)

[Cover Your Tracks | Hacker News](https://news.ycombinator.com/item?id=25166703)
good dialogue on uniqueness
[Introducing Cover Your Tracks! | Electronic Frontier Foundation](https://www.eff.org/deeplinks/2020/11/introducing-cover-your-tracks)

[Privacy Is a Human Right | Hacker News](https://news.ycombinator.com/item?id=28997501)
[Privacy is a Human Right | The Tor Project](https://blog.torproject.org/privacy-is-a-human-right/)

[Cops Are Suing a Teen for Invasion of Privacy After False Arrest Vid Goes Viral | Hacker News](https://news.ycombinator.com/item?id=37956714)

[Internet Health](https://foundation.mozilla.org/en/internet-health/)

[Block YouTube ads on AppleTV by decrypting and stripping ads from Profobuf | Hacker News](https://news.ycombinator.com/item?id=37279109)
[Block YouTube Ads on AppleTV by Decrypting and Stripping Ads from Profobuf](https://ericdraken.com/pfsense-decrypt-ad-traffic/)

[When an app asks for permissions, it should have a "feed fake data" option | Hacker News](https://news.ycombinator.com/item?id=36644895)
[Nifflas: "When an app asks for permissio…" - Gamedev Mastodon](https://mastodon.gamedev.place/@Nifflas/110668040598715116)

[Privacy vs. "I have nothing to hide" (2019) | Hacker News](https://news.ycombinator.com/item?id=32835966)
[Privacy vs "I have nothing to hide" | Kev Quirk](https://kevquirk.com/privacy-vs-i-have-nothing-to-hide/)

[No user accounts, by design | Hacker News](https://news.ycombinator.com/item?id=30503482)
[No user accounts, by design | F-Droid - Free and Open Source Android App Repository](https://f-droid.org/en/2022/02/28/no-user-accounts-by-design.html)

[The case for banning children from social media | Hacker News](https://news.ycombinator.com/item?id=35447588)
[The Case for Banning Children from Social Media | The New Yorker](https://www.newyorker.com/news/our-columnists/the-case-for-banning-children-from-social-media)

[What is AT&T doing at 1111340002? | Hacker News](https://news.ycombinator.com/item?id=29135559)
[What is AT&T doing at 1111340002?](https://scribe.rip/telecom-expert/what-is-at-t-doing-at-1111340002-c418876c212c)

[Wearable Microphone Jamming | Hacker News](https://news.ycombinator.com/item?id=28885739)
[Wearable Microphone Jamming](https://sandlab.cs.uchicago.edu/jammer/)

[A single laser fired through a keyhole can expose everything inside a room | Hacker News](https://news.ycombinator.com/item?id=28466737)
[NLOS Keyhole Imaging Can See Inside a Closed Room](https://gizmodo.com/a-single-laser-fired-through-a-keyhole-can-expose-every-1847638281)

[Who Owns My Name? | Hacker News](https://news.ycombinator.com/item?id=28007547)
[Who Owns My Name?. Does my name belong to me? Does my… | by Amanda Knox | Medium](https://amandamarieknox.medium.com/who-owns-my-name-93561f83e502)

[Website Fingerprinting on Early QUIC Traffic | Hacker News](https://news.ycombinator.com/item?id=25969886)
[[2101.11871] Website fingerprinting on early QUIC traffic](https://arxiv.org/abs/2101.11871)

[Your computer should say what you tell it to say | Hacker News](https://news.ycombinator.com/item?id=37050035)
[Your Computer Should Say What You Tell It To Say | Electronic Frontier Foundation](https://www.eff.org/deeplinks/2023/08/your-computer-should-say-what-you-tell-it-say-1)

[Is Internet Privacy a Myth? - codepaste](https://codepaste.net/static-topic-4/)

[Ask HN: How do you trust that your personal machine is not compromised? | Hacker News](https://news.ycombinator.com/item?id=34388866)

### digital sovereignty

[5G: The outsourced elephant in the room | Hacker News](https://news.ycombinator.com/item?id=26843068)
[5G: The outsourced elephant in the room - Bert Hubert's writings](https://berthub.eu/articles/posts/5g-elephant-in-the-room/)

[Sov's Compendium](https://sovs.notion.site/Sov-s-Compendium-41f097d28dae4d09801f10cde1b2d03b)

[Your online identity is owned by your email provider (2019) | Hacker News](https://news.ycombinator.com/item?id=32563735)
[Your online identity is owned by your email provider | Ctrl blog](https://www.ctrl.blog/entry/email-identity-provider.html)

### privacy community

[Toolkits - Transparency.org](https://www.transparency.org/en/toolkits)
[Home - Transparency.org](https://www.transparency.org/en/)

[dig deeper](https://digdeeper.neocities.org/)
[dig deeper](https://web.archive.org/web/20210102182957/https://digdeeper.neocities.org/)
articles on privacy on/and the internet
[Dig Deeper](https://digdeeper.club/)

[Teaching Privacy |](https://teachingprivacy.org/)

### privacy news

[Latest Privacy](https://latestprivacy.org/)
[RestorePrivacy](https://restoreprivacy.com/category/news-reports/)
Privacy News

[/r/privacy](https://www.reddit.com/r/privacy/)
everything about privacy on reddit

[10 Best Antivirus Software in 2024: Windows, Android, iOS, Mac](https://www.safetydetectives.com/)

### privacy is important

[Mo Bitar](https://dev.to/bitario/privacy-is-power)
Privacy is Power

[You can opt out of airport face scans | Hacker News](https://news.ycombinator.com/item?id=41051327)
[Can you opt out of airport face scans? Yes! Here’s how. - Vox](https://www.vox.com/future-perfect/360952/summer-travel-airport-facial-recognition-scan)

[People Still Aren't Patched or Protected : cybersecurity](https://old.reddit.com/r/cybersecurity/comments/tz8q44/people_still_arent_patched_or_protected)

### privacy actions

[Data Detox Kit](https://datadetoxkit.org/en/home/)

[Sven Taylor](https://restoreprivacy.com/privacy-tools/)
(2021) Privacy Tools - How to restore your online privacy in 2021

[Tech Solidarity](http://techsolidarity.org/)
Basic Security Guide, do and don'ts for basic security when using a laptop and/or mobile device.
Here's a guide: [Basic Security Guide (Tech Solidarity)](https://techsolidarity.org/resources/basic_security.html)
free

[Surveillance Self-Defense](http://ssd.eff.org/)
Tips and methodologies for safe(r) online communications. - free

[Security in a Box](https://securityinabox.org/en/)
Digital security tools and tactics with step by step instructions
Security in a box guide advice on how to use social media and mobile phones more safely. The Tool Guides offer step-by-step instructions to help you install, configure and use some essential digital security software and services - free
[Security in a Box](http://bpo4ybbs2apk4sk4.onion/)

[EPIC EPIC Online Guide to Practical Privacy Tools](https://www.epic.org/privacy/tools.html)
The Electronic Privacy Information Center (EPIC) focuses public attention on emerging civil liberties, privacy, First Amendment issues and works to promote the Public Voice in decisions concerning the future of the Internet.

[Google](https://www.google.com/safetycenter/everyone/start/)
Google' guide : How to keep your stuff secure and private

[Fried](https://fried.com/privacy/)
introduction guide to online privacy. a bit outdated on some advices

[Privacy Guides](https://www.privacyguides.org/)
Look at the [Providers](https://www.privacyguides.org/providers/) and [Software](https://www.privacyguides.org/software/) sections to find their privacy first recommendations to a variety of services.

[Privacy Tools Guide: Website for Encrypted Software & Apps](https://www.privacytools.io)
[Best Private Web Browsers for Most Privacy in 2024](https://www.privacytools.io/private-browser)
[Privacy Tools Encryption Against Global Mass Surveillance](https://www.privacytools.io/classic)
"Encryption against global mass surveillance". Plenty of information to help protect your privacy online.
provides knowledge and tools to protect your privacy against global mass surveillance.
[PrivacyTools.io VPN Recommendations](https://www.privacytools.io/providers/vpn)
[Encrypted DNS Resolvers](https://www.privacytools.io/providers/dns/)
[Don't use Windows 10 It's a privacy nightmare](https://www.privacytools.io/operating-systems/#win10)
[GitHub - CKs-Technology-News/PrivacyTools: Privacy Tools by CKTN](https://github.com/CKs-Technology-News/PrivacyTools)
[Suggested search engines by PrivacyTools](https://www.privacytools.io/#search)
[/r/privacytoolsIO/](https://www.reddit.com/r/privacytoolsIO/)

[Aliza Vigderman & Gabe Turner](https://www.security.org/vpn/anonymity/)
(2021) How To Remain Anonymous on the Internet
Learn over 20 ways to stay as private as possible on the web.

[DuckDuckGo](https://spreadprivacy.com/privacy-tips/home)
Fix Tracking : how to stop getting tracked on desktop and mobile

[RestorePrivacy](https://restoreprivacy.com/)
Your online privacy resource center

[GitHub - yaelwrites/Big-Ass-Data-Broker-Opt-Out-List](https://github.com/yaelwrites/Big-Ass-Data-Broker-Opt-Out-List)
List of Data Broker Opt-Out Resources

[crixus / gofoss · GitLab](https://gitlab.com/curlycrixus/gofoss)

[Try This One Weird Trick Russian Hackers Hate | Hacker News](https://news.ycombinator.com/item?id=27183734)
[Try This One Weird Trick Russian Hackers Hate - Krebs on Security](https://krebsonsecurity.com/2021/05/try-this-one-weird-trick-russian-hackers-hate/)

[What is cyber hygiene? Important tips and best practices | Ally](https://www.ally.com/stories/security/cyber-hygiene-best-practices/)

[Personal Digital Security - How to Protect Yourself Online for Beginners](https://www.freecodecamp.org/news/personal-digital-security-an-intro)

[Protect Yourself From Onlline Tracking](https://www.privacyinternational.org/act/protect-yourself-online-tracking)
Privacy International's guide that recommends tools and extensions for Android, iOS, MacOS and Windows that protect you from online tracking. - free

## Ally message

Tips to protect yourself:

- Deny requests for a password. We'll never call you and ask for your Ally account password to verify your account. These scammers will.
- Ask questions. Asking questions like "When's the last time I called you?" may prompt the fraudster to hang up.
- Call us directly and [report fraud](https://click.alerts.ally.com/?qs=5af77452725c4636ed5637135eac1d6f130c488e054159f0689ec0c6573b837b1e6d26b2478ced8907c8136ec8a422dfc0e711f26d2745dc). If someone calls you for this information, hang up and call us at [1-833-226-1520](tel:1-833-226-1520) to report it.
- Stay aware. Fraudsters are constantly changing the ways they try to cheat you out of your money. Learn how to protect yourself against the latest [smishing and social media scams](https://click.alerts.ally.com/?qs=6c03eeac23189158b47e2ae67e25df5fb5a85d80a99b5c25b4f45d5350b97b903062f350307ab821879c8144b964fd25233847cedf175a51).

## Amazon message

## FROM AMAZON

## Protect yourself from scammers

#### Be careful installing apps or software

Amazon will not ask you to install an app or download software in order to receive a refund or to get help from customer service.

#### Never pay over the phone

Amazon will not ask you to provide payment information, including gift cards (or "verification cards," as some scammers call them), for products or services over the phone.

#### Always verify orders directly with Amazon

Amazon will not include purchased product information in order confirmation and shipping confirmation emails we send to customers. For any questions related to an order, always check [Your Orders](https://www.amazon.com/gp/r.html?C=KXX8UEOO2L0J&K=12GHWUZNHA36N&M=urn:rtn:msg:20230413213300bbdfeb49664147aa8b32ef065840p0na&R=3UD0C6AQLG944&T=C&U=https%3A%2F%2Fwww.amazon.com%2Fgp%2Fcss%2Forder-history%3Fref_%3Dpe_49013300_706024580_nav_orders_first&H=EODT2YJH4DW99CV5BQNO53EAEJOA&ref_=pe_49013300_706024580_nav_orders_first) on Amazon.com or via the "Amazon Shopping" app.

#### Be wary of false urgency

Amazon will not pressure you to act now. Scammers may try to create a sense of urgency to persuade you to do what they're asking.

If you receive communication - a call, text, or email - that you think may not be from Amazon, please report it to us at [amazon.com/reportascam](https://www.amazon.com/gp/f.html?C=KXX8UEOO2L0J&K=12GHWUZNHA36N&M=urn:rtn:msg:20230413213300bbdfeb49664147aa8b32ef065840p0na&R=3CL2RENF6CPXL&T=C&U=https%3A%2F%2Fwww.amazon.com%2Freportascam%3Fref_%3Dpe_49013300_706024580&H=TTMALS4DNEDP6YNKBG2AYHVE178A&ref_=pe_49013300_706024580)

Scammers are creative and they constantly devise new schemes, exploit new technologies and change tactics to avoid detection. Stay safe by learning to identify and avoid scams.

Prime membership scams: These are unexpected calls/texts/emails that refer to a costly membership fee or an issue with your membership and ask you to confirm or cancel the charge. These scammers try to convince you to provide payment or bank account information in order to reinstate a membership.

Amazon will never ask you to provide payment information for products or services over the phone. Visit the Message Center on Amazon.com or on our app to review authentic emails from Amazon. To verify your Prime Membership status or make payments, log into your Amazon account, and go to Your Account._
Account suspension/Deletion scams: Scammers send texts, emails and phone calls stating that your account will be suspended or deleted and prompt you to click on a fraudulent link or verbally provide information to "verify your account." Customers who land on these pages or receive these phone calls are then lured to provide account information such as payment information or account login credentials.
Amazon will never ask you to disclose your password or verify sensitive personal information over the phone or on any website other than Amazon.com. Please do not click on any links or provide your information to anyone over the phone without authenticating the email or phone call. If you have questions about the status of your account, go directly to Amazon.com or on our app to view your account details, including the Message Center which displays a log of communications sent from Amazon._
Here are some important tips to identify scams and keep your account and information safe:
1. Trust Amazon-owned channels. Always go through the Amazon mobile app or website when seeking customer service, tech support, or when looking to make changes to your account.
2. Be wary of false urgency. Scammers may try to create a sense of urgency to persuade you to do what they're asking. Be wary any time someone tries to convince you that you must act now.
3. Never pay over the phone. Amazon will never ask you to provide payment information, including gift cards (or "verification cards," as some scammers call them) for products or services over the phone.
4. Verify links first. Legitimate Amazon websites contain "amazon.com" or "amazon.com/support." Go directly to our website when seeking help with Amazon devices/services, orders or to make changes to your account.|

## balancing trust

[What is a Parallel Economy? [A Road Map] - Citizen Xero](https://citizenxero.com/what-is-a-parallel-economy)

[There's a Good Chance Someone You Love Snoops on Your Phone | PCMag](https://www.pcmag.com/news/theres-a-good-chance-someone-you-love-snoops-on-your-phone?taid=6464c550c5e5b700013d8753)

## Bask Bank message

Protect Your Bank Accounts from Fraud: Tips to Stay Secure
At Bask Bank we understand the importance of safeguarding your personal information and financial security. With the rise of phishing scams and schemes, it's more important than ever to be aware of online threats this holiday season. Follow these tips to keep your information secure and learn what to do if you see suspicious activity on your account.

What you can do:

    Monitor your bank account transactions and security alerts in Online Banking. Bask Bank will notify you when account changes are made or requested.
    Avoid using a public Wi-Fi network to log in to websites or mobile apps that requires a username or password. Unsecure networks can put your personal and banking information at risk.
    Keep your personal financial information private. Never share your bank account or credit card details to anyone offering you prizes or gifts or in response to an unsolicited request.
    Never send money or gifts to anyone you haven't met in person. Be aware of anyone online asking you to send giftcards, wire funds, or send money through a mobile payment app.
    Be wary of emails, text messages or phone calls claiming to be a reputable company urging you to act immediately or asking you to verify your personal or financial information. Don't click links in suspicious emails or text messages and remember, Bask Bank will never ask you for your Online Banking password.

[Security Center | Bask Bank](https://www.baskbank.com/security-center#2254641303-1552167183-1=)

## Cybersecurity - Matt Levine

### Good honeypot

The internet [tells me](https://www.cnn.com/2022/08/15/politics/classified-information-what-matters/index.html) that there are about 1.2 million people in the US with top secret security clearance. You could imagine a sort of cool spy-movie world in which "top secret" secrets were really top secret and only shared with a few, carefully vetted, highly trustworthy people. But at 1.2 million people, nah. At 1.2 million people, even if your vetting process is 99.99% reliable, you will still have 120 people who forget their top secret documents on the train, or leave their top secret laptops open at the coffee shop while they go to the bathroom, or have loud top secret phone conversations in public places, or are actual spies for the other side. At 1.2 million people, no matter how good your vetting is, the far left tail of the trustworthiness distribution is going to be [this guy](https://www.justice.gov/opa/pr/air-force-employee-indicted-unlawful-disclosure-classified-national-defense-information):

> A civilian employee of the U.S. Air Force assigned to the U.S. Strategic Command (USSTRATCOM), at Offutt Air Force Base, was arrested Saturday, March 2, for allegedly conspiring to transmit and transmitting classified information relating to the national defense (National Defense Information or NDI) on a foreign online dating platform beginning in or around February 2022 until in or around April 2022.
> 
> According to the indictment, David Franklin Slater, 63, of Nebraska, worked in a classified space at USSTRATCOM and held a Top Secret security clearance from in or around August 2021 until in or around April 2022, after retiring as a Lieutenant Colonel from the U.S. Army. It is alleged that Slater willfully, improperly, and unlawfully transmitted NDI classified as "SECRET," which he had reason to believe could be used to the injury of the United States or to the advantage of a foreign nation, on a foreign online dating platform to a person not authorized to receive such information.

Yes, somewhere out there, there will inevitably be a guy who (1) has a top secret security clearance and (2) will hand out military secrets to impress obviously fake partners on an online dating site. Allegedly Slater got classified briefings about Russia's invasion of Ukraine, and he had a fake online girlfriend "who claimed to be a female living in Ukraine on the foreign dating website." From [the indictment](https://www.justice.gov/opa/media/1340961/dl?inline):

> Co-Conspirator 1 [the fake girlfriend] regularly asked DAVID FRANKLIN SLATER to provide her with sensitive, non-public, closely held, and classified NDI, to which DAVID FRANKLIN SLATER had access as a result of his employment with the United States Air Force. For example, Co-Conspirator 1 stated in 2022: …
> 
> On or about March 11, "Dear, what is shown on the screens in the special room?? It is very interesting." …
> 
> On or about March 15, … "You are my secret informant love! How were your meetings? Successfully?"
> 
> On or about March 18, "Beloved Dave, do NATO and Biden have a secret plan to help us?" ...
> 
> On or about April 12, "Sweet Dave, the supply of weapons is completely classified, which is great!"

Did he ever worry that maybe she only loved him for his top secret information and not for his sparkling personality? Did he care? How could this possibly have worked? Well, it only had to work on one guy.

## extension data theft

[Let's build a Chrome extension that steals as much data as possible | Hacker News](https://news.ycombinator.com/item?id=34889243)
[Let's build a Chrome extension that steals everything](https://mattfrisbie.substack.com/p/spy-chrome-extension)

## myths about security

[What are some myths about security products you would like to see busted?: cybersecurity](https://www.reddit.com/r/cybersecurity/comments/12thmpl/what_are_some_myths_about_security_products_you)

## old hardware

[Discarded, not destroyed: Old routers reveal corporate secrets : cybersecurity](https://old.reddit.com/r/cybersecurity/comments/12sw7q5/discarded_not_destroyed_old_routers_reveal)

## panic

[What is LifeLock and Should You Use It?](https://joywallet.com/article/what-is-lifelock)

[When in doubt: hang up, look up, and call back | Hacker News](https://news.ycombinator.com/item?id=22958477)
[When in Doubt: Hang Up, Look Up, & Call Back - Krebs on Security](https://krebsonsecurity.com/2020/04/when-in-doubt-hang-up-look-up-call-back/)

## permissions

[Google to ban financial lending apps from accessing user photos, contacts | Hacker News](https://news.ycombinator.com/item?id=35494366)
[Google to Ban Financial Lending Apps From Accessing User Photos, Contacts | PCMag](https://www.pcmag.com/news/google-to-ban-financial-lending-apps-from-accessing-user-photos-contacts)

[Why do Java, Silverlight, Adobe Acrobat and other plugins no longer work? | Firefox Help](https://support.mozilla.org/en-US/kb/npapi-plugins)

[How to Lock a Folder Using a Batch File (with Pictures) - wikiHow](https://www.wikihow.com/Lock-a-Folder-Using-a-Batch-File)

## remote attestation

[Remote Attestation is coming back | Hacker News](https://news.ycombinator.com/item?id=32282305)
[Remote attestation is coming back. How much freedom will it take? - Gabriel Sieben](https://gabrielsieben.tech/2022/07/29/remote-assertion-is-coming-back-how-much-freedom-will-it-take/)

## remove personal information

[White Pages Removal – Remove Your Information from Spokeo Search, MyLife, People Finder](https://www.freecodecamp.org/news/white-pages-removal-remove-information-spokeo-peoplefinder-whitepages-opt-out)

## Charles Schwab message

Steps to protect your accounts all year long.

The holiday season can also be a season of increased fraud and scams. That's why we're sharing a few steps you can take to help keep your assets, financial information, and personal identity safe and secure.

1. Set up security alerts.
Why it's important:

Security alerts can help you avoid or detect fraud by providing you with real-time notifications about activity in your account, such as changes to your password or your contact information.
Next steps:

Log in to Schwab.com to manage security alert preferences under your Profile.

2. Keep contact information up to date.
Why it's important:

Keeping your information current means we can reach you quickly when addressing unusual account activity.
Next steps:

Log in to Schwab.com to review and update your Contact Information.

3. Add a trusted contact.
Why it's important:

Establishing a trusted contact provides an additional person we can contact if an issue arises with your account(s).
Next steps:

To learn more about designating a trusted contact, read this article.

4. Discover how to identify, avoid, and report scams.
Why it's important:

With scams on the rise, it's more important than ever to learn about the common tactics fraudsters use so you can mitigate the risk of becoming a victim.
Next steps:

Read our brochure to learn about popular scam types, tips to protect yourself, and how to report if something should occur.

5. Protect yourself online.
Why it's important:

Following preventive steps to stay safe online can help keep your accounts and personal information more secure.
Next steps:

Use this online security checklist to better protect your identity and devices when online.

---

Ways to protect yourself from payment fraud:
- Pay it safe: Since most P2P apps don't allow you to cancel a transaction, treat payments like cash, and only send funds to those you know and trust.
- Take your time: If someone is pushing you to act quickly with a P2P payment, it could be a red flag.
- Use your security settings: Enable settings within the P2P applications, such as multifactor authentication (also known as two-factor authentication),
- Let your financial institution help: Fraud alerts can automatically notify you of activity, and always contact your financial institution immediately if you suspect something is wrong.
- Be aware of phishing: Fraudsters might try to access your account by posing as your financial institution or a P2P company. If someone calls you unexpectedly and claims to be from your financial institution, it is best to hang up and call your financial institution at the number printed on your statement rather than the number that called you.
- Use unique passwords: Use different passwords for P2P apps and other sites, avoid sharing your passwords with others, and consider a password manager tool if you have trouble remembering passwords.

FROM CHARLES SCHWAB
- Stay vigilant. You can help prevent fraud with these simple steps:
    - Hover over links in an email to confirm they are from legitimate sources before clicking on them and do not dial the number in an email or pop-up alert.
    - Ensure your computer systems, online browsers, and mobile devices are updated with the latest versions of software.
    - Establish unique and strong login credentials. At Schwab, you can create a password or passphrase. Be sure to create a password that you use only with Schwab and nowhere else.
    - Change your password periodically to ensure your security if you have not changed your password for a long period.
    - Use two-step verification, which will provide you a unique security code each time you access your accounts. Visit the Security Center tab to update your two-step verification settings.
    - Review your existing passwords and ensure they are updated to strong and unique passwords if they have not been updated or changed for a long period of time.
    - Manage your alert settings through [Schwab.com](http://schwab.com/) or the Schwab mobile app. When possible, enable "Push" notifications for real-time activity alerts.



Here are seven tips to know you’re working with Schwab:

Look out for unsolicited offers.

We’ll never contact you directly using a messaging app (like Facebook Messenger and WhatsApp) to offer unsolicited investment opportunities.

Check before giving remote access to your computer.

Before giving someone remote access, especially if they proactively contact you saying there's an issue or suspected fraud, call the phone number listed below or on Schwab's public site to verify you’re speaking with Schwab.

Avoid clicking suspicious links.

Don’t click on links sent through social media or text unless you’re confident they’re real, especially if they promise lucrative investment opportunities.

Use caution with “special” opportunities.

Be wary of investment opportunities based on alleged “insider” or confidential information, as these could involve illegal or fraudulent activities.

Beware of urgency and pressure tactics.

Be cautious of communications urging immediate action or pressuring you to invest quickly with promises of guaranteed or unusually high returns. Remember: If it sounds too good to be true, it probably is.

Do your research and verify.

Before committing to anything, call us at the number below or through one of our official channels first to verify the legitimacy of the information and the individuals involved.

Stick to our official channels.

Always use our verified, secure communication channels for all transactions and inquiries. These can be found at schwab.com/contactus.

## Preliminary steps to avoid accidentally running a malware infected file


For software, the best places are going to be private trackers, as they tend to have staff members dedicated to checking the validity of torrents uploaded. rutracker is a large public tracker that is well-known for their music and software catalogue. If you're going to download software and you don't want to make the effort to join private trackers, rutracker is one of the best public tracker to use. Warezbb is a great board for software (if you can catch it when it's not down).

If you're going to download software/games, [definitely avoid the piratebay](https://www.reddit.com/r/Piracy/comments/cxbn33/psa_ransomware_all_current_vegas_pro_17_torrents/). They have an immense amount of fake torrents and it's just not worth the risk of wading through their crap heap.

If you're going to download other torrents that aren't software, you can at least take preliminary measures that you're not running a fake file, even if you download from TPB.

The following examples use video files as an example, and while it is wholly possible to include malware in anything, malware in files like video files, music files, aren't a likely scenario. Even then, they would have to target a specific program (ie. a specific video player) to attempt to exploit in order to tailor a video file with malware only meant to be able to run on such a video player. The main idea here is to use up-to-date programs in order to prevent being a victim of most of these exploits.

If you're looking for video, obviously an exe file is not what you're looking for, so that's an obvious candidate for the trash bin. Other attack vectors include intentionally bloated videos that simply contain messages like "download `x` codec to properly view this video". In the download folder there may be a link or executable to install the supposed "codecs", which will obviously be malware.

SFX files may also be used to spread malware, as they are "self extracting executables", but by all intents and purposes treated as executables themselves. Do not run software if you do not trust the source.

Pay close attention to the file icon to make sure that it's recognized as a video file instead of anything else. If you have file extensions hidden, files such as `NotAVirus.mp4.exe` will simply show as `NotAVirus.mp4`, but they'll show the executable icon because windows sees the real file extension. Make sure you [unhide file extensions.](https://support.winzip.com/hc/en-us/articles/115011457948-How-to-configure-Windows-to-show-file-extensions-and-hidden-files)

Be on the lookout for RTL naming schemes that may make a filename of `filename.3pm.exe` be displayed as `filename.exe.mp3`: [Further Reading.](https://resources.infosecinstitute.com/spoof-using-right-to-left-override-rtlo-technique-2/)

Another attack vector includes windows shortcuts, which will provide (as an example) a supposed `videofile.avi` video file but it's actually shortcut to a batch/powershell other type of script, and won't show as such even with file extensions shown. The file icon may also be one similar to that of a video player's, but if you pay close attention to it, you'll notice an arrow in the corner that indicates it's a shortcut. Also note the `file type` column in file explorer showing `Shortcut`: <https://i.imgur.com/e0Cgeje.jpg>. In the screenshot, the tiny filesize is a giveaway, but these attack vectors typically 0-byte pad the file to inflate the filesize, in an attempt to make it look more convincing. [Some reading on this](https://blog.trendmicro.com/trendlabs-security-intelligence/rising-trend-attackers-using-lnk-files-download-malware/) [TrendMicro]. This type of download will never not be malware.

Use proper video players instead of the default windows media player: MPC, MPV, VLC.

Popular video file types will be avi, mp4, mkv. `wmv`, `wma` video/audio containers' specs allow for scripts, which windows media player can try to run.

Not very common, but `.scr` files are "screensaver setter" files that are actually just executables. Avoid these.

## wifi security

[Stop worrying about public WiFi and airport phone chargers - The Washington Post](https://www.washingtonpost.com/technology/2023/04/28/public-wifi-security-risks)

[When using Public WiFi.. is a VPN essential or should you just ensure you're using HTTPS? : AskNetsec](https://old.reddit.com/r/AskNetsec/comments/skvfp0/when_using_public_wifi_is_a_vpn_essential_or)

## anonymity

[Anonymity Guide](https://old.reddit.com/r/hacking/comments/15zcn7f/anonymity_guide/)

## general guides

[Secure the most important network - your home. - SWATeam](https://www.swateam.org.uk/2023/04/secure-the-most-important-network-your-home/)

[Resources Archive Stay Safe Online](https://staysafeonline.org/resources)

[Stop.Think.Connect.](https://stopthinkconnect.org/)

[preliminary measures to avoid running malware](https://www.reddit.com/r/Piracy/wiki/browsing_and_downloading_guide)

## packt video guides

[Login to your Packt account](https://subscription.packtpub.com/owned)

The Absolute Beginners Guide to Cyber Security 2023 - Part 1

Pentesting Fundamentals for Beginners

The Beginners 2023 Cyber Security Awareness Training Course

Cyber Security for Absolute Beginners - 2022 Edition - Part 02

[Login to your Packt account](https://subscription.packtpub.com/owned)

Learn Ethical Hacking From A-Z: Beginner To Expert Course

The Complete Ethical Hacking Bootcamp: Beginner To Advanced

Learn Hacking Windows 10 Using Metasploit from Scratch

### specific guides

[Login to your Packt account](https://subscription.packtpub.com/owned)

Hacking WEP/WPA/WPA2 Wi-Fi Networks Using Kali Linux

Learn Man in the Middle Attacks from Scratch

Nmap for Penetration Testing: From Beginner to Advanced [Updated for 2021]

Python for Penetration Testers

Threat and Vulnerability Assessment for Enterprises

Web Application Hacking with Burp Suite

Risk Management for Cyber Security Managers

## safety is hard

[Social media safety | WORLD](https://wng.org/podcasts/social-media-safety-1720047100)

## bank pin number

[How to create a pin number & tips to remember it | U.S. Bank](https://www.usbank.com/financialiq/manage-your-household/protect-your-assets/8-tips-and-tricks-for-creating-and-remembering-your-PIN.html)

## CUI

[What Exactly is CUI? (and How to Manage It) - Hyperproof](https://hyperproof.io/resource/what-is-cui/)

## PII

[What Is Personally Identifiable Information (PII)? Types and Examples](https://www.investopedia.com/terms/p/personally-identifiable-information-pii.asp)

## antivirus

[Do you need antivirus for your phone? @ AskWoody](https://www.askwoody.com/2024/do-you-need-antivirus-for-your-phone/)



There is a such thing as TOO secure:

- the ouroboros snake strikes when the authentication is BEHIND the authentication wall (e.g., email authentication sent to an email on the same server)

3-2-1 rule:
- 3 copies of your data on 2 different forms of media, 1 which is stored off site

NOTE: CLARIFY "PERMISSIONS" ON THE TS SECURITY PAGE

[Should all locks have keys? Phones, Castles, Encryption, and You. - YouTube](https://www.youtube.com/watch?v=VPBH1eW28mo)
- people who crack digital locks have no sense of distance and simply run lots of numbers
- locks CAN be made unbreakable with lots of math, but not entirely
- governments REALLY want to have back-doors for encryption, though many geeky privacy advocates don't want that to happen, and those governments can't be trusted to always be good
- SIDENOTE: encrypted files are essentially in scrambled gibberish in their resting state, then temporarily become usable when that authentication passes through

Be a pro. Back up your back up. Have at least one physical backup and one backup in the cloud. Have more than one of each. How much would you pay to retrieve all your data, photos, notes, if you lost them? Backups are cheap compared to regrets.

Assume anyone asking for your account information for any reason is guilty of scamming you, unless proven innocent. The way to prove innocence is to call them back, or login to your account using numbers or a website that you provide, not them. Don't release any identifying information while they are contacting you via phone, message or email. You must control the channel.

Follow best practices
- ASafaaWeb security analyzer
- Observatory by Mozilla

Cross-site scripting
- XSS cheat sheet
- DOM based XSS cheat sheet
- Free XSS scanner

Cross-site request forgery
- Explanation and walkthrough
- CSRF cheat sheet

Secure connection (SSL) (OPTIONAL)
- Setup SSL on IIS 7
- Setup SSL on Apache
- SSL Server Test

HTTP Strict Transport Security (OPTIONAL)
- MDN Overview
- OWASP Overview

Enable Content Security Policy (OPTIONAL)
- Content Security Policy
- MDN Guide
- OWASP Overview
    - CSP Tester

Data integrity takes several forms and can be divided into four categories:
1. Entity Integrity: No duplicate rows exist in a table. For example, we can't insert Ron Weasley twice in the database.
2. Domain Integrity: Restricting the type of values that one can insert in order to enforce correct values. For example, a House can only be Gryffindor, Ravenclaw, Slytherin, or Hufflepuff.
3. Referential Integrity: Records that are used by other records cannot be deleted. A teacher cannot be deleted if they are currently teaching a course.
4. User-Defined Integrity: An "other" category that consists of business-related logic and rules to the database.

Make sure to
- Add/change wireless passwords and any router passwords, ESPECIALLY admin ones
- When formatting, clear the MBR (often with fdisk /MBR)
- Zero out all data by clearing with multiple passes (to avoid data theft afterward) - 7 passes?

there has been a large push over the last 5 or so years to move to
zero-trust networks as opposed to relying on perimeter security.
Perimeter security is only as strong as the weakest node on your
network. You should _assume_
that
someone will be able to compromise a node on your internal network, and
thus you must never trust a client simply because it has access to your
network.

See e.g. this White House memo from a couple weeks back
[Office of Management and Budget Releases Federal Strategy to Move the U.S. Government Towards a Zero Trust Architecture | OMB | The White House](https://www.whitehouse.gov/omb/briefing-room/2022/01/26/office-of-management-and-budget-releases-federal-strategy-to-move-the-u-s-government-towards-a-zero-trust-architecture/)

FUD - Fear, Uncertainty and Disinformation
PII - personally identifiable information

Note: I can make a threat model that also ASSUMES getting hacked
- It can, for example, lead to specific info that's useless, or have a full-on cap on data requests (e.g. only get 1,000 emails on ANY request)

## History of the internet

- Confidentiality - prevent unauthorized viewing of information
- Integrity - it's from who you think it is and hasn't been modified since it was sent SHA-1 is decent, but not necessarily great
    - It's useful for non-critical situations
    - The public key can make a digest, but can't decrypt
    - Receiving a signed message
    - Receive message and digest from insecure transport
    - Remove digest and add secret
    - Compute SHA digest for message and secret
    - Compare the computed digest to the received digest
MD5 hash calculator
Base64 encoder and decoder
- To successfully manage cybersecurity, you have to understand the mind of a hacker
    - That doesn't mean you need to hack, but you DO need to understand the criminal mentality that drives a hacker, and how they tend to think.
- It uses the "secure socket layer" (SSL) to send the cryptographic data
    - The private key is the only one that decrypts, while the public key always encrypts
    - There are 2 kinds of public keys:
        1. Made-up general public keys
        2. 3rd-party authorized public keys (e.g., GoDaddy, Comodo, Verisign, etc.)
            - These second public keys are "digital certificates", or "signed private keys"
            - It can be $100-200 or $1000-2000 to get your certificate formally signed.
- Cryptography makes it relatively more work to hack anyone
    - Without cryptography, anyone can go after anyone
        - Governments can surveil and attack anyone at will
        - Criminals can hack anyone at will
    - With cryptography, while anyone CAN get hacked, the governments/hackers will only attack based on a priorities list, which will protect the majority of everyone else.
    - We can't really "trust" the cryptography, because it's simply math.
        - For it to actually matter, someone has to use code WITH that math.
        - Thus, we only really trust the people who make the systems.
        - Often, the math is never broken, but the stuff AROUND it is vulnerable (software, hardware, code, etc.)
    - The more complexity in the system, the more risks inherent to the system!
        - Keeping it simple keeps it safer.

ON CLASSIFIED DOCUMENTS:

SCIF: Sensitive Compartmentalized Information Facility. 

- Typically this is a physical location (room, building, etc) with specific physical security measures to keep classified information safe. Those with access can view, store, print, or otherwise access the products. The Congressional SCIF (I presume) is just for viewing…Not sure where the committees that have access actually do their work, which would probably create classified documents. 
- SCIFs are rated for the classification level of information they contain.  All of these locations have strict access requirements including the appropriate clearance, access lists and badges, no mobile devices, earbuds, smart watches, etc.   
- TS - Top Secret (exceptionally grave damage to National Security)
- S - Secret (grave damage to National Security)
- CUI - Controlled Unclassified Information (replaced For Official Use Only - FOUO) and includes things like personally identifiable info, or other things that we generally want to keep private, but aren't strictly classified. 
- Another way to accidentally attain a higher classification is by adding multiple pieces of unclassified information together. This is one of the things we have to be careful of, because if you're not careful, the final document might be a higher classification **because** of the sum of its parts.
- Classification markings are not only on the cover sheet, but also throughout the document itself, including pages and individual paragraphs. 
- Classified documents generally have to stay inside SCIFs. Documents can **only** come out if properly packaged to protect the information and then are carried by official couriers with special training, clearances, and lockable courier cases. Not quite a briefcase with handcuffs, but close. 

Computer Systems: 

- There are classified computer networks which have no connection (air gaps) to the regular internet or outside world. These are essentially completely securely self-contained and handle information up to a particular classification level; so, there are secret systems as well as top secret systems. TS can handle any level up to TS (including secret).  Secret can only handle up to secret info. These systems include email clients so you can send documents to other users with access and need to know. 
- There are also unclassified computer systems for daily work that have internet connectivity, but are regulated by IT policies and systems that filter what you can get to. E.g., for the longest time, Al Jazeera News wasn't accessible on the unclassified network. 
- Also, all users sign acceptable use policies as a prereq to getting network access, and sites that are forbidden in the AUP are routinely blocked; so if there's a bad link on the page (site, video, etc.), you'll often get an intimidatingly official looking "ACCESS TO THIS SITE IS FORBIDDEN" in that space.  Sometimes it's the whole page. 

Getting a Clearance.

- How one **gets** a security clearance is another saga that includes a veritable colonoscopy of background checks going over years of your past, personal connections, rap sheets, foreign travel, credit score and finances, past addresses, scrutiny of your family and much more including an in person interview, and if required, possibly a polygraph. Good times.
- Clearances are also re-vetted periodically to make sure the person is still considered safe to have a clearance. It used to be that clearance reviews only happened every 5 or 10 years (depending on the clearance level), but they're changing that to "continuous vetting" now where the security apparatus overseeing this will be alerted to things like criminal offenses, bankruptcies, other "derog" (derogatory) information; one can presume that they're closely looking at social media and such as well.

All of this to say that classified information **should** be taken seriously and there are myriad policies, and procedures deliberately put in place to ensure that it is cared for properly. Even though he may have declassified it, Trump probably shouldn't have had that stuff at Mar a Lago (declassified or not, that doesn't mean that it lost any of its importance or potential to cause harm to the country). Nor should the former VP Biden have had classified dox hanging out in file boxes in his (locked) garage. There may be legitimate reasons for former presidents to have that type of stuff, but it never negates the handling requirements.

## Windows 11 Privacy Apps

Tiny11Builder
Simplewall
ShutUp10++
Bulk Crap Uninstaller
BleachBit
Mullvad VPN
Firefox - in strict mode
uBlock Origin
Decentraleyes
Privacy Badger

## How To Be Safe

1) Atestation - periodic check of every account,
2) Rotate every key, every password.
3) Verify every open port as needed
4) verify the jobs for data transferrals
5) verify every vpn
6) verify every computer/ network device
7) trust nothing
8) assuming your already compromised don't bother with a baseline your already owned start the clean up.
9) employ red team attacks
10) patch
11) correlation optics
12) externalise the siem
13) add honey pots
14) test your DR from cold offline restore
15) do background checks on your admin staff
16) add nano segmentation

## 3D policy

3D system
- dead
- disappear
- disabled
- there is a trigger that goes off if someone isn't routinely (e.g., once a week) validating something
- this is a security policy for yourself

## Hacking

A lot of the domain of hacking is tied to violations of privacy

- in some capacity, there's a belief that only "authorized" people can go into something (which usually is the case, barring [big companies]FAANG) interfering)
- hacking is the intervention of someone finding a way to get around those constraints
    - this is ALWAYS possible, since the computer is nothing more than logic/math machine: match the logic/math, the computer thinks you're legit when you're not
    - the only way to NOT permit this is to have a human being reviewing everything, but [AI] is the dumb fashion of the day to fix the problem

MAKE SURE TO TALK ABOUT THE "DARK WEB"

To programmers, "hacker" connotes mastery in the most literal sense:
someone who can make a computer do what he wants.

The noun "hack" also has two senses. It can be either a compliment or an
insult. It's called a hack when you do something in an ugly way. But
when you do something so clever that you somehow beat the system, that's
also called a hack.

[Rockstar is selling cracked game copies on Steam | Hacker News](https://news.ycombinator.com/item?id=37394665)
[Silent on X: "OH FOR CHRIST'S SAKE https://t.co/vx8yDcz1B3" / X](https://twitter.com/__silent_/status/1698345924840296801)
- sometimes the hackers actually PRESERVE the integrity of the original games (see comments)
- cracked media are often the only way to preserve things that DRM might permanently lock down

[YouTuber sentenced to 6 months in prison for obstructing probe into plane crash | Hacker News](https://news.ycombinator.com/item?id=38523704)
[Central District of California | Santa Barbara County Man Sentenced to 6 Months in Prison for Obstructing Federal Probe into Plane Crash He Posted on YouTube | United States Department of Justice](https://www.justice.gov/usao-cdca/pr/santa-barbara-county-man-sentenced-6-months-prison-obstructing-federal-probe-plane)
- comments indicate:: Howard Baker (R-TN)
    "It is almost always the cover-up rather than the event that causes trouble."

### From old blog post

FROM MY OLD "TO MY FRIENDS" PAGE:

Focus your lives on things beyond this life. That aforementioned De1ty will come back and rule with strength and love. Focus on building that society, since the time is utterly short.

Change your language, both writing and speaking. Read Orwell's Nineteen Eighty Four to understand the scope of control that people have, especially with computers. It also helps to be aware of what computers can and can't do. My writing here is an example of something that will likely stay below the radar for now, but please…get creative!

Share organically. In-person engagement is how the early People of the De{ty interacted and grew. Ancient Rome feel before the People did, mostly because the ideas of the Book were more powerful than the meat part of us.

Get ready to travel. I don't mean that you must give everything up now, but be prepared to travel light, and fast. Trust the Great Pneuma who guides those that are loved by him.

Always pr@y. Give everything you can't presently control to that Being. He cares tremendously, and will protect you to accomplish the purpose you've been chosen for.

Clear history whenever possible. This includes web history, computer records, social profiles. Minimize what you can. Take things offline.

Decentralize whenever possible. Stay away from meeting in large groups. Use self-hosted websites and email over mainstream stuff. Distrust anything with computers that is "free" unless it's open-source. Stay at home for your interactions, even if you invite a few dozen people. Get creative on how. Learn from our Divine family from ch1n@.

## new sites - medium blogs

[Argonyte](https://medium.com/@argonyte.cybersec)

[Hunchly](https://medium.com/@hunchly)

[Irfan Shakeel](https://irfaanshakeel.medium.com/)

[Osint - Human Rights Center](https://medium.com/humanrightscenter/tagged/osint)

[Petro Cherkasets](https://medium.com/@Peter_UXer)

[Steve Micallef](https://medium.com/@micallst)

[The OSINT Toolkit](https://medium.com/osint/the-osint-toolkit-3b9233d1cdf9)

[What The OSINT!](https://medium.com/what-the-osint)

## VPN

A PROXY SERVER REROUTES IP ADDRESSES FOR WEB TRAFFIC
A VPN IS A PROXY SERVER, BUT ALSO REROUTES IP ADDRESSES FOR ALL TRAFFIC, AS WELL AS ENCRYPTING ALL THE TRAFFIC

## ai protection

[Private Cloud Compute: A new frontier for AI privacy in the cloud | Hacker News](https://news.ycombinator.com/item?id=40639606)
[Blog - Private Cloud Compute: A new frontier for AI privacy in the cloud - Apple Security Research](https://security.apple.com/blog/private-cloud-compute/)

## antivirus can be a virus in itself

[my pc doesnt even have a webcam : assholedesign](https://old.reddit.com/r/assholedesign/comments/sk0emr/my_pc_doesnt_even_have_a_webcam)

## antivirus software - kaspersky

[Antivirus Kaspersky Cloud](https://usa.kaspersky.com/free-cloud-antivirus)
Antivirus
[Kaspersky Lab Resource Center](https://usa.kaspersky.com/resource-center)
[Kaspersky TDSSKiller](https://media.kaspersky.com/utilities/VirusUtilities/EN/tdsskiller.exe)
[Kaspersky Threat Intelligence Portal - Analysis](https://opentip.kaspersky.com)
[Kaspersky KVRT](https://devbuilds.s.kaspersky-labs.com/devbuilds/KVRT/latest/full/KVRT.exe)
[Kaspersky Anti-Virus Can Actually Help Spies Steal Data, Warn Researchers](https://www.forbes.com/sites/thomasbrewster/2017/07/27/kaspersky-av-hack-with-satellite-malware?sh=4ba347692e0f)
[Kaspersky](https://www.kaspersky.co.uk/vpn-secure-connection)
Free VPN/200 MB per day/No Account Required
[Kaspersky is declared a US national security threat and is banned by the FCC | Hacker News](https://news.ycombinator.com/item?id=30842511)
[Kaspersky Is Declared A US National Security Threat And Is Banned By The FCC | HotHardware](https://hothardware.com/news/kaspersky-declared-us-national-security-threat-banned-fcc)
[Kaspersky believes it found new CIA malware | Hacker News](https://news.ycombinator.com/item?id=26970395)
[Security firm Kaspersky believes it found new CIA malware](https://therecord.media/security-firm-kaspersky-believes-it-found-new-cia-malware)
[MAP | Kaspersky Cyberthreat real-time map](https://cybermap.kaspersky.com/)

## antivirus software

[AV-Comparatives](https://www.av-comparatives.org/)
independent tests of antivirus softwares

## antivirus software - virustotal

[VirusTotal Data Leak Exposes Some Registered Customers' Details](https://thehackernews.com/2023/07/virustotal-data-leak-exposes-some.html)

[VirusTotal apologizes for data leak affecting 5,600 customers](https://www.bleepingcomputer.com/news/security/virustotal-apologizes-for-data-leak-affecting-5-600-customers/)

[Not-oss/virustotal-vm-blacklist: yep full list of virustotal machines](https://github.com/Not-oss/virustotal-vm-blacklist)

[How it works](https://docs.virustotal.com/docs/how-it-works)

[VTchromizer](https://chrome.google.com/webstore/detail/vtchromizer/efbjojhplkelaegfbieplglfidafgoka)

[VirusTotal](https://www.virustotal.com/fr/)
free online scanner for virus, malware and URL, to avoid downloading crap on your machine

## antivirus software - Windows Defender

[Windows Defender is so good, maybe even too good, as it detects ransomware inside of. vmdk files. : cybersecurity](https://old.reddit.com/r/cybersecurity/comments/yexkzm/windows_defender_is_so_good_maybe_even_too_good)

[Windows Defender is enough, if you harden it | Hacker News](https://news.ycombinator.com/item?id=30580444)
[Windows Defender is enough, if you harden it](https://0ut3r.space/2022/03/06/windows-defender/)

## avoiding tech

[Why do some "generals" and "intelligence heads" claim to not use mobile phones? Cant they just use a VPN router and connect their phone through that? : hacking](https://old.reddit.com/r/hacking/comments/16u8a7p/why_do_some_generals_and_intelligence_heads_claim/)

## code signing

[Morten Johan Sørvig](http://blog.qt.io/blog/2014/10/29/an-update-on-os-x-code-signing/)
(2014) An update on OS X Code Signing

[ouchangjian](http://www.ouchangjian.com/question/588b48cce4a1ca4b30edaff5)
difference between codesign and productsign ?

[Stack Overflow](https://stackoverflow.com/a/21564967/2309958)
what to sign, with which certificate ?

## CompTIA Cysec

What group has complete privilege control over a system?

- Administrator

A user logs into a computer and uses a camera that records a 3-D image with its infrared sensor to mitigate attempts to use a photo to spoof the authentication mechanism. What is this called?

- Facial recognition

A user wants to connect to multiple systems after a single login at only one of the devices. What is this called?

- Fingerprint

A company has given its employees a Windows 10 laptop to use for remote work. Employees who already have access to Office 365 applications can get to work right away. How would employees initially log on to their laptops to begin working on them?

- Use their Microsoft account.

An administrator applies Share and New Technology File System (NTFS) permissions to a folder on a Windows server. The group "Everyone" has Read permissions to the share, and the "Users" group has modify permissions through NTFS permissions. Which of the following is a true statement? (Select all that apply.)

- The "Users" group can modify files in the share.
- The "Users" group can see everything in the share folder.

Employees at a secure facility must log on to office workstations with two-factor authentication (2FA). All employees access the building with a smart card. What 2FA methods are employees most likely using to access their workstations? (Select all that apply.)

- Username and Password
- PIN

What type of local account does a user's Windows computer utilize for legacy applications?

- Power user account

What type of local account on a Windows computer has full rights and privileges to everything on the system?

- Administrator account

An administrator reviews an audit log and notices strange logins when the business is closed. Which policy does the administrator use to deter this activity?

- Restrict login times

Which root-level file allows for the automatic execution of commands in a legacy version of Windows?

- autorun.inf

What might a security engineer suggest as a solution to deter lunchtime attacks?

- Policies

A technician is evaluating what sources to allow on the organization's network. What type of source cannot be verified?

- Untrusted source

A technician prepares an organizational presentation on browser privacy settings and additional features that supplement the cookie policy and tracking protection. What uses more sophisticated techniques to prevent displaying anything that does not seem to be part of the site's main content or functionality?

- Ad blocker

An engineer develops a training packet for newly-hired employees regarding computer passwords. Regarding passwords, what is the benefit of using a password manager?

- It suggests strong credentials at each new sign-up.

A cyber consultant views the various methods of supplementing browser privacy settings. What prevents a website from creating dialogs or additional windows?

- Pop-up blocker

A consultant drafts a point paper for the organization's cyber department discussing the various methods of securing data. What is a tenet of hashing?

- It takes any amount of data and produces a fixed-length value.

A technician reviews possible methods of securing data through encryption and other processes. What function can take any amount of data as input and produce a fixed-length value as output?

- Hashing

A cyber consultant reviews the risk matrix associated with sources. What is the tenet of a trusted source?

- It involves the use of a source that contains a verified digital signature.

What is also known as a potentially unwanted application (PUA) and should be removed from the computer?

- Untrusted source

A user is on a website using an HTTPS URL; the browser displays the information about the certificate in the address bar. What does this certificate validate?

- Secure connection

What technique is often used to exhibit fake antivirus and security warnings or other malicious advertising?

- Pop-ups

A security manager reviews user roles to grant the minimum privileges necessary. What should the manager implement?

- Least privilege

Who is responsible for providing a safe and healthy work environment?

- Employer

What phase of the procurement life cycle includes the documentation of an asset, such as warranty and licensing details?

- A. Deployment
- B. Procurement (selected)
- C. Change management
- D. Maintenance

NOTE: what is p0f?

NOTE: what is a "common ground point" as opposed to a ground point?

NOTE: clarify SOP, RMA, MSDS, life cycle policy, etc.

What part of the ticketing system does a support agent use to group related tickets?

- Categories

When onboarding or offboarding an employee, a company generates a list of steps that must be followed to ensure that all processing for that employee is complete. Which of the following are the correct lists that are generated? (Select all that apply.)

- New-user setup checklist
- End-user termination checklist

NOTE: clarify escalation vs severity

NOTE: clarify what an "incident report" is

NOTE: what is "spine and leaf"?

NOTE: UX: "splash screen"

NOTE: procurement, deployment, change mgmt, maint, ??? (life cycle stages)

A security analyst notices a critical incident that has a widespread effect on customers that can eventually involve a potential data breach. The analyst creates a ticket with the vendor and sets the importance in order to trigger a faster response time. What describes what attribute of the ticket the analyst set?

- Severity levels

NOTE: [acceptable use policy]

Organizing support teams into tiers, such as Tier 1, Tier 2, Tier 3, is an example of?

- Escalation levels

During the course of an incident, the support technician at each tier will enter information related to the given problem. To assist in faster resolution for common incidents, a ticket can be linked to another part of the database that contains information relevant to the issue at hand. What is this information called?

- Knowledge Base

Electrical fires: they need something like carbon dioxide because foam and water are conductive and dry powder may not get onto it that well
NOTE: what is MPLS?

Which of the following is used as a safe place to organize sensitive components to prevent against electrical shock and damage?

- Electrostatic discharge (ESD) mat

## cybersecurity industry

[What are the fault lines in Cyber Security in 2022? : AskNetsec](https://old.reddit.com/r/AskNetsec/comments/urwbxy/what_are_the_fault_lines_in_cyber_security_in_2022)

## cyber vs infosec

[Why is "cyber" popular over "infosec"? What's the difference? : cybersecurity](https://old.reddit.com/r/cybersecurity/comments/1169y6u/why_is_cyber_popular_over_infosec_whats_the)

## dangerous VPNs

[Swing VPN app is a DDoS botnet | Hacker News](https://news.ycombinator.com/item?id=36382700)
[Swing VPN app is a DDOS botnet | Greek geek](https://lecromee.github.io/posts/swing_vpn_ddosing_sites/)

## dumb security ideas

[The six dumbest ideas in computer security (2005) | Hacker News](https://news.ycombinator.com/item?id=40959121)
[The Six Dumbest Ideas in Computer Security](https://www.ranum.com/security/computer_security/editorials/dumb/)

## excessive security

[I've locked myself out of my digital life | Hacker News](https://news.ycombinator.com/item?id=31652650)
[I've locked myself out of my digital life - Terence Eden's Blog](https://shkspr.mobi/blog/2022/06/ive-locked-myself-out-of-my-digital-life/)

## firewalls

[My mouse driver is asking for a firewall exemption (2019) | Hacker News](https://news.ycombinator.com/item?id=28274305)
[foone🏳️ ⚧️ on X: "Ahh yes, my mouse driver is asking for a firewall exemption so it can accept incoming connections. This is a totally normal thing to happen https://t.co/D3eKsQSxws" / X](https://twitter.com/Foone/status/1146135405793669121)

## hardening

[I can see your local web servers | Hacker News](https://news.ycombinator.com/item?id=20028108)
[I can see your local web servers](https://http.jameshfisher.com/2019/05/26/i-can-see-your-local-web-servers/)

[Aurore Malherbes](https://www.theodo.fr/blog/2017/05/prevent-command-with-a-specific-option-to-be-run-on-your-server/)
(2017) Prevent command with a specific option to be run on your server

[How to harden your login page against cloning](https://old.reddit.com/r/cybersecurity/comments/158tyy7/how_to_harden_your_login_page_against_cloning/)

[RFC 9225: Software Defects Considered Harmful | Hacker News](https://news.ycombinator.com/item?id=30880769)
[RFC 9225: Software Defects Considered Harmful](https://www.rfc-editor.org/rfc/rfc9225.html)

## hidden directories

[research/hidden_directories_leaks at master · bl4de/research · GitHub](https://github.com/bl4de/research/tree/master/hidden_directories_leaks)
as a source of sensitive information about web application.

## honeypots

[What You Get After Running an SSH Honeypot for 30 Days | Hacker News](https://news.ycombinator.com/item?id=40694768)
[What You Get After Running an SSH Honeypot for 30 Days](https://blog.sofiane.cc/ssh_honeypot/)

## ideology affects results

[Full article: Ideology in Costume: A Growing Threat to Intelligence Studies](https://www.tandfonline.com/doi/full/10.1080/08850607.2023.2254490)

## industrial control system security

[Hackers can infect network-connected wrenches to install ransomware | Ars Technica](https://arstechnica.com/security/2024/01/network-connected-wrenches-used-in-factories-can-be-hacked-for-sabotage-or-ransomware/)

## IPTABLES

[netfilter/iptables project homepage - The netfilter.org project](https://www.netfilter.org)
[netfilter/iptables project homepage - The netfilter.org "nftables" project](https://www.netfilter.org/projects/nftables)

## linux security

[How important do you consider learning Linux to be for cybersecurity? : cybersecurity](https://old.reddit.com/r/cybersecurity/comments/yqv8o3/how_important_do_you_consider_learning_linux_to)

[Bryan Kennedy](https://plusbryan.com/my-first-5-minutes-on-a-server-or-essential-security-for-linux-servers)
(2013) My First 5 Minutes On A Server; Or, Essential Security for Linux Servers

## making backups

[Don't Wanna Pay Ransom Gangs? Test Your Backups | Hacker News](https://news.ycombinator.com/item?id=27887329)
[Don't Wanna Pay Ransom Gangs? Test Your Backups. - Krebs on Security](https://krebsonsecurity.com/2021/07/dont-wanna-pay-ransom-gangs-test-your-backups/)

## military mindset

[Biden orders cybersecurity increases at U.S. ports | WORLD](https://wng.org/sift/biden-orders-cybersecurity-increases-at-u-s-ports-1708560261)

[How Home Assistant is being used to protect from missile and drone attacks | Hacker News](https://news.ycombinator.com/item?id=40479729)
[War Safety - Home Assistant Config by Denys Dovhan](https://denysdovhan.com/home-assistant-config/config/war/)

## network tunneling

[Tunneling Wikipedia through WhatsApp to (maybe?) get around WiFi restrictions | Hacker News](https://news.ycombinator.com/item?id=31463249)
[Wikipedia Over WhatsApp · Caffeinspiration](https://alexanderell.is/posts/wikipedia-over-whatsapp/)
[Show HN: Wa-tunnel - HTTP Tunneling through Whatsapp | Hacker News](https://news.ycombinator.com/item?id=33568994)
[aleixrodriala/wa-tunnel: Tunneling Internet traffic over Whatsapp](https://github.com/aleixrodriala/wa-tunnel)

## obscuring things in plain sight

[Invisible 'Keyhole' Security Developed With Printable Electronics | IE](https://interestingengineering.com/innovation/invisible-keyhole-security-developed-with-printable-electronics)

## packet and traffic analysis

[I want to learn more about packet and traffic analysis : HowToHack](https://old.reddit.com/r/HowToHack/comments/y17hd2/i_want_to_learn_more_about_packet_and_traffic)

[I built a system that takes pictures of all the airplanes that fly over my house | Hacker News](https://news.ycombinator.com/item?id=30039597)
[Luke Berndt on X: "Soo... I built a little system that takes pictures of all the airplanes that fly over my house: https://t.co/mLitxMgFBj ✈️📷🤖" / X](https://twitter.com/LukeBerndt/status/1484916000139194375)
[SkyBot](https://web.archive.org/web/20230506000416/https://skybot.cam/)

## privilege escalation

[Ben Wilson](https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/)
(2011) Basic Linux Privilege Escalation

[The Zoom installer let a researcher hack his way to root access on macOS | Hacker News](https://news.ycombinator.com/item?id=32447339)
[The Zoom installer let a researcher hack his way to root access on macOS - The Verge](https://www.theverge.com/2022/8/12/23303411/zoom-defcon-root-access-privilege-escalation-hack-patrick-wardle)

## proxy - reverse proxy

[Duncan Crombie](http://www.the-art-of-web.com/system/apache-reverse-proxy/)
New Apache instance with Reverse Proxy

## proxy services

[Why You Shouldn't Use a Free Proxy](https://www.vpnmentor.com/blog/why-you-shouldnt-use-free-proxies/)
VpnMentor

[Proxy Services Are Not Safe. Try These Alternatives](https://www.wired.com/2015/07/proxy-services-totally-unsecure-alternatives/)
WIRED

[HydraX.net 'Google Drive Streaming Proxy' Traffic Being Sent to ACE Anti-Piracy Coalition](https://torrentfreak.com/hydrax-net-google-drive-streaming-proxy-traffic-being-sent-to-ace-anti-piracy-coalition-200509/)
TorrentFreak

[YSK that translate.google.com can serve as a web proxy. Simply paste your URL into the translate field and then click on the result and view the page in the original language. This way you can navigate any web-page via google.com. Google is almost never blocked so this trick works on most occasions. : YouShouldKnow](https://old.reddit.com/r/YouShouldKnow/comments/fawkjy/ysk_that_translategooglecom_can_serve_as_a_web/)

[Ask HN: Someone is proxy-mirroring my website, can I do anything? | Hacker News](https://news.ycombinator.com/item?id=33952114)

## secure consoles

[Security Issue: Cloud Site Manager presented me your consoles, not mine | Hacker News](https://news.ycombinator.com/item?id=38643348)
[Security Issue: Cloud Site Manager presented me your consoles, not mine. | Ubiquiti Community](https://community.ui.com/questions/Security-Issue-Cloud-Site-Manager-presented-me-your-consoles-not-mine/376ec514-572d-476d-b089-030c4313888c)

## security audits

[MME | Security Audits & Training](https://www.mmebvba.com/)

## security bloggers

[LORÁND BODÓ](https://lorandbodo.com/)

[BushidoToken cybersecurity](https://blog.bushidotoken.net/)

[Aloria](https://securityreactions.tumblr.com/)
Infosec Reactions

[CloudPassage Blog](https://blog.cloudpassage.com/)
insights for a unsecure world / news & tips on protecting critical assets

[ASERT Threat Intelligence Team | NETSCOUT](https://www.netscout.com/asert)

[Blog - Benjamin Strick](https://benjaminstrick.com/blog/)

[Blog – ClearSky Cyber Security](https://www.clearskysec.com/blog/)

[CrowdStrike Blog](https://www.crowdstrike.com/blog)

[CyberCrime & Doing Time](https://garwarner.blogspot.com/)

[Threat Intelligence Blog | Flashpoint](https://flashpoint.io/blog/)

[Forcepoint Security Insights | Forcepoint](https://www.forcepoint.com/blog)

[Fox-IT International blog – News and opinions from Fox-IT](https://blog.fox-it.com/)

[Hacking Blogs - Every Hacker Should Know About](https://hackingblogs.com/)

[holisticinfosec.io/](https://holisticinfosec.io/)

[Tracy Z. Maleeff aka InfoSecSherpa – Medium](https://infosecsherpa.medium.com/)

[Joel Esler](https://blog.joelesler.net/)

[Resources - Videos, online product documentation, book](https://www.langner.com/resources/)

[LookingGlass is now ZeroFox](https://www.zerofox.com/looking-glass-cyber/)

[Threat Intelligence Blog | Recorded Future](https://www.recordedfuture.com/blog)

[Secureworks Blog | Secureworks](https://www.secureworks.com/blog)

[Security Affairs - Read, think, share … Security is everyone's responsibility](https://securityaffairs.com/)

[SurfWatch Labs, Inc.](https://blog.surfwatchlabs.com/)

[Symantec Enterprise Blogs](https://symantec-enterprise-blogs.security.com/)

[The Technical Blogs and Reports Source | ThreatConnect](https://threatconnect.com/blog/ingest-technical-blogs-reports/)

[Blog | VIPRE for Business](https://www.vipre.com/resources/blog)

[Exploring Information Security](https://www.exploresec.com/)

[Award-winning news, views, and insight from the ESET security community](https://www.welivesecurity.com/en/)
[welivesecurity.com/feed](https://www.welivesecurity.com/en/rss/feed/)

[We will always be OSINTCurio.us – We helped the OSINT community stay curious](https://www.osintcurio.us/)
[Webcast 20190106 – #1 – We will always be OSINTCurio.us](https://www.osintcurio.us/webcast-20190106-1/)
[OSINT Curious Webcasts - YouTube](https://www.youtube.com/playlist?list=PL423I_gHbWUXah3dmt_q_XNp0NlGAKjis)
is the investigative curiosity that helps people be successful in OSINT.

[decoded.legal's blog](https://decoded.legal/blog/)

[Didier Stevens | (blog 'DidierStevens)](https://blog.didierstevens.com/)

[FuzzySecurity | Home](https://fuzzysecurity.com/index.html)

[Penetration Testing Lab – Offensive Techniques & Methodologies](https://pentestlab.blog/)

[Shandyman InfoSec – Cyber Security Research, Blogs, Memes and Stuff I Like](https://shandyman.online/blog/)

[Blockint – Research | Consulting | Training](https://www.blockint.nl/)

[IT Cyber Security - ZDL - IT Security Services](https://www.zdlgroup.com/)

[blog.0xrishabh.dev/](https://blog.0xrishabh.dev/)

[Alkimiya](https://www.aniccaresearch.tech/)

[cmichel](https://cmichel.io/)

[Kyrian Alex's Newsletter | Kyrian💧 | Substack](https://kyrianalex.substack.com/)

[GainSec - Where OSINT, Hacking, Penetration Testing, Privacy, Piracy, Information Security, Cyber Security and Law are a lifestyle.](https://gainsec.com/)
Security News

[InfoSec Write-ups](https://infosecwriteups.com/)
Security News

[Securelist | Kaspersky’s threat research and reports](https://securelist.com/)
Security News

[ASEC BLOG - AhnLab](https://asec.ahnlab.com/en/)
Security News

[Home :: GFI](https://www.gfi.com/)
Security News

[Cybersecurity News, Insights and Analysis | SecurityWeek](https://www.securityweek.com/)
Security News

[Gemini Advisory Blog](https://geminiadvisory.io/blog/)
Security News

[KitPloit - PenTest & Hacking Tools](https://www.kitploit.com/)
[Search results for %s Hacking Tools](https://www.kitploit.com/search/max-results=7?q=%25s)
Security News

[HITBSecNews | Keeping Knowledge Free for Over a Decade](https://news.hitb.org/)

[Gynvael "GynDream" Coldwind](https://gynvael.coldwind.pl/)
is a IT security engineer at Google.

[Schneier on Security](https://www.schneier.com/)
is an internationally renowned security technologist, called a "security guru".

[Chrissy Morgan – @5w0rdfish](https://chrissymorgan.co.uk/)
advocate of practical learning, Chrissy also takes part in bug bounty programs.

[ZephrSec - ZSEC Blog - Andy Gill's Adventures](https://blog.zsec.uk/)
is a hacker at heart who works as a senior penetration tester.

[Cybersecurity expert Graham Cluley - keynote speaker • Cybersecurity expert & keynote speaker](https://grahamcluley.com/)
public speaker and independent computer security analyst.

[Kacper Szurek - Blog](https://blog.szurek.tv/)
detection engineer at ESET.

[Robert Penz Blog](https://robert.penz.name/)
IT security expert.

[CloudPassage Blog](https://blog.cloudpassage.com/)
insights for a unsecure world / news & tips on protecting critical assets

[/r/netsec](https://www.reddit.com/r/netsec/)
network security on reddit

[IT Security Blog](http://blog.feedspot.com/information_security_blogs)
Top 100 Information Security Blogs for Data Security Professionals

[Daniel Miessler](https://danielmiessler.com/blog/)
a very interesting blog about InfoSec, technology and humans

[SecurityHQ on Slack](https://securityhq.herokuapp.com/)
Security professionals and newbies

[LandzDown Forum - Index](https://www.landzdown.com/index.php?PHPSESSID=e4074bf4c3ff32a01115068f88bf3c86;wwwRedirect)

[Security Newsletter](https://securitynewsletter.co/)
security news as a weekly digest (email notifications).

[Packet Storm](https://packetstormsecurity.com/)
information security services, news, files, tools, exploits, advisories and whitepapers.

[publiclyDisclosed (@disclosedh1) / X](https://x.com/disclosedh1)
public disclosure watcher who keeps you up to date about the recently disclosed bugs.

[Sick Codes - Security Research, Hardware & Software Hacking, Consulting, Linux, IoT, Cloud, Embedded, Arch, Tweaks & Tips!](https://sick.codes)

[Firestick, Kodi, IPTV, VPN, Android TV Tutorials - TROYPOINT](https://troypoint.com/)

[Ghost in the Wires : hacking](https://old.reddit.com/r/hacking/comments/por6ph/ghost_in_the_wires)

[David Bombal](https://www.youtube.com/channel/UCP7WmQ_U4GB3K51Od9QvM0w/videos)

[Kody Kinzie](https://skickar.github.io/)

## security bloggers - linux

[Linux Audit](https://linux-audit.com/)
the Linux security blog about auditing, hardening and compliance by Michael Boelen.

[The Grymoire](http://www.grymoire.com/)
collection of useful incantations for wizards, be you computer wizards, magicians, or whatever.

## security community

[Do any of you regret going into cybersecurity? If so, why?: cybersecurity](https://www.reddit.com/r/cybersecurity/comments/12fg5cr/do_any_of_you_regret_going_into_cybersecurity_if)

[Cybersecurity: A rant: cybersecurity](https://www.reddit.com/r/cybersecurity/comments/12504t0/cybersecurity_a_rant)

[SANS Internet Storm Center](https://dshield.org/)
[Useful InfoSec Links - SANS Internet Storm Center](https://isc.sans.edu/links.html)
[DShield API](https://isc.sans.edu/api)

[Forums | SOLDIERX.COM](https://www.soldierx.com/bbs)

[L0phtCrack](https://l0phtcrack.gitlab.io)
[L0phtCrack Is Now Open Source | Hacker News](https://news.ycombinator.com/item?id=28900615)
[The early 90s tech scene that created L0pht, the legendary hackerspace | Hacker News](https://news.ycombinator.com/item?id=35190971)
[Phreaks and l33ts: Inside the early '90s tech scene that created L0pht, the legendary hackerspace  | CyberScoop](https://cyberscoop.com/boston-l0pht-hackers-tech-scene/)
[CyberScoop | Breaking Cybersecurity News, Public Sector Threats](https://cyberscoop.com/)

## security conferences

[DEF CON Media Server](https://media.defcon.org/)
great stuff from DEFCON.

[Black Hat](https://www.blackhat.com/)
[Black Hat | Archives](https://www.blackhat.com/html/archives.html)
[BlackHat](https://www.youtube.com/user/BlackHatOfficialYT)

[DEF CON 32 Was Canceled. We Un-Canceled it | Hacker News](https://news.ycombinator.com/item?id=39256930)
[DEF CON 32 Was Canceled. We Un-Canceled it. - DEF CON Forums](https://forum.defcon.org/node/248360)

[InfoCon Hacking and Security Conference Archives](https://infocon.org/)
[InfoCon Hacking Conference Archive](https://infocon.org/cons)

[DEFCON](https://www.youtube.com/user/DEFCONConference)
[DefCon 22: Blinding The Surveillance State](https://www.youtube.com/watch?v=xCH_q-xn760)
[Snoop unto them as they snoop unto you | Hacker News](https://news.ycombinator.com/item?id=37440104)
[Defcon 31 snoop unto them, as they snoop unto us | blog.dataparty](https://blog.dataparty.xyz/blog/snoop-unto-them/)

[Defcon stiffs badge HW vendor, drags FW author offstage during talk | Hacker News](https://news.ycombinator.com/item?id=41207221)
[Mogomra (e/acc) on X: "Haha, wtf, Defcon apparently stiffed the hardware company who designed the cool badges for this year, and physically booted the guy who wrote the software because he mentioned it in an easter egg https://t.co/T76Kvkbulq" / X](https://x.com/mightymogomra/status/1822119942281650278)

[DEF CON's response to the badge controversy | Hacker News](https://news.ycombinator.com/item?id=41211519)
[DEF CON's response to the badge controversy : Defcon](https://old.reddit.com/r/Defcon/comments/1ep00ln/def_cons_response_to_the_badge_controversy/)

[Room inspections at Resorts World confuse, annoy DEF CON attendees | Hacker News](https://news.ycombinator.com/item?id=41206168)
[Room inspections at Resorts World confuse, annoy hacker convention attendees | Tourism | Business](https://www.reviewjournal.com/business/tourism/invasion-of-privacy-hotel-room-inspections-confuse-hacker-convention-attendees-3121350/)

[EFF’s concerns about the UN Cybercrime Convention | Hacker News](https://news.ycombinator.com/item?id=41207987)
[EFF’s Concerns About the UN Draft Cybercrime Convention | Electronic Frontier Foundation](https://www.eff.org/deeplinks/2024/07/effs-concerns-about-un-draft-cybercrime-convention)

## security industry

[Making it clear when we're on a call with you to protect you from fraud | Hacker News](https://news.ycombinator.com/item?id=38420531)
[Making it clear when we're on a call with you to protect you from fraud](https://monzo.com/blog/2023/09/06/making-it-clear-when-were-on-a-call-with-you/)

[Dealing with impostor syndrome? : AskNetsec](https://old.reddit.com/r/AskNetsec/comments/t6mnja/dealing_with_impostor_syndrome)

## security

[DEV](https://dev.to/ben/what-are-some-fundamentals-of-security-every-developer-should-understand-3ki3)
What are some fundamentals of security every developer should understand?

[Reddit - Dive into anything](https://www.reddit.com/r/netsec/wiki/start/)

## security news

[CSO Online](https://www.csoonline.com/)

[Help Net Security](https://www.helpnetsecurity.com/)

[Infosecurity Magazine](https://www.infosecurity-magazine.com/)

[Linux Security](https://www.linuxsecurity.com/)
Linux News

[DarkNetLive](https://darknetlive.com/)
CyberCrime News
[Darknet Live News](http://darkzzx4avcsuofgfez5zq75cqc4mprjvfqywo45dfcaxrwqg6qrlfid.onion/)
[DarkNetLive Dark Web Markets (Tor)](http://darkzzx4avcsuofgfez5zq75cqc4mprjvfqywo45dfcaxrwqg6qrlfid.onion/markets)
[http://darkzzx4avcsuofgfez5zq75cqc4mprjvfqywo45dfcaxrwqg6qrlfid.onion/onions/](http://darkzzx4avcsuofgfez5zq75cqc4mprjvfqywo45dfcaxrwqg6qrlfid.onion/onions)

[ShadowBanker](https://www.shadowbanker.io/)
CyberCrime News

[IT Security News and Security Product Reviews](https://www.scmagazine.com/)

[SecuriTeam](https://www.securiteam.com/)

[Security Intelligence](https://securityintelligence.com/)

[Latest Hacking News](https://latesthackingnews.com/)
provides the latest hacking news, exploits and vulnerabilities for ethical hackers.

[/r/security](https://www.reddit.com/r/security/)
security news on reddit

[/r/opsec](https://www.reddit.com/r/opsec/)
opsec, to learn about proper habits and policies for minimizing attack surfaces and SPOF

[/r/OperationsSecurity](https://www.reddit.com/r/OperationsSecurity/)
Operations security news, resources, questions & discussions

[/r/websec](https://www.reddit.com/r/websec/)
Web security

[/r/compsec](https://www.reddit.com/r/compsec/)
computer security

[Geek Flare](https://geekflare.com/category/security/)
general security articles, tips & tools

[Google Security Blog](https://security.googleblog.com/)
latest news and insights from Google on security and safety on the Internet

[Stack Exchange](https://security.stackexchange.com/)
Information Security Stack Exchange

[Cybersecurity News & Education - The Cyber Post - Daily Hacker News](https://thecyberpost.com/)
[CyberPost](https://thecyberpost.com/category/news/)

[Cisco Talos Intelligence Group](https://www.talosintelligence.com/)
[Talos Intelligence Mail Server Reputation](https://talosintelligence.com/reputation_center/)
[Software || Cisco Talos Intelligence Group](https://talosintelligence.com/software)
CyberSecurity News

## security organizations

[Information Systems Security Association](https://www.members.issa.org/default.aspx)

[NIST Computer Security Division](https://csrc.nist.gov/)
[NIST Risk Management Framework | CSRC](https://csrc.nist.gov/Projects/Risk-Management)
[Dataplot | NIST](https://www.nist.gov/itl/sed/dataplot)
[NVD Search and Statistics](https://nvd.nist.gov/vuln/search)

[US-Cert](https://www.us-cert.gov/)

[Osint Losena Ltd](https://osint.ltd/)

[Reinventing mobile security - Secure Group](https://securegroup.com/)

[GitHub - Netflix/security-bulletins: Security Bulletins that relate to Netflix Open Source](https://github.com/Netflix/security-bulletins)
security bulletins that relate to Netflix Open Source.

[Emerald Onion](https://twitter.com/EmeraldOnion)
is a 501(c)(3) nonprofit organization and transit internet service provider (ISP).

## security organizations - owasp

[OWASP](https://www.owasp.org/index.php/Main_Page)
worldwide not-for-profit charitable organization focused on improving the security of software.

[Projects | OWASP Foundation](https://owasp.org/projects)

## security research

[securitum/research](https://github.com/securitum/research)
various Proof of Concepts of security research performed by Securitum.
[research.securitum.com - securitum.com vulnerabilities researches and cyber security education publications](https://research.securitum.com/)

[public-pentesting-reports](https://github.com/juliocesarfort/public-pentesting-reports)
is a list of public pentest reports released by several consulting security groups.

[nmap scan to a random website while I was learning this tool : hacking](https://old.reddit.com/r/hacking/comments/phwlt5/nmap_scan_to_a_random_website_while_i_was)

[Exploiting vulnerabilities in Cellebrite UFED and Physical Analyzer | Hacker News](https://news.ycombinator.com/item?id=26891811)
[Signal >> Blog >> Exploiting vulnerabilities in Cellebrite UFED and Physical Analyzer from an app's perspective](https://signal.org/blog/cellebrite-vulnerabilities/)

[Thinking about showing clients their leaked data : cybersecurity](https://old.reddit.com/r/cybersecurity/comments/u17zx2/thinking_about_showing_clients_their_leaked_data)

[Articles | Corelan Cybersecurity ResearchCorelan Cybersecurity Research](https://www.corelan.be/index.php/articles/)

[Ransomware Negotiation & Dark Web Investigation Services | Night Lion](https://nightlion.com/)

[totalhash](https://totalhash.cymru.com/)
[Team Cymru IP to ASN Lookup v1.0](https://asn.cymru.com/cgi-bin/whois.cgi)

[Request A Live Demo | IRONSCALES](https://ironscales.com/get-a-demo)

[Security Trails](https://securitytrails.com/)
[SecurityTrails: Data Security, Threat Hunting, and Attack Surface Management Solutions for Security Teams](https://securitytrails.com/#search)
APIs for Security Companies, Researchers and Teams.
[SecurityTrails Blog](https://securitytrails.com/blog)
[SecurityTrails](https://securitytrails.com/dns-trails)
[13 Online Vulnerability Scanning Tools to Scan your Website Security](https://securitytrails.com/blog/online-vulnerability-scanning-tools)

## security testing - saving money

[Gojko Adzic](https://gojko.net/favourites/testing/agile/2016/05/24/large-test-suites.html)
(2016) Five ways to reduce the cost of large test suites

## SOC2

[SOC2: The screenshots will continue until security improves | Hacker News](https://news.ycombinator.com/item?id=32018066)
[SOC2: The Screenshots Will Continue Until Security Improves · The Fly Blog](https://fly.io/blog/soc2-the-screenshots-will-continue-until-security-improves/)

## staying anonymous

[Be anonymous | Hacker News](https://news.ycombinator.com/item?id=30408236)
[Be anonymous](https://kg.dev/thoughts/be-anonymous)
(2022) Be anonymous

[Security by obscurity is underrated | Hacker News](https://news.ycombinator.com/item?id=24444497)
[Security by Obscurity is Underrated - Utku Sen - Blog - computer security, programming](https://utkusen.com/blog/security-by-obscurity-is-underrated)

[Lowering the cost of anonymization](https://desfontain.es/thesis/)

[Daniel Miessler](https://danielmiessler.com/study/security-by-obscurity/)
Obscurity is a Valid Security Layer

## stovepipe it model

[DIA CIO sees intel community moving beyond 'stovepipe' IT model | Federal News Network](https://federalnewsnetwork.com/inside-ic/2023/01/dia-cio-sees-intel-community-moving-beyond-stovepipe-it-model)

## the importance of collaboration

[Why the public and private sectors must join forces to address cyber risk for national security | The Hill](https://thehill.com/opinion/cybersecurity/3750096-why-the-public-and-private-sectors-must-join-forces-to-address-cyber-risk-for-national-security)

## tracking everything

[Carpenter's AirTags help uncover 'massive' case of stolen tools in Maryland | Hacker News](https://news.ycombinator.com/item?id=40535436)
[Carpenter’s AirTags help uncover ‘massive’ case of stolen tools in Md. - The Washington Post](https://www.washingtonpost.com/dc-md-va/2024/05/31/police-theft-thousands-power-tools/)

## VPN ads

[Investigating Influencer VPN Ads on YouTube [pdf] | Hacker News](https://news.ycombinator.com/item?id=30635989)
[vpn-ads-oakland22.pdf](https://www.cs.umd.edu/~dml/papers/vpn-ads-oakland22.pdf)

## VPN blocking

[Tell HN: Russia has started blocking OpenVPN/WireGuard connections | Hacker News](https://news.ycombinator.com/item?id=39067213)

[Check any website to see in real time if it is blocked in China](https://www.vpnmentor.com/tools/test-the-great-china-firewall/)

## VPN detection

[VPN Detection Methods : hacking](https://old.reddit.com/r/hacking/comments/phmvx7/vpn_detection_methods)

## VPN

[DNS traffic can leak outside the VPN tunnel on Android | Hacker News](https://news.ycombinator.com/item?id=40247604)
[DNS traffic can leak outside the VPN tunnel on Android | Mullvad VPN](https://mullvad.net/en/blog/dns-traffic-can-leak-outside-the-vpn-tunnel-on-android)

[VPNs on iOS are a scam | Hacker News](https://news.ycombinator.com/item?id=32488308)
[VPNs on iOS are a scam](https://www.michaelhorowitz.com/VPNs.on.iOS.are.scam.php)

## VPN Mullvad

[We are removing the option to create new subscriptions | Hacker News](https://news.ycombinator.com/item?id=31810104)
[We are removing the option to create new subscriptions | Mullvad VPN](https://mullvad.net/en/blog/2022/6/20/were-removing-the-option-to-create-new-subscriptions)

## VPN proxy - shadowsocks

[Dozens of VPNs & Shadowsocks Named in Leaked Russian Blocking Document * TorrentFreak](https://torrentfreak.com/dozens-of-vpns-shadowsocks-named-in-leaked-russian-blocking-document-231117/)

## VPN self-hosting

[An alternative to purchasing your VPN is hosting your own](https://www.reddit.com/r/VPN/search?q=vps&restrict_sr=on)
You will have much more flexibility and you can have your VPS hoster outside your country's copyright law jurisdiction.

## VPN services

[Don't use VPN services](https://gist.github.com/joepie91/5a9909939e6ce7d09e29)
which is what every third-party "VPN provider" does.
(2015) Don't use VPN services.
> Because a VPN in this sense is just a glorified proxy. The VPN provider can see all your traffic, and do with it what they want - including logging.

[NordVPN library and client code open-sourced | Hacker News](https://news.ycombinator.com/item?id=35152278)
[Nord Security · GitHub](https://github.com/NordSecurity)

[VPN-reviews](https://github.com/techlore/VPN-reviews)
[Website](https://techlore.tech/index)
[GitHub - techlore/channel-content: Techlore video channel content & more.](https://github.com/techlore/channel-content)
[GitHub - techlore/website: Home of Techlore - Spreading privacy & security to the masses.](https://github.com/techlore/website)

[Privacy Guides](https://www.privacyguides.org/providers/vpn/)
VPN Services - Find a no-logging VPN operator who isn't out to sell or read your web traffic.

[Techlore](https://techlore.tech/vpnchart.html)
VPN Chart - Transparent, community-driven VPN reviews.

[Do I need a VPN?](https://www.doineedavpn.com/)
Tell us what problems you want to solve, and we help you decide

[Dennis Schubert](https://schub.io/blog/2019/04/08/very-precarious-narrative.html)
(2019) VPN - a Very Precarious Narrative

[Viktor Vecsei](https://www.ivpn.net/blog/why-you-dont-need-a-vpn/)
(2020) Why you don't need a VPN

[Ernesto Van der Sar](https://torrentfreak.com/vpn-services-anonymous-review-2017-170304/)
Which VPN Services Keep You Anonymous in 2017?

## VPN services - Mozilla VPN

[Mozilla VPN Completes Independent Security Audit by Cure53 | Hacker News](https://news.ycombinator.com/item?id=28382585)
[Mozilla VPN Completes Independent Security Audit by Cure53](https://blog.mozilla.org/en/mozilla/news/mozilla-vpn-completes-independent-security-audit-by-cure53/)

[Firefox displayed a pop-up ad for Mozilla VPN over an unrelated page | Hacker News](https://news.ycombinator.com/item?id=36077360)
[1835158 - Firefox displayed a pop-up ad for Mozilla VPN over an unrelated page](https://bugzilla.mozilla.org/show_bug.cgi?id=1835158)

[Mozilla VPN | Hacker News](https://news.ycombinator.com/item?id=23565192)
[Introducing Mozilla VPN - Future Releases](https://blog.mozilla.org/futurereleases/2020/06/18/introducing-firefox-private-network-vpns-official-product-the-mozilla-vpn/)

## VPN services - Mullvad

[Mullvad is now available on Amazon | Hacker News](https://news.ycombinator.com/item?id=32238167)
[Mullvad is now available on Amazon (US & SE) | Mullvad VPN](https://mullvad.net/en/blog/2022/7/26/mullvad-is-now-available-on-amazon-us-se)

[Mullvad VPN was subject to a search warrant - customer data not compromised | Hacker News](https://news.ycombinator.com/item?id=35638917)
[Mullvad VPN was subject to a search warrant. Customer data not compromised | Mullvad VPN](https://mullvad.net/en/blog/2023/4/20/mullvad-vpn-was-subject-to-a-search-warrant-customer-data-not-compromised)

[Mullvad VPN now accepts Monero payments | Hacker News](https://news.ycombinator.com/item?id=31246662)
[We now accept Monero | Mullvad VPN](https://mullvad.net/en/blog/2022/5/3/we-now-accept-monero)

[The ownership and future of Mullvad VPN | Hacker News](https://news.ycombinator.com/item?id=28551960)
[The ownership and future of Mullvad VPN | Mullvad VPN](https://mullvad.net/en/blog/2021/9/16/ownership-and-future-mullvad-vpn)

[WireGuard multihop available in the Mullvad app | Hacker News](https://news.ycombinator.com/item?id=31005209)
[WireGuard multihop now easily available in the app | Mullvad VPN](https://mullvad.net/en/blog/2022/3/10/wireguard-multihop-now-easy-available-app)

## VPN services - Tailscale

[TAILSCALE](https://github.com/tailscale)
Tailscale is a WireGuard-based app that makes secure, private networks easy for teams of any scale
[Tailscale](https://github.com/tailscale/tailscal)
Tailscale is a mesh VPN that makes it easy to connect your devices, wherever they are. No more fighting configuration or firewall ports.
[Tailscale](https://github.com/tailscale/tailscale-android)
[F-Droid](https://f-droid.org/app/com.tailscale.ipn)
[Add ability to choose a custom coordination server | Hacker News](https://news.ycombinator.com/item?id=32468430)
[Add ability to choose a custom coordination server by half-duplex · Pull Request #45 · tailscale/tailscale-android](https://github.com/tailscale/tailscale-android/pull/45)

[Taildrop | Hacker News](https://news.ycombinator.com/item?id=33186523)
[Taildrop · Tailscale Docs](https://tailscale.com/kb/1106/taildrop)

[Tailscale vs. Narrowlink | Hacker News](https://news.ycombinator.com/item?id=37089739)
[Tailscale vs. Narrowlink | Narrowlink](https://narrowlink.com/docs/comparisons/tailscale)

[Tailscale ate my network (and I love it) | Hacker News](https://news.ycombinator.com/item?id=31955970)
[Tailscale ate my network (and I love it)](https://smackeyacky.blogspot.com/2022/07/tailscale-ate-my-network-and-i-love-it.html)

[Apple TV, now with more Tailscale | Hacker News](https://news.ycombinator.com/item?id=37560787)
[Apple TV, now with more Tailscale](https://tailscale.com/blog/apple-tv)

[Tailscale bug allowed a person to share nodes from other tailnets without auth | Hacker News](https://news.ycombinator.com/item?id=34420142)
[Security Bulletins · Tailscale](https://tailscale.com/security-bulletins#ts-2023-001/)

[Tailscale Funnel | Hacker News](https://news.ycombinator.com/item?id=33648341)
[Introducing Tailscale Funnel](https://tailscale.com/blog/introducing-tailscale-funnel)

[Improving Tailscale via Apple's open source | Hacker News](https://news.ycombinator.com/item?id=35559124)
[Improving Tailscale via Apple's open source](https://tailscale.dev/blog/darwin-spelunking)

[Mullvad on Tailscale: Privately browse the web | Hacker News](https://news.ycombinator.com/item?id=37420053)
[Mullvad on Tailscale: Privately browse the web](https://tailscale.com/blog/mullvad-integration)

[The New Internet | Hacker News](https://news.ycombinator.com/item?id=41080991)
[The New Internet](https://tailscale.com/blog/new-internet)

## VPN Wireguard

[WireGuard on Kubernetes with Adblocking | Ameya Shenoy](https://codingcoffee.dev/blog/wireguard_on_kubernetes_with_adblocking/)

[WireGuard in FreeBSD | Hacker News](https://news.ycombinator.com/item?id=33381949)
[src - FreeBSD source tree](https://cgit.freebsd.org/src/commit/?id=744bfb213144c63cbaf38d91a1c4f7aebb9b9fbc)

[Our User-Mode WireGuard Year | Hacker News](https://news.ycombinator.com/item?id=30275905)
[Our User-Mode WireGuard Year · The Fly Blog](https://fly.io/blog/our-user-mode-wireguard-year/)

[JIT WireGuard | Hacker News](https://news.ycombinator.com/item?id=39688545)
[JIT WireGuard · The Fly Blog](https://fly.io/blog/jit-wireguard-peers/)

## wartime

[Cyber Security: A pre-war reality check | Hacker News](https://news.ycombinator.com/item?id=40397637)
[Cyber Security: A Pre-War Reality Check - Bert Hubert's writings](https://berthub.eu/articles/posts/cyber-security-pre-war-reality-check/)

## web and app security

[Mozilla Web Security](https://infosec.mozilla.org/guidelines/web_security.html)
help operational teams with creating secure web applications.

[Application Security Wiki](https://appsecwiki.com/#/)
is an initiative to provide all application security related resources at one place.

## zero knowledge

[ZK Learning Resources](https://learn.0xparc.org/)

## zero trust

[Why are people here treating Zero Trust negatively/like a buzzword? : cybersecurity](https://old.reddit.com/r/cybersecurity/comments/uhe5ip/why_are_people_here_treating_zero_trust)

[I read the federal government's Zero-Trust Memo so you don't have to | Hacker News](https://news.ycombinator.com/item?id=30101411)
[Overview of the U.S. Zero Trust Government Mandate | BastionZero](https://www.bastionzero.com/blog/i-read-the-federal-governments-zero-trust-memo-so-you-dont-have-to)

[Generally speaking, Zero Trust is a misnomer. Rather than reducing trust to zero, it simply involves adopting a policy of controlling trust at every trust boundary, rather than letting uncontrolled trust be the primary mode of operation. : cybersecurity](https://old.reddit.com/r/cybersecurity/comments/yl9kdp/generally_speaking_zero_trust_is_a_misnomer)

[DNS problem: SERVFAIL looking up A for mydomain.com - Zero Trust/1.1.1.1 - Cloudflare Community](https://community.cloudflare.com/t/dns-problem-servfail-looking-up-a-for-mydomain-com/346517)

[Zero Trust SIM | Hacker News](https://news.ycombinator.com/item?id=32982697)
[The Cloudflare Blog](https://blog.cloudflare.com/the-first-zero-trust-sim/)

## 0 general security

[mbcrump/awesome-security: A collection of awesome ethical hacking and security related content!](https://github.com/mbcrump/awesome-security)

[GitHub - sbilly/awesome-security: A collection of awesome software, libraries, documents, books, resources and cools stuffs about security.](https://github.com/sbilly/awesome-security)

[Security Ninjas](https://github.com/opendns/Security_Ninjas_AppSec_Training)
open source application security training program.

## antivirus

[How to remove viruses and malware on your Windows PC](https://www.howtogeek.com/126911/what-to-do-if-you-get-a-virus-on-your-computer/)
Helpful HowToGeek article on cleaning out the pipes

## certification_casp

[CASP+ (Plus) CompTIA Advanced Security Practitioner Certification | CompTIA IT Certifications](https://www.comptia.org/certifications/comptia-advanced-security-practitioner)
[CASP+ CAS-004 Practice Questions | Sample Questions | Training | CompTIA IT Certifications](https://www.comptia.org/training/resources/practice-tests/casp-004-practice-questions)

[Dave - One Education](https://www.oneeducation.org.uk/members/davestucky-tech/course/#learning)
- CompTIA CASP+ course

## certification_ccsp

[Cloud Security Certification | CCSP - Certified Cloud Security Professional | (ISC)²](https://www.isc2.org/Certifications/CCSP)

## certification_cissp

[Cybersecurity Certification| CISSP - Certified Information Systems Security Professional | (ISC)²](https://www.isc2.org/Certifications/CISSP)
[CISSP Certification Course - PASS the Certified Information Security Professional Exam! - YouTube](https://www.youtube.com/watch?v=M1_v5HBVHWo)

## certification_cysa+

[Cybersecurity Analyst+](https://www.comptia.org/certifications/cybersecurity-analyst)

[Dave - One Education](https://www.oneeducation.org.uk/members/davestucky-tech/course/#learning)
- CompTIA CySA+ course
- there is a 2nd course in this domain

## certification_isaca

[IT Certification Programs | Information Technology Certifications | ISACA](https://www.isaca.org/credentialing/certifications)

## certification_isc2

[Understanding Associate of (ISC)2 Status - (ISC)² Community](https://community.isc2.org/t5/Career-Discussions/Understanding-Associate-of-ISC-2-Status/td-p/12539)

## certification_sc900

[Microsoft Security, Compliance, and Identity Fundamentals (SC-900) - Pass the Exam With This Free 3.5 Hour Course](https://www.freecodecamp.org/news/microsoft-security-compliance-certification-sc-900)

## certifications

[Information Security Certification | freeCodeCamp.org](https://www.freecodecamp.org/learn/information-security)

[Security Certification Roadmap](https://pauljerimy.com/security-certification-roadmap/)

[PEN-200: Penetration Testing Certification with Kali Linux | OffSec](https://www.offsec.com/courses/pen-200/)
- OSCP IS SUPPOSED TO BE THE BEST IN CYSEC

## certification_sscp

[IT Security Certification | SSCP - Systems Security Certified Practitioner | (ISC)²](https://www.isc2.org/en/Certifications/SSCP)

## cybersecurity

[Hacksplaining](https://www.hacksplaining.com/)
Developer Security Lessons

[GitHub - InfosecHouse/InfosecHouse: Tools & Resources for Cyber Security Operations](https://github.com/InfosecHouse/InfosecHouse)

[Training](https://opensecuritytraining.info/Training.html)

[Zenk - Security - Repository](https://repo.zenk-security.com/)

[GitHub - mthcht/awesome-lists: Security lists for SOC detections](https://github.com/mthcht/awesome-lists)

## detecting surveillance

[Is My Phone Listening to Me? How to Stop It | NordVPN](https://nordvpn.com/blog/is-my-phone-listening-to-me)

## devsecops

[GitHub - sottlmarek/DevSecOps: Ultimate DevSecOps library](https://github.com/sottlmarek/DevSecOps)

[GitHub - TaptuIT/awesome-devsecops: Curating the best DevSecOps resources and tooling.](https://github.com/TaptuIT/awesome-devsecops)
[awesome-devsecops](https://github.com/devsecops/awesome-devsecops)
an authoritative list of awesome devsecops tools.

[GitHub - hahwul/DevSecOps: ♾️ Collection and Roadmap for everyone who wants DevSecOps. Hope your DevOps are more safe](https://github.com/hahwul/DevSecOps)

## hardening

[GitHub - veeral-patel/how-to-secure-anything: How to systematically secure anything: a repository about security engineering](https://github.com/veeral-patel/how-to-secure-anything)

[How I re-over-engineered my home network for privacy and security | Hacker News](https://news.ycombinator.com/item?id=28378215)
[How I re-over-engineered my home network for privacy and security | Ben Balter](https://ben.balter.com/2021/09/01/how-i-re-over-engineered-my-home-network/)

[GitHub - decalage2/awesome-security-hardening: A collection of awesome security hardening guides, tools and other resources](https://github.com/decalage2/awesome-security-hardening)
tools and other resources.

[Practical Linux Hardening Guide | Hacker News](https://news.ycombinator.com/item?id=18992930)
[The Practical Linux Hardening Guide](https://github.com/trimstray/the-practical-linux-hardening-guide)
provides a high-level overview of hardening GNU/Linux systems.

[Linux Hardening Guide | Hacker News](https://news.ycombinator.com/item?id=25590079)
[Linux Hardening Guide](https://madaidans-insecurities.github.io/guides/linux-hardening.html)
how to harden Linux as much as possible for security and privacy.
[Madaidan](https://madaidans-insecurities.github.io/)
Security Privacy

## infosec

[GitHub - onlurking/awesome-infosec: A curated list of awesome infosec courses and training resources.](https://github.com/onlurking/awesome-infosec)

[GitHub - pe3zx/my-infosec-awesome: My curated list of awesome links, resources and tools on infosec related topics](https://github.com/pe3zx/my-infosec-awesome)

[GitHub - rmusser01/Infosec_Reference: An Information Security Reference That Doesn't Suck; https://rmusser.net/git/admin-2/Infosec_Reference for non-MS Git hosted version.](https://github.com/rmusser01/Infosec_Reference)
[Infosec_Reference | An Information Security Reference That Doesn't Suck!](https://rmusser.net/docs/#/)

## security

[Free Security eBooks](https://github.com/Hack-with-GitHub/Free-Security-eBooks)
list of a Free Security and Hacking eBooks.

[Hacking-Security-Ebooks](https://github.com/yeahhub/Hacking-Security-Ebooks)
top 100 Hacking & Security E-Books.

[awesome-sec-talks](https://github.com/PaulSec/awesome-sec-talks)
is a collected list of awesome security talks.

[Web Security Academy: Free Online Training from PortSwigger](https://portswigger.net/web-security)
General learning.
[PortSwigger Web Security Blog](https://portswigger.net/blog)
about web app security vulns and top tips from our team of web security.

[Linux Security Expert](https://linuxsecurity.expert/)
trainings, howtos, checklists, security tools, and more.

[SecLists](https://seclists.org/)
[danielmiessler/SecLists: SecLists is the security tester's companion. It's a collection of multiple types of lists used during security assessments, collected in one place. List types include usernames, passwords, URLs, sensitive data patterns, fuzzing payloads, web shells, and many more.](https://github.com/danielmiessler/SecLists)
Security Lists
Security Mailing List Archive
collection of multiple types of lists used during security assessments, collected in one place.
[SecLists/Passwords/Common-Credentials at master · danielmiessler/SecLists](https://github.com/danielmiessler/SecLists/tree/master/Passwords/Common-Credentials)
[Daniel Miessler](https://danielmiessler.com/)
cybersecurity expert and writer.

[Lenny Zeltser](https://zeltser.com/suck-at-security-cheat-sheet/)
(2015) How to Suck at Information Security – A Cheat Sheet

[Daniel Miessler](https://danielmiessler.com/study/infosecconcepts/)
(2018) Information Security Concepts

[DiabloHorn](https://diablohorn.com/)
a site for people attempting to understand security

[Matt Behrens](https://spin.atomicobject.com/2017/02/06/security-hygiene/)
(2017) Security Hygiene for Software Professionals

[GitHub - JakePeralta7/CyberSecurity: Research, Rules, Books, Tools and more basic stuff you can get anywhere](https://github.com/JakePeralta7/CyberSecurity)

[GitHub - liyansong2018/awesome-cybersecurity: A collection of awesome github repositories about security](https://github.com/liyansong2018/awesome-cybersecurity)

[GitHub - xapax/security: Stuff about it-security that might be good to know](https://github.com/xapax/security)
[Notes](https://xapax.github.io/security/)

[akenofu/HackAllTheThings: My personal repertoire of technology and security-related notes.](https://github.com/akenofu/HackAllTheThings)

## security principles

[Daniel Miessler](https://danielmiessler.com/study/practical-security-principles/)
(2018) Practical Security Principles

## self-surveillance

[How to Tap Your Network and See Everything That Happens On It](https://lifehacker.com/how-to-tap-your-network-and-see-everything-that-happens-1649292940)

## staying anonymous

[The Hitchhiker's Guide to Online Anonymity | The Hitchhiker's Guide to Online Anonymity](https://anonymousplanet.org)
[Hitchhiker's Guide to Online Anonymity](https://anonymousplanet.github.io/thgtoa/guide.html)
Privacy & Safety Guides/Tools

## threat detection

[GitHub - 0x4D31/awesome-threat-detection: A curated list of awesome threat detection and hunting resources](https://github.com/0x4D31/awesome-threat-detection)

## VPN_Guides

### What VPN should I get?

A paid VPN is recommended, as there are no good free ones that allow torrent traffic, not to mention that most will mine data from you for marketing purposes. You should seek a VPN that does not store connection and usage logs. Within this subreddit and Reddit as a whole, you will find aggressive VPN marketing tactics by nearly all top popular VPN services. Do your own research. You will often encounter the suggestion to visit [That One Privacy Site](https://thatoneprivacysite.net/vpn-section/). Do not rely blindly on the chart and look up each individual VPN's ToS. Many VPNs offer trials and refunds, use these to your benefit when determining which VPN best suits your needs.

### Extra information on VPNs

Popular VPN services aggressively market themselves on Reddit. Do not subscribe to a service just because Reddit deems it popular, cheap, or because it hits the front page. You are entrusting an entity with your personal data; do your own research. Keep in mind that VPN experiences are completely anecdotal. Someone's experience with a particular VPN may vary from location, servers, operating systems, downloads speeds, etc...

With that said, below are some resources with which you may begin your research. Most if not all popular VPNs offer trials and/or immediate refunds. Use them to your advantage in your quest to find a VPN that works best for you. Don't forget to also read their ToS!

Beware of free VPNs if you plan on using one for online purchases or to log into websites with sensitive data. Many free VPNs are able to provide their free services because they data mine, interpose ads in searches, etc...

Beware of pirating VPNs. You wouldn't pirate a condom?

One alternative to buying a VPN is hosting your own.

## windows privacy and telemetry

[Windows 10 Privacy Guide](https://github.com/adolfintel/Windows10-Privacy)
an In-depth guide on purging Windows 10 of Microsoft's attempts to track you

## secure apps

[How to make your app's architecture secure right now: separation, configuration, and access](https://www.freecodecamp.org/news/secure-application-basics)

## general security advice

[Get Safe Online | The UK's leading Online Safety Advice Resource](https://www.getsafeonline.org)

[CEOP Education](https://www.thinkuknow.co.uk)

[Online banking security | Unauthorized bank transactions | U.S. Bank](https://www.usbank.com/online-mobile-banking/online-risk-free-guarantee.html)

[What are the most effective ways to adapt to new security threats as a System Administrator?](https://www.linkedin.com/comm/advice/1/what-most-effective-ways-adapt-new-security-bpcje)

[How to stay safe on the Internet: it's proxy servers all the way down](https://www.freecodecamp.org/news/how-apps-stay-safe)

## zero trust

[What is Zero Trust? | IBM](https://www.ibm.com/topics/zero-trust)

## app security

[GitHub - paragonie/awesome-appsec: A curated list of resources for learning about application security](https://github.com/paragonie/awesome-appsec)

## code signing

[Apple Developer Docs](https://developer.apple.com/library/content/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40005929-CH1-SW1)
About Code Signing

[Apple Developer Docs](https://developer.apple.com/library/content/technotes/tn2206/_index.html)
macOS Code Signing In Depth
:star:

[Andy Brice](https://successfulsoftware.net/2012/08/30/how-to-sign-your-mac-os-x-app-for-gatekeeper/)
(2012) How to sign your Mac OS X App for Gatekeeper.
[things have changed, see this article for the update](https://successfulsoftware.net/2014/10/17/signing-qt-applications-for-mac-os-x-10-9-5-and-10-10/)

## firewalls

[0xInfection/Awesome-WAF: Web-application firewalls (WAFs) from security standpoint.](https://github.com/0xInfection/Awesome-WAF)
a curated list of awesome web-app firewall (WAF) stuff.

[Chapter 32. Firewalls | FreeBSD Documentation Portal](https://docs.freebsd.org/en/books/handbook/firewalls#firewalls-ipfw)

## hardening

[Security Harden CentOS 7](https://highon.coffee/blog/security-harden-centos-7/)
this walks you through the steps required to security harden CentOS.

[CentOS 7 Server Hardening Guide](https://www.lisenet.com/2017/centos-7-server-hardening-guide/)
great guide for hardening CentOS; familiar with OpenSCAP.

## ICS

[GitHub - ITI/ICS-Security-Tools: Tools, tips, tricks, and more for exploring ICS Security.](https://github.com/ITI/ICS-Security-Tools)

## IPTABLES

[Daniel Miessler](https://danielmiessler.com/study/iptables/)
An IPTABLES Primer

[Nick Congleton](https://www.maketecheasier.com/secure-linux-desktop-with-iptables/)
How to Secure Your Linux Desktop with Iptables

[Daniel Miessler](https://danielmiessler.com/blog/professional-firewall-iptables/)
Building a Professional Firewall with Linux and Iptables

## linux security

[The Paranoid Linux Security Guide - Linux - Level1Techs Forums](https://forum.level1techs.com/t/the-paranoid-linux-security-guide/77815)

[Vivek Gite](https://www.cyberciti.biz/tips/linux-security.html)
(2017) 40 Linux Server Hardening Security Tips
:star:

## macos security

[macOS-Security-and-Privacy-Guide](https://github.com/drduh/macOS-Security-and-Privacy-Guide)
guide to securing and improving privacy on macOS.
[macOS-Security-and-Privacy-Guide | Guide to securing and improving privacy on macOS](https://drduh.github.io/macOS-Security-and-Privacy-Guide/)

## mobile security

[GitHub - vaib25vicky/awesome-mobile-security: An effort to build a single place for all useful android and iOS security related stuff. All references and tools belong to their respective owners. I'm just maintaining it.](https://github.com/vaib25vicky/awesome-mobile-security)

[MSTG](https://github.com/OWASP/owasp-mstg)
The Mobile Security Testing Guide (MSTG) is a comprehensive manual for mobile app security testing.

[GitHub - OWASP/owasp-mastg: The Mobile Application Security Testing Guide (MASTG) is a comprehensive manual for mobile app security testing and reverse engineering. It describes the technical processes for verifying the controls listed in the OWASP Mobile Application Security Verification Standard (MASVS).](https://github.com/OWASP/owasp-mastg)

## phone number spoofing

[Phone Number Has Been Spoofed! - What to Do to Fix the Problem](https://www.techjunkie.com/phone-number-spoofed-what-to-do#What_You_Can_Do_If_Your_Number_Has_Been_Spoofed)

## proxies

[A Primer on Proxies](https://blog.cloudflare.com/a-primer-on-proxies)

[What is a Proxy Server? In English, Please.](https://www.freecodecamp.org/news/what-is-a-proxy-server-in-english-please)

## proxy - Heroku proxy

[Create Your Own 1337x Proxy](https://www.reddit.com/r/Piracy/comments/tz7nyx/guide_create_your_own_1337x_proxy/)
Try this after you have tried all the available domains/proxies.

## proxy redirect

[redirect_traffic [Frantech/BuyVM Wiki]](https://wiki.buyvm.net/doku.php/redirect_traffic)

[MoonPoint](http://support.moonpoint.com/network/proxy/putty/)
Using PuTTY to set up a SOCKS Proxy Connection

## proxy tunnel

[gre_tunnel [Frantech/BuyVM Wiki]](https://wiki.buyvm.net/doku.php/gre_tunnel)

[ipip_tunnel [Frantech/BuyVM Wiki]](https://wiki.buyvm.net/doku.php/ipip_tunnel)

## threat modeling

[GitHub - hysnsec/awesome-threat-modelling: A curated list of threat modeling resources (Books, courses - free and paid, videos, tools, tutorials and workshops to practice on ) for learning Threat modeling and initial phases of security review.](https://github.com/hysnsec/awesome-threat-modelling)

## VPN concentrator

[What is a VPN Concentrator and How does it Work? [2023]](https://www.privacyaffairs.com/vpn-concentrator)

## VPN

[Setting up a home VPN server with WireGuard | Hacker News](https://news.ycombinator.com/item?id=21421365)
[Setting up a home VPN server with Wireguard | Mikkel Høgh](https://mikkel.hoegh.org/2019/11/01/home-vpn-server-wireguard/)

[How To Set Up an OpenVPN Server on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-set-up-an-openvpn-server-on-ubuntu-16-04)
The guide still works on newer Ubuntu releases without any problems.

[Build your own private WireGuard VPN with PiVPN | Hacker News](https://news.ycombinator.com/item?id=35828046)
[Build your own private WireGuard VPN with PiVPN | Jeff Geerling](https://www.jeffgeerling.com/blog/2023/build-your-own-private-wireguard-vpn-pivpn)

[EEF Overview on what a VPN is and how to choose one](https://ssd.eff.org/en/module/choosing-vpn-thats-right-you)
Helpful guide from the EFF

[11 interesting VPN uses | NordVPN](https://nordvpn.com/blog/interesting-vpn-uses)

[Golden Frog](https://www.goldenfrog.com/blog/myths-about-vpn-logging-and-anonymity)
I Am Anonymous When I Use a VPN – 10 Myths Debunked

## VPN router

[How to Set Up a VPN Router [+Video] | NordVPN](https://nordvpn.com/blog/setup-vpn-router)

## VPN self-hosting

[How to Set Up a VPN Server at Home for Free](https://www.freecodecamp.org/news/how-to-set-up-a-vpn-server-at-home)

## VPN Wireguard

[GitHub - cedrickchee/awesome-wireguard: A curated list of WireGuard tools, projects, and resources.](https://github.com/cedrickchee/awesome-wireguard)

[WireGuard VPN - b3n.org](https://b3n.org/wireguard-vpn)

## wildcard certificates

[wildcard-certificates](https://gist.github.com/joepie91/7e5cad8c0726fd6a5e90360a754fc568)
why you probably shouldn't use a wildcard certificate.

## zero knowledge

[GitHub - ingonyama-zk/ingopedia: A curated list of ZK/FHE resources and links. Click below for the website version.](https://github.com/ingonyama-zk/ingopedia)
[Ingopedia: Your ZK Encyclopedia](https://www.ingonyama.com/ingopedia/communityguide)
