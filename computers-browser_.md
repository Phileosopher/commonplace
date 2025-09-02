
Usually, when people think of web development, they imagine web browsers. However, there are very specific aspects to browsers that specialize far more than simply the internet as a collective [network](networks-computer.md).

## Requests

Most of the internet's backbone for daily use is the HTTP protocol (hyper-text transfer protocol) and HTTPS (its secure version). Historically, it only sent HTML, but it now sends CSS, along with all sorts of [more advanced code](computers-languages.md).

The entire HTTP system is designed as a host/client relationship, with the client being the requester and the host being the responder.

Client computers submit a request to a host/server computer with a URL, an endpoint path off that URL, and one of a several possible methods:

- GET - ask for information from a specified location (sent in the URL directly and therefore *not* [securely sent](computers-cysec.md))
- POST - send data to a server to create or update a resource
- PUT - send data to a server to create or update a resource, but the information is "idempotent" (i.e., it won't create multiple instances of the resource if sent multiple times)
- HEAD - same as GET, but won't return any information, great for [testing](computers-software-redesign.md)
- DELETE - deletes a specified resource
- PATCH - like PUT, but only applies partial modifications to a resource
- OPTIONS - describes communication options for a specified resource
- CONNECT - starts a two-way commmunication (a "tunnel") with a resource
- TRACE - performs a message loop-back test to test the path to the target resource, also great for [testing](computers-software-redesign.md)

The request may optionally also include a body, headers, query strings, and the HTTP version.

The server/host computer interprets the information, then sends a response back with *its* protocol version, headers, a status code, and status text. The status codes/text have *mostly* been around since HTTP/1.0, but some have been added since HTTP/1.1:

- 100s - the host received and understood the header information, and tells the client computer to wait.
  - **100 Continue** sending the body of information
  - **101 Switch** protocols
  - **102 Processing** WebDAV at the server, but no response is available yet ([RFC 2518](https://datatracker.ietf.org/doc/rfc2518/))
  - **103 Early Hints**, where the server can send some early response information before the final HTTP message ([RFC 8297](https://datatracker.ietf.org/doc/rfc8297/))
- 200s - the request was received, understood, and accepted
  - **200 OK**, the standard response, though a GET request will give something connected to the requested resource and a POST will give something that describes or contains the result of the action
  - **201 Created** a new resource
  - **202 Accepted**, but hasn't been fulfilled yet, meaning it may be disallowed when processing later
  - **203 Non-Authoritative Information** because the server is a proxy to speed up data transfer but has a modified version of the original response from the primary server, new to HTTP/1.1
  - **204 No Content** to return
  - **205 Reset Content** request back to the client
  - **206 Partial Content** because the client's "range header" isn't all the information (e.g., resuming interrupted downloads, splitting a download into multiple streams).
  - **207 Multi-Status** for complex WebDAV needs that require multiple separate response codes ([RFC 4918](https://datatracker.ietf.org/doc/rfc4918/))
  - **208 Already Reported** for WebDAV, so not including again ([RFC 5842](https://datatracker.ietf.org/doc/rfc5842/))
  - **226 IM Used**, as in an "instance manipulation" for delta encoding ([RFC 3229](https://datatracker.ietf.org/doc/rfc3229/))
- 300s - the request is being redirected
  - **300 Multiple Choices** for the client to choose (typically the user)
  - **301 Moved Permanently** somewhere else, and everything should redirect to the new URI.
  - **302 Found**, though was once called Moved Temporarily, that indicates where a resource is moved to ([RFC 1945](https://datatracker.ietf.org/doc/rfc1945/) originally, but clarified as 303 and 307 in HTTP/1.1)
    - **303 See Other**, where the response can be found with another URI with the GET method, and a POST method means the server received the data and the client should issue a new GET to the new URI
    - **307 Temporary Redirect** to another URI and repeat the request, but future requests should use the original URI
  - **304 Not Modified** from the client's copy, so there's no need to re-transmit the resource
  - **305 Use Proxy** since *only* a proxy has the information, used since HTTP/1.1 but many web browsers don't obey this code because it's a wide-open risk for [hacking](hacking.md)
  - **306 Switch Proxy**, which originally meant that subsequent requests should use the specified proxy, but is no longer used
  - **308 Permanent Redirect** to a given URI, which is the same thing as 301 but doesn't allow the client's HTTP method to change.
- 400s - the client computer has an error
  - **400 Bad Request** because there was an apparent, but uncertain, client error
  - **401 Unauthorized** is similar to 403 but [authentication](computers-cysec-authentication.md) wasn't provided or has failed
  - **402 Payment Required** was reserved for future use, but hasn't been implemented
  - **403 Forbidden** means it was a valid request, but the host is refusing to act on it
  - **404 Not Found** means the requested resource couldn't be found, but that's it
  - **405 Method Not Allowed** because the request method isn't supported for the requested resource
  - **406 Not Acceptable** because the resource doesn't conform to the requested resource parameters
  - **407 Proxy Authentication Required** before accessing the resource
  - **408 Request Timeout** because the server waited too long for the client
  - **409 Conflict** because of the current state of the resource (e.g., being edited by 2 different computers)
  - **410 Gone**, meaning it was previously present but is no longer available and won't be available again
  - **411 Length Required** because the request didn't specify a length
  - **412 Precondition Failed** because the host doesn't fulfill one of the request header preconditions
  - **413 Payload Too Large** for the server to process
  - **414 URI Too Long** for the server to process
  - **415 Unsupported Media Type** for the server or resource to support
  - **416 Range Not Satisfiable** for the portion requested in the range header
  - **417 Expectation Failed** within the request header's Expect field
  - **418 I'm a teapot** was an April Fools' joke that shuld theoretically return a teapot's request to brew coffee ([RFC 2324](https://datatracker.ietf.org/doc/rfc2324/) and [RFC 7168](https://datatracker.ietf.org/doc/rfc7168/))
  - **421 Misdirected Request** toward a server that can't produce a response
  - **422 Unprocessable Entity** because the request was well-formed but semantic errors made it impossible to follow
  - **423 Locked** from access
  - **424 Failed Dependency** in a WebDAV configuration because it depended on another request that had failed ([RFC 4918](https://datatracker.ietf.org/doc/rfc4918/))
  - **425 Too Early** for the server to risk processing a request that might have to be replayed ([RFC 8470](https://datatracker.ietf.org/doc/rfc8470/))
  - **426 Upgrade Required** to the current protocol (e.g., TLS/1.3), specified in the Upgrade header field
  - **428 Precondition Required** because the server requires the request to be conditional ([RFC 6585](https://datatracker.ietf.org/doc/rfc6585/))
  - **429 Too Many Requests** by the user in a given amount of time, typically used for "rate-limiting" ([RFC 6585](https://datatracker.ietf.org/doc/rfc6585/))
  - **431 Request Header Fields Too Large** because the server won't process that much at once ([RFC 6585](https://datatracker.ietf.org/doc/rfc6585/))
  - **451 Unavailable For Legal Reasons** because the server operator can't [legally permit it](legal-safety.md) ([RFC 7725](https://datatracker.ietf.org/doc/rfc7725/))
- 500s - the host computer has an error
  - **500 Internal Server Error** because there was an apparent, but uncertain, host error
  - **501 Not Implemented** because either the host doesn't recognize the request method or can't fulfill the request
  - **502 Bad Gateway** because the server received a bad response from *its* upstream server
  - **503 Service Unavailable** because the server can't handle the request
  - **504 Gateway Timeout** because the server was a gateway or proxy and didn't receive a timely response from *its* upstream server
  - **505 HTTP Version Not Supported** because the HTTP version in the request wasn't supported
  - **506 Variant Also Negotiates** because the "content negotiation" between multiple variations creates a circular reference ([RFC 2295](https://datatracker.ietf.org/doc/rfc2295/))
  - **507 Insufficient Storage** on the server to complete a WebDAV request ([RFC 4918](https://datatracker.ietf.org/doc/rfc4918/))
  - **508 Loop Detected** while processing a WebDAV request ([RFC 5842](https://datatracker.ietf.org/doc/rfc5842/))
  - **509 Not Extended**, but the server needs further extensions to fulfill the request ([RFC 2774](https://datatracker.ietf.org/doc/rfc2774/))
  - **511 Network Authentication Required** by the client to gain network access, typically from intercepting proxies that control access to the network (e.g., "captive portals" to require [agreement to Terms of Service](people-contracts.md)) ([RFC 6585](https://datatracker.ietf.org/doc/rfc6585/))
- Further, there are plenty of other unofficial 400 and 500 codes that aren't supported by any standard.

Optionally, the response may also include a body, which can sometimes represent a *lot* of information, context-depending.

The standards for HTTP have moved around and are constantly improving. HTTP/1.1 was a great idea but had issues, and HTTP/2 and HTTP/3 are becoming increasingly better.

## Web domains & DNS

When you type in SomeWebsite.com, each of the domains has a "top level domain" (TLD):

- .com
- .net
- .biz
- [Many, many, many more](https://en.wikipedia.org/wiki/List_of_Internet_top-level_domains)

These TLDs are authorized by [ICANN](https://www.icann.org/), a [nonprofit-in-name-only](mgmt-npo.md) that issues those domains. Different organizations can buy them, then sell the subdomains at a fixed price. Some TLDs (like .edu or .gov) are only granted to specific authorities, but most of them are free-for-all first-come first-serve.

Below that, there are second-level domains (e.g. **somewebsite**.com). Further than that, there are also subdomains (e.g., **subdomainat**.somewebsite.com).

The "fully qualified domain name" (FQDN), which is often the "uniform resource locator" (URL) (e.g., `https://somewebsite.com`), should eventually connect to an IP address somewhere.

The domain information connects back to a system called DNS ("domain name service"), which has "resource records" located in "zone files" that specify where resources are located:

- There are many, *many* DNS records, but the bare-bones specifications mostly exist as [standards](standards-computers.md) in [RFC 1035](https://www.rfc-editor.org/rfc/rfc1035).
  - These records can be for specific resources, or "wildcard" across many possible situations.
- A - what [IPv4 address](networks-computer.md) to look for.
- AAAA - what IPv6 address to look for, specified by [RFC 3596](https://www.rfc-editor.org/rfc/rfc3596).
- CAA - [Certification Authority](computers-cysec-authentication.md) Authorization, specified by [RFC 6844](https://www.rfc-editor.org/rfc/rfc6844).
- CNAME - canonical name record, which indicates an alias of one name to another.
- DNAME - delegation name record, which is like CNAME but includes all subnames as well.
- MX - mail exchange record, specifies the servers that accept email for a domain, specified by both RFC 1035 and [RFC 7505](https://www.rfc-editor.org/rfc/rfc7505).
- NS - name server record, which indicates who the "authoritative" registrar is.
  - The domain resides at a registrar, which is often *not* where the computer files are hosted.
- PTR - pointer to a canonical name.
  - The client will typically look for an index.html or index.php file at that location.
- TXT - was originally designed for human-readable text, but has devolved to a miscellaneous junk drawer for machine-readable data.

The software (usually the web browser) makes DNS requests, which are answered with DNS records. DNS configurations connect to most of the issues over whether a website works or not.

To access most websites, a computer will [access](networks-computer.md) several computers that sit potentially across the world:

1. Since it's rapid compared to anything else, the software first looks within cache [memory](computers-memory.md) locally stored in its memory. Later, it'll also typically archive more information to that cache.
2. If there's nothing in the cache, it'll access the name server of the ISP ("internet service provider" who provides the internet service) about the DNS request.
   - If a name server happens to be recursive, it'll find the answer for the client, starting with its cache. Otherwise, it'll redirect the query to somewhere else.
3. If the name server doesn't have the information, it'll ask the root server, (also known as the Global Top Level Domain Server, or GTLD) to find the name server with the relevant name (e.g., there's a GTLD for all .com domains).
   - There are also [alternative DNS roots](https://en.wikipedia.org/wiki/Alternative_DNS_root) as well, beyond the standard ones, which allow for [decentralized systems](computers-distsys.md), [cryptocurrency](computers-blockchain.md), or [nations the ability to micromanage their internet](faang.md).
4. The GTLD will send back information that routes to the "authoritative" registrar (Step 6) or a DNS resolver.
5. The client accesses the DNS record held at a DNS resolver (e.g., CloudFlare at 1.1.1.1, Google at 8.8.8.8, Quad9 at 9.9.9.9).
   - Most internet service providers have *awful* built-in resolvers that keep very obsolete DNS records, so it makes sense to connect to your own (e.g., Cloudflare, Quad9).
   - It's not *too* difficult to make your own DNS resolver, but most DNS resolvers used by most websites are [gigantic FAANG corporations](faang.md).
6. The DNS resolver will point to a registrar, which has the authoritative DNS record.
   - When there are only a few large DNS resolvers, small failures can quickly turn off gigantic chunks of the internet because the computers will return a 500 error with no re-routing.
7. The registrar will either have resource records, or an NS record that points somewhere else, typically to a host (e.g., ns1.actualsite.com and ns2.actualsite.com).
   - If the resource records are part of the domain itself, they need "glue records" that specify exactly where that record is (e.g., ns1.somedomain.com is inaccessible before getting to somedomain.com).
8. Typically, most of the specific DNS records will be wherever a website is hosted, with the corresponding IP addresses or connected resources at least *somewhat* referenced there.
9. Further, there are extra [security aspects](computers-cysec.md), such as SSL/TLS and DNSSEC, that make [malicious hacking](computers-cysec-pentest.md) more difficult.
   - The difference expresses most simply as the domain being either http:// or https://.
   - SSL is very fast, and TLS [is rather slow by comparison](https://istlsfastyet.com/).

The entire DNS has had some improvements as well over decades of use:

1. Core DNS was made in the 1980s when the internet was smaller, so the 1990s saw DNS Security Extension (DNSSEC), which adds [encryption based on public key cryptography](encryption.md) to DNS standards.
2. VPNs route traffic to a given website through their IP address, but the DNS resolver still sees the raw IP address of the original client computer, even if it's using DNSSEC.
3. DNS over HTTPS (DoH) and DNS over TLS (DoT) have [encrypted](encryption.md) the information to the DNS resolver, but the resolver can still see the site the client is trying to visit.
4. Oblivious DNS over HTTP (ODoH) obscures what the DNS resolver sees.

The DNS *might* be a simple reference from a domain to a specific IP address, but it can (and often does) get *much* more complicated:

- somewebsite.com - the www is removed, mostly for cosmetic reasons.
- `www.news.somewebsite.com` - a subdomain of somewebsite.com, which can be for technical or cosmetic reasons.
- `www.somewebsite.otherwebsite.com` - somewebsite.com stands on its own, but it's an add-on of otherwebsite.com.
- `http://somewebsite.com` may send the browser somewhere differently than `https://somewebsite.com`.

Whenever there's a change at the primary DNS location, the DNS will "propagate" to all the other DNS records. This can often take a few days, which can be an *eternity* if the DNS records were incorrectly configured.

But, not all domains are equal:

- Some of them require existing conditions to be qualified as a domain (e.g., .org, .us).
- They all have a maintenance fee, both to the registrar for servicing it and to ICANN directly:
  - Most sites like .com and .net are ~$10-20 annually.
  - Others cost more (.ai is ~$90, .inc is >$1,000 and climbing).
  - Some are cheaper or free (.xyz is $12, .tk is free).
- To that end, many people who [scam](social-engineering.md), [hack](computers-cysec-pentest.md), and [host pirated content](computers-distsys-torrent.md) like using cheap/free, disposable domains, which may affect a domain as a [marketable](marketing.md) address when legitimate organizations block the entire domain extension.
- Some domains (e.g., .de) will validate *before* registration is approved.
- Some domains require more information (e.g., .us requires submitting a connection to [your legal fiction](image-modern.md)).

## Web search

Obviously, not everyone knows about SomeWebsite.com. The information on that site may be critically important to someone, but how would they know? The internet is a big place, and there are a *lot* of possible domain names!

To fill in the gap, some tech people created a "search engine", which is software designed to organize and categorize everything. Search engines are a relatively simple concept, but powerful:

1. Use a "web crawler" to dig through websites and find all the "keywords" the user may want.
2. Sort and process the information to create [database](database.md) associations between the keywords and "hyperlinks".
3. Run a [search algorithm](computers-programming-algorithms.md) whenever the user requests a keyword or phrase.
4. Collect data off the users' interactions with that website:
   - Count how long someone is on a webpage, and how many places they access within that website.
   - Rank the sites upward when they link to many sources beyond their site.
   - Downgrade sites when people simply "bounce" onto the page and off again.

Most search engines are so powerful that they tend to "web scrape" entire websites as well. This is particularly egregious [in the case of extremely large groups](computers-cysec.md).

## Search engine optimization

Since businesses want to make lots of money, there's an entire division of [marketing](marketing.md) that specializes in nothing but "search engine optimization" (SEO). [It involves a *lot* of technical back-end](https://www.toptal.com/developers/webdevchecklist):

1. Add your domain to all the major webmaster consoles (e.g., Google, Yandex, Bing, etc.).
2. Generate an XML site map and submit it on those consoles.
3. Add an [SSL certificate](computers-cysec.md) and make sure it's sending secure information.
4. Add links all over the site that link to other parts of the site (~3-4 links every 1500 words).
5. Do absolutely *everything* you can to improve [web/app accessibility](engineering-design.md).
   - Make sure your [UI](engineering-design.md) is properly color-matched.
   - Verify the input fields match up (e.g., make the "phone number" box only work with numbers and have (xxx)xxx-xxxx in it).
   - Describe all images with the alt tags (the "alternate" tag if the photo doesn't show up).
   - Use short URLs that don't have dates in them and are never more than 2 [subfolders](computers-files.md) deep.
   - Set social media image, title, and description (e.g., Open Graph [protocol](standards-computers.md) for Facebook, viewport meta tag for mobile).
6. Do absolutely *everything* you can do to speed up the website, both for users and for web crawlers:
   - [Debug](computers-software-redesign.md) all the code and delete unused code.
   - Compress and locally host all the images and videos.
   - Locally host your fonts.
   - Add keywords into the body of the page, as well as inside the title tag and [meta](data.md) description.
7. Test *everything* with [emulators](computers-distsys-vm.md) and real hardware for all sorts of weird "edge cases".

Obviously, some less-than-legitimately-motivated people have wanted to exploit the situation. If you've ever clicked through to an odd webpage that says, "Here's how you can have the best bicycle tires that are tires for biking, of which bicycles are the best you can bicycle to and from work for bicycling", you're looking at SEO gone horrifically wrong. Thankfully, the engineers behind the search algorithms usually punish sites that [hack their algorithm](hacking.md) in the long-term, so we can still achieve high-quality results.

## Web browser features

Most typical users interact with the internet through a "web browser", which is software specifically designed to handle a wide variety of internet content including pictures, [videos](engineering-screen.md), and [games](computers-software-gamedev.md).

While some web browsers emphasize [cybersecurity](computers-cysec.md) and others emphasize speed, they almost always do just about the same thing: give a safe and fast web-browsing experience that also *doesn't* download bloated, broken or [malicious](computers-cysec-malware.md) code.

Most information displayed on a web browser is "HyperText Markup Language" (HTML), which is more of a markup language than a proper [scripting language](computers-languages.md). It pairs with "Cascading Style Sheets" (CSS) that give visual style, as well as a scripting language (which is often JavaScript).

Amusingly, CSS was designed to address constraints within HTML, and JavaScript was designed to address constraints in CSS. Therefore, HTML-only or HTML+CSS has a certain type of simplicity that JavaScript can complicate.

To keep track of a browser (such as logging in), the "host" will frequently send files called "cookies" to save specific information (like your login or shopping cart) inside the browser cache within the user's computer.

- This is *very* convenient, since it can allow someone to stay logged-in, tailor the website to specific types of users, or keep track of information about the web browser to make the browsing experience more seamless.
- However, stored cookies can also lead to [privacy issues](computers-cysec.md), especially when third-parties (like advertising companies) can track behavior *across* websites or when [hackers](hacking.md) track where you're browsing.

The Tor [protocol](standards-computers.md) and its browser adds layers of anonymity to the web-browsing experience, which means more layers of complexity.

## Browser/page UX

While the [user experience](engineering-design.md) of mobile devices often separates the experience of internet-browsing into a wide variety of "apps", most of those apps are simply various specialized web browsers inside the [operating system](computers-os.md) (e.g., Electron app).

Differently sized screens and inputs are *not* trivial issues! The wide variety of [screen implementations](engineering-screen.md) means the user could be using a [mouse](computers-mouse.md) and [keyboard](computers-keyboard.md) on an office machine, their cell phone or tablet with their fingers, or an interactive [VR headset](computers-vr.md). To make it simpler, developers sidestep the pixel measurement in lieu of a root em (or "rem") measurement based on a basic font size (typically 16 pixels).

At one time, near the year 2000, almost every internet-enabled computer was working on about a 1024×768 [screen](engineering-screen.md). Now, they can range from 480×320 through to 3840×1080 (and growing), with all sorts of odd rectangular shapes (with [VR](computers-vr.md) and [driverless automotives](computers-autos.md) adding even more variety). This adds a layer of challenge to good web design, but has a few simple tricks:

- Make elements move and resize relative to the screen edges, such as with a percentage or with a *float* command.
- Use fluid grids to keep everything in place as things move around.
- Drop out or replace elements with "media queries" as the screen size hits a "breakpoint" when it gets too small or large.
- Focus on mobile-first or desktop-first design (depending on what you're designing), then work toward filling it in on the other.
- Program a "CSS reset", where the default design gets replaced by the developer's designs.

To maintain a workable [UX](engineering-design.md) across the wide variety of screens a web browser may use, front-end web developers use "media queries", which are instructions to change or add/remove elements depending on the size of the screen. This is called "responsive web design", which you can see simply by going to a web page with media query code (like this one) and scrolling in and out (either by pinch-zooming or CTRL and +/-).

## Visual elements

Visual web design is [an art form of its own](engineering-design.md). Besides all the conventions of [user experience](engineering-design.md), the site must be SEO-friendly (i.e., low-enough memory to quickly transfer across the internet). This means all aspects of programming [web graphics](engineering-graphics.md) is a Zen art: enough to get the point across with as little data transfer and distraction as possible.

One of the easiest ways to design motion into websites is by using a CSS feature called "keyframes". Instead of getting in the weeds with [graphics](engineering-graphics.md), developers can indicate multiple states with percentages, then the language has enough logical power to deduce the shifts:

1. State A is 50 pixels wide and red at 0%.
2. State B is 100 pixels wide and blue at 50%.
3. State C is 300 pixels wide and green at 100%.
4. The entire element will shift from red, double its size and shift to blue, triple its size and shift to green, then cycle back in reverse, over and over.

It's worth noting that CSS is not the *only* way to design graphics. For certain use cases, other 2-dimensional graphical representations like Canvas are better options. And, for 3-dimensional graphics, [shaved-down game engines](engineering-graphics.md) like Unity and OpenGL work better.

While it's barely detectable to most people, web browser pages have a "favicon" logo sitting in the web browser tab (or in the Task Manager tray in the [operating system](computers-os.md)). This little square logo ranges from 16 to 64 pixels wide and shows up in a *lot* of places in a web browser including web searches, history, and dropdown menus.

## Website structure

Websites, and by extension "social media", have degrees of complexity:

1. The most basic website simply conveys information by a single user or group (e.g., this site).
2. The data may become more complex than text and allow [images](engineering-camera.md), [videos](engineering-camera.md), and [audio recordings](computers-speakersmic.md).
3. When the site provides any public forum for discussion, it becomes "user-driven" (e.g., a comments thread).
4. Some sites are almost entirely user-made content, and are often called "wikis".
5. If each user gets the freedom to make their own custom content, it's a "profile page" system.
6. The user may also have a "feed" that allows that user to present constantly updated, date-sorted data.
7. Each element of data might give the user freedom to constrain [permissions](computers-cysec-authentication.md) for which users (or unidentified computer users) can access the information.
8. Users may have the freedom to make comments on other users' information.
9. The comments system may be enhanced so heavily that the users can centralize it on a topic, which is often called a "forum".
10. The users may grant shared permissions with one another, with some demarcated relationship (e.g, friend, connection, buddy, etc.).
11. Finally, "recommender systems" can recommend portions of relevant users' data to other users.

In practice, the core of social media has distilled to several website categories:

- Blog - mostly static content by a single user or group, sometimes allowing comments (e.g., [WordPress](https://wordpress.com/), [Medium](https://medium.com/)).
- Wiki - mostly static content by many users, but only allowing edits and not comments (e.g., [Wikipedia](https://www.wikipedia.org/), [Fandom](https://www.fandom.com/)).
- Content showcase - a media-based network that showcases specific, topic-based content (e.g., [DeviantArt](https://www.deviantart.com/), [Pinterest](https://www.pinterest.com/), [YouTube](https://www.youtube.com/)).
- Forum - constantly updating content by many users, organized by topic (e.g, [Reddit](https://www.reddit.com), [Lemmy](https://join-lemmy.org/)).
- Feed - constantly updating content by many users, typically algorithmically sorted (e.g., [Twitter/X](https://twitter.com/), [Instagram](https://www.instagram.com/), [Mastodon](https://joinmastodon.org/)).
- Online Store - content that users can update for the purpose of selling merchandise (e.g., [Amazon](https://www.amazon.com/), [Etsy](https://www.etsy.com/)).
- Classified Ads - constantly updating content users can use for various reasons, but mostly for business reasons (e.g., [Craigslist](https://craigslist.org/), [eBay](https://www.ebay.com/)).
- Everything Sites - an abominable hybrid of everything above, without much coherence for the users on how to use it (e.g., [Facebook](https://www.facebook.com/), [LinkedIn](https://www.linkedin.com/)).

Further, the entire social network can be [distributed](computers-distsys.md) as-needed, with the extreme version of it being *completely* decentralized (such as a [blockchain implementation](computers-blockchain.md)).

## App design

To make apps more "cross-platform", they're often SPAs ("single page apps") to cut down on various interface differences. SPAs are literally only 1 webpage ([this other site I made](https://entertaining.space/) is an example). They can interchangeably be an app or webpage, since they don't have links to any other internal pages.

In fact, Electron apps are effectively working with all the inefficiencies of a web browser. While it's *great* at building a quick cross-platform solution, the greatest [efficiencies](computers-software-redesign.md) will come in rewriting the software for each of those particular [operating systems](computers-os.md).

* * * * *

## Additional reading

HTTP

- [The HTTP crash course nobody asked for](https://fasterthanli.me/articles/the-http-crash-course-nobody-asked-for)
- [HTTP Methods GET vs POST](https://www.w3schools.com/tags/ref_httpmethods.asp)

Domains

- [mess with dns](https://messwithdns.net/)
