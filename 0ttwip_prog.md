
Programming is giving a computer the instructions to reliably do things. This requires:

1. Getting [information](/data/) from some sort of input
2. Manipulating it, typically with a coded [algorithm](/algorithms/) stored in [memory](/memory/)
3. Outputting it, storing it in [memory](/memory/), or both (and sometimes manipulating the coded algorithm in #2!)

Technically, if you *ever* interact with a computer, you're programming it:

- Typing out a text message to a friend is programming the computer to send that message when you hit "send".
- Drawing in a paint program is updating the [screen](/screen/) with new images every time you drag the cursor, then saving to long-term storage when you hit "save".
- Playing any video/computer game is you pressing buttons, with *very* specific premade reactions in the program based on the timing of the buttons you're pressing.
- Using a key card or gate sensor is programming that computer to activate the mechanism to open the door or gate.
- If you design a website to make it look pretty, you're programming the computer to show that website to everyone else who will access it over the internet.

Computers store both their programs *and* their results in [memory](/memory/). While this creates a tremendously versatile system, it also can be confusing because nothing else in reality conforms to this approach (imagine using construction equipment as part of a house's design, for example).

However, nobody considers someone editing a spreadsheet or playing Super Mario Bros. a programmer. "Programming" is implied as *changing* how programs behave.

Computers are the world's fastest idiots, and will do *exactly* what you tell them, without any common sense or survival impulse. Their absurdly fast speed permits them to do many detailed, boring things within a split second, but without naturally discovering the permutations that a small child would be able to infer. Even [machine learning](/ai/) hasn't made a particularly intuitive computer, and therefore computer programmers are constantly necessary to [debug](/software-redesign/), even after software has been developed.

Programming has layers of complexity based on how much information you're giving. The fewer the keystrokes, the more you're [trusting](https://gainedin.site/trust/) some other person did all the programming work already.

Each language is designed with codified rules ("syntax"), which are meant to convey some clear type of [meaning](https://gainedin.site/meaning/) ("semantics"). Most software development projects start with writing code that prints "hello world" to the [screen output](/screen/), and then becomes more complex from there.

## Machine language

At the bottom of the coding stack, there's a bunch of 0s and 1s. Machine code is the link between hardware and software.

Thus, machine languages must answer some very practical philosophical questions:

1. What sorts of stuff will it do, and what types of data will it process?
   - [Math](https://gainedin.site/math/), including things like floating-point math
   - [Logic](https://gainedin.site/logic/)
   - Flow control - specific conditions to go to a specific instruction
   - Heavy work - specific things like large-scale copying, multiplication, and long division
2. Where in the [memory](/memory/) will it do those things?
3. Where will it output those things after it's done calculating it?

The more things it can do, the more it'll cost to make, since it needs more sophistication. However, calculations performed in hardware are typically much faster than running software to do it. Deciding machine code operations are a game of *many* tradeoffs.

The computer understands machine language, but only geeky people can work well with it. All those 0s and 1s make your eyes hurt after a while.

So, engineers use a symbolic language that "assembles" into machine code.

## Low-level language

To code the machine, engineers can use an abstracted language called "assembly code".

Assembly code is shorthand for machine code. For example, 0100010101101110 can become "add r3 r2".

While it takes effort to make those 0s and 1s into symbols, it's *much* easier for programmers to type out instructions.

When the programmer is ready, they can run an "assembler" that converts the human-written instructions into the machine code.

One neat advantage of this setup is that people can label specific memory locations useful things, so "Mem[42]" can become "input1" or "runningtotal". Labels can make programming *much* easier, especially with a few hundred variables.

This code is almost completely "one-to-one correspondence", which means that one instruction gives one command, which will get tedious very fast. Plus, each computer has unique machine code, coded differently from the original people who made it, so its assembly language differs depending on the computer you're using.

To combat these shortcomings, most programmers employ a "high-level language".

## High-level language

High-level languages can run on any computer that can compile the code.

*Right* above assembly code, we have C. C is so low-level that it often gets used interchangeably with assembly as "low-level" code. While it doesn't have all the cool features of most other high-level languages, it's technically high-level because it's human-readable. Rust is much newer, but also becoming popular.

*Most* of your "programming languages" are high-level, including popular ones like Python or Java. They involve making commands that look like a jumbled mess of pseudo-English.

Frequently, [high-level languages](/prog-features/) can define all sorts of reusable types, classes, and variables. Plus, high-level languages can include "libraries" and "frameworks" to make them even *more* useful.

Each of the commands can frequently include dozens, hundreds, or even *thousands* of specific actions for the [processor](/cpu/). When the programmer is done and runs it through a "[compiler](/compilers/)", it converts it to assembly code, though it may use an "interpreter" that converts it to assembly code as the computer reads each line.

## No-code/low-code programming

You can do quite a bit these days without knowing how to type code ("syntax"). The platforms that do this are called no-code/low-code.

Many services are available for this. Because they're so convenient, they often charge for what they're doing compared to high-level programming.

While they're extremely convenient, they can only do relatively common computer stuff, since someone had to do the high-level programming for it.

Of course, playing a computer game or browsing the web is also programming, but it's so constrained by the software that it feels more like "interaction" than "programming". Interestingly, those roles are somewhat reversed because the computer actually makes *you* the (somewhat) reliable thing [following instructions](https://gainedin.site/power/)!

## User interface

The whole point of [software design](software-design.md), however is typically to assist people who *don't* know how to use computers. That's why they (usually) spend effort on making a slick and usable [UX](ux-ui.md).

This can range from [console commands](/console/), [the mouse or touchscreen](/mouse/), and can even include [AI prompts](/ai/)!
