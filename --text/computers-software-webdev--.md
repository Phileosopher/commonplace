
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
