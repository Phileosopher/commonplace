
in 1989, There was a holy war over text editors. IDEs weren't a thing yet, so we all coded in a text editor. I was firmly in the Emacs camp, but most of my co-workers loved vi.

DIFFICULT BUT AWESOME:
The vim text editor is very Nintendo Hard to learn, as you rely entirely on keyboard macros to do things that aren't typing. Once mastered, however, vim is a very efficient editor. Modern vim is pretty softcore compared to its predecessor vi. At least vim has arrows working as expected.
vim's "opponent", emacs, is similar: like vim, it uses key combinations for all editor control. It's practically impossible to learn, but capable of doing anything. And anything actually means anything. Standard builds of EMACS (which includes a LISP dialect specific to EMACS built right in) have included web browsers, email clients, image viewers, and just about any other tool you might possibly want to use. It can call the compiler, too, in case you happen to want to write a little code somewhere along the way. (Coders and sysadmins, pretty much the only people who bother with something like EMACS or vi, have been known to do all their work from inside EMACS with built-in tools.)

You can set VI mode in your *-nix environment by adding the following to your ~/.profile file:set -o viWhen you have VI mode set, you can hit Escape (which puts you in command mode), then / to put yourself in search mode. Type the search text, then hit Enter. The first match will be the most recent command that matches the search string. If that's not the one you want, hit / followed by Enter to search for the next occurrence. Also in bash, if you have recently executed a command, you can hit the hotkey ! along with the first letter of the recent command to re-run it. The ! gives you access to the history directly. If you want to see your command-line history, execute the history command, which provides a numbered list of the commands you've executed,
Each time the pushd command is issued, it shows the existing directories already on the stack.
find . -regex ".*Db\.java"

## IDE Projects

Merge /toolbox from PhilosAccounting into /toolbox for Phileosopher
- Make an "export" feature to send Toolbox out to an HTML-parsed Bookmarks Export (for importing to others' Bookmarks library)

[How to Contribute to Open-Source Projects - A Handbook for Beginners](https://www.freecodecamp.org/news/how-to-contribute-to-open-source-handbook/)
- left off at "## How to Set Up a Development Environment"
- will need to revisit FLOSS at "## Understanding Project Structure and Workflow"

[Modern IDEs are magic. Why are so many coders still using Vim and Emacs? - Stack Overflow](https://stackoverflow.blog/2020/11/09/modern-ide-vs-vim-emacs/)
- good discussion on vim/emacs by contrast
- i.e., it's all about habit and convention (i.e., the programmer's brain-hand interface is the slowest point)
