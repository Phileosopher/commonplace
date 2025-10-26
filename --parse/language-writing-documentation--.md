
## architecture documentation

[Mike Crittenden](https://critter.blog/2020/12/03/the-you-get-one-diagram-approach-to-architecture-documents/)
(2020) The “You Get One Diagram” approach to architecture documents

[Dustin Barnes](https://dev9.com/blog-posts/2017/5/increasing-software-transparency-with-lightweight-architectural-decision-records)
(2017) Increasing Software Transparency with Lightweight Architectural Decision Records

## ARCHITECTURE file

[Architecture.md (2021) | Hacker News](https://news.ycombinator.com/item?id=39494925)
[Architecture.md | Hacker News](https://news.ycombinator.com/item?id=26048784)
[ARCHITECTURE.md](https://matklad.github.io//2021/02/06/ARCHITECTURE.md.html)

## code vs documentation

Apply all of our pragmatic principles to documentation as well as to code.
- PRAGMATIC PROGRAMMER IS GOOD FOR THIS AS WELL??

Times you need to present the same documentation in different formats: a printed document, Web pages, online help, or perhaps a slide show. The typical solution relies heavily on cut-and-paste, creating a number of new independent documents from the original. This is a bad idea: a document's presentation should be independent of its content. If you are using a markup system, you have the flexibility to implement as many different output formats as you need. You can choose to have <H1>Chapter Title</H1> generate a new chapter in the report version of the document and title a new slide in the slide show. Technologies such as XSL and CSS can be used to generate multiple output formats from this one markup.

As long as your original markup is rich enough to express all the concepts you need (including hyperlinks), translation to any other publishable form can be both easy and automatic. You can produce online help, published manuals, product highlights for the Web site, and even a tip-a-day calendar, all from the same source-which of course is under source control and is built along with the nightly build.

## comments and code health

[Sarah Drasner](https://css-tricks.com/the-art-of-comments/)
(2017) The Art of Comments

[Stack Overflow](https://stackoverflow.com/questions/184618/what-is-the-best-comment-in-source-code-you-have-ever-encountered)
What is the best comment in source code you have ever encountered? - closed

[Artur Śmiarowski](https://alemil.com/guidelines-for-writing-readable-code)
(2018) 23 guidelines for writing readable code

[Alex Zurek](https://spin.atomicobject.com/2017/08/15/todo-comments/)
(2017) TODO Comments Don’t Work

[Dori Reuveni and Kevin Bourrillion](https://testing.googleblog.com/2017/07/code-health-to-comment-or-not-to-comment.html)
(2017) Code Health: To Comment or Not to Comment?

[Marc Eaddy](https://testing.googleblog.com/2017/11/obsessed-with-primitives.html)
(2017) Code Health: Obsessed With Primitives?

[Joël Spolsky](https://www.joelonsoftware.com/2005/05/11/making-wrong-code-look-wrong/)
(2005) Making Wrong Code Look Wrong

[What are the odds that some idiot will name his mutex ether-rot-mutex (2017) | Hacker News](https://news.ycombinator.com/item?id=31524669)
[Ether's Web: "What are the odds that some idiot will name his mutex ether-rot-mutex!"](https://etherrotmutex.blogspot.com/2017/07/what-are-odds-that-some-idiot-will-name.html)

[Open source code with swearing in the comments is statistically better than that without : programming](https://old.reddit.com/r/programming/comments/110mj6p/open_source_code_with_swearing_in_the_comments_is/)
[Open source code with profanity in comments is statistically better | Hacker News](https://news.ycombinator.com/item?id=36584464)
[Open source with profanity in comments is statistically better than code without profanity | From Linux](https://blog.desdelinux.net/en/open-source-with-profanity-in-comments-is-statistically-better-than-code-without-it/)

[Writing Well-Documented Code - Learn from Examples | Hacker News](https://news.ycombinator.com/item?id=28416269)
[Writing Well-Documented Code - Learn from Examples - Code Catalog](https://codecatalog.org/2021/09/04/well-documented-code.html)

[Comment the Why and the What • Buttondown](https://buttondown.email/hillelwayne/archive/comment-the-why-and-the-what)

## computer manuals

[The strangest computer manual ever written | Hacker News](https://news.ycombinator.com/item?id=34224174)
[The Strangest Computer Manual Ever Written](https://ironicsans.substack.com/p/the-strangest-computer-manual-ever)

## creating processes

[CrowdSync](https://www.crowdsync.io/blog/2018/01/17/7-tips-for-creating-a-new-process/)
(2018) 7 Tips for Creating a New Process

## documentation

[Tanja Roth](https://opensource.com/article/17/12/7-rules)
(2017) 7 rules for avoiding documentation pitfalls

[Carmen Bourlon](https://www.javascriptjanuary.com/blog/document-like-a-journalist)
Document like a Journalist

[Steve Losh](http://stevelosh.com/blog/2013/09/teach-dont-tell/)
(2013) Teach, Don't Tell
about documentation

[Felix](https://thinkingsideways.net/working/culture/2019/01/03/knowledge-transfers.html)
(2019) The Trouble with Knowledge Transfers

[Brad Appleton](http://wiki.c2.com/?LocalityOfReferenceDocumentation)
Locality Of Reference Documentation (LoRD)
> * Code and documentation should be kept as close as feasible, but no closer!
> * Minimizing the amount of documentation that must be created and maintained in the first place is probably one of the most important aspects of applying LoRD (perhaps even a precursor)

[Graydon Hoare](https://graydon2.dreamwidth.org/193447.html)
(2014) always bet on text

[Justin Garrison](https://www.justingarrison.com/blog/2021-03-15-the-document-culture-of-amazon/)
(2021) The Document Culture of Amazon

[Four kinds of documentation | Hacker News](https://news.ycombinator.com/item?id=21289832)
[A Framework for Writing Better Documentation | Hacker News](https://news.ycombinator.com/item?id=26002656)
[Documentation System](https://documentation.divio.com/)

[Patterns in Confusing Explanations | Hacker News](https://news.ycombinator.com/item?id=28254630)
[Patterns in confusing explanations](https://jvns.ca/blog/confusing-explanations/)

## DRY principle

Suppose we have a specification that lists the columns in a database table. We'll then have a separate set of SQL commands to create the actual table in the database, and probably some kind of programming language record structure to hold the contents of a row in the table. The same information is repeated three times. Change any one of these three sources, and the other two are immediately out of date. This is a clear violation of the DRY principle. To correct this problem, we need to choose the authoritative source of information. This may be the specification, it may be a database schema tool, or it may be some third source altogether. Let's choose the specification document as the source. It's now our model for this process. We then need to find a way to export the information it contains as different views-a database schema and a high-level language record, for example.

[Nicolò Pignatelli](https://hackernoon.com/this-is-not-the-dry-you-are-looking-for-a316ed3f445f)
(2018) This is not the DRY you are looking for

[Jamie Wong](http://jamie-wong.com/2013/07/12/grep-test/)
(2013) Too DRY - The Grep Test

## error messages and bug reporting

[Remove "This incident will be reported." from user warnings | Hacker News](https://news.ycombinator.com/item?id=35752237)
[Remove "This incident will be reported." from user warnings. · sudo-project/sudo@6aa320c](https://github.com/sudo-project/sudo/commit/6aa320c96a37613663e8de4c275bd6c490466b01)

[This Message Does Not Exist | Hacker News](https://news.ycombinator.com/item?id=40535868)
[This message does not exist | Mark J. Nelson](https://www.kmjn.org/notes/message_existence.html)

[Feynman’s Razor | Hacker News](https://news.ycombinator.com/item?id=40612285)
[Feynman's Razor - by Defender of the Basic](https://defenderofthebasic.substack.com/p/feynmans-razor)

[What's in a Good Error Message? - Gunnar Morling](https://www.morling.dev/blog/whats-in-a-good-error-message)
[Gunnar Morling](https://www.morling.dev/)
[GitHub - gunnarmorling/awesome-opensource-data-engineering: An Awesome List of Open-Source Data Engineering Projects](https://github.com/gunnarmorling/awesome-opensource-data-engineering)

[Write better error messages | Hacker News](https://news.ycombinator.com/item?id=33261125)
[When life gives you lemons, write better error messages | by Jenni Nadler | Wix UX](https://wix-ux.com/when-life-gives-you-lemons-write-better-error-messages-46c5223e1a2f)

## Heuristic for contenteditable rich-text editors

Editor should:

Be stable

Be open source

Handle soft breaks

Be able to manipulate styles on block level elements

Be able to manipulate styles on inline level elements

Be able to manipulate classes on block level elements

Be able to manipulate classes on inline level elements

Be able to alter custom attributes on block level elements

Be able to alter custom attributes on inline level elements

Cache the selection

Have iframing capabilities as well as inline mode capability

Change the tag type of nodes

Clear the format

Have a concise api

Support various module loaders

  AMD & Common.js

Should have an organization backing the service and have a potential paid support plan

Should copy & paste from Microsoft word

## knowledge management system

[PKMS](https://old.reddit.com/r/PKMS/)

## markdown

[Peter Ritchie's Blog - Data URLs in Markdown](https://blog.peterritchie.com/posts/data-urls-in-markdown)

[MDN converted to Markdown | Hacker News](https://news.ycombinator.com/item?id=33477842)
[MDN => Markdown](https://openwebdocs.org/content/posts/markdown-conversion/)

[Render mathematical expressions in Markdown On GitHub | Hacker News](https://news.ycombinator.com/item?id=31438864)
[Render mathematical expressions in Markdown - The GitHub Blog](https://github.blog/changelog/2022-05-19-render-mathematical-expressions-in-markdown/)

[Daichi](https://hackernoon.com/boost-your-productivity-using-markdown-b8a84fc2a089)
(2017) Boost your productivity using Markdown.

[CommonMark](http://commonmark.org/help/)
syntax reference for CommonMark, a rationalized version of Markdown syntax

[CommonMark](http://spec.commonmark.org/dingus/)
Try CommonMark / CommonMark Demo

[Import and Export Markdown in Google Docs | Hacker News](https://news.ycombinator.com/item?id=40982118)
[Google Workspace Updates: Import and export Markdown in Google Docs](https://workspaceupdates.googleblog.com/2024/07/import-and-export-markdown-in-google-docs.html)

[Mermaid Gantt diagrams for displaying distributed traces in Markdown (2023) | Hacker News](https://news.ycombinator.com/item?id=40981954)
[TIL: Mermaid Gantt diagrams are great for displaying distributed traces in Markdown - brycemecum.com](https://brycemecum.com/2023/03/31/til-mermaid-tracing/)

## markdown vs rst

[I prefer rST to Markdown | Hacker News](https://news.ycombinator.com/item?id=41120254)
[Why I prefer rST to markdown • Buttondown](https://buttondown.email/hillelwayne/archive/why-i-prefer-rst-to-markdown/)

## mobi vs epub

[Retirement of Amazon MOBI eBook file format | Hacker News](https://news.ycombinator.com/item?id=32421350)
[Product Announcement: Retirement of Amazon MOBI eBook file format | Microsoft Press Store](https://www.microsoftpressstore.com/promotions/product-announcement-retirement-of-amazon-mobi-ebook-142421)

## non-code contributions

[Non-code contributions to open source | Hacker News](https://news.ycombinator.com/item?id=39356320)
[Non-code contributions are the secret to open source success](https://github.com/readme/featured/open-source-non-code-contributions)

[Two open source projects with great architecture documentation | Hacker News](https://news.ycombinator.com/item?id=39819409)
[Two open source projects with great documentation • johnjago.com](https://johnjago.com/great-docs/)

[hightower/nocode](https://github.com/kelseyhightower/nocode)
No code is the best way to write secure and reliable applications. Write nothing; deploy nowhere.

## note-taking - Kindle

[Nate Hoffelder](https://the-digital-reader.com/2015/02/21/how-to-download-your-kindle-notes-and-highlights-and-export-them/)
(2015) How to Download Your Kindle Notes and Highlights and Export Them

## note-taking - obsidian

[Writing down what I do in Obsidian | Hacker News](https://news.ycombinator.com/item?id=33527296)
[Writing Down What I Do-In Obsidian - Sympolymathesy, by Chris Krycho](https://v5.chriskrycho.com/journal/writing-down-what-i-do-in-obsidian/)

## note-taking - Zettelkasten

[James McTiernan aka Jimmy](https://theproductiveengineer.net/how-to-use-zettelkasten-as-a-programmer-or-developer/)
(2021) How To Use Zettelkasten as a Programmer or Developer

## pdf manipulation

[iOS Tip: Export PDFs from Print Preview with 3D Touch](https://www.macstories.net/ios/ios-tip-export-pdfs-from-print-preview-with-3d-touch)

[The drama in trying to convert election PDFs to Spreadsheets | Hacker News](https://news.ycombinator.com/item?id=35272227)
[The drama in trying to convert election PDFs to Spreadsheets - Mark Essien](https://markessien.com/posts/drama_of_transcription/)

## plain text

[Plain Text Project](https://plaintextproject.online/)
[Tools](https://plaintextproject.online/tools.html)
by Scott Nesbitt et al

[Plain Text Accounting | Hacker News](https://news.ycombinator.com/item?id=25745615)
[Plain Text Accounting, a guide to Ledger and friends | Hacker News](https://news.ycombinator.com/item?id=28420797)
[Plain Text Accounting (PTA) - plaintextaccounting.org](https://plaintextaccounting.org/)
[Ledger Syntax Quick Reference](http://plaintextaccounting.org/quickref)
by Simon Michael et al

## README and github profile

[Rejected GitHub profile achievements | Hacker News](https://news.ycombinator.com/item?id=36607439)
[Flet/rejected-github-profile-achievements: 😵 GitHub achievements that did not make the cut.](https://github.com/Flet/rejected-github-profile-achievements)

[Is there a way to represent a directory tree in a GitHub README.md?](https://stackoverflow.com/questions/23989232/is-there-a-way-to-represent-a-directory-tree-in-a-github-readme-md/35889620)

[Tom Preston-Werner](https://tom.preston-werner.com/2010/08/23/readme-driven-development.html)
(2010) Readme Driven Development

[Lauri Apple](https://opensource.com/open-organization/17/10/readme-maturity-model)
(2017) documentation : a maturity model for READMEs
Your step-by-step guide to more effective documentation

## rtfm

[293: RTFM - explain xkcd](https://www.explainxkcd.com/wiki/index.php/293:_RTFM)

## sequence diagrams - UML

[Sequence diagrams, the only good thing UML brought to software development | Hacker News](https://news.ycombinator.com/item?id=36342931)
[Sequence diagrams, the only good thing UML brought to software development · MermaidChart Blog](https://www.mermaidchart.com/blog/posts/sequence-diagrams-the-good-thing-uml-brought-to-software-development)

[Why UML "Really" Died • Buttondown](https://buttondown.email/hillelwayne/archive/why-uml-really-died)

[Can Formal Methods Succeed where UML Failed? • Buttondown](https://buttondown.email/hillelwayne/archive/can-formal-methods-succeed-where-uml-failed)

[Has UML died without anyone noticing? | Hacker News](https://news.ycombinator.com/item?id=26934577)
[Has UML Died Without Anyone Noticing? | Ernesto Garbarino](https://garba.org/posts/2021/uml/)

[Lee Copeland](https://www.stickyminds.com/article/state-transition-diagrams)
(2003) State-Transition Diagrams - Testing UML Models

## technical communication

[Gojko Adzic](https://gojko.net/2012/01/23/splitting-user-stories-the-hamburger-method/)
(2012) Splitting user stories -- the hamburger method

[How to communicate effectively as a developer | Hacker News](https://news.ycombinator.com/item?id=33370870)
[How to communicate effectively as a developer](https://www.karlsutt.com/articles/communicating-effectively-as-a-developer/)

[Ask HN: How to level up your technical writing? | Hacker News](https://news.ycombinator.com/item?id=31859040)

## technical communication - screenshots

[Take more screenshots (2022) | Hacker News](https://news.ycombinator.com/item?id=34544199)
[Take more screenshots | Hacker News](https://news.ycombinator.com/item?id=32215277)
[You should take more screenshots - alexwlchan](https://alexwlchan.net/2022/screenshots/)

## technical documentation - Apple

[On Apple's Piss-Poor Documentation | Hacker News](https://news.ycombinator.com/item?id=25046691)
[On Apple's Piss-Poor Documentation - Liss is More](https://www.caseyliss.com/2020/11/10/on-apples-pisspoor-documentation)

## technical documentation - diagrams

[How to create technical conceptual diagrams](https://krutiepatel.com/blog/how-to-create-technical-conceptual-diagrams)

[I print the motherboard layouts and stick them to the lids of my servers : homelab](https://old.reddit.com/r/homelab/comments/tui1t9/i_print_the_motherboard_layouts_and_stick_them_to)

## technical documentation

[Chastity Blackwell](https://opensource.com/article/17/10/7-deadly-sins-documentation)
7 deadly sins of documentation

[Fred Hébert](https://ferd.ca/don-t-be-a-jerk-write-documentation.html)
Don't be a Jerk: Write Documentation

[Mislav Marohnić](https://mislav.net/2014/02/hidden-documentation/)
(2014) Every line of code is always documented

[Dimitris Staikos](http://www.commonsense4commonpeople.net/2008/11/the-code-is-the-documentation.html)
(2008) The code is THE documentation
why the code is not the documentation

[Love and hate relationship with documentation : ProgrammerHumor](https://old.reddit.com/r/ProgrammerHumor/comments/12l147p/love_and_hate_relationship_with_documentation)

[An engineer's tips for writing documentation devs love | Hacker News](https://news.ycombinator.com/item?id=31945863)
[How to Criticize Computer Scientists (2001) | Hacker News](https://news.ycombinator.com/item?id=26609492)
[How To Criticize Computer Scientists](https://www.cs.purdue.edu/homes/dec/essay.criticize.html)

[Writing documentation for your house | Hacker News](https://news.ycombinator.com/item?id=38444577)
[Writing Documentation for Your House](https://luke.hsiao.dev/blog/housing-documentation/)

[Just Simply - Stop saying how simple things are in our docs | Hacker News](https://news.ycombinator.com/item?id=35759449)
[Just Simply | Stop saying how simple things are in our docs](https://justsimply.dev/)

[90% of software engineering done today is integrating poorly documented APIs | Hacker News](https://news.ycombinator.com/item?id=31226100)
[Austen Allred on X: "90% of the software engineering being done today is integrating poorly documented API A with poorly documented API B." / X](https://twitter.com/Austen/status/1520792630853918722)

[GitHub SHA256 change broke many package managers : programming](https://old.reddit.com/r/programming/comments/10phfvm/github_sha256_change_broke_many_package_managers/)
- ALWAYS communicate like crazy about things you change

[The Localization Handbook - How to Translate Your Website Into Different World Languages [Full Book]](https://www.freecodecamp.org/news/localization-book-how-to-translate-your-website)
- make sure to consider ALL possible spoken languages
- if it's more than 1 language, keep the words as simple as possible to prevent mistranslation (e.g., thing explainer translator)

[Note-taking 101: from Evernote to Obsidian - CoCoSys lab](https://anneurai.net/2021/03/16/note-taking-101-from-evernote-to-obsidian/)
- markdown-based note-taking is, by far, THE best way to take notes
- anything else out there is essentially adding extra complexities beyond what normal people need
- however, it's also useful for DRM by the owner of the notes system
- of course, it can't be the ONLY note system:
	- 2D data - spreadsheet
	- 3D+ data - proper database
	- visual design - drawing/art/graphics software
	- mindmap - visual/data visualization software

Technical documentation is VITALLY important
- instead of answering questions all day, a developer can simply communicate that in writing and point people to that
- most Tier 1/2 helpdesk tech support(TTfixing) will be dramatically improved by good documentation, even if the users are too dense to understand

[Use forums rather than Slack/Discord to support developer community | Hacker News](https://news.ycombinator.com/item?id=29154216)
[You should use forums rather than Slack/Discord to support developer community - Dan Moore!](https://www.mooreds.com/wordpress/archives/3451)
- Slack and Discord are TERRIBLE for software code: the information gets lost in the chat feed
- by contrast, forums give room for information to be easily accessed, and are also more public

## technical documentation - MDN

[MDN Plus | Hacker News](https://news.ycombinator.com/item?id=27302702)
[MDN Plus](https://developer.mozilla.org/en-US/plus)
[Introducing MDN Plus: Make MDN your own - Mozilla Hacks - the Web developer blog](https://hacks.mozilla.org/2022/03/introducing-mdn-plus-make-mdn-your-own)

[MDN Web Docs evolves: Lowdown on the upcoming new platform | Hacker News](https://news.ycombinator.com/item?id=24931862)
[MDN Web Docs evolves! Lowdown on the upcoming new platform - Mozilla Hacks - the Web developer blog](https://hacks.mozilla.org/2020/10/mdn-web-docs-evolves-lowdown-on-the-upcoming-new-platform/)
[MDN](https://developer.mozilla.org/en-US/)
[Developer.Mozilla](https://developer.mozilla.org/)
[MDN Web Docs](https://developer.mozilla.org/en-US/)
[Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn)
[mdn web docs](https://developer.mozilla.org/en-US/)
[mdn web docs](https://web.archive.org/web/20210102182957/https://developer.mozilla.org/en-US/)
the mozilla web docs for referencing things to do with the web such as html or css. w3schools on steroids _sorta
Developer Resources

## technical documentation - OpenBSD

[Why is the OpenBSD documentation so good? | Hacker News](https://news.ycombinator.com/item?id=32515928)
[Solene'% : Why is the OpenBSD documentation so good?](https://dataswamp.org/~solene/2022-08-18-why-openbsd-documentation-is-good.html)

## text editor - Kate

[Kate editor on all platforms | Hacker News](https://news.ycombinator.com/item?id=40032869)
[Kate on all Platforms - 2024 | Ignorance is bliss...](https://cullmann.io/posts/kate-on-all-platforms-2024/)

## type system notation

[How should I read type system notation? | Hacker News](https://news.ycombinator.com/item?id=37138807)
[How should I read type system notation? - Programming Language Design and Implementation Stack Exchange](https://langdev.stackexchange.com/questions/2692/how-should-i-read-type-system-notation)

## uses page

[GitHub - wesbos/awesome-uses: A list of /uses pages detailing developer setups, gear, software and configs.](https://github.com/wesbos/awesome-uses)
[/uses](https://uses.tech/)

## version updates

[Extremely Linear Git History | Hacker News](https://news.ycombinator.com/item?id=33704297)
[Extremely Linear Git History](https://westling.dev/b/extremely-linear-git)

[Pratul Kalia](https://blog.uncommon.is/using-git-to-generate-versionname-and-versioncode-for-android-apps-aaa9fc2c96af)
Using git to generate versionName and versionCode for Android apps

## word processors

[Bruce Bastian, WordPerfect co-creator, has died | Hacker News](https://news.ycombinator.com/item?id=40858583)
[Bruce Bastian, BYU alum-turned-tech pioneer and equality advocate, dies at 76 | News, Sports, Jobs - Daily Herald](https://www.heraldextra.com/news/local/2024/jun/17/bruce-bastian-byu-alum-turned-tech-pioneer-and-equality-advocate-dies-at-76/)

[Proton launches its own version of Google Docs | Hacker News](https://news.ycombinator.com/item?id=40864914)
[Proton launches its own version of Google Docs](https://www.engadget.com/proton-launches-its-own-version-of-google-docs-100044471.html)

## writing technical content

[The economics of writing technical books | Hacker News](https://news.ycombinator.com/item?id=40830332)
[The Economics of Writing Technical Books - The Architect Elevator](https://architectelevator.com/strategy/book-author-economics/)

[Jeff Atwood](https://blog.codinghorror.com/do-not-buy-this-book/)
(2007) Do Not Buy This Book

[Heinrich Hartmann](https://www.heinrichhartmann.com/posts/writing/)
(2022) Writing for Engineers

[Charles Petzold](http://www.charlespetzold.com/blog/2007/10/081247.html)
(2007) Hard Work, No Pay: What's the Point?
Charles Petzold on writing books, reading books, and exercising the internal UTM
> Of Course Writing Books is Hard! But that's what makes it fun and rewarding! You really shouldn't try to write a book unless you have a fire in your belly. If you have that fire, then nothing that Jeff Atword or I can say will discourage you.

[Michael Foord](http://www.voidspace.org.uk/python/articles/technical-writing.shtml)
(2009) Writing a Technical Book
IronPython in Action with Manning Publications

[Ben Watson](http://www.philosophicalgeek.com/2014/11/10/tips-for-writing-a-programming-book/)
(2014) Tips for Writing a Programming Book

[Della Anjeh aka Black Queen of Tech](https://eng.lyft.com/awesome-tech-specs-86eea8e45bb9)
(2017) How to Write Awesome Tech Specs

[Quora](https://www.quora.com/What-is-publishing-a-book-with-OReilly-Media-like)
(2014) What is publishing a book with O'Reilly Media like?

[Thomas Wedell-Wedellsborg](https://hbr.org/2017/01/are-you-solving-the-right-problems)
(2017) Are You Solving the Right Problems?
[Jim Leonardo](https://jimsrulesregardingeverything.com/2017/03/11/export-to-pdf-a-tale-in-understanding-the-business-need/)
article titled "Export to PDF: A Tale in Understanding the Business Need"

[Matt Stauffer](https://mattstauffer.com/blog/why-i-wrote-my-book-with-oreilly/)
(2016) Why I wrote my book with O'Reilly

[James Routley](https://routley.io/posts/starting-a-programming-blog/)
(2017) Advice on starting a programming blog

## markdown

[GitHub - croqaz/awesome-markup: Awesome list of markdown-like goodies](https://github.com/croqaz/awesome-markup)

[dyrobooks](https://dyrobooks.com/blog/2018/04/03/using-markdown/)

[Mundi Mark - All About Markup & Markdown](https://mundimark.github.io/)
[Awesome Markdown](https://github.com/mundimark/awesome-markdown)

[GitHub - mundimark/why-text: Why Markdown? Why Text? The Past, Present and Future of Writing and Publishing](https://github.com/mundimark/why-text)

[MarkdownGuide](https://www.markdownguide.org/)
Guide for Markdown (.md)
[Tools | Markdown Guide](https://www.markdownguide.org/tools/)
[Extended Syntax | Markdown Guide](https://www.markdownguide.org/extended-syntax/)
[Hacks | Markdown Guide](https://www.markdownguide.org/hacks/)

[The Ultimate Guide to Writing & Publishing with Markdown](https://ghost.org/changelog/markdown/)

[udacity-fsnd/markdown-guide.md at main · br3ndonland/udacity-fsnd](https://github.com/br3ndonland/udacity-fsnd/blob/main/info/markdown-guide.md)

## obsidian

[kmaasrud/awesome-obsidian: Awesome stuff for Obsidian](https://github.com/kmaasrud/awesome-obsidian)

## technical communication

[The Plain Person's Guide to Plain Text Social Science](https://plain-text.co/)

[GitHub - jenniferlynparsons/awesome-writing: An awesome list of information to help developers write better, kinder, more helpful documentation and learning materials](https://github.com/jenniferlynparsons/awesome-writing)

## technical documentation

[Write the Docs](http://www.writethedocs.org/guide/)
Documentation Guide : a best practice handbook for building, structuring, and writing software documentation, for creating more wonderful documentation in the world
:star:

[GitHub - writing-resources/awesome-scientific-writing: A curated list of awesome tools, demos and resources to go beyond LaTeX](https://github.com/writing-resources/awesome-scientific-writing)

[GitHub - tiffanyjachja/writing-resources: DevRel Writing Resources](https://github.com/tiffanyjachja/writing-resources)

[GitHub - dharmelolar/technical-writing-resources: A compilation of technical writing resources](https://github.com/dharmelolar/technical-writing-resources)

[GitHub - BolajiAyodeji/awesome-technical-writing: A curated list of awesome resources: articles, books, videos, tools, podcasts about technical writing.](https://github.com/BolajiAyodeji/awesome-technical-writing)

[Introduction - Spinning Up documentation](https://spinningup.openai.com/en/latest/user/introduction.html)

## asciidoc and asciidoctor

[Using AsciiDoc and Asciidoctor to write documentation Tutorial](https://www.vogella.com/tutorials/AsciiDoc/article.html)

## commit messages

[Conventional Commits](https://www.conventionalcommits.org/)
Commit message specification
The Conventional Commits specification proposes introducing a standardized lightweight convention on top of commit messages. This convention dovetails with SemVer, asking software developers to describe in commit messages, features, fixes, and breaking changes that they make.

[Commit messages guide](https://github.com/RomuloOliveira/commit-messages-guide)
a guide to understand the importance of commit messages.

## github profile and README

[How To Create A Kickass GitHub Profile Page](https://catalins.tech/how-to-create-a-kickass-github-profile-page)

[GitHub Snake](https://dev.to/mishmanners/how-to-enable-github-actions-on-your-profile-readme-for-a-contribution-graph-4l66)
Enable Snake Game on GitHub ReadMe

[Create Awesome Git readMe Profile | by Eresh Gorantla | The Startup | Medium](https://medium.com/swlh/create-awesome-git-readme-profile-84efa0bcda3b)

[GitHub - kylelobo/The-Documentation-Compendium: Various README templates & tips on writing high-quality documentation that people want to read.](https://github.com/kylelobo/The-Documentation-Compendium)
Various README templates & tips on writing high-quality documentation that people want to read.

[Manually Create A Markdown Table Of Contents For Your GitHub Readme](https://www.setcorrect.com/portfolio/work11)

[Akash Nimare](https://medium.com/@meakaakka/a-beginners-guide-to-writing-a-kickass-readme-7ac01da88ab3)
(2016) A Beginners Guide to writing a Kickass README ✍

## knowledge management system

[GitHub - brettkromkamp/awesome-knowledge-management: A curated list of amazingly awesome articles, people, applications, software libraries and projects related to the knowledge management space](https://github.com/brettkromkamp/awesome-knowledge-management)

[Handwritten Notes & Study Materials Online | Lecture Notes](https://lecturenotes.in/)

## lightweight markup language

[Lightweight markup language @ Wikipedia](https://en.wikipedia.org/wiki/Lightweight_markup_language)

## sequence diagrams - UML - PlantUML

[PlantUML](http://plantuml.com/guide)
Drawing UML with PlantUML : PlantUML Language Reference Guide

## TeX - LaTeX

[Typst: An easy to learn alternative for LaTex | Hacker News](https://news.ycombinator.com/item?id=41014941)
[GitHub - typst/typst: A new markup-based typesetting system that is powerful and easy to learn.](https://github.com/typst/typst)

[How to Run LaTeX Projects Locally (for Free) On Windows](https://www.freecodecamp.org/news/how-to-run-latex-projects-locally-for-free-on-windows/)

## TeX

[TeX for the Impatient - GNU Project - Free Software Foundation (FSF)🆓](https://www.gnu.org/software/teximpatient)

[Texinfo - GNU Documentation System - GNU Project - Free Software Foundation (FSF)🆓](https://www.gnu.org/software/texinfo)

## unicode characters

[GitHub - jagracey/Awesome-Unicode: A curated list of delightful Unicode tidbits, packages and resources.](https://github.com/jagracey/Awesome-Unicode)
