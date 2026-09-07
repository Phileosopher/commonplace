
# Electrical engineering summarized

Electricity was discovered by observing the electric eel. It etymologically combines "electrum" from Latin and "ēlektron" from Greek. This word was synonymous with was a naturally occurring alloy of gold and silver called "amber".

There are a vast range of [standards](standards.md) for electrical code, and they move around based on new developments and implementations. However, given that the technology is about 200 years old, they're nowhere *near* as volatile as [computer standards](standards-computers.md)

Electricity and magnetism are *very* connected.

- A magnetic force can be multiplied through an electric current by wrapping an electrical coil around an object. This is how speedometers and voltmeters work.
- It's always safe to assume magnetism is present when electricity is present, and the converse.

Electricity is simply the large-scale movement of many electrons from atoms with more electrons than protons to atoms with fewer electrons than protons. Electricity is *everywhere* in small amounts, but we only see it naturally occur on a dramatic scale with lightning.

## Electrical connections

Electrical energy travels through current between positively or negatively charged objects. Voltage is the potential energy difference available between two charges, and is defined as the amount of potential that causes 1 amp moving in 1 second (a "coloumb") to do 1 joule (0.737 ft-pounds) of work.

The formation of electricity gives *tremendous* capacity for magnifying their labor, and is by far the most ubiquitous. An electrically powered engine generally has less torque than anything combusted (e.g., internal combustion engine, rocket engine) but the energy is *much* easier to transfer around to other sources compared to almost every other mechanical object.

Amperes measure how fast electrons flow, and volts measure the difference in how many electrons between two points. There's usually an analogy with water where voltage is pressure and amperage is flow speed. Wattage is simply amperage multiplied by voltage.

Electricity travels from one point to another through a conductor that has a certain amount of resistance measured in ohms. Metal tends to have a much lower resistance than most other materials, and some of the best conductors happen to be copper, silver, and gold because they're [more capable of picking up additional electrons relatively easily](science.md).

Water itself is a poor conductor, but small impurities like salt, acid, and solvents can make water convert from being an insulator into a conductor. This holds true as well for anything that can get wet, such as dry wood or dry skin.

Alternating current (AC) travels *much* farther than direct current (DC), and is generally safer simply from the fact that electrocution will make the victim's muscles seizure instead of contract. However, most small-scale electrical components that use batteries use AC, and [most computers](computers-cpu.md) use AC for their signals because they're more predictable.

Static electricity can also cause a shock, but not usually as severely. It comes from electron buildup, usually from friction, without any grounding.

## Wiring

Wires can be temporarily engaged to complete a circuit. Electricity works with wires because the wire is the path of least resistance (i.e., usually copper or aluminum). That pathway is usually from the live current to its designed destination, the ground, an accidentally energized piece of metal, or another conductor with a current.

To ensure the path is always through desired conductors, all engineered electrical components have insulators that impede the flow of electricity. Further, wires are typically hidden behind a [designed](engineering-design.md) housing with a switch for the user's safety.

There are usually fuses placed in a box to precisely detect where the assembly will break in the case of a severe spike in electric current. All the wiring is supposed to travel through that fuse box at some point in its journey to prevent any cables from breaking in an unpredictable location. For that reason, barring a frayed wire from exposure to the elements, most typical electrical failings are either within the output (e.g., light bulb) or within the fuse.

The most basic division of wire and cable technology is based on voltage:

- 300V: signaling, controls, [wired communications](computers-networks.md)
- 600V: the most widely used, typically for power and light circuits
- 2kV-25kV: medium-voltage electrical power distribution circuits

At high voltages, power lines have to be separated from any risks of an accidental connection (or nearby due to arc flash). In particular, overhead power lines have [specific clearance requirements based on their rated voltages](engineering-electrical-overheadlines.jpg).

## Phases

A single-phase power transfer is best done with DC, since AC will constantly vacillate.

The 2-phase power system is the simplest usage of AC:

