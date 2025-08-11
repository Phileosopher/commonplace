
# Quantum computers summarized

Each atom that defines all matter in the universe is made of a nucleus of protons and neutrons, along with electrons that circle around the atom. The protons have a positive charge and the electrons have a negative charge.

The chemical state of absolutely everything is programmed with these atoms. More or less protons create new atoms (e.g., hydrogen is 1 proton, helium is 2 protons), and more or less electrons creates an ionized atom.

Chemically, the movement of electrons can create elaborate results. For example, water (2 hydrogen and 1 oxygen atom) is very stable because the atoms share electrons.

There are *many* more components to [quantum science](science-quantum.md), but many of them are theoretical, disputed, move around constantly, or so niche that they don't apply to the scope of quantum computers.

## Computing

The transfer of electrons is what we call electricity. AC power is a back-and-forth motion, while DC is a chain-reaction domino effect of electrons. In that sense, we have been using a stable technology based on the limited knowledge we really have about electrons.

As long as we can find a reliable pattern, we can still build on it, even if we don't understand how it works or why.

## Quantum states

A quantum state is far more complicated than we often imagine, for two major reasons:

1. Superposition - until something has been measured, it exists in a strange unknown limbo state, where it is in all the states at once. As far as we know [scientifically](science.md), once a being perceives it, it distills down to its singular state that we are perceiving:
   - Object 1 may be in State A or State B, and it's in State A/B until it's somehow perceived.
2. Entanglement - many things are connected in strange, unrelated-seeming ways:
   - Object 1's determination of being in State A or State B will determine whether Object 2 is in State A or State B, even if no physical laws of the universe dictate this connection.

What we *can* prove is that light photons behave differently as either a particle when it's observed, and stays a wave when it's *not* observed. The big question is *how* this can happen. Some people allude to [God](god.md), others believe in [determinism](glossary-philosophy.md), some people think there's another reason like we're in a simulation or don't actually exist until we perceive it.

## Superposition computing

The theoretical possibility of a quantum computer has been around since a 1980 paper on a quantum Turing machine, and has been discussed since 1982. If it *were* to work, it would remove many of the limits of conventional computers, to the same effect that vacuum tubes' transition to silicon have created. In 1996, Lou Grover created an [algorithm](programming-algorithms.md) that could use quantum superpositions faster than conventional Turing-based ones. Specifically, it was better at searching an [unstructured database](database.md) than a conventional computer.

A quantum computer takes advantage of superpositions and entanglement to create computations. Quantum states can be channeled to create a unique type of computer that doesn't abide strictly by 0s and 1s. Instead, each quantum bit ("qubit") is sitting in a probable state (a "superposition") that has a *likelihood* of 0 or 1.

To work correctly, each qubit stays in a state of entanglement with other qubits. This creates a chain of interdependent quantum states. The combined likelihood of each of those quantum states literally doubles the number of probabilities for each new qubit, and those percentages of likely scenarios are what computer scientists are programming inside a quantum computer environment.

There are 5 major assembly code instructions for a quantum computer:

1. Measure - makes 1 qubit 100% certain, which also will radically change the other qubits and likely end the processing
2. Hadamard - based on the Hadamard matrix, changes the probabilities of the qubits
3. Phase - changes the probabilities differently
4. T - changes the probabilities a third way
5. CNOT - changes 2 qubits' probabilities at once

## Implementation

These qubits can be constructed from the relative locations of electrons, photons, or lots of other possible physical implementations, and there are options regarding what to use. The only universal requirement is that they're *not* measured until it's time to make a quantum state certain.

Quantum processing is managed by a "quantum processing unit" (QPU), which simply does what a controller CPU is telling it to do. It's worth noting that there's no real "hardware", but more that it's operating based on the rules that govern physics. The mind-blowing part is that the state will change simply from an observer.

Quantum computers will always be expensive because they require freezing environments below zero, so cooling it is a significant part of operating them. They also have a very "noise" rate that gets incrementally worse as the computer has more qubits.

Qubits are also *very* error-prone. There have been efforts to use additional qubits to correct for errors, but it's a generally fiddly experience because it's working with objects at the very edge of [our scientific understanding](science.md).

