
# Electrical engineering

## Electrical connections

Electricity is simply the large-scale movement of many electrons from atoms with more electrons than protons to atoms with fewer electrons than protons. Electricity is *everywhere* in small amounts, but we only see it naturally occur on a dramatic scale with lightning.

The formation of electricity gives *tremendous* capacity for people to magnify their labor, and is by far the most ubiquitous. An electrically powered engine generally has less torque than anything combusted (e.g., internal combustion engine, rocket engine) but the energy is *much* easier to transfer around to other sources compared to anything strictly mechanical.

Amperes measure how fast electrons flow, and volts measure the difference in how many electrons between two points. There's usually an analogy with water where voltage is pressure and amperage is flow speed. Wattage is simply amperage multiplied by voltage.

Electricity travels from one point to another through a "conductor" that has a certain amount of resistance measured in ohms. Metal tends to have a much lower resistance than most other materials, and some of the best conductors happen to be copper, silver, and gold because they're [more capable of picking up additional electrons relatively easily](science.md).

Wires can be temporarily engaged to complete the "circuit". The engagement is typically hidden behind a [designed](engineering-design.md) housing with a switch for the user's safety.

There are usually "fuses" placed in a box to precisely detect where the assembly will break in the case of a severe spike in electric current. All the wiring is supposed to travel through that fuse box at some point in its journey to prevent any cables from breaking in an unpredictable location. For that reason, barring a frayed wire from exposure to the elements, most typical electrical failings are either within the output (e.g., light bulb) or within the fuse.

Alternating current (AC) travels *much* farther than direct current (DC), and is generally safer simply from the fact that electrocution will make the victim's muscles seizure instead of contract. However, most small-scale electrical components that use batteries use AC, and [most computers](computers-cpu.md) use AC for their signals because they're more predictable.

## Solar cells

Solar cells are made of photovoltaic cells, which convert photons into electrons:

1. Light strikes a photovoltaic (PV) cell, usually made of a material like silicon and sandwiched between glass or plastic for protection.
2. The energy of the absorbed light knocks electrons loose.
3. By attaching metal contacts on both sides of the cell, they can gather those electrons to make electricity.

## Electrical heat & magnetism

One of the side effects of electrical transfer is heat. By winding electrical cabling into a tight coil, electric current can generate a heating element. This is essentially how *all* electric heaters work, from toasters to coffee pots.

Another side effect of electrical transfer is magnetism. Again, by winding electrical cabling into a tight coil, current can make the device an electromagnet. They have several uses:

- Generate electricity by applying mechanical energy to it (e.g., a generator).
- Detect magnetic activity through energy within its proximity (e.g., metal detector).
- Configure it with a magnet to create a gauge (e.g., speedometer).

## Batteries

In a straightforward sense, a battery is an AC electricity storage container for later use:

1. Have something in a safe box which holds a positive electrical charge for a long time (i.e., many atom ions missing [electrons](science-physics-quantum.md)).
2. Have something in another safe box which holds a negative electrical charge for a long time (i.e., many atom ions with extra electrons).
3. Attach the device you want to power with a + and - conductor, typically a cable.
4. As the device needs, it'll draw electrons off - (the cathode) as they travel to + (the anode).
5. Over time, the cathode reduces and the anode oxidizes, and the charge decreases.
6. The process can sometimes be reversed, meaning the cathode increases and the anode deoxidizes (i.e., recharging).

The design of the boxes and how fast they connect determines how much power draw you get, as well as whether more electrons can be added to the negative side (i.e., recharged).

Some batteries (like car batteries) are meant for rapid discharge all at once, while others (like cell phone batteries) are designed to discharge *very* slowly.

Batteries are ionized atoms, so they're in a state of kinetic potential energy, which means they're subject to decay per Newton's First Law (An object at rest remains at rest, and an object in motion remains in motion at constant speed and in a straight line unless acted on by an unbalanced force). Because of this, they tend to incur a type of "memory" for their capacity, and they must stay ionized (i.e., charged) or will decay more quickly over time.

In practice, longevity with *any* battery requires a few habits:

1. Keep the battery charged as much as possible.
2. Recharge a battery whenever reasonably possible to next charge it.
3. With a few exceptions for specific engineering, don't permit the battery to get down to 0%.

Batteries used to be liquid acid in jars:

