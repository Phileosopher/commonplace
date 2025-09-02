
# Assembly code explained

Assembly code is the lowest-level programming that any sane person will need. Instead of machine code (e.g., 1110010100010101), chunks of the code can represent much more intuitive ideas (e.g., add r1, r2).

Assembly code is an abstraction that allows people to write the machine language more easily, then runs it through an assembler to become binary information.

- Its information is referred to as a "one-to-one relationship" because it's 1 line of code for 1 instruction.
- By contrast, higher-level languages (like [Python or JavaScript](computers-languages.md)) can have 1 line of code carry out *many* instructions.

It's worth noting computer hardware never sees *anything* but machine language (0s and 1s), so assembly code and the assembler are by *far* the most bare-bones portion of anything related to computers.

[Higher-level languages](computers-programming-basics.md) must run through a compiler first to become assembly code, *then* convert through an assembler that converts it to binary. The system flows information through a distinct process:

1. The user puts in information via the input (e.g., double-click on the Microsoft Word icon)
2. That information is converted to text code (C:\>word.exe)
3. Run the machine code that had been compiled from the high-level language into assembly code and then assembled.

It's worth noting that most troubleshooting and [debugging](computers-software-redesign.md) involves getting below the higher-level elements to view everything from a different perspective.

The cycled logic of what an assembler actually *does* is relatively similar to a compiler:

1. Read the next assembly language command, skipping irrelevant white space and comments.
2. Break out the commands into the fields it's made of, based on syntax rules.
3. Look up the binary code for each of those fields by consulting a table.
4. Combine those codes into a single machine language command.
5. Output that machine language command.

The relatively simple nature of an assembler means assembly code is *very* easy to mess up: transpose a period or mistype a letter, and the code won't work. Higher-level languages have plenty of [spell-checking and debugging](computers-software-redesign.md) to compensate for this.

## Operations

A few types of operations are *always* in a machine language:

- Arithmetic operations - doing all sorts of [math](math.md).
- Logical operations - working with [logic](logic.md).
- Flow control - directing where the CPU should place or retrieve information, also known as "addressing".

However, the hardware can also have many additional features.

- Many features simply make the computer faster by the hardware performing tasks instead of software (e.g., long division, advanced logical calculations, long [number width](computers-memory.md)).
- Some features improve the ability to work with specific [data types](data.md) (e.g., floating point arithmetic).

## Flow Control

[CPUs](computers-cpu.md) follow instructions, exactly to the letter. They start at the first instruction, then move to the second, and so on. They'll keep going until they're told otherwise.

"Flow control" is telling the computer to do something else instead, expressed in machine/assembly language in 2 ways:

- Unconditional jumps - makes the CPU jump to a specific instruction, no matter what.
  - Very useful for making "loops" to have it do the same thing over and over.
- Conditional jumps - makes the CPU jump to a specific instruction only if the memory satisfies a specific condition.
  - This allows computers to work with specific information.
  - Conditional jumps define how people can [feel](mind-feelings.md) defines a "[computer](computers.md)".

Combined, unconditional and conditional jumps let a computer work tirelessly on a task, then jump to the next. It continues indefinitely until it's powered off or commanded to stop.

Each task is more-or-less structured with this particular format:

1. Instruction 1
2. Instruction 2
3. Instruction 3
4. Conditional jump to 6 if something equals something else
5. Unconditional jump to instruction 1
6. (carry on to other things)

This system allows for endless possibilities, since you can make programs jump to *wherever* you want them to go.

To make things easier and more convenient for the human programmers, specific places in memory can be given labels. Thus, instead of jumping to "Memory Location 42561" you can just jump to "sum".

## Addressing Modes

"Addressing" is the reference number to specify where the CPU should look. It varies by the manufacturer, but all computers always have a few modes of addressing:

- Register - directly interact with 2 registers inside the [CPU](computers-cpu.md).
  - add R1, R2
- Direct - address the register and directly address the memory address.
  - add R1, M[150]
- Indirect - address the register and indirectly address the memory address with a name already loaded into the CPU.
  - add R1, TotalSum
- Immediate - use a constant with the register.
  - add 73, R1

## Syntax

Generally, assembly code follows [normal code procedure](computers-programming-basics.md) like white space not being counted and comments, though the one-to-one relationship means it's far more rudimentary than higher-level languages.

Assembly code, compared to higher-level languages is *very* rudimentary:

- Assembly code does *not* have quick-access libraries to pull from. It's all binary information, meaning any repetitions must be manually coded.
- There are no "[variables](computers-programming-basics.md)" in the conventional sense, since there are only binary memory registers that can get duplicated as separate references.
- Arrays get lost in the memory shuffle, since they're encoded as whatever memory locations they were at.
- Pointers are somewhat hard to decipher because they're referencing memory registers.

## Usually Unnecessary

Most tech people will *never* need to program in assembly code:

- You'll never typically need to examine machine or assembly language unless you're writing [compilers](computers-compilers.md) or trying to make your computers *insanely* precise (such as a satellite going beyond the solar system).
- For must use cases, you can usually get by with the C or Rust [programming language](computers-languages.md).

However, understanding assembly code is a *very* important "soft skill" for computer science, since it lets people "see the way computers see".
