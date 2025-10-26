
# The features of programming languages

There are a plethora of features that a programming language can do. Often, with enough diligence, *any* programming language can contort itself to do just about anything, but some are easier to program certain logical operations into it than others.

## Tradeoffs

Deciding how to assemble the high-level logic is complicated, and based heavily on what the language is used for:

- Do you want short commands for specific purposes that require a wide variety of words or hard-to-write stuff that's insanely powerful?
- Do you want it to use copy-pasted boilerplate "callable" procedures, or do you want it to group things as "objects" which each have special rules (i.e., object-oriented vs. procedure-oriented)?
- Do you want to maximize the computer's efficiency with lower high-level languages (e.g., C) or want something super easy to learn (e.g., Ruby on Rails)?

There's no "one-size-fits-all" solution for a high-level language. But, some languages *do* work better than others for various applications.

Many languages are general-purpose (e.g., Python, Java, C++). They pretty much do anything you want, though how *well* they do them can vary spectacularly. For example, Java is better at game and web development, Python is better at data analysis and scripting, and C++ is better at making applications and [system programs](computers-os.md).

Scripting/extension languages (e.g., Perl, PHP, JavaScript, Ajax) don't need to be compiled, so they're *super* portable and can run almost anywhere, which is why websites run well with them. They're about as high-level as languages get without becoming [no-code programming](computers-programming.md).

Some languages are really, *really* specific (e.g., HTML, CSS). Think of them as only existing in a certain "box" of possible solutions. If you want to write web-enabled content, HTML is your friend, but will abandon you when you want to make a fun game.

One noteworthy reality is that there's no hard "box" around any of the languages. For example, someone *could* make a computer game with CSS and HTML, but they'd make better use of their time and effort to simply learn JavaScript or C. But, some people do it for fun or are insanely stubborn.

## Libraries

There are a *lot* of people who work with computers. The beauty of [specialization](jobs-specialization.md) is that someone can build something, then someone else can use it later. Unlike real-life tools, code doesn't really cost money to reproduce.

Thus, many programmers have created "libraries" of [functions](math-functions-cs.md). By using a library, programmers can create vastly complex things with only a few lines of code. It's basically a big block of commands that you can add to your language that save the time of building the functions yourself.

For any popular language, most typical things have *many* libraries to choose from. Unless you have an edge case, there's probably a library for that.

Beyond [debugging](computers-software-redesign.md) and writing code, a programmer spends a *lot* of time researching to find library packages that make their life easier.

Importing a library is easy. Just call the language-specific function that usually has the word "import", specify the package you want to download, then specify the classes of that package you want (or just put "*" to import everything in that package).

Generally, you should only import the classes you'll use. The more you have to import, the more computations the computer has to run through, and the slower your program gets. In a small program, it's not a big deal, but a large program can get noticeably slow and make the users' lives suck.

## Frameworks

Unlike libraries, frameworks are more constrained. They're often designed for specific-use.

## Namespaces

Everything needs a unique name. Otherwise, it's impossible to distinguish things apart. If you know 3 people named "Mark", then it's hard to know which Mark you're talking about. The old convention was to say "Mark the Miller", "Mark the son of John", or "Mark of the Reilly clan". It got so convenient that we just simplified it to "Mark Miller", "Mark Johnson", and "Mark O'Reilly".

A "namespace" is exactly that: a space for names. It lets you use the same name in different places without the headache of making something different every time.

- If you poke around in your [files](computers-files.md), you'll notice that you can have "Documents/Family/mom.jpg" as well as "Documents/September/mom.jpg" and "Documents/mom.jpg" at the same time.
- Every website under ".com" is pointing to a completely different location than the ".gov" or ".net" version of it.

While programmers can often define a namespace, most languages come with a standard set of names, and libraries often add many more names and namespaces. It's important to know what those namespaces and names are, since you could be reinventing the wheel when someone else already made a namespace or create errors by making the same namespace.

## MapReduce

To work with large sets of data, there's a reliable two-step model for processing them:

1. Make a "mapping" of information/functions to each item of data:
   - e.g., the dataset [1,2,3] can have a mapped function of (x => x * 2), which makes [2, 4, 6].
2. Reduce the information step-by-step:
   - e.g., to add [7, 8, 9], reduce 7 and 8 to 15, then reduce 15 and 9 to 24.