- There is a *very* affordable sodium-sulfur battery (Na-S), but it uses a molten salt electrolyte, so it's only useful for large-scale uses (e.g., home battery backup, solar/wind generation).

Most everyday batteries are a few broad classes of solid metals, and most of them are subject to the memory effect (its capacity deteriorates with each recharge):

- The first rechargeable battery was lead-acid in 1859, which doesn't hold much energy but can produce large surges of current (which is necessary for starter engines in autos).
- The zinc-carbon battery in 1886 was one of the first dry-cell batteries that mixed manganese dioxide dipped in a mix of ammonium chloride and plaster of Paris with trace amounts of zinc chloride, then sealed in a zinc shell.
- Nickel cadmium (NiCd) was developed in 1899 and uses nickel and cadmium in a potassium hydroxide solution.
- Nickel-iron is like NiCd and was also developed in 1899, but iron is inferior to cadmium because it produces lots of hydrogen gas when charged (and therefore can't be sealed).
- Alkaline batteries in the 1950s dramatically improved on the zinc-carbon battery with a manganese dioxide cathode, powdered zinc anode (which gave the battery a larger surface area), and an alkaline electrolyte.
- Nickel-hydrogen arose in the 1970s for smaller applications (e.g., electronics). It was followed by nickel metal hydride (NiMH) in 1989. They have longer lifespans than NiCd, and aren't as toxic as cadmium.
- Lithium-ion (Li-ion) is more lightweight than nickel-based batteries, but is also pricier. There were experiments as far back as 1912, but it didn't develop commercially until the 1970s.
- Lithium polymer (LiPo) was developed in 1997, and holds the electrolyte inside a solid polymer instead of a liquid solvent, and the electrodes and separators are laminated to each other (which means it can be flexible instead of inside a rigid metal housing) and wrapped around as a coil. The positive electrode is aluminum foil, and the negative one is copper. The one downside is that LiPo tends to swell, and any connection between
- Lithium iron phosphate (LiFePO~4~, or LFP) is a low-cost, non-toxic, relatively safe derivative with naturally abundant materials. LiFePO~4~ was only developed as early as 1996.
- Gallium nitride (GaN) has been used for blue light-emitting diodes (LEDs) since the 1990s, but has recently been developed for battery use. If they can successfully make them affordable, they'll be able to charge faster than the others (which is critical for use cases like electric vehicles).

The specific metals necessary for batteries are rare earth metals that require unique mining techniques to extract. Even though lithium batteries are 100% recyclable, they are often discarded. Some regions [illegalize](people-rules.md) discarding batteries, which can be a problem [at scale](groups-large.md).

Battery indicators require a specialized "integrated circuit" (IC) that tracks battery usage. One of the simplest battery indicators is an [algorithmic](computers-programming-algorithms.md) implementation of the Coulomb counter:

1. Measures the current charge.
2. Measures the available charge later.
3. It uses a simple calculation to figure out how much charge is left (e.g., it started with 10 amps, there are 4 amps now, and it's discharging 1 amp per hour, so it's at 40%).

Battery technology develops relatively slowly compared to the things it tends to power. Typically, better [software programming](computers-software.md) that saves on memory management increases battery life more than actual battery improvements.

Batteries are *very* versatile, and can serve to benefit a household by preparing for a [short-term disaster](hardship-disaster-2_long-stay.md), glean energy from an engine's movement, or be quickly and easily manufactured as a replaceable supply material for small-scale electrical needs.

Batteries are built into *many* objects (e.g., laptops, scales) without an off switch and simply a timer for [design reasons](engineering-design.md). However, every single piece of technology *needs* a physical switch that can kill the connection to the battery. Otherwise, the latent stray electricity can create [break-fix](fix.md) headaches later.

One of the newest developing technologies for batteries is called a hydrogen fuel cell. The concept is essentially the same as a battery, with a few modifications:

1. The anode and cathode are separated only by a polymer electron membrane (PEM), which only allows positively charged ions to travel through it.
2. On the cathode side, oxygen is fed into the system.
3. On the anode side, a catalyst (such as platinum) splits hydrogen molecules into protons and electrons.
4. The electrons travel through an external circuit as a battery output.
5. The hydrogen protons travel across the PEM and bond with the oxygen, producing water (H~2~O), then move out of the system.

One significant issue with hydrogen fuel cells is in finding a reliable and affordable source of pure hydrogen for the inputs.
