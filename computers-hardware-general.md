
# The design of a general-purpose computer

[Many varieties of nerds](https://en.wikipedia.org/wiki/List_of_pioneers_in_computer_science) engineered what we now call a computer. But, we tend to use that word in a more limited scope than reality.

The cheapest alarm clocks and refrigerators now use computers, but those computers are specific-purpose. It's usually something small like activating an alarm when the time matches the alarm time or sending an electrical signal that turns a compressor on or off.

On the other hand, a "general-purpose" computer can do nearly *anything* based on [logic](logic.md) or [math](math.md). If you want, you *could* program your desktop computer to control your thermostat or run a timer. Sometimes it won't be as reliable, but it can do just about anything you want it to do.

Because they're so useful, manufacturers have adopted a relatively standard "modular" format for selling general-purpose computers.

## Case

The biggest enemy of computers is dust, for several reasons:

1. A layer of dust is like a blanket on the computer, and a case keeps most dust away.
2. Computers, specifically the processors, generate a *lot* of heat, so you need something to reliably hold the cooling system.
3. Since computers operate on [electricity-based logic](computers-alu.md), a static charge can ruin a computer or fry the system, and dust often builds up static electricity.

Thus, a case is critical to fight dust, though it doesn't need to be fancy. It also should be big enough to hold everything you need on it. Typically, there's room to feed cables toward the back to prevent them from blocking air flow.

Apparently, building a PC has become [cool](trends.md), so tempered glass and lighting is an accented [up-sell](marketing.md).

To make the device waterproof, standard waterproofing engineering applies for most of the device (e.g., seals, gaskets), but the ports themselves typically have a sensor that kills all electrical power from running through them. No electricity means the electronics are safe as long as no power runs through it before it's dry again.

## Power Supply

Computers process with DC ("direct current") instead of AC ("alternating current"). But, your typical household plug runs on AC, which tends to fluctuate all over the place.

A "power supply" serves two roles:

1. Convert AC power to DC.
2. regulate the flow of electricity for what the computer needs ("continuous wattage"), measured as a wattage rating.

Conveniently, batteries are designed to hold DC power already. Depending on how the circuit runs into the computer, batteries are separate power supplies because they regulate the wattage.

The power supply can sometimes be fragile, especially with events like a lightning storm. It's a *really* good idea to have a power strip or a UPS ("uninterruptible power supply") with a backup battery to keep a steady flow of electricity.

An average computer uses 200-300W (i.e., 0.2-0.3 kWh/hr), though it can go as high as necessary. It's worth noting that more electricity generates more heat and loses its efficiency, meaning that a standard computer needs about 20% more wattage than you think it'll need (i.e., get a 350W power supply for a standard computer just to be safe).

Power supplies can be non-modular, semi-modular, and fully-modular. Non-modular has *all* the cables you'll need, semi-modular has *only* the cables you'll need with options to plug in more, and fully-modular is a box without cables. This is almost strictly a cosmetic thing if you're not trying to do something elaborate, but many people building PCs will attach their [identity](identity.md) to how their computer looks.

Most power cables for laptops and other smaller tech have a "stepdown transformer" to lower the voltage that'd normally come from a household power plug (120-240V, depending on your country), since they don't need much (never more than 12V).

Amusingly, if you use a power plug adapter for your car to power your laptop, you're converting from AC (to crank the car's starter) to DC, back to AC inside the computer.

## Cooling

The CPU and power supply generate the most heat, so they need cooling.

Conventionally, both the CPU and power supply have had a fan to send heat away:

- Positive air flow is pulling (theoretically) cooler air into the case.
- Negative air flow is pulling warmer air out of the case.
- Neutral air flow is a combination of both positive and negative air flow.

The fans that usually come with a preassembled computer are sufficient for most purposes.

- Adding more can't hurt, assuming you can maintain a healthy air flow and don't overload your power supply.
- However, more fans guarantee more noise.
- The shape of the fan's grille pattern also makes a difference in noise. In general, wire and mesh grilles attached to the housing are the best for noise, and a swirl pattern directly engraved into the housing comes as a close second.

The more air that runs across a surface, the more friction it creates, and it ends up with the [engineering](engineering.md) constraint of a boundary layer that moves rather slowly near a surface. The only solutions that really work to offset it are to either blast the air directly *onto* the surface, or blast it rapidly near the bottom with an extreme aerodynamically-enhanced surface.

The latest in cooling technology involves running water through pipes over the CPU and fan, a bit like a car's radiator.

- In fact, some of the most elaborate and advanced computers involve running water *inside* the CPU's chipset.

