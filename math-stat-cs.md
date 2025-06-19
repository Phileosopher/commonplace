
# Statistics in computers

Statistical likelihood and probability is difficult for us to wrap our minds around, mostly because it deals with numerical values (which represent a [certainty](understanding-certainty.md)) applied to future possibilities (which represent an [uncertainty](unknown.md)).

## Birthday Paradox

One example of unintuitive statistical projects is the birthday paradox:

- What is the likelihood that X number of people will share the same birthday?

As much as it *seems* to be 1 in 365, the number pushes past 50% after 23 people.

The reason is relatively straightforward:

1. Instead of looking at the number of birthdays, look at the number of individuals who have to pair with another.
2. This means 23 x 22 / 2, which becomes 253.
3. 253 possibilities is over half the number of days in a year (182.5).

Or, to look at it another way, Person 1 must compare their birthday with Person 2, 3, ..., X, then Person 2 does the same with Person 3, 4, ..., X, and so on.

This has far-reaching [computer cryptographic](encryption.md) implications with respect to hash versus block size.
