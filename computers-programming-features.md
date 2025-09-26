
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

## Functions

A function is a like a box of [logical](logic-cs.md) statements that build into a process:

1. Information goes into the function.
2. The computer follows a bunch of rules to fiddle with the information and "call" more functions.
3. The function "exits" when it reaches the end.

The function is "callable" by referencing its label. Sometimes the function does things, and sometimes it doesn't, but it's all depending on what's in the box. If you haven't noticed, every function is a type of mini-API.

Often, the functions have "clauses", which are optional conditions that you can use in the language. Like clauses in language, they can dramatically change what the function does or how it does it.

Usually, the function in most languages will use brackets to separate ideas like "()", "{}", "<>", and "[]". Other languages will use colons (":") or white space (i.e., spaces and tabs) instead. Functions do, however, have certain universals:

1. Usually a function label, whatever you want to call it.
   - If a function is "called" from a previous function, it'll often have an underscore in front of it (e.g., "check_scores" will call "_check_scores").
2. The "arguments" that go into the function, usually closed by brackets. This can include "global variables" (stored in the [operating system's](computers-os.md)[memory](computers-memory.md) "heap") or new, temporary "local variables" (stored in the program's "stack").
   - Some functions don't take in arguments and just use "()" instead, which can be useful when you want to do a *lot* of stuff based on another set of conditions.
3. The things the function does, also usually closed by brackets. If it's a simple function, this one won't be needed.
   - Sometimes the function will "return" out for use later, other times it'll pass information on to something else or "print" the information as output.

There are quite a few mundane functions in nearly *every* high-level language:

- PRINT - spits out information to a screen. It's usually the first thing any programming class teaches. It's called "print" because it *used* to go to a printer before someone attached [screens](engineering-screen.md) to computers!
- CONCATENATE - adds multiple strings and other variables together. It's pretty much how a computer can say "You win! 18 points!"
- Arithmetic functions that perform [math](math-cs.md).
- Conditional statements, as explained below.

Functions are condensed versions of the [many, many tasks a CPU must do](computers-cpu.md). The "print" function, for example, saves a *ton* of trouble by condensing the entire process of outputting to a [screen](engineering-screen.md) down to a simple command. In technicality, *any* command that isn't machine/assembly code is a function!

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

## Conditional statements

The CPU recognizes [conditional jumps](computers-cpu.md), which form into conditional statements. In short, conditional statements are logical "statements" that run when certain "conditions" are met. This creates "branching" in the instructions to separate the flow into multiple logical outcomes.

When "foo" is 0 and a conditional statement specifies that "foo" must be greater than 2, that statement won't run and the program will advance to the code right after the statement.

Conditional statements run when the [logic](logic-cs.md) is true, represented by a Boolean 1. There are a variety of operators to specify the logic:

- < less than
- > greater than
- <= less than or equal to
- >= greater than or equal to
- AND for when both conditions are met
- OR at least one of the conditions are met
- XOR *only* one of the conditions are met

In one sense, *everything* in programming is merely "if" and "for" loops:

- An "if loop" only activates when a condition is met (e.g., x=1).
- A "for loop" empowers iterations (e.g., x=1 and y=3, do something and add 1 to x, in this case repeat until x=4).

### Statement types

IF statements are *extremely* frequent in functions. They test the condition, then run the code inside it if it's true, or gloss over if if it's not true. They don't tend to permit [alternative interpretations](image.md) of "true", either.

- IF (*statement that must be true*) {

  *stuff to do if it's true*

  }

ELSE-IF statements are sub-IF statements. They're IF statements that run if the statement before it didn't work out.

ELSE statements are a catch-all at the end. If, for whatever reason, none of the IF statements worked out, ELSE is there to do something useful.

It's generally a good practice to always have an ELSE at the end of a function to catch any weird stuff that didn't fit with the rest. Smart hackers can exploit the absence of an ELSE function, since they'll be able to send code *outside* the function without an ELSE condition.

If you want to have *many* IF statements, you can create a type of [demultiplexer](computers-alu.md) with a SWITCH function. It'll break out into case "a", "b", and so on as much as necessary. In this case, the ELSE function is labeled "default:"

Functions are callable, just like variables. Plus, functions can sit inside other functions (function-ception!). This can sometimes get confusing for new programmers.

As a general rule, 1 function does 1 purpose. Some people don't follow this rule and make life very miserable for all the other programmers.

### Loops

By telling the computer to "jump" back to a previous instruction, you can assemble a loop, or "iteration". Loops are *really* useful at doing a repetitive task many times, since you can instruct it once and it'll keep going until you want it to stop.

FOR loops are excellent for doing something a specific number of times, and have several parts:

1. an integer value: i = 0
2. a conditional statement to keep doing the loop: i < 20
3. something to do to that integer *after* the instructions of that loop: i++

Thus, a FOR loop is "syntactic sugar":

- for (i = 0, i<20, i++) {*code to run over and over*}

It's worth noting that computers are stupid enough to easily destroy themselves with a loop that runs forever and ever. Always, always, *always* have an exit to a FOR loop!

WHILE loops run indefinitely until a certain condition is met:

- while (x == y) {*code to run over and over*}

FOR loops are meant to end, but WHILE loops can run forever. They're really useful for constantly [refreshing the screen](engineering-screen.md) many times a second or for keeping programs open all the time in an operating system. If you want to make it run forever, just put "while (true)".

DO-WHILE loops are unusual variants for a specific use. Sometimes you want to do something once, *then* check if conditions are met.

### Recursions

One of the most difficult concepts to understand in programming is when functions "recurse". Basically, instead of repeating a loop over and over until some conditions are met, programmers can make the *function* repeat itself inside over and over:

- recursionFunction (n) {

  recursionFunction (n+1);

  }

In the above example, this will keep going forever, opening up a new function with that adds 1 to the original number until the computer crashed or you stopped it:

The rule for loops applies to functions: *always have an exit*:

- recursiveFunction (n) {

  if (n<100) {

  return n;

  } else {

  return (n + recursiveFunction(n+1))

  }

  }

The reason people have a hard time getting their head around it is because nothing in reality works quite like this. When we say a sentence, that sentence doesn't make any sense when it references itself:

- This statement is false.
- The previous statement is only true if this statement is true.
- All the statements here make no sense, and are therefore false.

In practice with computers, however, their stupidity is their saving grace. Here's how it would look if you used 1 as the argument:

- recursionFunction (1) {

  recursionFunction (2) {

  recursionFunction (3) {

  recursionFunction (4) {

  recursionFunction (5) {

  (on and on forever until your computer broke)

What that means is that when something *does* satisfy the recursion (also known as the "base case"), all those functions will fulfill and exit in reverse order. So, in the above case, it'll use 5,4,3,2,1 in that order if it was fulfilled.

If the [memory](computers-memory.md) gets full from all those recursions, it's called a "stack overflow" error.

Recursions are extremely useful because you can apply them wherever you can find a pattern across [data](data.md).

### Making functions

It's less work to just [import a library](computers-programming.md), but sometimes you have to get your hands dirty and make your own functions.

Creating functions is relatively simple:

1. Depending on the language, the scope of the function. This determines which types the function will work with.
2. What the function will return, if applicable.
3. The name of the function.
4. The arguments for the function, which will always be in parentheses.
5. The code for the function.

- public int thatFunction (int num1, num2) {

  print(num1 + num2);

Then, when you call the function, it returns whatever you drop into the arguments:

- thatFunction (5, 4) \\ prints 20

Whatever type of variable you specify must get fed into the function. This is also true for return types as well. For example, you can't drop a string argument into an integer-based function, and can't return a float if the function is returning an integer.

If the function is supposed to return something, it *must* return *something*! This can be easy to forget if the logic doesn't have an ELSE condition. The best thing to do in that case is to drop a "return" command at the end of the function that makes it clear you failed.

## Data structures + loops

Each variable can hold 1 value. While you *could* theoretically use 1 value to hold "MilkEggsCheese", it's better to spread those across multiple variables. An "array" is an ordered list, and can hold variables, constants or other arrays. It's one of a wide variety of available [data structures](data-structures.md).

FOR EACH functions allow loops over arrays. The loop will run across the array, but the EACH part asks for a condition. If the condition is met that time, the computer will run the instructions in the FOR EACH function.

This can be *really* useful for lots of data. You can count the data that matches something, or make the computer do something related to where that data is stored (like modify the previous values or increment the data).

## Additional reading

[freeCodeCamp](https://freecodecamp.org/) made [a high-quality 2-hour video](https://www.youtube.com/watch?v=zOjov-2OZ0E) that I nearly copied verbatim.
