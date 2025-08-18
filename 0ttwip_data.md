
Data is information. It's the plural of datum, which can easily be defined as a "known fact". In other words, data are known facts.

While computers are always too dumb to understand the essence of truth, all computer data is some form of absolute. Even when it's vaguely expressed or is intended to have an intuitive component (e.g., [AI](/ai/)), it *must* have a concrete aspect to it for the information to be encoded.

This is a bit foreign to our minds, since we're able to *not* [understand](understanding.md) something while at the same time [believe it](understanding-certainty.md), which is a *massive* component of what drives our [creativity](https://gainedin.site/creativity/).

Human sensory experiences process first with [emotions](mind-feelings.md) that branch outward into reasoning and [logic](https://gainedin.site/logic/) that then form into [decisions](https://gainedin.site/decisions/), but computers work through information differently:

1. Computers start with [logic](/logic/), represented as simple 0s and 1s.
2. Those 0s and 1s then build into [math](/math/).
3. That math can capture a *lot*, including [text](/handwriting-ocr/) and [visual information](/camera/), using a vast variety of standards and procedures.
4. The numerical values can be manipulated, expressed, transferred, and whatever else that the computer is [programmed](/prog/) to do.

Computers are dumb, so they need clarification on what sort of data they have before working with it.

Computers don't automatically understand that **"4"** looks like **4**, since that requires intuition, which is a component of feelings. Unless specifically instructed to, they will treat all the following things as completely unrelated:

- 4
- "4"
- 4.0
- four
- Four
- FOUR
- 4.0000
- 5-1
- fore
- one more than 3, 1 less than 5

## Data primitives

Null

- A null value is empty. Not 0 or blank, but empty, a bit like an empty box.
- They can't be operated on, though doing so is also *philosophically* difficult.
- Depending on the [programming language](/langs/) and [compiler](/compilers/), it returns 3 possibilities if it's operated on:
  1. Ignores it (e.g., "John's email is ")
  2. Prints it (e.g., "John's email is null")
  3. Gives a NullPointerException [error](/software-redesign/)

Boolean

- True or False, that's it. Simple [binary logic](/logic/). 0 or 1.
- They can't be operated on at all.

Integers

- Integers are whole numbers, *never* decimals, and can include 0.
- Comes from putting Boolean numbers together (counting up as 0, 1, 10, 11, 100, 101, 110, etc.).
- As of writing this, they can be anything between positive and negative 2,147,483,648 (2^21 because of [how bits work](/alu/)).
- They can be fully operated on (e.g., [add/sub/mult/div](/math/)).

Floats/Doubles

- Floats hold decimal places up to 32 bits and doubles up to 64 bits.
- They're essentially integers, but with a separate number for the area to the right of the decimal point.
- They're fully operable.
- There are also fixed-point numbers that only hold digits out to a certain specific decimal place (e.g., 98.20), which can be very useful for specific things like money.

Chars

- Chars are 1 letter/number ("character"). You can store a [string](/data-structures/) with 1 character as a char.
- They're *really* useful for tracking [keyboard](/keyboard/) presses (such as a [computer game](/game-dev/)).
- They come through symbolically representing certain numbers as specific characters (e.g., [U+0034 for "A"](/keyboard/)).
- They can't be operated on at all.

Date/Time

- Date and Time is a variously expressed form of capturing time-based values, based on [set standards](/protocols/).
- The values can be short (e.g., 5/1/16) or long (e.g., May 1st, 2016 15:25:36.435).
- Often, dates can be stored as whole numbers to represent days and decimals to represent time (e.g., December 21, 2012, at 12:12 pm becomes 41264.5083333333).
- Dates typically pick an arbitrary starting point to cross-reference with "zero" (e.g., December 30, 1899, for spreadsheets).

Refs

- Refs (short for references) are pointing to other things such as [memory](/memory/) locations, [variables](/prog-basics/), or [network locations](/networks/).
- They can be overwritten with a re-reference to something else, but the only operating is on what that reference points *to*.

Enumerated type

- Enumerated type creates classified groups of things based on a category (e.g., COLOR can have Red, Blue, and Green in it), sometimes with number codes attached to each.
- They're useful to clearly demarcate certain values.
- Technically, other data types like Boolean logic are frequently enumerated types, depending on how the [programming language](/langs/) sets it up.

There are many, many, many more classifications of data, which typically comply to a wide variety of [industry standards](/protocols/), and these data primitives can assemble into many more advanced [data structures](/data-structures/).

Most additional data types are *not* standardized as much as the above primitives, for several reasons:

1. There are often multiple design choices involved, which means any standards would prohibit the full range of usable structures.
2. The text implementations often represent as multiple forms that can't be reduced or simplified to a single set of syntax rules.
3. Those data types are far too important to allow slowdown through translation into a standardized system, so it's not wise to even *think* of adding any constraints to speed.

Even then, data types can often be standardized more locally, such as in a programming language (e.g., graphs exist as a standard in the Datalog [programming language](/langs/)).

## To what end?

Incoming data doesn't always conform to what may be needed for a computer's input, so many [algorithms](/algorithms/) are designed to "normalize" that data. This may include:

- Altering text case (e.g., "JOHn sMiTh" becomes "John Smith")
- Removing punctuation (e.g., "mark.johnson" may become "markjohnson")
- Adding clarifications about punctuation and special characters (e.g., "mike.jones" may become "mike/.jones" for the computer to understand it)

Data itself is stored in [memory](/memory/), and computers only do a few possible things with it:

1. Wait and do nothing, with the information held for later use.
2. Do further logical things with it, based on what a [program](/prog/) is instructed to do.
3. Output the information somewhere. It may be nearby (e.g., a [screen](/screen/)) or sent out to another computer via a [network](/networks/).

Individually, data doesn't mean much, but combining data with other data can generate *immense* results, especially as [databases](/database/) grow substantially larger.