- 2 different conductors carry AC with the same frequency and voltage amplitude based on a common reference.
- However, each phase is offset by 1/2 of a cycle (i.e., 180 degrees out of phase).
  - At any given point in time, the magnitude of each conductor will be the same as the other conductor, but with the opposite polarity.
    - e.g., if one conductor at a specific point in time charged with +125V, the other will have -125V.

The most common electrical system is the 3-phase power supply system:

- The 3-phase supply is more [economical](money-economics.md) because it allows the same amount of power transmitted with 75% of the conductor material.
- At any given point in time, the magnitude of each conductor will be the same as the other two currents combined, but with the opposite polarity.
- 3-phase systems often include a 4th wire, especially in a low-voltage distribution, which is a "neutral" wire that allows separate phases to act as a single-phase output.
  - This offsets the downside of 3-phase systems, since most consumer-grade electrical power runs on single-phase power.
- The phase offset can either be configured in a star connection (which looks like a "Y") or a delta connection (which looks like a "Δ").
  - There is no neutral point in delta, so delta always uses 3 wires.
  - The one advantage of delta is that it has more starting current, so it works great for things that need high starting torque (e.g., large electric factory motors).

## Voltage

The voltage classifications aren't universally standard, so the IEC and ANSI/NEC [standards](standards.md) differ:

- Extra Low Voltage (ELV)
  - IEC: below 50V AC or 120V DC
  - Applications include low-power devices like battery systems and control circuits.
  - This also dovetails closely with [computer signals](computers-networks.md), where the electricity is meant as information instead of power generation.
