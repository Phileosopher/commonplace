
Because technology and software change around so frequently, programs have to change proportionally to the number of places that they're "implemented".

Thus, features require maintenance, and require constant rework.

On the granular level, software development is about reliable [version control](computers-software-versionctrl.md), but good development requires [*constant* direct feedback](people-customerservice.md) from the users. This is harder than it sounds because the users often don't know what they want.

## Optimizing

Optimizing software can be boring or unpleasant for software developers:

- They're essentially working over the same thing as before, which might be boring.
- It's not uncommon for many of them to have unspecified [PTSD](hardship-ptsd.md) about the *last* effort they took to simply get the software to work correctly in the first place.
- The original developer is long-gone, and the other developers are terrified to touch it out of fear of possibly breaking it.

However, it usually makes sense to have other people improve the creator's original work:

- They don't have the [bias](mind-bias.md) of having worked on it, meaning they're more fine with destroying and rebuilding huge portions of the codebase.
- Their ability to get their mind around the [algorithms](computers-programming-algorithms.md) and [flow of data](data-structures.md) is a new experience to them altogether (and therefore enjoyable).

## Feature bloat

The best feature in computers, no matter what, is speed. The faster the computer performs tasks, the more efficiently it's using resources, and the more burden that task can take on when it's part of a much larger system.

Every feature that accommodates different situations adds to the complexity of the program. Imagine, for example, a non-software comparison with a screwdriver:

1. At the onset, the screwdriver is a simple tip, shaft, and handle.
2. Since the tip may slip off from the screw, a later installment could add a feature that protects the sides from slipping.
3. This anti-slip feature is sometimes hard to use, so the next installment will make a retractable button for it, along with a telescoping feature.
4. Since it's hard to torque a screw sometimes, it's a convenient addition to add a motorized torque feature, and all the extra features will require a larger handle to hold them.
5. That larger handle will need to be either longer or wider, and there will be multiple "forks" for the ideal handle, with a large contention over which one is better.
6. On the trunk version, detachable tips add unlimited portability, including users able to insert their own tips, creating even more complexity.

In software, [the UI](engineering-design.md) can hide away most features, so there are nowhere *near* as many constraints to adding features as most other engineering. This is good because it allows the core function of the software to be relatively unaffected, and bad because the list of features can be theoretically endless.

The more time software developers work on features, the less they're working on the core function of the software.

One of the most significant sources of slowdown and [cybersecurity risks](computers-cysec.md) comes from using an off-the-shelf [framework](computers-programming-basics.md) for an application:

- That framework will likely be sufficient (even to easily [scale](computers-distsys-enterprise.md)), but over time the developers of *that* framework can often add arbitrary features that will severely slow it down (and therefore the dependent project).
- Even without a framework, a sufficiently complex framework-free application will have an ad-hoc, [informally-specified](language-writing-documentation-cs.md), [bug-ridden](computers-software-redesign.md), slow implementation of half of a framework.
- With a sufficiently talented team, the half-framework will outperform the off-the-shelf framework, but only if they can keep things simple enough for new developers to get up-to-speed on it.

In competing software in the same space, one software will be invariably faster, while another one will have many features, and a third one will have some features but won't be as robust as the second one. It can be amusing to see them borrow features off each other *many* years after it had been a "killer feature" of the other software.

## Decay

Over time, a software can develop a strong "user base", which means the software developers will have a clearer interest in developing the software further. This usually creates a [marketing](marketing.md) incentive to improve user retention by adding more features, even when *very* few users requested that feature.

However, more features create more avenues of maintenance. The [nature of specialization](jobs-specialization.md) means that the software will slowly advance to several possible states:

1. The software is finished. Outside of [security patches](computers-cysec.md) or [OS updates](computers-os.md), there is no further need to work on the software.
2. The software isn't as good as it used to be. All the features have bogged it down, or some features interfere with the software's core use.
3. The software is still very good, but it has been acquired by developers who don't care to maintain it. It doesn't receive critical updates and becomes unsafe or unwieldy compared to alternatives.

Except for the first case, the software will soon find itself among other, better software programs:

- Some will be as simple (or simpler) as earlier versions of that software.
- Some do precisely the same thing, but are [open-source](legal-ip-floss.md) or disable telemetry.
- There will be an entirely new implementation that carries the spirit of the original software.

Even then, [software trends](trends.md) move so fast that it doesn't really matter. If the developer made money on it before it became obsolete, it was good enough.

## End-of-life

Often, a software will become "deprecated":

- If the lead developer [passes on](legacy.md), but [with a succession plan](hardship-death.md), nothing in the software itself will change, but the brilliant mind that [created that software](computers-software-design.md) will be difficult to replace.
- If the lead developer passes on, but *without* a succession plan, the software may be inaccessible. In that situation, there may be a need for another developer to reinvent the entire codebase to serve the community that needs it.
- If a superior software came along that was designed more efficiently or with more features, the developer may release it as [open-source](legal-ip-floss.md). From there, other developers will likely borrow parts of the code for *their* future projects.

Sometimes, however, a [large company](computers-distsys-enterprise.md) will buy out well-maintained software. From that point, the software will likely suffer one of several fates:

- In the pursuit of profit, the software will be modified to [track more data](faang.md) or will develop a [freemium business model](legal-ip-floss.md).
- If the software was [open-source](legal-ip-floss.md), the developer or company will release a closed-source version of it, and another developer will subsequently [fork the software](computers-software-versionctrl.md) as another open-source implementation.
- The software will stay open-source, and will become the vehicle for other for-profit software the company was using.