## API

Every culture has its [jargon](jobs-specialization.md), and tech is no exception. One of the most frequently used words is API ("application programming interface").

The word API gets thrown around a lot, and it's a buzzword for "the rules that one computer/thing has to follow to interact with another computer/thing".

In practice, though, an API is an "abstraction" that gets all the clutter out of the way. You can enter information into it, and the computer does all its back-end stuff, and produces what you want at the end without all the extra access to the code.

It's the same way that a steering wheel is the API for a car, and you don't need to understand how it runs to operate it.

## Constants

A "constant" is something that doesn't move, and computers borrows the word from [algebra](math-algebra-cs.md). It could be the number 5, the word "blue", the *color* blue, the image of a puppy, or the laughter of a child.

However, while people treat the *universe itself* as a soft-ish constant, computers don't actually have "constants" outside of numbers. They're emotionless logic machines, so they don't assign philosophical value like us.

The way they're designed, a computer will drop out almost everything unless it can convert to [language](language.md) or [math](math.md).

To account for uncertain things, computers use variables to define the constants.

## Variables

The word "variable" *also* has its origins from [algebra](math-algebra-cs.md). But, in computers, it can be named almost *anything* instead of specific math concepts like "x", "y", or "Δ".

Programmers tell the computer to grab a piece of [memory](computers-memory.md) and call it whatever they want (within reason):

- burpNow = 5
- burpNow = "tires"

That variable can be whatever value you want, including nothing (aka, "null"). If it starts with a value, it's called an "initialized" variable. Otherwise, it's uninitialized.

- burpNow

An operating system can organize the [memory](computers-memory.md) to make referencing variables easier, programmers don't usually need to know about memory management when they're starting out. They just need to know what variables they're using and what's in the boxes.

Whenever the programmer wants that variable, the computer can "call" the variable with a "pointer":

- get burpNow

The pointer might be to an input or output value:

- clickStatus = mouse[0] (the first mouse button becomes "clickStatus")
- screen[135,0] = pixel135 (pixel135 becomes the 135th pixel value on the screen)

Often, variables can point to *other* variables ("dual-pointed variables"):

- name = "Bob"
- firstName = name

Dual-pointed variables make managing multiple things with the same original value easier.

Variables are useful, but computers are stupid enough that they need to know beforehand what's in the variable. Thus, engineers created "types" of variable [data](data.md).

Two common variables in many programming examples are "foo" and "bar" as simple placeholders.

## Syntax

Each computer language (its "syntax") is unique. Thus, while they're *all* [logical](computers-alu.md), they each structure that logic a little differently. Not following syntax rules makes the computer spit out errors, and is a huge part of [debugging](computers-software-redesign.md).

There's a *general* syntax that span across many of the the languages, but each one has its own quirks. If people are used to a specific language, they'll often hate transitioning to another one strictly because of those quirks.

Often, the left thing will be the result, with the information on the right specifying what to do with it:

- newVariable = oldVariable + 5

Depending on the language, spaces and tabs either don't matter or demarcate hierarchical instructions. Same goes for capitalization.

### Shortcuts

All [high-level programming is technically a shortcut](computers-programming.md), so since software developers often have to write the same thing repetitively, it makes sense to make *more* shortcuts. Software development is a type of industrious laziness because of this, and they create all sorts of "syntactic sugar" to sweeten the experience of repetitive work.

*Very* often, programmers tick numbers up or down by one:

- thatNumber = thatNumber + 1
- thatNumber = thatNumber - 1

INSTEAD:

- thatNumber ++
- thatNumber--

Other times, they just want to do basic math and use the new number instead:

- thatNumber = thatNumber + 5
- thatNumber = thatNumber - 5
- thatNumber = thatNumber * 5
- thatNumber = thatNumber / 5
- thatNumber = thatNumber [% 5](math-cs.md)

INSTEAD:

- thatNumber += 5
- thatNumber -= 5
- thatNumber *= 5
- thatNumber /= 5
- thatNumber %= 5

### Equality

If you use one equals sign, you're telling the computer that the variable on the left now equals whatever's on the right:

- numberValue = 5

So, if you want to see if something is the same, you use the equals sign twice:

- numberValue = 5
- 5 == numberValue (the computer will give a [Boolean](logic-cs.md) of TRUE)

