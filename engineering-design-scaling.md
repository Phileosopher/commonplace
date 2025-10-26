
# Design at scale

Often in large organizations, a [committee](groups-large.md) makes changes to the UX, and it tends to follow a lengthy procedure for it to roll out.

First, there are a variety of techniques to learn what the users' optimal behaviors will be:

- Focus groups will ask for opinions and feelings related to specific cues.
- Card sorting, where people organize and categorize information in a way that makes sense to them.

There's a *lot* of testing that goes into most large-scale visual designs:

- A/B testing, through exposing alternative interfaces side-by-side.
- Diary testing, collecting information via users writing a "digital diary" about their experience as they use the interface.
- Gorilla/monkey testing, where the users repeatedly behave incompetently.
- Guerilla testing, by going to public places and getting feedback.
- System usability scale, where people are interviewed on 10 1-to-5 questions on how much they like the interface.
- Task-based testing, by giving people instructions and observing how well they do them in the interface, as well as any hangups in their flow.

The entire experience of UX testing can be harrowing for designers and UX developers, since test subjects are only talking about what they [feel](mind-feelings.md) versus the creators focusing on [reality](reality.md) or on an [idealized aesthetic](values-quality.md). However, every $1 invested in good UX can often make a return of $2-100 in practice.

However, A/B testing can yield inaccurate results when implemented alone. People often enjoy novelty but don't realize its adverse effects. Large organizations frequently make a decision after *extensive* A/B testing that doesn't capture an ideal product, and they're forced to make a difficult decision:

1. Keep it as it is, with all its terrible elements.
2. Rework the change, which will often confuse the users who have to adapt.
3. Make another change to compensate, which will often confusing a *different* subset of users.

The best prevention is to make design decisions that, if they were wrong, won't make a dramatic difference to results. By pure [statistical reality](math-stat.md), designers are almost *guaranteed* to foul up on something:

