
# Logic gates and the ALU

At their most basic, a computer is a [logic machine](logic.md). Each logical value is a "bit", represented as a 0 or a 1.

## NAND/NOR

All logic is built on the three foundations of NOT, AND, and OR.

- NOT:
  - 1 goes in, 0 goes out
  - 0 goes in, 1 goes out
- AND:
  - 1 and 1 go in, 1 goes out
  - anything else goes in, 0 goes out
- OR:
  - 0 and 0 go in, 0 goes out
  - anything else goes in, 1 goes out

If you have those 3 [Boolean](logic-cs.md) "logic gates", you can build out any other logic by attaching the output of some to the inputs of others. XOR, for example (only 1 and 0 or 0 and 1 go in to make 1 go out) can involve an OR gate and 2 AND gates.

But, some engineers realized something clever: by using one specific part that was a hybrid of NOT and AND they could do *everything* with that one piece:

- NAND:
  - 1 and 1 go in, 0 goes out
  - anything else goes in, 1 goes out

Thus, they'd only have to keep track of 1 part instead of at least 3:

- NOT (1 gate) - feed the same thing into both inputs, then the AND part of NAND won't matter, and it gives back the opposite.
- AND (2 gates) - feed both through one NAND gate, then through a NOT gate.
- OR (3 gates) - feed A and B through a NOT gate, then both those outputs through a 3rd NAND gate.
- XOR (4 gates, though trickier to understand)
  1. Run A into both NAND1 and NAND2
  2. Run B into both NAND3 and NAND2
  3. Run NAND2 into both NAND1 and NAND3
  4. Run NAND1 and NAND3 into NAND4

There are also tricks to use NOR gates as a primitive instead, but it's basically the same idea. NOR is less common because it's pricier, but NOR gates are faster than NAND gates.

By combining these gates together, we can create a switch that sends information from one of multiple sources ("multiplexer", or MUX) or a switch that selects something that can go down multiple possible ends ("demultiplexer", or DEMUX).

From here, we can create arrays of those gates, which flows like a busload of these bits (aka, a "bus"). More building out can allow 4-way and 8-way switches, either in parallel or all converging together.

Thus, the logic can get as complicated as it needs to be with lots of only one gate. From here it's lather, rinse, repeat.

It's worth noting that the way I describe them from here on is the easiest way to understand them. Because it's *all* based on NAND/NOR, there are much more efficient solutions that engineers actually use that create the same result.

## But What *is* It?

If you're curious, you're probably wondering what those little gates are made of. That requires learning *lots* of electrical engineering and physics, which is *technically* almost outside the domain of computer science. Currently, engineers use CMOS logic to create them, but that may change in a decade or two.

There is lots of complicated stuff in there to closely consider, and it's an engineering art of its own:

- Bad design that crosses wires
- "Electrostatic interference" from nearby electricity
- The amount of "power draw" that runs up the need for electricity

However, the idea for a gate is relatively simple. You could have an electrical resistor that requires the charge from two inputs, for example.

Generally, the less gates and less distance electricity travels, the more reliable the technology gets, so engineers are *constantly* improving their computers to be smaller with parts closer together.

## Math

All these logical things can become [base-2 math](math-cs.md).

Mathematically, almost everything in computers starts with adding, including subtraction (see below). If you remember second grade, both multiplication and division are fancy versions of adding and subtracting, so adding will effectively let us do *all* the math.

One huge difference between base-10 (how normal people count these days) is that base-2 uses "zero-based numbering":

- In base-10 (decimal), you count as 1, 2, 3, 4, etc.
- In base-2 (binary), you count as 0, 1, 10, 11, etc.
- Base-2 above translates into base-10 as 0, 1, 2, 3, etc.
- The implications of this mean that a list of 54 items will number as 0-53, and referring to #25 *might* refer to either 24 or 25, depending on the numbering convention.

### Adding

