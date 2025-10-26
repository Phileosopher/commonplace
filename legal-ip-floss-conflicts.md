
# Open-source conflicts

## Inter-community conflicts

If it's public-facing, open-source software developers will get plenty of unwarranted hate for what they do, especially if their software becomes popular. Some developers [enjoy some levity with it](https://notepad-plus-plus.org/news/v843-unhappy-users-edition/), but there are often many toxic people who send unpleasant messages.

While the codebase is completely public and open, open-source [version control](politics-systems.md) forms into several competing views:

1. Anyone is free to contribute or fork whatever they want, and the original code owners will support all the variants.
   - It's a type of [communism](politics-systems.md), which creates an organic and varied form of growth, but is wildly unpredictable.
   - In terms of quality, it's often *very* difficult for fully open software to compete with proprietary software.
2. Anyone is free to contribute or fork whatever they want, but the original code owners possess a "[benevolent dictatorship](politics-systems.md)" through the approval/denial of [pull requests](computers-software-versionctrl.md).
   - This is a much more hands-on form of [management](groups-large.md) (and can sometimes become highly controversial).
   - Centralized control by a few developers guarantees a more effective software, and the software is often *better* than any proprietary software could be.
   - However, there's a *much* higher likelihood of the code forking off due to a petty dispute over a mostly irrelevant feature.
3. An "open-core" concept, with all the features coming as plugins or extensions.
   - The final software is effectively a proprietary system, with most of the work maintaining the code performed by the organization's members.
   - This has been proven as a successful [business model](entrepreneur-2_idea-cs.md) (e.g., Google's Android OS, most Apache software) that allows complete freedom while also giving control to the original developers.
   - It's not uncommon for forks without that [organization's](groups-large.md) involvement, which may mean competition or dramatic permutations from the original software.
4. People are *not* free to contribute or fork whatever they want (closed-contribution), though the software is still open-source.
   - This is basically #2, but with more constraints, since too many pull requests can cause burnout for developers.
   - [Features](computers-software-maintenance.md) require extra work to implement, and then require more work to maintain.
   - Usually, the pull requests are constrained to *only* [bug fixes](computers-software-redesign.md).

Open-source projects are *not* exempt from politics and [social decay](mgmt-badsystems.md).

