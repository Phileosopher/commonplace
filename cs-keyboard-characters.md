
# Coded keyboard characters

Once the standardized keyboard signal enters the computer, it needs to be converted to represented text. It may pass to the [operating system](cs-os.md), but there's a very high likelihood the user will want to visually see they just typed something, which presents another set of challenges. Text must [display in some user-friendly fashion](engineering-graphics.md), with many forms of [typography](language-writing-typography.md) available.

## ASCII

If we count all the upper and lowercase letters within Western languages, along with special characters like "," and "?", we can easily fit them all into 128 numbers.

- Thus, we can use [7 bits](cs-memory.md) to represent all the basic Latin-based letters, with each number corresponding to a certain letter.
- [An example with this ASCII "code page"](https://www.asciitable.com/)

In case you're wondering why it wasn't [8 bits](cs-memory.md), teleprinters used to send text well, but the early microprocessors weren't always reliable, so that final bit was typically used for parity. [Memory](cs-memory.md) wasn't as reliable as it is today and a 0 or 1 would sometimes swap, so they created an error-checking system with a bit at the end:

1. Count the number of 1's in the [memory register](cs-memory.md).
2. When it's "even parity", the parity bit is 1 if the sum is odd, and 0 if it's even, which makes the sum always even. The bits are the opposite for "odd parity".
3. When reading, check if the sum is odd or even, then send it again if it doesn't match what it should be.

These code pages wasn't always easy to work with, since they varied on certain details.

- It's critically important that you know *which* code page you're using, since the wrong conversion will make the data completely useless.

To avoid further headaches, [engineers got together](standards.md) and created the ASCII standards to match the same numbers to letters on all the computers. This worked, but only gave 95 characters. See [EBCDIC](https://en.wikipedia.org/wiki/EBCDIC) to understand the headaches involved.

## Unicode

Later, they created a universal standard called Unicode, which ambitiously tried to represent *every single character for language that humanity has ever made*.

- UTF-8 is meant to be backwards-compatible with ASCII.
- UTF-16 wasn't and is generally not used as much. The original Unicode standard would have given 65,536 characters, which they imagined would be enough code points, but they needed a few more.
- UTF-32 is the current standard for an all-inclusive text format. It's still being added to, but is presently over 140,000 characters. Until [software standards](cs-standards.md) can use 262,145 characters, Unicode only requires 18 bits per character to transfer.
  - The wealth of characters means there have been many icons that can be used in-text as emoji (e.g., each country's flag, happy face).
- As of the early 2020s, UTF-8 is *usually* the standard for [most websites](cs-sofware-webdev.md). The intuition would be that UTF-32 is the best solution, but it often requires multiple "code points" to store the information, so it's easier to use a smaller UTF format.

To save on data (since a database can frequently be *trillions* of characters), engineers developed "variable-length" encodings, where the leading bits can communicate how many bits the rest of the text has. The human-readable code point for each character looks like U+0041 U+0052, and doesn't carry over any [graphic design](engineering-graphics.md) or font selection.

Somewhat adjacent to UTF-8 is how text is represented in URLs and some filenames. By using [RFC 3986 section 2.1](https://datatracker.ietf.org/doc/html/rfc3986#section-2.4), UTF-8 maps to modern web standards with a percent-encoding.

- The syntax is "%", followed by two hex values that represent a character (e.g., %35 for "5").
- It isn't precise many times, and [this reference sheet](https://www.w3schools.com/tags//ref_urlencode.asp) shows some of the differences between Windows-1252 and UTF-8.

### Unicode issues

The standards for Unicode are drawn from the history of language, so they are *not* an exact science. Many of them borrow from prior printmaking conventions, and some characters are imported straight from it without much consideration. Further, some [fashions](people-trends.md) can affect whether some characters become [standardized](cs-standards.md).

In fact, Unicode standards for higher-level text can be messy, and each language will parse it differently. For example, 🤦🏼‍♂️ is accurately defined as 1 character in Swift and Elixir, but 3 characters in Python, 7 in JS/Java/C#, and 17 in Rust.

Further, there are duplicates of some characters, meaning the text is *not* the same encoding even when it appears the same. As an example, Å and Å are *not* the same character, since one of them is composed of the Latin A with a combining character and the other is a pre-composed code point.

There are also regional considerations, but unfortunately the region is contained in metadata, which is often lost during transfer, creating further issues.

Since the computer must read the entire [memory register](cs-memory.md) to understand what character the text is, any errors are represented as �.

The space character in particular has been troublesome. Space delimiting in [commands](cs-cli.md) often implies a demarcation, so most [programming](cs-software.md) either uses quotes, indicates that the spaces *don't* matter in a specific context, or use another set of characters like "%20" to indicate it.

This will probably move around based on the Unicode standard moving as well (new standard [every year](cs-software-versionctrl.md)), meaning the above example may become obsolete by the time you read this.
