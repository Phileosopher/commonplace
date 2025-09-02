
Since computers advance so fast, all previous analysis and efforts were made in a different time period, so anything over a year old is the soft social science of history.

There's no universal ideal solution, but there are ideals for use cases. There are also more wrong solutions than right ones.

You only legitimately understand something either the third time you see it or the first time you teach it.

You'll never have all the information, so start the analysis as soon as possible and reconfigure often.

Make guesses when in doubt, guess in an emergency, but always clean up the mess later.

You're not as smart or experienced as everyone else in the industry. If your analysis says your prototype will run faster than Google, you may have invented a new [mathematical proof](math.md), but it's more likely you missed something.

Designing something better than requirements is completely uncorrelated to the final product's quality.

Requirements come from the ability to "do" things, no matter what engineering textbooks say.

The fastest way to solve something is often to throw out everything and start over.

### fixing things

[Hacking](hacking.md) and [coding](computers-programming-basics.md) is an analytical [creative](mind-creativity.md) art pursuing vague goals, so it's not worth taking failure personally.

### working

Don't use a company account to sign up for something if you plan to use that service longer than staying with the company ([which is *very* likely](/your-job-sucks/)).

Unless you enjoy the experience, only make a productivity-enhancing system if the work to do it takes less time than the time you save over a year.

### Trends

The unwashed masses don't understand computers, but they vote with their wallet, so the tech industry is run by the tyranny of the majority.

