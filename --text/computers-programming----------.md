
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