- Many open-source developers feel entitled:
  - They may feel their contributions deserve [recognition](image.md), they deserve payment, or their pull requests should be automatically approved from [what they've done in the past](power-influence.md).
- The scope of authority in an open-source project comes through how much contribution someone invests into it, and an open-source community has the same [group hierarchy](groups-small.md) as any other organization.
  - They often must invest time to follow the project's mailing list or pull requests, and typically must follow the group's [social norms](people-rules.md).
- Every open-source project goes through the same predictable [trend](trends.md) of growth, stagnation, then decay, which will eventually spawn a [defective culture](mgmt-badsystems.md) around it.
  - Sometimes, a long-standing and popular open software may be significantly inferior to another open-source product, but can screw up the [reputation](image.md) of the *entire* open-source community by dominating everyone's attention. This entire situation can make proprietary choices prevail for longer.
- It's not uncommon for large organizations running on open-source software to *not* credit specific developers who [find bugs](computers-software-redesign.md) in the code, often with them responding rudely to the developer before publicizing they fixed the bug.
- [Technical idiots](https://gainedin.site/idiot/) who are *not* aware of how open-source works may demand answers or fixes from open-source developers.
  - Ironically, if they *do* perform without compensation, this can [set a precedent](people-contracts.md) that frames a type of business contract, though it's not typically enforced (since it's [too unethical](morality.md) for any reasonable judge to rule in the favor of the requestor).
  - Some of the more [contract-savvy](people-contracts.md) developers will ask them to arrange a business arrangement first before acting more promptly.
  - Every software developer must learn [healthy boundaries](people-boundaries.md) to avoid the exploit and abuse from ignorant [managers](mgmt-1_why.md).
- If a company offers both a proprietary and open-source version, and the proprietary version makes more money, they may completely disregard the open-source version.
- If a developer significant to a project ever starts committing implementations of their current [political views](politics-conservativeliberal.md) into the project, political fashions can overtake projects and corrupt them away from their simple purpose.
- Since the developers have to [pay their bills](money-3_budget.md), they need *some* sort of funding. This may connect to the software itself (see above), or the project may have to run like a [not-for-profit](mgmt-npo.md).

However, the beauty of *any* open-source project is that absolutely anyone can fork the original code and create something new with it, thereby building their own software inspired by the original software.

Sometimes, irrespective of the relationship with the original creator, it may be wise to fork the software.

- To expand on an open-source project with very few recent updates, fork the project and start your own, or find other people who have made a more recent project that does effectively the same thing.
- If the software is used for anything sensitive, it needs attention on it to maintain [security patches](computers-cysec-compliance.md).
- The licensing may bind you into constraints you may not want (e.g., can't sell the software without also releasing the code), and a fork may provide opportunities to change that.
- If the software is used for particularly high-attention things (e.g., [illegal activities](computers-distsys-torrent.md)), it may make sense to clone a copy of the software to prevent complete removal of the software for the public to use.

## Legal conflicts

Whether a license was open-source or closed-source can often create unforeseen consequences *much* later:

- Most [immoral actions by Big Tech](faang.md) are driven by closed-source software that was often *not* released as open-source before they started abusing their power.
- [Linksys accidentally released the WRT54G model under GPL, and undoing it later created a PR disaster](https://tedium.co/2021/01/13/linksys-wrt54g-router-history/).
- John Carmack, the developer of many famous id Software [games](computers-software-gamedev.md), [regrets releasing the source code under GPL instead of under BSD](https://web.archive.org/web/20210706044408/https://twitter.com/ID_AA_Carmack/status/1412271091393994754).

[Many, many efforts have been made](faang.md) to subvert the nature of open-source, but the community typically [pushes back](https://trendless.tech/faang-response/) with intelligent solutions that make the software more accessible.

- On that specific front, there is a *lot* of resentment by Big Tech against the open-source community.
- There's also quite a bit of fear in the open-source community over *any* proprietary over-reach.

Many, *many* discussions revolve around intellectual property and the legal battles in over who gets to use software, and a few poorly decided judicial rulings are enough to *dramatically* alter the state of the open-source industry.

- Sometimes, a software developer will release their code as open-source while they're an employee, then their company will try to claim intellectual property rights over it.

However, the fight against open-source is a losing battle.

- [It's a human universal](humanity-universals.md) that secrets are difficult to keep. Eventually, the methods and implementation will become public knowledge, then someone will create an open standard that basically does the same thing but in a different way. Suing everyone is only financially viable for a season.
- Another part is that developers are often more motivated by [ideals](values.md) than profit. They'll tirelessly work on an open-source project [antagonistically](https://trendless.tech/faang-response/) or simply [for fun](fun-cs.md), and a geek locked-away on a project can create *gigantic* changes that otherwise wouldn't happen if it was driven strictly by money.
- Open software and standards mean *any* developer or company can build on it (especially when the license allows them to create closed-source products). There's almost no business reason to reinvent and rebuild what has already been built, especially if it's good-enough.
- Most closed-source developers and companies can fight off the inevitable open-sourcing by releasing it for free.

The [trend](trends.md) for free software, as of 2023, is a bit complex:

- Open-source software terms are definitely enforceable, and failure to honor them can lead to a lawsuit.
- GPL code has effectively been labeled as a [contract-based matter](people-contracts.md), *not* over [intellectual property](legal-ip.md). It doesn't make much intuitive sense, but it [gives lawyers more work](legal-doctrines.md) and means the payment for damages is generally higher (i.e., [California district court](https://web.archive.org/web/20200719095524/https://www.theregister.com/2017/05/13/gnu_gpl_enforceable_contract/)).
- There are also movements that imply that *any* [decompilation](computers-compilers.md) of software might be legal, if only for the intention of [fixing a bug](computers-software-redesign.md). Nothing says the [core logic](computers-alu.md) can't be reproduced, either, even if the software isn't outright copied (i.e., [EU court ruling](https://curia.europa.eu/juris/document/document.jsf?text=&docid=247056&pageIndex=0&doclang=en&mode=req&dir=&occ=first&part=1)).
- Copying your software's [API outputs](computers-programming.md) to make it interoperable with another, more popular software *might* be legal, but will be somewhat of an uphill battle to wrestle over the dispute (i.e., [Google vs. Oracle's Java ruling](https://www.supremecourt.gov/opinions/20pdf/18-956_d18f.pdf)).
- Calling software open-source when it's *not* open-source is considered false advertising.

The reality about software developers is many of them (especially anyone who wants to work on an open-source project) does *not* care as much about money as they do about their [specialization](jobs-specialization.md) inside computers.

- Legal battles are unpleasant, and it's very difficult to visualize anyone who [engages in lawfare](legal-safety.md) against software developers that make software free to the public as anything *but* an [antagonistic](stories.md) or [evil](morality-evil.md) entity.
- The [win/win solution](people-5_conflicts.md) is to give substantial wealth to those developers: if a tool generated a few hundred million dollars for a company, give a few million to that developer.
- However, barring that, some software-based lawyers [near the end of their life](legacy.md) would be *thrilled* to lend their time to winning legal battles that promote free software.
