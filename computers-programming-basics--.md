
## automation

Suppose you wanted to automate code review scheduling and approval. You might put a special marker in each source code file:
/* Status: needs_review */
A simple script could go through all of the source code and look for all files that had a status of needs_review, indicating that they were ready to be reviewed. You could then post a list of those files as a Web page, automatically send e-mail to the appropriate people,

Letting the (automated) wizards have their way leaves your knowledge shallow and leaves you limited to what the wizards can already do for you.

## avoid manual procedures

Don't Use Manual Procedures:
People just aren't as repeatable as computers are. Nor should we expect them to be. A shell script or batch file will execute the same instructions, in the same order, time after time.

## built-in debugging

Every module can have its own unit test built into its code, and these tests can be performed automatically as part of the regular build process.

Tracer code is lean but complete, and forms part of the skeleton of the final system.

What sorts of things might you choose to investigate with a prototype? Anything that carries risk. Anything that hasn't been tried before, or that is absolutely critical to the final system. Anything unproven, experimental, or doubtful. Anything you aren't comfortable with. Its value lies not in the code produced, but in the lessons learned.

## changing objects

If you need to change an object's state, get the object to do it for you.

## common mistakes

Don't leave "broken windows" (bad designs, wrong decisions, or poor code) unrepaired. Fix each one as soon as it is discovered. If there is insufficient time to fix it properly, then board it up.

Nothing is more dangerous than an idea if it's the only one you have.

## deliberate programming

Program deliberately:
Don't code blindfolded. Attempting to build an application you don't fully understand, or to use a technology you aren't familiar with, is an invitation to be misled by coincidences.
Proceed from a plan.
Document your assumptions.
Don't just test your code, but test your assumptions as well. Don't guess; actually try it. Write an assertion to test your assumptions

Are there dusty corners of your primary programming language that you rarely visit?
- Regular expressions are extremely powerful and tragically underutilized.
- Multithreaded programming
- stream libraries
- network programming APIs
- utilities available for dealing with collections or lists?

The more successful you are, the more likely you are to make a fatal mistake. When you've got everything going for you, you're less likely to question your own judgment. When the way you've always done it has always worked, you're less likely to recognize a new way that might work better.

Every wrong note is at most one step away from a right one. What makes improvisations bad is when the improviser doesn't know what to do when the wrong note pops out.

"I don't know" is not a phrase for the insecure.

Heroes never panic.

## design by contract

The concept of Design by Contract: What is a correct program? One that does no more and no less than it claims to do. Documenting and verifying that claim is the heart of Design by Contract

Be strict in what you will accept before you begin, and promise as little as possible in return. Remember, if your contract indicates that you'll accept anything and promise the world in return, then you've got a lot of code to write!

## focusing on the problem

Program Close to the Problem domain: By coding at a higher level of abstraction, you are free to concentrate on solving domain problems, and can ignore petty implementation details.

## global vs local

Avoid global data. Explicitly pass any required context into your modules.

## human-readable code

While the code for parsing a "real" language may be harder to write, it will be much easier for people to understand, and to extend in the future with new features.

The units you use make a difference in the interpretation of the result. If you say that something will take about 130 working days, then people will be expecting it to come in pretty close. However, if you say "Oh, about six months," then they know to look for it any time between five and seven months

Human-readable forms of data, and self-describing data, will outlive all other forms of data and the applications that created them.

In explaining the problem to another person you must explicitly state things that you may take for granted when going through the code yourself. By having to verbalize some of these assumptions, you may suddenly gain new insight into the problem.

## keep it small

It is easier to write relatively small, self-contained components than a single large block of code.

If components have specific, well-defined responsibilities, they can be combined with new components in ways that were not envisioned by their original implementors.

If I dramatically change the requirements behind a particular function, how many modules are affected?

## law of demeter

Using The Law of Demeter will make your code more adaptable and robust.

## managing a knowledge portfolio - DRY principle

The DRY principle: Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.

Duplication we see falls into one of the following categories:
Imposed duplication. Developers feel they have no choice-the environment seems to require duplication.
Inadvertent duplication. Developers don't realize that they are duplicating information.
Impatient duplication. Developers get lazy and duplicate because it seems easier.
Interdeveloper duplication. Multiple people on a team (or on different teams) duplicate a piece of information.

Sometimes, duplication seems to be forced on us. With a bit of ingenuity you can normally remove the need for duplication. Often the answer is to write a simple filter or code generator. Structures in multiple languages can be built from a common metadata representation using a simple code generator

The trick is to make the process active: this cannot be a one-time conversion, or we're back in a position of duplicating data.

## managing a knowledge portfolio

Your knowledge and experience are your most important professional assets. Unfortunately, they're expiring assets. Your knowledge becomes out of date as new techniques, languages, and environments are developed.

Managing a knowledge portfolio is very similar to managing a financial portfolio: Serious investors invest regularly-as a habit. Diversification is the key to long-term success. Smart investors balance their portfolios between conservative and high-risk, high-reward investments. Investors try to buy low and sell high for maximum return. Portfolios should be reviewed and rebalanced periodically. Buy low, sell high. Learning an emerging technology before it becomes popular can be just as hard as finding an undervalued stock, but the payoff can be just as rewarding.

Learn at least one new language every year. Different languages solve the same problems in different ways. By learning several different approaches, you can help broaden your thinking and avoid getting stuck in a rut. If you've used only makefiles and an editor, try an IDE, and vice versa.

Keep the low-level knowledge in the code, where it belongs, and reserve the comments for other, high-level explanations.

## modularize

Organize your code into cells (modules) and limit the interaction between them.

## problems with being detail-oriented

No amount of genius can overcome a preoccupation with detail.

"Out with the details!" Get them out of the code. While we're at it, we can make our code highly configurable and "soft"-that is, easily adaptable to changes.

Think declaratively (specifying what is to be done, not how) and create highly dynamic and adaptable programs. We do this by adopting a general rule: program for the general case, and put the specifics somewhere else-outside the compiled code base.

Because business policy and rules are more likely to change than any other aspect of the project, it makes sense to maintain them in a very flexible format.

Rather than construction, software is more like gardening-it is more organic than concrete.

## refactoring

When Should You Refactor? When you come across a stumbling block because the code doesn't quite fit anymore, or you notice two things that should really be merged, or anything else at all strikes you as being "wrong," don't hesitate to change it

Don't try to refactor and add functionality at the same time.

## specialized information

One body of knowledge is neither technical nor domain-specific and won't be outdated at any time soon: the basics of business finance.

## text cases

Make Camel Case: test string becomes testString
Make Screaming Snake Case: test string becomes TEST_STRING
Also available as Make Constant Case
Make Dot Case: test string becomes test.string
Make Header Case: test string becomes Test-String
Also available as Make Train Case
Make No Case: testString becomes test string
Make Flat Case: testString becomes teststring
Make Snake Case: Test string becomes test_string
Make Pascal Snake Case: Test string becomes Test_String
Make Camel Snake Case: Test string becomes test_String
Make Kebab Case: Test string becomes test-string
Make Screaming Kebab Case: Test string becomes TEST-STRING
Make Pascal Case: test string becomes TestString
Make Path Case: test string becomes test/string
Make Sentence Case: testString becomes Test string
Make Sponge Case: Test string becomes tEsT StRiNG
Make Capital Case: Test string becomes Test String
Make Lower Case: Test string becomes test string
Make Upper Case: Test string becomes TEST STRING
Make Title Case: step-by-step instructions becomes Step-by-Step Instructions

## the software developer

Software developers are typically creative, freedom-loving people.

## users' and managers' expectations

The success of a project is measured by how well it meets the expectations of its users. A project that falls below their expectations is deemed a failure, no matter how good the deliverable is in absolute terms.

Gently Exceed Your Users' Expectations

Some consultants call this process "managing expectations"-actively controlling what users should hope to get from their systems. We think this is a somewhat elitist position. Our role is not to control the hopes of our users. Instead, we need to work with them to come to a common understanding of the development process and the final deliverable, along with those expectations they have not yet verbalized.

If you work closely with your users, sharing their expectations and communicating what you're doing, then there will be few surprises when the project gets delivered. This is a BAD THING. Try to surprise your users. Not scare them, mind you, but delight them. Give them that little bit more than they were expecting. The extra bit of effort it requires to add some user-oriented feature to the system will pay for itself time and time again in goodwill. Listen to your users as the project progresses for clues about what features would really delight them.

He had this uncanny ability to predict what you were going to ask him to do and do it before you thought of it. It was like magic. He was only doing things that I had already said I wanted. I had just said them in ways that were subtle enough that even I didn't realize I had said them.

Mind reading not only applies to your managers but also to your customers. If they're giving you the right cues, you might be able to add features that they're either going to ask for or would have asked for if they had realized they were possible.

Start making some notes about what you think your users and managers are going to ask for. Be creative. Try to see the system from their points of view.

## write code that writes code

Write Code That Writes Code:
There are two main types of code generators: Passive code generators are run once to produce a result. From that point forward, the result becomes freestanding-it is divorced from the code generator.

Active code generators are used each time their results are required. The result is a throw-away-it can always be reproduced by the code generator. Often, active code generators read some form of script or control file to produce their results.

It is simpler to express it in a simpler, language-neutral representation and generate the code for both languages,

## abbreviations

