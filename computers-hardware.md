
# Computer hardware described

Anytime we build something as a condition-based cause-and-effect, we've made a "computer", though using household items usually never represents more than a few "bits" of memory, and it can't be used for a broad range of purposes.

If someone can physically observe or measure something, they can use a computer to magnify their [purposes](purpose.md). Technologists tend to [go too far](https://trendless.tech/trends/) and veer into making computers a [religion](religion.md), but it's irrefutably true that computers have and can improve any aspect of daily living that can [distilled into math](data.md).

All computers are simply electronic math machines, built up from [logic](logic.md) using two-based numbering and various forms of [programming](computers-programming.md) to accomplish specific purposes.

## History

Computers are much older than people realize. The oldest one we know of is the [Antikythera mechanism](https://en.wikipedia.org/wiki/Antikythera_mechanism), made ~150 BC, but adding machines have been around since the 1800s, with the most famous one being the [difference machine](https://en.wikipedia.org/wiki/Difference_engine).

Computers had been mechanical up until World War II, where they became electronic to keep pace with the need to [decrypt](encryption.md) German military messages. The first electronic computer was named Colossus, and was dramatically faster than the mechanical implementations that came before it.

The mathematician David Hilbert asked a simple question in 1928, "Is it possible to have a method/procedure that will clearly answer all math questions?" Alan Turing had a theory called the [Universal Turing machine](https://en.wikipedia.org/wiki/Universal_Turing_machine), which was designed to answer that question.

Now, most everyday computers use the [Von Neumann Architecture](https://en.wikipedia.org/wiki/Von_Neumann_architecture), based on the Universal Turing machine theory, and it was first implemented by Konrad Zuse's Z3 in 1941:

- Input - something goes into it
- Processing - it does [logical](logic.md), conditional stuff with that input
- Memory - it stores and retrieves information
- Output - it yields some final results from all that processing

Across the years, computer "abstractions" typically stay about the same while its "implementations" [trend](trends.md) insanely fast through various technologies:

- Right now, computers use electricity through silicon (0s and 1s represented as positively and negatively charged electricity).
- At one time, the 0s and 1s were electric charge held within vacuum tubes.
- Originally, computers were mechanical plates that read holes punched into old 35mm film stock.
- In decades, it may be something else, such as [quantum superstates](science-physics-quantum.md) or [DNA](computers-biological.md).

In fact, most of the standard computer needs were demonstrated already in [a 1968 demo by Doug Engelbart's team](https://www.youtube.com/watch?v=B6rKUf9DWRI).

## Design: Hardware

Since most computers run at the speed of electricity, the input-to-output in modern computers feels like it transfers information instantly. However, on the back end, computers are doing many types of calculations based on logical conditions which were configured in advance by engineers.

Technically, a computer could be assembled with a vast agglutination of wires and transistors, but that's messy. To make it simpler, a "printed circuit board" (PCB) will contain all the wires in pre-configured arrangements. Then, by using a standardized plug or solder point, just about anything can be easily attached to the PCB.

Around the core wiring/logic, the rest is largely protective. Padding, a housing, screws, and metal shielding protect it from getting broken, wet, picking up static or (in some cases) [interference from radio waves](engineering-radio.md). For higher-power needs (e.g., a PSU), they can fill the rest of the space with a brown epoxy-like substance called "potting" around the wires to provide protection from electric shock, vibration, or moisture.

In practice, this means a [hacker](hacking.md) can cobble together just about anything that's conductive and attach it to anything. With the exception of circuitry that's too small to work with (e.g., cell phones), most low-grade electronics are very accessible (such as the [Raspberry Pi](computers-embedded.md)).

The design of a general purpose computer has [specific elements as well for each component](computers-hardware-general.md).

## Design: Software

With the exception of [logic gate primitives](computers-alu.md), anything can be assembled as software *on* logic gates, and further hardware design simply speeds up how fast the computer will perform.

In simple terms, computers are vast collections of [logic gates](computers-alu.md) that build into ever-more complicated things. Combined together, it makes working with them extremely trivial.

Designers are *constantly* improving computers, but the gains in improvement are starting to become incremental (similar to the [autos](autos.md) that came before it). Even though they can become much faster, they're not really adding much to the experience anymore for a typical user, and even a low-tier desktop computer is more than enough for most non-[gaming](computers-software-gamedev.md)/design computer needs until [VR headsets](computers-vr.md) or [AI](computers-ai.md) become a popular trend to everyday people.

## Input

Inputs can be pretty much anything you can stick a sensor to and measure. That sensor must then do one of two things:

1. Activate something after reaching certain thresholds (aka "analog signal")
2. Convert that information into a string of 0s and 1s (aka "digital signal")

Conventionally, we're used to keyboards and mice, but pretty much *anything* can be an input:

- Barcode readers
- Touch pads
- Body gestures
- Speaking
- Heat or moisture

## Memory

The [memory](computers-memory.md) holds "programs" that tell the processor what to do.

It also holds the results of that processing for further use.

If that information is moving to the processor faster than it can process (which *very* often happens) then it'll offload the information in its memory.

This memory takes a wide variety of forms, from USB sticks to hard drives to the memory built into the CPU chip. Each type of memory has pros and cons.

The memory to store processed information has gone through *many* iterations of implementation. Vinyl records, magnetic tape, compact discs, magnetic disk drives, and solid-state memory are all examples of long-term storage.

## Processing

The [processor](computers-cpu.md) is where the magic happens. By using a set of *very* clear rules, a processor can convert the input data in endless ways.

A processor cycles the information between a control unit and [math/logic unit](computers-alu.md).

## Output

In effect, output is pretty much anywhere where a processor sends information:

- It could send it to a [computer screen](engineering-screen.md) or a [printer](engineering-printers.md), which is what most people think of.
- It may output to [audio](computers-speakersmic.md) or activate lights.
- It might store it to the hard drive for long-term storage between power cycles.
- It may send the information [across an electrical cable](networks-cs.md) to be *another* computer's input.

## Other Computers

There are a *lot* of other computers beyond your average household computer. Technically, you *can* do anything with a general-purpose computer, but it's often far more inefficient than using that special-use computer.

Since computers have gotten so cheap, so easy to work with, and so powerful, most manufacturers stick them in *everything* that isn't disposable or edible.

You want a remote control? Computer. Maybe you want to entertain your ~~drool factory~~ one-year-old? Computer. How about showing what song is playing? Computer. You want to track the time? Clearly, you'll want a complex assembly of cogs, sprockets, and springs.

If you have a modern office workspace, you may be surprised how many separate processors are in it:

1. The CPU on the motherboard, naturally, though it may have a split processing/graphics setup with an APU.
2. If you have a graphics card or sound card, it has a CPU on it, though graphics cards call it a GPU.
3. Inside the computer, it has specific-function chips called "device controllers" that regulate peripherals.
4. If you have a printer/scanner, it typically has its own computer to regulate its jobs.
5. Most fancier computer monitors have small processors that regulate information or tweak visual settings.
6. Computer mice and most keyboards have small processors inside them that convert the signals into digital information before sending.
7. Modems, which are usually built right onto the motherboard, are computers designed to send and receive information.
8. Network routers and adapters, all along the string between computers with screens, are each their own computer. These computers are most of the internet.

### Supercomputers

By sticking multiple parts together in a big metal box, such as hard drives or CPUs, they can all work together as if they're all one "supercomputer". This is how big companies run their computers, since they need a *lot* of computing power.

The problem with big supercomputers, though, is that there are a *lot* more parts, so more things can break:

- To make sure the computer is *always* on, they need redundant power supplies.
- To ensure the data is safe, the computers are typically on a [RAID array](computers-memory.md).
- Several separate processors run inside the device at once, just in case one goes out.

### Lamecomputers

On the *extremely* cheap end, some general-purpose computers like the [Raspberry Pi and Arduino](computers-embedded.md) are designed as "single board computers". They're meant to be so affordable that you can give it to children (~$40).

In fact, if you're tenacious enough, you can even [build a computer in your own garage](http://sam.zeloof.xyz/first-ic/).

Also, like stated above, many computers can be specific-purpose. NAS (network attached storage), for example, is just a normal computer that does nothing but send information back-and-forth to other computers on a [network](networks-cs.md). You can even make one with a [Raspberry Pi](computers-embedded.md)!

Computers are so fast now that these computers can pretty much do anything the average person could imagine using it for, so there are a *ton* of projects available for them. These can range from automatic pet feeders to home security systems to running websites!

## Maintenance

Computers require consistent maintenance. This pretty much guarantees job security for everyone working with computers, even with automation.

### Dust

The biggest enemy of computers is dust, for several reasons:

1. Dust creates a blanket-like effect on the parts, which keeps heat in. Left unchecked, it can melt the computer, *especially* the [CPU](computers-cpu.md).
2. Static electricity builds up in dust, which can short-circuit the parts. Since most things in a computer are electrical, this is bad.

Thus, computers need regular dusting. Once a month is ideal for home users, but don't let it go for more than 6-12 months, *especially* if you're in a dusty area.

When dusting, an air compressor works much better than canned air, since canned air has chemicals that can damage the circuitry.

### Updates

Computers *always* need updating. It can be the instructions for input/output devices ("drivers"), instructions for how the system that keeps it operating ("[operating system](computers-os.md)") or specific instructions for software.

There's often downtime during updates, which isn't *that* big a deal if you're browsing the web, but becomes an issue if you run a business.

Also, updates might not work right. Always, always, *always* play it safe:

1. Keep a copy of everything ("backup") that you can restore everything from.
2. Avoid running more stuff than you have to while it's updating, *especially* if it's a BIOS update. Call of Duty can wait.
3. Only run the updates when you don't plan to use your computer much. Overnight on weekends is usually best because you get a few days if you really screwed up.

The reason it becomes an issue is because sometimes two "processes" on the operating system can use the exact same "file" and screw up what they're both doing with it.

### Upgrades

Of course, sometimes that computer needs new parts. Other times, it's been long enough that it's a cheaper *and* more economical solution to simply buy a whole new computer.

Typically, upgrading computers requires understanding the specific marketing of each OEM ("original equipment manufacturer"). Each of them has their own compatibility requirements, and often make agreements with other OEMs about how to interconnect their parts.

This interconnected nature means that if a part is old enough, other OEMs might stop designing their hardware to connect to it.

### Quality

Not all computers are the same. Consumer-grade technology is relatively flimsy, with the "planned obsolescence" of at least one major component in it set for about a month after the extended warranty expires, presuming home use (i.e., no more than 2-6 hours of moderate use a day). Commercial-grade technology, on the other hand, is designed to last for about the same amount of time, but under heavy use 24 hours a day. This is a portion of why [enterprise-grade computers](computers-distsys-enterprise.md) are far more expensive.

The *actual* quality of any given computer is a competing, advanced calculation of [economics](economics.md) and [technological development](technology.md). When something has become [a hot trend](trends.md), manufacturers will spend more effort and money on developing that component, up until people stop caring and the trend dies. As boring technology starts becoming a commodity instead of a novelty, a [Big Tech](faang.md) company will pick up most operations in that space (and not innovate much more), all the way until something better comes along.

To that end, buying the *best* computer is nearly impossible because you're paying for an experimental technology (which may break on you) or a boring technology (which won't be as fast).

### Complicated

Computers will always be a big career-maker as long as the following chain of events happens:

1. Computers get used for more and more things.
2. Computers need increasingly more complicated instructions to deal with the many varieties of things they can get used for.
3. Complicated instructions create horrifically complex situations.
4. More elaborate systems mean more links in the chain that can break.
5. If anything breaks, it's so complicated that replacing it isn't very easy.
6. Only people who are patient enough to slog through encyclopedias of documentation can work with complicated computer issues.

In other words, if you're patient with computers, you have job security.

$$ Further Reading

[Effects of Grill Patterns on Fan Performance/Noise](https://www.pugetsystems.com/labs/articles/Effects-of-Grill-Patterns-on-Fan-Performance-Noise-107/)
