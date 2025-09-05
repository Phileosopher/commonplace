
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
