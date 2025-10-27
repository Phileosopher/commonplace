
# Peak requirements for game development

## Peak development

Game development is all effective aspects of [software development](computers-software.md), but requires *many* [specialized](jobs-specialization.md) roles that would otherwise be optional or unnecessary in most other software domains:

- Direct game designers, which can branch out into gameplay, levels, monetization, [usability/UI](engineering-design.md), cinematic cutscenes, [narrative](stories.md), [writing](language-writing.md), and [missions/quests](purpose.md).
- Programming roles that branch out into all standard software development, including [graphics](engineering-graphics.md), [animation](art.md), [AI](computers-ai.md), [servers](computers-distsys.md), physics, pipeline engineers, build engineers, testing, visual effects, databases, [language-specific](computers-languages.md) roles, and roles specific to game engines.
- A wide variety of [art](art.md) roles including 2D and 3D versions of environments, animation, rigging, motion capture, textures, lighting, 2D characters, 2D concept art, 3D camera, storyboarding, and both UI *and* UX.
- [Quality assurance](computers-software-redesign.md) roles, especially play testing.
- All aspects of [management](mgmt-1_why.md), for *everyone*, with subdivisions for product management and studio administration.
- Community support roles, such as [customer support](people-customerservice.md).

To that end, most game development takes a *lot* of money and time, often by a factor of four relative to most high-budget films.

The draw for game developers is a confluence of factors:

1. The challenge of the above
2. The opportunity to make a lucrative career at something they love
3. A blind [addiction](addiction-substances.md) to games

To that end, it has the same workplace abuse and political issues that encompass the [financial industry](money-investing.md).

### Peak performance

Gaming computers are the most expensive consumer-grade computers on the market, and why they tend to push hardware to their limits. This is because game development is the pinnacle of high-quality software development, for several reasons:

1. The [visual elements](engineering-design.md) are usually far more [vast](engineering-graphics.md), and the designers need to worry about both animation *and* static elements.
2. The [audio](computers-speakersmic.md) must be synchronized to the visual experience, so it has to be correctly designed, from the sound effects to the soundtrack.
3. Games require *immediate* feedback from the input peripherals (such as the [keyboard](computers-keyboard.md) or [mouse](computers-mouse.md), and now [VR](computers-vr.md)). While people can endure a 1-second delay in many other programs, 0.1 seconds is enough to make a janky game.
4. For many games, you need an elaborate [mathematical framework](computers-programming-algorithms.md) to keep all the visual and audio elements working in tandem. This is *much* more than most other programs.
5. Across the internet, the demand for rapid-response [networking](networks-cs.md) in many genres is a perpetual need, for *both* player input and [visual output](engineering-screen.md).
6. In multiplayer games that need computer players (e.g., a 2v2 game with 3 humans), the [AI](computers-ai.md) has to have enough logic to permit the player to feel like the "bot" is human-like.
7. [Graphics](engineering-graphics.md) technology is often driven by large-scale game developers, who build incredibly elaborate designs for their games that need ever-increasing [processing power](computers-cpu.md). This ranges from the character designs all the way to expansive and beautiful "skyboxes" and long-distance rendering to recreate extremely large worlds.

This means you need *lots* of processing power to make sure it stays above 30-60 FPS (frames per second). Most modern games require a dedicated GPU (i.e., a CPU that only processes graphics) strictly for this reason.

At one time, producing games became absurdly complicated because of the limits in graphics processors.

- e.g., it's relatively easy to set up a static display (e.g., player score and health) overlaid over a scrolling portion (where the game was happening) frame-by-frame by rendering the scrolling part and then rendering the static part on top of it.
- However, in the 1990's Nintendo Entertainment System, the developers had to [hack](hacking.md) the CPU to halt drawing one portion with a predetermined sound that forced the hardware to stop, then used the hardware's "collision detection" bit to draw the other part.
- Even through to today, vintage [game emulators](computers-distsys-vm.md) are notoriously difficult to build because the software must reproduce the individual clock cycles and constraints of the original hardware.

### Netcode

Across a network, games have extremely stringent requirements for input, and heavy requirements for output. From frame to frame across a [network](networks-cs.md), the game must match on *both* computers.

Online games are typically designed as "deterministic", which means two instances of the same program will create *precisely* the same outputs with the same inputs. Even random numbers can be [algorithmically](computers-programming-algorithms.md) derived deterministically. This gives the added convenience that a replay of a game can simply be the inputs mapped to timing inside a game, but also allows other games to reconstruct a match even with [network](networks-cs.md) latency.

Instead of using a server that holds the information, games on computers can synchronize with each other with "lockstep networking", where they can communicate back-and-forth about the state of the game. By bypassing a central server for both computers, it can theoretically be a quicker network speed. One side advantage of lockstep networking is that hacks that mess with the timing of the game (such as a character "sprite" that goes faster) will cause the game to desynchronize, which prevents cheating.

But, networks are still slow, relatively speaking. So, there's still a delay in the "netcode". There are two ways to deal with this.

