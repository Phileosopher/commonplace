
# List of universal laws and axioms regarding technology

## General

Roosevelt's Law of Task Planning - Work with what you have, not with what you hope to have or might exist later.

Clarke's Third Law - Sufficiently advanced [technology](technology.md) looks the same as magic.

Kranzberg's First Law of Technology - Technology has no value of good, bad, or neutral.

Maes-Garreau Law - The nearest predictions about large-scale future technology tends to be right before the predictor imagines they'll die.

Technology Life Cycle - Every invented technology is first not that useful, then becomes more useful up to a point, then becomes less useful as other technology replaces it, until it becomes generally obsolete.

Van Loon's Law - Societies develop technology when they can't [make people do things for them](slavery.md).

## Dev/Design

Atwood's Law - If it can be, it eventually will be written in JavaScript.

Cupertino Effect - The stupidity of computers means they'll frequently override a common use case (like "cooperation") for an obscure one (like "Cupertino" instead of "co-operation").

de Saint-Exupery's Law of Design - A designer doesn't achieve perfection when there's nothing left to add, but when there's nothing left to take away.

DRY Principle / Don't Repeat Yourself - All pieces of information in a system must always have a single, clear, official representation.

Greenspun's Tenth Rule - Any sufficiently complicated C or Fortran program contains an ad hoc, informally specified, bug-ridden, slow implementation of half of Common Lisp.

- Morris' Corollary - This includes Common Lisp.

Kranzberg's Third Law of Technology - Technology breaks apart into "packages".

Liskov Substitution Principle - When inserted into a system, a subtype must be interchangeable with its parent type (e.g., if Type B is a subtype of Type A, then Type A can fit into everything that Type B fits into).

Miller's Law - All large-group discussions about a small software update will eventually include discussing giant redesigns, adding features, or replacing that software.

Semantic Meaning - things have an associated meaning that humans must interpret.

Separation of Concerns - Each thing should be separated by their specific designed [purpose](purpose.md).

Shea's Law - The most significant design improvements are in its interface, but are also the easiest to screw up.

Unix Philosophy - The best-designed computer software should do one thing well (like a building block), which will include sending out a standardized flow of text information.

von Tiesenhausen's Law of Engineering Design - To share your understanding, learn to draw, since the finished product for some reason always ends up looking like the concept art.

Zawinski's Law - Every program keeps expanding until it can read mail (i.e., long-form time-insensitive messages), or will be replaced by ones that can.

## Improvements/Debugging

Amdahl's Law - The improvement of any given component of a system will only make an effective improvement proportionally to how much it's used in that system.

Claasen's Law - Incrementally more technology means exponentially more [results](results.md).

Haitz's Law - Every decade, each LED's cost per lumen is divided by 10 and becomes 20 times more efficient.

Kernighan's Law - Debugging a program is twice as hard as writing it, so simple code is better than complex code.

Last Line Effect - Developers tend to make most of their errors in their last line of copy-pasted code.

Leaky Abstractions Law - Nearly all abstractions overlook at least some technical details that would make those abstractions more inefficient than a more complex solution.

Linus' Law - Given enough eyeballs, all bugs are trivial.

Premature Optimization Effect - About 97% of the time, the benefits of optimizing something aren't worth its potential gains.

## Hardware

IETF Motto - Be precise in what you send, flexible in what you receive.

Grosch's Law - The relative speed increase of a computer is the square of its relative increased cost.

Klaiber's Law - The silicon wafer's size proportionally dictates the largest diameter of ultra-pure water piping necessary for a semiconductor wafer factory.

Marconi's Law - The effective distance of an [antenna tower](engineering-radio.md) is approximately the height of the antenna squared.

Moore's Law - Computers become twice as powerful every 2 years, which compounds to 32x over a decade.

The only place where improvements in a chain of dependencies matter are on the slowest components.

The optimum is almost always somewhere in the middle in nature, so distrust assertions that the optimum on a graph is at an extreme point.

## System Growth

Cooper's Law of Spectral Efficiency - The maximum number of simultaneous flows of information across a medium doubles every 30 months.

[Hyrum's Law](https://www.hyrumslaw.com/) / Law of Implicit Interfaces - When there are enough [API](computers-programming-features.md) users, someone will have to maintain every single aspect of that API, irrespective of what a public [contract](people-contracts.md) indicates.

Koomey's Law - The number of computations for energy doubles every 1.57 years, which compounds to 100x over a decade.

Lindy Effect - The longer a technology has been around, the longer it will persist before becoming obsolete.

Metcalfe's Law - A system's value grows at about the square of the number of users in the system.

Wirth's Law - Over time, software gets slower faster than hardware gets faster.

## Distributed Systems

Brewer's Theorem / CAP Theorem - for any distributed data storage, only 2 of 3 guarantees are possible:

1. Consistency - every request returns the most recent data or an error.
2. Availability - every request returns data without an error, even if it's not the most recent.
3. Partition Tolerance - everything still works even when nodes fail.

- An addition is PACELC, which adds 2 variables in the case of node failure (E, for "else"):
  - Latency - partially-working systems can prioritize staying fast.
  - Consistency - partially-working systems can prioritize sending consistent data.

## Internet-Specific

1% Rule / 1-9-90 Rule / 89:10:1 Ratio - On a user-generated website (like a wiki) only 1% of people create content, another 9% contribute somewhat, while the other 90% only consume.

Brandolini's Law / Bullshit Assymetry Principle - The amount of energy required to refute lies is exponentially more than to create them.

Cunningham's Law - Instead of asking a question, the best way to get the right answer on the internet is to give the wrong answer.

Godwin's Law - As online discussions grow, it'll eventually guarantee comparing someone to Nazis or Hitler.

Lewis' Law - Publicly announcing a perceived injustice that's controversial guarantees the comments will justify that idea.
