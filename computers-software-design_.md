
There's a distinct difference between front-end and back-end development, though it can sometimes blur:

- "Front-end" development is making code to build out a [user experience](engineering-design.md), often on the [internet](computers-sofware-webdev.md).
- "Back-end" development is working heavily with [databases](database.md) and [algorithms](computers-programming-algorithms.md), typically with lots of [math](math-cs.md).

## Mindset

Anyone working with code must have a few specific skills:

- Able to see a logical pattern from start to finish (which is largely trainable, especially with puzzle/coding games).
- Understand [math concepts](math-cs.md) (mostly the basics, since code is *always* working with math).
- [Creativity and imagination](mind-creativity-how.md) to see the product and [how the user will interact with it](engineering-design.md).
- The ability to mentally visualize the large-scale image of what their software will do.

When designing code, there are several levels of thought that a programmer has to vacillate back-and-forth between:

1. "Syntax" - the code itself, which consists of various commands and "variables".
2. "Idiom" - an [algorithmic](computers-programming-algorithms.md) structure that the code builds into for most tasks.
3. Design pattern - large-scale time-tested solutions to common code problems.
4. Architecture - the large-scale structure of the software system, including how all the subsystems and "modules" connect.

All of this takes *way* more time than any non-developer could realize.

- It takes time to plan and think through things, and most of that planning is part of a [creative process](mind-creativity-how.md) with a [logic-based](logic.md) implementation.
- Frequently, the implementation isn't always easy to put in place. This is especially true in [large](groups-large.md) or [badly managed](https://trendless.tech/your-job-sucks/) organizations, for a wide variety of reasons.
- The layers of complexity involved across various systems can often create a productivity approach of "yak shaving", or performing seemingly unrelated tasks that all contribute to the long-term goal of a functioning software package.

## Tools

Designing software requires a few key tools:

- A [version control](computers-software-versionctrl.md) system (such as Git).
- An [IDE](computers-software-ide.md) that highlights code and helps [debug](computers-software-redesign.md), among many other things.
- Beyond the IDE, a "plaintext" editor for small modifications (e.g., Windows Notepad, Linux gedit, macOS TextEdit w/ PlainText in Preferences).
- A [cloud platform](computers-distsys-cloud.md) to host apps and "infrastructure" for "end users".

## Design

There are 3 major types of programs, and their type determines how to approach designing it:

1. Completely abstracted programs that work with clear and simple specifications (e.g., adding 2 numbers).
2. Completely abstracted programs with complicated specifications that need the computer to work through many things (e.g., playing chess).
3. Programs that directly interact with the environment and are measured by their feedback (e.g., an alarm clock app).

In practice, every high-quality software will at least *somewhat* abide by the Unix philosophy, meaning it will do 1 thing well and send out a [standardized](standards-computers.md) flow of text information. Even when it's not strictly followed, complex software can be atomized as consisting of multiple smaller software programs.

No matter what someone is designing, they need to keep a few large-scale ideas in place:

1. Because of Moore's Law (where technology doubles in capacity every 2-5 years), computers will be absurdly faster in a few years than they are right now. Thus, getting something with a few features on the market right now is better, and adding features and optimizations later will become progressively easier. There are only a few strange exceptions to this, such as [batteries](engineering-electrical.md).
2. Take advantage of [abstractions](understanding.md). Instead of building everything from scratch, focus on the element you want to get out the door, and don't reinvent the wheel when you don't have to.
3. Many cases are common, but there will always be "edge cases". It's tempting to work on edge cases, but you'll make a *very* high-quality system by optimizing the *heck* out of the common case and disregarding the edge cases.
4. Optimize for parallel processing whenever possible. Treat a computer as [a Gantt Chart](https://en.wikipedia.org/wiki/Gantt_chart) on nanosecond-based projects instead of merely as a single task list: some things need to be performed in sequence, while others can be performed at the same time.
5. Optimize by "pipelining" tasks. Make each function do 1 thing, and divide that thing into as many steps as reasonably possible. This allows for things to scale easily, and each operation can be simple and quick.
6. Guess and start working now with what you can. With technology, it's almost always better to start and edit the results later than to wait until you know for sure, though [that's not always true](entrepreneur-7_exit-cs.md).
7. [Memory](computers-memory.md) works in a hierarchy, and it's either fast or plentiful. While programmers want fast, cheap, and large memory, they'll need to trade off one of them. The capacity of various speeds determines the size of solvable problems. While the "cache" is a great workaround for memory limits, there are *always* hard tradeoffs between fast and large.
8. Computers need to be dependable, so make the systems "redundant" with multiple copies of everything. Use ECC, store results in different memory registers than inputs, have the software backup user data often, and verify anything downloaded with [checksums](encryption.md).

For each function, a programmer should design it first:

1. Issue analysis - identify the information that must be represented, and how the selected [programming language](computers-languages.md) will represent it.
2. Data definitions - define what data will go through it, and make a good variety of sample input [data](data.md).
3. Purpose definition - create a concise answer to *what* that function will compute, and define the steps that will create the result.
4. Functional examples - work through examples that show the function's purpose.
5. Function template - translate the data definitions into an outline of the function.
6. Function definition - fill in the gaps in the function template by using the purpose definition and sample data.
7. Testing - use the examples as tests and make sure the function passes all of them, which helps find all [errors](computers-software-redesign.md).
8. Document - after making the function, create [documentation](language-writing-documentation-cs.md) to clarify how to use the function, using sample data to give examples.

## Building

Usually, computer code has already been built, at least partially. Most developers consult [Stack Overflow](https://stackoverflow.com/) for 98% of their questions and copy-paste code, or search an online "repository", then "refactor" the code for their purposes. It's often not perfect, but works well-enough.

Many times, the software may create a "shim", which pulls from an API and somehow modifies that information before outputting it.

## Testing

To make less painful [errors](computers-software-redesign.md) (especially logic errors), good software development tests the code incrementally:

1. Break the task into distinct phases of what you want the computer to do.
2. Create each phase, then test it.
3. If you mess up, you know you only messed up that phase, since you know all the previous phases worked fine.