If you're particularly bold to try it, and the motherboard supports it, you can overclock the computer in the BIOS settings. This makes the computer run faster, but increases heat output *everywhere* (especially the CPU), so make sure you have enough cooling beforehand and know *exactly* what you're doing or the heat will literally melt the processor.

On the other hand, if the BIOS supports changing the clock settings, you can also underclock the computer, which might be useful if you want to prolong the life of your computer and don't need a computer to be relatively fast.

## Motherboard

A motherboard is a "printed circuit board" that connects all the parts together on a really small scale. It also usually has a "clock" with a "CMOS battery" to track time and a "BIOS" chip ("basic input-output system") that runs before the computer "boots" up. They use a variety of connectors with various voltages (mostly 12V, but also 3.3V and 5V), and connect large buses via the 20+4 pin connector (which permits both 20-pin and 24-pin buses to connect).

Motherboards are usually the most complicated-looking and largest part of a computer, but are often much less expensive and complicated compared to the CPU, though they can often have many components built-in for increased functionality or reliability.

Each motherboard has specific limits to its "form factor". Specifically, the bigger the motherboard, the more chips in its "chipset", the more stuff you can put on it, and the bigger your case has to be. In order of size:

- Nano/Pico/Mobile ITX (best for small embedded systems)
- Micro ATX (standard for many generic PCs)
- ATX
- EATX (Extended ATX)
- XL ATX
- (they get larger for [enterprise-grade needs](computers-distsys-enterprise.md))

Motherboards have a variety of "rear ports" to plug other things in with the case closed. You can usually see these on the back of your computer, but they often stick a few through the front for convenience:

- USB ("universal serial bus") plugs, which are pretty much the universal standard right now, with different versions that have different speeds, and a few types of plugs.
- Display ports for the [screen](engineering-screen.md), which can include HDMI ("high definition multimedia interface"), VGA ("video graphics array"), and DVI ("digital video interface").
- "PS/2" port (from IBM's "Personal System 2") for keyboard/mouse, though this has largely been replaced by USB.
- Digital/analog sound cables. Unless you're doing something fancy, lime-green is for audio out and pink is for your microphone.

When you open the case, the motherboard has a wide variety of connectors:

- "CPU socket", which holds a CPU (absolutely necessary, and must match the motherboard)
- "SATA" connectors (only as necessary as the things you need, though "hard drives" have been popular for a few decades)
- The "RAM slots", which hold short-term memory (*really* necessary to have at least 1 if you don't want The World's Slowest Computer).
- Expansion slots, which permit you to expand what you can do (only as necessary as you need).
- Connectors that go to the "power supply" (one for the CPU, one for the motherboard), the front panel (separately for USB plugs and the power button), and fans.

Motherboard sizes generally use the ITX/ATX standard (in order from smallest to largest: Micro-ITX, Mini-ITX, Mini-ATX, Micro-ATX, ATX, EATX). Make sure you have the correct case for your motherboard: if the motherboard is too large it may not fit, and if it's too small you may need to get creative with cable ties.

Further, each motherboard has specific size requirements for all the parts that go on it. The pieces snap on like "LEGO" if they're the right size, but if they don't fit you'll need extreme tech skills to get it to run (though it's rarely impossible if the components themselves work fine).

There's no substitute for experience to tell why a motherboard won't detect a component:

- Sometimes the motherboard and component don't mesh because of how much newer one of them is, even if it fits fine.
- Sometimes the component or that specific port on the motherboard was manufactured incorrectly.
- The computer may be running on low power or have an issue with power draw.
- Some other weird thing that happens 1 in 1,000 times, but only someone who works with the troubled computers would have experience with.

## CPU

The [CPU](computers-cpu.md) is where the computer processes information. It fits into a "CPU socket" on the motherboard. Because it runs so hit, it *needs* a fan sitting right on top of it, and it also *needs* a dab of heat-conductive "thermal paste" to get the heat over to the CPU fan.

In a modern computer not [designed for cheapness](computers-embedded.md), that CPU has multiple "cores". Those cores are all CPUs in their own right, but are part of the singular chipset.

While there are a ton of various features (e.g., [hyper-threading to help with VMs](computers-distsys-vm.md)), most of them aren't particularly relevant for you unless you know exactly what you're getting into. However, *make absolutely sure you've got the right socket*. CPU sockets are [*constantly* changing](https://en.wikipedia.org/wiki/CPU_socket) every 2-3 years, and a CPU can *not* work in a different socket, so buy precisely what you need.

## RAM

The [RAM](computers-memory.md) is the "working memory" of the computer. They usually slide into the motherboard into conspicuously nearby slots to the CPU. Abstractly, it functions the exact same as a storage drive, but is much faster and gets wiped as soon as you kill the power to the computer (which is often why rebooting can often [fix](fix-cs.md) your computer).

