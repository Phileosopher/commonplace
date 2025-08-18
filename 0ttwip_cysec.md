
Cybersecurity is doing several things:

1. Putting a box around the hardware/network, giving the trusted/verified computers and people access.
2. The untrusted/unverified computers/people are denied access.
3. In case things break, the entire system has backups with pretty much the same permissions.

However, trust isn't strictly binary.

- People move in and out of groups/networks, earn trust, break trust, appear to be trustworthy but aren't, and so on.
- Some things (such as anything public on the internet) are far more valuable/useful than other things (such as [trade secrets](http://notageni.us/ip/) or core [operating system](/os/) files)
- People forget passwords and [hard drives](/memory/) break down.

There are many [security philosophies](/security/) that bind a good security policy together, but it's worth noting that cybersecurity isn't really a subject of computer science as much as protecting computers from bad stuff happening, which means moving the box of trust around with two battlefronts at once:

1. Safety *of* the information, which usually involves making duplicates of things ("redundancy") for when the computers fail.
2. Safety *from* bad people, which usually involves verifying people and devices ("authentication").

It's important to understand that [hacking comes in a variety of forms](/hacking/), so it's not simply theft or destruction and all mid-level IT-skilled people can technically "hack". Most of the time, a "hacker" in popular culture is a PenTester.

* * * * *

## How to defend yourself

Safety and performance have tradeoffs beyond a certain point, but there are many simple-enough ways to protect yourself from most [cyber attacks](/hacking/).

As a general concept, [computers are extremely versatile](/computer/). The engineers who first designed computers never expected that the computer needed to be *forbidden* to do some things. But, like dynamite and the aeroplane, computers are highly effective weapons. Unfortunately, a reliable [lock](/authentication/) doesn't always protect computers.

### Simple Things

The easiest way to make your computers safer is to reduce the "attack surface" by cutting down the possible "attack vectors" . One of those ways is to "harden" a computer by [turning everything off you're not using](/security/).

By renaming default "credentials" that come with most hardware, hackers can't easily gain high-level access to computers (e.g., username "admin" with password "admin").

Most computers come with pre-installed software (also known as "bloatware"). Most hackers know this, so it's a very good idea to remove *all* the pre-installed software that isn't a [driver](/os/) (e.g., "HP User Experience" and "Lenovo Assistant").

The companies who make the hardware and software are constantly trying to stay ahead of hackers. Thus, with *very* few exceptions (such as an update that *creates* vulnerabilities), install their firmware and software "patches" as soon as reasonably possible.

In Windows, many services come pre-installed and running. Disabling them when you don't use them (via services.msc) prevents a hacker from using them. Remote Desktop Services is probably the most notorious example of this, since it permits anyone to remotely control a computer.

If you ever need to dispose of any non-volatile [memory](/memory/) (i.e., hard drives, portable media), avoid leaving supposedly deleted data on there. If you're particularly concerned, physically destroy the memory by drilling holes into it.

Instead of remembering 150 passwords, use a password manager, such as KeePass. It serves several benefits:

- Most people tend to remember 1 password that they use on everything. This means that hackers who break into myrandomsocialnetwork.com can enter that email and password into every major bank and social network.
- Remembering permutations of a password (e.g., MyDogIsAwesome65, mydogisAwesome67) is very hard on your memory, so keeping information safely inside an encrypted file means you only need to remember *one* password.
- Writing down a password on paper means someone else can steal it or take a photo of it.
- It's harder to forget 1 password than 150 of them, no matter how simple your inner schema is.

Keep backups of everything important. This can range from simply keeping your core documents in [cloud storage](/cloud/) all the way to maintaining a networked disk image of everything you've done. It all depends on what you need.

Never save credit card information when you purchase something, and make sure the purchase is a legitimate place. Intermediary groups (e.g., PayPal) aren't much help because *they* can get [hacked](/hacking/), so the only "safe" method might be to transfer via [blockchain cryptocurrency](/blockchain/) if you're particularly concerned.

If you don't use software on your computer, uninstall it. Keep the installation program/file around if you need, but unused programs with file access permissions can be used to hack your computer.

### Operating System

Only give permissions to things that the app/plugin *needs*. Often, permissions in mobile devices are permanently on, so make it a habit to manually deactivate them in your settings after you're done using that app.

If there's a legitimate system update, install it immediately. If you're worried about it, read the [changelog](/documentation/) to see what they changed.

### Browsing

Assume that [Big Tech](/faang/) is collecting data on you. They often can create a profile of you based on your computer or IP address, even if you don't have an account with them. Simple information like your IP address, uploaded photos, time spent on your website, and device's [screen resolution](/screen/) can be useful to cross-reference other details.

Pay very, *very* close attention to the address bar, since that's the easiest way people get [hacked](/hacking/). `https://facebook.com` is legitimate, but `http://facbook.com` or `http://faceebook.net` is an impostor site. You'll also notice that it won't have a current SSL certificate (and your browser will often display an indicator of it).

Whenever you see a "hyperlink", mouse-over it or long-press it to investigate the link. Make sure you're familiar with the [domain](/web-dev/).

Mind whether the website starts with HTTP or HTTPS. Older websites often use HTTP and are fine for browsing, but *never* send important information over HTTP if you can ever help it.

For that matter, make sure you're using secure [protocols](/protocols/). Use FTP instead of SFTP, use SSH instead of Telnet, use Signal instead of SMS.

Avoid installing any plugins into your browser unless you know *exactly* what they do. Even then, make sure it's legitimate software and not coming from a dodgy source. However, install an ad blocker like uBlock Origin to make sure you're not getting deluged by the constant targeted advertising.

If you don't know if you feel comfortable with your computer keeping information about where you went, then use private/incognito mode. Regularly clear your browsing history if you don't want advertisers to know what you're doing.

Many other computers ([the OS](/os/), [other apps](/faang/), governments, [internet service providers](/networks/), [hackers](/hacking/)) can see your browser history, so regularly clear your browser history, or use separate browsers/profiles for different activities.

If you're particularly paranoid, get Tor browser, which is a fork of Firefox that hyper-emphasizes security, and will delete your browsing history and cookies every time you close it.

If you don't want other people to see your [IP address](/networks/), use a VPN. Preferably, pay for it, since free VPNs tend to [track data](/faang/).

Even with all this, you're never fully safe from someone hacking you, though the above measures make you much safer.

### Cyberbullying

While everything else above is a matter of technical understanding, avoiding harassment online is a much more social matter.

Avoid sharing or showing personal details whenever possible. If you must put in information you don't want to (e.g., birthday), then put in the wrong information.

Pay attention to the "atmosphere" of the social network or forum. If your idea is unpopular in that group, you'll likely get assaulted and called names.

Make sure to only speak from things you *know* for sure, and spell-check frequently. People will nitpick over very dumb things, and other users will heavily scrutinize *any* misstatement.

Acknowledge you're wrong when you are, no need to hide it. In any online community, it's almost a certainty that you missed something that they know, and you can both coexist with your own value systems as long as you're both willing to yield that you *don't* have all the answers to everything.

Even then, there are mentally unwell people who *will* try to force an argument ("trolling"). While blocking them is often a good idea if it gets toxic, make sure that person in real life won't take further action. If there are lots of trolls in a portion of the internet, stay away from it for your own [happiness](https://adequate.life/happiness-1/).

### Large Organizations

Beyond this, there's also the risk of [your technological relationship with large organizations](/faang/). They don't always have your best interests in mind, and have the ability to surveil and subdue you if it serves their interests.

When signing the terms of service, pay very close attention to their policies on data security, data sharing with third parties, and data collection. People often click through without realizing how much they're giving up.

### Canaries

Frequently, the safest way to stay secure is to keep a nearly-disposable computer that's disconnected from the network, such as a [Raspberry Pi](/pi-arduino/) Zero or a cheap cell phone. That way, if you ever run across a USB drive you don't know about or a potentially suspicious-looking file, you can open it in there without any risk to your more important computers.

However, even without that, you can still use a [virtual machine](/vm/) to isolate suspicious files you're working with.
