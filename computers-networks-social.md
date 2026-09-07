
# Social networks explained

"Social media", as a concept, has degrees of complexity:

1. The most basic website simply conveys information by a single user or group (e.g., this site).
2. The data may become more complex than text and allow [images](engineering-camera.md), [videos](engineering-camera.md), and [audio recordings](computers-speakersmic.md).
3. When the site provides any public forum for discussion, it becomes "user-driven" (e.g., a comments thread). This is when people technically consider it "social media".
4. Some sites are almost entirely user-made content, and are often called "wikis".
5. If each user gets the freedom to make their own custom content, it's a "profile page" system.
6. The user may also have a "feed" that allows that user to present constantly updated, date-sorted data.
7. Each element of data might give the user freedom to constrain [permissions](computers-infosec-authentication.md) for which users (or unidentified computer users) can access the information.
8. Users may have the freedom to make comments on other users' information.
9. The comment system may be enhanced so heavily that the users can centralize it on a topic, which is often called a "forum".
10. The users may grant shared permissions with one another, with some demarcated relationship (e.g, friend, connection, buddy, etc.).
11. Finally, "recommender systems" can recommend portions of relevant users' data to other users.

## Social network design

In practice, the core of social media has distilled to several website categories:

- Blog - mostly static content by a single user or group, sometimes allowing comments (e.g., [WordPress](https://wordpress.com/), [Medium](https://medium.com/)).
- Wiki - mostly static content by many users, but only allowing edits and not comments (e.g., [Wikipedia](https://www.wikipedia.org/), [Fandom](https://www.fandom.com/)).
- Content showcase - a media-based network that showcases specific, topic-based content (e.g., [DeviantArt](https://www.deviantart.com/), [Pinterest](https://www.pinterest.com/), [YouTube](https://www.youtube.com/)).
- Forum - constantly updating content by many users, organized by topic (e.g, [Reddit](https://www.reddit.com), [Lemmy](https://join-lemmy.org/)).
- Feed - constantly updating content by many users, typically algorithmically sorted (e.g., [Twitter/X](https://twitter.com/), [Instagram](https://www.instagram.com/), [Mastodon](https://joinmastodon.org/)).
  - In particular, the path of the [Bad Information Age](https://gainedin.site/information/) leads everything to video-based feeds.
- Online Store - content that users can update for the purpose of selling merchandise (e.g., [Amazon](https://www.amazon.com/), [Etsy](https://www.etsy.com/)).

## Algorithmic tailoring

To design an [algorithm](computers-programming-algorithms.md), there has to be a desired outcome of that algorithm. In the case of a social network, the algorithm is designed for several non-exclusive and somewhat competing purposes:

1. To maintain the user's interaction (by consuming).
2. To provoke the user's interaction (by commenting or posting new content).
3. To provoke the user to consume [advertising](marketing.md) (and therefore get paid for it).
4. To provoke the user to do something else outside the social media.

Since the last one is *not* advantageous to the social media company, and the first one is the easiest for someone to do, most social media uses an endless scroll feature with content specifically tailored for that user's continuous consumption.

However, besides the self-interested aspect of every social media business, every social media algorithm is subject to [Goodhart's Law](philosophy-lawsaxioms.md). In this case, any algorithm tailored to maximum effectiveness in something will invariably provoke someone to exploit it.

And, with any algorithmic tailoring, there will be more [bias](mind-bias.md) toward some things over other things indiscriminately:

- Prioritizing the most-viewed things will make a few things absurdly popular, but nobody will view the other 99.9% of the content, which disincentivizes creation.
- Prioritizing the least-viewed things will make unpopular things rise to the surface, but without any measurable quality metric the consumers will do something else.
- Prioritizing anything based on viewer attention will emphasize low-quality things that capture that attention.
  - Even supposedly high-quality things (e.g., authentic writing, high-quality production values) run the risk of exploitation by [morally unscrupulous people](computers-infosec-socialengineering.md).
- [The YouTube Apparatus clearly emphasizes this exploitation in far more detail](https://www.cambridge.org/core/elements/youtube-apparatus/36600D69788530F805C650B70976A585).
