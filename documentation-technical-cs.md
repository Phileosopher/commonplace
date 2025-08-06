
# Computer technical documentation

All the [general rules of technical documentation](documentation-technical.md) apply, but there are some extra quirks inside the tech industry.

Since all computer code in the first place is a set of instructions for a computer, the documentation can be easily derived by copying the things that make the software:

1. Copy the flow of how everything works inside the software and across various nodes.
2. Simplify it by emphasizing *what* things do and throwing out the details that describe *how* things work, which should make a reliable technician manual.
3. Simplify even further by describing what *to* do to interact with it, which should make a thorough user's manual.

## Comments

Commenting code is *very* critical for any developer who wishes to leave something for future developers.

- The code itself doesn't need to be explained if it's obvious what it does.
- However, if there are particularly complicated elements, it helps to summarize what's going on.
- Indicate any engineering trade-offs or reasons that justify a particular decision on why a particular design pattern was made over other potential approaches.
- The code will be written once, but will be read and re-read potentially *hundreds* of times by many people, so think ahead to save time for them (and future you).
- Spell out the entire thing: don't abbreviate stringPool as sp unless you're letting everyone know what you're talking about

Always leave a few comments, on *any* project:

- A simple module-level header comment
- Comments for significant data and type declarations
- A brief per-class and per-method header

## Git Commits

To keep track of what you change, it's *critical* to maintain good notes, especially [when things break](computers-software-maintenance.md). Thankfully, Git has the feature built-in with mandatory notes for "commits".

There are a few important ways to write good Git commits:

- Explain what you changed, why you changed it, and what it affects. Assume the reader has no clue what you're addressing.
- Capitalize the first word and don't end with punctuation, though [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0-beta.2/) are all lowercase.
- Use a direct, to-the-point tone of [writing](language-writing.md) (avoid kinda, I think, maybe, et al.).
- Specify what commit type you're making:
  - feat - new feature comes with the changes
  - fix - fixed a [bug](computers-software-redesign.md)
  - chore - changes that aren't fixes/features that don't modify src or test files
  - refactor - redesigned code
  - docs - updates to documentation such as README
  - style - changes that don't affect the code's meaning, such as whitespace or missing semicolons
  - test - adds new/more tests
  - perf - performance improvements
  - ci - "continuous integration": merging multiple developers' work
  - build - affects "build system" or external "dependencies"
  - revert - restores a previous commit, often because something broke
- The first line is 50 characters max, and the body is 72 characters max.

## Changelogs

When [software gets updated](computers-software-versionctrl.md), people need to understand what happened and why. While it's tempting to dump system logs into it (such as a git log), the purpose of a "changelog" or "release notes" is to allow a technical person to understand what changed without having to observe the source code directly.

There are several things to *always* do in a changelog:

- Specify any changes that significantly change. Keep track of them in a streaming format (usually with the latest version change at the top, and adding new versions above it). Avoid informing much about minor changes that don't affect the user.
- Keep the information simple for the users. They never need to know exactly what lines of code changed, but they do need to know how it changes the way they interact with the software.
- To avoid confusion on dates, use the date convention of YYYY-MM-DD, which goes from largest to smallest order.
- As of 2022, there is no reliable [universal standard](standards-computers.md) for changelogs.
- If a version was "yanked", it's still important to indicate the changes if the version was publicly released, often by putting [YANKED] after the version number.
- It's perfectly fine to rewrite changelogs. Just make sure that it's clarifying or adding information, such as unspecified releases, and make sure to not devote *too* much time to it when you should be doing something more productive.

## Data Visualizations

The domain of visualizing data is a geekier implementation of standard [graphics](graphics.md) development, but its most valuable use is in depicting technical concepts. For that reason, it does broadly classify as "technical documentation".

The simplest form of data visualization is via [markdown text](markdown.md). It allows for rich text formatting in plaintext documents. However, it never allows for much latitude in visual diagrams.

For many visualizations, Unified Modeling Language (UML) allows for quick text-based sketches of diagrams.

Many technical software honor UML and markdown, which opens up many varieties of [graphical](graphics.md) possibilities for a pleasant [user experience](design-uxui.md).

Also, ASCII is monospaced, so it can be used to make ASCII charts and diagrams, beyond simply ASCII art.

## Additional Information

[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0-beta.2/)
