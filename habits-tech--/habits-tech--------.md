
### Slow programming principles

* No broken window. A repo should always be in a clean and working state, i.e the last commit should always build successfully.
* If you broke it, take ownership for the repair. If you break something, you are responsible of the situation, fix it (it's ok to ask for help).
* Avoid branching/batching your changes | Be careful what you batch. Changes and version bumps should be integrated continuously, not all at once.
* Don't hide your work, branch instead, and get it reviewed before creating a PR / merging it.
* If possible, don't branch, work on trunk/main. Branching/Feature flags can help.
* Use Peer code review, if possible pre-commit reviews. Peer code review is a key element in building a robust and egoless engineering culture of collaborative problem-solving ([source](https://semaphoreci.com/blog/cicd-pipeline))
* If you change the principles/systems/processess, do it incrementally. Developer productivity matters a lot. Minimize friction. e.g don't do a migration of all CI/CD Ecosystem in a way that breaks everything for a while. Do it step by step, phase the changes. Make it possible to rollback easily to previous working state.
* Quality first | Quality is always right. If you’re doing CI and for some reason the integration fails, that means the broken build becomes the highest priority to fix before continuing to add more features. System quality—not just velocity—is important. CI works in three simple stages: push, test, and fix. But despite this simplicity, CI might become challenging if only a few members of the team practice it. Consequently, CI also requires a change in culture and support from management. [source](https://stackify.com/what-is-cicd-whats-important-and-how-to-get-it-right/)
  * There is never enough time to do it right yet we find time to do it again and again. Jack Bergman?
* Refactoring can only truly begin once you've actually learned what a piece of code or some data structure did, the unique properties for which they were written or chosen. Anything else is setting yourself up for failure. [source](https://ferd.ca/lessons-learned-while-working-on-large-scale-server-software.html)
* It also means that when building systems, you should not assume that operators will do things correctly. Expect failure from people. Try to think about tools you can give them to undo their mistakes, because they will happen sooner or later. Have some dread. Be understanding. Know things won't be perfect. [source](https://ferd.ca/lessons-learned-while-working-on-large-scale-server-software.html)
* Study your tools, see how you work, understand how you can improve it. Don't rush. Before you run, you have to learn to walk. 
  * Whether you’re getting a lot of satisfaction from being busy or just feeling exasperated, don’t forget to occasionally stop and ask yourself: Is this the best use of time?
  * Improve systems : Improving systems helps remove busywork from an employee’s day, but it also makes things easier for the customer. 
  * See also: [Ref : How Being Busy Kills Productivity](https://www.hellosign.com/blog/busy-kills-productivity) on how doing less can help you be more productive
  * Focus on results; not time : Time tracking is unavoidable in some instances, but rather than the rule by which companies operate, it should be used as a secondary metric to the results they achieve. Rather than give an employee a 2-hour window to do a job, have her do it right the first time (bonus points for documenting the process), then review and adjust your future plans based on time tracking data.
* Do one thing at a time. Only one item under your name in the WIP. The rest will wait. You cannot fix all things.
* Test the crap out of everything you do before telling anyone you are "finished". See also [Ref : Being a slow programmer](https://shansvex.wordpress.com/2013/12/03/being-a-slow-programmer/)
* Use right tools for the job (email != todo list, PR and commits != code documentation, Jenkins != long term storage for releases/versions/build info/state of quality of your code)
* Love what you have. Using boring technology. Don't get distracted too often with shiny tools that reinvent the wheel.
* Write less code, read more than you write. Read more tips, manuals, blogs, articles, watch presentations and listen to podcasts about your programming craft. Learn from others prior to writing bugs. As with culture and and knowledge, you are the books you read, the films you watch, the music you listen to, the people you spend time with, the conversations you engage in. Choose wisely what you feed your mind with, and it's true with code as well. See also [Ref : Being a slow programmer](https://shansvex.wordpress.com/2013/12/03/being-a-slow-programmer/) and [Ref : Learn to Read the Source, Luke](https://blog.codinghorror.com/learn-to-read-the-source-luke/)
* Learn how to write clean code, and repeat. So when you will have to rush, you will not forget to do your work right, and you will naturally provide more quality work. Also you will tend to detect issues earlier before they hit production, i.e during reviews, and writing better code will lead the whole team in getting a better codebase you can all be proud of, which mean work will become more agreeable. 
* Do your research, don't always rush in coding or in reinventing the wheel. You will learn a lot through research.
* Don't react yet. Take a little time before taking action / reacting to a task/request/message. It allows you to think more about your answer / action. Also, ask yourself if you really need to take action now for this task, or if it can wait later in the day/week. Check if you're not giving the task more focus/consideration than it deserves.
  * Wait before jumping immediately on every opportunity/request/problem. Don’t touch it / don’t (re)act too soon
  * :star: Respond rather than react
  * Before you write any code, think first about what problem this is solving and for whom. See also: [Ref : Think first about what problem this is solving and for whom](https://letterstoanewdeveloper.com/2021/01/18/think-first-about-what-problem-this-is-solving-and-for-whom/)
  * The faster you react, the less you think. Not always, but often. [Ref : Give it five minutes](https://signalvnoise.com/posts/3124-give-it-five-minutes) 
  * See also: [Ref : How Being Busy Kills Productivity](https://www.hellosign.com/blog/busy-kills-productivity) on how doing less can help you be more productive
* Reuse existing code. GitHub is your friend.
* Discipline / Consistency beat motivation and quality. 
* You don't want heroes, but you might benefit from experts / excellents colleagues / colleagues & managers that provide support and insights and who do not let you take everyting on your plate.
* Simplify. Become a minimalist. 
* Don't be overconfident | the fallacy of skipping the planning stage. Some tasks look simple at first glance, but it can hide some challenges. Take the time needed to run your analysis and estimate the effort after you have checked all possible impacts you could check. Overestimating is one thing, but underestimating the effort and challenge can really lead to getting cascade issues and mistakes that would add a lot of pressure on every team and lead then to rushing even more and causing even bigger mistakes. See also [Ref : Skipping the planning stage](https://www.caines.ca/blog/2009/12/13/code-slower/)
* Writing classes and functions that do a lot. 
* Be helpful not harmful, fix things and care more about your impact.  You have a big responsibility on your hands, and you should take it seriously. The world needs as much care and conscience as we can muster. Defend your users against anti-patterns and shady business practices. Raise your hand and object to harmful design ideas. Call out bad stuff when you see it. Thoughtfully reflect on what you’re sending out into the world every day. See also: [Ref : Move Slowly and Fix Things](https://m.signalvnoise.com/move-slowly-and-fix-things/)
* Comment.
  * More so than all other tools (issue tracker, code management system, etc.) comments in code have the greatest chance of still being around and easily searchable if they haven't been deleted. See also: [Ref : The case for comments in code](https://notes.eatonphil.com/the-case-for-comments-in-code.html)
  * Code can’t self-document if it isn’t there. If you decide to not write some code and don’t leave a comment explaining why, there will be nothing left to explain what you were thinking! Add comments that explain why the code is doing what it is doing, or is structured the way that it is structured. See also: [Ref : How to write readable code](https://jeremymikkola.com/posts/2021_02_02_how_to_write_readable_code.html)
* When you're done with your commit and push, just double check what you have just done. Sometimes issues or possible improvements appear obvious only when the work is already pushed. Next time, slow down and double check before pushing ;-) 
* Make your app fail fast in case of error. Ignoring errors will have side effects and can cause even more harm than if you just had the app crashing on first error.
* Focus on simplicity. The answer is always there. [source](https://blog.strategicedge.co.uk/2013/03/tidy-up-as-you-go-along-be-it-cooking-diy-or-selling-your-software-solution-remember-the-small-stuff-as-it-is-big-stuf.html)
* Slow is steady. Steady is smooth. Smooth is fast. [Source](https://twitter.com/DanielMiessler/status/1406038903878868992)

### Slow programming Healthy tips / helpers
* Disconnect & Focus. Value your time, use it to focus. Put lot of non-meeting blocks in your agenda. 
* Stay positive. Focus on what is doing ok, what you have accomplished. Focus your brain attention more often on something that is stress free.
* Limit your coffee intake. 
  * Drinking caffeine triggers the release of adrenaline. Adrenaline is the source of the “fight-or-flight” response, a survival mechanism that forces you to stand up and fight or run for the hills when faced with a threat. The fight-or-flight mechanism sidesteps rational thinking in favor of a faster response. This is great when a bear is chasing you, but not so great when you’re responding to a curt email. [source](https://www.linkedin.com/pulse/20140805002649-50578967-how-successful-people-stay-calm/)
  * Less caffeine. More hot water and sliced ginger. [source](https://blog.strategicedge.co.uk/2013/03/tidy-up-as-you-go-along-be-it-cooking-diy-or-selling-your-software-solution-remember-the-small-stuff-as-it-is-big-stuf.html)
* Get enough sleep. 
  * When you sleep, your brain literally recharges, shuffling through the day’s memories and storing or discarding them (which causes dreams), so that you wake up alert and clear-headed. Your self-control, attention, and memory are all reduced when you don’t get enough—or the right kind—of sleep. Sleep deprivation raises stress hormone levels on its own, even without a stressor present. Stressful projects often make you feel as if you have no time to sleep, but taking the time to get a decent night’s sleep is often the one thing keeping you from getting things under control. [source](https://www.linkedin.com/pulse/20140805002649-50578967-how-successful-people-stay-calm/)
  * The alarm clock is for back-up. Not wake up: get enough sleep. [source](https://blog.strategicedge.co.uk/2013/03/tidy-up-as-you-go-along-be-it-cooking-diy-or-selling-your-software-solution-remember-the-small-stuff-as-it-is-big-stuf.html)
* Look for help | Use your support system. It’s tempting, yet entirely ineffective, to attempt tackling everything by yourself. To be calm and productive, you need to recognize your weaknesses and ask for help when you need it. This means tapping into your support system when a situation is challenging enough for you to feel overwhelmed. Everyone has someone at work and/or outside work who is on their team, rooting for them, and ready to help them get the best from a difficult situation. Identify these individuals in your life and make an effort to seek their insight and assistance when you need it. Something as simple as talking about your worries will provide an outlet for your anxiety and stress and supply you with a new perspective on the situation. Most of the time, other people can see a solution that you can’t because they are not as emotionally invested in the situation. Asking for help will mitigate your stress and strengthen your relationships with those you rely upon. [source](https://www.linkedin.com/pulse/20140805002649-50578967-how-successful-people-stay-calm/)
* Breathe. The practice of being in the moment with your breathing will begin to train your brain to focus solely on the task at hand and get the stress monkey off your back. When you’re feeling stressed, take a couple of minutes to focus on your breathing. Close the door, put away all other distractions, and just sit in a chair and breathe. The goal is to spend the entire time focused only on your breathing, which will prevent your mind from wandering. Think about how it feels to breathe in and out. This sounds simple, but it’s hard to do for more than a minute or two. It’s all right if you get sidetracked by another thought; this is sure to happen at the beginning, and you just need to bring your focus back to your breathing. If staying focused on your breathing proves to be a real struggle, try counting each breath in and out until you get to 20, and then start again from 1. Don’t worry if you lose count; you can always just start over. [source](https://www.linkedin.com/pulse/20140805002649-50578967-how-successful-people-stay-calm/)
* Drink / eat well.  
  * Don’t forget to drink water, get sunlight, and that we are basically a house plant with complicated feelings. [source](https://twitter.com/TheWeirdWorld/status/930155807651528706)
  * Often when we think we are hungry we are simply thirsty. Drink water first. [source](https://blog.strategicedge.co.uk/2013/03/tidy-up-as-you-go-along-be-it-cooking-diy-or-selling-your-software-solution-remember-the-small-stuff-as-it-is-big-stuf.html)
  * Drink decent tea and coffee. Do the simple pleasures properly. [source](https://blog.strategicedge.co.uk/2013/03/tidy-up-as-you-go-along-be-it-cooking-diy-or-selling-your-software-solution-remember-the-small-stuff-as-it-is-big-stuf.html)
  * Eat slowly
* Let things blow up from time to time, you're not your work, don't feel you are not responsible for everything within your employer's company, and your employer is more resilient than you think.
* Check your posture. It will reflect how you are treating your body. [source](https://blog.strategicedge.co.uk/2013/03/tidy-up-as-you-go-along-be-it-cooking-diy-or-selling-your-software-solution-remember-the-small-stuff-as-it-is-big-stuf.html)
* [Unix Sheikh](https://www.unixsheikh.com/about.html)
    software engineering principles
> * Simplicity: The system should always be as simple and small as possible. When software projects grow, so do errors and bugs. Techniques such as line-by-line inspection of software, relevant unit testing, and physical examination of hardware that implements protection mechanisms are great. For such techniques to be successful a small and simple design is essential. This is sometimes described as the KISS principle and YAGNI.
> * Least privilege: Each user and program should operate using the fewest privileges possible.
> * Open design: In order for a system to be secure it must never depend on attacker ignorance. Instead the design should be based upon technology that depend upon public scrutiny - whenever possible.
> * Complete mediation: Every access attempt must be checked and validated.
> * Easy to use: The human interface must be as easy and intuitive to use as possible. Easy and simple is always better than smart and fancy. Simple user testing is a great way to get valuable feedback.
> * Usability: Well known usability standards should be met if required.
> * Discrimination: User discrimination is never good. User discrimination is when an application only works for a very limited amount of systems, like when a website only works with JavaScript enabled even though it doesn't provide any functionality that really requires JavaScript.
> * Documentation: Lacking or inadequate documentation is a bug. Everything needs to be adequately documented from the very beginning, it is an integrate part of software development. I strongly abhor poor or lacking documentation.


[Jeremy Mikkola](https://jeremymikkola.com/posts/2021_02_02_how_to_write_readable_code.html)
(2021) How to write readable code
> * Prioritize Clarity : The first step to writing clear code is to make it a priority.
> * Develop a sense for clarity : requires knowing what clear code looks like.
> * Edit : Reading back over what you just wrote will help give ideas for how to improve it.
> * Start by explaining : start by explaining what needs to be done as though you are telling it to another person (or rubber duck). Write it down. Take that explanation and transform it into code.
> * Comments : Code can’t self-document if it isn’t there. If you decide to not write some code and don’t leave a comment explaining why, there will be nothing left to explain what you were thinking!
> * Don’t mix levels : Mixing levels of abstraction makes the reader jump between thinking about what is being done and how it is implemented.
> * Break out functions - :duck: self-comment here : It's true to some extent, but breaking a code in too many functions can also force jumping a lot between code locations. So I would say it depends on the semantic and scope distance between those functions. 
> * Don’t break out functions : DRY starts to go too far when two functions that happen to share a handful of lines become a target for deduplication. The test for whether some pieces of code should be deduplicated is simple: would anything bad happen if one was changed without also changing the other? If the answer is yes, then make a single source of truth for it. If not, consider leaving it alone. - :duck: self-comment : exactly... what I just wrote above :-) 
> * Avoid configurable functions : Prefer many functions to a few, configurable functions, i.e It’s much better to have multiple functions, each of which does just one thing.
> * Don’t prematurely optimize

## being productive - slow programming

[Jeffrey Ventrella](https://ventrellathing.wordpress.com/2013/06/18/the-case-for-slow-programming/)
(2013) The Case for Slow Programming
“Slow down, son. You’ll get the job done faster.”

[Esther Schindler](https://blog.newrelic.com/2016/02/22/8-ways-become-a-better-coder/)
(2016) 8 Ways to Become a Better Coder
> “The code works” isn’t where you stop; it’s where you start

[Umer Mansoor](https://codeahoy.com/2016/06/03/write-less-code/)
(2016) Write Less Code

[Shaun Finglas](https://blog.shaunfinglas.co.uk/2015/09/waste-write-less-code.html)
(2015) Waste: Write Less Code

[Alicia Liu](https://medium.com/counter-intuition/go-slow-to-go-fast-part-1-you-a4974ceb8a7c)
(2018) Go Slow to Go Fast
[Part 1: You](https://medium.com/counter-intuition/go-slow-to-go-fast-part-1-you-a4974ceb8a7c)
[Part 2: Team](https://medium.com/counter-intuition/go-slow-to-go-fast-part-2-team-e793bb0d658a)
[Part 3: World](https://medium.com/counter-intuition/go-slow-to-go-fast-part-3-world-efb76c4de220)

[Jonas Downey](https://m.signalvnoise.com/move-slowly-and-fix-things-e5a560fd928b)
(2017) Move Slowly and Fix Things
Ruminations on the heavy weight of software design

[Logan Mayville](https://www.hellosign.com/blog/busy-kills-productivity)
(2018) How Being Busy Kills Productivity
How doing less can help you be more productive
> * Focus on results; not time : Time tracking is unavoidable in some instances, but rather than the rule by which companies operate, it should be used as a secondary metric to the results they achieve. Rather than give an employee a 2-hour window to do a job, have her do it right the first time (bonus points for documenting the process), then review and adjust your future plans based on time tracking data.
> * Improve systems : Improving systems helps remove busywork from an employee’s day, but it also makes things easier for the customer. 
> * Whether you’re getting a lot of satisfaction from being busy or just feeling exasperated, don’t forget to occasionally stop and ask yourself: Is this the best use of time?
How doing less can help you be more productive
> * Focus on a single strategy
> * Focus on results; not time
> * Improve systems

[Calm Tech](https://calmtech.com/)
Principles of Calm Technology

[Tanmay Vora](http://qaspire.com/2012/09/21/a-gentle-friday-reminder-go-slow/)
(2012) A Gentle Friday Reminder: Go Slow
> * You are moving too fast. Overwhelmed with everything, good or bad, happening around.
> * Life is too short (really) to zoom past it.
> * People who survive (and grow) are the ones who stay in the moment, concentrate and strive to deliver their best.
> * Quality never comes from rushing through things.
> * Just because you can do so many things doesn’t mean you should attempt all of them.
> * Rushing too fast through these is a risk, it is a killer. You never savor the moment, be in the present and enjoy the process. You end up ‘doing’ so much that there is no time to ‘ruminate’

[Slow Programming](https://slowprogramming.com/)
Programming has become a pursuit of profit over personal knowledge. The craft of programming has developed into a rapid rush to the finish line via bootcamps and brief tutorials.

[Nikol](https://pro-wp.in.ua/stop-a-moment-slow-programming-is-a-trend-for-tired-developers/)
(2023) Stop a moment. Slow programming is a trend for tired developers

[George Gritsouk](https://gggritso.com/legacy-code)
(2016) Legacy Code
The noblest pursuit of our weekdays
slow programming

[Itamar Turner-Trauring](https://codewithoutrules.com/2016/06/26/code-faster/)
(2016) Code faster by typing less
