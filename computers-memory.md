
# Computer memory described

Computers depend on time to perform their logic operations.

There are many reasons why we might need to delay logic across [time](datetime.md):

- With all the electricity flowing through, running all the logic gates at once will overheat everything.
- We might only want the computer to calculate things when we hit a button.
- The computer might need to measure or perform something at an interval, such as every second.

Combinational logic is treating logic as an instant thing, but sequential logic works on a moment-by-moment basis. So, Logic Calculation A will create Result A when Logic Calculation B starts.

Technically, electricity doesn't just move from one area to another sequentially, and it flows a bit like water as the electrons migrate. To compensate for that, engineers figured out how much time it takes for electricity to move from one place to another, put stopping points in the middle (typically with "capacitors"), then made slightly larger separated units of time ("discrete time", rather than "continuous time") to track it. These are called "clock cycles".

## Each cycle

To keep track of time from the [motherboard](computers-motherboard.md), engineers use a Data Flip Flop (DFF) at each stopping point between each cycle, which holds either a 0 or a 1. It's usually made of 2 NAND gates stuck together.

This happens fast. A 3.6 MHz processor, for example, is processing about 3,600,000 cycles a second. To put that in perspective, our brains can never react faster than 8 cycles a second and the [display](engineering-screen.md) for most high-end games run at about 120 frames a second.

Normally, the entire endeavor can look a bit like stop-and-go traffic ("synchronous logic"), but engineers who manage asynchronous logic can make everything move even *faster* by getting rid of gaps where the electricity in the DFF is waiting for another clock cycle. This is a crazy-complicated engineering and design challenge.

## Across cycles

Now that we have the DFF, we sometimes want to hold that information across as many cycles as we want. To achieve this, we'll need to keep that information while allowing future information to come in ("register").

There's a straightforward implementation to make it work:

1. Attach a multiplexer before a DFF.
2. Feed the DFF output to *both* the output and that multiplexer's input.
3. Use a "load" to select whether we want the old info (if it's "0") or the new input (if it's "1", aka "assert").

Or to put more simply, imagine two light switches. Switch 1 controls the light, but only switches it on or off when Switch 2 is on. You can flip 1 back and forth all day with no difference until you flip 2 on. Flip 2 off again, and whatever you do with 1 doesn't matter.

## Remembering stuff

We can put registers together in parallel to make any size we want (represented by "w" for word width). Naturally, like everything else in computers, it'll be a [base-2 setup](computers-alu.md) (2-bit, 4-bit, etc.).

To make a RAM unit, we'll set up those registers in parallel, then make an "address" that locates which register to look at, represented by "k".

We'll then take the load selector, but run it through a gigantic demultiplexer, with the load as the input and the address as the selector.

In this way, we can assert on *many* registers. Even with a million registers, the logic is only operating on 1 register at a time. We don't notice because it's millions of times a second.

In other words, to reference a specific 0 or 1 in memory, it goes through the following:

1. Send the input to *all* the registers at once, but the "load" on all the registers (except our target register) is 0, so nothing changes. (e.g., register 1-8 are *all* receiving "00000001")
2. Run the load through a demultiplexer, with a selector for the desired address. (e.g., the selector address is "01000000", so the demultiplexer routes to register 2)
3. If the load is 0, only read the register.
4. If the load is 1, copy the information to the register.
5. Run the desired address through a gigantic multiplexer to read the memory. (e.g., the selector address is "01000000", so the multiplexer pulls from register 2)
6. Repeat a bazillion times.

To compare, the entire operation feels like a forklift driver accessing a gigantic warehouse full of filing cabinets: Row D, Pallet 14, Cabinet 3, second drawer. Row D, Pallet 14, Cabinet 3, third drawer, and so on.

After about 64 milliseconds, the electrical signals in bits would start decaying. For that reason, the memory system performs a refresh operation 8,192 times every 64 milliseconds (ms), which means it'll refresh (called tREFI) every 7,812.5 nanoseconds (ns), or every 7.81 microseconds (μs). When the memory gets hot, the refresh command will happen more slowly (every 3,906.25 ns). Anywhere from 0.4% to 5% of the running time is made of refreshes, which block any other operations on memory while they're happening.

By using ECC ("error correcting code"), we can be sure the information is reliably stored and retrieved. Not all processors use ECC, but they really, *really* should.

