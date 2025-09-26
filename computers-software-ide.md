
# What an IDE is

Word processors are technically too advanced for programmers. They add advanced formatting into the [file](computers-files.md) (such as **bold** or *italic*), and some code will represent in odd ways inside the document once it reads it later.

Instead, if you wanted to, you *could* write software into a text file, then compile it each time, then test it after it compiles. But, that's the hard, time-consuming way to do it:

- If the program has an [error](computers-software-redesign.md), it's hard to easily "debug" it without compiling it first, so it's convenient to find errors as soon as possible. Depending on the language, one missing semicolon or tab can mean the entire program doesn't work, so IDEs can catch "syntax errors", and will underline them in red.
- It's not very easy to automate writing tedious things over and over. Try writing "for (int i = 1; i <= n; i++)" 40 times.
- It's not easy to see what you're making as you build it. This is *especially* important for [web](computers-sofware-webdev.md) and [game](computers-software-gamedev.md) development.
- Elaborate programs require multiple files, which means tracking what and where things are and what they reference.
- While files can have code, many languages require compiling, which means the program won't run until it's given a specific command to compile.
- Different [versions](computers-software-versionctrl.md) of code may work differently, and it can be difficult or impossible to track changes in the code without constantly saving alternative versions of a file.

Thus, programmers like to use an IDE ("integrated development environment"). It's a glorified [text editor](computers-cli.md) that expands into a toolbox of various things to let programmers write faster, catch [bugs](computers-software-redesign.md) quicker, and stay organized. Also, depending on the language, it'll also interpret on-the-fly or quickly allow [compilation](computers-compilers.md).

There are a *ton* of IDEs, and they all have their strengths, but they're all designed as [productivity tools](success-4_routine.md). Many features are stock-standard:

- Tab completion, which fills in the rest of the likely text that will follow.

## History

At the beginning, around 1976, were Emacs and Vim:

- Emacs is basically an entire build-it-yourself operating system designed for programming. It runs on the math-based programming language Lisp.
- Vim is a humble text editor (originally "vi") converted to a full-service programming solution (i.e., "vi iMproved").
- Both are highly adaptable, and are still popular because they can be modified to conform to absolutely everything else on this list.
- However, both are also rather old. They predated conventions like Ctrl+Z/X/C/V for Undo/Cut/Copy/Paste, and both use the word "yank" to describe other, more standardized terms (Vim uses "yank" for "copy" and emacs uses it for "paste").

[BBEdit](https://www.barebones.com/products/bbedit/index.html) is a text editor designed for MacOS released around 1992. It added many of the conveniences of a modern IDE, though it didn't adapt to the modular package-driven ecosystem of modern IDEs.

[TextMate](https://macromates.com/) for the MacOS in 2004 may have been the most influential IDE ever. It popularized numerous features including:

- Abbreviation-based snippets - write big chunks of text with shorthand abbreviations.
- Auto-paired characters - matched up the pairing of characters that always went together (e.g., for every "(", there's a ")").
- Fuzzy search - automatically add [regular expressions](computers-programming.md) into search results to give non-exact searches.
- Easily moving between multiple files.

However, it also had a very important detail: it was built primarily around extensions. Developers could build their own features and plugins that could dramatically improve how they worked. However, TextMate's extensions had limitations, which later IDEs would remove.

[Sublime Text](https://www.sublimetext.com/), released in 2008, was "cross-platform" and could run on [Linux](computers-os-unix.md) and [Windows](computers-os-windows.md) instead of simply MacOS. However, it cleaned up TextMate's limits:

- [Linters](computers-software-redesign.md) with [GUI](engineering-graphics.md) components - allowed programmers to visually see what they're failing at before runtime.
- Package control - made it straightforward to browse, install, and update extensions, which *every* IDE afterward would adopt.

However, Sublime Text didn't have package control built-in, and some GUI elements weren't very optimized (because they used custom calls in [Python](computers-languages.md), which isn't very scalable).

Later, in 2014, GitHub (before it was [owned by Microsoft](faang.md) but after Microsoft expressed serious interest in it) designed [Atom](https://atom.io/), which made the package manager built-in. They also displayed graphics inside the software that made it convenient.

In 2015, Microsoft borrowed GitHub's Electron (a very reliable [web/app framework](computers-sofware-webdev.md)) that was released alongside Atom and was able to convert their [Monaco Editor](https://microsoft.github.io/monaco-editor/) into [VS Code](https://code.visualstudio.com/) (or Visual Studio Code), which could run [inside a web browser](https://vscode.dev/) or as a standalone program.

Most modern IDEs plug seamlessly into [git](computers-software-versionctrl.md) (or, in VS Code, GitHub, since Microsoft owns it now).

VS Code is wildly popular because of how easy it is to use. Often, it requires nearly *zero* technical understanding to set it up. Most purists like to say that vim or emacs is the ideal IDE and always will be, similarly to how [Linux enthusiasts often say Arch Linux is the only "true" Linux distro](computers-os-unix.md).

There are a variety of other IDEs that have generally kept pace with all these [trends](trends.md), each with their own strengths and weaknesses:

- JetBrains' [IntelliJ IDEA](https://www.jetbrains.com/idea/) works intimately with Java, which happens to be what much of the internet runs on right now.
- GitHub Copilot has a *very* powerful tab completion, which has a trained [machine learning](computers-ai-ml.md) algorithm that essentially fills in most of the standard code a typical programmer will use frequently.
