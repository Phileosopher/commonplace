
# How robots work

Inside, a robot is mostly the same concept as any other computer-based design:

- It always requires an input with sensors that detect something that physically changes. This input is often a [camera](engineering-camera.md) or [microphone](computers-speakersmic.md), and often includes sensors along with it. If it's a simple-enough robot, it just needs sensors.
- The [operating system](computers-os.md) is relatively similar to any other computer, though interacting in the "real world" is *absurdly* complex compared to working strictly with raw information.
- The [processor](computers-cpu.md) eventually operates an output that physically does something. It may use a [screen](engineering-screen.md), but almost always uses a mechanical arm, and typically has lots of driver "middleware" to accommodate the extra mechanical hardware.

Externally, though, a robot is the ultimate "implementation" of a computer in the physical world. All other computer aspects are mostly confined to the realm of [the mind and ideas](values.md), but robots have the means to legitimately [*do* things](purpose.md).

The first industrial robot was Unimate, created in the 1950s by George Devol. It worked on an assembly line at a New Jersey General Motors plant and worked off drum [memory](computers-memory.md).

## Uses

Most robot parts are designed by borrowing directly from [nature](science.md) or existing [technology](technology.md).

Robots are designed for various uses, based on the roboticist's purposes. However, their uses are always far more limited (and often more effective) than a person employed in a relatively similar capacity.

The tasks a robot does best are highly precise, highly repetitive, or require hair-trigger reaction times. One system for controlling them is called computer numerical control (CNC), which specifies with precise mathematical formulas where the computer should go and what trajectory it should travel.

However, robots are *terrible* at some tasks:

- The input information sometimes requires further investigation to determine if it's worth acting on, but some inputs are too vague to articulate into logic.
- The output must be modulated according to an approximate estimation, but that estimate may be too vague to articulate into logic.
- Absolutely *anything* involving human interaction is a somewhat emotional experience, but more on that below.

Because of the excess of details and the *very* specific use cases of robotic machinery, the most prevalent use of robotics is in tedious factory and warehouse work. In fact, some warehouses are almost *entirely* automated. [Machine learning](computers-ai-ml.md) also won't likely expand their potential implementations much.

## Dumb machines

Computers are the world's fastest idiots, and robots demonstrate it by understanding specificities without grasping anything in the realm of general principle or intuition.

In many respects, a robot demonstrates how utterly stupid computers really are. They are effective at doing *exactly* what they're told, repetitively, but don't understand how to improvise or adapt.

One simple example of this idea is the seemingly easy task of laying bricks:

1. Lay mortar.
2. Place brick evenly on mortar.
3. Lay mortar on the side.
4. Scrape off excess mortar.
5. Repeat.

However, after a few trial runs programming a brick-laying robot, you'll notice it creating bad brickwork. [Debugging](computers-software-redesign.md) would show details necessary for a successful task:

- If any bricks slide from their spot, put them back in their place or adjust other bricks.
- Press firmly on the mortar to create cohesion, but not so firmly that it offsets the brick from the others too far.
- If there are any offset bricks, place future bricks at an aesthetically similar height to reflect them.
- Recognize impurities in the mortar and compensate the brick for it.

All of this would be resolved by the intuition of most people who have been laying bricks consistently for a few weeks.

As another example, imagine instructing someone to pick up pebbles from a flat surface and place them in a jar:

1. Pick up the pebbles you see over there (pointing finger).
2. Place the pebbles in that jar there (pointing finger).
3. Inform me when you're done.

While small children can do this easily, effectively programming a robot takes a lot of work:

1. Demarcate the grabbing zone, indicated as a specific range mapped out from captured [camera](engineering-camera.md) information.
2. Set an [algorithm](computers-programming-algorithms.md) that clarifies exactly what a pebble is, then create [instructions](computers-programming.md) to grab it, with each grabbing effort modulated with the camera data for every single pebble.
3. Move the arm to the jar, which must be *exactly* specified before the maneuver. There should be subroutines for whether the jar is missing, full, fell over, or broke.
4. Repeat 1-3 until all pebbles are in the jar, then clarify a stop sequence for the arm to rest.

