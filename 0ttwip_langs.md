
This is a comparison of programming languages. The thrust of it is to give an approximation of the strengths and weaknesses of that language compared to other programming languages.

It's worth noting that each "lang" has its "use case", so none of them are technically "bad", though many of them are awkward for doing specific things. They all were designed for some reason or another, and so there's no *best* language until we start talking about [what it's used for](https://gainedin.site/purpose/).

With that said, it really boils down to personal preferences that each individual programmer prefers. Anyone who doesn't know how to program is, therefore, asking the wrong question, a bit like saying "what musical instrument should I learn?"

## Stacks

There are a few tech stacks that most developers tend to build out, and this stays the same no matter what language:

- A relatively lower-level OS-oriented language, often spun off from C (e.g., C++, C#, F#)
- An object-oriented language (e.g., Python, Java)
- A [database](/database/) language (e.g., MySQL)
- Front-end language (e.g., JavaScript)

The order of the stack learning doesn't really matter, outside of how challenging the language will be to pick up. Python and Java are easy to learn, but expertly working in Unix requires understanding C, and lots of system administration and "common gateway interface" (CGI) scripts are written in Perl.

Learning a second programming language is a fraction of the difficulty of learning the first, since you've already mastered the rigor of thinking in strictly computer-based reasoning.

There are 3 major high-level languages that arose before *all* the other languages:

- COBOL - a procedural language designed for business use, is still used in the majority of banking transactions because it's *very* fast
- Fortran - a language designed for heavier computations, has largely been outmoded by many other languages
- Lisp - a [mathematical](/math/) implementation of computer logic, still exists through [a *wide* variety of implementations](https://en.wikipedia.org/wiki/List_of_Lisp-family_programming_languages).

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

* * * * *

## Types

There are *many* languages, and they can be broadly classified by how they're used, but also the pathway between how written code converts to machine code (generally, [compiled](/compilers/) versus interpreted) and how [primitives](/primitives/) are constructed into more advanced components.

### Assembly code

[Assembly](/assembly/) is a low-level language compiled by an assembler.

They're often the intermediate stage between a higher-level language and machine code, and tend to be proprietary to the [processor](/cpu/) (e.g., AMD assembly code is different than Intel).

### Scripting languages

Many times, you'll want to run a [console command](/consoles/), and do it based on certain conditions. Most operating systems come with pre-built scripting languages:

- [Windows](/windows/) has PowerShell, though it once used batch files.
- [Unix](/unix/) generally uses bash, but has a wide variety of other ones (as is the nature of [open-source software](/floss/)).
- Most automation software (like [AutoHotKey](https://www.autohotkey.com/)) have their own smaller scripting language.
- Many languages like JavaScript and PHP qualify as scripting languages.

They typically are interpreted, and don't need [compilation](/compilers/), and are comparatively simpler than other languages for the computer to understand.

### Procedural languages

Instead of working through conditional scripts, the language may perform a series of procedures before executing a program.

- Some languages like Go and Julia work procedurally.

### Functional languages

The functional language approach involves many tiny reproducible functions that have many types of uses, then stacking them together to build more complex programs.

- This doesn't mean that *only* functional languages have [functions](/functions/), but that the function is the primitive for how the language is designed.
- Haskell and Scala are functional languages.

### Object-oriented languages

Object-oriented is designed around building and putting together collections of objects, which are then used as primitives for other aspects.

- In many ways, it reproduces how we interpret the rest of reality (e.g., assemble a brick, then use bricks to build a house).
- However, OO is *highly* controversial among advanced software developers because it can be highly inefficient with resources.
- Some of the most popular languages are OO, such as Java and Python.

* * * * *

## BASIC

While BASIC has largely gone out of style, it was designed to be a syntactically easy language, and most of its future iterations (e.g., QBasic, Visual Basic) keep that simplicity.

In the spirit of that simplicity, Scratch is probably the best programming language for easy accessibility. It uses a convenient [GUI](/graphics/) that makes it *very* [kid-friendly](https://adequate.life/parenting-2/).

## C

One step above [assembly code](/assembly-code/). Has been the go-to for making *very* fast code for quite a long time. It was originally created to work with [Unix](/unix/).

It can be a bit painful to work with, especially with things like pointers, and that's why other C-based languages have tried to fill in the gaps.

There are a wide variety of C-based languages:

- C++ was originally called C with Classes. It has many [features](/prog-features/) that C does *not* have built-in. It has historically been one of the most popular [game development](/game-dev/) languages for a very long time. C syntax is *not* a good idea to write in C++.
- Objective-C is Apple's attempt at improving on C, so it's often the fastest way to program for iOS. All valid C code is valid Objective-C code.
- Java and JavaScript were both inspired by C, but have their own spinoffs that make them entirely different.

However, C by itself is the perfect language for working with very hardware-leaning applications, such as the [Raspberry Pi/Arduino](/pi-arduino/) or [robotics](/robotics/).

## C#

C# is Windows' attempt to improve on Java, and has very little to do with C technically (though it shares the name). Because of how easy it is to program compared to straight C, many high-end [games](/game-dev/) are programmed in C#.

## C++

At first, Bjarne Stroustrup wanted an extension of the C language, but it eventually evolved into its own high-level language.

While the language is general-purpose, it's frequently a heavily-used language for [audio engineering](/speakers-mic/). It is *very* powerful, though it can sometimes be unwieldy.

One of its downsides is that it's *very* complex, and those complexities make it difficult to communicate algorithms to other developers or quickly modify code.

## COBOL

One of the oldest languages alongside FORTRAN, Lisp and ALGOL, created in 1959.

The language processes information *fast*, which is why most financial transactions (about 70%) are *still* written in COBOL.

Syntax for COBOL is designed to be human-readable code, as opposed to the mathematically-based language of the time. Most languages have done more and better since then.

Its awkwardness (it doesn't do recursion) along with its general unfashionable nature make it *very* hard to find good COBOL programmers.

## G-code

A specific programming language for physical implementations of a computer (e.g., [robotics](/robotics/), [automotives](/3d-printer/), [3D printers](/3d-printer/)) that uses Cartesian coordinates to indicate precisely where an object should begin or end.

The code is very low-level: almost like C, but for physical space.

Further reading:

- [G-code Explained](https://howtomechatronics.com/tutorials/g-code-explained-list-of-most-important-g-code-commands/)

## Java

Java was made by a committee, and has *tons* of unnecessary syntax. However, it's still the industry standard for many domains (such as Android apps).

It exists mostly because it's been existing, though it's waned in popularity somewhat now that other languages like Rust have become more powerful and easier to work with.

## JavaScript

JavaScript is the language of the internet, though the internet-based version of it is technically ECMAScript. HTML is the skeleton and CSS is the appearance of the internet, and JavaScript are the muscles.

In that sense, because of the internet's ubiquity, just about everything that *can* be written in JavaScript will eventually be written in it (Atwood's Law), and JavaScript will stick around as long as [the internet](/web-dev/) exists.

Further, JavaScript runs a huge chunk of [game development](/game-dev/) and most front-end content for phones.

JavaScript's only connection to Java is that it was a marketing move. Java was hot at the time, so calling something JavaScript might get some programmers interested. It obviously worked, and has now outpaced Java in popularity.

## Julia

While Julia isn't as popular as the others (mostly because it's newer), it's a heavily math-based language, so it's very useful for scientific data management.

## Kotlin

While Kotlin isn't nearly as popular as most other languages on this page, it's still a good alternative for Android apps if you hate Java.

## Lisp

While many other languages were designed to fix a problem, Lisp was formed strictly as a theoretical mathematical model. For that reason, it ends up being relatively timeless and somewhat of an abstraction unto itself, a bit like C.

For that reason, there are a *lot* of languages in the Lisp family: Maclisp, MDL, Scheme, Common Lisp, [Emacs Lisp](/ide/), [GNU Guile](/unix/), Clojure, Racket, and Hy.

## Lua

Since Lua's "interpreter" is written in C, it exists as another variant of C.

## MATLAB

MATLAB was designed to work with [statistical](/stat/) analysis. For that reason, it's very powerful at crunching probabilities and not useful for many other implementations.

## Python

A high-level language. It's universally accepted, and dominates all across the world. Like BASIC once was, it's great for beginners to learn, but comes with drawbacks that beginners won't really care about.

The philosophy behind Python is to create something elegant, simple and clear.

It's very, very powerful, and the language of choice for heavy-math implementations like [machine learning](/ml/). But, it doesn't scale well:

- The packaging is bad when there are lots of cross-cutting dependencies.
- There's no concurrency designed into the language.
- The code ends up becoming heavily typed, since it's not the dominant form of expression in the language.

This is barely noticeable in a small project, but becomes incredibly painful in a [large production system](/enterprise/). People working on small projects love it, but not the ones who have to manage millions of lines of code.

In practice, Python is great for [creating an MVP](/freelancing/) as fast as possible, but bogs down and traps developers later.

R

R, like MATLAB, was designed to work with [statistical](/stat/) analysis. For that reason, it's a bit limited for broader purposes, but very powerful at crunching probabilities.

## Rust

Rust is meant to be a more memory-safe version of C++. It has become widely supported in most [operating systems](/os/), and has now become a faster language than C.

## Smalltalk

A little project language that had some uniquely interesting features. For this reason, many languages after it have borrowed from it.

## Swift

Swift is the language for Apple software, more than anything else, especially iOS apps.
