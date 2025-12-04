
# Search engine optimization (SEO)

Online marketing fulfills two purposes:

1. It maintains a long-term brand.
2. It motivates people to talk about the product with others.

If something becomes wildly popular, it goes viral and can create near-instant fame if you focus *super* heavily on the niche that drove your first popular content.

Modern marketing *needs* a decent web presence.

- Not every industry requires a well-made site, but a poorly designed website is often worse than none.
- Social media profiles can typically be sufficient, but [self-maintained websites](computers-sofware-webdev.md) allow a centralized brand and more flexibility for marketing professionals by not having the social network as an intermediary.

The art of search engine optimization (SEO) is through improving your web presence via keyword management and [design](engineering-design.md).

- This effort goes all the way from the search engine results page (SERP) all the way to [the design of the website itself](computers-sofware-webdev.md), from landing page all the way to after the customer has made a purchase.
- After learning it, most SEO work is as tedious as [accounting](money-accounting.md).

For internet marketing, there are several standardized billing arrangements:

- Depending on the billing, there's plenty of incentive to get many people to get *to* your site who won't be that interested in your product.
- Cost per thousand/mil (CPM) is the charge for every thousand impressions/views of an ad (it should be no more than ~4.2 cents per user, or $42).
- Cost per click (CPC) charges every time a user clicks on an advertisement.
- Cost per lead (CPL) charges every time someone expresses an interest in the product (e.g., a mailing list).
- Cost per acquisition (CPA) charges every time there's a new customer or sale.

## Improving hit count

The most common measurement of a website's success is from visits by users (hit count).

- Hit count matters somewhat, but the more important detail is that people will want to type in your brand name over a generic alternative.

Not all hits are good.

- A savvy stranger could make a viral complaint, so proactively and professionally manage any social media presence.
  - The quickest complaint management solution is with an on-site instant messenger service, but only if people are quickly *responding* to it.
- The click-through rate (CTR) is the number of clicks, divided by the number of impressions.
  - It *should* be more than 2%, or people are clearly not interacting with the advertisement at all.
- Have a key performance indicator (KPI) that measures how well a campaign has been.
  - The conversion numbers (from view to click to lead to acquisition to retention) will show how well each step of the marketing process has been doing.
  - Generally, CPA or lifetime value (LTV) are the best indicators, though you may want to measure the return on investment (ROI).

## Designing a website

There are [many, many design rules](engineering-design-elements.md) to nitpick about.

