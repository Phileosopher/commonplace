
# Computer math

Computers use plenty of math. In fact, computer science is pretty much a [runaway branch](math.md) of applied mathematics.

## Boolean/Arithmetic

The primary difference between math computations and our minds is that most applied mathematics uses a base-10 "denary" system, while computers operate in base-2 binary.

[Boolean math](logic-cs.md) is a fancy name for "logic", and has the traits of [any other math](math.md). Specifically, it can expand its [logic](logic.md) to assemble into most other calculations. Boolean, in specific, maps each TRUE statement as 1 and each FALSE statement as 0.

## Two-based

Two-based math isn't as hard to understand as it may appear. Instead of counting fingers, you count fists. Here's how it looks if you start counting from zero:

1. 0
2. 1
3. 10
4. 11
5. 100
6. 101
7. 110
8. 111
9. 1000
10. 1001
11. 1010
12. 1011
13. 1100
14. 1101
15. 1110
16. 1111
17. 10000

...and so on.

To make it easier to look at, engineers simplified large binary numbers. The range of 0000-1111 could represent in 1/4 the symbols with 0-f (0,1,2...9,a,b,c,d,e,f). The "hexadecimal" format starts with 0x to avoid confusing anyone (e.g., 0xffd4267).

## Calculations

"Combinatorics" is the math of counting up and down, and is a frequent part of computer science because [assembly code](programming-assembly.md) is almost always simply counting.

At its most basic, a computer can calculate basic arithmetic:

- Addition
- Subtraction

Multiplication is merely addition several times over (hence, 5 *times* 4). Division is merely subtracting as many times as possible before the number becomes negative (or positive if it's already negative).

It's worth noting that the representation of binary numbers is always 1 less than denary, so an 8-bit (or 1-byte) register will show as 0-255 but will represent 256 locations.

## Finite States

Every portion of the information in a calculation has a "state", which is simply what the information is at that specific point in time. This is almost always constrained to the purpose of what you want the computer to calculate, so it's not easy to broadly define because the purpose will change depending on what you want to do.

To manage more than a moment-by-moment calculation, computers use "pushdown automation", which is running through calculations one after the other on a "stack". By using pushdown automation with memory, you've successfully created a Turing machine.

The 2-based numbering system places a unique limit on computer [memory](computers-memory.md). Instead of limits set at 10, 100, 1,000, and so on, they limit at 2, 4, 8, 16, 32, 64, 128, 256, 512, etc. The consequences of this are that some constraints are unintuitive without looking at memory registers.

[Advertised](marketing.md) technology will use base-2 numbers in their branding (e.g., 32-bit graphics, 128-bit encryption, Nintendo 64), but most [computer interfaces](design-uxui.md) abstract away the constraints by the time the software is [finished](computers-software-versionctrl.md).

## Modulus

One frequent part of computer math that we don't see as much in daily life is a "modulus", which is represented using "%". Instead of incrementing the numbers upward or downward, the math of [boolean logic](logic-cs.md) will wrap around to the other side, just like how a clock moves from 11 to 12 to 1.

While a modulus is *technically* everything that fits in that set, the modulo operation in computers is meant to return the "remainder" you may remember from [third-grade math](math-algebra.md) (e.g., 14%3=2, 25%2=1, 17%3=2).

Modulus are useful in many places, but *really* useful when trying to find out if something is even or odd, since only even numbers cleanly divide by 2. It can, for example, verify information was successfully transferred.

## Zero-Based

Another frequent hangup between computers and human math is the idea of zero-based numbering.

Normally, people start intuitively at 1 when counting:

- 1, 2, 3, 4, 5...

Because of [how computers count](computers-alu.md), the first number for computers is 0. Thus, counting goes:

- 0, 1, 2, 3, 4...

Without being aware of this, programmers can often create [logic errors](computers-software-redesign.md) that differ by 1. Generally, it's worth paying close attention to *any* number that is off by 1, since the computer won't know any better.

## Algebra

By combining [arithmetic](math.md) together, we can create variable-based math, which moves into the world of [algebra](math-algebra-cs.md).

The beauty of algebra is that it can be used to represent all sorts of lines in Euclidean space, which allows us to apply algebra to geometry and, thus, create [three-dimensional graphics](graphics.md).

## Calculus

[Calculus](math-calc-cs.md), in a sense, is the reverse of algebra. Instead of giving the computer a formula and being able to create lines from it, calculus gives a set of points in space and asks what the formula is. This has profound implications for fields such as [machine learning](computers-ai-ml.md).

## Statistics

When reality's complexities apply, it's far more important to work with likelihoods and probabilities, which is the [realm of statistics](math-stat-cs.md). Most practical computer applications in [large-scale systems](computers-distsys-enterprise.md) need to operate with statistics more than anything else.