Adding is pretty simple. If you have two bits, there are only 3 possible outcomes:

- 0 and 0 make 00
- 0 and 1 or 1 and 0 make 01
- 1 and 1 make 10

An AND gate for the left number and an XOR gate for the right will let you output the two numbers. The whole thing is called a "half-adder".

The leftmost number is a "carry", like when you "carry the 4" in [second-grade math](math.md). It moves to the left, so if you want to use more math you'll want to do something with the carry.

By attaching two half-adders together and sticking an OR gate on both the carries, you can do math on 2 bits. A full-adder can be scaled indefinitely, though it can be optimized when it gets bigger.

One notable difference between computer science and proper math: the final number on the far left (an "overflow") gets dropped. Thus, 1000 plus 1001 makes 0001 instead of 10001.

Making an "incrementer" is simply a specific adder that adds 1 to the entire thing.

## Subtracting

Negative numbers also need representation, and there are several ways to do it.

What they *could* do is swap the leftmost number, like we already do with normal base-10 numbers, to make -# the inverse of #. So, the negative of 001 is 101. The problem with this system is that there are *two* representations for zero (0000 and 1000), so doing calculations on it gets weird, and weird calculations create bigger problems later.

Instead, they use what's called [Two's Complement](https://en.wikipedia.org/wiki/Two's_complement). Complex math aside, the negative numbers are the complementary additions to the positive ones:

1. Start with the 3-bit binary number for 2 (010).
2. There are 8 possible numbers for a 3-bit number (###), so the complement of the number 2 will add to 8.
3. 8 - 2 = 6, so 2's complement is 6.
4. Thus, -2 in a 3-bit number is the binary number 6 (110).

In practice, you can count downward by cycling back to the top number. 0 is 0000, -1 is 1111, -2 is 1110, -3 is 1101, and so on. Plus, to find the inverse, you just have to flip the 0s and 1s, then add 1 (0101 becomes 1011, 001101 becomes 110011, and so on). This also means that the first number in the binary sequence will be 1 if negative.

While two's complement makes adding numbers relatively straightforward with positive/negative addition, the mathemagic on this gets intense once you add negatives. Basically, you can add two numbers as their positive version:

- e.g., in a 4-bit setup, the complement of -2 is 14, or 1110, and -3 is 13, or 1101
- The total will, naturally, be the sum of the two:
  - e.g., in this case, 11011, or 27
- But because it drops off the overflow (as stated above), it converts the number to the correct answer:
  - e.g., 11011, or 27, gets stripped down to 1011 (or 11), which converts its complement back to -5, which is -2 plus -3

### All together now

Now, we can slam all of the above together into one logic unit called the Arithmetic Logic Unit (ALU).

Each ALU varies in the varieties of things it can do. Basically, more features cost more but calculate everything faster. However, anything else above this can be completely handed off to software on a higher-up level.

Every ALU has 2 inputs labeled x and y, a bus of control bits ("opcodes"), an output, and control outputs.

The opcodes have *very* specific purposes, which use all of the above stuff in various formats to make. They're essentially 1/0 on/off "switches":

- zx - set x to 0 if on
- nx - set x to NOT x if on (0 becomes 1 and 1 becomes 0)
- zy - set y to 0 if on
- ny - set y to NOT y if on (0 becomes 1 and 1 becomes 0)
- f - use x AND y if off, use x+y if on
- no - operate NOT on the finished result if on (0 becomes 1 and 1 becomes 0)

The output produces the result, but with other control outputs:

- zr - if the output is zero, give 1
- ng - if the output is negative, give 1
- ov - if there's a carry bit, give 1

This humble ALU can now do any [math](math.md) or [logic](logic-cs.md) anyone could ever need. Addition and subtraction are the basis of all the multiplication and division, it can verify binary information against other information via subtraction, and it can zero something out. All it requires is a useful implementation!

This ALU can now work inside the [CPU](computers-cpu.md).