Robot [AI](computers-ai.md) must also incorporate elements of kinesiology to manage complex tasks.

## Less dumb

One of the easiest workarounds for dumb robots is to have robots operated by people who remotely control them:

- When a location is too unsafe (e.g., near a bomb, drilling), remote-control robots have been popular for decades.
- Robotic hands and legs may soon become novel prosthetics technology for disabled people, assuming the artificial limb can accurately process nervous system signals.

Lately, [machine learning algorithms](computers-ai-ml.md) have dramatically improved the variability of the robot's instructions. They still have some trouble improvising while crossing difficult terrain, but can balance enough to ride skateboards or zip lines.

But, they're still relatively useless when completely unsupervised, and are still dumb enough for an errant cardboard box or towel to force them to stop.

The largest impediment to robotics advances, however, is in how absurdly difficult programming seemingly simple tasks becomes:

- The logic necessary to frame robotic instructions is conventional [software design](computers-software.md) work.
- The input is very fuzzy, and almost always analog.
- The output typically must fulfill very precise specifications.
- It's difficult to correctly account for all the "edge cases" you can't know while programming a robot.
- Even after many iterations, the work to [revise a robot's code](computers-software-redesign.md) is never technically done.

Dozens or hundreds of hours of expert programming can often be offset by a simple stroke of intuition.

## Fantasy robots

Beyond reality, robots have a tremendous draw in the world of fiction, and people like to imagine rather dramatic (and unrealistic) portrayals of what robots could do:

- *All* low-skill jobs replaced by robots, to the point that unions will fight their use in the workplace.
- Human-looking robots in customer service roles.
- Use cases in the sex industry.
- Robots becoming sentient and demanding [right](people-boundaries-why.md).

However, beyond the above concepts about how dumb they are at tasks, there are specific problems for many of the perceived domains:

- In the event of a poorly programmed robot, high-risk robotic implementations (e.g., [cars](computers-autos.md)) won't withstand human nature's tendency to [blame](people-rules.md) when people die, so it becomes a heavily [politicized](power.md) situation far more than simply upgraded [technology](technology.md).
- To make a human-like science fiction robot (e.g., Asimov's "I, Robot") would require adding the fields of psychology and sociology into all the *other* disciplines required for robots, meaning robots would have to first be ubiquitous everywhere to approach that challenge.
- Like realistic [game development](computers-software-gamedev.md), [widespread adoption](trends.md) of robots will always be suppressed by the [uncanny valley](https://en.wikipedia.org/wiki/Uncanny_valley):
  - Robots are more relatable as they become more human-like, and they're very relatable when they're precisely human-like.
  - *Right* before they're fully relatable, there's an odd point where their behaviors and mannerisms are terrifying and creepy.
  - At that point, a robot sabotages *all* human connection it may have gained, and will create a prolonged state of [unease](mind-feelings-fear.md) for the observer.

In particular, the uncanny valley can deter the public at large, since they're conditioned against it further through the genre of horror [stories](stories-storytellers.md) and spend more time among other humans than most roboticists do. Human expressions are vastly complex, with precise timings and exceptions for absolutely *everything*, and robots simply [can't compete with the intuition required](computers-ai.md) to accomplish something that could pass as human.

## Economics

Like all other [technology](technology.md), robots have a more profound effect than people who discredit them believe, but that profound effect happens over longer periods than the apologists would be quick to assert.

Despite the sillier trends attributable to robotics, there *have* been changes to society:

- Robots have very specific, purposed uses in realms like [horticulture](horticulture.md), factory work, military support, and navigating small corridors. Many of them are remote-controlled, but they serve as an agent of the human who uses them. This arrangement has been completely favorable.
- Skills *do* get replaced, which frees up people to do other things. People find [meaning](meaning.md) in work, and they do something else that can add [value](values.md), though older people surpassing about age 40 can be left behind from the change as the technology develops. This, however, happens slowly enough that it never destroys society in any collective sense.
- Lower-intelligence jobs (i.e., for people below an IQ of 85) have almost ceased to exist, since robots can do the job, and nobody has found a workable solution for this. It's reasonable to expect the most intelligent people in society to solve this issue, but that's [not how the world works](politics-perfectsociety.md).