[Lieven Vaneeckhaute (denshade)](https://softwareefficiency.wordpress.com/2016/11/30/abbreviations-are-your-false-friend/)
(2016) Abbreviations are your (false) friend!

## building for other devs

[Building for the 99% Developers | Hacker News](https://news.ycombinator.com/item?id=30367781)
[Building for the 99% Developers | Future](https://future.com/software-development-building-for-99-developers/)

## code conferences

[Devoxx](https://www.youtube.com/channel/UCCBVCTuk6uJrN3iFV_3vurg)
Devoxx channel on youtube

[GOTO Conferences](https://www.youtube.com/user/GotoConferences)
video interviews and presentations from GOTO Conferences and GOTO Nights.

[kitze/awesome-conference-practices](https://github.com/kitze/awesome-conference-practices)
Did you like anything in particular about a conference? Did you hate anything? Let's make organizing conferences an easier task 🎉

[GitHub - tech-conferences/confs.tech: Frontend for https://confs.tech](https://github.com/tech-conferences/confs.tech)
[Tech conferences in 2024 and 2025 | Confs.tech](https://confs.tech/#)

## coding can be easy

[Show HN: My 70 year old grandma is learning to code and made a word game | Hacker News](https://news.ycombinator.com/item?id=41217109)
[Grandma's Word](https://grandmasword.com/)

## coding forums

[TechBliss](https://www.techbliss.org/)
Coding Forum

## coding is hard

[Why Learning to Code is Hard - And How to Make it Easier](https://www.freecodecamp.org/news/why-learning-to-code-is-hard-and-how-to-make-it-easier)

[To the brain, reading computer code is not the same as reading language (2020) | Hacker News](https://news.ycombinator.com/item?id=40480913)
[To the brain, reading computer code is not the same as reading language | MIT News | Massachusetts Institute of Technology](https://news.mit.edu/2020/brain-reading-computer-code-1215)

## common mistakes

[What was your biggest mistake as a beginner programmer?](https://old.reddit.com/r/learnprogramming/comments/168qc5e/what_was_your_biggest_mistake_as_a_beginner/)

[Stuck coding real-world projects : learnprogramming](https://old.reddit.com/r/learnprogramming/comments/1135oo1/stuck_coding_realworld_projects)

[What I Learned from Reading "The Pragmatic Programmer"](https://www.freecodecamp.org/news/thought-on-the-pragmatic-programmer)

## concurrency and parallelism

[GitHub - brunohenrique/concurrency-and-parallelism: My references about Concurrency & Parallelism](https://github.com/brunohenrique/concurrency-and-parallelism)

[GitHub - deadlockempire/deadlockempire.github.io: The Deadlock Empire: Slay dragons, learn concurrency!](https://github.com/deadlockempire/deadlockempire.github.io)
[The Deadlock Empire](https://deadlockempire.github.io/)

[50 years later, is two-phase locking the best we can do? | Hacker News](https://news.ycombinator.com/item?id=37706893)
[Concurrency Freaks: 50 years later, is Two-Phase Locking the best we can do?](https://concurrencyfreaks.blogspot.com/2023/09/50-years-later-is-two-phase-locking.html)

## data science

[Jonathan Callahan](https://dzone.com/articles/best-best-practices-ever)
(2013) Best Best Practices Ever (for scientific computing)

## developer blogs

[abdelhai/devblogs: +2600 developer-related blogs and publications.](https://github.com/abdelhai/devblogs)

[GitHub - bnb/awesome-developer-streams: Awesome Developers, Streaming](https://github.com/bnb/awesome-developer-streams)

## functions

[Functorio | Hacker News](https://news.ycombinator.com/item?id=26157969)
[Functorio |   Bartosz Milewski's Programming Cafe](https://bartoszmilewski.com/2021/02/16/functorio/)

## generic programming

[Generic programming - Wikipedia](https://en.wikipedia.org/wiki/Generic_programming)
- this is an intermediate between pseudocode and actual code

## history

[Classic Usenet posts on computer architecture, operating systems and languages | Hacker News](https://news.ycombinator.com/item?id=40404440)
[Computers](https://yarchive.net/comp/index.html)

## ifs and fors

[Push Ifs Up and Fors Down | Hacker News](https://news.ycombinator.com/item?id=44013157)

## industry defects

[Programming breakthroughs we need | Hacker News](https://news.ycombinator.com/item?id=32495133)
[Programming breakthroughs we need](https://yoyo-code.com/programming-breakthroughs-we-need/)

[IT Runs on Java 8 | Hacker News](https://news.ycombinator.com/item?id=19877916)
[IT runs on Java 8 | ★❤✰ Vicki Boykis ★❤✰](https://vickiboykis.com/2019/05/10/it-runs-on-java-8/)

## keep it small

[John Cutler](https://hackernoon.com/work-small-even-if-it-makes-no-sense-6bd1f401fc3a)
(2017) Work Smaller (Even If It Makes No Sense)

## naming conventions

[IMStudio](https://medium.com/geekculture/naming-rules-one-of-the-hard-things-in-computer-science-643dba6a0e36)
(2021) Naming Rules: one of the hard things in Computer Science

[Jérôme Beau](https://javarome.medium.com/programming-naming-361a41c86928)
(2021) Programming: Naming
Where are you talking from?

[Lane Wagner](https://medium.com/qvault/naming-variables-the-right-way-12e2d7769be2)
(2021) Naming Variables the Right Way
bugs are due to the poor naming of variables way more often than you would expect.

[Jason Swett](https://www.codewithjason.com/variable-name-anti-patterns/)
(2018) Variable name anti-patterns

[Christopher Laine](https://medium.com/it-dead-inside/ubiquitous-language-in-your-software-domain-1ff6df49ac8c)
(2019) Ubiquitous Language in your software domain
Defining your software domain’s language makes everything easier

## pair programming

[Fagner Martins Brack (fagnerbrack)](https://medium.com/@fagnerbrack/pair-programming-8cfbf2dc4d00)
(2016) Pair Programming
A technique that, IF DONE CORRECTLY, has the potential for delivering software faster with lower cost

[Dave Nicolette](https://www.leadingagile.com/2018/01/in-favor-of-pairing/)
(2018) In Favor of Pairing

[Iwein Fuld](http://blog.xebia.com/practical-styles-of-pair-programming/)
(2010) Practical Styles of Pair Programming

[Philippe Bourgau](http://philippe.bourgau.net/from-zero-to-pair-programming-hero/)
(2015) From Zero to Pair Programming Hero

[Arlo Belshee](http://arlobelshee.com/is-pair-programming-for-me/)
(2012) Is Pair Programming for Me?

[Wesley Moore](http://www.wezm.net/technical/2017/10/pair-programming/)
(2017) Pair Programming

[Raúl Ávila](https://dev.to/raulavila/my-experience-with-pair-programming)
My Experience with Pair Programming

[Bitbucket](https://bitbucket.org/spooning/)
Spooning makes pair programming look like child's play. Achieve the speed of pair programming with an added level of quiet, knowing intimacy.

## podcasts and papers

[GitHub - karlhorky/awesome-speakers: Awesome speakers in the programming and design communities](https://github.com/karlhorky/awesome-speakers)

[GitHub - facundoolano/software-papers: A curated list of papers for Software Engineers](https://github.com/facundoolano/software-papers)

## pragmatic programmer

[AdesisNetlife/coder-bible](https://github.com/AdesisNetlife/coder-bible)
Thoughts and resources to be a pragmatic programmer

[braydie/PragProgTips](https://github.com/braydie/PragProgTips/blob/master/index.html)
some tips from pragmatic programmer book

[Hugo Matilla](https://github.com/HugoMatilla/The-Pragmatic-Programmer)
Summary of the book The Pragmatic Programmer by Andrew Hunt and David Thomas
:star:

[Raymond Rutjes](https://blog.algolia.com/pragmatic-releasing/)
(2017) Pragmatic Releasing: Less Worry, More Shipping

[Andrew Hunt and David Thomas](https://pragprog.com/the-pragmatic-programmer/extracts/coincidence)
(1999) Programming by Coincidence
Don’t Program by Coincidence. Extract from The Pragmatic Programmer book

## pragmaticprogrammer

Care About Your Craft: Why spend your life developing software unless you care about doing it well?
Think! About Your Work: Turn off the autopilot and take control. Constantly critique and appraise your work.
Provide Options, Don't Make Lame Excuses: Instead of excuses, provide options. Don't say it can't be done; explain what can be done.
Don't Live with Broken Windows: Fix bad designs, wrong decisions, and poor code when you see them.
Be a Catalyst for Change: You can't force change on people. Instead, show them how the future might be and help them participate in creating it.
Remember the Big Picture: Don't get so engrossed in the details that you forget to check what's happening around you.
Make Quality a Requirements Issue: Involve your users in determining the project's real quality requirements.
Invest Regularly in Your Knowledge Portfolio: Make learning a habit.
Critically Analyze What You Read and Hear: Don't be swayed by vendors, media hype, or dogma. Analyze information in terms of you and your project.
It's Both What You Say and the Way You Say It: There's no point in having great ideas if you don't communicate them effectively.
DRY – Don't Repeat Yourself: Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.
Make It Easy to Reuse: If it's easy to reuse, people will. Create an environment that supports reuse.
Eliminate Effects Between Unrelated Things: Design components that are self-contained. independent, and have a single, well-defined purpose.
There Are No Final Decisions: No decision is cast in stone. Instead, consider each as being written in the sand at the beach, and plan for change.
Use Tracer Bullets to Find the Target: Tracer bullets let you home in on your target by trying things and seeing how close they land.
Prototype to Learn: Prototyping is a learning experience. Its value lies not in the code you produce, but in the lessons you learn.
Program Close to the Problem Domain: Design and code in your user's language.
Estimate to Avoid Surprises: Estimate before you start. You'll spot potential problems up front.
Iterate the Schedule with the Code: Use experience you gain as you implement to refine the project time scales.
Keep Knowledge in Plain Text: Plain text won't become obsolete. It helps leverage your work and simplifies debugging and testing.
Use the Power of Command Shells: Use the shell when graphical user interfaces don't cut it.
Use a Single Editor Well: The editor should be an extension of your hand; make sure your editor is configurable, extensible, and programmable.
Always Use Source Code Control: Source code control is a time machine for your work – you can go back.
Fix the Problem, Not the Blame: It doesn't really matter whether the bug is your fault or someone else's – it is still your problem, and it still needs to be fixed.
Don't Panic When Debugging: Take a deep breath and THINK! about what could be causing the bug.
"select" Isn't Broken: It is rare to find a bug in the OS or the compiler, or even a third-party product or library. The bug is most likely in the application.
Don't Assume It – Prove It: Prove your assumptions in the actual environment – with real data and boundary conditions.
Learn a Text Manipulation Language: You spend a large part of each day working with text. Why not have the computer do some of it for you?
Write Code That Writes Code: Code generators increase your productivity and help avoid duplication.
You Can't Write Perfect Software: Software can't be perfect. Protect your code and users from the inevitable errors.
Design with Contracts: Use contracts to document and verify that code does no more and no less than it claims to do.
Crash Early: A dead program normally does a lot less damage than a crippled one.
Use Assertions to Prevent the Impossible: Assertions validate your assumptions. Use them to protect your code from an uncertain world.
Use Exceptions for Exceptional Problems: Exceptions can suffer from all the readability and maintainability problems of classic spaghetti code. Reserve exceptions for exceptional things.
Finish What You Start: Where possible, the routine or object that allocates a resource should be responsible for deallocating it.
Minimize Coupling Between Modules: Avoid coupling by writing "shy" code and applying the Law of Demeter.
Configure, Don't Integrate: Implement technology choices for an application as configuration options, not through integration or engineering.
Put Abstractions in Code, Details in Metadata: Program for the general case, and put the specifics outside the compiled code base.
Analyze Workflow to Improve Concurrency: Exploit concurrency in your user's workflow.
Design Using Services: Design in terms of services – independent, concurrent objects behind well-defined, consistent interfaces.
Always Design for Concurrency: Allow for concurrency, and you'll design cleaner interfaces with fewer assumptions.
Separate Views from Models: Gain flexibility at low cost by designing your application in terms of models and views.
Use Blackboards to Coordinate Workflow: Use blackboards to coordinate disparate facts and agents, while maintaining independence and isolation among participants.
Don't Program by Coincidence: Rely only on reliable things. Beware of accidental complexity, and don't confuse a happy coincidence with a purposeful plan.
Estimate the Order of Your Algorithms: Get a feel for how long things are likely to take before you write code.
Test Your Estimates: Mathematical analysis of algorithms doesn't tell you everything. Try timing your code in its target environment.
Refactor Early, Refactor Often: Just as you might weed and rearrange a garden, rewrite, rework, and re-architect code when it needs it. Fix the root of the problem.
Design to Test: Start thinking about testing before you write a line of code.
Test Your Software, or Your Users Will: Test ruthlessly. Don't make your users find bugs for you.
Don't Use Wizard Code You Don't Understand: Wizards can generate reams of code. Make sure you understand all of it before you incorporate it into your project.
Don't Gather Requirements – Dig for Them: Requirements rarely lie on the surface. They're buried deep beneath layers of assumptions, misconceptions, and politics.
Workwith a User to Think Like a User: It's the best way to gain insight into how the system will really be used.
Abstractions Live Longer than Details: Invest in the abstraction, not the implementation. Abstractions can survive the barrage of changes from different implementations and new technologies.
Use a Project Glossary: Create and maintain a single source of all the specific terms and vocabulary for a project.
Don't Think Outside the Box – Find the Box: When faced with an impossible problem, identify the real constraints. Ask yourself: "Does it have to be done this way? Does it have to be done at all?"
Start When You're Ready.: You've been building experience all your life. Don't ignore niggling doubts.
Some Things Are Better Done than Described: Don't fall into the specification spiral – at some point you need to start coding.
Don't Be a Slave to Formal Methods.: Don't blindly adopt any technique without putting it into the context of your development practices and capabilities.
Costly Tools Don't Produce Better Designs: Beware of vendor hype, industry dogma, and the aura of the price tag. Judge tools on their merits.
Organize Teams Around Functionality: Don't separate designers from coders, testers from data modelers. Build teams the way you build code.
Don't Use Manual Procedures: A shell script or batch file will execute the same instructions, in the same order, time after time.
Test Early. Test Often. Test Automatically: Tests that run with every build are much more effective than test plans that sit on a shelf.
Coding Ain't Done 'Til All the Tests Run: 'Nuff said.
Use Saboteurs to Test Your Testing: Introduce bugs on purpose in a separate copy of the source to verify that testing will catch them.
Test State Coverage, Not Code Coverage: Identify and test significant program states. Just testing lines of code isn't enough.
Find Bugs Once: Once a human tester finds a bug, it should be the last time a human tester finds that bug. Automatic tests should check for it from then on.
English is Just a Programming Language: Write documents as you would write code: honor the DRY principle, use metadata, MVC, automatic generation, and so on.
Build Documentation In, Don't Bolt It On: Documentation created separately from code is less likely to be correct and up to date.
Gently Exceed Your Users' Expectations: Come to understand your users' expectations, then deliver just that little bit more.
Sign Your Work: Craftsmen of an earlier age were proud to sign their work. You should be, too.

## programming vs software engineering

[Ask HN: Do you hate software engineering but love programming? | Hacker News](https://news.ycombinator.com/item?id=34366610)

[Anyone likes coding but don't want to be a dev?: learnprogramming](https://www.reddit.com/r/learnprogramming/comments/10xfvs8/anyone_likes_coding_but_dont_want_to_be_a_dev)

[234: Escape Artist - explain xkcd](https://www.explainxkcd.com/wiki/index.php/234:_Escape_Artist)

## project ideas

[Project ideas](https://dev.to/yuridevat/how-i-come-up-with-project-ideas-and-never-faced-tutorial-hell-3287)

[YC: Requests for Startups | Hacker News](https://news.ycombinator.com/item?id=39371805)
[Some more project ideas (that could turn into business ideas) on Y Combinator](https://www.ycombinator.com/rfs/)

[IdeasGrab](https://www.ideasgrab.com/)

[Codastro](https://codeastro.com/)
Source Code Projects

[ItSourceCode](https://www.itsourcecode.com/)
Source Code Projects

[NanoDano](http://www.devdungeon.com/content/i-know-how-program-i-dont-know-what-program)
"I know how to program, but I don't know what to program"

## researching

[Should I look at outsource when answering freecodecamp questions? : FreeCodeCamp](https://old.reddit.com/r/FreeCodeCamp/comments/16rk6ss/should_i_look_at_outsource_when_answering/)

## RSCG

[GitHub - ignatandrei/RSCG_Examples: Roslyn Source Code Generators with Examples](https://github.com/ignatandrei/RSCG_Examples)
[Time based List of RSCG | RSCG Examples](https://ignatandrei.github.io/RSCG_Examples/v2/docs/List-of-RSCG)

## software dev news

[Lobsters](https://lobste.rs/)
[lobsters-reader](https://github.com/cfdrake/lobsters-reader)
Lobsters is a technology-focused community centered around link aggregation and discussion
:unicorn:
[sister sites](https://github.com/lobsters/lobsters/wiki)

[InfoQ](https://www.infoq.com/)
news, videos, books for software developers

[DEVURLS](https://devurls.com/)
a developer news aggregator.
:fire:

[ThoughtWorks](https://www.thoughtworks.com/radar/tools)
Technology radar : trends, insights into tools, frameworks, languages, techniques & platforms shaping the future
:star:
[ThoughtWorks](https://www.thoughtworks.com/radar)
Technology radar : trends, insights into tools, frameworks, languages, techniques & platforms shaping the future
:star:
[ThoughtWorks Insights](https://www.thoughtworks.com/insights)
ThoughtWorks Insights
[ThoughtWorks Insights](https://www.thoughtworks.com/insights/continuous-delivery)
ThoughtWorks Insights on continuous delivery
[ThoughtWorks](https://www.thoughtworks.com/radar/how-to-byor)
How to build your ThoughtWorks Radar
[Thoughtworks Technology Radar](https://www.thoughtworks.com/radar)

[TechCrunch](https://techcrunch.com/)
latest technology news and information on startups

[the morning paper](https://blog.acolyer.org/)
an interesting/influential/important paper from the world of CS every weekday morning, as selected by Adrian Colyer

[TECHURLS](https://techurls.com/)
a technology news aggregator.
Tech News

[HackNews](https://hackne.ws/)
Tech News

[DiggTech](https://www.digg.com/technology)
Tech News

[ReclaimNet](https://reclaimthenet.org/)
Tech News

[TechNadu](https://www.technadu.com/)
Tech News

[GeekWire](https://www.geekwire.com/)
Tech News

[Protocol](https://www.protocol.com/)
Tech News

[DailyDot](https://www.dailydot.com/)
Tech News

[TheNextWeb](https://thenextweb.com/)
Tech News

[Techmeme](https://techmeme.com/)
Tech News

[Techworm](https://www.techworm.net/)
Tech News

[TechRadar](https://www.techradar.com/)
Tech News

[TechHive](https://www.techhive.com/news/)
Tech News

[AfterDawn](https://www.afterdawn.com/)
Tech News

[TheRegister](https://www.theregister.com/)
Tech News

[ZDNet](https://www.zdnet.com/)
Tech News

[Neowin](https://www.neowin.net/)
Tech News

[TheVerge](https://www.theverge.com/)
Tech News

[TheRecord](https://therecord.media/)
Tech News

[MITReview](https://www.technologyreview.com/)
Tech News

[VentureBeat](https://venturebeat.com/)
Tech News

[TechGuy](https://techguylabs.com/)
Tech News

[GHacks](https://www.ghacks.net/)
Tech News

[Tidbits](https://tidbits.live/)
Tech News

[Ars Technica](https://arstechnica.com/)
Tech News

[Geeks3D](https://www.geeks3d.com/)
Tech News

[SingularityHub](https://singularityhub.com/)
Tech News

[Slashdot](https://slashdot.org/)
Tech News

[n-gate](http://n-gate.com/)
"hacker" "news" roundup

[Newsletters](https://github.com/zudochkin/awesome-newsletters)
Tech Newsletters

[DevSpotlight](https://github.com/DominatorVbN/DevSpotlight)
Latest tech news

[Industrial Logic Blog](https://www.industriallogic.com/blog/)
leveraging safety wisdom in workspace from manufacturing, psychology, culture change and Agile and Lean developmen

[DZone](https://dzone.com/)
programming & devops news

[Code as Craft](https://codeascraft.com/)
Etsy' blog for craftsmen

[TIOBE Index](https://www.tiobe.com/tiobe-index/)

[Methods & Tools Editor Blog](http://blog.martinig.ch/)
Software Development Ideas + [links](http://blog.martinig.ch/category/links/)

[Radar – O’Reilly](https://www.oreilly.com/radar/)
What's on the radar

[TLDR](https://www.tldrnewsletter.com/)

## software dev news - tech reviews

[WccfTech](https://wccftech.com/)
Tech Reviews

[Guru3D](https://www.guru3d.com/)
Tech Reviews

[AnandTech](https://www.anandtech.com/)
Tech Reviews

[TomHardware](https://www.tomshardware.com/)
Tech Reviews

[TweakTown](https://www.tweaktown.com/)
Tech Reviews

[VideoCardz](https://videocardz.com/)
Tech Reviews

## software engineering

[Kevin London](https://www.kevinlondon.com/2015/09/10/10-software-talks-to-listen-to.html)
(2015) 10 Software Talks to Listen to on Your Way to Work

[Ben Putano](https://stackify.com/software-development-trends-2018/)
(2017) 5 Software Development Trends for 2018: Developers Needed

[Richard Clayton](https://rclayton.silvrback.com/software-engineering-is-not-a-job-it-s-a-profession)
(2014) Software Engineering is not a Job. It's a Profession.

[bloggy - bloggy](https://web.archive.org/web/20221026153905/https://kristian-blogg.netlify.app/content/blog/philosophy/software-engineering-is-more-than-code)

## weird issues

[The cursed computer iceberg meme (2021) | Hacker News](https://news.ycombinator.com/item?id=32612931)
[The Cursed Computer Iceberg Meme](https://suricrasia.online/iceberg/)
AMAZING RESOURCE

## you don't need a good computer

[programming while poor: learnprogramming](https://www.reddit.com/r/learnprogramming/comments/11s3a3o/programming_while_poor)

## coding

[Code by Charles Petzold](https://www.codehiddenlanguage.com)

[The Nature of Code (2nd Edition) | Hacker News](https://news.ycombinator.com/item?id=40221067)
[Introduction / Nature of Code](https://natureofcode.com/introduction/)

[The freeCodeCamp Mobile App - Learn to Code Right On Your Phone](https://www.freecodecamp.org/news/freecodecamp-mobile-app-curriculum-update)

[Fireship - Learn to Code Faster | Hacker News](https://news.ycombinator.com/item?id=33925197)
[Fireship - Learn to Code Faster](https://fireship.io/)

[faq - learnprogramming](https://old.reddit.com/r/learnprogramming/wiki/faq#wiki_getting_started)
[/r/learnprogramming Wiki](https://www.reddit.com/r/learnprogramming/wiki/index#wiki_other_resources)

["Code" 2nd Edition Now Available | Hacker News](https://news.ycombinator.com/item?id=32377735)
[Charles Petzold: "Code" 2nd Edition Now Available!](https://www.charlespetzold.com/blog/2022/08/Code-2nd-Edition-Now-Available.html)
["Code" 2nd Edition | Hacker News](https://news.ycombinator.com/item?id=31696901)
[Charles Petzold: Announcing "Code" 2nd Edition](https://www.charlespetzold.com/blog/2022/06/Announcing-Code-2nd-Edition.html)

[epoyraz/Awesome-Youtube-Channels: Curated list of Awesome Youtube Channels about Programming](https://github.com/epoyraz/Awesome-Youtube-Channels)

[Learn to Code - for Free | Codecademy](https://www.codecademy.com/)
[Full Catalog](https://www.codecademy.com/catalog/all)

[GitHub - interneto/awesome-coding: Collection or awesome-list of coding links](https://github.com/interneto/awesome-coding)

[GitHub - Faranheit15/Coding-Resources: Free coding resources, feel free to contribute if you have something useful.](https://github.com/Faranheit15/Coding-Resources)

[GitHub - Ngoakor12/coding-resource-finder: An easier way to find coding related topics and projects on the ACN syllabus.](https://github.com/Ngoakor12/coding-resource-finder)

[Sololearn: Learn to Code](https://www.sololearn.com)
[Sololearn: Learn to Code](https://www.sololearn.com/en/)

[GitHub - Devang-25/Best-Resources-for-a-Programmer: Compilation of the Best Resources for a Programmer](https://github.com/Devang-25/Best-Resources-for-a-Programmer)

[GitHub - softwareByAndi/useful-programming-resources: useful resources for students learning to program](https://github.com/softwareByAndi/useful-programming-resources)

[Coding Bootcamp | Learn 1-on-1 with a Mentor | Thinkful™](https://www.thinkful.com/)

[Pocket Code](https://github.com/catrobat/catty)
[Home - Catrobat](https://catrobat.org/)
Create games, animations, interactive music videos, and many kind of other apps, directly on device

[GeeksforGeeks](https://www.geeksforgeeks.org/)
Portal to Computer Science topics.
Programming/Coding Tutorials

[A-to-Z-Resources-for-Students](https://github.com/dipakkr/A-to-Z-Resources-for-Students)
Coding Learning Resources
[Xplainerr | Upskilling & Interview Prep for AI, PM, Engineering, and Design](https://www.xplainerr.com/)

[mike-north/awesome-learn-to-code: A list of awesome resources for learning to code](https://github.com/mike-north/awesome-learn-to-code)
Programming/Coding Learning Resources

[Nayuki](https://www.nayuki.io/)
Programming Tutorials

[Karel The Robot](https://github.com/fredoverflow/karel)
Basic Programming Teaching Environment

[Learn today, build a brighter tomorrow. | Code.org](https://code.org/)

[Programming Projects for Advanced Beginners | Robert Heaton](https://robertheaton.com/2018/12/08/programming-projects-for-advanced-beginners/)

[GitHub - fnplus/community-project-ideas: Catalog of all the ideas/tutorials for project based learning!](https://github.com/fnplus/community-project-ideas)

[GitHub - florinpop17/app-ideas: A Collection of application ideas which can be used to improve your coding skills.](https://github.com/florinpop17/app-ideas)
[iCodeThis](https://icodethis.com/)

[ProjectLearn - Learn to Code by Creating Projects](https://projectlearn.io/)

[GitHub - sixclones/creative-journey: List of ressources that helped me in my creative journey.](https://github.com/sixclones/creative-journey)

[tutsplus](https://code.tutsplus.com/tutorials)

[64json/DuoCoder: Duolingo for Coders](https://github.com/64json/DuoCoder)

## coding games

[CodinGame](https://www.codingame.com/)
[Coding Games and Programming Challenges to Code Better](https://www.codingame.com/start)
Learn how to code video games
Games to Practice Coding/Programming

[CheckiO - coding games and programming challenges for beginner and advanced](https://checkio.org/)
[py.CheckiO - Python coding challenges and exercises with solutions for beginners and advanced](https://py.checkio.org/)
Games for coding.

[CodeCombat - Coding games to learn Python and JavaScript | CodeCombat](https://codecombat.com)
Programming Game designed for Students.
[CodeCombat Coding games to learn Python and JavaScript](https://codecombat.com/home)
[CodeCombat](https://github.com/codecombat/codecombat-ios)
Multiplayer programming game for learning how to code

[Codewars - Achieve mastery through coding practice and developer mentorship](https://www.codewars.com/)
[I use codewars to practice python as a beginner to learning programming, I find their beginners problems also too difficult..](https://old.reddit.com/r/learnprogramming/comments/169s97g/i_use_codewars_to_practice_python_as_a_beginner/)
[Codewars](http://www.codewars.com/dashboard)
Free Code Challenges,Getting Hired
Skills: Front End,Back End,Computer Science
Sub-Skills: JavaScript,Ruby,PHP,Python,Java,SQL,CLI,Swift,BF,C,Clojure,CoffeeScript,C++,C#,Crystal,Dart,Elixir,Erlang,Fortran,F#,Go,Groovy,Haskell,Julia,Kotlin,Lua,NASM,Nim,Objective-C,OCaml,PowerShell,R,Rust,Scala,Shell,Solidity,TypeScript,D,Lisp,Chapel,Racket,Perl
Make it a point to make this a daily routine. There are plenty of languages supported by the multitude of challenges available, but focus on the ones that are familiar and the ones that will be most marketable to employers. Document thought process and once solved, blog about it on technical blog. Codewars is also used at Flatiron for study group pair programming sessions. Typically used in conjunction with JSFiddle (https://jsfiddle.net/) to allow for live collaboration with other programmers.

[10 Best Coding Games to Advance Your Programming Skills - GeeksforGeeks](https://www.geeksforgeeks.org/10-best-coding-games-to-advance-your-programming-skills)

[Elevator Saga - the elevator programming game](https://play.elevatorsaga.com)

[Practice your coding skills on short coding contests - Clash of Code](https://www.codingame.com/multiplayer/clashofcode)

[Break The Code 2.0: A Browser Game Where You Solve Missions Using Coding Skills](https://www.freecodecamp.org/news/break-the-code-2-game)

[Learn more - International Colobot Community](https://colobot.info/learn-more)

[GitHub - lmammino/awesome-learn-by-playing: A collection of tech resources that allow you to learn new things by playing games](https://github.com/lmammino/awesome-learn-by-playing)

[RoboMind](https://www.robomind.net/)
Code Learning Game

[yrgo/awesome-educational-games: A curated list of awesome educational games to learn editors, languages, programming, etc](https://github.com/yrgo/awesome-educational-games)

[Developer Training | Test Coding Skills Online Codility](https://app.codility.com/programmers/)
[Codility](https://codility.com/programmers/challenges/)

## computer programs

[Design of Computer Programs | Free Courses | Udacity](https://www.udacity.com/course/design-of-computer-programs--cs212)

## creative coding

[terkelg/awesome-creative-coding: Creative Coding: Generative Art, Data visualization, Interaction Design, Resources.](https://github.com/terkelg/awesome-creative-coding)
Creative Coding Resource Index

[GitHub - terkelg/awesome-creative-coding: Creative Coding: Generative Art, Data visualization, Interaction Design, Resources.](https://github.com/terkelg/awesome-creative-coding)

[GitHub - linooohon/creative-coding-jobs-update: "Creative Coding Jobs Daily Update" : Glassdoor, SimplyHired](https://github.com/linooohon/creative-coding-jobs-update)

## cs basics

[Teach Yourself Computer Science - Key CS Concepts You Should Know](https://www.freecodecamp.org/news/what-every-software-engineer-should-know/)

[Computer Science (Bachelor's) | University of the People](https://www.uopeople.edu/programs/online-bachelors/computer-science/)

[CMU CS Academy: a free online computer science curriculum by Carnegie Mellon | Hacker News](https://news.ycombinator.com/item?id=34814178)
[CMU CS Academy](https://academy.cs.cmu.edu/)

[What is a Computer Scientist? What Exactly Do CS Majors Do?](https://www.freecodecamp.org/news/what-is-a-computer-scientist-what-exactly-do-cs-majors-do)

[CS Primer: Learn computer science by writing code](https://csprimer.com)

[GitHub - rbaker26/Programming-Merit-Badge: PowerPoint and Code Resources for BSA Programming Merit Badge](https://github.com/rbaker26/Programming-Merit-Badge)

## cs general

[GitHub - the-akira/Computer-Science-Resources: A list of resources in different fields of Computer Science](https://github.com/the-akira/Computer-Science-Resources)

[GitHub - P1xt/p1xt-guides: Programming curricula](https://github.com/P1xt/p1xt-guides)

[Path to a free, self-taught education in Computer Science | Hacker News](https://news.ycombinator.com/item?id=34673581)
[ossu/computer-science: Path to a free self-taught education in Computer Science!](https://github.com/ossu/computer-science)
path to a free self-taught education in Computer Science.
CS course from OSS University

[CompSci](https://functionalcs.github.io/curriculum/)
Learning

[GitHub - Beelzenef/codeReads: goodReads (pun intended) for coding and programming](https://github.com/Beelzenef/codeReads)

[GitHub - Dylan-Israel/ultimate-coding-resources: A collection of the best resources for programming, web development, computer science and more.](https://github.com/Dylan-Israel/ultimate-coding-resources)

[GitHub - elfalehed/uniqueresources.dev: The only website you'll need to find resources to learn coding and programming](https://github.com/elfalehed/uniqueresources.dev)

[GitHub - modersetech/awwwesome: Awesome list of web development resources As you learn, keep this list handy.](https://github.com/modersetech/awwwesome)

[GitHub - ryparker/Awesome-List: A list of my favorite findings in the software industry.](https://github.com/ryparker/Awesome-List)

[GitHub - seeniforu/Useful_Repository: I got so many Free Online Resources Mostly Everything You need to Know which is collected in a Structured manner.](https://github.com/seeniforu/Useful_Repository)

[GitHub - jotavare/42-resources: My curated 42 school resource collection. The good, the bad and the ugly.](https://github.com/jotavare/42-resources)

[GitHub - pawelborkar/awesome-repos: A curated list of GitHub Repositories full of FREE Resources.](https://github.com/pawelborkar/awesome-repos)

[GitHub - eagleusb/awesome-repositories: Personal representation of my 4k github repositories stars.](https://github.com/eagleusb/awesome-repositories)

[GitHub - 0xRitesh/awesome-repositories: Useful GitHub Repos That Every Developer Should Follow](https://github.com/0xRitesh/awesome-repositories)

[GitHub - RahulBirCodes/awesome-steam: An awesome list of resources for specific science, technology, engineering, art, and math (STEAM) classes that students and teachers can use to supplement their learning](https://github.com/RahulBirCodes/awesome-steam)

[GitHub - nobodyme/Listception: Collection of lists of all the lists related to programming I managed to find so far.](https://github.com/nobodyme/Listception)

[GitHub - pyxelr/recommendations-for-engineers: All of my recommendations for aspiring engineers in a single place, coming from various areas of interest.](https://github.com/pyxelr/recommendations-for-engineers)

[GitHub - prakhar1989/awesome-courses: List of awesome university courses for learning Computer Science!](https://github.com/prakhar1989/awesome-courses)

[GitHub - world-class/REPL: The Learning Hub for UoL's Online CS Students](https://github.com/world-class/REPL)

[GitHub - tenhobi/the-devs-guide: A collection of useful tools, guides, hacks, know-hows and more.](https://github.com/tenhobi/the-devs-guide)

[anu0012/awesome-computer-science-opportunities: An awesome list of events and fellowship opportunities for Computer Science students](https://github.com/anu0012/awesome-computer-science-opportunities)

[GitHub - quabanc/awesome-computer-science: Some of the awesome resources in Computer Science.](https://github.com/quabanc/awesome-computer-science)

[860+ Free Online Programming & Computer Science Courses You Can Start This New Year](https://www.freecodecamp.org/news/free-online-programming-cs-courses)

[GitHub - Sunwarul/become-software-engineer: This repository is a collection of resources, and step by step guidelines that can be helpful for any one who self studying to become a good Software Engineer.](https://github.com/Sunwarul/become-software-engineer)

[GitHub - CodheadClub/AwesomeResources: An awesome list of computer science related resources.](https://github.com/CodheadClub/AwesomeResources)

[GitHub - Surajv311/one4All: This repository consists of tech resources and opportunities which could be useful for students interested in computer science. It also hosts non-tech sources which could be useful for anyone.](https://github.com/Surajv311/one4All)

[GitHub - GoldinGuy/CollegeCompendium: A curated collection of free public Computer Science classes from colleges across America](https://github.com/GoldinGuy/CollegeCompendium)

[GitHub - PanXProject/awesome-certificates: List of IT, computer science and business courses with free certificates & badges.](https://github.com/PanXProject/awesome-certificates)

[GitHub - iamjatinchauhan/resources-for-developers: Crazy website links for you!](https://github.com/iamjatinchauhan/resources-for-developers)

[GitHub - PTDZ/SORTED: SORTED: a curated list of interesting science ideas and links (cognitive/neuro & data science)](https://github.com/PTDZ/SORTED)

[GitHub - sudhakar3697/awesome-web-tech: To learn & implement things](https://github.com/sudhakar3697/awesome-web-tech)

[GitHub - bobeff/programming-math-science: This is a list of links to different freely available learning resources about computer programming, math, and science.](https://github.com/bobeff/programming-math-science)

[GitHub - Besnn/computer-science-and-computer-engineering-books-and-resources: Free Access Books/Resources for Computer Engineering (and Computer Science) Students](https://github.com/Besnn/computer-science-and-computer-engineering-books-and-resources)

[GitHub - MusaAkyuz/Computer-Science-Resources: Books, Handnotes, Cheatsheets, Pictures, Presentations...](https://github.com/MusaAkyuz/Computer-Science-Resources)

[GitHub - mostafatouny/awesome-theoretical-computer-science: The interdicplinary of Mathematics and Computer Science, Distinguisehed by its emphasis on mathemtical technique and rigour.](https://github.com/mostafatouny/awesome-theoretical-computer-science)

[ArunkumarRamanan/Computer-Science-Resources: The Curated List of Computer Science CS Resources](https://github.com/ArunkumarRamanan/Computer-Science-Resources)

[Arbazkhan4712/GSC-Open-Source-Computer-Science-Degree: GSC Open Source Computer Science Degree](https://github.com/Arbazkhan4712/GSC-Open-Source-Computer-Science-Degree)

[GitHub - gourab98/All-Resources: All Resources For Computer Science](https://github.com/gourab98/All-Resources)

[GitHub - trimstray/the-book-of-secret-knowledge: A collection of inspiring lists, manuals, cheatsheets, blogs, hacks, one-liners, cli/web tools and more.](https://github.com/trimstray/the-book-of-secret-knowledge)

[alexandraglam/Resources-For-New-Developers: A curated list for new developers and web designers.](https://github.com/alexandraglam/Resources-For-New-Developers)

[GitHub - Fetz/reads: A list of books, articles, videos, courses and subscriptions that I like or I wish to use](https://github.com/Fetz/reads)

[GitHub - vinibrsl/digest: Blogs and reads for devs to start their mornings.](https://github.com/vinibrsl/digest)

[GitHub - codeclannigeria/learning-resources: All the FREE learning resources in one place. These resources are strictly recommended.](https://github.com/codeclannigeria/learning-resources)

[GitHub - GDGAhmedabad/Awesome-Learning-Resources: "Technology Gold mine" to collect and share materials/resources](https://github.com/GDGAhmedabad/Awesome-Learning-Resources)

[GitHub - Gia-Tech/megalist-of-learning-resources: This is a list consisting of the most comprehensive lists of resources about endless topics of computer science, software development, programming, etc., created, shared and maintained by very good people on github.](https://github.com/Gia-Tech/megalist-of-learning-resources)

[GitHub - jobream/List-of-Learning-Resources: This collection provides a list of educational resources for Software Engineers. Feel free to add your favorite resources as well and help others in their journey of learning.](https://github.com/jobream/List-of-Learning-Resources)

[GitHub - lauragift21/awesome-learning-resources: Awesome list of resources on Web Development.](https://github.com/lauragift21/awesome-learning-resources)

[GitHub - nwplus/self-learning-resources: A wiki containing helpful resources for those looking to learn more about the world of CS on their own](https://github.com/nwplus/self-learning-resources)

[GitHub - rshwndsz/learning-resources: What I use to learn everything from figure drawing to computer vision](https://github.com/rshwndsz/learning-resources)

[it-ebooks](http://it-ebooks.info)
Large selection of free and open-source IT ebooks

[GitHub - amitness/learning: A log of things I'm learning](https://github.com/amitness/learning)

[asadravian/top-free-courses: Top best FREE courses directory with index, titles and working links.](https://github.com/asadravian/top-free-courses)

[Online Tutorials, Courses, and eBooks Library | Tutorialspoint](https://www.tutorialspoint.com/index.htm)

[Tuts 4 You](https://forum.tuts4you.com/)
Coding/Developer Tutorials

[ahdinosaur/intertwingled: A collection of videos to showcase the magic alchemy of computation.](https://github.com/ahdinosaur/intertwingled)

[GitHub - ghaiklor/awesome-internals: A curated list of awesome resources and learning materials in the field of X internals](https://github.com/ghaiklor/awesome-internals)

[GitHub - hcgatewood/travel-guide: An MIT undergrad's compilation of useful CS resources](https://github.com/hcgatewood/travel-guide)

[GitHub - logancyang/my-cs-degree: A CS degree with a focus on full-stack ML engineering, 2020](https://github.com/logancyang/my-cs-degree)

[GitHub - mayfrost/guides: Looking for a guide? You came to the right place. Here you can find documentation for a variety of topics I research to make complex computing easier. For comments go to the IRC channel #nfo at the Rizon network.](https://github.com/mayfrost/guides)

[GitHub - illinois-cs241/coursebook: Open Source Introductory Systems Programming Textbook for the University of Illinois](https://github.com/illinois-cs241/coursebook)

[GitHub - DSC-DYPCOE/Learning-Resources: This repository contains curated, useful resources drafted by DSC Domain Leads.](https://github.com/DSC-DYPCOE/Learning-Resources)

[GitHub - droxey/awesome-teachcode: Awesome resources to use in the classroom, while reviewing code, and when writing tutorials, lesson plans/objectives.](https://github.com/droxey/awesome-teachcode)

[GitHub - patrykwozinski/dev-stuff: Programming stuff for everyone. Collection of articles, videos about architecture, Domain Driven Design, microservices, testing etc.](https://github.com/patrykwozinski/dev-stuff)

[GitHub - KleoPetroff/dev-log: A comprehensive list of links and resources about anything programming related](https://github.com/KleoPetroff/dev-log)

[GitHub - ujjwalchadha8/resourcify.me: This project aims to compile high quality tech resources and road maps from around the internet and make them available under roof in an easy to consume manner. The resources will help you to learn and develop great tech](https://github.com/ujjwalchadha8/resourcify.me)

[GitHub - Timonwa/techroadmap: Open Source. Roadmaps, articles, and useful resources to help you choose a career path, start your journey and grow in tech.](https://github.com/Timonwa/techroadmap)

[GitHub - mikeroyal/Developer-Handbook: Developer-Handbook](https://github.com/mikeroyal/Developer-Handbook)

[GitHub - dreamworkers/developers-toolkit: Useful tools, websites, and services for developers](https://github.com/dreamworkers/developers-toolkit)

[GitHub - Dharaneeshwar/Resource-Bucket: This is a curated and hand-picked collection of learning resources for programmers.](https://github.com/Dharaneeshwar/Resource-Bucket)

[GitHub - ocean1/awesome-thesis: A curated list of practical tips and tricks to help you achieve an awesome CS master thesis [WIP] - contributions are welcome](https://github.com/ocean1/awesome-thesis)

[aboelkassem/awesome_roadmaps: A curated list of roadmaps for the software industry and other technologies from GitHub and other resources](https://github.com/aboelkassem/awesome_roadmaps)

[GitHub - Ishaan28malik/Get-Dev-Resources: Adding Developer resources for best developer practices.](https://github.com/Ishaan28malik/Get-Dev-Resources)

[aaryan2134/Engineering-Resources: List of resources for Engineering Students](https://github.com/aaryan2134/Engineering-Resources)

[GitHub - kunalkeshan/Shiryoku: Incredible resources (with links) to help up-skill yourselves on various fields. Resources like programming, designing, engineering and much more and completely Open Source.](https://github.com/kunalkeshan/Shiryoku)
[Shiryoku (Resources) by Kunal Keshan](https://resources.kunalkeshan.dev/)

[GitHub - kishanrajput23/Ultimate-Resource-Hub: All the resources available here related to many languages, domains, and skills.](https://github.com/kishanrajput23/Ultimate-Resource-Hub)

[GitHub - Eomm/digi-tags: A collection of knowledge resources for IT enthusiast!](https://github.com/Eomm/digi-tags)

[GitHub - etsfactory/reference_material: This repo contains guides and other reference material that may be useful when learning how to use a particular tool or programming language](https://github.com/etsfactory/reference_material)

[GitHub - kappa-wingman/useful-links: List of useful links, tools and resources](https://github.com/kappa-wingman/useful-links)

[GitHub - GDGVIT/Resource-Hub: One stop repository of resources for getting started with any of the mentioned domains](https://github.com/GDGVIT/Resource-Hub)

[GitHub - elfalehed/RTLT: Resources to learn tech (sharing useful links)](https://github.com/elfalehed/RTLT)

[GitHub - daveads/awesome-articles: list of awesome-articles](https://github.com/daveads/awesome-articles)

[GitHub - coder/awesome-coder: A curated list of awesome Coder resources.](https://github.com/coder/awesome-coder)

[GitHub - bhavaniravi/my-favorite-resources: A Repository that showcases developers' favorite resources to learn a technology](https://github.com/bhavaniravi/my-favorite-resources)

[byteshaman/useful-stuff: Basic website in which I store my favorites, useful software etc.](https://github.com/byteshaman/useful-stuff)
[UsefulStuff](https://byteshaman.github.io/useful-stuff/)

[Engineering | Opinionated Guides](https://opguides.info/engineering/engineering/)

[ABSphreak/devLinks: Important links that can help your development toolkit and enhance your skillset.](https://github.com/ABSphreak/devLinks)

[GitHub - vaibhav18matere/developer-support-group: uncommon resources related to tech](https://github.com/vaibhav18matere/developer-support-group)

[GitHub - Source-Pocket/source-pocket: Useful resources for passionate developers.](https://github.com/Source-Pocket/source-pocket)
[Hello from Source Pocket | Source Pocket](https://sourcepocket.netlify.app/)

[GitHub - Design-and-Code/Design-and-Code: Design and Code a global community where anyone can learn and network with fellow developers and designers.](https://github.com/Design-and-Code/Design-and-Code)
[Home | Design and Code](https://designandcode.netlify.app/)

[GitHub - kana-sama/roadmap](https://github.com/kana-sama/roadmap)

[GitHub sunilkumarvalmiki/Anonymous-Developemnt-Resources: this Repo contain's A list of useful development resources . . . .](https://github.com/sunilkumarvalmiki/Anonymous-Developemnt-Resources)

[TopAnswers - Knowledge Communities](https://topanswers.xyz/)

[Katacoda](https://www.katacoda.com/)
Learn new technologies right in your browser
Interactive Learning and Training Platform for Software Engineers

[andriksantos/keebox: This repository is a valuable resource for anyone looking to boost their career in software development. The division of resources by programming language makes it easy to find the information you need, and the focus on including frameworks, libraries, and other resources makes it a comprehensive resource for all types of projects.](https://github.com/andriksantos/keebox)
[Developer Resources | Keebox List ™](https://andriksantos.github.io/keebox/)

[GitHub - Bereket-G/A-for-apple](https://github.com/Bereket-G/A-for-apple)

[GitHub - Uvacoder/uva-tips-cheatsheets-collection](https://github.com/Uvacoder/uva-tips-cheatsheets-collection)

[GitHub - szabgab/awesome-lists: The awesome list of all the awesome lists](https://github.com/szabgab/awesome-lists)

[GitHub - meet59patel/awesome-resources: Awesome Resources, Bookmarks, Websites and Stars of the Web!](https://github.com/meet59patel/awesome-resources)

[Immersion Den](https://immersionden.xyz/)

[JoseDeFreitas/awesome-youtubers: An awesome list of awesome YouTubers that teach about technology. Tutorials about web development, computer science, machine learning, game development, cybersecurity, and more.](https://github.com/JoseDeFreitas/awesome-youtubers)
Programming & Development Learning Channels

[Show HN: Digital Superpowers, a free book highlighting various FOSS tools | Hacker News](https://news.ycombinator.com/item?id=39653634)
[Digital Superpowers: a whirlwind tour of your computer](https://digitalsuperpowers.com/)

[GitHub - tegg89/Deep-blogs: A curated lists of self-taught materials including research blogs](https://github.com/tegg89/Deep-blogs)

[GitHub - mikebronner/interesting-packages-and-articles: List of packages and articles we are interested in using that fulfill specific needs.](https://github.com/mikebronner/interesting-packages-and-articles)

[InfoWorld](http://www.infoworld.com/article/2614635/application-development/-200k-for-a-computer-science-degree--or-these-free-online-classes-.html)

[aGupieWare](http://blog.agupieware.com/2014/05/online-learning-bachelors-level.html)

[OpenCulture](http://www.openculture.com/computer_science_free_courses)

[Open Source Society - Computer Science](https://github.com/open-source-society/computer-science)

[Computer_Science_Web_Resources](https://github.com/the-akira/Computer_Science_Web_Resources)

[No CS Degree](https://www.nocsdegree.com/)

[Google Codelabs](https://codelabs.developers.google.com/?category=web)
[Google Codelabs](https://codelabs.developers.google.com/)

[Online platform for learning tech skills | Hyperskill](https://hi.hyperskill.org/)
Jetbrains sponsored Java beginner courses

[basecs - Medium](https://medium.com/basecs)

[Teach yourself CS](https://teachyourselfcs.com/)

[Google Tech Dev Guide](https://techdevguide.withgoogle.com/)

[GitHub - vicoyeh/pointers-for-software-engineers: A curated list of topics to start learning software engineering](https://github.com/vicoyeh/pointers-for-software-engineers)

[Refactoring and Design Patterns](https://refactoring.guru/)

[[IndieHackers] What books do you recommend?](https://www.indiehackers.com/forum/what-books-do-you-recommend-4dfa511caa)

[/r/learnprogramming books](https://www.reddit.com/r/learnprogramming/wiki/books)

[GitHub - com-puter-tips/Technical-eBooks: PDFs for programming tutorials.](https://github.com/com-puter-tips/Technical-eBooks)

[GitHub - costinEEST/almanacs: Search through the recipes](https://github.com/costinEEST/almanacs)

[GitHub - Tahanima/sqa-set-resources: A curated list of resources for SQA/SET role](https://github.com/Tahanima/sqa-set-resources)

[GitHub - serkanalc/LinkWay: Linkway is a pathway created to reach the right resources for your development process. No code just resource! #linkway #nocode](https://github.com/serkanalc/LinkWay)

[bitsacm/Slack-Stock-DAG: This repository holds a list of cool resources for Silica.](https://github.com/bitsacm/Slack-Stock-DAG)

[GitHub - detailyang/awesome-cheatsheet: awesome cheatsheet](https://github.com/detailyang/awesome-cheatsheet)

[GitHub - squadrun/squad-resources: An index of resources by categories that we find helpful and use quite often. These can be tools, articles, blogs etc.](https://github.com/squadrun/squad-resources)

[GitHub - suco-gt/HPC-Resources: Links for the self-taught HPCer. Or supplemental material. Whatever suits your fancy](https://github.com/suco-gt/HPC-Resources)

[GitHub - parulagg27/allSem-resources](https://github.com/parulagg27/allSem-resources)

[emitron](https://github.com/razeware/emitron-iOS)
[Kodeco | Learn iOS, Android & Flutter](https://www.kodeco.com/)
[Real-time Chat](https://www.kodeco.com/22067733-firebase-tutorial-real-time-chat)

[NetworkChuck](https://networkchuck.com/)

## data science

[GitHub - siboehm/awesome-learn-datascience: Curated list of resources to help you get started with Data Science](https://github.com/siboehm/awesome-learn-datascience)

[geekywrites/datascience: This repository is a compilation of free resources for learning Data Science.](https://github.com/geekywrites/datascience)

[AdiBro/Data-Science-Resources: Data Science related resources and cheatsheets](https://github.com/AdiBro/Data-Science-Resources)
[Data Science Resources | Website with various data science and machine learning resources](https://adibro.github.io/Data-Science-Resources/)

[GitHub - ieshreya/Data-Science-Resources: Free self-taught educational resources for Data Science! I'm currently learning Data Science. I build this repository for helping myself. But if it helps you anyhow, feel free to star it!](https://github.com/ieshreya/Data-Science-Resources)

[cdeweyx/DS-Career-Resources: Compilation of resources for aspiring data scientists](https://github.com/cdeweyx/DS-Career-Resources)

[GitHub - Data-Science-Community-SRM/Resourceify: A curated list of everything you need in the field of Data Science, Machine Learning, and Artificial Intelligence including but not limited to Online Courses, Documentations, Blogs, Podcasts, Cheatsheets, research papers, latest developments etc.. arranged in sub-domains and further by the language or framework being used.](https://github.com/Data-Science-Community-SRM/Resourceify)
[RESOURCEIFY | Resourceify](https://data-science-community-srm.github.io/Resourceify/)

[GitHub - quantmind/awesome-data-science-viz: A curated list of data science, analysis and visualization tools](https://github.com/quantmind/awesome-data-science-viz)

[GitHub - ElizaLo/Data-Science: Projects and awesome list for all Data Science fields](https://github.com/ElizaLo/Data-Science)

[GitHub - firmai/data-science-career: Career Resources for Data Science, Machine Learning, Big Data and Business Analytics Career Repository](https://github.com/firmai/data-science-career)

[GitHub - benthecoder/yt-channels-DS-AI-ML-CS: A comprehensive list of 180+ YouTube Channels for Data Science, Data Engineering, Machine Learning, Deep learning, Computer Science, programming, software engineering, etc.](https://github.com/benthecoder/yt-channels-DS-AI-ML-CS)

[Learn Data Science - Python, R, SQL, PowerBI](https://www.dataquest.io/)

[Launch Your Career in Data Science](https://elitedatascience.com/)

[Free Data Analytics Course: Learn the Skills to Thrive in a Data-Driven World](https://www.springboard.com/resources/learning-paths/data-analysis/)

[Learn Data Science and AI Online | DataCamp](https://www.datacamp.com/)

[The Turing Way](https://github.com/alan-turing-institute/the-turing-way)
A series of open source guides about data science and AI. Contributors can add to new and ongoing chapters, work on translation efforts, contribute to infrastructure maintenance work within the project, and more.

[Data Science Notes](https://github.com/wyattowalsh/data-science-notes)
Share notes across topics in data science such as mathematics, visualization, and modeling!

[academic/awesome-datascience: An awesome Data Science repository to learn and apply for real world problems.](https://github.com/academic/awesome-datascience)

[GitHub - andkret/Cookbook: The Data Engineering Cookbook](https://github.com/andkret/Cookbook)
[Learn Data Engineering with Courses & Coaching | Learn Data](https://learndataengineering.com/)

[Jeroen Janssens](http://datascienceatthecommandline.com/)
Data Science at the Command Line

[We're Building Data Science Courses with Advanced Mathematics and Machine Learning](https://www.freecodecamp.org/news/building-a-data-science-curriculum-with-advanced-math-and-machine-learning)

[Learning Data Science — Learning Data Science](https://learningds.org/intro.html)

## data science - python

[Applied Data Science with Python – Business Intelligence for Developers [Full Book]](https://www.freecodecamp.org/news/applied-data-science-with-python-book/)

## dev certifications

[1000+ Free Developer Certifications](https://www.freecodecamp.org/news/free-certificates)

## general programming tutorials

[Your Career in Web Development Starts Here | The Odin Project](https://www.theodinproject.com/)
[The Odin Project](https://www.theodinproject.com/dashboard)
Free Tutorials
Skills: Front End,Back End,Technical Interviewing
Sub-Skills: HTML,CSS,JavaScript,React.js,jQuery,Sass,Ruby,Ruby on Rails,Git,SQL
Mostly references to other sources (e.g. Codecademy) for learning materials and assignments. Very crude structure, would require a lot of extra work and discipline. Do not recommend as sole resource.

[Teach Yourself Programming in Ten Years (1998) | Hacker News](https://news.ycombinator.com/item?id=39001755)
[Teach Yourself Programming in Ten Years](https://norvig.com/21-days.html)

## history

[GitHub - watson/awesome-computer-history: An Awesome List of computer history videos, documentaries and related folklore](https://github.com/watson/awesome-computer-history)

## livecoding

[GitHub - toplap/awesome-livecoding: All things livecoding](https://github.com/toplap/awesome-livecoding)

[livecoders](https://github.com/toplap/livecoders)

## mobile development

[GitHub - jerielng/mobile-guide: Curated list of resources and tips for aspiring cross-platform mobile developers](https://github.com/jerielng/mobile-guide)

[GitHub - brentonhouse/geek-mobile: Geek Mobile Toolkit - Everything a geek needs to create, build, and manage cross-platform native mobile apps.](https://github.com/brentonhouse/geek-mobile)

## passionate programmer

[onaclov2000/PassionateProgrammer](https://github.com/onaclov2000/PassionateProgrammer)
a list of the tips from the book "Passionate Programmer"

## programmer pioneers

[GitHub - rekihattori/awesome-programmers: A list of history's greatest software engineers and tech pioneers](https://github.com/rekihattori/awesome-programmers)

## Programming Basics

210 Programming:

[TeachYourselfCS1] Structure and Interpretation of Computer Programs (SICP)
course
video series
  work through at least first 3 chapters and do exercises
    [Computer Science 61A, 001 - Spring 2011 : Free Movies : Free Download, Borrow and Streaming : Internet Archive](https://archive.org/details/ucberkeley-webcast-PL3E89002AA9B9879E?sort=title)
    [Structure and Interpretation of Computer Programs | Electrical Engineering and Computer Science | MIT OpenCourseWare](https://ocw.mit.edu/courses/6-001-structure-and-interpretation-of-computer-programs-spring-2005/)
    [Welcome to the SICP Web Site](https://mitp-content-server.mit.edu/books/content/sectbyfn/books_pres_0/6515/sicp.zip/index.html)
    Structure and Interpretation of Computer Programs (1996)
    [Welcome to the SICP Web Site](https://mitp-content-server.mit.edu/books/content/sectbyfn/books_pres_0/6515/sicp.zip/index.html)
    [gentoomen library](https://g.sicp.me/books/)
    [gentoomen library](https://web.archive.org/web/20210102182957/https://g.sicp.me/books/)
    [Why "Structure and Interpretation of Computer Programs" matters (2011) | Hacker News](https://news.ycombinator.com/item?id=40698906)
    [Why <cite>Structure and Interpretation of Computer Programs</cite> matters](https://people.eecs.berkeley.edu/~bh/sicp.html)
[TeachYourselfCS1alt]
PDF - How to Design Programs (DrRacket)
much easier
course
    [How to Design Programs](https://htdp.org/)
[TeachYourselfCS1InferiorAlt] Composing Programs (uses Python)
course
    [Composing Programs](https://www.composingprograms.com/)
[TeachYourselfCS2]
    [Exercism.io](http://exercism.org/)
    Free Code Challenges,Code Reviews
    Skills: Front End,Back End,Mobile Development,Computer Science
    Sub-Skills: C,C++,C#,Clojure,CFML,CoffeeScript,Common Lisp,D,Dart,Delphi Pascal,ECMAScript,Elixir,Elm,Emacs Lisp,Erlang,F#,Go,Haskell,Java,JavaScript,Julia,Kotlin,LFE,Lua,MIPS Assembly,Objective-C,OCaml,PHP,PL/SQL,Prolog,Perl,PureScript,Python,R,Racket,Ruby,Rust,Scala,Scheme,Standard ML,Swift,TypeScript,Vim Script
    Features code challenges with a focus on test-driven development as well as code readability, which is unique. Code challenge submission will be reviewed by other developers, who will then provide feedback to the coder to improve. Have an impression that all the steps are done anonymously.
    [Exercism](http://exercism.io/)

The hardest part of learning how to program is _not_ learning how a programming language works: it's learning how to _solve problems_ with code.

freeCodeCamp dev quiz - Prog Basics/Features
- what is encapsulation in coding?
- What is a parallel array?
- What is a high order function?
- What's the difference between a "for" and "while" loop?
- The rules that determine the correct structure of the code in a computer program are known as syntax.
- The value of a const variable in JS must be specified when the varible is declared.
- The sequence of statements in a do..while loop runs at least once because the condition is evaluated after running the statements.
- If functions can be sent and received just like values, than that languge is said to have first class functions. They are also called first class citizens.
- An argument is a value passed to a function (or method) when the function or method is called.
- Object destructuring is used to extract an object's values into new variables.
- A special symbol used to perform arithmetic or logical computations is known as operator.
- The rest operator takes the individual arguments passed to a function and converts them into an array.
- The bind function returns a new function with given arguments as the new function's 'this' keyword. [Function.prototype.bind() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_objects/Function/bind)
- Each one of the alternative sequence of statements in a conditional statement is known as a branch.
- A computer programming language used for inserting, deleting, and updating data in a database is known as a Data Manipulation Language.
- What is a [Data control](https://en.wikipedia.org/wiki/Data_control_language) language?
- The value undefined is returned by functions that do not have a return statement in JS, but returns None in Python.
- The spread operator can be used to copy portions of an array or object into another array or object.

[GitHub - packing-box/awesome-executable-packing: A curated list of awesome resources related to executable packing](https://github.com/packing-box/awesome-executable-packing)
- _Packing_ is the action of modifying an executable in a way that does not modify its purpose. It is generally one or a combination of the following operations:
	- bundling: makes a single executable with multiple files
	- compression: compresses the executable to reduce its original size
	- encoding: obfuscates the executable by encoding it
	- encryption: obfuscates the executable by encrypting it
	- mutation: alters the executable's code so that it uses a modifided instruction set and architecture (e.g. using oligomorphism)
	- protection: makes the reversing of the executable harder (i.e. using anti-debugging, anti-tampering or other tricks)
	- virtualization: embeds a virtual machine that allows to virtualize executable's instructions

## programming books

[Ask HN: Books that teach programming by building a series of small projects? | Hacker News](https://news.ycombinator.com/item?id=34412069)

[How to Learn to Code & Get a Developer Job in 2023 [Full Book]](https://www.freecodecamp.org/news/learn-to-code-book)

[Knuth's Art of Computer Programming, V 4B, has gone into print | Hacker News](https://news.ycombinator.com/item?id=33082128)
[The Art of Computer Programming - Wikipedia](https://en.wikipedia.org/wiki/The_Art_of_Computer_Programming)
[GNU MDK - GNU Project - Free Software Foundation🆓](https://www.gnu.org/software/mdk)

## roadmaps - front-end

[Web Skills](https://andreasbm.github.io/web-skills/)

[RPG variant](http://www.dungeonsanddevelopers.com/)

[The 2018 Web Developer Roadmap. An illustrated guide to becoming a… | by Brandon Morelli | codeburst](https://codeburst.io/the-2018-web-developer-roadmap-826b1b806e8d?gi=7d3d975e60b3)

[The 2023 Web Developer Roadmap. Learn to become a Frontend, Backend… | by Trey Huffine | Level Up Coding](https://levelup.gitconnected.com/the-2020-web-developer-roadmap-76503ddfb327?gi=0bf36a5f7bee)

[The Front-End Developer Learning Roadmap by Frontend Masters](https://frontendmasters.com/guides/learning-roadmap/)
roadmap for becoming a "complete" front end (+ back end + devops etc.) developer

[FrontEndMasters](https://frontendmasters.com/)

## roadmaps

[GitHub - kamranahmedse/developer-roadmap: Interactive roadmaps, guides and other educational content to help developers grow in their careers.](https://github.com/kamranahmedse/developer-roadmap)

[GitHub - orsanawwad/awesome-roadmaps: View roadmaps about developer roles to help you learn](https://github.com/orsanawwad/awesome-roadmaps)

[GitHub - liuchong/awesome-roadmaps: A curated list of roadmaps.](https://github.com/liuchong/awesome-roadmaps)

[Roadmap.sh](https://roadmap.sh/)
roadmap for becoming a "complete" front end (+ back end + devops etc.) developer

[GitHub - Uncodedtech/RoadmapsResources: This repository includes links to forked repositories which hold a list of different developer roadmaps and resources.](https://github.com/Uncodedtech/RoadmapsResources)

[Non-visual but super comprehensive](https://hawkticehurst.com/mega-full-stack-resource-guide/)

## software engineering

[Foundations of Software Engineering | Hacker News](https://news.ycombinator.com/item?id=24949322)
[CMU 17-313: Foundations of Software Engineering - CMU 17-313: Foundations of Software Engineering](https://cmu-313.github.io/)

[Brian Kelly](https://morethancoding.com/2011/02/27/the-greatest-software-stories-ever-told/)
(2011) [Book] The Greatest Software Stories Ever Told

[Julian Cohen](https://medium.com/@HockeyInJune/secure-engineering-guidelines-3b8845ac3265)
(2017) Secure Engineering Guidelines
Some best practices for building and trusting software.

[Bohdan Balov](https://betterprogramming.pub/lead-software-engineer-roadmap-37b8fc10a93f)
(2022) The Roadmap of a Lead Software Engineer
Experience and knowledge you need to gain to become a lead software engineer

## typing tests

[Typing.io](https://typing.io/)
Typing Practice for Programmers

## hacktoberfest

[Hacktoberfest](https://hacktoberfest.digitalocean.com/)
Free Party Time,Open-Source
Skills: Front End,Back End,Mobile Development,Computer Science,Data Analysis,Documentation
Sub-Skills: Pull Requests,C++,Julia,Rust,Go,C#,Python,Ruby,PHP,Java,CSS,JavaScript,Haskell,Algorithms,Meteor.js,Ruby on Rails
A month-long celebration for open-source projects and official invitation to contribute. Good place to start contributing to real-world projects (e.g. Parity Ethereum, Discord, etc.) and practicing code. If some of the projects are too hard, freeCodeCamp has a place for beginners to start practicing how to contribute (https://guide.freecodecamp.org/). Hacktoberfest mails out free T-shirts and stickers if you make at least 4 pull requests anytime from 1 October - 31 October. During this period, there will also be local meetups, depending on your area.

## coding

[GitHub - gazaskygeeks/Coding-Foundations-course](https://github.com/gazaskygeeks/Coding-Foundations-course)

[Paul Ford: What Is Code? | Bloomberg](https://www.bloomberg.com/graphics/2015-paul-ford-what-is-code)

[How to Start Learning to Code - Handbook for Beginners](https://www.freecodecamp.org/news/learn-coding-for-everyone-handbook/)

[How to Learn to Code and Get a Developer Job [Full Book]](https://www.freecodecamp.org/news/learn-to-code-book/)

## programming

[What is Programming? A Handbook for Beginners](https://www.freecodecamp.org/news/what-is-programming-tutorial-for-beginners)

[What is Computer Programming? Defining Software Development.](https://www.freecodecamp.org/news/what-is-computer-programming-defining-software-development)

[James Hood](https://dev.to/jlhcoder/tips-for-new-software-developers)
Tips for New Software Developers

[Software Engineering Tips](http://www.yacoset.com/Home/programming-tips)
(2010) Programming Tips

## concurrency - swift

[SwiftUI Concurrency Essentials](https://github.com/peterfriese/SwiftUI-Concurrency-Essentials)

## naming conventions

[Jonathan Boccara](http://www.fluentcpp.com/2017/01/30/how-to-choose-good-names/)
(2017) How to choose good names in your code

[Tom Benner](https://namingthings.co/)
(2023) A book about the naming things in software engineering