The people who build out the winning tech [trends](https://gainedin.site/trends/) are some random guy name Ronald who makes a Unix-based software package called "runk" that stands for "Ronald's Universal Number Kounter". Then, big names like Bill Gates and Steve Jobs streamline it and sell it at enormous profit.

### Wadler's Law

Wadler's Law on wiki.haskell.org

    In any language design, the total time spent discussing a feature in this list is proportional to two raised to the power of its position.

        Semantics
        Syntax
        Lexical syntax
        Lexical syntax of comments

    (In short, for every hour spent on semantics, 8 hours will be spent on the syntax of comments).

Similar to The Law of Triviality, Wadler's Law states what when designing a language, the amount of time spent on language structures is disproportionately high in comparison to the importance of those features.

### The Fallacies of Distributed Computing

Also known as Fallacies of Networked Computing, the Fallacies are a list of conjectures (or beliefs) about distributed computing, which can lead to failures in software development. The assumptions are:

    The network is reliable
    Latency is zero
    Bandwidth is infinite
    The network is secure
    Topology doesn't change
    There is one administrator
    Transport cost is zero
    The network is homogeneous

The first four items were listed by Bill Joy and Tom Lyon around 1991 and first classified by James Gosling as the "Fallacies of Networked Computing". L. Peter Deutsch added the 5th, 6th and 7th fallacies. In the late 90's Gosling added the 8th fallacy.

The group was inspired by what was happening at the time inside Sun Microsystems.

These fallacies should be considered carefully when designing code which is resilient; assuming any of these fallacies can lead to flawed logic which fails to deal with the realities and complexities of distributed systems.

### SOLID

This is an acronym, which refers to:

- S: [The Single Responsibility Principle](https://github.com/dwmkerr/hacker-laws#the-single-responsibility-principle)
- O: [The Open/Closed Principle](https://github.com/dwmkerr/hacker-laws#the-openclosed-principle)
- L: [The Liskov Substitution Principle](https://github.com/dwmkerr/hacker-laws#the-liskov-substitution-principle)
- I: [The Interface Segregation Principle](https://github.com/dwmkerr/hacker-laws#the-interface-segregation-principle)
- D: [The Dependency Inversion Principle](https://github.com/dwmkerr/hacker-laws#the-dependency-inversion-principle)

These are key principles in [Object-Oriented Programming](https://github.com/dwmkerr/hacker-laws#todo). Design principles such as these should be able to aid developers build more maintainable systems.

### The Single Responsibility Principle

[The Single Responsibility Principle on Wikipedia](https://en.wikipedia.org/wiki/Single_responsibility_principle)

> Every module or class should have a single responsibility only.

The first of the '[SOLID](https://github.com/dwmkerr/hacker-laws#solid)'
principles. This principle suggests that modules or classes should do
one thing and one thing only. In more practical terms, this means that a
single, small change to a feature of a program should require a change
in one component only. For example, changing how a password is validated
for complexity should require a change in only one part of the program.

Theoretically, this should make the code more robust, and
easier to change. Knowing that a component being changed has a single
responsibility only means that _testing_ that change should be
easier. Using the earlier example, changing the password complexity
component should only be able to affect the features which relate to
password complexity. It can be much more difficult to reason about the
impact of a change to a component which has many responsibilities.

### The Open/Closed Principle

[The Open/Closed Principle on Wikipedia](https://en.wikipedia.org/wiki/Open%E2%80%93closed_principle)

> Entities should be open for extension and closed for modification.

The second of the '[SOLID](https://github.com/dwmkerr/hacker-laws#solid)'
principles. This principle states that entities (which could be
classes, modules, functions and so on) should be able to have their
behaviour _extended_, but that their _existing_ behaviour should not be able to be modified.

As a hypothetical example, imagine a module which is able
to turn a Markdown document into HTML. Now imagine there is a new syntax
added to the Markdown specification, which adds support for
mathematical equations. The module should be _open to extension_ to implement the new mathematics syntax. However, existing syntax implementations (like paragraphs, bullets, etc) should be _closed for modification_. They already work, we don't want people to change them.

This principle has particular relevance for
object-oriented programming, where we may design objects to be easily
extended, but would avoid designing objects which can have their
existing behaviour changed in unexpected ways.

### The Liskov Substitution Principle

[The Liskov Substitution Principle on Wikipedia](https://en.wikipedia.org/wiki/Liskov_substitution_principle)

> It should be possible to replace a type with a subtype, without breaking the system.

The third of the '[SOLID](https://github.com/dwmkerr/hacker-laws#solid)'
principles. This principle states that if a component relies on a type,
then it should be able to use subtypes of that type, without the system
failing or having to know the details of what that subtype is.

As an example, imagine we have a method which reads an XML
document from a structure which represents a file. If the method uses a
base type 'file', then anything which derives from 'file' should be
usable in the function. If 'file' supports seeking in reverse, and the
XML parser uses that function, but the derived type 'network file' fails
when reverse seeking is attempted, then the 'network file' would be
violating the principle.

This principle has particular relevance for
object-oriented programming, where type hierarchies must be modeled
carefully to avoid confusing users of a system.

### The Interface Segregation Principle

[The Interface Segregation Principle on Wikipedia](https://en.wikipedia.org/wiki/Interface_segregation_principle)

> No client should be forced to depend on methods it does not use.

The fourth of the '[SOLID](https://github.com/dwmkerr/hacker-laws#solid)'
principles. This principle states that consumers of a component should
not depend on functions of that component which it doesn't actually use.

As an example, imagine we have a method which reads an XML
document from a structure which represents a file. It only needs to
read bytes, move forwards or move backwards in the file. If this method
needs to be updated because an unrelated feature of the file structure
changes (such as an update to the permissions model used to represent
file security)
then the principle has been invalidated. It would be
better for the file to implement a 'seekable-stream' interface, and for
the XML reader to use that.

This principle has particular relevance for
object-oriented programming, where interfaces, hierarchies and abstract
types are used to [minimise the coupling](https://github.com/dwmkerr/hacker-laws#todo) between different components. [Duck typing](https://github.com/dwmkerr/hacker-laws#todo) is a methodology which enforces this principle by eliminating explicit interfaces.

### The Dependency Inversion Principle

[The Dependency Inversion Principle on Wikipedia](https://en.wikipedia.org/wiki/Dependency_inversion_principle)

> High-level modules should not be dependent on low-level implementations.

The fifth of the '[SOLID](https://github.com/dwmkerr/hacker-laws#solid)'
principles. This principle states that higher-level orchestrating
components should not have to know the details of their dependencies.

As an example, imagine we have a program which read
metadata from a website. We would assume that the main component would
have to know about a component to download the webpage content, then a
component which can read the metadata. If we were to take dependency
inversion into account, the main component would depend only on an
abstract component which can fetch byte data, and then an abstract
component which would be able to read metadata from a byte stream. The
main component would not know about TCP/IP, HTTP, HTML, etc.

This principle is complex, as it can seem to 'invert' the
expected dependencies of a system (hence the name). In practice, it also
means that a separate orchestrating component must ensure the correct
implementations of abstract types are used (e.g. in the previous
example, _something_ must still provide the metadata reader
component a HTTP file downloader and HTML meta tag reader). This then
touches on patterns such as [Inversion of Control](https://github.com/dwmkerr/hacker-laws#todo) and [Dependency Injection](https://github.com/dwmkerr/hacker-laws#todo).
