
# Compilers

There are two major ways languages can be expressed:

- Compilers are a one-time translation of [high-level code](cs-langs.md) into [assembly code](cs-langs-specific-assembly.md). They're typically time-intensive at the beginning, then run quickly afterward.
- Interpreters run the translation every time the code executes, meaning the software takes a longer time but doesn't require any preliminary installation.

Each language's design will determine whether the code is compiled or interpreted after it has been created.

- Compiled languages include C, C++, and Objective-C.
- Interpreted languages include PHP and JavaScript.
- Some languages use a combination of compilation and interpretation, such as Java, C#, and Python.

## Compiling vs interpreted

Many languages are compiled (e.g., Python, Java, C++). They are very powerful, but must be converted to binaries before they can be run. While they're far more powerful than interpreted languages, how *well* they perform them can vary spectacularly. For example, Java is better at game and web development, Python is better at data analysis and scripting, and C++ is better at making applications and [system programs](cs-os.md).

Scripting/extension/interpreted languages (e.g., Perl, PHP, JavaScript, Ajax) don't need to be compiled, so they're *super* portable and can run almost anywhere, which is why websites run well with them. They're about as high-level as languages get without becoming [no-code programming](cs-langs.md).

These aren't really features of the language, but of the implementation. however, the distinction is still important because it distinguishes between a high-intensity need (for compiling) or a general-purpose need (for scripting).

This further becomes complicated because compilers can convert it ahead-of-time to machine code or just-in-time (JIT) at runtime. While intuition would imply that JIT compilation is slower than ahead-of-time, this isn't always the case, depending on what benchmark matters and the quality of the implementations.
