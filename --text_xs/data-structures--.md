
NOTE: ADDRESS SOCIAL GRAPHS, SINCE THEY'RE REFERENCED FROM FAANG PAGE

Values, records, hierarchies (trees), types & more

## freeCodeCamp dev quiz - Data Structures

When you create an array, you are allocated a block of contiguous memory and in order to change it's size, you will have to create a new array.

A stack is the most suitable data structure for converting an infix expression to a postfix expression

Lists are mutable built-in data structures in Python. This means that you can add new elements to a list, update the elements of a list, and remove elements from a list.

The "indexing" of a data structure starts at 0

- The index is just a relative location from the beginning of the data set
- While the rest of the record can be mutable, the keys typically MUST be immutable
- Over time, in BIG data sets, the index number becomes very large and complicated, and the database needs to get rebuilt to cut down on memory use

Array destructuring is used to extract array values into new variables.

A dictionary can store key-value pairs, which are pairs of associated values. We use the key to access its corresponding value in the dictionary.

Here are the data structures a block group can contain:
Super Block: a metadata repository, which contains metadata about the entire file system, such as the total number of blocks in the file system, total blocks in block groups, inodes, and more. Not all block groups contain the superblock, though. A certain number of block groups store a copy of the super as a backup.
Group Descriptors: Group descriptors also contain bookkeeping information for each block group
Inode Bitmap: Each block group has its own inode quota for storing files. A block bitmap is a data structure used to identify used and unused inodes within the block group. 1 denotes used and 0 denotes unused inode objects.
Block Bitmap: a data structure used to identify used & unused data blocks within the block group. 1 denotes used and 0 denotes unused data blocks
Inode Table: a data structure that defines the relation of files and their inodes. The number of inodes stored in this area is related to the block size used by the file system.
Data Blocks: This is the zone within the block group where file contents are stored.
