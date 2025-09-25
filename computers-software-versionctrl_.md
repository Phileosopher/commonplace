
# How version control works

Since developers are human, software isn't a fire-once-and-done matter. To allow for these imperfections, software comes in "versions".

## Version numbers

To keep things simple, programmers tend to release program versions with numbers on them, using a few possible conventions.

The first, and oldest, convention is to name versions by their relationship to a programmer's goals:

- "Alpha" versions are barely-working programs that were quickly pushed out (e.g., v0.36). Features are sparse and it barely works (at least, by the developer's standards).
- "Beta" versions are nearly complete, but may still have bugs (e.g., v0.80).
- "Final" versions are finished, but there are often little details that need tweaking afterward (e.g., v1.02).
- After that, most developers tend to make version numbers based on features they've added. On a large project with many developers, it's not uncommon to add letters and extended numbers afterward (e.g., v2.58.7216.R35).

Alternately, if you have a particularly long-term [software development cycle](mgmt-2_projects-cs.md), you can use the year and month the version is released instead (e.g., v.2019.10).

In general, there are 3 categories of update, which may have different versioning:

1. Major updates, which will make the [API](computers-programming-basics.md) integrations no longer work the same.
2. Minor updates, which will allow the older versions to be "backwards-compatible".
3. "Patches", which make backwards-compatible bug fixes.

One long-term solution is to roll out beta/testing versions with odd numbers (e.g., v1.25) and stable versions with even (e.g., v1.26).

In long-term software where there's a certain level of public exposure for that software (such as entire [operating systems](computers-os.md)), the [marketing](marketing.md) people will often make catchy names to reflect the version (e.g., Precise Pangolin, Big Sur, Lollipop).

## Control software

To keep track of changes while creating software, most programmers like to use a version control system such as Microsoft's [GitHub](https://github.com) or Apache's [SubVersion](https://subversion.apache.org/).

Version control systems let software engineers figure out when code was updated, so they can trace where they may have made a mistake.

Further, many version control systems track each *line* of code, so they can easily trace exactly what happened.

## Git

In the early 2000s, most software development had various issues with awkward "commits" and "branches", and BitKeeper had provided a relatively seamless solution. However, their software wasn't [open-source](legal-ip-floss.md) and BitKeeper's terms of service indicated that they weren't allowed to "reverse-engineer" the software. However, because it worked, much of [Linux](computers-os-unix.md) was maintained with it.

The issue came to a severe conflict when a developer was able to figure out how to work with BitKeeper by observing [network packets](networks-computer.md) (which wasn't *technically* reverse-engineering). While it didn't outright violate the terms of service, BitKeeper shut down Linux development.

In ten days, the creator of [Linux](computers-os-unix.md), Linus Torvalds, created [Git](https://git-scm.com/) as a response to the need. Its design philosophy was "release early, iterate often", which has had a profound elegance. However, its mandatory complexities and [command-line interface](computers-cli.md) require a steep learning curve to understand it.

Git's complexity was for a reason: it accommodates decentralized versions held on [various systems](computers-distsys.md) with a local copy of the code, and is portable enough to be used by any [large organization](computers-distsys-enterprise.md) and integrates well into most [IDEs](computers-software-ide.md).

The flow of activity in a normal IDE is pretty straightforward with Git:

1. Modify code, with the IDE of your choice tracking the changes.
2. "Staging" the information to be ready for the final code. This way, people can review it to make sure it's error-free. Make any more changes, and those can be staged as well.
3. "Commit" the code, which makes it populate the changes to all the "repositories" of that code. The developer usually leaves [notes](language-writing-documentation-cs.md) about what changed as well.

If the source code is maintained by someone else, then a programmer can submit a "pull request", which requires the maintainer to approve the change before submitting it.

In a strictly practical sense, a Git version control is simply a [file folder](computers-files.md), but with a hidden .git folder that keeps logs of *all* the changes, including alternate versions of everything that has changed. A developer can also have a .gitignore file with [regular expression](computers-programming-basics.md) conditions that prevent certain files from being tracked by Git.

However, there are [security issues](computers-cysec.md) with Git. Since it keeps track of *every* change, information that may be accidentally uploaded to a public repository may effectively stay there indefinitely, even if it gets deleted. However, it has become more [encrypted](encryption.md) over time.

### GitHub

[GitHub](https://github.com/) came in 2008 as a public Git repository that also served as a type of [social media](networks-social.md), which pushed it into widespread adoption.

While Git is a completely open-source experience, Git*Hub* is a private organization that began as [a startup](entrepreneur-1_why.md) to host Git instances. It scaled upward to become like almost any other [large-scale company](mgmt-1_why.md), then was bought out by Microsoft in 2018 to become another part of [Big Tech](faang.md).

Beyond being a form of social media, Github's most advantageous offering is GitHub Copilot, which scraped *all* the GitHub code to create an [AI-assisted model](computers-ai.md) to help with coding.

## Forks

When someone is [developing software](computers-software-design.md), there are a variety of reasons to make an alternative version of that software:

- Cleaning up code to make it more stable, but it'll take a long time.
- Someone else wants to add [features](computers-programming-basics.md) of their own, or wants to take over the project.
- The developer gave up on that implementation of the project and wants to start over, but other people are depending on it.
- The developer lost his mind, and someone has to continue developing with a "known-good" implementation of the code.

For whatever reason, the developer can "fork" the version. This new version is identical at first, but is meant to change differently than its original version.

One of the most common ways to fork is to "checkout" a previous version. It allows rolling back to a previous version without committing. That second version can be committed separately without affecting the master/main. When/if the developer wants to "merge" them together, they simply have to run a [console](computers-cli.md) command.

Forks, however, need to be "merged" together, and it is *not* a straightforward experience. It's not always clear when the last code edit was done, and by whom, especially across time zones. This holds true as well for any changed dependencies as well.

## Phasing out

Unfortunately, all the changes in software mean that it's not usually sensible to support only the latest version:

- Feature-rich things like [programming languages](computers-languages.md) often have many plugins, libraries, and optional features that many users may not want to update right away when the current version is "known-good". This is especially true with [enterprise software](computers-distsys-enterprise.md), where an update can be very expensive and time-consuming.
- Often, users can fit into archetypes based on how they update. Some people want a stable experience and will be slower to update, while others want the latest immediately.

For that reason, a project cycle will often "end-of-life" certain versions once they know 100% that a newer version has everything the older version has, though sometimes the developer will have rebuilt the next version of the system to be [closed-source](legal-ip-floss.md).

Sometimes, a version has to be "yanked" if it failed miserably. Maybe that version could easily [hacked](hacking.md), or it might have crashed core features. For whatever reason, certain version numbers become *very* dangerous to keep around without patching or uninstalling/reinstalling with another version ASAP.

Some [enterprise software](computers-distsys-enterprise.md) can be so feature-laden and complex that most managers won't feel comfortable bringing it to version 1.x. This can cause extreme consternation in developers [as the project persists](computers-software-maintenance.md), and can provoke rewriting the code from scratch or trying to close out all [bug reports](computers-software-redesign.md). This psychological effect can also express with releasing to 2.x, 3.x, and so on.

Eventually, Git may be phased out itself, likely with a new system that implements [blockchain](computers-blockchain.md).

## Additional reading

- [Semantic Versioning](https://semver.org/)
- [ZeroVer: 0-based Versioning](https://0ver.org/)