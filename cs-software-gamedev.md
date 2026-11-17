
# What game developers do

In terms of raw talent and delivering results, game development requires [peak performance](cs-software-gamedev-peak.md) compared to almost anything else beyond [large-scale computing](cs-distsys.md).

## Storytelling

Except for some very small games, most games have a [story](stories-why.md).

When an interactive story is created correctly, the capabilities and uniqueness of immersion are immense. Almost every other medium (book, movie, radio drama, etc.) involves the audience viewing the experiences of that character, but game development is typically designed for a player to *be* a character.

There are, however, inherent limits to the range of usable stories within a game.

- Unless the game designer is particularly [creative](mind-creativity.md), there must be an enemy or set of enemies.
- Often, the enemies need to scale upward in perceived danger (e.g., start with unimportant enemies like rats at the beginning, then mundane ones, then grandiose gigantic enemies at the end).
- Most games involve one player character against *many* enemies, so there must be a reason why there are more enemies than the player character and why that character can successfully defeat them.

Compared to movie or book stories, most game stories are passable or awful, for many interconnected reasons:

1. [Writing high-quality stories](stories-why.md) requires a completely different skillset and talent than coding a game.
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

Since game development is a lot of work, many developers decide to insert easter eggs into the game, which are simple references to the developer or something outside the game's in-world narrative.

- The original easter eggs were an act of corporate rebellion, back when developers weren't given credit for the games they developed.

## Appeal

A game has to be [fun](fun.md), but this "fun" represents three very specific domains:

1. Context (i.e., [story](stories-why.md))
2. Challenge
3. Catharsis (i.e., gratification)

All three are necessary, but each dimension can be weaker if another dimension makes up for it.

- A simple arcade-style game usually has barely any story, but has *extremely* well-tuned controls and high-quality visual feedback to constantly [communicate to the player](engineering-design.md).
- A visual novel isn't challenging at all, but holds together with a high-quality story and gratuitous amounts of [visual art](art-media-visual.md).
- Many experimental and independent games are in no way gratifying, but their story's context and the challenge they provide evokes a contradictory experience that can give players [meaning](meaning.md).

[Storytelling](stories-form.md) in games is similar to any other medium, with a few key differences:

1. The stories have to pace themselves at the speed of the game, meaning it's a variable timing that's dependent on player [choice](mind-decisions.md).
2. There is a higher chance that players won't complete the stories than other media due to time constraints or frustration.

With respect to challenge, players must feel the game is being [fair](morality-justice.md) or they'll give up:

1. The enemies must come in small groups (3-4 usually), and never overwhelming numbers.
2. Every enemy uses the same attack pattern every time, and they are starkly demarcated from each other for quick visual recognition.
3. The environment's layout adjusts to add more difficulty, but never add random behaviors from enemies.
4. The final enemy in each wave is slightly easier than the rest, which leaves players with a softer impression of the game's difficulty.

In other words, a game's challenge has to make the player feel like they're improving at the game as they play it.

Catharsis has, in many ways, become the fallback for many games.

- At its core, the behavior reproduces the same psychology that corresponds to casino interaction (i.e., making [addicts](addiction.md)).
  - There are severe [ethical](morality.md) problems with casino mechanics, especially when they monetize the approach.
- Unfortunately, many mainstream games are nothing but raw catharsis, so they can be exciting and stimulating, but generally don't give any [meaning](meaning.md) following the game.
  - [Stories](stories-why.md) give an implicit meaning by giving the player more guidance on [how they ought to live](people-goodlife.md).
  - Challenge gives the players meaning through the development of a specific, not-that-useful [skillset](jobs-specialization.md), similar to [sports](fun-sports.md) without the [exercise](body-exercise.md).

## Industry competition

Designing a good game requires [graphics development](engineering-graphics.md), both in 2D and 3D, as well as tons of [programming](cs-langs.md), but much of it is automated. It once required direct programming for just about everything, meaning it used to be *far* more challenging.

Today's game development has many drag-and-drop interfaces that turn game programming into far more of a dynamic moving visual art than simply a highly-involved domain of [software development](cs-software.md).

The simplicity of making games now has created a heavily saturated market of game developers, and the increased demand from all the people who want to play games has made it a heavily competitive domain.

- Developers are *constantly* stealing [intellectual property](legal-ip.md) from one another, and most of the ideas from AAA game developers are blatantly pulled from an indie developer who wouldn't be able to sue for copyright infringement.
- In the long-term, AAA games spend so much on mass [marketing](marketing.md) that they receive credit for new features or gameplay elements.

For each genre or style, game developers generally move through a [trend](people-trends.md) of motivations that drive them into the industry:

