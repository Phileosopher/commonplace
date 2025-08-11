
# The CPU described

The "central processing unit" (CPU) is the device that sifts through information and turns it into other information. It's an implementation of an "instruction set architecture" (ISA).

The older CPUs [weren't as miniaturized](computers-cpu-8086.jpg), so you couid visibly see the [logic gates](computers-alu.md), which is helpful to understand what's actually happening on a computer chip.

Lately, most general-purpose computers have more than one CPU inside its main "chipset". Engineers call them "cores", so it's a "dual-core processor" or "quad-core processor" or whatever size that applies.

Each of these cores can only work on 1 [memory](computers-memory.md) register at a time. While they do it very fast, the only way a computer can legitimately multi-task is by having more than 1 core.

Further, to make them faster, CPUs often have memory on the chip as well. To make them faster, they'll often give L1 memory to *each* of the cores. Some of the more advanced processors have *tons* of memory embedded in the processor chipset.

To keep track of super long procedures, a CPU will also often have an "accumulator" that holds unfinished results to use later instead of having to write it to memory.

## Components

CPUs are a far simpler abstraction than it may appear:

1. An [ALU](computers-alu.md) that processes [logical](logic-cs.md) calculations and outputs data.
2. [Memory registers](computers-memory.md) to hold information.

The ALU's control bits will give context-sensitive information to indicate what else to do with the information (e.g., whether the answer is negative or zero).

This information comes in several classifications:

1. Control memory, often called a "program", which is a set of instructions for what you want calculated.
2. Address memory, which the references inside memory to *other* memory addresses that have what you want.
3. [Data](data.md), which is information that gets fed into the control memory or outputted at the end.

A CPU only really does 2 things, called the "fetch-execute cycle", over and over:

1. Fetch: use the program counter to get a program instruction located in a [memory address](computers-memory.md).
2. Execute: reference the program instruction to work the data located in (usually) another memory address.

While all computers broadly use the [von Neumann architecture](https://en.wikipedia.org/wiki/Von_Neumann_architecture), the [Harvard architecture](https://en.wikipedia.org/wiki/Harvard_architecture) often gets used instead. The only main difference is that the memory for programs versus data are processed on separate channels. Most modern computers designed for high-performance use *both* of them, where they split the cache into a "modified Harvard architecture" ("split cache").

## Peripherals

To work with information coming in (inputs such as a [keyboard](computers-keyboard.md)) and outgoing information (outputs such as a [screen](computers-screen.md)), the CPU tends to see it as merely specific [memory](computers-memory.md) registers. Memory location 14136, for example, might be where the computer listens to the [mouse](computers-mouse.md) input.

Drivers are instructions about where that memory goes, as well as how the CPU can interact with that information.

## Ticking things along

Computers need instructions, but they're the world's fastest idiots. Without further instructions, they'll keep doing the same thing over and over.

Thus, programmers want computers to move from one instruction to the next, then jump around as instructed. CPUs have a "program counter" for this.

A program counter has 3 major functions:

1. Add 1 to the number given, then output.
2. Output 0 to reset everything.
3. Output any number specified.

There are 3 control bits that do this:

1. inc - adds 1 to the input
2. reset - overrides everything and gives 0
3. load - gives the input as the output

The result creates a pleasantly simple solution:

- Left alone, it transitions from 0, to 1, to 2, and so on.
- If you put in 15, 16 comes out, then 17, then 18, and so on.
- If you want, you can zero it out at any time to start over.

Even when a computer is doing "nothing", it's still ticking along with a "nothing" process.

## But what *does* it do?

From a different viewpoint, a CPU is a tiny information factory. As an example, let's use 4 8-bit [memory](computers-memory.md) registers:

1. 00010111
2. 11001000
3. 01011101
4. 10010011

While it's cryptic, each of those bits has a meaning (which varies depending on the manufacturer). For the sake of example, here are the following rules:

1. The first bit may be a switch that dictates whether the rest is a memory address or an actual instruction.
2. Bits 2-4 are [advanced logic](computers-alu.md) operations that give instructions on what to do.
3. Bits 5-6 are specifying whether to store the output information in the address register (that points to the memory location), a temporary memory register inside the CPU, or outside the CPU in RAM.
4. Bits 7-8 specify a "jump", where the next instruction might feed into the program counter.

So, it'll look like this:

1. 0 0010111 - It's referencing a memory address, so go to memory address 0010111
2. 1 100 10 00 - It's an instruction, saying to do the advanced logic of x+y, then output to RAM, then to increment the program counter
3. 0 1011101 - It's referencing a memory address, so go to memory address 1011101
4. 1 001 00 11 - It's an instruction, saying to do the advanced logic of NOT y, then output to the CPU's memory register, then feed the output into the program counter

The CPU I've made was 16-bits, and I have a hard time completely imagining a full-function 8-bit computer (I needed 14 bits to feed all the instructions), but it would likely mean sending the instructions on multiple registers with another control bit to indicate if it's Instruction Part 1 or Instruction Part 2. It would also mean you could only address 128 memory registers at a time (as opposed to 32,768 with 16 bits or 4,294,967,296 with 32 bits).

However, the above paragraph is merely a thought experiment, because CPUs have had at least a 64-bit architecture for a long time, ever since RAM started surpassing 4 GB (c. mid-2000s), and the trends will keep growing that size as memory becomes larger.

Of course, these 0s and 1s are difficult to program with, which is why [assembly code](programming-assembly.md) is so important.

When the the processor is able to handle words that are smaller than the register, they use a weird informal word called "endianness". Basically, big-endian memory holds it at the "big end" or back of the register (e.g., 0000000010101111) and little-endian on the "little end" or front (e.g., 1010111100000000). This feature allows for backwards compatibility with old [operating systems](computers-os.md) or odd-sized registers.

## Better CPUs

CPUs travel at the speed of electricity or light, but the "speed" of a CPU is basically how many computations it can do per second, measured in hZ. Thus, more transistors on a CPU means it's "faster", since it can work through more stuff at once. Multiple cores can also magnify this, assuming that the computer program can be set to run different sets of instructions at the same time (also known as "pipelining" or "parallel processing").

Because of how elaborate (and microscopic!) these transistors are, processors are often the most expensive parts of a CPU, and this trend is likely to continue.

Moore's Law once stated that transistors halved in size about every 2-5 years, but it now broadly refers to how computers simply double in speed, since many processing improvements are more improving the arrangement than necessarily cutting down its size.

These transistors are stunningly small. As of writing this in 2022, there's talk of 2-nanometer transistors coming to the market, which is one billionth the size of a meter. To put that into perspective, a DNA strand has a 2.5-nanometer diameter and an atom is ~0.1 nanometers.

Also, while speed is important, energy efficiency is as well, especially with anything that runs off a battery, such as mobile devices. Heat management, especially, is a major concern: silicon CPUs run around 65-80°C (150-175°F).

Plus, reliability is important, since it's not good to have a CPU that fails after a few months of continuous use. Thankfully, energy efficiency goes hand-in-hand with reliability, since less electricity means it generates less heat.

While Average User You can ratchet up or dial back the clock speed to give you better or longer performance ("overclocking" or "underclocking"), engineers are constantly improving their designs to get more performance out of a CPU:

- Stack the "nanosheets", thin arrays of transistors, together more closely.
- Stick the media control, graphics, calculating, and a hefty amount of [memory](computers-memory.md) onto the chipset as well.
- Add hardware-based code into the CPU to do more things that would have normally been implemented as software (e.g., [advanced math](math.md), [machine learning](computers-ai-ml.md)).
- Give better [code](programming-basics.md) that better balance how multiple cores handle information. This may mean changing the workload of each core when one is idle, translating the data into another format that's quicker to work with, condensing the information and getting rid of it before a core sees it, or timing cores to handle certain things at certain times.

It's worth indicating that performance benchmarks are rarely representative of real-world hardware performance. Besides [Goodhart's Law](lawsaxioms.md) regarding benchmarks against competitors, the device would only hit those marks in a perfect environment (e.g., near sub-zero temperatures, brand-new motherboard, zero peripherals). This happens to be true for [networking equipment](networks-computer.md) as well (e.g., in a vacuum on the moon).

Even in relatively mundane chip-making manufacturing plants, the technology to make them is remarkable. The "extreme ultraviolet lithography" (EUV) technique, for example:

1. Spray microscopic drops of molten tin across a vacuum chamber.
2. Blast the drops with an incredibly precise 25-kilowatt ultraviolet laser. The laser is so precise that it can hit a penny from the moon, which will evaporate the droplets into a small flat cloud.
3. Fire a second shot that bounces the beam off a series of mirrors that directs the tin onto a silicon wafer. This will directly draw the transistors and other features onto the chip.

## Looking ahead

This section was updated in 2025.

Now that [miniaturization connected with Moore's Law](lawsaxioms-tech.md) has stopped due to the limits of electrons, the future of CPUs is in [quantum computers](computers-quantum.md), but more readily may come from light-based implementations instead of electricity (i.e., using photons instead of electrons). The advantage of light is that it generates much less heat, but it can be difficult to capture and manipulate photons.

Because of advances in [3D printing](computers-printers.md), we may likely see an average person have the ability to make a decently-powerful computer in their own home simply by gathering the components.

There are attempts at creating affordable, flexible plastic 32-bit chips. They would expand with IoT's IPv6 allocations dramatically and give *everything* a [networked](networks-computer.md) component. However, beyond the affordability aspect, it does beg the question whether it's economically worth labeling and sending network data about whether milk is expired, so it may take some decades to adopt.

The disadvantage of any new hardware [trend](https://trendless.tech/trends/) is that it takes time for the hardware to catch up. Silicon microcomputers were painfully slower than vacuum tube implementations for a long time, until the technology became mature enough, and now almost nobody outside of [radio enthusiasts](radio.md) use vacuum tubes anymore for processing information.

## Further Learning

[nand2tetris](https://www.nand2tetris.org/) Part 1 is a definite recommendation, and there are several implementations of it:

- The [Coursera course](https://www.coursera.org/learn/build-a-computer) made by the creators.
- [The Nand Game](http://nandgame.com/). However, the creator was trying to make it extremely simple, so it overlooks certain necessary elements that make it more challenging to progress.
- [MHRD](https://store.steampowered.com/app/576030/MHRD/) is a puzzle game, which is the same thing as the Coursera course without as much instruction.
- [Just download the software from their website](https://www.nand2tetris.org/) and do it yourself.