Delay-based netcode will intentionally slow down the input from registering on the frame it was used. Instead, it'll update a few frames later (each frame represents [~1/60 of a second](engineering-screen.md)). While a few people well-trained in games may notice the delay, clever game design and the delay staying consistent make delay-based netcode work fine. Unfortunately, networks are rarely consistent: any slowdown in the network will slow the game down, even with plenty of tricks that predict network behavior, and physical distance will have a profound impact on gameplay.

Rollback netcode is designed to uniquely deal with network uncertainty:

1. When a network drops the information, the computer will predict the behavior of that input (likely by holding down the same button as before).
2. When there's a solid connection again, the computers will send a frame-by-frame retroactive input mapping for their respective players.
3. Both games will update the data of the previous frames to synchronize with each other, then deliver the same consequences.
4. This will mean certain portions of the game may move around a tiny bit, but not enough to significantly alter the gameplay, and precise button timings are preserved.

A rough and dirty example will help the concept. First, a human conversation with delay-based netcode:

- Aaron: Hello, I heard you're from Wales, right?
- Bob: ...
- Aaron: ...
- Bob: No, I'm from Scotland. And where are you from?
- Aaron: I'm from Pakistan.

And, a rollback netcode conversation:

- Aaron: Hello, I heard you're from Wales, right?
- Bob: ...
- Aaron: I had a friend in Wales. Maybe you know him?
- Bob: No, I'm from Scotland. And where are you from?
- Aaron: I'm from Pakistan.

## Peak psychology

Games are a unique medium compared to books, audio, and movies because it's the only medium that directly interacts *back* with the user's interaction.

- The only exception to this is specific game genres (e.g., visual novels, some [VR experiences](computers-vr.md)), but advancing the interface doesn't define as a "game" (i.e., there should be a capacity for [making decisions](people-decisions.md)).

Game [UX](engineering-design.md) should be non-intrusive, where the user will feel or observe what they should do *without* explicit instruction. To avoid text boxes with instructions or written signage, there are several tools to guide the player:

1. Place desirable items to direct the player where they should go (e.g., a healing potion located near the next important passageway).
2. Use "non-diegetic" lighting to indicate what the player should interact with (e.g., a lever has a flashing effect on it).
3. Train the user by designing specific, new enemies that are most easily taken down by the actions or abilities they should learn to use.

Most games have an initial setup, followed by a "gameplay loop", up until the end.

- A gameplay loop is a hot-and-cold cycle through a developed [habitual](habits.md) routine.
- Gameplay loops can be classified as primary, secondary, and tertiary:
  1. Primary gameplay loops are iterated across seconds (e.g., pressing button combinations).
  2. Secondary gameplay loops iterate across minutes (e.g., completing a level).
  3. Tertiary gameplay loops iterate across longer stretches of time (e.g., complete enough levels to get a high score).
- Every loop *must* be a struggle for the player, but not so much that they feel overwhelmed.
- Each loop should deliver a significant payout for the player (e.g., extra points, bonus health, visually stimulating WIN screen).

The contrast in intensity between the action and relaxing modes of a gameplay loop determine how exciting and thrilling the player will feel.

- e.g., peppy overworld music that transitions to peppy level music maintains a general sensation throughout the game, while calm menu music before high-intensity level music makes each level feel like a rush before the menu screen feels comparatively calmer.

Every game developer must balance three major psychological balances throughout the player's experience:

1. The game has to be fun, which is balancing between enjoyable familiar things and novelty.
2. The game must be challenging enough: too much and the player will "ragequit", too little and the player will be bored. The challenge must come from the player's *interaction* with the game, not from [software errors](computers-software-redesign.md) or arbitrary game design that stretches out time.
3. The game must make the person curious, or they won't want to keep playing. This sometimes come from the game's [story](stories.md), but more often comes from the functionality of what the player controls and the possibilities that it opens (e.g., seeing if they can jump across a normally impassable large chasm using a weapon that launches them backward).

The most reliable way to keep a player engaged with the game is to give them a clear way to overcome the challenge, as well as potentially helping them to overcome it more easily:

- Give them back health if they react after getting hit.
- Give them the exact same level over and over to make it easy to memorize actions.
- Have mid-level checkpoints that let them restart later in the level when they fail.
- Give hints (or the chance for a hint) after they've failed a few times.

The challenges the player experiences from the game define what the player learns and, ultimately, their experience when they leave the game.

Skilled/smart players want a difficult and unforgiving experience, but newer/unskilled players want simpler and forgiving challenges. The best way to accommodate both is to create at least a two-tiered way to win:

- The easy way involves merely getting through the level and rewards more levels, all the way to the final level.
- The hard way requires tons of dedication and skill.
- The extra challenge should *never* follow the "critical path", and the player should receive silly things like hats or "easter eggs" that don't make future challenges easier.
  - The easiest implementation of this is a star or rating system.
- However, no game can please everyone. It'll be too hard for some people, or too easy for others.

In online games that have in-game currency and permit players to trade with each other, the emergent nature of [economic bartering](economics.md) arises.

- If the developers only permit cash to flow into the system (i.e., through natural gameplay) but don't allow it to flow *out* of the system, the bartering will slowly yield a natural inflation.
- To that end, most online game developers have to deal with rudimentary economic policy concepts.
