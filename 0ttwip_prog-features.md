
There are a plethora of features that a programming language can do. Often, with enough diligence, *any* programming language can contort itself to do just about anything, but some are easier to program certain logical operations into it than others.

## Tradeoffs

Deciding how to assemble the high-level logic is complicated, and based heavily on what the language is used for:

- Do you want short commands for specific purposes that require a wide variety of words or hard-to-write stuff that's insanely powerful?
- Do you want it to use copy-pasted boilerplate "callable" procedures, or do you want it to group things as "objects" which each have special rules (i.e., object-oriented vs. procedure-oriented)?
- Do you want to maximize the computer's efficiency with lower high-level languages (e.g., C) or want something super easy to learn (e.g., Ruby on Rails)?

There's no "one-size-fits-all" solution for a high-level language. But, some languages *do* work better than others for various applications.

Many languages are general-purpose (e.g., Python, Java, C++). They pretty much do anything you want, though how *well* they do them can vary spectacularly. For example, Java is better at game and web development, Python is better at data analysis and scripting, and C++ is better at making applications and [system programs](/os/).

Scripting/extension languages (e.g., Perl, PHP, JavaScript, Ajax) don't need to be compiled, so they're *super* portable and can run almost anywhere, which is why websites run well with them. They're about as high-level as languages get without becoming [no-code programming](/prog/).

Some languages are really, *really* specific (e.g., HTML, CSS). Think of them as only existing in a certain "box" of possible solutions. If you want to write web-enabled content, HTML is your friend, but will abandon you when you want to make a fun game.

One noteworthy reality is that there's no hard "box" around any of the languages. For example, someone *could* make a computer game with CSS and HTML, but they'd make better use of their time and effort to simply learn JavaScript or C. But, some people do it for fun or are insanely stubborn.

## Libraries

There are a *lot* of people who work with computers. The beauty of [specialization](https://gainedin.site/specialization-cities/) is that someone can build something, then someone else can use it later. Unlike real-life tools, code doesn't really cost money to reproduce.

Thus, many programmers have created "libraries" of [functions](/functions/). By using a library, programmers can create vastly complex things with only a few lines of code. It's basically a big block of commands that you can add to your language that save the time of building the functions yourself.

For any popular language, most typical things have *many* libraries to choose from. Unless you have an edge case, there's probably a library for that.

Beyond [debugging](/software-redesign/) and writing code, a programmer spends a *lot* of time researching to find library packages that make their life easier.

Importing a library is easy. Just call the language-specific function that usually has the word "import", specify the package you want to download, then specify the classes of that package you want (or just put "*" to import everything in that package).

Generally, you should only import the classes you'll use. The more you have to import, the more computations the computer has to run through, and the slower your program gets. In a small program, it's not a big deal, but a large program can get noticeably slow and make the users' lives suck.

## Frameworks

Unlike libraries, frameworks are more constrained. They're often designed for specific-use.

## Namespaces

Everything needs a unique name. Otherwise, it's impossible to distinguish things apart. If you know 3 people named "Mark", then it's hard to know which Mark you're talking about. The old convention was to say "Mark the Miller", "Mark the son of John", or "Mark of the Reilly clan". It got so convenient that we just simplified it to "Mark Miller", "Mark Johnson", and "Mark O'Reilly".

A "namespace" is exactly that: a space for names. It lets you use the same name in different places without the headache of making something different every time.

- If you poke around in your [files](/files/), you'll notice that you can have "Documents/Family/mom.jpg" as well as "Documents/September/mom.jpg" and "Documents/mom.jpg" at the same time.
- Every website under ".com" is pointing to a completely different location than the ".gov" or ".net" version of it.

While programmers can often define a namespace, most languages come with a standard set of names, and libraries often add many more names and namespaces. It's important to know what those namespaces and names are, since you could be reinventing the wheel when someone else already made a namespace or create errors by making the same namespace.

## MapReduce

To work with large sets of data, there's a reliable two-step model for processing them:

1. Make a "mapping" of information/functions to each item of data:
   - e.g., the dataset [1,2,3] can have a mapped function of (x => x * 2), which makes [2, 4, 6].
2. Reduce the information step-by-step:
   - e.g., to add [7, 8, 9], reduce 7 and 8 to 15, then reduce 15 and 9 to 24.
