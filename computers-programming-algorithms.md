
# What algorithms are

## Algorithms

An algorithm is a math problem where the formula has specific rules that only sometimes apply (e.g., X-5=Y if X is more than 5, but otherwise X=Y).

An algorithm is subject to the same realities as [statistics](math-stat.md): the incoming variables determine its accuracy to [reality](reality.md).

APPLICATION: Since math exists in the mind alone, algorithms are always biased, no matter how much data is fed into it or how well it's [constructed](creations.md), meaning algorithms are as fallible as statistics.

In computers, algorithms and [data structures](data-structures.md) work hand-in-hand, and the concepts are often merged, but there is a distinctive difference between them:

- An algorithm is a set of very specific instructions. It's a mathematical function (like X = Y + 5), but has more functions inside it that make it more complicated.
- A data structure is the form of the information itself.

Unfortunately, it's difficult to imagine a verb without a noun, and a noun without a verb isn't very useful, which is why the concepts are often merged. Further, some algorithms are designed for specific data structures, further adding complexity.

Hiding an actual calculation for an algorithm is a very effective way to [distort how things appear](people-image-distortion.md). The people who run most [computer technologies](technology.md) over a network can often tweak information for various reasons from what it legitimately was expressing.

Whenever a computer receives information and converts it into something else, it uses an algorithm of *some* sort. It can create strange consequences, so it can be helpful for most people to broadly understand what algorithms even are and what they do.

## Big O notation

Algorithms need time and memory to work through lots of information. There are a variety of algorithms that can each work for specific purposes.

The more information, the more time or [memory](computers-memory.md) the computer will need to work with it.

Computer scientists focus on how much time and memory those algorithms take with 3 major calculations:

- The worst-case scenario: "Big O notation"
- The average: "Big Omega (Ω) notation"
- The best-case scenario: "Big Theta (Θ) notation"

However, most data scientists worry the most about Big O because it's the most likely to leave the computer hung-up on calculating.

## Searching algorithms

It may seem simple to search for stuff, but it gets complicated with 100,000,000 points of data. Even a 1% increase in efficiency is a noticeable improvement.

A searching algorithm has a simple enough procedure:

1. Take a value that someone gives in the form of a text "string".
2. Use the algorithm's procedure to find the string in the given list or array.
3. Return an "index" number corresponding to where the match is located.
4. If the string doesn't have a value, return "null".

There are several ways to search, but linear and binary searches are the most common.

"Linear search" is the easiest to understand. Match the input value to the first value, then the second, and so on until you find what you're looking for or run out of list.

- Linear searches suck at efficiency (O(n)=n, Ω(n)=n/2) and their only advantage is that they can work through *both* sorted and unsorted lists.

"Binary search" is splitting a sorted list in half, over and over:

1. Tests the middle-most value to see if it's the input value.
2. If it isn't, it only looks at the half that could possibly match it.
3. Repeat indefinitely until the list is exhausted or the computer finds a match.

- Binary searches are *very* scalable because they run at a logarithmic speed (O(n) = log n), so finding data in a pile of 1,000,000 data points only takes 1 extra iteration compared to finding data in 500,000.

## Sorting algorithms

A sorting algorithm will take a dataset and organize it by some [organizing](organization.md) convention, typically alphabetically/numerically.

"Bubble sort" is the simplest sorting algorithm, but can also be the most resource-intensive and time-consuming. It simply compares a data point with another data point later in the database, and swaps it if it's out of order. Unfortunately, bubble sort needs to "iterate" through *all* the sorted data points for it to be successfully sorted.

"Insertion sort" is the reverse of bubble sort. It compares the data entry with the entries *before* it and places it where it's supposed to go. Insertion sort only takes half the time as bubble sort, since it has a "known-good" organized database behind the current examined data point.

Many sorting algorithms have been designed to sort faster than insertion or bubble sort. They all work on the same idea of breaking the entire database into large blocks/partitions, sorting each block, then sorting the blocks together. QuickSort is the most popular and effective "divide and conquer algorithm".

## Transfer algorithms

TCP's slow start algorithm is relatively straightforward, but a genius solution to scalable network speeds when they're impossible to predict:

1. Start slow in *slow-start* phase with a packet window size of 1 (where a packet window is the number of packets before waiting for an acknowledgment). Double the packet window size each iteration until the first packet loss (which becomes the *threshold* value).
2. Move to *congestion-avoidance* phase and increase the packet window size at a linear rate.
3. When 3 of the same are acknowledged (ACK), set current speed to half and set it as the *threshold*.
4. When a *timeout* happens, set *threshold* to half the current speed and set the current speed to the slowest possible.

## Encryption algorithms

Because of the ubiquity of encryption (as well as the constant changes from all the [password-cracking](hacking.md)), encryption is in an [entirely different domain](encryption.md) than most other algorithms.

## Compression algorithms

To send [files](computers-files.md) across a [network](networks-cs.md) or [store long-term](computers-memory.md) without using it, it makes sense to cut down on as much space as possible.

To do this, compression algorithms essentially run a sequential process of shrinking all the data:

1. Find specific patterns (e.g., 010101, 111111, etc.).
2. Convert the patterns (e.g., 010101 becomes 01, 111111 becomes 11, etc.).
3. Keep the conversion available to decompress when needed (e.g., 0100011 will become 010101000111111 later).

## Machine learning algorithms

Machine learning, in particular, is a vast collection of the previous algorithms, but tends to use other algorithms as well. Most of it is to articulate and clarify [uncertainties](understanding-certainty.md) (called "entropy" inside the industry).

A decision tree uses a tree-like model of decisions to walk through a set of selections, a bit like [project management](mgmt-2_projects-cs.md) but with more specificity. When documenting and building, the nodes break apart into sections:

- Decisions - a clear condition to indicate what the computer must do, represented by squares.
- Chances - a probable likelihood of a response, represented by circles.
- End - a termination of any further action or transition to a different algorithm or decision tree, represented by triangles.
