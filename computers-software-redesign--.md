
[Dummied Out - TV Tropes](https://tvtropes.org/pmwiki/pmwiki.php/Main/DummiedOut)
- older hardware (i.e., when coded straight to firmware) requires invalidating code more than removing it
    - it opens up opportunities for [hacking] as well!

freeCodeCamp dev quiz - Software Redesign

- An IndexError is raised in Python when you try to index a list, tuple, or string beyond the permitted boundaries.
- A RecursionError in Python occurs when the interpreter detects that the maximum recursion depth is exceeded. This usually occurs when the recursive process never reaches the base case.
- A NameError is raised in Python when a name that you are referencing in the code doesn't exist.
- A ZeroDivisionError is raised in Python when you try to divide by zero.
- A KeyError is raised in Python when you try to access the value of a key that doesn't exist in a dictionary.
- A TypeError is raised in Python when an operation or function is applied to an object of an inappropriate type.
- Function overloading is when you have multiple functions with the same name but with different parameters. This results in the function being overloaded with different jobs.
- Hoisting is the process of moving variables, classes, and functions to the top of the scope.

Here's a couple considerations that factor into being a good QA engineer:

- Do you take the time to understand why the bug is happening?
    Alongside the clearly defined and reproducible steps, do you have
    insight into why the issue might be occurring and how to fix it? Is
    there a similar bug from the past that might help? Can you point to the
    exact lines of code responsible for this bug? (You might think this last one is crazy but I've had QA engineers that did this and I was beyond
    impressed)
- Do you take the time to make complicated or not easily reproducible bugs more reproducible?
- If there are tests that the devs need to run themselves, have you automated or streamlined that process?
- Have you grokked the code base and understood how the app
    functions? This is important because it allows you to have a better
    understanding of what is a trivial bug and what is a significant
    undertaking, allowing your team better planning.
- Do you stay actively involved throughout the sprint and know when requirements have changed? Instead of making it the responsibility of
    the devs to include you, do you include yourself since you know it's
    relevant to your testing?
- Do you anticipate bugs that may arise with new features and preemptively point them out as requirements?

## Debugging

[Coding in the Debugger (2007) | Hacker News](https://news.ycombinator.com/item?id=37690320)
[Coding in the Debugger - by Kent Beck](https://tidyfirst.substack.com/p/coding-in-the-debugger)
- this is WAY more advanced than print-based, but it's pretty cool

[GitGuardian/ggshield: Find and fix 360+ types of hardcoded secrets and 70+ types of infrastructure-as-code misconfigurations.](https://github.com/GitGuardian/ggshield)
- MAKE SURE TO REMOVE SECRETS AND PERSONAL CONTENT IF THE THING BECOMES PUBLIC

## testing and debugging

Most developers hate testing. They tend to test gently, subconsciously knowing where the code will break and avoiding the weak spots. Pragmatic Programmers are different. We are driven to find our bugs now, so we don't have to endure the shame of others finding our bugs later.

A good project may well have more test code than production code.

Types of software testing that you need to perform:
- Unit testing
- Integration testing
- Validation and verification
- Resource exhaustion, errors, and recovery
- Performance testing
- Usability testing

Integration testing shows that the major subsystems that make up the project work and play well with each other.
When the system does fail, will it fail gracefully?

You need data to stress the boundary conditions. This data may be completely synthetic: date fields containing February 29, 1999, huge record sizes, or addresses with foreign postal codes.

Once a human tester finds a bug, it should be the last time a human tester finds that bug. The automated tests should be modified to check for that particular bug from then on, every time, with no exceptions, no matter how trivial,

## alpha and beta

[Obvious Beta - TV Tropes](https://tvtropes.org/pmwiki/pmwiki.php/Main/ObviousBeta)

## asserts

[Bill Wake](https://www.industriallogic.com/blog/multiple-asserts-are-ok/)
(2015) Multiple Asserts Are OK
Some people suggest we should restrict ourselves to a single assertion per test. Are multiple asserts in a test ever OK?

## auto increment

[Clément Delafargue](https://www.clever-cloud.com/blog/engineering/2015/05/20/why-auto-increment-is-a-terrible-idea/)
(2015) Why Auto Increment Is A Terrible Idea
interesting debate in the comments

## bad code

[Ask HN: Started a new job and their existing code sucks. What to do? | Hacker News](https://news.ycombinator.com/item?id=16233961)

[Nicolai M. Josuttis](http://www.josuttis.com/WelcomeCrappyCode.html)
(2009) Welcome Crappy Code - The Death of Code Quality

[Serge Beaumont](http://blog.xebia.com/do-you-worry-about-crappy-code-then-face-reality-and-grow-up/)
(2009) Do you worry about crappy code? Then face reality and grow up.

[Itamar Turner-Trauring](https://codewithoutrules.com/2017/11/07/no-such-thing-as-bad-code/)
(2017) There’s no such thing as bad code

[Applying the Linus Torvalds “Good Taste” Coding Requirement](https://web.archive.org/web/20161220124347/https://medium.com/@bartobri/applying-the-linus-tarvolds-good-taste-coding-requirement-99749f37684a)
(2016) Applying the Linus Torvalds “Good Taste” Coding Requirement

[Michal Ciurus](http://yourcodesucksexception.blogspot.be/2014/11/your-code-sucks.html)
(2014) Your code sucks - things you need to know about clean code and architecture

[Idiot Programming/Darth Wiki - TV Tropes](https://tvtropes.org/pmwiki/pmwiki.php/DarthWiki/IdiotProgramming)

["We ran out of columns" | Hacker News](https://news.ycombinator.com/item?id=41146239)
["We ran out of columns" - The best, worst codebase](https://jimmyhmiller.github.io/ugliest-beautiful-codebase)

## bug hunting

[Gitlab and NFS bug](https://about.gitlab.com/2018/11/14/how-we-spent-two-weeks-hunting-an-nfs-bug/)
how we spent two weeks hunting an NFS bug in the Linux kernel.

## bugs and errors

[Error Index - TV Tropes](https://tvtropes.org/pmwiki/pmwiki.php/Main/ErrorIndex)

[The weirdest bug I've seen yet | Hacker News](https://news.ycombinator.com/item?id=38477100)
[The Weirdest Bug I've Seen Yet](https://engineering.gusto.com/the-weirdest-bug-ive-seen-yet/)

[The Safari bug that never was (2022) | Hacker News](https://news.ycombinator.com/item?id=34289328)
[The Safari bug that never was](https://obyford.com/posts/the-safari-bug-that-never-was/)

[Bugs in Hello World | Hacker News](https://news.ycombinator.com/item?id=30611367)
[Bugs in Hello World · sunfishcode's blog](https://blog.sunfishcode.online/bugs-in-hello-world/)
[sunfishcode's blog](https://blog.sunfishcode.online/)

[Cut the cutesy errors | Hacker News](https://news.ycombinator.com/item?id=32337520)
[Cut the cutesy errors - alexwlchan](https://alexwlchan.net/2022/no-cute/)

[The code worked differently when the moon was full | Hacker News](https://news.ycombinator.com/item?id=28686016)
[The code worked differently when the moon was full - Scott Hanselman's Blog](https://www.hanselman.com/blog/the-code-worked-differently-when-the-moon-was-full)

[Null | Hacker News](https://news.ycombinator.com/item?id=25771953)
[null - Alan Pope's blog](https://popey.com/blog/2021/01/null/)

[Spending 3 months investigating a 7-year old bug and fixing it in 1 line of code | Hacker News](https://news.ycombinator.com/item?id=40749624)
[The time I spent three months investigating a 7-year old bug and fixed it in 1 line of code - Lemmy.World](https://lemmy.world/post/16763534)

## bug tracking

[Joël Spolsky](https://www.joelonsoftware.com/2000/11/08/painless-bug-tracking/)
(2000) Painless Bug Tracking

## code reviews

[How to Make Your Code Reviewer Fall in Love with You | Hacker News](https://news.ycombinator.com/item?id=25330182)
[How to Make Your Code Reviewer Fall in Love with You · mtlynch.io](https://mtlynch.io/code-review-love/)

[Why is it so hard to see code from 5 minutes ago? | Hacker News](https://news.ycombinator.com/item?id=26187881)
[Why is it so hard to see code from 5 minutes ago? - Austin Z. Henley](https://web.archive.org/web/20221222191713/https://austinhenley.com/blog/yestercode.html)

[Ask HN: What's the best source code you've read? | Hacker News](https://news.ycombinator.com/item?id=32793534)

[Vaidehi Joshi](https://dev.to/vaidehijoshi/crafting-better-code-reviews)
Crafting Better Code Reviews

[Karl E. Wiegers](http://www.processimpact.com/articles/humanizing_reviews.html)
Humanizing Peer Reviews

[Bruce Johnson](https://blog.fullstory.com/what-we-learned-from-google-code-reviews-arent-just-for-catching-bugs-b125a13aa292)
What we learned from Google: code reviews aren’t just for catching bugs

[Safia Abdalla](https://blog.safia.rocks/post/170269021619/tips-for-reading-new-codebases)
(2018) Tips for reading new codebases

[Stack Exchange](https://codereview.stackexchange.com/)
Stack Exchange for code reviews

[Lawrence Kesteloot](https://www.teamten.com/lawrence/writings/the_language_squint_test.html)
(2008) The Language Squint Test

[Joe L. Wroten](https://dev.to/sharpshark28/self-code-review-with-git-add-patch)
Self Code Review with Git Add Patch

[Thomas Paul Mann](https://raycast.com/blog/no-code-reviews-by-default/)
(2021) No code reviews by default
How one built an engineering culture based on trust that allows us to move incredibly fast without requiring code reviews.

[Elisabeth Irgens](https://elisabethirgens.github.io/notes/2021/06/code-reviews/)
(2021)
Why I Won’t Approve Your PR
in-house development has been influenced too much by the GitHub open source PR driven development process. A process driven by zero trust doesn’t fit well in a team with trust.

[Umer Mansoor](https://codeahoy.com/2016/04/03/effective-code-reviews/)
(2016) Effective Code Reviews

[Jeff Wainwright](https://css-tricks.com/code-review-etiquette/)
(2017) Code Review Etiquette

[Erlend Hamberg](https://hamberg.no/erlend/posts/2010-03-20-code-reading-as-a-team-activity.html)
(2010) Code Reading as a Team Activity

[William Shawn](https://spin.atomicobject.com/2017/06/01/how-to-read-code/)
(2017) How to Read Code (Eight Things to Remember)

[Tyler Hoffman](https://spin.atomicobject.com/2017/07/29/code-reviews-boost-productivity/)
(2017) Code Reviews as a Tool to Boost Productivity

## compiler warnings_c++

[c++ - Why should I always enable compiler warnings? - Stack Overflow](https://stackoverflow.com/questions/57842756/why-should-i-always-enable-compiler-warnings)

## debugging

[When LIMIT 9 works but LIMIT 10 hangs | Hacker News](https://news.ycombinator.com/item?id=36138642)
[When LIMIT 9 works but LIMIT 10 hangs, a short debugging story - Neon](https://neon.tech/blog/when-limit-9-works-but-limit-10-hangs)

[Debugging a Linux network stack crash via a single register value | Hacker News](https://news.ycombinator.com/item?id=29260464)
[The tale of a single register value](https://blog.cloudflare.com/the-tale-of-a-single-register-value/?a)

[Uncovering a 24-year-old bug in the Linux Kernel (2021) | Hacker News](https://news.ycombinator.com/item?id=33214439)
[Uncovering a 24-year-old bug in the Linux Kernel - Skroutz Engineering](https://engineering.skroutz.gr/blog/uncovering-a-24-year-old-bug-in-the-linux-kernel/)

[Jaroslav Tulach](http://www.methodsandtools.com/archive/debugger.php)
Use the Debugger. Stupid!

[Brian Vanderwal](https://spin.atomicobject.com/2017/11/28/less-time-debugging/)
(2017) Six Strategies to Spend Less Time Debugging

[R0ml](https://codewords.recurse.com/issues/one/why-are-objects-so-hard-to-debug)
Why are objects so hard to debug?

[ServiceNow Docs](http://wiki.servicenow.com/index.php?title=Debugging_Business_Rules#gsc.tab=0)
Debugging Business Rules

[Kode Vicious](https://queue.acm.org/detail.cfm?id=1740550)
(2010) Broken Builds
Frequent broken builds could be symptomatic of deeper problems within a development project.

[Jessy Bernal](https://medium.com/doctolib-engineering/handling-bugs-at-doctolib-847d54fd1990)
(2017) Handling bugs at Doctolib

[A decade-old Steam bug | Hacker News](https://news.ycombinator.com/item?id=38977128)
[A decade long Steam issue, is everyone just too fast for Valve? | freudenjmp](https://blog.freudenjmp.com/posts/no-user-logon/)

## error culture

[Ascended Glitch - TV Tropes](https://tvtropes.org/pmwiki/pmwiki.php/Main/AscendedGlitch)

## integrated tests

[J. B. Rainsberger](http://blog.thecodewhisperer.com/permalink/integrated-tests-are-a-scam)
Integrated Tests Are A Scam

## large consequences

[Gitlab password reset bug leaves more than 5.3K servers up for grabs | Hacker News](https://news.ycombinator.com/item?id=39159002)
[GitLab password reset bug leaves more than 5.3K servers up for grabs | SC Media](https://www.scmagazine.com/news/gitlab-password-reset-bug-leaves-more-than-5-3k-servers-up-for-grabs)

## latency

[Philip Stark](https://gist.github.com/hellerbarde/2843375)
Latency numbers every programmer should know

## lean software

[A 2024 plea for lean software | Hacker News](https://news.ycombinator.com/item?id=39315585)
[Why Bloat Is Still Software's Biggest Vulnerability - IEEE Spectrum](https://spectrum.ieee.org/lean-software-development)

## legacy hardware

[Junkyard computing - repurposing discarded smartphones to minimize pollution | Hacker News](https://news.ycombinator.com/item?id=34742266)
[Junkyard Computing: Repurposing Discarded Smartphones to Minimize Carbon - 3575693.3575710.pdf](https://dl.acm.org/doi/pdf/10.1145/3575693.3575710)

## legacy software - browser updates

[GitHub - styfle/breaking-changes-web: A list of breaking changes to the web platform](https://github.com/styfle/breaking-changes-web)

## legacy software

[The optional chaining operator, "modern" browsers, and my mom | Hacker News](https://news.ycombinator.com/item?id=29894300)
[The Optional Chaining Operator, "Modern" Browsers, and My Mom - Jim Nielsen's Blog](https://blog.jim-nielsen.com/2022/a-web-for-all/)

## linting

[Interesting Bugs Caught by ESLint's no-constant-binary-expression (2022) | Hacker News](https://news.ycombinator.com/item?id=38196644)
[Interesting bugs caught by no-constant-binary-expression - ESLint - Pluggable JavaScript Linter](https://eslint.org/blog/2022/07/interesting-bugs-caught-by-no-constant-binary-expression/)

[Horia Coman](https://dev.to/horia141/jupiter-dev-log-3-lint-all-the-things-51lh)
(2020) Jupiter Dev Log 3 - Lint All The Things

## log files

[Duncan Crombie](http://www.the-art-of-web.com/system/logs/)
System: Analyzing Apache Log Files

[Tim O'Brien](https://discursive.com/2013/10/30/how-to-get-your-crazy-logs-under-control/)
(2013) 10 Steps to Get Your Crazy Logs Under Control

[Sumit Maingi](https://cloudncode.blog/2016/12/30/what-should-you-log-in-an-application-and-how-to-avoid-having-24x7-support-looking-at-them/)
(2016) What should you log in an application and how to avoid having 24×7 support looking at them?

## machine learning assists

[Software 2.0 (2017) | Hacker News](https://news.ycombinator.com/item?id=34881881)
[Software 2.0. I sometimes see people refer to neural… | by Andrej Karpathy | Medium](https://karpathy.medium.com/software-2-0-a64152b37c35)

## memory corruption

[Debugging memory corruption: who the hell writes "2" into my stack? (2016) | Hacker News](https://news.ycombinator.com/item?id=29215725)
[Debugging memory corruption: Who wrote '2' into my stack?! | Unity Blog](https://blog.unity.com/engine-platform/debugging-memory-debugging-memory-corruption-who-wrote-2-into-my-stack-who-the-hell)

## no-shot machine learning

[Karen Hao](https://www.technologyreview.com/2020/10/16/1010566/ai-machine-learning-with-tiny-data)
(2020) A radical new technique lets AI learn with practically no data
“Less than one”-shot learning can teach a model to identify more objects than the number of examples it is trained on.

## optimizing

[Speed Matters | Hacker News](https://news.ycombinator.com/item?id=28879240)
[Speed matters](https://www.scattered-thoughts.net/writing/speed-matters/)

[Speed Is the Killer Feature | Hacker News](https://news.ycombinator.com/item?id=26312516)
[Speed is the killer feature - bdickason.com](https://bdickason.com/posts/speed-is-the-killer-feature/)

[Surprisingly Slow | Hacker News](https://news.ycombinator.com/item?id=26710763)
[Gregory Szorc's Digital Home | Surprisingly Slow](https://gregoryszorc.com/blog/2021/04/06/surprisingly-slow/)

[Operation Costs in CPU](http://ithare.com/infographics-operation-costs-in-cpu-clock-cycles/)
should help to estimate costs of certain operations in CPU clocks.

[StackExchange](https://stackexchange.com/performance)
Amazing presentation of Stack Exchange infrastructure. All about performance

[Optimizing the Lichess Tablebase Server | Hacker News](https://news.ycombinator.com/item?id=40949943)
[revoof's Blog • Optimizing the tablebase server • lichess.org](https://lichess.org/@/revoof/blog/optimizing-the-tablebase-server/MetV0ZQd)

[The art of high performance computing | Hacker News](https://news.ycombinator.com/item?id=38815334)
[The Art of HPC](https://theartofhpc.com/)

[My £4 a month server can handle 4.2M requests a day | Hacker News](https://news.ycombinator.com/item?id=28449162)
[My £4 a month server can handle 4.2 million requests a day](https://mark.mcnally.je/blog/post/My%20%C2%A34%20a%20month%20server%20can%20handle%204.2%20million%20requests%20a%20day)

[Achieving 11M IOPS and 66 GB/S IO on a Single ThreadRipper Workstation | Hacker News](https://news.ycombinator.com/item?id=25956670)
[Achieving 11M IOPS & 66 GB/s IO on a Single ThreadRipper Workstation | Tanel Poder Consulting](https://tanelpoder.com/posts/11m-iops-with-10-ssds-on-amd-threadripper-pro-workstation/)

[56TB Zpool Upgrade - b3n.org](https://b3n.org/56tb-zpool-upgrade)

[A 1.5GB string | Hacker News](https://news.ycombinator.com/item?id=35496712)
[a 1.5GB string - BackSlasher](https://blog.backslasher.net/1.5GB-string.html)

[Squeeze the hell out of the system you have | Hacker News](https://news.ycombinator.com/item?id=37091983)
[Squeeze the hell out of the system you have - Dan Slimmon](https://blog.danslimmon.com/2023/08/11/squeeze-the-hell-out-of-the-system-you-have/#like-2777)

## print debugging

[The unreasonable effectiveness of print debugging | Hacker News](https://news.ycombinator.com/item?id=26925570)
[Starting this newsletter, print debugging, BYOC • Buttondown](https://buttondown.email/geoffreylitt/archive/starting-this-newsletter-print-debugging-byoc/)

## rebuilding code

[Joël Spolsky](https://www.joelonsoftware.com/2000/04/06/things-you-should-never-do-part-i/)
(2000) Things You Should Never Do, Part I
About rewriting code from scratch

[Spencer Baugh](https://catern.com/change_code.html)
(2022) Prefer to change the code rather than write a workaround

## refactoring

[J. B. Rainsberger](http://blog.thecodewhisperer.com/permalink/musings-on-refactoring-as-waste)
(2014) Musings on Refactoring as Waste

[Omar El Gabry](https://hackernoon.com/refactoring-the-hygienic-habit-b2ee0f5528ba)
Refactoring — The Hygienic Habit

[Andy Zaidman](https://azaidman.wordpress.com/2015/01/19/old-habits-die-hard-why-refactoring-for-understandability-does-not-give-immediate-benefits/)
(2015) Old Habits Die Hard: Why Refactoring for Understandability Does Not Give Immediate Benefits

[Rule of three (computer programming)](https://en.wikipedia.org/wiki/Rule_of_three_%28computer_programming%29)
only refactor when similar code is used three times (and more)

[Bill Wake](https://www.industriallogic.com/blog/isolate-improve-inline-refactoring-tactic/)
(2016) Isolate-Improve-Inline: The 3-I Refactoring Tactic

## resolving issues

[There are no open issues or pull requests on Flask | Hacker News](https://news.ycombinator.com/item?id=31953470)
[David Lord on Twitter: "I've done it. I've achieved the open source maintainer platinum trophy. There are ✨no open issues or pull requests on Flask ✨, a framework downloaded 75 million times in the last month. https://t.co/PIJbJ7cb3P" / Twitter](https://web.archive.org/web/20220701194216/https://twitter.com/davidism/status/1542956488355762176)

## reviewing logs

[I looked through attacks in my access logs | Hacker News](https://news.ycombinator.com/item?id=39165711)
[I looked through attacks in my access logs. Here's what I found](https://nishtahir.com/i-looked-through-attacks-in-my-access-logs-heres-what-i-found/)

[Charity Majors aka mipsytipsy](https://honeycomb.io/blog/2017/04/lies-my-parents-told-me-about-logs/)
(2017) Lies My Parents Told Me (About Logs)

[Download Free Utilities From SystemTools Software Inc](https://www.systemtools.com/somarsoft/index.html)

## safety critical programs

[RankRed](http://www.rankred.com/nasa-coding-rules/)
NASA’s 10 Coding Rules for Writing Safety Critical Program
:star:

[awesome-safety-critical - awesome-safety-critical 0.1 documentation](https://awesome-safety-critical.readthedocs.io/en/latest/)
[GitHub - stanislaw/awesome-safety-critical: List of resources about programming practices for writing safety-critical software.](https://github.com/stanislaw/awesome-safety-critical)
resources about programming practices for writing safety-critical software.

## secure with insecure content

[How to fix mixing of secure and insecure content on a web page](https://www.a2hosting.com/kb/security/ssl/secure-and-insecure-content-on-a-web-page)

## self-inflicted problems

[Have you ever hurt yourself from your own code? | Hacker News](https://news.ycombinator.com/item?id=27292219)
[Have you ever hurt yourself from your own code?](https://blog.nikitas.link/have-you-ever-hurt-yourself-from-your-own-code)

[It Can Happen to You | Hacker News](https://news.ycombinator.com/item?id=26337046)
[It Can Happen to You](https://www.mattkeeter.com/blog/2021-03-01-happen/)

## software redesign

[Tamir Bahar](https://dev.to/tmr232/dont-amend-fix)
Don't Amend, Fix

[Andrew Yurisich/unmaintainable-code](https://github.com/Droogans/unmaintainable-code)
How To Write Unmaintainable Code.
[Original article by Roedy Green / Canadian Minds](https://www.doc.ic.ac.uk/~susan/475/unmain.html)

[Brian Vanderwal](https://spin.atomicobject.com/2017/03/07/attitudes-maintainable-code/)
(2017) Three Attitudes that Lead to Maintainable Code

[Thomas Figg (tef)](https://programmingisterrible.com/post/139222674273/write-code-that-is-easy-to-delete-not-easy-to)
(2016) Write code that is easy to delete, not easy to extend.

## testing

[Working as a Software Tester; nobody gives a damn : cscareerquestions](https://old.reddit.com/r/cscareerquestions/comments/twrrxu/working_as_a_software_tester_nobody_gives_a_damn)

[I'm the high QA guy. Let me test your website | Hacker News](https://news.ycombinator.com/item?id=26042416)
[The High QA Guy](https://web.archive.org/web/20210217001006/http://www.highqaguy.com/)

[Multiple assertions are fine in a unit test | Hacker News](https://news.ycombinator.com/item?id=33479397)
[Stop requiring only one assertion per unit test: Multiple assertions are fine - Stack Overflow](https://stackoverflow.blog/2022/11/03/multiple-assertions-per-test-are-fine/)

[Use console.log() like a pro (2020) | Hacker News](https://news.ycombinator.com/item?id=26779800)
[Use console.log() like a pro - Marko Denic - Web Developer](https://markodenic.com/use-console-log-like-a-pro/)

[The Importance of Testing for Cloud-Based Software Is Heavily Underestimated](https://www.testmonitor.com/blog/the-importance-of-testing-for-cloud-based-software-is-heavily-underestimated)

[Sarah Mei](https://www.devmynd.com/blog/five-factor-testing/)
Five Factor Testing

[Andrew Wulf](http://thecodist.com/article/my_job_as_a_programmer_is_to_make_testers_miserable)
My Job As A Programmer Is To Make Testers Miserable

[Kent C. Dodds](https://kentcdodds.com/blog/write-tests)
(2017) Write tests. Not too many. Mostly integration.

[Jason McCreary](https://jason.pureconcepts.net/2015/01/are-you-a-boy-scout/)
(2015) A look at how the simple practice of "boyscouting" can improve your code.

[Joël Spolsky](https://www.joelonsoftware.com/2000/08/09/the-joel-test-12-steps-to-better-code/)
(2000) The Joel Test: 12 Steps to Better Code

[Dale Myers](https://myers.io/2017/04/04/the-joel-test-for-2017/)
(2017) The Joel Test for 2017

[Dennis Stevens](https://www.leadingagile.com/2013/09/stop-writing-code-cant-yet-test/)
(2013) Stop Writing Code You Can't Yet Test

[Andy Zaidman](https://azaidman.wordpress.com/2017/05/10/is-testing-on-stackoverflow-dead/)
(2017) Is Testing (on StackOverflow) Dead?

[Robert Ecker](https://dev.to/teamcoder/the-problem-with-high-test-coverage-4dh)
(2017) The Problem With High Test Coverage

[Scott Vokes](https://spin.atomicobject.com/2014/09/16/property-based-testing/)
(2014) Property-Based Testing
Testing Assumptions You Don’t Know You’re Making

[Anna Kennedy](http://annaken.github.io/testing-packer-builds-with-serverspec)
(2017) Testing Packer builds with Serverspec

[J. B. Rainsberger](http://blog.jbrains.ca/permalink/what-if-we-forget-to-write-the-tests)
What If We Forget To Write the Tests?

[Michal Charemza](https://charemza.name/blog/posts/methodologies/testing/questions-to-ask-yourself-when-writing-tests/)
(2018) Questions to ask yourself when writing tests : Talk to yourself to make sure your tests help you achieve your aims

[Josh Giller](https://www.stickyminds.com/article/using-decision-tables-clear-well-designed-testing)
(2018) Using Decision Tables for Clear, Well-Designed Testing

[Arthur Hicken](https://www.stickyminds.com/article/shift-left-approach-software-testing)
(2018) The Shift-Left Approach to Software Testing

[Codetester.org](https://codetester.org/)

## testing automation

[Jakub Skałecki](https://rock-it.pl/automatic-code-quality-checks-with-git-hooks/)
(2017) Automatic code quality checks with git hooks

## testing - continuous testing

[Gregg Caines](http://caines.ca/blog/2015/01/29/continuous-testing/)
(2015) Continuous Testing
:star:

## testing - inputs

[There are only four billion floats, so test them all (2014) | Hacker News](https://news.ycombinator.com/item?id=24745563)
[There are Only Four Billion Floats-So Test Them All! | Random ASCII - tech blog of Bruce Dawson](https://randomascii.wordpress.com/2014/01/27/theres-only-four-billion-floatsso-test-them-all/)

[test, [, and [[ (2020) | Hacker News](https://news.ycombinator.com/item?id=38387464)
[test, [, and [[ - Julio Merino (jmmv.dev)](https://jmmv.dev/2020/03/test-bracket.html)

## testing - platforms

[Test your product on a crappy laptop | Hacker News](https://news.ycombinator.com/item?id=29610806)
[Test Your Product on a Crappy Laptop | CSS-Tricks - CSS-Tricks](https://css-tricks.com/test-your-product-on-a-crappy-laptop/)

## testing - users

[Users are Nondeterministic Agents of Chaos • Buttondown](https://buttondown.email/hillelwayne/archive/users-are-nondeterministic-agents-of-chaos)

[Alternatives to "Manual Testing"](https://www.linkedin.com/pulse/alternatives-manual-testing-michael-bolton)

[Ask HN: How to get an accessibility tester job as a blind programmer? | Hacker News](https://news.ycombinator.com/item?id=34986264)
- THE BEST PERSON FOR TESTING IS THE PERSON WHO ACTUALLY USES THE CONSTRAINTS OF BEING A USER

## types of testing

[I have complicated feelings about TDD | Hacker News](https://news.ycombinator.com/item?id=32509268)
[I have complicated feelings about TDD • Buttondown](https://buttondown.email/hillelwayne/archive/i-have-complicated-feelings-about-tdd-8403/)

## typos

[5% of 666 Python repos had comma typo bugs (inc V8, TensorFlow and PyTorch) | Hacker News](https://news.ycombinator.com/item?id=29841560)
[5% of 666 Python repos had comma typos (including Tensorflow, and PyTorch, Sentry, and V8) | by Code Review Doctor | Dev Genius](https://blog.devgenius.io/5-of-666-python-repos-had-comma-typos-including-tensorflow-and-pytorch-sentry-and-v8-7bc3ad9a1bb7)

## unit testing

[Dave Syer](https://spring.io/blog/2007/01/15/unit-testing-with-stubs-and-mocks/)
(2007) Unit Testing with Stubs and Mocks

## website testing - chrome devtools

[My Favorite Chrome Dev Tools Tips and Tricks](https://www.freecodecamp.org/news/awesome-chrome-dev-tools-tips-and-tricks)

## website testing

[Daniel Miessler](https://danielmiessler.com/blog/10-ways-to-test-your-website-performance/)
10 Ways to Test Your Website Performance

## debugging

[Software Debugging | Free Courses | Udacity](https://www.udacity.com/course/software-debugging--cs259)

[The pocket guide to debugging | Hacker News](https://news.ycombinator.com/item?id=34088398)
[New zine: The Pocket Guide to Debugging](https://jvns.ca/blog/2022/12/21/new-zine--the-pocket-guide-to-debugging/)

[Rubber Duck Debugging](https://www.freecodecamp.org/news/rubber-duck-debugging)
[Rubber duck debugging - Wikipedia](https://en.wikipedia.org/wiki/Rubber_duck_debugging)

[How to Use Developer Tools to Debug JavaScript in the Browser](https://www.freecodecamp.org/news/how-to-use-developer-tools-to-debug-javascript-in-the-browser/)

## testing

[PaulWaltersDev/FreeLearningResourcesForSoftwareTesters](https://github.com/PaulWaltersDev/FreeLearningResourcesForSoftwareTesters)
free Online Learning Resources for New and Experienced Software Testers.

## debugging

[What is Debugging? How to Debug Your Code for Beginners](https://www.freecodecamp.org/news/what-is-debugging-how-to-debug-code)

[The Beginner's Guide to Bug Squashing: How to Use Your Debugger and other tools to find and fix bugs](https://www.freecodecamp.org/news/the-beginner-bug-squashing-guide)

## bugs and errors

[Segmentation fault - Wikipedia](https://en.wikipedia.org/wiki/Segmentation_fault)

## code reviews

[How to Make Good Code Reviews Better - Stack Overflow Blog](https://stackoverflow.blog/2019/09/30/how-to-make-good-code-reviews-better)

[How to Do Code Reviews Like a Human (Part One) · mtlynch.io](https://mtlynch.io/human-code-reviews-1/)
(2017) How to Do Code Reviews Like a Human (Part One).
[Part Two](https://mtlynch.io/human-code-reviews-2/)

[GitHub - joho/awesome-code-review: An "Awesome" list of code review resources - articles, papers, tools, etc](https://github.com/joho/awesome-code-review)

[How to do a code review | Hacker News](https://news.ycombinator.com/item?id=20890682)
[How to do a code review | eng-practices](https://google.github.io/eng-practices/review/reviewer/)

[David Mytton](https://blog.serverdensity.com/how-to-do-code-reviews/)
How to do code reviews

[James Wade](https://wade.be/development/2017/10/06/reviewing-code.html)
(2017) What's involved in a code review?

[Kevin London](https://www.kevinlondon.com/2015/05/05/code-review-best-practices.html)
(2015) Code Review Best Practices

## cognitive load

[GitHub - zakirullin/cognitive-load: 🧠 Cognitive Load is what matters](https://github.com/zakirullin/cognitive-load)

## debugging

[Some ways to get better at debugging](https://jvns.ca/blog/2022/08/30/a-way-to-categorize-debugging-skills)
[Julia's Drawings](https://drawings.jvns.ca/)
some drawings about programming and unix world, zines about systems & debugging tools.

[Ostrich algorithm - Wikipedia](https://en.wikipedia.org/wiki/Ostrich_algorithm)

[7 Reasons Why Software Developers Are Prone to Bugs | by Fabio Veronese | Better Programming](https://betterprogramming.pub/7-reasons-why-software-developers-are-prone-to-bugs-bda2fa91e156)

[Debugging tricks in the browser | Hacker News](https://news.ycombinator.com/item?id=38226743)
[67 Weird Debugging Tricks Your Browser Doesn't Want You to Know | Alan Norbauer](https://alan.norbauer.com/articles/browser-debugging-tricks)

## debugging - python

[Python Debugging Handbook - How to Debug Your Python Code](https://www.freecodecamp.org/news/python-debugging-handbook/)

## fuzzing

[What is Fuzzing? Fuzz Testing Explained with Examples](https://www.freecodecamp.org/news/whats-fuzzing-fuzz-testing-explained)

[GitHub - cpuu/awesome-fuzzing: A curated list of awesome Fuzzing(or Fuzz Testing) for software security](https://github.com/cpuu/awesome-fuzzing)

[GitHub - secfigo/Awesome-Fuzzing: A curated list of fuzzing resources ( Books, courses - free and paid, videos, tools, tutorials and vulnerable applications to practice on ) for learning Fuzzing and initial phases of Exploit Development like root cause analysis.](https://github.com/secfigo/Awesome-Fuzzing)

## linting

[GitHub - sindresorhus/awesome-lint: Linter for Awesome lists](https://github.com/sindresorhus/awesome-lint)

[What is linting and how can it save you time?](https://www.freecodecamp.org/news/what-is-linting-and-how-can-it-save-you-time)

[Don't just lint your code - fix it with Prettier](https://www.freecodecamp.org/news/dont-just-lint-your-code-fix-it-with-prettier)
[How to Use Linters and Code Formatters in Your Projects](https://www.freecodecamp.org/news/using-prettier-and-jslint)

## logging

[Using journalctl - The Ultimate Guide To Logging](https://www.loggly.com/ultimate-guide/using-journalctl/)

[What Are Logs in Programming?](https://www.freecodecamp.org/news/what-are-logs-in-programming/)

## progressive enhancement

[GitHub - voorhoede/progressive-enhancement-resources: Resources on Progressive Enhancement. From concept and strategies to feature detection & testing methods. Complete with a list of (code) examples.](https://github.com/voorhoede/progressive-enhancement-resources)

## QA

[GitHub - fityanos/awesome-quality-assurance-roadmap: The starting point of your career as a Software Quality Assurance Engineer | Quality Automation Engineer](https://github.com/fityanos/awesome-quality-assurance-roadmap)

[Quality Assurance Certification | freeCodeCamp.org](https://www.freecodecamp.org/learn/quality-assurance)

## refactoring

[Hugo Matilla/Refactoring-Summary](https://github.com/HugoMatilla/Refactoring-Summary)
Summary of "Refactoring: Improving the Design of Existing Code" by Martin Fowler

[Ronald Jeffries](https://www.ronjeffries.com/xprog/articles/refactoring-not-on-the-backlog/)
(2014) why you shouldn't put refactoring stories on your backlog

## testing automation

[Joe Colantonio](https://www.joecolantonio.com/2017/03/02/automation-testing/)
(2015) Automation Testing Resources & Best Practices

[Aaron Maxwell](http://redsymbol.net/articles/build-test-automation-system/)
Building a Automated Testing/Quality Assurance System

## testing - js react

[React Testing Library Tutorial - How to Write Unit Tests for React Apps](https://www.freecodecamp.org/news/write-unit-tests-using-react-testing-library)

## testing

[Profiling (computer programming) - Wikipedia](https://en.wikipedia.org/wiki/Profiling_(computer_programming))

[GitHub - abhivaikar/howtheytest: A collection of public resources about how software companies test their software](https://github.com/abhivaikar/howtheytest)

[An introduction to @testing-library: Part 1](https://blog.kieranroberts.dev/an-introduction-to-testing-library-part-1)

[What is Software Testing? | Free Courses | Udacity](https://www.udacity.com/course/software-testing--cs258)

[atinfo/awesome-test-automation: A curated list of awesome test automation frameworks, tools, libraries, and software for different programming languages. Sponsored by https://zapple.tech](https://github.com/atinfo/awesome-test-automation)

[GitHub - LukaszLapaj/software-testing-resource-pack: Various files useful for manual testing and test automation etc.](https://github.com/LukaszLapaj/software-testing-resource-pack)

[GitHub - mfaisalkhatri/awesome-learning: Curated lists of awesome learning resources for a Software Test Automation Engineer](https://github.com/mfaisalkhatri/awesome-learning)

[GitHub - TheJambo/awesome-testing: A curated list of testing resources](https://github.com/TheJambo/awesome-testing)

[web-platform-tests documentation - web-platform-tests documentation](https://web-platform-tests.org)

## testing - python

[Testing in Python with Pytest](https://www.freecodecamp.org/news/testing-in-python-with-pytest/)

## TLA+

[Learn TLA+ | Hacker News](https://news.ycombinator.com/item?id=31952643)
[Announcing: Learn TLA+](https://www.hillelwayne.com/post/learntla/)
[TLA+ - Wikipedia](https://en.m.wikipedia.org/wiki/TLA+)
[Learn TLA+ - Learn TLA+](https://www.learntla.com/)

## types of testing

[Why Property Testing Finds Bugs Unit Testing Does Not • Buttondown](https://buttondown.email/hillelwayne/archive/why-property-testing-finds-bugs-unit-testing-does)

[The Difference Between TDD and BDD - Josh Davis](https://joshldavis.com/2013/05/27/difference-between-tdd-and-bdd)

[A Seasoned Tester's Crystal Ball: The Conflated Exploratory Testing](https://visible-quality.blogspot.com/2021/04/the-conflated-exploratory-testing.html)

[Test-Driven Development Tutorial - How to Test Your JavaScript and ReactJS Applications](https://www.freecodecamp.org/news/test-driven-development-tutorial-how-to-test-javascript-and-reactjs-app)

[What is Software Testing? The 10 Most Common Types of Tests Developers Use in Projects](https://www.freecodecamp.org/news/types-of-software-testing)

[An Intro to Metrics Driven Development: What Are Metrics and Why Should You Use Them?](https://www.freecodecamp.org/news/metrics-driven-development)

[Fuzz Testing Is the Best Thing To Happen to Our Application Tests](https://old.reddit.com/r/programming/comments/15tz4pv/fuzz_testing_is_the_best_thing_to_happen_to_our/)

## website testing - chrome devtools

[GitHub - ChromeDevTools/awesome-chrome-devtools: Awesome tooling and resources in the Chrome DevTools & DevTools Protocol ecosystem](https://github.com/ChromeDevTools/awesome-chrome-devtools)

[Flavio Copes](https://flaviocopes.com/chrome-devtools-tips/)
(2018) A list of cool Chrome DevTools Tips and Tricks
