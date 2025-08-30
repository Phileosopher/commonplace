
# Engine design

At its simplest, an engine is a machine that produces movement.

Except for rocket propulsion, most engines are designed to produce rotational energy to a few possible outputs:

- A "flywheel", which is a one-way gear that keeps spinning even when force isn't applied. This can usually translate to applied torque (e.g., a bicycle) or a transmission (e.g., most autos).
- An "alternator" that converts the kinetic energy into DC electrical energy that goes to a battery.

## Steam engine

The steam engine is a relatively straightforward assembly:

1. High-pressure steam comes in from boiling water, historically with coal.
2. A valve rod is timed to open an aperture that leads to one side of a cylinder with a sealed piston.
3. The force of the steam's pressure pushes the piston and creates motion that moves a cross-head, and the valve rod closes as the piston moves the cross-head.
4. At the end of the cylinder, there is an open exhaust port where the high-pressure steam vents out.

## Internal combustion engine

The internal combustion engine assembly has a very specific flow of energy:

1. Drive a small, well-timed, controlled explosion at the top of a "piston".
2. The force of the piston pushes a "connecting rod" that's bound to a "crank pin".
3. The crank pin is the handle connected to a "crank arm" and "shaft", and is part of an assembly called the "crankshaft".
4. The crankshaft directly applies rotational energy with the exterior of the engine.

An internal combustion engine assembles the pistons in an evenly balanced array (typically an even number), and that array gives a shorthand format. V8 means alternating in a V-pattern, I4 means 4 vertical pistons, and so on.

The four-stroke engine consists of 4 distinct phases for each piston:

1. Intake - as the piston drops, pass fuel in through an "intake valve".
2. Compression - intake valve closes and piston pushes the fuel up to increase the combustion's thermal efficiency.
3. Power - generate a spark through a spark plug (for gasoline) or heat through a glow plug (for diesel) that triggers the explosion, launching the piston downward (and also propelling the other alternate pistons on the array during their 1st stroke).
4. Exhaust - open the exhaust valve *after* the explosion, and the inertia of the piston pushes it out.

A two-stroke engine combines the engine into only two strokes and has fewer moving parts, though it's often only ideal for smaller engines:

1. Controlled explosion pushes the piston downward, with the exhaust naturally venting out without a valve.
2. Near the bottom of the piston's motion, a valve opens up to permit more fuel to come in, which pushes out the rest of the exhaust.
3. Piston returns back to the starting position from its inertia.

## Alternators/generators

Nearly *all* mechanical energy converting to electrical uses a simple principle in electromagnetism: spin a magnet near a low-resistance material like copper, and it'll generate electricity. The only difference is its source (e.g., wind, hydroelectric turbine).

A generator converts mechanical energy into AC or DC electrical energy, while an alternator is *only* AC. Alternators tend to be cheaper with fewer parts, while generators are more powerful.

There are 3 major components to generate a rotating magnetic field:

1. Rotating shaft - spins while force is applied, with an electromagnet in the middle of alternators.
2. Stator - a static ring around the outside of the rotor with coil windings that doesn't touch the rotor directly, has a stationary magnet in generators.
3. Brushes and other parts that generate magnetic field voltage.
4. If it's converting to DC voltage, a set of diodes that serve as one-way pathways for the current.
5. A voltage regulator that maintains the energy flowing into the power source to prevent it from overloading.

## Rocket engines

Rocket fuel is *highly* combustible, and most rockets are designed to ignite the fuel as quickly and efficiently as possible. While hobbyist rockets can work with short-circuited wires, most larger motors require some form of black powder to ignite from wires to create a self-sustaining burn.

For highly advanced rockets, they tend to need *extremely* advanced cooling through the outside of the engine. Otherwise, the entire assembly would burn up. Regulating the timing between launching and temperature regulation is a highly advanced feat of engineering.

Igniting the propellant is the largest challenge, and multi-stage rockets in space need additional effort. Often, many of them synchronize the ignition of the next stage *while* the previous stage is still attached.

## Jet engines

A jet engine design is a little less straightforward than a rocket's, but not by much:

1. At the front of a jet engine, it has a compressor that converts air into a high-pressure high-temperature gas, then combines it with jet fuel and ignites it.
2. The flaming flow of gas goes through a set of blades arranged as a turbine, which extracts energy from the gas, lowering its pressure and temperature and increasing its velocity.
3. As the hybrid air/fuel gas is expelled, the aircraft is thrust forward.

## Nuclear reactors

There are two forms of nuclear energy: fusion and fission. Fusion gathers energy from combining atoms, while fission gathers energy from splitting them and using the energy from released neutrons.

Fission energy typically uses uranium processed into small ceramic pellets and stacked into sealed metal tubes called fuel rods. A fuel assembly typically has 200 fuel rods, with a reactor core made of a few hundred assemblies.

The fuel rods are immersed in water to serve as both a moderator (to slow down the neutrons produced by fission and sustain the chain reaction) and coolant (to redirect the resulting heat). The heat produced by the fission turns the water into steam, which powers a turbine.

There are two forms of fission reactor:

- About a third of reactors are BWR (boiling water reactor), which directly runs a steam line to a turbine.
- Most reactors are PWR (pressurized water reactor), which keeps the water pressurized, with the outgoing water regulated with a pressure tank and the energy from the steam powering a steam generator. That steam generator maintains the reactor's pressure and sends its resulting steam through a turbine.

Fusion energy is a vastly different structure, though it's still shooting something into unstable isotopes to break off extra neutrons:

1. Direct high-powered lasers at a hydrogen isotope fuel capsules called deuterium and tritium encased in diamond.
2. The diamond surface blows off and creates a rocket-like implosion of the deuterium/tritium mix.
3. Under extreme heat and density, the atoms combine and create helium while releasing energy.

Fusion generation at scale is mostly theoretical, but the idea is that it can replicate the conditions of the sun on a tiny scale using magnets.

An alternative fusion generator is called a stellarator, which uses a series of magnet coils to keep a ring of plasma in place. The rotation of the plasma can then be harvested to generate energy.

Both fusion and fission require *highly* particular and volatile materials. Isolating the isotopes (a statistically unlikely occurrence in nature) requires using a vast network of centrifuges that scoop up the comparatively heavier isotopes from the rest, and it can take *months* to acquire small amounts of it.