- There aren't any standards for ECC, so it all lands on the hardware vendor or [the programmer downstream](computers-software.md).
- While it's theoretically an increase in performance, individual bits (a 0 or 1) can sometimes flip, which can change anything from a barely different-colored pixel to a different text character in a file name.
- A 0.0000001% chance of a bit flip means a one-in-a-million chance, which becomes thousands of bits when it's *billions* of bits of data (and 1 gigabyte has 8 billion bits).
- Without ECC, [hackers](hacking.md) can often exploit bit flips, such as "race conditions".

## Clumping together

As a quantity, memory is measured by a downright confusing convention:

- 8 bits (i.e., registers) becomes one byte.
- 1024 (2^10) bits is a kilobit (kb).
- 1024 bytes is a kibibyte (kiB).
- BUT...1000 bytes is a kilobyte (kB).
- 1024 kilobits is a megabit (mb).
- 1024 kibibytes is a mebibyte (miB).
- BUT...1000 kilobytes is a megabyte (mB).
- The pattern carries onward for giga-, tera-, peta-, and so on.
- Beyond petabit/petabyte, we have exa-, zetta-, yotta-, xenotta-, shilentno-, and domegenegrotte-.

Computer-minded people like 1024-based numbers, so they'll use the "ibi" version, though sometimes people use bit-based numbering, so you have to divide it by 1/8. Data transfer often uses "bit" while hard drives tend to use "byte", so multiply it by 8 to calculate the actual amount of data downloaded or uploaded.

Non-tech normal people use 1000-based numbers, and [marketing](marketing.md) people like it because it makes their numbers feel bigger (4 terabytes is just under 3.64 tebibytes).

However, the prefixes are always the same, and are very useful to get a sense of scale. They go in a predictable order:

- Kilo- (a text file is rarely more than a few of these)
- Mega- (a music file is usually a few of these)
- Giga- (a game often takes this much, and used to be the memory size of computers c. 2002)
- Tera- (the typical size of c. 2020 computers' memory)
- Peta- (more than any consumer would ever need, often the amount needed for [machine learning](computers-ai-ml.md) or [running a large website](computers-sofware-webdev.md))
- Exa- (only giant corporations use this much c. early-2020s)
- Zetta- (massive)
- Yotta- (very, very massive and nobody talks about it)

## Physical vs. logical

Obviously, memory must be stored *somewhere*. That location defines what its "physical memory" is.

However, by using [distributed systems](computers-distsys.md), a computer can have more memory (by pretending multiple memory units are the same) or less memory (and allowing *other* computers to use the leftover memory). The portion the computer has designated as *its* memory (or how it's grouped across multiple media) determines is "logical memory".

This distinction between logical and physical memory, along with balancing [CPU load](computers-cpu.md) and [bandwidth](networks-computer.md), is essentially the basis of all [cloud systems](computers-distsys-cloud.md).

## Memory hierarchy

The faster the memory, the more expensive it is. Memory is often the most expensive part of a computer. But, if you want a fast computer, you'll want plenty of memory for processing.

However, addressing a large memory set takes more time than a small memory set:

- Memory addresses can become profoundly long, meaning more time to string along the 0s and 1s for it.
- The location of the memory has to physically be further away, just because of how big it is, meaning more length of wire to travel across.

Instead of paying top-dollar for *all* top-of-the-line memory, processors typically have a faster memory for constantly changing things (typically called the "cache") and a slower memory for less frequent changes (called main memory or RAM), and even slower and larger memory on a disk somewhere.

This situation has evolved into what's known as a "memory hierarchy":

- Modern general-purpose CPUs have multiple caches (on this computer it's L1 at 32 kilobytes, L2 at 256 kilobytes, and L3 at 9 megabytes).
- There's typically gigabytes' worth of RAM plugged into the motherboard.
- Beyond the motherboard, there's long-term storage that can be terabytes' worth of information.
- Plus, in a [distributed system](computers-distsys.md), the memory can theoretically sit all the way across the world and be as big as you want.

A CPU has to manage this memory hierarchy efficiently. To achieve this, the [CPU](computers-cpu.md) has a "memory management unit" (MMU) that connects the virtual location with the physical memory location. This would mean, for example, that memory register 00000985 will correspond to memory bank 1, register 986. The MMU stores this information in a "translation lookaside buffer" as a type of cheat sheet for the CPU.

## Long-term storage

There are several physical ways to store memory long-term.

RAM (random access memory) depends on electricity, meaning it's "volatile". But, it's easily accessible and relatively cheap.

- One of the older implementations of memory was called drum memory, which involved a spinning cylinder with read-write heads along the outside of the drum. It was eventually replaced in the 1970s by magnetic-core memory (i.e., RAM).

ROM (read only memory), on the other hand, doesn't depend on electricity. But, you can't write anything to it.

There are a few critical measurements of memory. They're often representing [statistical averages](math-stat-cs.md) more than precise numbers, but can be significant for [planning](mgmt-2_projects-cs.md) (especially [at scale](computers-distsys-enterprise.md)):

1. Its transfer speed. It uses [standard network speeds](networks-computer.md) to determine it, but should be magnitudes faster than a network's (since it's supposed to be literally next to the [CPU](computers-cpu.md)).
2. Its projected lifespan, which is measured by "program-erase cycles" (or simply P/E).

There's a frequent RAM/ROM hybrid called "electronically-erasable programmable read-only memory" (EEPROM) that lets you read and write things to it, but it sticks around after turning the computer off.

- EEPROM is at the heart of a *lot* of memory:
  - Long-term storage in flash drives (aka "flash memory drives") and MP3 players
  - Memory that holds the computer's BIOS
  - Solid-state drives (SSDs)
- EEPROM does have downsides:
  - Depending on what you need it for, it can be expensive.
  - The data *will* deteriorate after decades of sitting dormant.
- More modern iterations of EEPROM/flash memory use what's called NAND flash or NOR flash:
  - Single-level cell (SLC) stores 1 bit of information per cell. It's the highest-performing at 100,000 P/E cycles, but also slow and expensive.
  - Multi-level cell (MLC) stores multiple bits per cell (typically 2). It's denser than SLC and therefore can store more, but more sensitive to data errors and can only last about 10,000 P/E cycles.
  - Triple-level cell (TLC) stores 3 bits per cell. It's even *more* data-dense, but much more susceptible to errors and only lasts about 3,000 P/E cycles.
  - Constraints in electrical engineering prevent quad-level cells on a two-dimensional circuit board. 3D NAND is a new approach that stacks the cells into a 3rd dimension instead of as flat panels. It allows for more storage capacity without a huge price increase, and tends to give better endurance and lower power consumption.

There's also EPROM (erasable programmable read-only memory) that uses UV light to clear it. They're a pain to set up, so they're only useful for specific things that won't ever get changed (like an alarm clock or stopwatch).

Parameter RAM was a RAM on older Mac computers that required a constant battery backup.

Many computers use NVRAM (non-volatile random access memory) to hold key system settings that may need to change (such as most of the [BIOS](computers-boot.md) settings).

If you're trying to store *lots* of information, you likely have only a few possible uses:

- Desktop PC - mixed read/write, but only on for hours at a time (and not days or weeks).
- Network Attached Storage (NAS) - mixed read/write, but not accessed for days, weeks, or months.
- Surveillance - *heavy* amounts of writing data, but less than 1% of the data is ever read.
- Cold storage - idle for most of the time, but requires enormously fast response and speed when accessed.
- [Data center](computers-distsys-enterprise.md) - *constant* read/write on a hefty [network connection](networks-computer.md).

To store *lots* of information for a long time, there are several specific options:

- Compact discs (CDs) are coated polycarbonate plastic with optical (i.e., laser-readable) information permanently burned onto them, with a thin layer of aluminum to reflect the information. Some are read-only (CD-R) and others are read/write (CD-RW). While they can get scratched, the ink from a permanent marker can also erode the reflective coating over years.
- Hard disk drives (HDDs) are cheap, even if they're slower than SSDs, and are often bigger capacity. Like their granddaddy floppy drives, they use magnetic signals to store information. Unlike floppies, HDDs use a neodymium magnet as a pivoting actuator (rather than hardware in the floppy drive itself).
  - HDDs and SSDs have historically used Serial Advanced Technology Attachment (SATA) cables, but some SSDs use Non-Volatile Memory express (NVMe) to connect straight to the motherboard for improved speed.
- Tape drives are still popular for huge amounts of relatively unimportant data (such as soil measurements or trivial user data).

Regarding how computers view memory logically, any long-term media is functionally the same as RAM, but much slower and often *much* bigger, as well as treated differently by the [operating system](computers-os.md). In fact, many operating systems convert hard drives into "swap space", which creates "virtual memory" for the [CPU](computers-cpu.md) to work with more memory.

When fabricating memory, there are several constant realities to manufacturing them that make it expensive when not at scale:

- The environment needs to be *spotle*ss, to the magnitude of 100-1000x cleaner than a surgeon's operating room.
- The memory is first fabricated on a flat surface based on a pre-made diagram, then layered together, frequently with something in the middle to protect the layers from each other.
- The layers are woven together with a conductive wiring like gold thread or copper circuitry.
- If it's on a circuit board, the solder paste must be melted through a large oven.
- It needs a metric *shed load* of quality control to pass the high standards everyone expects from their media.

## Safe memory

Memory must be tested rigorously before it's sold. The general approach is to test it for up to *millions* of program/read/erase/read cycles to ensure it's reliable. Flash memory goes through less rigorous testing than hard drives.

Higher-quality memory has built-in ECC, with a parity bit for every 8 bits (i.e., a 64-bit register will have 72 bits total).

Before a hard drive permanently fails, it'll often provide S.M.A.R.T. (Self-Monitoring, Analysis, and Reporting Technology) errors. These errors can be crucial in detecting problems before they arise and avoid permanent data loss.

For long-term storage, it's not always safe to only have one place to hold the memory:

- If it's your desktop computer, you won't really need any redundancy besides [cloud backup](computers-distsys-cloud.md) of your important user files.
- Because of the sensitivity of the information, NAS and surveillance utterly *require* a "redundant array of independent disks" (RAID).
- For cold storage, it's safest to use at least 12--24 drives in a RAID array, possibly higher.
- In a data center, the vast size of the project can mean hundreds or even thousands of drives.

RAID configurations are based on redundant information ("parity") and spreading the information across multiple drives ("striping"):

- RAID 0 has striping, but no parity:
  - DISK1 - A1, A3, A5, A7
  - DISK2 - A2, A4, A6, A8
  - This is technically the most unsafe way to set up an array, but gives you the most space.
- RAID 1 has parity, but no striping:
  - DISK1 - A1, A2, A3, A4
  - DISK2 - A1, A2, A3, A4
  - Because all the memory is used twice, you can usually swap the drive while the computer is still running.
- RAID 5 has striping across multiple disks *and* parity to check if there are errors:
  - DISK1 - Ap, A2, A3, A4
  - DISK2 - B1, Bp, B3, B4
  - DISK3 - C1, C2, Cp, C4
  - DISK4 - D1, D2, D3, Dp
  - This is a tradeoff: it isn't as fast or large as RAID 0 (from the parity bits) or as safe as RAID 1.
- RAID 10 is a hybrid of RAID 1 and RAID 0:
  - RAID 0: 2 disks
    - RAID 1 with 2 disks (DISK1 and DISK2)
    - RAID 1 with 2 disks (DISK3 and DISK4)
  - This solution is the best for large-scale endeavors because there's always a copy of the data if any individual drive fails.

For read-only external media like CDs, the best way to store a backup is to make a .iso archive file. Most modern operating systems can pull up that file as a [virtual drive](computers-distsys-vm.md).

If the drive is [self-encrypted](encryption.md), it means there's a [processor](computers-cpu.md) attached directly to the memory unit that encrypts and decrypts the memory as it's used.

## Faster memory

Memory access is typically the slowest part of processing, so engineers are constantly working to make faster RAM.

The clock speed can be a bit misleading. While it can be pretty accurate (3200 = 3,200,000,000 megatransfers/cycles per second), RAM timing/frequency is based on how fast it takes to move information to *or* from the RAM, which means you need to cut it in half. It's not too difficult to break down the math:

- 3200 megatransfers/second
- x 64 bits per transfer in a 64-bit computer
- / 8 bits per byte
- = 25,600 MB/s
- / 2 for *actual* speed (because it's read/write) = 12,800 MB/s

To speed it up even further, RAM started using multiple channels at once.

At first, they used a "ganged" setup, where they connected 2 64-bit buses together to make a 128-bit bus. Once [CPUs](computers-cpu.md) started having more than 1 core, unganged RAM became faster because it could pipe the information to multiple cores at once. This entire setup is known as "dual channel", but can also be quad, 6, 8, or higher.

So, a dual-channel takes the above calculation and doubles it, a quad-channel quadruples it, and so on.

Further, RAM will often include ICs (integrated circuits) to perform tasks to make it even *faster*.

## Abstraction

Once the memory has been created physically, it groups into "sectors" when a new hard drive is created, which then assemble into blocks of memory. At this point, it's a homogeneous abstraction where it really doesn't matter *what* it is, as long as it's reliable.

Of course, like all things in [reality](science.md), memory attenuates over time, so it will need periodic scanning to find bad sectors. From there, the operating system can earmark those sectors as bad, and hopefully no important data was lost.
