
# Project model theories

## Areas of Operation (AOs)

The system divides out the roles and responsibilities to specific individuals:

1. Designate sub-leaders who are exclusively responsible for specific, non-overlapping domains.
   - The domains can be contiguous (shares a boundary with other sub-leaders) or non-contiguous (not sharing a boundary).
2. That sub-leader is responsible for that domain, and their management performance is defined by their results.
   - If any members fail, that sub-leader is exclusively responsible.

While the system works *very* well for clearly defined goals with clearly-defined actions (e.g., military activities), it's very inflexible to changes and doesn't accommodate the individuals' situations or ideas.

## The Waterfall model

The system step-by-step sequence across 5 phases to carry the project to completion:

1. Requirements - outline the high-level conditions that determine a project's success.
2. Design - create solutions that meet the requirements, often considering backup plans as well.
3. Implementation - pick a design and use [technology](technology.md) to apply it.
4. Verification - test whether the implementation worked.
5. Maintenance - keep testing and [fixing anything that breaks](https://adequate.life/fix/).

It requires specific goals from the very beginning.

- It works on hard deadlines and treats every task as "final".
- Any failures from previous process steps roll into later process tasks.

This system doesn't handle unexpected problems very well.

## Objectives and Key Results (OKR)

The system is designed to achieve clearly-understood purposes:

1. Make an objective that is significant, concrete, and clearly defined.
   - Further, the objectives should inspire everyone working toward them.
   - Avoid a "business as usual" attitude, which means avoiding vague words like "help" and "consult".
2. Each objective should have 3-5 key results, which are measurable either as 0-100% or a numerical value.
   - Aim to measure leading indicators (readily measurable things) instead of lagging indicators (things that measure after a lead time).
   - The target success rate for key results should be 70%, since it encourages competitive goal-making.
   - If the key results are consistently hit at 100%, they should be re-evaluated.
3. If necessary, objectives can be supported by initiatives, which are plans and activities that help move forward the objectives and key results.

One of the downsides of the system is that on the individual level the entire project simply looks like a task list, which makes it very easy for managers to conflate OKRs with performance reviews.

## Agile methodology

The original idea was from [software development](computers-programming.md), where the goals and possible risks aren't always easy to understand.

- The system revises every development stage as the situation changes.

There are 12 principles that bind the concept together:

1. Aim for satisfied customers by giving early and continuous results.
2. Adapt without resistance to whenever any requirements change at any time.
3. Give frequent results (weeks, not months).
4. Every day, make sure the workers and customers are cooperating.
5. Trust individuals who are motivated, and build projects around them.
6. Prioritize face-to-face [communication](people-conversation.md) whenever possible.
7. Measure progress by whether the product actually works.
8. Keep going at a constant pace ("sustainable development").
9. Constantly draw attention to high-quality work and [good design](engineering-design.md).
10. Maximize simplicity, which is the amount of work that doesn't need to be done.
11. Emphasize self-organized teams and expect the best designs, systems, and requirements to come from them.
12. Routinely find ways and adjust things to make the team more effective.

Broadly, the "agile manifesto" emphasizes something that [feels](mind-feelings.md) very human and a little bit [libertarian](politics-conservativeliberal.md):

- Individuals and interactions over processes and tools
- Working software over comprehensive documentation
- Customer collaboration over contract negotiation
- Responding to change over following a plan

The system is designed around smaller-scale iterations:

1. Break the project into subprojects, called iterations or "sprints".
2. At the end of a sprint, everyone reviews the work and makes adjustments for the next sprint.
3. In difficulties come in the middle of a sprint, make smaller subprojects within that sprint with newer, smaller goals.
4. Repeat until complete.

In large organizations that require more centralized planning, agile isn't very useful.

- The issue is that it is focused on people and results more than processes and systems, so it's very difficult to scale.
- Most of the methodologies are so decentralized that most "agile companies" are actually using hybrids of Agile.
- Other variations of Agile like [Scrum](https://www.scrum.org/) or [Lean](https://www.lean.org/WhatsLean/) add more structure to Agile.

### Scrum variations

In Scrum, the team is directed by a Product Owner (PO), who decides what to build next.

- They are essentially the manager, but with the implication that they're doing more communicating than directing.
- The PO is backed by a Scrum Master (SM) who promotes and supports the Scrum system and helps with finding and fixing risks to the project.
- All of this connects to a multi-function Development Team, with each "developer" having no [special role](jobs-specialization.md) and working autonomously toward the designated goals.

Scrum uses three classes of "artifacts":

- The Product Backlog is the collective and compiled set of known tasks about the product.
  - For transparency, this [database](database.md) is visible to the stakeholders.
  - Every item has a description, position, estimated effort required, and approximate value.
  - Higher-ordered items are more detailed and clearer than lower-ordered ones.
  - Every item must be attainable within one sprint.
- The Sprint Backlog is the collection of estimated tasks that can get done in a given sprint.
- The Increment is the collection of tasks in the Sprint Backlog that actually got done.
  - The Definition of Done (DoD) is a *very* specific demarcation with no room for uncertainty (e.g., unit tests, integration tests, [documentation](language-writing-documentation.md), deployed to production).

Scrum goals are sprints, but set by the product owner and then adapted by the team to stay measurable and clear.

- The emphasis is to avoid [stories](stories-why.md) that incorporate vagueness and instead focus on clear goals.

Sprints themselves are divided into a few stages:

1. The Development Team performs Sprint Planning, where they create a Sprint Backlog.
   - This phase may last up to 8 hours to prepare for 4-week sprint.
   - At this time, they fill the Sprint Backlog with as many Product Backlog Items they think they can finish.
   - After communicating for clarification, everyone phrases a Sprint Goal.
   - Once they have a Sprint Goal, they discuss how they'll turn the items into bite-size Increments.
2. Every day, the Development Team meets for a Daily Scrum (or "Stand Up").
   - These meetings may last up to 15 minutes, and detailed discussions come after the Stand Up.
   - It's mostly a focus on what happened the day before, what to do next, any delays, and how to resolve delays.
3. After the sprint, conduct a Sprint Review with the Development Team and customers.
   - The meeting may last up to 4 hours for a 4-week sprint.
   - They meet and discuss the finished Increment and update the Product Backlog.
4. The Development Team performs a Retrospective separately to find possible improvements.
   - This meeting may take up to 3 hours in a 4-week sprint.
   - The meeting is both about [finding problems](https://adequate.life/fix/) and introducing [creative ideas](mind-creativity-how.md).

More info on its defects: [The Scream Guide to Scrum Anti-Patterns](https://www.scribd.com/document/606134290/The-Scream-Guide)

## Holacracy

[The system](https://www.holacracy.org/) is a very flat management structure designed around a constitution made of 5 modules, which everyone is expected to follow:

1. Organizational structure
   - Defines an exact format for roles, responsibilities, and rules.
2. Rules of cooperation
   - Defines what everyone should expect from each other.
   - Clarifies duties involving everyone being transparent with each other, how they process others' requests, and how everyone should prioritize work.
3. Tactical meetings
   - Communicates specific standards for how to run meetings and keep them efficient.
   - Also prevents from anyone dominating the meeting or distractions about unrelated discussions.
4. Distributed authority
   - Speeds tasks up by granting partial autonomy without needing prior approval.
   - Creates constraints to prevent abuse of that autonomy.
5. Decentralized governance process
   - Creates a process for making improvements or changes within the scope of each person's work.
   - Defines constraints which prevent anyone from abusing the governance process.

The system gives everyone power to self-manage, which is a very effective system if everyone is trustworthy to self-direct.

- If everyone depends heavily on each other, though, it can cause severe breakdowns in communications and activities and be *worse* than micromanagement.

## Project Management Triangle

Every single project will only permit 2 of 3 variables:

1. Cost (i.e., cheap)
2. Time (i.e., fast)
3. Quality (i.e., good)

Every single effort to add the third will sacrifice one of the others.

It's entirely possible to have all 3 of them in the following:

1. Average-priced
2. Within an accommodating deadline
3. Good enough

When this calculates for goods instead of services, the "fast" component is within the required research to attain the goods.

There is also an [insurance](money-insurance-how.md) calculation that runs similarly:

1. Low premium and deductible
2. High limits
3. Thoroughly covers things
