
# The Python programming language

A high-level language. It's universally accepted, and dominates all across the world. Like [BASIC](cs-langs-specific-basic.md) once was, it's great for beginners to learn, but comes with drawbacks that beginners won't really care about.

The philosophy behind Python is to create something elegant, simple and clear. For that reason, the language is very readable and simple to understand.

Python can be *either* interpreted or compiled, which is part of its versatility.

Beyond simpler things like [web development](cs-software-webdev.md) it's very, very powerful, and the language of choice for heavy-math implementations like [machine learning](cs-ai-ml.md).

However, Python doesn't scale well:

- The packaging is bad when there are lots of cross-cutting dependencies.
- There's no concurrency designed into the language.
- The code ends up becoming heavily typed, since it's not the dominant form of expression in the language.

This is barely noticeable in a small project, but becomes incredibly painful in a [large production system](cs-distsys-enterprise.md). People working on small projects love it, but not the ones who have to manage millions of lines of code.

In practice, Python is great for [creating an MVP](entrepreneur-4_freelancing.md) as fast as possible, but bogs down and traps developers later.
