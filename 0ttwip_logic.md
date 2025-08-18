
With respect to how computers see it, (and irrespective of what you believe about [logicism](https://gainedin.site/glossary/)), [arithmetic](https://gainedin.site/math/) is an advanced form of [logic](https://gainedin.site/logic/).

Math operations start with addition and subtraction, then compound to create multiplication/division, then compound *again* to create exponents and squares.

However, to express it, computers use Boolean algebra, which begins with a few base primitive operations:

- NOT (¬x or !x)
  - ¬x=0 if x=1, ¬x=1 if x=0
  - If x gives 1, give back 0, and the other way around.
- AND (x∧y or Kxy or x&y)
  - x∧y=1 if x=1 and y=1, otherwise x∧y=0
  - When x and y are 1 and 1, then give 1, but otherwise give 0.
- OR (x∨y or Axy or x|y)
  - x∨y=1 if x=1 or y=1, otherwise x∨y=0
  - When x and/or y is 1, give 1, and give 0 if neither are.

By implication, those calculations derive some secondary operations:

- XOR or x⊕y or x≠y (exclusive or)
  - x⊕y=1 if only x=1 or y=1, otherwise x⊕y=0
  - When *only* x or y is 1, give 1, and 0 for everything else.
- x → y (material implication)
  - if x=0 use x's number, if x=1 use y's number.
  - Not used *nearly* as often in computers as XOR.
- x ≡ y (equivalence)
  - x≡y=1 if both x and y are the same, otherwise x≡y=0.
  - It's the inverse of XOR.

From here, there are plenty of "no duh" laws that these primitives can work with:

OR (∨)

- Associativity of ∨: x∨(y∨z) = (x∨y)∨z
- Commutativity of ∨: x∨y = y∨x
- Identity for ∨: x∨0 = x
- Annihilator for ∨: x∨1 = 1 (but not in normal algebra)
- Idempotence of ∨: x∨x = x (but not in normal algebra)

AND (∧)

- Associativity of ∧: x∧(y∧z) = (x∧y)∧z
- Commutativity of ∧: x∧y = y∧x
- Identity for ∧: x∧1 = x
- Annihilator for ∧: x∧0 = x
- Idempotence of ∧: x∧x = x (but not in normal algebra)

OR / AND together (no symbols, to keep it real)

- Absorption (not in normal algebra):
  - x AND (x OR y) = x
  - x OR (x AND y) = x
- Distributivity of AND over OR:
  - x AND (y OR z) = (x AND y) OR (x AND z)
- Distributivity of OR over AND (not in normal algebra):
  - x OR (y AND z) = (x OR y) AND (x OR z)

In case you're wondering (like I was), there's a reason why rearranging all this logic matters. It doesn't really matter in a vacuum, but once you start assembling it into [advanced logic](/alu/), you're drawing hard rules to not simply clarify what a computer should accept, but also to fully clarify *future* possibilities.

As an example, you might tell a computer to sort colored balls. If there's only red and green balls in the box, you *can* simply say "give me all the red ones". But, if you throw some yellow ones in there and want it to grab it as well, you have more than one way to fix that issue:

- Give me all the red balls, give me all the yellow balls.
- Give me all the NOT green balls.

The first one is tiresome, and becomes obsolete if you bring in a third color. The second allows you to only omit green balls no matter how many colors there are. This becomes very significant if there were, let's say, 300 colors in the mixture.

Thus, understanding these primitives and how they operate is to get inside the mind of a computer and how to work with it. All this math compiles itself inside meaningful mathematics inside the [arithmetic logic unit](/alu/). It's a big reason why computer scientists are some of the most logical people on the planet, even if they're [not always the most sensible](/trends/).

* * * * *

## Additional reading

[QED](https://teorth.github.io/QED/) - a simple, interactive primer on formal logic