- Give *many* options for the user, even if it looks ugly or unwieldy in the end.
- Make small modifications, step-by-step, instead of large changes.
- *Always* maintain [convention](habits.md), even if the designers hate it.
- Keep everything as open as possible to allow people to [fix](https://adequate.life/fix/) and [improve](creations.md) on it later.

Plus, design decisions are subject to the perils of [miscommunication](language.md) and [power dynamics](power-types.md) that come with any [large group](groups-large.md). To avoid it, projects often develop in as many phases as necessary to prevent working on a wrongly defined [purpose](purpose.md):

1. First, get consensus on an idea, which typically has to be realistic, but whoever approves it must [believe](understanding-certainty.md) in it.
2. Conduct plenty of focus groups and research to find exactly what people would want or how they would use the thing.
3. Designers/engineers will typically create wireframes and stock prototypes of the thing. These wireframes often give a visual aesthetic of what the final product will look like, but lack most details.
4. After someone approves it, the creators will create a near-finished work without any features. This is the first time the thing actually "exists", but it's pretty lame by comparison to the final product.
5. After another approval, the product is slated for final production, which will often involve testing to make sure that it can be mass-produced or shown to the public.
6. Finally, after another round of approvals, it's shipped out the door, with numerous tweaks and updates as things fail.
7. Maintain a continuous design cycle that *constantly* harvests feedback and updates the product to get better.
8. If the product itself has become obsolete or needs to be abandoned, use the information from it for a *new* design, and start at step 1 again.

To combat the extra complexity, there are a few major ways to improve interface changes:

1. Understand *exactly* the kinds of people using the interface. This often requires including someone in the discussion who would normally *not* talk with the designers/developers, and preferably isn't part of the organization at all.
2. Create a "visual language" that demarcates a consistent pattern across the entire organization, often with a style guide.
3. Put together a shared set of components the entire organization is supposed to use.
4. Constantly communicate as things change, using one system for all discussions.
5. Keep designers and [engineers](engineering.md) constantly discussing with each other about any changes.
6. Constantly [document](language-writing-documentation-cs.md) as things change, and keep it integrated with the style guide.
7. No matter what, *always* maintain constraints on what designers can do (e.g., time limits, space limits).

If the product is particularly complex, divide out the rate of the design's change into "layers":

- Site - its location or designated place, (hours to never)
- Skin - its exterior structure (minutes to every 20 years)
- Structure - foundation and load-bearing capacity (weekly to rarely)
- Services - people who must maintain it (hourly to every 7-15 years)
- Space Plan - changes *inside* the element (every few months to every 10-30 years)
- Zeitgeist - shared awareness and understanding (every few months to every 2-3 years)
- Stuff - the inner workings and miscellaneous domains

It's worth indicating that "slower" design elements tend to constrain the "faster" ones.

Generally, the size of large organizations and the work required tends to inhibit completely free customization. In simple commodities this isn't a problem, but more high-end products need more freedom for the users to explore and [identify](identity.md) with the object.

Another risk of large-scale endeavors is complete blandness. Since people can get easily offended at small distinctions, the best form that offends nobody is incredibly boring. It also pleases very few people as well.

## Big issues in design

Most of the time, UX developers follow safe fashions, but frequently they'll [run a fashion out to its most extreme](trends.md) and make the interface almost unusable, often for a few broad reasons:

- Designers became intimately familiar with what they were designing, and have very limited interaction with the users. Often, they may only know what marketing professionals or their friends think.
- Designers have seen the same old, tired thing. They tend to not understand that the thing exists in its current form is because it was often *the* best way to do it, or they're disregarding conventions that everyone is used to.
- When a new design trend or [technology](technology.md) becomes popular, designers tend to abuse it.
- Sometimes, [managers](mgmt-1_why.md) will override the designers' professional experience, testing, and common sense based on their personal preferences or interests.
- Often, once a product has become complex enough to fulfill a specific use, its complexity forms a [cult-like](marketing.md) culture around it that elevates the object as more valuable than what it actually *does*. At that point, it satisfies [market demand](economics.md) through appealing to an [image](image.md) of sophistication, while being awful for the user (and also opening up the opportunity for [a better version](entrepreneur-1_why.md) elsewhere).

There are plenty of examples of bad fashions:

- Using touchscreens instead of buttons in [automotives](autos.md).
- Having [internet-connected](networks-computer.md) devices that don't need to be connected to the internet.
- Aggressively auto-connecting Bluetooth when the user doesn't want it.
- Giving "popular choices" that are *clearly* not popular.
- Washing out the visual contrast for style reasons, but making it somewhat unreadable.

The best solution, in all respects, is to get users using the thing as soon as possible, since making large changes can become very difficult or expensive. After all, the marketing professional and even the *designer* can't understand how the user interacts with it as much as the user.

## Dark patterns

One of the more sinister uses of UX is to create "dark patterns" that steer users to make decisions they otherwise wouldn't have taken:

- Motivating a service upgrade that someone may have not wanted to pay for.
- Provoking the user to give information they likely wouldn't have given.
- Create friction against actions they don't want the user to take (e.g., unsubscribing, deleting user profile).
- Requiring the user to repeatedly decline a permission or service, ignoring the user's response, or intentionally causing the app/site to crash once they select it.
- Requiring a login to an otherwise-free service (like cat videos), even when the user doesn't want to give a login.
- Requiring users to speak to a human being to cancel their subscription.
- Showing a product is out of stock, with a completely identical product with the same price, but with a clear reduction in its weight.

Most engineers often compromise when they're instructed to design those patterns, and evil prevails when good people do nothing.

## Addiction

Very frequently, UX developers are motivated to create elements that draw the user in indefinitely. Even when something is free, more time with the software means the person is more likely to spend money on an upgrade, give data that can be sold, or increase the value of selling [advertisement space](marketing.md).

The obsession with "user engagement" (i.e., [addiction](addiction.md)) makes "user experience" in many become "user exploitation", and it'll present itself through many subtle dark patterns:

- Creating a feeling of urgency with relative timestamps (e.g., "3 hours ago" instead of "6:15 PM").
- Making an endless loop of behavior with infinite scrolling instead of a "More" button or link.
- A fake points system with icons that reinforce the experience with interaction and feedback.
- Tweaking the system to promote or bury certain user-made content, either through hidden [algorithms](computers-programming-algorithms.md) or at the developer's/company's whim.
- Making leaving the service frustratingly difficult, or requiring a human being to finalize the process.
