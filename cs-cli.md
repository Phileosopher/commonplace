
# Command line interfaces

If you're unfamiliar with computers, it can be overwhelming when you're given a black screen with something like "C:\Users\Bob>" and a blinking cursor.

However, unless someone takes the time to specifically [program](cs-langs.md) a [visual interface](engineering-design.md), a "command-line interface" (CLI) is the easiest way to work with computers.

It goes by multiple names:

- Shell: it was an analogy that contrasted with the [kernel](cs-os.md)
- Terminal emulator ([Linux](cs-os-unix.md)): it was originally emulating teletype printers, which were typewriters that sent data to print elsewhere (a technology advancement of the telegram)
- Command prompt ([Windows](cs-os-windows.md)): a prompt to run a command

At first, command interfaces sound daunting. In a sense, shells are effectively the combination of a [programming language](cs-langs.md) and an interface for running programs.

This makes shell scripts absurdly powerful inside a computer. Once you have experience with terminals/command prompts, you'll actively *want* that sort of interface, for several reasons:

1. Typing in a console gives immediate feedback. [Mice and touchscreens](cs-mouse.md) don't always indicate when you clicked something, and moving your hand to the mouse is time-intensive when you're doing *lots* of computer work.
2. Almost everything you can do by [typing](cs-keyboard.md) into the computer can often be automated. [Mouse clicks](cs-mouse.md) and touches, by contrast, are very difficult to automate. If you have to do something 3,429 times (which is often the case with tons of computer data), the less physical labor for yourself the better.
3. Many of the most powerful and versatile tools in computing are CLI-only, since it's easy for software engineers to visually design. Sometimes, they're elegantly simple compared to a visual interface (e.g., the "ping" command).
4. If you're working on a [large-scale system](cs-distsys-enterprise.md) like a web server or a very tiny system like a [Raspberry Pi](cs-embedded.md), extra [graphics](engineering-graphics.md) can be clunky and slow everything down, and can be another possible thing that could break down.
5. Text output can display a *lot* of information at one time, without the risk of rich text cluttering the flow of information.
6. Text output is very easy to copy-paste in a CLI for diagnostic reasons, emailing your boss, capturing what happened, print to a file/paper copy, or simply for posterity.

On many consumer-targeted [operating systems](cs-os.md), the console is hidden or nonexistent, though you can often see the console blink for a half-second when a console-based program activates, especially when [booting](cs-boot.md).

One wacky quirk that isn't readily apparent on [Unix-likes](cs-os-unix.md) and [database management systems](database.md) is that you *need* a closing character or the system will bug out in a strange sub-console.

- e.g., not putting a complete argument into bash will give a useless prompt that won't act until you complete the argument, which will usually output an error.
- e.g., not putting a semicolon in MariaDB wll give a useless prompt until you enter a semicolon.
