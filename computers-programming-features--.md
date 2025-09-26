
NOTE: This page is a bit wobbly, and will probably be the top-level aspect of things that are in other pages
- concurrency
- functional, object oriented, etc
- apis
- libraries and frameworks vs vanilla install
- garbage collection? memory management?

NOTE: ADD DESCRIPTIONS OF THE FOLLOWING:
- Object-oriented
- Types
    [Things I Was Wrong About: Types | Hacker News](https://news.ycombinator.com/item?id=24604943)
    [Things I Was Wrong About: Types  - Sympolymathesy, by Chris Krycho](https://v5.chriskrycho.com/journal/things-i-was-wrong-about/1-types/)
    [Sympolymathesy, by Chris Krycho](https://www.chriskrycho.com/)
- Classes
    [Class (computer programming) - Wikipedia](https://en.wikipedia.org/wiki/Class_(computer_programming))

freeCodeCamp dev quiz - Prog Features - Python
- what is a dictionary in Python?
    - The values of a Python dictionary can be either mutable or immutable. Both will work correctly.
- In the context of Python, PEP means Python Enhancement Proposal. (to documentation?)
- What is a [Data definition language](https://en.wikipedia.org/wiki/Data_definition_language)?
- f-strings are string literals prefixed with 'f' and 'F' in Python.
- The in operator is a membership operator in Python. It can be used to check if a value is in a sequence or not because it returns True if the value is in the list and False if it is not in the list.
[6. Expressions - Python 3.10.4 documentation](https://docs.python.org/3/reference/expressions.html#operator-precedence)
    - The floor division operator in Python is //. This operator performs a mathematical division that rounds down to the nearest integer.
- In Python, it is recommended to use 4 spaces per level of indentation.

freeCodeCamp dev quiz - Prog Features - JS
- What is a Promise in JS?
- JavaScript and Node.js have a huge package ecosystem and was relatively easy to program in. Node.js is also very fast, and works well at scale. Large websites like Netflix and LinkedIn use it as a primary language.
- The JS map() method creates a new array filled with the results of calling a function (provided within the method) on every element in the array that calls the method.
[Let's talk about semicolons in JavaScript](https://www.freecodecamp.org/news/lets-talk-about-semicolons-in-javascript-f1fe08ab4e53/).
- Prototypes provide the means for JavaScript objects to inherit features from other objects.
- var is hoisted with the default value of undefined while let, const and classes are hoisted but are in the Temporal Dead Zone(TDZ) until the declaration is executed.
- An event loop first empties the Microtask queue and once it is empty it starts to empty the Callback queue.
- How does JS use constructor elements to construct elements in a class? [Object Oriented Programming in JavaScript - Explained with Examples](https://www.freecodecamp.org/news/how-javascript-implements-oop/)
- push vs pop, shift vs unshift
- When you declare variables with var, they can be re-declared within their scope.
- TB: [10 Awesome JavaScript Libraries You Should Try Out in 2021](https://www.freecodecamp.org/news/10-javascript-libraries-you-should-try/)
- The three types of scope in JavaScript are global, function and block.
- || is the logical OR operator in JavaScript.
[Nullish coalescing operator (??) - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing_operator)

Frameworks/Libraries
- Buy a house, or cautiously build your own. What's the difference between a framework and library? I've had this discussion with developers at work and meetups, and the core idea boils down to this. You tell libraries what to do, frameworks tell you what to do. Framework Upsides Generally speaking

## Classes vs Interfaces

A boy scout has badges that merits them to do certain things, such as
cooking, swimming, starting a campfire, canoeing, etc. The boy scout
troop doesn't care how they were able to do these things (i.e. swimming
with the breast-stroke, back-stroke, etc.) as long that they meet the
specification for it (being able to move in the water by a certain,
controlled movement of the body while staying afloat). Each boy scout
can have zero or many badges, meaning they are certified to do each of
the things merited by the badge.

Despite that, they are still boy scouts. Every boy scout is allowed
to attend their periodic meetings, wear their uniform, etc… A boy
scout doesn't need a badge to swim. However, they can't go river-rafting
unless they have a swim badge.
Edit: a swim badge can't swim by itself. It is merely an indicator that the boy scout it's attached to can swim.

#### The boy scout is the class, and the swim badge is an interface it implements.

Every object that of the class that is instantiated have the same
functions (i.e. attending periodic meetings, uniforms, etc). If the
class implements an interface, the class MUST have be able to perform
the functions specified in the interface (i.e swimming, canoeing). Some
classes can't be used in certain parts of your code unless they
implement that interface (i.e. going river rafting requires swim
badges).
Edit: An interface is an abstraction, so it can't be instantiated. (A badge by itself can't swim.) To sum up, an interface is a contract a class must follow in order for a class to implement it.

Interfaces and classes behave differently in different languages (My
example is from what I know in C# with generics). I suggest you read the
documentation to your language carefully.

Interfaces can also be used to collect objects from different classes (they act like a data type).

You could collect all boy scouts who can swim, regardless of their
nationality, gender, age, etc. and go river rafting. You don't need to
know anything about the individual boy scouts, but you know that each of
them is able to swim.

# articles - pointers

[138: Pointers - explain xkcd](https://www.explainxkcd.com/wiki/index.php/138:_Pointers)

# articles - prog features

[6 interesting features in programming languages](https://blog.frankel.ch/six-interesting-features-programming-languages)

[Fernando Rubbo  ](https://fernandorubbo.blogspot.be/2013/03/feature-toggles-good-or-bad.html)
(2013) Feature toggles: good or bad

[Martin Fowler](https://www.martinfowler.com/bliki/FeatureToggle.html)
(2010) FeatureToggle
feature toggles as an alternative to evil feature branching

[Paul Hammant](https://paulhammant.com/blog/branch_by_abstraction.html)
(2007) Introducing Branch By Abstraction

[Martin Fowler](https://www.martinfowler.com/bliki/FeatureBranch.html)
(2009) FeatureBranch
and dangers of feature branching

[Jim Bird](http://swreflections.blogspot.be/2014/08/feature-toggles-are-one-of-worst-kinds.html)
(2014) Feature Toggles are one of the worst kinds of Technical Debt

[Matthew Skelton](https://blog.softwareoperability.com/2013/04/08/lets-talk-about-operational-features-not-non-functional-requirements/)
(2013) Let’s Talk About Operational Features, not Non-Functional Requirements

# guides - jmp

[Let's write a setjmp | Hacker News](https://news.ycombinator.com/item?id=34760828)
[Let's write a setjmp](https://nullprogram.com/blog/2023/02/12/)

# guides - type introspection

[Type introspection - Wikipedia](https://en.wikipedia.org/wiki/Type_introspection)
