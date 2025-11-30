
# What databases are

[Data](data.md) itself is important, but a huge part of that importance comes from the connections it has to other things. The number "40" doesn't mean much by itself, but it has a *huge* implication if it's sitting next to another datum that says "age", "friends" or "number of people killed in falling pillow incident".

There are many ways to store data, but the longest-standing method for most situations is to use relational databases.

## Relational databases

A simple relational database will look like a standard two-dimensional "table":

| ID | **Name**    | **City**        | **Residence** | **Family** |
| 1 | John Smith   | Phoenix, (AZ)   | House         | 2          |
| 2 | Mark Jones   | Anchorage, (AK) | Apartment     | 1          |
| 3 | Adam Harris  | Atlanta, (GA)   | House         | 15         |
| 4 | Diane Jensen | Brussels (UK)   | Flat          | 4          |

If that looks familiar, that's because Microsoft Excel spreadsheets are simple relational databases.

Each of the elements in a table is called a "field". You can make a list by putting the fields together, and each field can technically become its own list:

1. One list could be "John Smith, Mark Jones, Adam Harris, Diane Jensen". This would be a column of data.
2. Another list, though, could be "Diane Jensen, Brussels (UK), Flat, 4". This one would be a row/record of data.

The level of lists determines how many "dimensions" of data you have. The above is only 2D, but it can go as far as you need, with each field becoming its own data table.

More database complexity becomes more difficult to manage. Every new dimension to a database creates exponentially more need for [memory](computers-memory.md), and can become exponentially more difficult to [search through](computers-programming-algorithms.md). To that end, it makes sense to shave down databases whenever possible.

### Primary key

One important part of a relational database is that it needs a "primary key", which is the association to all the other parts of the database.

That primary key can be a "foreign key" in other parts of the document, but it'll be the same identifier:

- In the above example, Mark Jones' primary key is 2, and it would be 2 on another table even if the column was called something else like SalesID.

The primary key has a few consistent attributes:

1. It never changes. Ever.
2. It's used over and over again to cross-reference information.
3. It's never "null".

The easiest way to have a primary key is to make it a "surrogate key", where it has no real-world equivalent. That way, when weird statistical exceptions to the rule happen and people change their Social Security or name, you don't have to worry about rebuilding an entire record.

## SQL

SQL stands for Structured Query Language. It's a [language](computers-programming.md) designed to let anyone (not just technical people) deal with [data](data.md) by using "queries". A query is requesting for data, but then can change the data after requesting it.

Most people get daunted by the fact that SQL is a programming language, but [their fear is a bit overblown](computers-programming.md). SQL is relatively easy to understand, though it may take an afternoon or two to fully feel out the concept.

It's worth noting that the term "SQL" the database isn't the same as "SQL" the server. Microsoft SQL Server happens to be one of a variety of languages that use SQL, but there are other "relational database management systems" (RDMS) including postgreSQL, MySQL, AQL, Datalog, and DMX.

### Simple queries

To make a table, use the CREATE TABLE command. To delete, use DROP TABLE.

First, we can SELECT the columns to grab and specify FROM where it comes from:

- SELECT family
- FROM table;

We can add more information to change which rows apply:

- SELECT name
- FROM table
- WHERE family >5;

There are many ways to specify information even further:

- `*` selects *everything* in that selection range.
- Clarify how you want to organize it with ORDER BY.
- SELECT DISTINCT gets rid of duplicates.
- LIMIT specifies how many items you want in the list.
- SELECT (column/function) AS (alias) can give you a new label for something. This can be immensely useful when you start using mathematical calculations to present new columns of information.
- GROUP BY lets you arrange counted information into new classifications.
- HAVING is like WHERE, but runs *after* SELECT, meaning that it can grab a larger scope of data.

It gets more complicated with more tables. The simple command for handling multiple tables is JOIN:

- INNER JOIN, or simply JOIN, will only pull data where *both* tables have the same data. The other 3 are called outer joins.
- LEFT JOIN will keep rows from the first table no matter what(think of 2 tables side-by-side).
- RIGHT JOIN will keep rows from the second table no matter what.
- FULL JOIN means keeping rows from both no matter what.