Generally, RAM is the easiest (and most benefit-per-dollar) upgrade, though it's a good idea to keep an eye on which RAM slot numbers on the motherboard you're using, since it may require a specific order for using RAM slots.

The only thing to watch out for is that you *need* the same exact speeds and latency timing of RAM together. The RAM will often work with two different capacities, but *not* different speeds.

## Hard Drive

The hard drive contains the [memory](computers-memory.md) that stays around when you turn the computer off. It usually sits plugged into the motherboard on the side, but off in a separate part of the case.

It's worth noting that the hard drive doesn't necessarily *need* to fit in a "slot" in the case, especially with the newer "solid state drives". It just needs to be somewhere where air can easily flow by.

## External Media/Networking

You can often use a variety of external media to store and migrate information, such as CDs, tape drives, and USB/flash drives.

But, the more popular way to send information around is via the [internet](networks-cs.md), which rquires a network card. With the internet you can send and receive information, including updates. This makes the computer less of an information box and more of a connection device.

## Buildable/Upgradeable

The modular design of general-purpose computers lets you build computers from all the parts or upgrade parts as you need. This is *crucial* since new computer parts blow the old ones out of the water. In 5 years, a fancy $4,000 computer will be worth $1,000 before anything breaks on it that costs more than $500 to fix.

Things that fit in the expansion slots are never necessary to run a computer. These days, a computer has everything it needs to run everyday sound and video. However, upgrading the graphics card and sound card can *dramatically* improve your gaming/productivity.

When buying anything, the computers run benchmarks that measure how well something performs. Keep in mind that benchmarks for *any* computer part only apply for when the computer operates in a vacuum on the dark side of the moon. Real-life performance is often a fraction of the advertised number.

When you're working on a computer, make sure you have anti-static mats and an anti-static wrist strap. Electrostatic discharge can often damage circuitry or wipe drive space. Also, *never drop the parts*. The parts are so delicate that even *bumping* some of them at the wrong angle can permanently break them.

Bear in mind that upgrading *anything* often requires more electrical power and more space. Noting your power draw/capacity and physical space dimensions can *really* save on Next-Day Delivery shipping charges.

Of course, stuff *does* break, and a modular design means you can replace the part instead of the whole thing. Generally, once you're all setup, hard drives are often the most unreliable part in a computer.

Laptops and mobile devices are a weird exception to modularity. Their form factor is so small that most of their parts don't have standard sizes. To use something "standard", you're forced into a few possible options:

1. Get creative to hook it up, while will likely remove the "mobile" part of the mobile device.
2. Order another part of that exact type from the manufacturer (which is rare because they *want* you to buy a new device every 2-5 years)
3. If it was popular enough, buy an aftermarket part from a part vendor that specializes in it.
4. Pull apart a similar or exact model elsewhere to replace that component.
5. Accept defeat and throw it away.

## I/O Chains

Computers frequently output things without considering where that input will go. Then, someone can connect that "output" anywhere:

- A peripheral, such as the [speakers](computers-speakersmic.md) or [screen](engineering-screen.md)
- Long-term storage
- Another computer
- Absolutely nowhere

Physically, components typically connect with "ports" to other peripherals (e.g., [mouse](computers-mouse.md), [keyboard](computers-keyboard.md), extra storage). They're highly modular, and abide by [standardized](standards-computers.md) "form factors":

- The [design communicates](engineering-design.md) what's supposed to connect and where, as well as any constraints on what *can't* or *shouldn't* connect.
- However, bad design can sometimes mean multiple types of devices can create conflicts by using the exact same form factor (e.g., most USB cables). This defies the IETF principle to be precise in what you send, and flexible in what you receive.
- Further, it doesn't mean it's not possible to use alternative cabling. By separating out the wires and carefully attaching them to a different form factor plug, anything can technically plug into anything else, and may only need some [programming](computers-programming.md) (or software) to fix any information transfer problems.

This limited information transfer is a huge reason why [operating systems](computers-os.md) are elaborate while also allowing many unrelated people to work with them at once. Each person can [focus exclusively on what they understand](https://trendless.tech/understanding/).

We can also create some fascinating combinations by stapling the input and output together onto the same object.

- The touch screen, for example, is *both* an input ([digitizer](computers-mouse.md)) and an output ([LCD screen](engineering-screen.md)).
- A network router takes raw information, then [routes the information somewhere](networks-cs.md). It's the basis of most networks, but focuses on finding where something is supposed to go, then sending it there.

By sending the output to another computer, we can string them together:

- If they have different purposes, multiple computers talking with each other creates a "[network](networks-cs.md)". The largest network we have is the internet.
- If that network is tight enough and the computers are sharing resources, they're known as a "[distributed system](computers-distsys.md)".
