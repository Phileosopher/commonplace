
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

## productivity

[My productivity app is a never-ending .txt file (2022) | Hacker News](https://news.ycombinator.com/item?id=39432876)
- check the comments for vim/emacs shortcuts

## history

[IDEs we had 30 years ago | Hacker News](https://news.ycombinator.com/item?id=38792446)
[The IDEs we had 30 years ago... and we lost](https://blogsystem5.substack.com/p/the-ides-we-had-30-years-ago-and)

## text editor

[Text editing on mobile: the invisible problem | Hacker News](https://news.ycombinator.com/item?id=37630804)
[The invisible problem - Scott Jenson](https://jenson.org/text/)

### apple

[9 years of Apple text editor solo dev | Hacker News](https://news.ycombinator.com/item?id=38866170)
[9 years of Apple text editor solo dev](https://papereditor.app/dev)

[Nerdy internals of an Apple text editor | Hacker News](https://news.ycombinator.com/item?id=39603087)
[Nerdy internals of an Apple text editor](https://papereditor.app/internals)

## simple dev environments

[Nix Dev Guide](https://nix.dev/tutorials/ad-hoc-developer-environments)
Ad hoc developer environments¶

## emacs


[The benefits of everything being a buffer in Emacs | Hacker News](https://news.ycombinator.com/item?id=34580943)
[Marcin Borkowski: 2023-01-30 The benefits of everything being a buffer](https://mbork.pl/2023-01-30_The_benefits_of_everything_being_a_buffer)

[Elite for Emacs (2015) | Hacker News](https://news.ycombinator.com/item?id=34550574)
[Elite for Emacs | Sami Salkosuo](https://www.salkosuo.net/2015/10/22/elite-for-emacs.html)

[Emacs 29 is nigh | Hacker News](https://news.ycombinator.com/item?id=33788208)
[Emacs 29 is nigh! What can we expect? // Phundrak's rambling](https://blog.phundrak.com/emacs-29-what-can-we-expect/)

[Batteries included with Emacs (2020) | Hacker News](https://news.ycombinator.com/item?id=29342176)
[Batteries included with Emacs | Karthinks](https://karthinks.com/software/batteries-included-with-emacs/)

[Closing 45% of the open Emacs bugs | Hacker News](https://news.ycombinator.com/item?id=28181575)
[10×10% - Random Thoughts](https://lars.ingebrigtsen.no/2021/08/14/10x10/)

[Improving Emacs Performance | Bytedude](https://web.archive.org/web/20221126113808/https://www.bytedude.com/improving-emacs-performance)

[Bringing GNU Emacs to Native Code (2020) | Hacker News](https://news.ycombinator.com/item?id=27011013)
[[2004.02504] Bringing GNU Emacs to Native Code](https://arxiv.org/abs/2004.02504)

[EmacsConf 2020 Talks | Hacker News](https://news.ycombinator.com/item?id=25324311)
[EmacsConf - 2020 - Talks](https://emacsconf.org/2020/talks/)

[Toward a "modern" Emacs [LWN.net]](https://lwn.net/Articles/832311)

[Building an Intelligent Emacs | Hacker News](https://news.ycombinator.com/item?id=30308272)
[Building an Intelligent Emacs | Ian Y.E. Pan](https://ianyepan.github.io/posts/emacs-ide/)

[Eglot has landed on master: Emacs now has a built-in LSP client | Hacker News](https://news.ycombinator.com/item?id=33277985)
[Eglot has landed on master🆓](https://lists.gnu.org/archive/html/emacs-devel/2022-10/msg01609.html)

[I won an award from the FSF for my contributions to Emacs | Hacker News](https://news.ycombinator.com/item?id=30774724)
[I won an award from the FSF for my contributions to Emacs | Protesilaos Stavrou](https://protesilaos.com/codelog/2022-03-22-libreplanet-fsf-award/)

[Use GNU Emacs | Hacker News](https://news.ycombinator.com/item?id=35006952)
[Use GNU Emacs](https://www2.lib.uchicago.edu/keith/emacs/)

[What's new in Emacs 28.1? | Hacker News](https://news.ycombinator.com/item?id=30930816)
[What's New in Emacs 28.1? - Mastering Emacs](https://www.masteringemacs.org/article/whats-new-in-emacs-28-1)
[What's new in Emacs 29.1 | Hacker News](https://news.ycombinator.com/item?id=37427279)
[What's New in Emacs 29.1? - Mastering Emacs](https://www.masteringemacs.org/article/whats-new-in-emacs-29-1)

[Emacs 29.1 | Hacker News](https://news.ycombinator.com/item?id=36929514)
[Emacs 29.1 Released | Emacs Redux](https://emacsredux.com/blog/2023/07/30/emacs-29-1-released/)

[Bad NEWS, Emacs | Hacker News](https://news.ycombinator.com/item?id=38591584)
[Bad NEWS, Emacs](https://eshelyaron.com/posts/2023-12-10-bad-news.html)

[I just wanted Emacs to look nice - Using 24-bit color in terminals | Hacker News](https://news.ycombinator.com/item?id=39189881)
[I Just Wanted Emacs to Look Nice - Using 24-Bit Color in Terminals | Chad Austin](https://chadaustin.me/2024/01/truecolor-terminal-emacs/)

[Sam Whited](https://blog.samwhited.com/2015/04/the-dharma-of-vi/)
(2015) The Dharma of Vi

[How To Use the Emacs Editor in Linux | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-the-emacs-editor-in-linux)

[A beginner's guide to text editing with Emacs | Enable Sysadmin](https://www.redhat.com/sysadmin/beginners-guide-emacs)

[Getting started with Emacs | Opensource.com](https://opensource.com/article/20/3/getting-started-emacs)

[emacs-tw/awesome-emacs](https://github.com/emacs-tw/awesome-emacs)
list of useful Emacs packages, libraries and others.

### guides

[How to type "blimpy" in Emacs [video] | Hacker News](https://news.ycombinator.com/item?id=37366341)
[🥩How to type "blimpy" in Emacs?🥩 - YouTube](https://www.youtube.com/watch?v=2VOnKMJqIL0)

[Setting up Rust Support in Emacs (And Introducing Rant-o-Vision) | Bytedude](https://web.archive.org/web/20221126112753/https://www.bytedude.com/setting-up-rust-support-in-emacs)

[Secure GPG In Emacs, Featuring Agent Smith | Bytedude](https://web.archive.org/web/20221126121912/https://www.bytedude.com/secure-gpg-in-emacs)

[Emacs - Wikipedia](https://en.wikipedia.org/wiki/Emacs#Emacs_pinky)

[Emacs commands I got by with for years | Hacker News](https://news.ycombinator.com/item?id=38851699)
[Emacs Commands I Got By With For Years - MacAdie Web Blog](https://macadie.info/2023/12/30/emacs-commands-i-got-by-with-for-years/)

[My Emacs Lisp book is finished | Hacker News](https://news.ycombinator.com/item?id=29157859)
[Marcin Borkowski: 2021-11-06 The Emacs Lisp book is finished](https://mbork.pl/2021-11-06_The_Emacs_Lisp_book_is_finished)

[Get things done with Emacs | Hacker News](https://news.ycombinator.com/item?id=33033017)
[Get Things Done with Emacs](https://www.labri.fr/perso/nrougier/GTD/index.html)

[Emacs: Custom Eshell Prompts | Bytedude](https://web.archive.org/web/20221126112522/https://www.bytedude.com/custom-eshell-prompts)

[Top (Programming in Emacs Lisp)🆓](https://www.gnu.org/software/emacs/manual/html_node/eintr)

[System Crafters Videos](https://www.youtube.com/c/SystemCrafters)

### org mode

[Simple Inline Images In Org-Mode | Bytedude](https://web.archive.org/web/20221126114204/https://www.bytedude.com/simple-inline-images-in-org-mode)

[Org Mode's new site | Hacker News](https://news.ycombinator.com/item?id=24903311)
CHECK THE COMMENTS

[Org-mode Workflow:](https://blog.jethro.dev/posts/org_mode_workflow_preview)

[Org Mode Organize Your Life In Plain Text!](http://doc.norang.ca/org-mode.html)

[Basic Intro](http://www.jesshamrick.com/2012/09/10/absolute-beginners-guide-to-emacs)

[Being productive with emacs](https://lucidmanager.org/tags/emacs)

[Org mode beginning at the basics](https://orgmode.org/worg/org-tutorials/org4beginners.html)

[Org mode for beginners](https://orgmodeforbeginners.com/overview)

## vim

[An Intro to Vim for People Who Use Visual Studio Code](https://www.freecodecamp.org/news/vim-for-people-who-use-visual-studio-code)

[Vim for People Who Use Visual Studio Code (Full Article) - DEV Community](https://dev.to/codenutt/vim-for-people-who-use-visual-studio-code-full-article-1j1c)

[How not to be afraid of Vim anymore](https://www.freecodecamp.org/news/how-not-to-be-afraid-of-vim-anymore-ec0b7264b0ae)

[How to Use Vim - Tutorial for Beginners](https://www.freecodecamp.org/news/vim-beginners-guide)

[VimGenius](http://www.vimgenius.com/lessons)

[What is Vim? | Opensource.com](https://opensource.com/resources/what-vim)

[Interactive Vim tutorial](https://openvim.com)

[How to Exit Vim | Hacker News](https://news.ycombinator.com/item?id=21988968)
[how-to-exit-vim/README.md at master · hakluke/how-to-exit-vim](https://github.com/hakluke/how-to-exit-vim/blob/master/README.md)
[hakluke/how-to-exit-vim](https://github.com/hakluke/how-to-exit-vim)
Gorgeous ways to exit Vim :-D (it goes beyond what you expect)

[Show HN: I built an online interactive course that helps you learn Vim faster | Hacker News](https://news.ycombinator.com/item?id=25846347)
[learnvim - practice and learn vim fast, with interactive exercises](https://www.learnvim.com/)

[Show HN: I built an interactive course that helps you learn Vim faster | Hacker News](https://news.ycombinator.com/item?id=32034625)
[Learn Vim the Simple Way](https://www.vimified.com/)

[Vimtutor :: Vimschool](https://vimschool.netlify.app/introduction/vimtutor/)

[VIM Adventures](https://vim-adventures.com/)
VIM Learning Game

[Learn Vim For the Last Time](https://danielmiessler.com/p/vim/)

[Mastering VIM: Your Guide to Efficient Text Editing](https://www.freecodecamp.org/news/mastering-vim-your-guide-to-efficient-text-editing/)

[mhinz/vim-galore](https://github.com/mhinz/vim-galore)
awesome list of tips and resources for Vim

[Daniel Miessler](https://danielmiessler.com/study/vim/)
A vim Tutorial and Primer

[iggredible/Learn-Vim](https://github.com/iggredible/Learn-Vim)
A book for learning the Vim editor the smart way.

[I Made an Extended Version of Vimtutor – Introducing Vimtutor Sequel | Hacker News](https://news.ycombinator.com/item?id=41144843)
[micahkepe/vimtutor-sequel: Vimtutor Sequel - Advanced Vim Tutor Lessons](https://github.com/micahkepe/vimtutor-sequel)

[Vim Racer | Hacker News](https://news.ycombinator.com/item?id=41347051)
[Vim Racer - An Online Game for VIM Navigation](https://vim-racer.com/)

[7 Vim Tips That Changed My Life (With Demo)](https://www.freecodecamp.org/news/7-vim-tips-that-changed-my-life)

[The Future of the Vim Project | Hacker News](https://news.ycombinator.com/item?id=37074452)
[The future of the Vim project](https://groups.google.com/g/vim_dev/c/dq9Wu5jqVTw)

[Vim Boss | Hacker News](https://news.ycombinator.com/item?id=37078719)
[Vim Boss - Neovim](https://neovim.io/news/2023/08)

[Happy birthday Vim (2020) | Hacker News](https://news.ycombinator.com/item?id=29113216)
[Happy birthday!](https://groups.google.com/g/vim_announce/c/bQtQSHTK1sg)

[Bram Moolenaar has died | Hacker News](https://news.ycombinator.com/item?id=37011324)
[Message from the family of Bram Moolenaar](https://groups.google.com/g/vim_announce/c/tWahca9zkt4)

[Foot Pedal Ups Vim Productivity, Brings Ergonomic Benefits](https://hackaday.com/2022/12/16/foot-pedal-ups-vim-productivity-brings-ergonomic-benefits/)

[Plain text journaling in Vim | Hacker News](https://news.ycombinator.com/item?id=36390405)
[Plain Text Journaling · peppe.rs](https://peppe.rs/posts/plain_text_journaling/)

[Moving fast with the core Vim motions | Hacker News](https://news.ycombinator.com/item?id=36312027)
[Moving Blazingly Fast With The Core Vim Motions | Barbarian Meets Coding](https://www.barbarianmeetscoding.com/boost-your-coding-fu-with-vscode-and-vim/moving-blazingly-fast-with-the-core-vim-motions/)

[Vim prank: alias vim='vim -y' | Hacker News](https://news.ycombinator.com/item?id=29837543)
[Vim prank: alias vim='vim -y'](https://learnbyexample.github.io/mini/vim-prank/)

[Vim is Turing-Complete • Buttondown](https://buttondown.email/hillelwayne/archive/vim-is-turing-complete)

[Vim 9 will be dedicated to Sven Guckes | Hacker News](https://news.ycombinator.com/item?id=30416558)
[Sven Guckes passed away](https://groups.google.com/g/vim_announce/c/MJBKVd-xrEE/m/joVNaDgAAgAJ)

[Vim 9.0 | Hacker News](https://news.ycombinator.com/item?id=31936725)
[Vim 9.0 : vim online](https://www.vim.org/vim90.php)

[Tell HN: Vim users, `:x` is like `:wq` but writes only when changes are made | Hacker News](https://news.ycombinator.com/item?id=34287407)

[Sandra Henry-Stocker](http://www.computerworld.com/article/2968352/linux/tricks-to-play-with-vim.html)
Tricks to play with vim

[vimcolorschemes](https://vimcolorschemes.com/)
Trending vim color schemes

[Alexander Vasilyevich Dzyoba](https://alex.dzyoba.com/blog/vim-revamp/)
(2019) How I revamped my Vim setup

[Vincent Danen](https://www.techrepublic.com/blog/linux-and-open-source/using-vi-key-bindings-in-bash-and-zsh/)
(2008) Using vi key bindings in bash and zsh

[Tom Ryder](https://sanctum.geek.nz/arabesque/vim-koans/)
(2016) Vim Koans

[ntpeters/vim-better-whitespace](https://github.com/ntpeters/vim-better-whitespace)
Better whitespace highlighting for Vim

[Fred Hébert](https://ferd.ca/vim-and-composability.html)
Vim and Composability

[Ian Langworth](https://statico.github.io/vim3.html)
Vim After 15 Years

[Roger Guldbrandsen](https://kinbiko.com/vim/my-shiniest-vim-gems/)
(2017) Vim: My Shiniest Gems

[Tom Ryder](https://sanctum.geek.nz/arabesque/vim-anti-patterns/)
(2012) Vim anti-patterns

[Vim Tips Wiki](https://vim.fandom.com/wiki/Highlight_unwanted_spaces)
(2003) Highlight unwanted spaces

[Samuel Walladge](https://www.swalladge.net/archives/2018/06/11/why-vim-2018/)
(2018) Why vim is a solid code editor for 2018

[Joe Nelson aka begriffs](https://begriffs.com/posts/2019-07-19-history-use-vim.html)
(2019) History and effective use of Vim

[George Ornbo](https://shapeshed.com/vim-netrw/)
(2019) Vim: you don't need NERDtree or (maybe) netrw

[VimTricks Archives](https://vimtricks.substack.com/archive)
Vim tricks, tips, plugins, recipes, and more. Learn valuable tips to hone your Vim skills - either novice or advanced!

[Alexander González Fertel](https://alexfertel.hashnode.dev/vim-is-actually-worth-it)
(2021) Vim is actually worth it

[Vimways](https://vimways.org/)
is a Vim-themed advent calendar.
Largely inspired by the early [24ways](https://24ways.org/)
their primary goal is to publish one high quality article about Vim per day during the twenty-four days before Christmas.

[Rajob Raihan](https://levelup.gitconnected.com/why-every-software-engineer-should-use-vim-b9fb97e69d97)
(2022) Why every software engineer should use vim
Conquer the “quitting vim” fear and give it a go

[Zeynel Abidin Öztürk](https://defkey.com/nerdtree-6-shortcuts)
(2020) NerdTree 6.9.10 keyboard shortcuts

[Justin M. Keyes](https://vimconf.org/2019/slides/justin.pdf)
(2019) We Can Have Nice Things
Neovim and the state of text editor art in 2019.
[Video](https://www.youtube.com/watch?v=Bt-vmPC_-Ho)
[Source](https://lobste.rs/s/wfj5y2/neovim_state_text_editor_art_2019)

[Derek Prior](https://thoughtbot.com/blog/my-life-with-neovim)
(2016) My Life with NeoVim

### guides

[A Vim Guide for Advanced Users | Hacker News](https://news.ycombinator.com/item?id=26284618)
[A Vim Guide for Advanced Users](https://thevaluable.dev/vim-advanced/)
A Vim Guide for Advanced Users

[Matthieu Cneude](https://thevaluable.dev/vim-expert/)
A Vim Guide For Experts

[Why Vim Is More than Just an Editor - Vim Language, Motions, and Modes Explained : coding](https://old.reddit.com/r/coding/comments/11395gf/why_vim_is_more_than_just_an_editor_vim_language)

[Intermediate Vim - Dennis Hotson](https://dn.ht/intermediate-vim/)

[zzapper](http://rayninfo.co.uk/vimtips.html)
Best of Vim Tips / compiled from 16 Years of Vi + 10+ years of Vim

[Steve Losh](http://learnvimscriptthehardway.stevelosh.com/)
Free book : Learn Vimscript the Hard Way, learn how to customize vim
[Steve Losh](http://learnvimscriptthehardway.stevelosh.com/chapters/17.html)
Status Lines

[Tom Ryder](https://sanctum.geek.nz/arabesque/shell-from-vi/)
(2017) Shell from vi

[Lucas Fernandes da Costa](http://lucasfcosta.com/2017/01/23/Quick-vIM-Tips-That-Will-Save-Your-Life.html)
(2017) Quick vIM Tips That Will Save Your Life

[Dimitri Merejkowsky](https://dmerej.info/blog/post/lets-have-a-pint-of-vim-ale/)
(2017) Let's have a pint of (vim) ale!
Write a custom language linter for ale

[Bennett Hardwick](https://bennetthardwick.com/beginner-advanced-vim-tips/)
(2019) Advanced beginner Vim tricks

#### history

[Where Vim Came From](https://twobithistory.org/2018/08/05/where-vim-came-from.html)

#### editor modes

[Vim Editor Modes Explained](https://www.freecodecamp.org/news/vim-editor-modes-explained)

#### go dev

[Preslav Mihaylov](https://pmihaylov.com/vim-for-go-development/)
(2021) How to set up Vim for Go Development

[Jogendra Kumar](https://jogendra.dev/using-vim-for-go-development)
(2020) Using Vim for Go Development

[Paschalis Tsilias](https://tpaschalis.github.io/vim-go-setup/)
(2019) My Vim IDE setup for Go.

### neovim

[Neovim 0.5 is overpowering | Hacker News](https://news.ycombinator.com/item?id=27291302)
[Neovim (0.5) Is Overpowering | CrispDev](https://crispgm.com/page/neovim-is-overpowering.html)

[Leaving Neovim for Zed | Hacker News](https://news.ycombinator.com/item?id=41284322)
[Leaving Neovim for Zed • Steve Simkins](https://stevedylan.dev/posts/leaving-neovim-for-zed/)

## vim vs emacs

[Differences between Emacs and Vim - Stack Overflow](https://stackoverflow.com/questions/1430164/differences-between-emacs-and-vim)

[Emacs vs. Vim: Differences Between the Top Terminal Editors for Linux - LinuxForDevices](https://www.linuxfordevices.com/tutorials/linux/emacs-vs-vim)

## vs code

[How to Set Up VS Code for Web Development in A Few Simple Steps](https://www.freecodecamp.org/news/how-to-set-up-vs-code-for-web-development)

[VSCode.one](https://vscode.one/)

[Reflections on IDEA vs VS Code | Hacker News](https://news.ycombinator.com/item?id=26367410)
[reflections on the competing IDEs · GitHub](https://web.archive.org/web/20210306141609/https://gist.github.com/rambingthoughts/c28fc8caa07733443c77551fb096d830)

[VSCode deprecates Enable Telemetry, auto-enrolls you in Telemetry? | Hacker News](https://news.ycombinator.com/item?id=28812486)
[Imgur: The magic of the Internet](https://imgur.com/a/nxvH8cW)

[Making bracket pair colorization faster | Hacker News](https://news.ycombinator.com/item?id=28692470)
[How We Made Bracket Pair Colorization 10,000x Faster In Visual Studio Code](https://code.visualstudio.com/blogs/2021/09/29/bracket-pair-colorization)

[Microsoft previews free Visual Studio Code for the Web • The Register](https://www.theregister.com/2021/09/01/microsoft_previews_free_visual_studio)

### snippets

[Visual Studio Code Snippets - the Definitive VS Code Snippet Guide for Beginners](https://www.freecodecamp.org/news/definitive-guide-to-snippets-visual-studio-code)

## vs code vs emacs

[Emacs or VS Code? Why and How I'm Slowly Switching to GNU Emacs | by Tommaso De Ponti | Better Programming](https://betterprogramming.pub/emacs-or-vs-code-why-and-how-im-slowly-switching-to-gnu-emacs-ea33c0837ac4)

## atom

[Atom on Slack](http://atom-slack.herokuapp.com/)
Slack community for Atom Text editor

### go dev

[Pipat Methavanitpong](https://fulcronz27.wordpress.com/2016/03/07/setting-atom-for-golang-on-windows/)
(2016) Setting Atom for Golang on Windows

[Marcio Castilho](http://marcio.io/2015/07/supercharging-atom-editor-for-go-development/)
(2015) Supercharging the Atom Editor for Go Development

## eclipse

[Stop Making Students Use Eclipse (2020) | Hacker News](https://news.ycombinator.com/item?id=29136820)
[Stop Making Students Use Eclipse | Nora Codes](https://nora.codes/post/stop-making-students-use-eclipse/)

## enterprise ide

[Shivam](http://www.trysudo.com/7-tips-for-a-productive-development-setup-on-linux/)
7 tips for a productive development setup on Linux

## jetbrains

[JetBrains invites developers to join the Fleet Public Preview Program | Hacker News](https://news.ycombinator.com/item?id=33175373)
[Introducing the Fleet Public Preview | The Fleet Blog](https://blog.jetbrains.com/fleet/2022/10/introducing-the-fleet-public-preview/)

[Dear JetBrains, Don't mess with your UI | Hacker News](https://news.ycombinator.com/item?id=33242730)
[Dear JetBrains. Don't mess with your UI.](https://neil.computer/notes/dear-jetbrains-dont-mess-with-your-ui/)

## sublime text

[Sublime Text 4 | Hacker News](https://news.ycombinator.com/item?id=27230042)
[Sublime Text 4 - News - Sublime HQ](https://www.sublimetext.com/blog/articles/sublime-text-4)

## misc IDEs

[BBEdit is 30 years old today | Hacker News](https://news.ycombinator.com/item?id=31008290)
[BBEdit - free text editor](https://groups.google.com/g/comp.sys.mac.announce/c/gvPGyuX3UCs)
[BBEdit: Where Respect Is Due | Hacker News](https://news.ycombinator.com/item?id=36303371)
[Where Respect Is Due : App Store Story](https://apps.apple.com/us/story/id1435835881)

[Why LSP? | Hacker News](https://news.ycombinator.com/item?id=31151048)
[Why LSP?](https://matklad.github.io//2022/04/25/why-lsp.html)

[Cool desktops don't change | Hacker News](https://news.ycombinator.com/item?id=31769604)
[Cool desktops don't change 😎 - Tyler Cipriani](https://tylercipriani.com/blog/2022/06/15/choose-boring-desktop-technology/)

[Show HN: Carbide - A New Programming Environment | Hacker News](https://news.ycombinator.com/item?id=12355102)
[Carbide Alpha | Buggy But Live!](https://alpha.trycarbide.com/)

[CudaText - Home](https://cudatext.github.io/)

[Light Table](https://lighttable.com/)

### web dev focused

[A modern, open source code editor that understands web design](https://brackets.io/)
(free)

### python focused

[Thonny - Python IDE for beginners | Hacker News](https://news.ycombinator.com/item?id=34424854)
[Thonny, Python IDE for beginners](https://thonny.org/)

### gui focused

[GNUstep: Open-source, Object-oriented, Cross-platform Development Environment | Hacker News](https://news.ycombinator.com/item?id=29537172)
[GNUstep.org](https://gnustep.github.io/)
