
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
