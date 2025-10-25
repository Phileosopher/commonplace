
# How software is redesigned and fixed

Code can be finicky. Depending on the language, one missing semicolon or tab can mean the entire program doesn't work.

In fact, the only difference between a functioning computer and a failing one is literally 203 key characters of specific assembly code. The only reason we don't run into more issues is because engineers work tirelessly to make computer information as close to 100% reliable as possible.

## Errors

Errors come from 2 facts:

1. Computers do *exactly* what people tell them to.
2. People make mistakes in telling computers what to do.

Thus, computers make incredibly fast, incredibly accurate mistakes. These are called "errors" or "bugs".

**Syntax errors** are errors in the syntax because the person writing the code didn't follow the instructions precisely. The [IDE](computers-software-ide.md) usually points this out before even running the code, (usually underlined in red) so the programmer can correct it before running the code.

**Runtime errors** are errors that *[feel](mind-feelings.md)* logical, but aren't. They tend to crash the program, website, or computer because the computer has instructions that will *never* stop the functioning of the program. In the old days, the entire computer's operating system would freeze when it ran out of [memory](computers-memory.md), but these days the operating system will detect the "stack overflow" and shut down the program before the situation becomes too extreme.

**Logic errors** are when the computer did everything correctly, but the human didn't. For whatever reason, the [information output](engineering-screen.md) doesn't match what *should* happen. These are frustrating because it *should* work fine, but the engineer successfully created something useless for their [purposes](purpose.md).

Often, logic errors earlier in the code's execution will create runtime errors later. This is *extremely* common in complicated computer activities, such as [operating systems](computers-os.md) or [high-graphics](engineering-graphics.md) [games](computers-software-gamedev.md). Shrewd developers hide the error messages while the brilliant ones fix them.

Another easy way to avoid logic errors is to practice [good coding habits](programming-tech.md).

There are a *ton* of simple rookie mistakes with [file/folder management](computers-files.md) that create logic errors:

- Naming the file/webpage incorrectly (e.g., "My File With Spaces In It.html" will *not* work on an older computer or a website)
- Failing to reference the correct file (e.g., "CaseSensitive.txt" isn't "casesensitive.txt")
- Failing to reference the correct folder/path ("./docs/image.jpg" is [*not* the same](computers-cli.md) as "../docs/image.jpg")

One good practice is to name the development folder with a space and, preferably, a permitted special character. That way, you can catch errors *before* someone else's computer runs it.

**Platform errors** are issues with the code once it hits the real world: [network](networks-computer.md) issues, [hard drive](computers-memory.md) failure, invalid [file permissions](computers-cysec.md), etc.

The easiest way to save misery long-term is to have preset error messages at the beginning of the code (e.g., "Syntax Error", "Runtime Error"). Even simply putting "error" as the output of an "if statement" for an error will go a long way to prevent misery.

## Debugging

You'll often fail. Most professional software engineers spend most of their time examining *others'* failures at implementing sound, rational logic. [Failure is normal](success-2_attitude.md).

To remove bugs, programmers have to "debug". This requires finding what you did wrong, then fixing it.

If you ever see an error message, read it:

1. If it's in a small prompt that quickly goes away, don't just click through it without reading it! Instead, take a screenshot or write down the error codes.
2. If the computer was programmed to be particularly helpful, it'll specify the line of code or memory address where it failed.
3. A few web searches for what it says will go a *long* way to discovering what's wrong.

Computers give a *lot* of information about runtime errors. They frequently store many log files *all over the [file system](computers-os.md)*. In fact, they can sometimes store so many "plaintext" error log files that it often creates [memory](computers-memory.md) bloat.

If there's a logic error, one way to find it is to modify the code to PRINT at various places in the code. By doing this, you can see what the computer has in memory at specific points in time and figure out if the failure happened before or after that point.

In a sophisticated program, you'll want to pause it at a certain point to see what it's doing. By setting a "breakpoint", you can pause the program until you press a key to continue. At that point, you can easily see what PRINT gave you before it overwrites it with something later on.

Fixing bugs can be complicated, depending on what you're doing. If there's a block of code you still want, for whatever reason, you can clarify all the code syntax as a "comment". That way, the computer won't care about it but the programmer can still refer to it.

The secret to an easy time debugging is to run your program frequently as you work on it. This accomplishes several things:

1. You have many more variations of a "known good" program, meaning there are fewer steps to roll back when something fails.
2. Small issues can snowball *very* quickly with other small issues to create a horrifyingly huge issue, so you can spot them early on.

## Testing

What you test the software on matters tremendously. If you use a high-spec computer compared to most consumer computers (as most tech-savvy people are prone to having), you won't see the glitches from buffer overflow or slowdown from poor memory management.

The only way to thoroughly be prepared for publishing software is with an "end-to-end test", where you run *everything* live, and at the scale you expect to see. This is often difficult to set up individually, but [enterprise-grade](computers-distsys-enterprise.md) development practically needs it.

## Optimizing

Computer programs are often extremely slow when they're first designed. This comes from the fact that the programmer is simply trying to [make something that works](programming-tech.md) more than making something efficient.

A "callback" is computer code that references *other* computer code that will appear later in the sequence of the code:

1. Function A activates and asks for Function B.
2. (other code, where Function A is hung up)
3. Function B activates and returns something.
4. Function A uses whatever Function B returned.

Unfortunately, this can slow down the computer for several reasons:

- The computer has to move forward in the code to the callback function, then backward again to the original code.
- During that time, the code that's waiting on the callback function is "hung", waiting for further input.

There are some ways to fix "callback hell":

- Inside a function, don't reference another function that's inside it. Name and separate out functions into smaller roles.
- Whenever defining things, try to move them to the top of the function ("function hoisting"). The computer tends to grab the definitions, *then* execute the function, so it saves processing time.
- Break apart the tasks into modules that each do 1 thing. This becomes the beginnings of making [libraries and APIs](computers-programming.md).

## Teamwork

One of the advantages of working on a team is that other people can see things you can't.

The [Torvalds principle](lawsaxioms.md) applies here, and most debugging can be done more effectively and easily if there are more people looking at it. This is why [open source](legal-ip-floss.md) can have financial benefits.