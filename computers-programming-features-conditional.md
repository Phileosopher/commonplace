
# Conditional statements

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

## Statement types

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

## Loops

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

## Recursions

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

## Making functions

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