Because of [data types](data.md), there's a *huge* difference between equality (=) and identity (≡). High-level languages like Python and JavaScript are smart enough to convert data types before calculating with it ("type coercion"). But, sometimes you don't want it to do that.

To prevent the high-level language from automatically changing the data type, you can use "===", "is" or some other variation depending on the [programming language](computers-languages.md):

- 5 == "5" (returns the Boolean of TRUE)
- 5 === "5" (returns the Boolean of FALSE)

If a piece of data generally expresses to FALSE because it naturally rounds out to 0, it's "falsy". The values of 0, -0, NaN, undefined, "", false, and null are all falsy values. Otherwise, if the value has something in it, it's "truthy", which can include "0" or "false", an empty [array](data-structures.md), or an empty object.

Sometimes, you want something to *not* equal each other. NOT is often represented by "!":

- 51 != 51 (returns FALSE)
- 51 !== "51" (returns TRUE)

### Commenting

You may need to leave a note for yourself. Or, maybe you want to inform anyone editing the code later about something. You might want to clean up the code later and need to clarify that you have no clue how to parse the arcane monstrosity your Project Manager gave you.

Whatever the case, you'll need to comment on the code:

- <!--Each language does it differently,-->
- /*but the important thing*/
- //is that the computer will ignore
- ;;;whatever is in here when it
- #compiles or interprets everything

To make the comments easier to distinguish, the [IDE](computers-software-ide.md) usually turns the comments gray.

There are often single-line and multi-line variants of commenting. If you want to be *really* specific about certain things, you can often write the comments on the same line as the executed code.

## Naming conventions

Choosing names is one of the most difficult concepts in computer science.

For one thing, the programmer has to know what the program will do. Naming something TotalSum sounds like a good idea, until the software is working with multiple total sums. DataOutput sounds sensible, until it might connect with *another* data output. So, specificity is crucial.

Computers are pretty stupid, so variables and functions are case-sensitive. If you wanted to, you could assign *all* the variables and functions as separate things:

- THAT
- That
- thaT
- tHAt
- that

A programmer who is [debugging](computers-software-redesign.md) that abomination you made later, however, will kill you. So, to avoid an untimely cessation of a primary organ, programmers agree on naming conventions.

There are many awful ways to "define" things:

- hair color - two words, so it might be mistaken as a command
- haircolor - could be seen as a built-in command
- HaIrColOr - confusing to read and type again
- HAIRCOLOR - it better be a constant
- hairColor - it better be a variable
- haierColor - why did you mispell?

Back in the day, programmers used all-caps to delineate commands. This was when *everything* compiled to all-caps:

- PRINT I'm a little teapot
- EXECUTE short and stout
- WHILE I have a handle
- ELSE on what syntax is about

Now, programmers often use "camel case" or "Pascal case" or "bicapitialization", all in one word, no special characters like periods or commas. It separates out the words for easy reading, but it's still "one" word:

- hairColor
- HairColor
- headShapePlayerCharacter
- playerHitPointsAfterFirstBossButBeforeFinalBoss

If you have multiple words, many languages use the convention of "snake case":

- player_hit_points
- hat_color
- cheese_eaten

If you just need to use placeholder variables, most programmers use "foo" and "bar". Its history goes back to [MIT's Model Railroad Club](https://en.wikipedia.org/wiki/Foobar#History_and_etymology), because computers have always been cool.

## Data structures + loops

Once [conditional statements](computers-programming-features-conditional.md) are established, the information can become more complex.

Each variable can hold 1 value. While you *could* theoretically use 1 value to hold "MilkEggsCheese", it's better to spread those across multiple variables. An "array" is an ordered list, and can hold variables, constants or other arrays. It's one of a wide variety of available [data structures](data-structures.md).

FOR EACH functions allow loops over arrays. The loop will run across the array, but the EACH part asks for a condition. If the condition is met that time, the computer will run the instructions in the FOR EACH function.

This can be *really* useful for lots of data. You can count the data that matches something, or make the computer do something related to where that data is stored (like modify the previous values or increment the data).

## Additional reading

[freeCodeCamp](https://freecodecamp.org/) made [a high-quality 2-hour video](https://www.youtube.com/watch?v=zOjov-2OZ0E) that I nearly copied verbatim.
