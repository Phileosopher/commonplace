
# What game developers do

In terms of raw talent and delivering results, game development requires [peak performance](computers-software-gamedev-peak.md) compared to almost anything else beyond [large-scale computing](computers-distsys.md).

## Storytelling

Most games, with the exception of some skill or puzzle games, are driven by a [story](stories.md).

When an interactive story is created correctly, the capabilities and uniqueness of immersion are immense. Almost every other medium (book, movie, radio drama, etc.) involves the audience viewing the experiences of that character, but game development is typically designed for a player to *be* a character.

There are, however, inherent limits to the range of usable stories within a game.

- Unless the game designer is particularly [creative](mind-creativity.md), there must be an enemy or set of enemies.
- Often, the enemies need to scale upward in perceived danger (e.g., start with unimportant enemies like rats at the beginning, then mundane ones, then grandiose gigantic enemies at the end).
- Most games involve one player character against *many* enemies, so there must be a reason why there are more enemies than the player character and why that character can successfully defeat them.

Compared to movie or book stories, most game stories are passable or awful, for many interconnected reasons:

1. [Writing high-quality stories](stories.md) requires a completely different skillset and talent than coding a game.
2. The most important part of a game is that it's playable: people are more inclined to buy and play a decent game with a terrible storyline than an unplayable game with an award-winning story.
3. A story that adapts as the player interacts with it requires extensive "dialogue trees" that cover all the forms of the story according to player's decisions, which is *much* more challenging than the one-story design of a movie.
4. The game's "ludonarrative" (difference between gameplay and story) has to stay small. To avoid dissonance, the story is forced to adapt to the gameplay, or the gameplay to the story (e.g., either a character can shrug off dozens of bullets and another one in a cutscene shouldn't change anything, or the character can only ever get hit by one or two bullets).
5. For the most part, players like to operate characters with superhuman abilities, so realistic stories are almost entirely off-limits without a high ludonarrative, which profoundly affects the experience.