Quantum computers can perform dramatically more data than conventional binary machines. The way they do this is by performing *all* possible iterations of a dataset at runtime, rather than the sequential approach that binary computers use. For example, to find a matching database entry, conventional binary computers will sift through the database line-by-line, but a quantum [algorithm](programming-algorithms.md) will search *all* of them at once.

In that sense, all [large-scale parallel processing](computers-distsys-enterprise.md) needs can benefit significantly from quantum computers.

At the same time, there are limits:

- While it can *draw* information all at once, it will only be able to output it at the speed of the peripheral (i.e., sequentially). It may get rid of any slowdown in the pipeline *to* the peripheral, but won't speed up output.
- The noise rate becomes absurdly high after a certain point to where it's unworkable. The only way to fix that is by improving the quantum computers (which is hard when we barely understand why superpositions are what they are), and the only remedy is to run it many times and average out the results. Running a database of 1,000,000 entries into the quantum computer 5,000 times might be the same time and cost as running that same database through a large-scale [distributed system](computers-distsys.md) once.
- They can't run for long. As of 2022, they can only run 0.00009 microseconds reliably, which is where its [algorithm](programming-algorithms.md) processes all the data.
- It's difficult to create quantum entanglement states. As of 2021, getting triple-entanglement is possible (i.e., 3 qubits), but the scalability of a quantum computer comes in how many sequential qubits it can work with, and that gets harder for reasons which we haven't begun to comprehend.

Engineers are throwing all *sorts* of ideas at the wall to see if they can get quantum computers to work better:

- Light-based processing instead of electrical
- Superconductors that create wave-particle fields instead of working with particles directly
- Glass CPUs (or QPUs) instead of silicon
- Silicon-based qubits

Their motivation makes sense. If quantum computers could be made to be reliable and efficient, it's almost certain that they'd rapidly overtake conventional binary computers in terms of power and [memory](/memory/) capacity. At scale, they can run *millions* of times faster than a binary computer.

Until quantum computers can run more reliably and affordably, binary computers will stay with us. Even then, there will still be many use cases where quantum computers may not be the best fit.

## The same

On the back-end, a quantum computer will demonstrate an abstraction that allows for users to do the same thing as any other [large-scale](computers-distsys-enterprise.md) data management system.

In some ways, it's history repeating itself:

- The 1950s mainframe computers were various [algorithms](programming-algorithms.md) that piped through [assembly language](programming-assembly.md) and circuits, which then expressed through vacuum tubes onto peripherals like printers.
- The modern quantum computers are various algorithms that pipe through a wide variety of control modules to manage quantum states and correct errors, which express through qubits onto peripheral CPUs that process the information.

However, there are explorations into new components. One of them is a memory resistor (or "memristor") that can hold electrically activated [memory](computers-memory.md) even without any electric charge involved.

Since they're so expensive, many quantum computing systems will be [cloud-based](computers-distsys-cloud.md), where everything will pass into a quantum computer a long distance away, then the output will come back to a local computer.

## Not Useful Today

Later, we may see [high-level languages](computers-languages.md), [compilers](computers-compilers.md), [operating systems](computers-os.md), drivers, and peripherals that operate *strictly* on quantum computers. Currently, it's a [hyped trend](https://trendless.tech/trends/).

In fact, many quantum computer developers are already working on [programming](computers-languages.md) within the quantum computing field, even if there's not much hardware right now that can actually *run* the software. In effect, its abstraction is a very far extension of parallel processing.

However, quantum computers can become an immense source of [informational power](power-types.md). They'd be able to sift through [the unbelievably massive piles of accumulated data obtained by many corporations and governments](faang.md), and the people in power would have a tremendous edge in [whatever they wish to do](purpose.md). This could be a [major risk](mgmt-badsystems.md).

## Further Exploration

[Quantum Flytrap](https://quantumgame.io/) - a browser-based game that explores quantum physics

[Quantum Marble Maze](https://fiftysevendegreesofrad.github.io/quantum/) - a game that explores quantum physics

[Quantum Roulette and the Nature of Reality](https://freelanceastro.github.io/bell/) - a simple dive into quantum entanglement
