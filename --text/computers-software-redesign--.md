
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