Now, all together:

1. SELECT (ColumnRange) FROM (Database)
2. JOIN (Database2) ON (DatabaseColumn) = (Database2Column)
3. WHERE (SpecificCondition)
4. HAVING (AnotherCondition)
5. GROUP BY (CountableRange)
6. ORDER BY (Column)
7. LIMIT (Number)

### Under the hood

Intuitively, the impulse is to think that SQL is doing the following:

1. Joining the data together.
2. Filtering out the irrelevant data.
3. Grouping the data and condensing it.

In reality, computers operate differently because of how data processes in them, so SQL queries operate behind the scenes in a specific order:

1. FROM and JOIN (and all the ON conditions) - specify the database you're pulling from
2. WHERE - specify the rows
3. GROUP BY - condense multiple rows into more concise information (such as COUNT)
4. HAVING - specify rows again, but with more specific instructions
5. SELECT - specify the columns (which is *almost always* used) or window functions.
6. ORDER BY - organize by ascending or descending.
7. LIMIT - set a limit to how many items you want to grab.

Of course, there are many optimizations that database managers run before executing code, so this isn't quite precise. Often, the RDMS is verifying *everything* a few times before it actually *does* anything, and it will sometimes skip irrelevant steps.

The reason the SQL database language has persisted (and likely will continue) is because *most* programming languages can plug into this rather elegant solution to access and modifying information. Here's [an example from pandas pulled from a programming blogger](https://jvns.ca/blog/2019/10/03/sql-queries-don-t-start-with-select/):

```sql
df = thing1.join(thing2)  # like a JOIN
df = df[df.created_at > 1000] # like a WHERE
df = df.groupby('something', num_yes = ('yes', 'sum')) # like a GROUP BY
df = df[df.num_yes > 2]   # like a HAVING, filtering on the result of a GROUP BY
df = df[['num_yes', 'something1', 'something']] # pick the columns I want to display, like a SELECT
df.sort_values('sometthing', ascending=True)[:30] # ORDER BY and LIMIT
df[:30]
```

In other words, it's interoperable and simple enough to use anywhere. That's not to say there aren't downsides (especially when dealing with tremendously large datasets), but that's why there are other equally viable solutions outside of RDMS.

There are other components to SQL. For example, a function can sit inside another function to make it a "nested function". SQL can also do JOIN to a newly created table with data derived off the source table, which is called a "self join".

### Redundant

There are several ways to design a database. You can "normalize" it by making it have less redundant data points:

- ID#
- Name
- Address
- ZIP code
- Age
- Birthday
- Phone #
- Email

This is fine to cut down on [memory](computers-memory.md), but it takes a long time for the computer to read through it all. In this situation, it'd have to read through the Name, Address, ZIP code, and Age fields on *every single applicable record* just to get to the Birthday. That adds up if you do it 8,000,000 times.

Instead, we can "denormalize" the data to make it take up more room, but make it easier to access:

- ID#
- Name
- Address
- ZIP code

- ID#
- Name
- Age
- Birthday

- ID#
- Name
- Phone #
- Email

## NoSQL

SQL isn't the only way to structure data. Another option is to use NoSQL (with things like managers like MongoDB).

In short, NoSQL refers to any data that isn't held strictly in a relational database. This means you don't have to store related information about a particular record in a host of data tables.

At one time, SQL databases were a great idea to hold lots of information, back when the cost of storing data was more expensive than the cost of having developers work on it. However, now that we can hold comparatively huge amounts of information cheaply, NoSQL makes more sense.

When you scale up to [enterprise-grade](computers-distsys-enterprise.md) databases, NoSQL makes even more sense, since developers have more options to store data without being bound by the old relational database rules.

## More information

SQL:

- [Select Star SQL](https://selectstarsql.com/) - a much better and in-depth tutorial than this could ever be
- [SQL Police Department](https://sqlpd.com/) - solve crimes while learning SQL
