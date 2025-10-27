
# Good computer interface design

Designing a "user interface" (UI) is a subdivision of visual artistry. At one time, the design field was oriented toward "human computer interaction" (HCI) but has since moved to the realm of "user experience" (UX) from the ubiquity of business within technology. UI is what users perceive, while UX/HCI is what users do.

All the [general rules of good design](engineering-design.md) apply, but computers take a divergence in a few key areas.

## Rules

The speed of successful [tech trends](trends.md) mixed with the relatively young age of most [tech innovators](trends.md) tend to see the industry *constantly* break the rules of UX.

No design is *ever* perfect, but computers have taken bad design to a new level:

- Make things invisible.
  - Exploit the tyranny of a blank screen.
  - Don't use hints for effectively operating the system.
- Give no feedback or results of what happened.
  - Have a huge interface gap between different related elements.
  - Make a gap in time between doing and observing anything.
- Be arbitrary.
  - Use non-obvious commands.
  - Be inconsistent and change the rules.
  - Let something get done one way in one mode, then another way in another.
- Make operations difficult to understand.
  - Use idiosyncratic language or abbreviation.
  - Use uninformative error messages or notifications.
  - Make all the information available in [the manual](language-writing-documentation-cs.md), instead of in the interface.
- Be impolite.
  - Treat errors and near-errors as completely invalid.
  - Make errors seem or be very dangerous, as if they're [breaches of contract](people-contracts.md).
  - Permit 1 error to destroy valuable work.

Users can only draw from their [environment](reality.md) (observations) or [memory](imagination.md) (expectations), so [computer design](engineering-design.md) frequently borrows from the world around us:

- Building things to reflect biological form, such as making the case look like a plant or adding earth tones.
- Adding context-sensitive colors, such as shades of gray for industrial tones or a brightly colored palette for children's themes.
- Inputs that match how we interact with nature (e.g., a scroll wheel interacts like rolling a ball on the ground, a steering wheel interacted like pulling the reins of a horse).

We draw [patterns](symbols.md) that connect different aspects of the world around us ("skeuomorphism"), so it's *absolutely* critical that technology reproduce the feedback mechanisms in other existing technology or in nature.

- This can be very difficult if the industry standard has been *bad* design.
- To get new users to understand new concepts, they must migrate from the old through slow adaptations, which are *guaranteed* to move more slowly than the technology itself.

The available information from that technology also allows for more specialized design requirements:

- Computers can only display an astronomically small percentage of all their information at any given moment, so designers must severely consider the users' "attention economy", which makes [good design philosophy](engineering-design.md) (especially regarding visual hierarchy and visual structure) absolutely critical.
- Since a computer is *constantly* working when it's on with an inhuman logical flow, use empty space to articulate silence to the user and personalize it to indicate that a human designed it.
- Make sure the presented information is using any tracked [location data](logistics-navigation.md), and make it location-agnostic if there's a [VPN](computers-cysec.md) or no location. Generally, there's still usually an *approximate* nation or region to derive data from.
- If there is *any* information about the [operating system](computers-os.md), assume the user is using that particular OS. Either way, give a simple selection for *all* available OSes.
- If the user has provided information, use it to tailor all relevant [algorithms](computers-programming-algorithms.md) of the software (e.g., their genre preference should define *all* the content).
- Provide personal information based on the software's usage. Generally, a large-scale enterprise's needs are different from a home user.
- Since people value their privacy, build trust *before* asking for permissions for more information.
- Create designs that direct the user's incentive toward something else that is *not* the computer. We are [wired to need human connection](humanity-universals.md), and computer-assisted [interaction](people-conversation.md) is typically *less* [meaningful](meaning.md) than in-person.

## Communication

Typically, the nature of tech trends means most of the styles communicates from the sci-fi/fantasy of the time to imply the technology is "futuristic" by that decade's [fashions](trends.md).

The domain of technology has *magnitudes* of complexity, so users have a dramatically higher chance of frustration than any other industry:

1. Most people don't understand computers in full.
2. They also often don't communicate that lack of understanding to others, for various reasons.
3. This lack of shared non-understanding creates a conspiracy of silence.

[Software engineers](computers-programming.md), by the nature of their trade, do not need great [communication skills](people-conversation.md) and often have limited [people skills](people-image.md), so many computer design elements have been, from their inception, fundamentally obtuse.

This is almost standard in tech, and never seems to [trend](trends.md) otherwise. Most software is either bloated or under-communicates, depending on the psychological idiosyncrasies of the software engineer and design team (if any).