1. An independent developer [creatively](mind-creativity-how.md) designs their heartfelt art. The game is beautiful, but often unpolished from the fact that they're pioneering the entire thing and don't have the staff to clean it up.
2. Further developers polish that first creator's art with their own games. Those games are superior to play (since the idea was already made), and they refine the formula.
3. A big-budget game takes that formula into the mainstream. They use high-end graphics, often integrate it into a huge game world, and make the game represent more of a lifestyle than simply an experience.

Often, unscrupulous developers will borrow heavily from the [operant conditioning chamber](https://en.wikipedia.org/wiki/Operant_conditioning_chamber) (also called a "Skinner box" after the psychologist B.F. Skinner) first developed in 1898. The general pattern runs most casinos by forming addictions, and operates as follows:

1. Present a set of possible actions for the user, with rewards for some of those actions.
2. For the rewarded actions, modulate the chances of the actions occurring (e.g., 1 in 20 chance, every 15 times, etc.).
3. Optionally, give the user a wide variety of possible rewards to provide the experience of making [choices](mind-decisions.md).
4. Repeat indefinitely, changing out rewards occasionally, adding new types of rewards, and scaling them up before the user gets bored.
5. Branch out the rewards into tiers (e.g., an easily acquired type of coin and a rare type of coin).
6. Eventually, extend the experience into real-world [economics](money-economics.md) by making real-world currency necessary to advance the game.

Most of the time, game developers will [scale up](mgmt-7_changes.md) by having *other* developers make the games, contributing their accumulated experience in [ideas](mind-creativity-how.md)/[marketing](marketing.md)/[debugging](cs-software-redesign.md), then publishing with their brand attached to it and likely a royalty for sales.

## Trends

The electronic games industry has gone through many [trends](people-trends.md) that no longer exist, though they tend to pop up in weird places.

To change difficulty or configurations in the early 1980s, Atari games had simple toggle switches before starting a game that required [documentation](language-writing-documentation-cs.md) to decipher. By the 1990s, this difficulty switch eventually dissolved to an Easy/Medium/Hard selection when starting a game, and became an obscure feature hidden in the settings by the 2010s or simply nonexistent.

For some time in the mid-1990s, game installers took advantage of multimedia graphics, and started the [UX](engineering-design.md) into the game as soon as someone inserted a disc. The Command & Conquer: Red Alert game may have been the most interesting one, with [full animations of a rocket going through stages of loading for getting fired as the installation progressed](https://www.youtube.com/watch?v=Ri-VlJVxc-g).

In the mid-1990s, game CDs had a then-staggering memory capacity, so full-motion [video](engineering-graphics.md) could fit on it (though it was pretty lame at first). One form of game was called QuickTime events, named after Apple's then-new QuickTime protocol. The idea was that a full video would play, and the player would have to press a button when prompted. The pinnacle games of this were Dragon's Lair and Night Trap that were literally *nothing* but QuickTime events. They weren't particularly fun to play, but were novel enough to draw attention.

As [networks](cs-networks.md) developed more bandwidth capacity, many gamers would combine multiple game consoles or computers to create LAN parties, where upwards of 16 people would play mostly first-person shooter games like Halo or Counterstrike together.

[Memory](cs-memory.md) constraints limited most games in the early and mid 1980s, so they all had some relatively similar features. Later games (especially after the 2010s) would imitate them for nostalgic/artistic effect:

- No discernible plot, or it was in the supplied [manual](language-writing-documentation-cs.md). Often, the goal of the game was a recorded high score, and maxing out the score (which was a feat of extreme skill or [exploitation](mind-creativity-hacking.md)) would make the game crash.
- To pad out play time, the game was absurdly and unfairly difficult, even on the easiest setting.
- To help with [play-testing](cs-software-redesign.md), certain button combinations could give the player more lives, invincibility, swap out the sprites with other sprites, or skip ahead levels. These stayed in the game afterward and became known as cheat codes.

In the late-2000's, games spent the better part of a decade embellishing a very dull color palette of grays and browns, as well as getting a bit carried away on shadows. It was meant to capture a dark, grungy impression that would fit a post-apocalyptic environment, but it made everything unpleasant to look at and difficult to see.

Shortly after the grungy, disgusting trend, games pivoted hard into the other end: they added tons of "bloom" and "particle effects". This made the game very unpleasant to look at and difficult to see for the opposite, though this time it was easier to adjust visual settings to compensate for it.

Online games tend to use "leaderboards", online high score systems that track *everyone* who played the game. Since this number can be thousands or a few hundred thousand players, it's not particularly enjoyable for most players, and most leaderboards eventually devolve into [hackers](mind-creativity-hacking.md) who exploited the game to achieve an inhumanly high score.

Since the late-2000's, most [graphics](engineering-graphics.md) trends have moved toward trying to reproduce the constraints and artifacts from video [cameras](engineering-camera.md). This trend hasn't stopped yet as of 2023, and has even gone as far as reproducing grit and water spots on the screen, which destroys the immersion of controlling a proxy character.

One trend that started around the time Fortnite became popular in the late-2010's is to release the multiplayer game for free, then charge for the single-player experience. This allows the developer to collect user data, both to [reconfigure](cs-software-redesign.md) the software to make it more addicting or to [sell the data outright](cs-bigtech.md).

There's a general economic gap in the industry that has arisen.

- Many, *many* games are released for free after a very short game jam. They're often well-received, have lots of [bugs](cs-software-redesign.md), and will only capture the player's attention for less than a half hour.
- Of those games, some people who get enough positive attention will quit their job, work with other developers, and devote their life to that game for ~3 years.
- The middle ground is missing, where 1-2 developers can create a game over the course of a few months and see if they can turn a profit before making something more substantial.
- This trend seems to be the standard due to a confluence of factors, so it will likely persist for decades.
- One consequence of this trend is that, beyond free user-generated mods to AAA games, there's a very small pipeline between [creative](mind-creativity.md) ideas in independent games versus using their implementation in AAA games.

## Social effects

The increased realism of games creates quite a few social consequences.

Games have a soft correlation with better cognitive performance.

- Veterans with PTSD have had their symptoms alleviated by playing Tetris.
- Depending on the game mechanics, children have improved cognitive performance in various tasks.

There is an unclear [political](politics-conservativeliberal.md) consequence from how little we know about the impact of video game violence.

- On one side, a video game is reproducing real-life circumstances that can easily desensitize gamers to violence they'd *never* otherwise commit (e.g., Grand Theft Auto series).
- On the other, video game [AI](cs-ai.md) is so inaccurate in most contexts to real life that the player very quickly recognizes the human-looking non-player characters are simply computer code.
- However, there are reported instances of game developers diagnosed with PTSD due to a game's violence.

Online MMO games suffer absolutely everything that exist in association with [the human condition](humanity-universals.md).

- There was a glitch in World of Warcraft in 2005 called the Corrupted Blood incident that actually reproduced real-life pandemic behaviors.
- Games like Roblox are built to become [addictive](addiction.md) for children, but the lack of parental supervision mean child sex traffickers also inhabit that space.

However, there are also other unaddressed impacts that come from excessive gameplay:

- Some games promote excessively losing, which can create a culture of people who can accept loss more than they should.
- Horror games can easily merge into our [imagination](mind-imagination.md) and advance delusions about reality.
- The relatively easier challenges of most games can create delusions about creating [results](results.md), specifically in underestimating how much effort things take to do.
- The low-context dialogue present in most games can create an impaired [ability to socialize](people-friends.md), and at greater levels [replace friends altogether with awful alternatives](https://gainedin.site/diet-social).

## Versioning

The ambitious nature of games makes its [software lifecycle](cs-software-versionctrl.md) more involved and complex than most non-game software.

Ever since the internet (and since online stores like Steam that also manage [updates](cs-software-redesign.md)), the game will often release in an unfinished state. At its simplest, the game will have glitches during gameplay, but many developers intentionally release games in so-called Early Access, which is effectively a [remarketed](marketing.md) "alpha" or "beta" build of the game.

For many [open-source](legal-ip-floss.md) games, they're *never* officially done because of the constant improvements added by independent developers.

Game developers will sometimes work on an Early Access game until they understand the best way to balance it, then release that game from Early Access a few months before selling almost the same game entirely as a full version.

- To hide this, they'll often change the theme (e.g., medieval, then space).

If a game becomes commercially successful, game developers can get more money relatively easily by creating expansions/addons/DLC (downloadable content):

- They typically only add new graphical assets or tweak small mechanics of the game, and some are simply designed to support the developers.
- However, some games may make the progression through the base game impossible without the DLC, and others can add *hundreds* of DLC.
- In fact, some games are entirely *[free](legal-ip-floss.md)*, with the expansions being most of the game's content.

Sadly, publishers often don't maintain games indefinitely after they're not making money from them, and they'll frequently [end-of-life](cs-software-versionctrl.md) a game that has a devoted fanbase.

- Legally, since the game *is* the [intellectual property](legal-ip.md) of the publisher, they have every right to do this, even if it's [unethical](morality.md).
- This can be especially egregious if the game was extremely popular or the publisher wants them to pay for a newer version of the game.
- In this context, many [hackers](mind-creativity-hacking.md) will break open the code and release it for everyone to continue playing it if it's popular enough.
- At this point, [87% of classic video games are now completely unavailable](https://gamehistory.org/87percent/).
