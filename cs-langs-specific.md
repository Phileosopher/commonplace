
# Specific programming languages, in general

There are *thousands* of programming languages.

- In effect, anyone who feels like it's better to reinvent the wheel will create another programming language with their own semantic preferences.
  - This actually makes sense sometimes, especially if someone does something so frequently that creating syntactic sugar would make their life easier.
  - Other times, it's because highly intelligent people had an ideal they wanted to attain, without much consideration if it made sense.
- That's not to say it was all serious, and many programming languages were made [simply for the fun of it](cs-fun.md).

Actually usable programming languages need to solve actual problems. In particular, Frank Atanassow asked some very good questions about whether a new programming language is worth it:

1. What problem does this language solve? How can I make it precise?
   - Making it "cleaner" is not a solution.
   - Having a very small definable core has already happened with SKI.
2. How can I show it solves this problem? How can I make it precise?
   - It shouldn't just be to write programs, since the feedback cycle is too long.
3. Is there another solution? Do other languages solve this problem? How?
   - What are the advantages of my solution? of their solution?
   - What are the disadvantages of my solution? of their solution?
   - There is *always* more than one solution to a problem.
   - He addresses *many* known solutions in other languages that have worked, except for Java:
     - Prolog, ML, Haskell, Charity, Lucid Synchrone, OBJ, Erlang, Smalltalk, Epigram, Coq, HOL, LEGO, Nuprl
   - Further, Perl, Python, Ruby, PHP, Tcl, and Lisp are effectively the same language with different syntax.
4. How can I show that my solution cannot be expressed in some other language?
   - That is, what is the unique property of my language which is lacking in others which enables a solution?
   - Without an answer, the solution is a library in another language, *not* another language.
5. What parts of my language are essential to that unique property?
   - If those parts are only a few elements, then rip them out of the language and add them to an existing language and refactor mercilessly.
   - If the answer is "almost everything", you're most likely wrong.
