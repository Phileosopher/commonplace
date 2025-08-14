
# The motherboard summarized

One of the most complex-looking parts of a computer's internals is its "motherboard".

Ironically, while motherboards often look intimidating, they're one of the *least* complex parts of a computer. In effect, they're simply a "printed circuit board" (PCB) with "ports" for:

- A [CPU](computers-cpu.md)
- Onboard [memory](mind-memory.md) (as RAM)
- An input (typically for at least a [keyboard](computers-keyboard.md) or other computer data)
- An output (typically via a [screen](computers-screen.md)).

In most typical computers, there are other built-in features:

- Long-term storage (as a hard drive)
- A [graphics](graphics.md) card port
- [Network](networks.md) ports (including wireless).

Without a motherboard, everything in a [computer](computers.md) would be a gigantic tangle of wires. So, while the motherboard isn't particularly complex, it's critical to keep everything [organized](organization.md) and regulate airflow for heat management.

## Failing

Typically, the extreme complexity of a motherboard means it's the [first thing to fail](networks.md).

Thankfully, it's also often one of the least expensive parts of a computer.

## Clock

Beyond keeping everything organized, motherboards tend to come with a built-in "[clock](datetime.md)" that oscillates a 0-1-0-1 signal. It's a bit like a ticking clock, with each 1 as a cycle. *All* the sequential logic circuits get this signal, and the clock runs at about 200,000,000 times a second (200 MHz).

The clock is typically made of quartz, since quartz resonates at a predictable vibration when electricity runs through it. However, heat can modulate those vibrations, and the inaccuracies from that heat can resonate for upwards of 30 seconds a *month*. The easiest solution has been to [synchronize](networks.md) the time consistently with a timeserver ([NTP protocol](standards-computers.md)).

## Designing

To create a computer system, not everything starts with PCBs.

1. First, the designer needs to understand what circuits are doing, so they need schematics.
2. Then, they will use "breadboards" to create prototypes of electronic circuits, which don't require soldering and are completely reusable. The circuits will be low-speed because they're simply clipped onto the board.
3. After they know what they're doing or want something higher-speed, they'll either use "strip board" to prototype mid-speed circuits or PCBs for high-speed circuits.
4. Finally, when they want to build something for commercial use, they'll use PCBs.

[The Gerber format](https://en.wikipedia.org/wiki/Gerber_format) is a convenient alternative to creating something directly on a PCB. It's an open PCB [standard](standards-computers.md) that gives all the instructions necessary for an engineer to manufacture finished computer parts at scale.

The improvements of error-correcting code within [processors](computers-cpu.md) have made circuit design *much* more forgiving than in the past.
