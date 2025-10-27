
# Web domains & DNS

When you type in SomeWebsite.com, each of the domains has a "top level domain" (TLD):

- .com
- .net
- .biz
- [Many, many, many more](https://en.wikipedia.org/wiki/List_of_Internet_top-level_domains)

These TLDs are authorized by [ICANN](https://www.icann.org/), a [nonprofit-in-name-only](mgmt-npo.md) that issues those domains. Different organizations can buy them, then sell the subdomains at a fixed price.

Most domains are free-for-all first-come first-serve, with a secondary market for selling them. However, some TLDs are only granted to specific authorities, such as the following examples:

- .edu: educational institutions
- .org: not-for-profit organization
- .mil: US military
- .gov: US government

Below that, there are second-level domains (e.g. **somewebsite**.com). Further than that, there are also subdomains (e.g., **subdomainat**.somewebsite.com).

The "fully qualified domain name" (FQDN), which is often the "uniform resource locator" (URL) (e.g., `https://somewebsite.com`), should eventually connect to an IP address somewhere.

The domain information connects back to a system called DNS ("domain name service"), which has "resource records" located in "zone files" that specify where resources are located:

- There are many, *many* DNS records, but the bare-bones specifications mostly exist as [standards](standards-computers.md) in [RFC 1035](https://www.rfc-editor.org/rfc/rfc1035).
  - These records can be for specific resources, or "wildcard" across many possible situations.
- A - what [IPv4 address](networks-cs.md) to look for.
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

To access most websites, a computer will [access](networks-cs.md) several computers that sit potentially across the world:

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
- Some domains require more information (e.g., .us requires submitting a connection to [your legal fiction](people-image-modern.md)).
