
To store information, engineers have a variety of possible techniques to work with data in [memory](computers-memory.md).

At its base, there are [data primitives](data.md). They are combined together to create more elaborate structures of data.

There are *many* elaborate ways to store data. Each one has its "use cases".

## Composite data types

These primitives can work into more elaborate "composite data types", which are almost a secondary "primitive".

### Arrays

Arrays are a list of things that are the same [data type](data.md).

One of the most common arrays are strings:

- Strings are a "string" of characters, so pretty much any text meant for someone to see.
- They usually stick quotes around it inside code.
- Strings are great for storing keyboard input as well as outputs.
- You can't operate on them outside of sticking them together ("kiss " + "the cook" = "kiss the cook"). This is known as "concatenating".
- If you *do* need to change them, you're usually simply replacing the original string with a new string.

By putting an array inside another array, it's called a "2-dimensional array":

- 2D arrays will visually look like a spreadsheet.
- The index [row,column] will look like reversed x-y coordinates from algebra (e.g., [0,2] to reference the 1st row and 3rd column).

Arrays can have as many dimensions as you want.

Array sizes are set in stone when you first make them. Thus, you'll have to think ahead about how big the "dataset" will be. So, you can either make an array with the data "populated" already or leave the data blank to be filled in later.

It's usually a good idea to make bigger arrays than you think you'll need when it's a small program, but watch out if you're making something large-scale! A few dozen extra index lines can *really* add extra memory "bloat" if it's implemented 1,000,000 times!

To list this information, the array stores it in an "index", which is just a numbered list. However, unlike anywhere else, because of [how bits work](computers-alu.md), the number starts at 0:

- [0] Item A
- [1] Item B
- [2] Item C
- etc.

If you fail to remember this, you'll keep referencing the wrong value. Referring to anything past the last item will give an array "out of bounds" error.

Arrays can only hold one type, so they often must be defined beforehand, such as "string array" or "integer array".

Since you can do something over and over in an array (such as pull data from index 0, then index 1, and so on), arrays are known as "iterable".

Arrays can be sorted by some other value (such as alphabetical or numerical order) or unsorted. Generally, [searching algorithms](computers-programming-algorithms.md) work much faster on sorted data.

### Records

By grouping an arrays into a homogenous system, you can create a "record" that consists of various data types. This is the backbone of most databases.

A record will often contain a key at the beginning, then a set of organized data values based on the information you're trying to hold (e.g., [1, "John Smith", 32], [2, "Mark Jones", 25]).

### Unions

Though it's not as common and a little more elaborate, software engineers can store more than one data value in a memory register. This only works well when you need an object to be one of many things, but can only be one thing at a time.

* * * * *

## Abstract Data Types

There are a variety of broad "abstractions" on how to structure data.

### Sets

A set can store unique data values, of any type, without any particular order.

While sets are the broadest way to store data, they're also the least useful. The importance of data comes from its relationship with other data, which is why there are [a *lot* of data structures](https://en.wikipedia.org/wiki/List_of_data_structures).

A "multiset" is a set that can store multiple values of the same thing. They can either store the same value and simply count how many there are, or can store the same value in different locations and treat them as distinct.

### Lists

A list doesn't need to have the same data types in it.

Lists aren't ideal for data processing, since working with various types of data can create issues. A list of words and numbers, for example, would return errors on the words, or would treat the numbers as if they were text.

If you use an [algorithm](computers-programming-algorithms.md), you can make the list "sorted", which makes it workable. Otherwise, it's simply an "unsorted list".

If you put the list with references at the end to other locations (instead of setting it in the same place in memory), you can create a "linked list".

One specific type of list is called a "tuple", which is a finite ordered list of elements that can't be changed. An n-tuple has n elements in it.

### Associative arrays

An associative array, or "dictionary", is a variation of an array, but uses a "key" instead of an index. This gets rid of the linear nature of arrays. So, you'll have to know what "key" you want instead of the number it corresponds to ("key/value pair"). Most [databases](database.md) use dictionaries.

Each key must be unique or the database will spit out an error, though the *values* can be the same. Thus, `bobjohnson@yahoo.com` is taken right now, but `bobjohnson_2015@yahoo.com` or `bobjohnsondestroyerof17worldsofwarcraft@yahoo.com` might still be open.

If the key is designed to grab more than one value, then the data structure is called a "multimap".

### Stacks

A stack can be an array or a list, but with the one notable exception that you can only "pop" things off the ends of the collection or "push" things onto it.

A specific type of stack is called a "queue", where information is added on one end and removed on the other. Queues are perfect for absolutely any type of task list. Some queues can be double-ended, in removing or adding values.

A more advanced type of queue is called a "priority queue", where each value has a priority assigned to it for changing its placement into the queue.

### Graphs

Broadly, graph data structures incorporate [graph theory](math-cs.md). These can include trees and heaps.

### Containers/collections

By grouping data types together, you can solve all sorts of problems. These hybrid types can come in all sorts of shapes and sizes, with connections or a lack of connections to other data or references.

* * * * *

## Special Mention

While most data structures are very specific, and [there are a lot of them](https://en.wikipedia.org/wiki/List_of_data_structures), some are so frequently used that they deserve mentioning.

### Dynamic arrays

To fix the limited size of arrays, engineers created "array lists". Instead of something "fixed", they start with a list of ~10 things and keep adding as needed.

The implication of this is vast. It means that you can store an unlimited amount of information when you don't know how much you'll have beforehand. Because of its versatility, user data is often stored this way.

### Hash-based structures

By using various [cryptographic techniques](encryption.md), you can add many layers of complexity to a data structure with hashes. This is often for [data security](computers-cysec.md).

One frequent hash-based data structure is a Merkle Tree:

1. Convert all the data elements into [hashes](encryption.md).
2. Use an algorithm to process some of the hashes into a separate hash (e.g., "abc" and "def" together becomes "ab").
3. Keep doing it to the hashes until you have 1 hash. The entire structure will visually look like a tree.
