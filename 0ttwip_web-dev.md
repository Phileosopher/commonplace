
The internet is a fascinating experience, but people often take it for granted and don't know how it works.

Like most other aspects of computers, web development encompasses *many* sub-disciplines.

Every single "thing" on the internet is given a sequence of characters as a "uniform resource identifier" (URI) to indicate its location. Sometimes multiple URIs can point to the same thing, and other times a URI is simply routing to multiple other URIs. It's simply a means of specifying a location for the computer.

Most network [protocols](/protocols/) work over the internet. Since it's a worldwide network, various protocols and standards need to talk with each other, and their interoperability can be an *extremely* complicated endeavor.

To add to the above complexity, there are also [cybersecurity](/security/) concerns from literally the entire planet. Every website essentially needs a [signed certificate](/authentication/) to be trustworthy. Even then, it's absolutely crucial to develop [healthy web browsing habits](/cysec/).

## Hardware

The hardware of the internet is a worldwide [network](/networks/), mostly connected through various cables and [wireless signals](/radio/), along with some [satellite connections](/gps/).

While computers maintain constant connection with each other (by human standards), the systems involved require *constant* asynchronous data transfer:

- Sometimes, website data is preloaded to ensure it'll present itself.
- Other times, a resource represents as a placeholder (e.g., an image), and is then replaced by a more memory-consuming resource (e.g., a video).

## OS

Most web servers run on Apache [Linux](/unix/) in an "AMP server" configuration (**A**pache HTTP Server, **M**ySQL, and **P**HP or **P**erl or **P**ython). The most popular one by far is Linux (LAMP), though quite a few are Windows-based (WAMP) or MacOS (MAMP).

## IP address

Ever since the "Internet of Things", just about every computer has an "IP address". This means they have a code (IPv4 and/or IPv6) to distinguish them from all the other ones.

The "public IP address" is usually the internet-facing "router" or "gateway device" that the computer is connecting through, though it can be a [VPN's IP](/cysec/) if you have one. Underneath that, there are multiple "private IP addresses" assigned to every computer on that network.

There are 3,706,452,992 possible public IPv4 addresses, and IPv6 has some technical hangups. Part of it comes from the fact that IPv4's dotted-quad notation is on the upper threshold of [standard human memorization](https://adequate.life/memory/), while IPv6 is absurdly hard to memorize. To that effect, IPv4 addresses have become [somewhat of a tradable commodity](https://gainedin.site/economics/) due to scarcity.

However, IP management has become more complex in light of increased VPN usage. With a VPN, there's another VPN IP to consider as well, meaning that IP blocking isn't necessarily a good solution anymore to deal with people trying to access a website.

## RSS

The RSS and Atom [protocol](/protocols/) are utterly simple: an updated ticker-tape of the most recent information available in a feed.

RSS ("really simple syndication") was the inception of the idea, and Atom tried to flesh out the concept further.

RSS and Atom feeds are simple enough that tehy'll probably last as long as the internet. These feeds can apply to nearly anything: blog posts, podcasts, music releases, and just about anything else that can be updated.

Most sites have feeds built-in, but are an often arcane setup to find if you don't know what to look for.

Sometimes, tech companies will *not* make their feeds freely available to enforce [a walled garden](/faang/). But, in those instances, you can usually use a third-party update service for whenever a page changes or new content is distributed.

## Always expanding

The internet is constantly changing and adapting, and each technology is constantly adapting to *other* technology improvements. In effect, that means this summarized essay may be mostly obsolete in 10-20 years.