[Cybersecurity](computers-cysec.md) design, by contrast, is simply the *reverse* of good design: instead of communicating what a user can do, the designer is obscuring and *hiding* things instead.

Of course, this means many possibilities for growth within computers. Many more things frustrate users in computers than anywhere else, so there are more possible places where [taking a risk](entrepreneur-1_why.md) may yield a positive result.

## Documentation

The complexity of computers almost *mandate* a manual, and it's about as important as the product itself (since the product won't work without the knowledge contained in that manual). It's a necessary evil from how utterly complex computers are.

With software, it's not difficult to include help files and browser-based [hyperlinks](computers-sofware-webdev.md) to lead the user to what they need. With hardware, it's worth including both simplified and advanced documentation for different levels of users, or to at least maintain a permanent archive hyperlink built onto the package.

The most effective internet-based form of a manual is a Q&A-based forum with the engineers and product designers answering user questions, since it allows a direct conduit for feedback from the users, which gives the designers criteria to develop *future* iterations of the product.

## Forcing functions

Forcing functions within the domain of computers is *way* more dangerous than any other domain. While people may [hack](hacking.md) their fridge or car to do what they want, tech hackers are *very* intelligent and *really* hate forcing functions, especially lock-outs. Many of them will try to break a lock-out on principle alone.

## Human error

Computers work with information at scale, so devote intensive effort to preventing the user from breaking everything with one button-press.

- Ask for confirmation before deleting or moving large amounts of something.
- Hold on to important information before deleting (e.g., "Recycle Bin").
- Require that massive tasks (e.g., deleting 1,896 files) require typing in the exact number shown.

However, it is vital that any error-correcting system *must* work or people will absolutely hate it. And, once it's implemented, people will come to *depend* on it, so be careful removing it if you already have it.

## Elements

Since a computer is so different from everything else in its implementation, the [elements of a computer](engineering-design-elements-cs.md) have specific requirements.

## Design at scale

[Software development](computers-software.md) has a unique, nasty problem:

1. First, the software must be designed, then [tested a *lot*](computers-software-redesign.md) to ensure it actually works.
2. Then, the software must be tested to ensure that people *beyond* the designer are capable to use it.

The implication of this is that the [project management lifecycle](mgmt-2_projects.md) in a large organization will likely be *twice* what the manager is probably thinking.

Further, on top of making design changes, the revolving nature of version control requires a few elements at the end of the process:

1. Use paced updates and small version control updates on *each* element, to avoid complicating things with a large-scale update all at once.
2. Have automation that tests each of the dependencies, to track for any failings in the interfaces.
3. Automate *all* updates for each element, meaning nobody has to manually change elements as they update.

Fixing bad software/hardware design isn't as easy as it sounds. The technology experience can suffer for multiple reasons:

- It takes 5-6 ideas to get a design right, and startups often only get 1-2 shots at good design before they run out of money, so their design often becomes industry-standard even if it's not that great.
- Most design rules in tech create *many* contradictions which arise across a plethora of edge cases.
- The people who design software are human beings who [may not want the users' best interests](faang.md), and have reason to employ "dark patterns" to make some elements difficult to access (e.g., unsubscribe, delete account, remove connection).
- [Social trends](trends.md) can redefine elements, so most websites are *constantly* changing. Some elements become archaic, new elements become the standard, and some elements can become purely offensive.

Good software design starts with a rudimentary structure, then works outward. Unfortunately, the feature/complexity paradox dramatically expresses itself within computers:

- Watching a rapid update of files can be scary to watch for a non-tech-savvy person, but a spinning wheel often won't indicate an error.
- Every new version of the software adds features, but often clutters up the menu or makes the experience more inaccessible.
- Without discretion, every software eventually becomes an okay multi-use product instead of a great single-use one.
- The only way to keep an inherently complex product like software or a computer simple is to *constantly* investigate how to merge or remove obsolete features. Just make sure you explicitly document those changes, and allow people to roll back [those updates](computers-software-redesign.md) if they need.
- If the features become difficult to work with, reorganize the features and give the user the full option between the new and old way.

Generally, large-scale changes can force an immobilized design experience. Back when [Windows 95](computers-os-windows.md) dominated the OS market, people could tweak their wallpaper, colors, and sound effects, but most granular control is constrained in most mainstream [OS's](computers-os.md). Having the freedom to keep a customizable interface would require exponentially more work, or the quality would suffer.

At least, theoretically. Customizable elements heavily contribute to a user's feeling that the interface is "theirs", and gives the users a more [meaningful](meaning.md) experience, even while it's more awkward.

### Big issues at scale

Some UI ideas are terrible, for various reasons:

- Hidden elements (e.g., scrollbars, buttons) can often work fine on mobile devices, but are unwieldy if someone has a desktop computer.
- Moving elements around with every update will perpetually disorient the user, especially if they don't communicate the changes publicly beforehand or in an "Updates" prompt when they open the program.
- Not instructing the user via tooltips when hovering over an element. This often leads to confusion and, sometimes, tremendously large mistakes.
- Failing to clarify the difference between input locations, such as placing "Projected Budget" and "Estimated Budget" on two input boxes next to each other.
- Saving information when the user presses "Submit", but not communicating a response.
- Saving information that the user volunteered, but not using that information for inherently obvious future tailoring of the experience.
- Excessive JavaScript or elements that interfere with the user experience instead of help direct their attention.
- Modal windows (windows that pop out information inside the page) can't easily have a hyperlink to it, can't be opened in a new tab, can't be bookmarked or shared as a link, make the back button confusing, and can't compensate for slow page load.
- Making the "Sign In" selection difficult to find, or making it indistinguishable from the "Sign Up" one.
- QR codes without an alternative URL to key in, since not all devices reliably read them.
- Creating an infinite scroll feature on a product that doesn't need it.
- Only having a "like" button for feedback, but without extra clarifications or using the numerical "likes" as a simple means of prioritization.
- Requiring the user install extra software or accept extra [permissions](computers-cysec-authentication.md) that are convenient for the developer, but often involve [tracking data that the user may not want tracked](faang.md).
- Removing any features that the users had become familiar with.
- Messages and prompts with excessive wording and explanation, instead of providing [documentation](language-writing-documentation-cs.md) for people who wish to read more.

Most tech designers are *way* more fickle than the average non-tech comparison, which makes tech design even *more* volatile:

- They'll get bored way more quickly, and their creative tendencies will provoke them to reinvent the wheel by designing [a better volume control](https://uxdesign.cc/the-worst-volume-control-ui-in-the-world-60713dc86950?gi=64381f3bdf3b), menu system, mouse pointer, or whatever.
- They'll be *much* quicker to adopt trends, and the speed of adoption determines how fast it'll get abused. It can lead to absolutely absurd interfaces until it's [patched later](computers-software-maintenance.md).
- Sometimes, they'll stumble across a stunningly *brilliant* design, but it'll take too much work to maintain, and a future update will replace it with a simpler (and more boring) one.
- Asking for [permissions](computers-cysec-authentication.md) or for the user to download software is highly convenient for the developer, even while it's annoying for the user, and that selfishness bleeds into the software experience.
- Giving icons or elements users may find interesting in focus groups, but don't plainly articulate the information the user may need.
- Moving things around on the user, but without giving any warning or communication of the old ways of doing things.

Generally, the context of UX determines which direction it'll fail.

- If it's consumer-facing (e.g., [web design](computers-sofware-webdev.md)), the push for simplicity and ease-of-use will make arcane systems hiding behind deceptively simple visual elements.
- If it's more technical or organizationally facing, the constant [feature bloat](computers-software-maintenance.md) will make the interface cluttered with all the extra edge cases present for the user.
- The solution is to find ways to make it accessible for the first-time user, in such a way that a technical user won't feel hampered by the experience. This is difficult to do.

While it may be useful to catch most glaring issues, A/B testing can absolutely *ruin* the longevity of a design in lieu of short-term gains.

- Harassing users will maximize short-term results, but will drive away long-term growth.
- Over time, UX driven by A/B testing will generate a lingering unpleasantness with anyone who *didn't* want to perform precisely according to the metrics.

Computers have a unique paradox:

1. We must abide by [existing convention](habits.md) to learn how to operate something new.
2. Simplicity is critical for people to easily, quickly [understand](understanding.md) information that helps them make [decisions](people-decisions.md).
3. For the convenience of the hardware and software engineer, *all* the complexities are laid out when they first design the object.

Those 3 elements combine to mean that computers *can't* please all the users unless there are *many* dropdown menus and extra hidden elements for more complex features.

In technology, the "slow" element is the user's understanding. More than anything else, the slowest part of any designed computer that isn't a [large-scale distributed system](computers-distsys.md) is the user.

As society keeps moving more toward browser/app-based computer interaction, proportionally fewer designers can create increasingly more misery for users. In high-stakes information transfer, such as large-scale banking and government websites, dark patterns and incompetence are almost guaranteed.

One of the most significant forms of dark pattern comes through default settings. Most users don't think to reconfigure settings, so they'll often automatically opt-in to whatever settings are provided, and *possibly* change them later.

### Addiction

Computers can magnify [addiction](addiction.md) more than just about anything else, mostly because a computer's design permits room for *many* dark patterns without the user's awareness:

- Forcing users to opt-out of things instead of letting them opt in.
- Email lists divided into many groups, which require the user to manually select *all* of them individually to fully remove their subscription.
- Swapping out UI elements to provoke users to make a mistaken selection.
- Hiding a [contractual agreement](people-contracts.md) behind a checkbox that has terms the user would certainly *not* agree to if they read it.
- A "download" button that's near the *actual* download button that typically contains [a virus](computers-cysec.md).
- Providing an inadequate experience *outside* the "paywall", then not permitting multiple payment options depending on the users' needs.

Shame is a [manipulation tactic](power-types.md) that tries to coerce users to do something. In software, this can be magnified because the software was *designed* that way, meaning it's scaled with the number of users:

- Confirm-shaming by making the "no" selection something terrible (e.g., "no, I hate outstanding content and freedom").
- Manipulinks that provoke people to select hyperlinks.
- Provoking users to accidentally select something.

Sometimes, in the interests of [marketing numbers](marketing.md), some UI decisions will be *terrible*:

- Email popups that confront the user 3 seconds into opening the website, since [A/B testing](engineering-design.md) showed it gained 10% more subscribers (while not really considering the lead-to-sales ratio).
- Moving around highly established design elements, since marketing [fashions](trends.md) dictated it was trendy and the key demographic would like it.

To get more money, online shopping has a few specific dark patterns:

- Hiding or subduing the presence of the free version to imply it's inferior or doesn't exist.
- Sneaking items to someone's shopping cart without their permission before they purchase an item.
- Copious [advertising](marketing.md) that promotes an unrelated product as part of the software experience.
- Making default selections that pre-select a price the user would likely not want to pay.

The incentive of a social media organization is for more people to use it more frequently, so some dark patterns are exclusive to them with the intent of people spending more time on the service or selecting advertisements:

- Requirements to share content to fully consume media (e.g., an article, free music).
- Adding [advertisements](marketing.md) in between users' content, with [algorithms](computers-programming-algorithms.md) that tailor those ads to be as associated as possible to what the user may want to have.
- The software requesting consent by the user to send messages to that user's contacts (typically email), then abusing that permission and messaging *everyone* in their contacts without their knowledge.
- Artificial notifications with no relevance that still provoke the [habit](habits.md) of checking and removing them.
- Sending fake requests to connect to the user as if they were initiated by another person, but the user's *reply* is the request to connect.
- Making the default message for connection requests sound desperate or urgent.

Except for casinos, [game development](computers-software-gamedev.md) contains some of the most addiction-inducing design possible. Games use goals and rewards to create an [operant conditioning chamber](https://en.wikipedia.org/wiki/Operant_conditioning_chamber) that leaves people *constantly* emulating the sense of reward that comes from [succeeding at life](success-1_why.md), but within their small ecosystem:

- Time the delay of rewards to be frequent enough to prevent boredom.
- Let off on rewards for a little bit to offset diminishing return and overload.
- Provide *just* enough incentive to keep playing the "free" game, while constantly [advertising](marketing.md) the paid game.
- Force scarcity over certain collectible items that would dramatically improve a player's performance.
- Create "loot boxes" to incentivize more purchasing with only a *chance* of granting an incentive.
- "Shaping" behavior to curate habits (e.g., spending free money at the beginning, starting a time-intensive task).
- Creating symbolic distance between the user and their money with a token/currency system.
- Using patterns to imply real people are using the game, with their status implying that they're more financially invested than the player.
- Constraining the progress a player is capable of performing on any given day without paying more money.
- If there's a social component to it, all the dark patterns specific to social media may apply as well.

At its most sinister, social media can provoke people to "doomscroll" (consume a large amount of bad news at once) to keep people constantly engaged with that platform.

## Additional reading

Delivering Impact

- [Juice](https://garden.bradwoods.io/notes/design/juice)

Colors

- [Building Your Color Palette](https://www.refactoringui.com/previews/building-your-color-palette)
- [Why are hyperlinks blue?](https://blog.mozilla.org/en/internet-culture/deep-dives/why-are-hyperlinks-blue/)
- [Contrast Rebellion](https://contrastrebellion.com/)

Specific Elements

- [You don't need a modal window](https://youdontneedamodalwindow.dev/)

Generating Addiction

- [Dark Patterns](https://neal.fun/dark-patterns/)