There are many content management systems (CMS), and almost *all* of them will work fine for the average user who just wants an online billboard (assuming they aren't a tech company with specific needs).

- However, you'll need to learn [software development](computers-software.md) or hire someone who knows it to eventually accomodating the natural consequences of a [scaling business](entrepreneur-6_scaling.md).

Naturally and seamlessly connect everything in the site with links.

- Add social media sharing buttons to every page.
- The web domain (something.com) should associate to what you sell.

Avoid using modal windows, since they're absurdly difficult to link to, create accessibility problems, and are often a world of additional [web design](computers-sofware-webdev.md) headaches with form fills and caching.

The checkout experience should be seamless, with multiple payment options, but not so many that it [overloads](engineering-design.md) the user.

While it may be tempting to expand your leads with a mailing list, only ask about the mailing list *after* the product was sold.

To maintain a consistent design, maintain fewer website pages.

- A few [well-designed](engineering-design.md) pages are *much* easier to update and rebuild than a few hundred.

## Making it fast

To make search engines favor your site and users enjoy the experience, optimize it for speed.

You should have the clicks-to-loading speed ratio over 90%.

Embed videos to a video streaming service instead of hosting them yourself.

Downgrade images:

- Use smaller images on the screen.
  - Don't downscale the image inside the CMS: downgrade it *before* you upload it.
  - If it's a very large image that matters (e.g., a [chart](data-viz.md)), have a small image that links to that one.
- Lazy-load images, with placeholder images to keep the format while it's loading.
- Since JPG images are "lossy", downgrading them means they'll look crappy, so choose something else (e.g,. PNG, GIF, WEBP)

- The [text expression of icons](computers-keyboard.md) is acceptable, but SVGs tend to load faster even if the filesizes get larger.

Self-host your fonts instead of pulling from somewhere else.

Trim out extra computer code you don't need whenever possible.

- Your CMS often will have a plugin to do this.

Test the site repeatedly as you go to make sure it's optimized.

- Test the site's loading on the slowest possible internet connection with the crappiest possible computer you can find.

## Building publicity

Advertise the content on official channels to bring your keywords more frequently into search results.

Use guerrilla marketing to get site views:

- Leave sticky notes in random places or create temporary images on buildings or cars.
- Write with chalk on sidewalks.
- Leave branded pens at banks and other public places.
- Donate branded bookmarks or books to a library.
- Give out business cards with the site on it:
  - Leave them with a tip.
  - Attach them to public bulletin boards.
  - Place them in library books associated with your business.
  - Put one in a contest fishbowl.
- Find a common frustration (e.g., vandalism, [bureaucracy](bureaucracy.md)), then place branded fliers nearby with requests to email feedback.
- Connect with influential people by connecting with less-influential people they know first.
- Give a commission of *your* commission to other people who refer business to you.
- Provide a free community service, with casual advertisements for more service if they're interested.

## Specific forms of content

Like any other [marketing](marketing.md), tailor your marketing messages to the media.

From the content in the website, all the way into the "meta tags" in HTML, each keyword has to be parsed very carefully.

- Further, the meta tags can have the Open Graph Protocol (popularized by Facebook) to specify the content in it.
  - The most essential tags are:
    - og:title (the title of the content)
    - og:type (the expressed format, such as image or text)
    - og:image (a link to the image representing the content)
    - og:url (the canonical and permanent URL, which also represents as its [database](database.md) ID)

Make sure to communicate clearly within the site where the user is, what they can do, and what will happen if they do it.

- If you're not communicating things plainly, people will tune out the information.
  - The [content/copy](language-writing.md), photos, and overall message should all match up.
- Frequently, your writing will be too broad (and therefore too many people won't be interested) or too specific (and will drive people who might be interested away).
- Have a decisive, clear call to action (CTA) to work through it.

### Blogs

Keep a separate blog page to avoid cluttering the homepage.

A blog is only successful if it has at least 4 of the following 6 components:

1. Sincere
2. Urgent
3. Appropriately timed
4. Brief
5. Controversial
6. Useful

When posting:

- Solve a problem for the reader instead of selling a product.
- Grab the reader's attention with compelling images.
- Capture the target demographic with a strong and keyword-laden title/header and matching description.
- Use very particular keywords to create statistically unpopular (long-tail) search words.
- Verbose and descriptive descriptions show up more often in search results.
- Adding a video's text transcript increases search engine results.
- Do things unconventionally to make people select your content more often.
- Create many relevant links to other content you want to advertise.
- The longer your essay, the more keywords, and the more traffic you'll get.
- Showcase informal reviews from loyal users, since everyone will think the well-written reviews are paid actors!

To stand out, you'll need something *far* more appealing than what everyone else is talking about, which requires immense [creativity](mind-creativity.md).

Routinely:

- Find a publishing cadence and stick with it (e.g., once a week).
- Repost all applicable content on relevant social media profiles.
- Consistently repost great-quality content with a creative remix (e.g., infographics, cartoons, quizzes).
- Verify everything is visually presentable, links work correctly, and everything conforms to the brand's image.
- Schedule content posts that show the brand in a new light.
- Reorder links and emphasize the cornerstone content to place the best content first.
- Network with others to link across websites.
- Blog relatively frequently to show search engines the site is still live.
- Create a community by opening up the end for questions and then answering them.
- Invite industry experts to contribute to your blog.
- Constantly look for new content channels and layers.

### Social media

Don't waste time on social channels that don't speak to your audience:

- Not everyone wants the product, so don't follow everyone.
- Discussion forums gives profound long-term results, but takes *lots* of content and time.
- In-person events actually have [*dis*-economies of scale](economics.md).
- Streaming networks are only good when you've reached a critical mass (often ~40,000 followers).

Increase the volume of posts, add visual media, and create videos to fight the deluge of competitors.

- However, make sure your content is legitimately interesting, or people won't care.

It's difficult to retain visitors, so try surveys, forums, building a community, or an email list.

- Give them something for their information (e.g., 10% discount, $20 gift certificate), and do *not* simply ask for their information without a reason for them to give it.
- Promise something in your content that people will actually *want* to read, then give it to them.

If you start using ads, you'll probably lose about 10% of your users compared to not having them.

- Be careful with paywalls as well, since customers will need to receive at least some free content of value to not feel left out.

Build hyperlinks directing toward your site (i.e., "backlinks") whenever possible:

- Comment on social media elsewhere about the site.
- Create a network of sites with complementary elements.
- Work with affiliates to link to each other.

Search engines usually blacklist unethical SEO.

- Search engines discourage sites where people visit and then leave (high bounce rate).
- If you manipulate search engine systems, you'll get temporary spikes in views and dramatic dropoffs later.
- You'll find more search engine attention by creating high-quality content people *want* to consume and share (organic exposure).
- Keep on top of [all the back-end technical elements of web/app design](computers-sofware-webdev.md).
  - Try technical tricks like semantic markups and editing meta tags.
  - Make sure the website *actually functions well*: a bad web interface is worse than an awful font/image pairing.
  - *Only* add features that reflect the image you want to convey.

Watch for the Content Scarcity Paradox:

- Synchronous, time-sensitive content can boost engagement (e.g., instant messaging).
- However, the longer the content is, the harder it is to consume (e.g., a 2-hour video).
- If the content is both short and asynchronous, it will be *too* abundant.
- If the content is both long and synchronous, it will be *very* scarce.
- The best hybrid is to have "stories" that give short-term windows of content (e.g., 1 day).

## Email

Don't over-send emails, or people will unsubscribe.

- If you have plenty of content (i.e., more than once a month) publish news directly to your brand website.

Do *not* ask people privately to share content on social media because it forces them into an awkward conflict:

- If they liked it already, they would probably share it.
- If they *don't* share, they'll appear disorganized.
- They can say no and seem rude.
- Instead, tell them about it and how it may interest them, then let them look at it at their leisure.