- Low Voltage (LV)
  - IEC: 50V-1kV AC or 120V-1.5kV DC
  - ANSI/NEC: up to 600V AC
  - Applications include consumer-grade uses like residential power, commercial buildings, and lighting systems.
  - Beyond LV, just about everything is AC power (due to its long-distance usefulness and that it's generally safer).
- Medium Voltage (MV)
  - IEC: 1kV-35kV, but sometimes extends to 52kV
  - ANSI/NEC: 601V-69kV
  - Applications include local distribution, industrial facilities, datacenters, and low-power power plants (e.g., solar and wind)
- High Voltage (HV)
  - IEC: 35kV-230kV
  - ANSI/NEC: 69kV-230kV
  - Applications include transmission lines, substations, interceity power transfer, and heavy industrial power.
  - In general, the classifications move around, but everyone agrees that things get a bit different at 230kV.
- Extra High Voltage (EHV)
  - IEC: 230kV-800kV
  - ANSI/NEC: 230kV-500kV
  - Applications include long-distance transmission lines, grid interconnection, large power plants, and cross-border power exchanges.
- Ultra High Voltage (UHV)
  - IEC: over 800kV
  - ANSI/NEC: over 500kV
  - Applications include bulk power transmission, supergrids, continental power transfer, and future grid technologies.

## Ground faults

When the cable insulation fails, there will be a ground fault.

- Essentially, the cable will somehow make contact with a conductor that makes its way to the ground.
- This will represent as *massive* power draw, as well as possible arc flash
- However, a ground fault can be cleared if the cable's design prevents the ground fault from persisting.
- Even a small cut can slowly erode a cable because it creates a pocket of air.
  - The breakdown can often represent something visually similar to water erosion, where the electricity erodes the insulation until something breaks through.

People can detect current as small as 1 milliamp.

- At 5 milliamps, someone will feel a slight shock that's uncomfortable but not painful.
- Due to muscle and fat composition, at 6-25 milliamps for women or 9-30 milliamps for men it will be a painful shock and muscular control will be lost.
  - At this point, it may not be possible to let go, but the person can be thrown away from the current if their extensor muscles are stimulated.
- At 50-150 milliamps, the shock will be extremely painful and can potentially cause a heart attack.
- At 1-4.3 amps, the heart will cease, muscular and nerve damage will happen, and it's likely fatal.
- At 10 amps, the heart will cease and there will be severe burns, and death is probable.
- However, 15 amps is the lowest overcurrent when a fuse or circuit breaker opens a circuit.

The most common injury from electrocution is through burns.

- Electrical burns are from current generating heat while flowing through body tissues.
- Arc or flash burns come through high temperatures from an electric arc or explosion near the body.
- Thermal contact burns are from the skin touching hot surfaces of overheated, energized equipment.
- The duration of exposure can be magnified, however, through a "freezing" effect due to involuntary contraction.
  - Even long exposure to relatively low voltages can be as dangerous as shorter exposure at higher voltages.

Arc flash will happen across air at about 60-70 volts/mil:

- i.e., a 600-volt cable will jump 0.1 inches or a 15,000-volt cable for 0.25 inches.
- The electric flux travels farther than this, but isn't concentrated enough to be dangerous.
- This is a major risk, so engineers are *constantly* redesigning cable to offset this.

The insulation level determines how long until the ground fault can be cleared before it destroys the cable.

- 100% level means it will clear within 1 minute because it can't handle the higher stress and voltage.
- 133% level means it can't exceed 1 hour, and is often the standard even with a well-grounded system.
- 173% level means it could be indefinite, meaning the insulation may *never* fail even with a ground fault.

The risks of ground faults can come from overheating.

- It's not uncommon to calculate the amperage heat requirement, but forget that grounding also generates amperage, which can push the cables past their heat threshold.

To prevent ground faults, many places where there may be an undesirable conductor present (e.g., a bathroom, construction site) have ground fault circuit interrupters (GFCIs) that kill the flow of electricity within 1/40 of a second when the wire has a surge from a ground fault (i.e., exceeding 5 milliamperes). There are also arc-fault devices designed for larger voltage systems.

## Cabling

[Each cable is designed](engineering-electrical-cables.jpg) with several factors in mind:

1. An attempt to minimize resistance to allow a channel of unrestrained current
2. Weather-resistance to maintain the cable (e.g., waterproofing, heat)
3. Shielding to prevent the cable from causing risks to others
4. Risks from degradation to the environment (e.g., lead).
5. In the case of [signals](computers-networks.md), shielding to prevent interference *with* the conduit (e.g., electromagnetic).

Cables are, therefore, composed of several components:

- Conductor, which carries the current
  - Often copper or aluminum (copper is better but expensive, aluminum is worse but cheaper)
    - Copper is also [economically](money-economics.md) volatile as a commodity, so it's harder to [scope out projects](mgmt-2_projects.md) at scale.
    - Aluminum also tends to form oxide that interferes with current, which becomes an effective insulator.
      - One practice for crimping is to wire brush the oxidation, then apply an oxide inhibitor (usually zinc) that breaks it down.
    - It's not preferable to use both, since aluminum expands faster than copper, but dual-rated cables can work if necessary.
  - The strand configuration has a few major approaches:
    - The design is about occupying less space to send as many amps as possible, with the tradeoff coming in flexibility and cost
    - Solid: one continuous spool of metal
    - Stranded: multiple strands together
      - Bunched: no particular arrangement
      - Unilay: multiple layers twisted in the same direction
      - Rope Lay: Unilay, but woven into a mega-twist
        - This is the most flexible arrangement relative to size
      - Concentric: multiple layers twisted, with each layer twisted in opposite directions
      - Compressed: pushes the cables closer together without as much separation
      - Compact Round: separate cables, but pressed against each other to make a solid-like shape
        - This is necessary especially for aluminum to increase conductivity
- Insulation, which protects the conductor
- Insulation shield, which protects the insulation
  - There is also often a drain wire to ground the shielding
- Further, higher-voltage like Medium Voltage (MV) and High Voltage (HV) have a few more protective elements:
  - Strand shield for each individual strand (in multi-cable)
  - Semi-conductor, which help dissipate high voltage that can build up across the line
    - There can be air in-between strands, but it's not a good insulator.
      - Slowly, a cable will eat away and literally vaporize insulation, which creates a ground fault.
    - By extruding a semi-conducting layer that is in contact with the strands, it effectively creates a Faraday cage to prevent insulator decay.
  - Metallic shield, which works to inhibit arc flash
    - This accomplishes several things
      1. Confines the dielectric field within the cable
      2. The voltage stress within the dielectric is distributed symetrically on a radial axis
      3. It limits [radio](engineering-radio.md) interference
      4. There's a lower risk of shock
      5. It gives a return for short circuit current in the event of a failure
      6. it gives a neutral return path for concentric neutral cables (where the neutral cables are on the outside of the cable)
  - Jacket, which further separates the cable from its environment
    - It doesn't add much electrical value whatsoever, but protects from water damage.
    - If the jacket, and nothing else, is damaged, it can use any unrated electrical tape to resolve it.

There is a contentious question about installing ground cables on one side or both sides.

- The problem is that additional grounds create additional heat within the circuit and therefore create more cable decay.
- A 3-conductor setup will certainly benefit from a ground on both sides.
- However, a case can be argued that a single-phase current only needs one ground, especially if it's a very long run.

Besides [patience and a good attitude](success-5_persevering.md), good cable preparation requires several important factors:

- Have a working familiarity with the tools.
  - This includes keeping the blades sharp.
  - If using specialty tools, set the blade depth on a scrap piece of cable.
- Understand the kit you're working with.
  - This may take a few minutes of reading the instructions, but can save a lot of problems.
- Understand the environment you're working with.
  - This usually means scoping out if you'll need to make any special arrangements.
- Cutback dimensions are critical, so check your math twice before cutting.
- Crimp the lug or connector correctly.

## Cable repair

Before anything, make sure EVERYTHING is powered off.

- Double and triple check, since it can be fatal.

With some exceptions *never* splice a cable.

- Terminating may have to happen, but new construction should avoid splicing at all costs because it sabotages the integrity of the cable over time.

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

## Electricity and biochemistry

Our [body systems](body-systems.md) are connected with electricity.

- The nervous system is a series of well-refined electrical signals.
  - The heart, as part of the cardiovascular system, is maintained by consistent electricity.
- The heart itself, however, also has a "little brain" of 40,000 neurons, which serves to generate and read a small electromagnetic field
  - We have a built-in ability to detect electromagnetism, and that reading directly resonates with our ability to identify [spiritual warfare](spiritual-warfare.md).

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

Batteries are built into *many* objects (e.g., laptops, scales) without an off switch and simply a timer for [design reasons](engineering-design.md). However, every single piece of technology *needs* a physical switch that can kill the connection to the battery. Otherwise, the latent stray electricity can create [break-fix](https://adequate.life/fix/) headaches later.

One of the newest developing technologies for batteries is called a hydrogen fuel cell. The concept is essentially the same as a battery, with a few modifications:

1. The anode and cathode are separated only by a polymer electron membrane (PEM), which only allows positively charged ions to travel through it.
2. On the cathode side, oxygen is fed into the system.
3. On the anode side, a catalyst (such as platinum) splits hydrogen molecules into protons and electrons.
4. The electrons travel through an external circuit as a battery output.
5. The hydrogen protons travel across the PEM and bond with the oxygen, producing water (H~2~O), then move out of the system.

One significant issue with hydrogen fuel cells is in finding a reliable and affordable source of pure hydrogen for the inputs.

## Solar and wind

Since solar and wind energy are effectively unlimited, many people feel it's the future of energy. However, they both come with issues.

Wind power, in particular, has several problems:

- Wind is, by its very nature, volatile, so over-generation with reliable and extreme battery storage is critical.
- The biome heavily affects wind flow, so most places don't have a great setup for it unless they're in a plain or well-placed gorge.
- Since wind power is literally one of the destroying elements of nature, it will also wear down the [turbine](engineering-engines.md).
- Whenever a part fails on the turbine, the region downwind can have parts and fluids spread across it for *miles*.

Solar power also has a biome issue (needs plenty of sunlight) and is also volatile (needs nice weather), though it's far less violent on the parts.

- The problem with solar panels, though, is that dust can often set on the panels and requires constant cleaning.
- Further, solar panels are very expensive to make, so they become very expensive to replace when they fail.

However, the future viability of solar, as well as the general culture that accompanies [autonomous living](home-homestead.md), has created solarpunk culture around rigging up all sorts of interesting arrangements with solar cells.
