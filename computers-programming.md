
# Computer programming languages

Computer coding has a relatively long history compared to most other computer-based things. While Charles Babbage created [the difference machine](https://en.wikipedia.org/wiki/Difference_engine) in the 1820s, Ada Lovelace was the first "programmer".

Programming is giving a computer the instructions to reliably do things. This requires:

1. Getting [information](data.md) from some sort of input
2. Manipulating it, typically with a coded [algorithm](computers-programming-algorithms.md) stored in [memory](computers-memory.md)
3. Outputting it, storing it in [memory](computers-memory.md), or both (and sometimes manipulating the coded algorithm in #2!)

Technically, if you *ever* interact with a computer, you're programming it:

- Typing out a text message to a friend is programming the computer to send that message when you hit "send".
- Drawing in a paint program is updating the [screen](engineering-screen.md) with new images every time you drag the cursor, then saving to long-term storage when you hit "save".
- Playing any video/computer game is you pressing buttons, with *very* specific premade reactions in the program based on the timing of the buttons you're pressing.
- Using a key card or gate sensor is programming that computer to activate the mechanism to open the door or gate.
- If you design a website to make it look pretty, you're programming the computer to show that website to everyone else who will access it over the internet.

Computers store both their programs *and* their results in [memory](computers-memory.md). While this creates a tremendously versatile system, it also can be confusing because nothing else in reality conforms to this approach (imagine using construction equipment as part of a house's design, for example).

However, nobody considers someone editing a spreadsheet or playing Super Mario Bros. a programmer. "Programming" is implied as *changing* how programs behave.

Computers are the world's fastest idiots, and will do *exactly* what you tell them, without any common sense or survival impulse. Their absurdly fast speed permits them to do many detailed, boring things within a split second, but without naturally discovering the permutations that a small child would be able to infer. Even [machine learning](computers-ai.md) hasn't made a particularly intuitive computer, and therefore computer programmers are constantly necessary to [debug](computers-software-redesign.md), even after software has been developed.

Programming has layers of complexity based on how much information you're giving. The fewer the keystrokes, the more you're [trusting](trust.md) some other person did all the programming work already.

Each language is designed with codified rules ("syntax"), which are meant to convey some clear type of [meaning](meaning.md) ("semantics"). Most software development projects start with writing code that prints "hello world" to the [screen output](engineering-screen.md), and then becomes more complex from there.

## Machine language

At the bottom of the coding stack, there's a bunch of 0s and 1s. Machine code is the link between hardware and software.

Thus, machine languages must answer some very practical philosophical questions:

1. What sorts of stuff will it do, and what types of data will it process?
   - [Math](math.md), including things like floating-point math
   - [Logic](logic.md)
   - Flow control - specific conditions to go to a specific instruction
   - Heavy work - specific things like large-scale copying, multiplication, and long division
2. Where in the [memory](computers-memory.md) will it do those things?
3. Where will it output those things after it's done calculating it?

The more things it can do, the more it'll cost to make, since it needs more sophistication. However, calculations performed in hardware are typically much faster than running software to do it. Deciding machine code operations are a game of *many* tradeoffs.

The computer understands machine language, but only geeky people can work well with it. All those 0s and 1s make your eyes hurt after a while.

So, engineers use a symbolic language that "assembles" into machine code.

## Low-level language

At its core, programming *could* be machine code: just a bunch of 0s and 1s. But, that's tiresome, and hard to read, so they made [assembly code](computers-programming-assembly.md) that's easier to read.

Assembly code is shorthand for machine code. For example, 0100010101101110 can become "add r3 r2".

While it takes effort to make those 0s and 1s into symbols, it's *much* easier for programmers to type out instructions.

When the programmer is ready, they can run an "assembler" that converts the human-written instructions into the machine code.

One neat advantage of this setup is that people can label specific memory locations useful things, so "Mem[42]" can become "input1" or "runningtotal". Labels can make programming *much* easier, especially with a few hundred variables.

This code is almost completely "one-to-one correspondence", which means that one instruction gives one command, which will get tedious very fast. Plus, each computer has unique machine code, coded differently from the original people who made it, so its assembly language differs depending on the computer you're using.

But, assembly code is *also* tiresome. The computer takes 40 steps to do generally simple things. Plus, because each manufacturer has their rules, not every computer does *quite* the same thing with the same instructions.

To combat these shortcomings, most programmers employ a "high-level language".

## Enter high-level

So, programmers made (and make) high-level languages. These languages let you type 1 command that does dozens, hundreds, or thousands of "lines" of assembly code. When the programmer is done and runs it through a "[compiler](computers-compilers.md)" or interpreter, it converts it to assembly code, though it may use an "interpreter" that converts it to assembly code as the computer reads each line.

"High-level languages" come at a cost. Although you're making a "one-size-fits-all" code, it means the program won't always be optimal for specific hardware. As it progresses to being more high-level, it becomes less optimized and more user-friendly.

High-level languages can run on any computer that can compile the code, so you can write it on one computer and it'll work *anywhere*, so it's very convenient. That's worth the tradeoff for a little bit of slowness.

*Most* of your "programming languages" are high-level, including popular ones like Python or Java. They involve making commands that look like a jumbled mess of pseudo-English.

Frequently, [high-level languages](computers-programming.md) can define all sorts of reusable types, classes, and variables. Plus, high-level languages can include "libraries" and "frameworks" to make them even *more* useful.

*Right* above assembly code, we have C. C is so low-level that it often gets used interchangeably with assembly as "low-level" code. While it doesn't have all the cool features of most other high-level languages, it's technically high-level because it's human-readable. Rust is much newer, but also becoming popular. Even though it's technically high-level, some developers find it so close to assembly language that they think it's *low-level* language!

To work with high-level language, programmers usually use an "integrated development environment", or [IDE](computers-software-ide.md).

## No-code/low-code programming

You can do quite a bit these days without knowing how to type code ("syntax"). The platforms that do this are called no-code/low-code.

Many services are available for this. Because they're so convenient, they often charge for what they're doing compared to high-level programming.

While they're extremely convenient, they can only do relatively common computer stuff, since someone had to do the high-level programming for it.

Of course, playing a computer game or browsing the web is also programming, but it's so constrained by the software that it feels more like "interaction" than "programming". Interestingly, those roles are somewhat reversed because the computer actually makes *you* the (somewhat) reliable thing [following instructions](power.md)!

## User interface

The whole point of [software design](software-design.md), however is typically to assist people who *don't* know how to use computers. That's why they (usually) spend effort on making a slick and usable [UX](ux-ui.md).

This can range from [console commands](computers-cli.md), [the mouse or touchscreen](computers-mouse.md), and can even include [AI prompts](computers-ai.md)!

## Various languages

It's worth noting that each "lang" has its "use case", so none of them are technically "bad", though many of them are awkward for doing specific things. They all were designed for some reason or another, and so there's no *best* language until we start talking about [what it's used for](purpose.md).

With that said, it really boils down to personal preferences that each individual programmer prefers. Anyone who doesn't know how to program is, therefore, asking the wrong question, a bit like saying "what musical instrument should I learn?"

## Stacks

There are a few tech stacks that most developers tend to build out, and this stays the same no matter what language:

- A relatively lower-level OS-oriented language, often spun off from C (e.g., C++, C#, F#)
- An object-oriented language (e.g., Python, Java)
- A [database](database.md) language (e.g., MySQL)
- Front-end language (e.g., JavaScript)

The order of the stack learning doesn't really matter, outside of how challenging the language will be to pick up. Python and Java are easy to learn, but expertly working in Unix requires understanding C, and lots of system administration and "common gateway interface" (CGI) scripts are written in Perl.

Learning a second programming language is a fraction of the difficulty of learning the first, since you've already mastered the rigor of thinking in strictly computer-based reasoning.

There are 3 major high-level languages that arose before *all* the other languages:

- COBOL - a procedural language designed for business use, is still used in the majority of banking transactions because it's *very* fast
- Fortran - a language designed for heavier computations, has largely been outmoded by many other languages
- Lisp - a [mathematical](math-cs.md) implementation of computer logic, still exists through [a *wide* variety of implementations](https://en.wikipedia.org/wiki/List_of_Lisp-family_programming_languages).

As of 2019, the top languages on WakaTime were:

1. JavaScript (5,036,909 hrs)
2. PHP (2,695,295 hrs)
3. TypeScript (2,114,010 hrs)
4. Java (1,709,433 hrs)
5. Python (1,407,783 hrs)
6. Vue.js (1,142,832 hrs)
7. HTML (1,090,992 hrs)
8. C# (771,636 hrs)
9. SCSS (543,318 hrs)
10. JSON (541,879 hrs)
11. Ruby (533,978 hrs)
12. Kotlin (457,646 hrs)
13. JSX (451,577 hrs)
14. Go (418,271 hrs)

## Types

There are *many* languages, and they can be broadly classified by how they're used, but also the pathway between how written code converts to machine code (generally, [compiled](computers-compilers.md) versus interpreted) and how [primitives](https://trendless.tech/primitives/) are constructed into more advanced components.

### Assembly code

[Assembly](computers-programming-assembly.md) is a low-level language compiled by an assembler.

They're often the intermediate stage between a higher-level language and machine code, and tend to be proprietary to the [processor](computers-cpu.md) (e.g., AMD assembly code is different than Intel).

### Scripting languages

Many times, you'll want to run a [console command](computers-cli.md), and do it based on certain conditions. Most operating systems come with pre-built scripting languages:

- [Windows](computers-os-windows.md) has PowerShell, though it once used batch files.
- [Unix](computers-os-unix.md) generally uses bash, but has a wide variety of other ones (as is the nature of [open-source software](legal-ip-floss.md)).
- Most automation software (like [AutoHotKey](https://www.autohotkey.com/)) have their own smaller scripting language.
- Many languages like JavaScript and PHP qualify as scripting languages.

They typically are interpreted, and don't need [compilation](computers-compilers.md), and are comparatively simpler than other languages for the computer to understand.

### Procedural languages

Instead of working through conditional scripts, the language may perform a series of procedures before executing a program.

- Some languages like Go and Julia work procedurally.

### Functional languages

The functional language approach involves many tiny reproducible functions that have many types of uses, then stacking them together to build more complex programs.

- This doesn't mean that *only* functional languages have [functions](math-functions-cs.md), but that the function is the primitive for how the language is designed.
- Haskell and Scala are functional languages.

### Object-oriented languages

Object-oriented is designed around building and putting together collections of objects, which are then used as primitives for other aspects.

- In many ways, it reproduces how we interpret the rest of reality (e.g., assemble a brick, then use bricks to build a house).
- However, OO is *highly* controversial among advanced software developers because it can be highly inefficient with resources.
- Some of the most popular languages are OO, such as Java and Python.