Some independent game developers find ways to cleverly work with ludonarrative and have the story advance directly by player interaction (e.g., [Undertale](https://undertale.com/), [The Stanley Parable](https://www.stanleyparable.com/)), but most games use a few possible story/gameplay boilerplates:

1. There is no story, and it's designed strictly as a game (e.g., most games made before 1985). This one is literally timeless because it's an abstract existence.
2. The story is a general theme, but is almost completely unimportant beyond giving context for why the character is doing what they're doing (e.g., most games made between 1985-1998, most first-person shooters). While this is also timeless, it's also often lazy.
3. The linear progression of the game gives a story that could be made into a full-length movie or TV show, but is relatively unrelated to the game mechanics (e.g., point-and-click adventure games, most Japanese role-playing games). While many people may enjoy this type of game, it's a bit like forcing the viewers of a movie to pass skill games to keep watching scenes.
4. The game has a clear story that makes sense in context, but allows the player/character excessive liberty to take their time and explore everywhere (e.g., open-world games). This one has probably been explored to its fullest, and requires extensive development time to get correct.
5. The story of the game is actually many small stories triggered by player choices through the role of the character, often with a main story to advance the character through their experiences (e.g., many open-world role-playing games).

To advance the game's events, there's an invisible box in the game world called a "trigger volume" that starts an action when the user enters or exits it. For the savvy gamer, it becomes absurdly obvious by how an event happens suddenly, so setting events on a randomly generated delay of at least several seconds can add to the realism.

## Industry competition

Designing a good game requires [graphics development](engineering-graphics.md), both in 2D and 3D, as well as tons of [programming](computers-programming.md), but much of it is automated. It once required direct programming for just about everything, meaning it used to be *far* more challenging.

Today's game development has many drag-and-drop interfaces that turn game programming into far more of a dynamic moving visual art than simply a highly-involved domain of [software development](computers-software.md).

The simplicity of making games now has created a heavily saturated market of game developers, and the increased demand from all the people who want to play games has made it a heavily competitive domain. Developers are *constantly* stealing [intellectual property](legal-ip.md) from one another, and most of the ideas from AAA game developers are blatantly pulled from an indie developer who wouldn't be able to sue for copyright infringement. In the long-term, AAA games spend so much on mass [marketing](marketing.md) that they receive credit for new features or gameplay elements.

For each genre or style, game developers generally move through a [trend](trends.md) of motivations that drive them into the industry:

1. An independent developer [creatively](mind-creativity-how.md) designs their heartfelt art. The game is beautiful, but often unpolished from the fact that they're pioneering the entire thing and don't have the staff to clean it up.
2. Further developers polish that first creator's art with their own games. Those games are superior to play (since the idea was already made), and they refine the formula.
3. A big-budget game takes that formula into the mainstream. They use high-end graphics, often integrate it into a huge game world, and make the game represent more of a lifestyle than simply an experience.

Often, unscrupulous developers will borrow heavily from the [operant conditioning chamber](https://en.wikipedia.org/wiki/Operant_conditioning_chamber) (also called a "Skinner box" after the psychologist B.F. Skinner) first developed in 1898. The general pattern runs most casinos by forming addictions, and operates as follows:

1. Present a set of possible actions for the user, with rewards for some of those actions.
2. For the rewarded actions, modulate the chances of the actions occurring (e.g., 1 in 20 chance, every 15 times, etc).
3. Optionally, give the user a wide variety of possible rewards to provide the experience of making [choices](people-decisions.md).
4. Repeat indefinitely, changing out rewards occasionally, adding new types of rewards, and scaling them up before the user gets bored.
5. Branch out the rewards into tiers (e.g., an easily acquired type of coin and a rare type of coin).
6. Eventually, extend the experience into real-world [economics](economics.md) by making real-world currency necessary to advance the game.

Most of the time, game developers will [scale up](mgmt-7_changes.md) by having *other* developers make the games, contributing their accumulated experience in [ideas](mind-creativity-how.md)/[marketing](marketing.md)/[debugging](computers-software-redesign.md), then publishing with their brand attached to it and likely a royalty for sales.

## Trends

The electronic games industry has gone through many [trends](trends.md) that no longer exist, though they tend to pop up in weird places.

To change difficulty or configurations in the early 1980s, Atari games had simple toggle switches before starting a game that required [documentation](language-writing-documentation-cs.md) to decipher. By the 1990s, this difficulty switch eventually dissolved to an Easy/Medium/Hard selection when starting a game, and became an obscure feature hidden in the settings by the 2010s or simply nonexistent.

For some time in the mid-1990s, game installers took advantage of multimedia graphics, and started the [UX](engineering-design.md) into the game as soon as someone inserted a disc. The Command & Conquer: Red Alert game may have been the most interesting one, with [full animations of a rocket going through stages of loading for getting fired as the installation progressed](https://www.youtube.com/watch?v=Ri-VlJVxc-g).

In the mid-1990s, game CDs had a then-staggering memory capacity, so full-motion [video](engineering-graphics.md) could fit on it (though it was pretty lame at first). One form of game was called QuickTime events, named after Apple's then-new QuickTime protocol. The idea was that a full video would play, and the player would have to press a button when prompted. The pinnacle games of this were Dragon's Lair and Night Trap that were literally *nothing* but QuickTime events. They weren't particularly fun to play, but were novel enough to draw attention.

[Memory](computers-memory.md) constraints limited most games in the early and mid 1980s, so they all had some relatively similar features. Later games (especially after the 2010s) would imitate them for nostalgic/artistic effect:

- No discernible plot, or it was in the supplied [manual](language-writing-documentation-cs.md). Often, the goal of the game was a recorded high score, and maxing out the score (which was a feat of extreme skill or [exploitation](hacking.md)) would make the game crash.
- To pad out play time, the game was absurdly and unfairly difficult, even on the easiest setting.
- To help with [play-testing](computers-software-redesign.md), certain button combinations could give the player more lives, invincibility, swap out the sprites with other sprites, or skip ahead levels. These stayed in the game afterward and became known as cheat codes.

In the late-2000's, games spent the better part of a decade embellishing a very dull color palette of grays and browns, as well as getting a bit carried away on shadows. It was meant to capture a dark, grungy impression that would fit a post-apocalyptic environment, but it made everything unpleasant to look at and difficult to see.

Shortly after the grungy, disgusting trend, games pivoted hard into the other end: they added tons of "bloom" and "particle effects". This made the game very unpleasant to look at and difficult to see for the opposite, though this time it was easier to adjust visual settings to compensate for it.

Online games tend to use "leaderboards", online high score systems that track *everyone* who played the game. Since this number can be thousands or a few hundred thousand players, it's not particularly enjoyable for most players, and most leaderboards eventually devolve into [hackers](hacking.md) who exploited the game to achieve an inhumanly high score.

Since the late-2000's, most [graphics](engineering-graphics.md) trends have moved toward trying to reproduce the constraints and artifacts from video [cameras](engineering-camera.md). This trend hasn't stopped yet as of 2023, and has even gone as far as reproducing grit and water spots on the screen, which destroys the immersion of controlling a proxy character.

One trend that started around the time Fortnite became popular in the late-2010's is to release the multiplayer game for free, then charge for the single-player experience. This allows the developer to collect user data, both to [reconfigure](computers-software-redesign.md) the software to make it more addicting or to [sell the data outright](faang.md).

## Versioning

The ambitious nature of games makes its [software lifecycle](computers-software-versionctrl.md) more involved and complex than most non-game software.

Ever since the internet (and since online stores like Steam that also manage [updates](computers-software-redesign.md)), the game will often release in an unfinished state. At its simplest, the game will have glitches during gameplay, but many developers intentionally release games in so-called Early Access, which is effectively a [remarketed](marketing.md) "alpha" or "beta" build of the game.

For many [open-source](legal-ip-floss.md) games, they're *never* officially done because of the constant improvements added by independent developers.

Game developers will sometimes work on an Early Access game until they understand the best way to balance it, then release that game from Early Access a few months before selling almost the same game entirely as a full version. To hide this, they'll often change the theme (e.g., medieval, then space).

If a game becomes commercially successful, game developers can get more money relatively easily by creating expansions/addons/DLC (downloadable content):

- They typically only add new graphical assets or tweak small mechanics of the game, and some are simply designed to support the developers.
- However, some games may make the progression through the base game impossible without the DLC, and others can add *hundreds* of DLC.
- In fact, some games are entirely *[free](legal-ip-floss.md)*, with the expansions being most of the game's content.
