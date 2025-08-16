
# FLOSS licensing explained

While [intellectual property](legal-ip.md) *generally* sits on a spectrum of usage (e.g., free to consume but not distribute, free to distribute if it's also free), software has its complexities regarding free use of code.

The broad term for the entire domain was FOSS (Free and Open-Source Software), but has more particularly used the acronym FLOSS (Free/Libre Open-Source Software).

In many ways, developers are passively taking a type of [political stance](power-types.md) based on their adoption of open-source licensing, and users are passively endorsing those politics by [consenting](contracts.md) to use that software.

The scope of [artistic expression](mind-creativity.md) often shines much more in open-source than closed-source.

- Unless they're maintaining a critical piece of software infrastructure, developers are free to build, play, and abandon whatever they feel like.
- These creations may even include *massive* projects such as [games](computers-software-gamedev.md), or [compilers](computers-compilers.md), [machine learning](computers-ai-ml.md), or entire [operating systems](computers-os.md).

## Copyright vs. Software

When you're writing, that information [is automatically copyrighted as you write it](legal-ip.md). The same goes for computer software, even though a computer will certainly treat code completely differently than a person with a book. This means that you reserve the right to prosecute over *any* misuse of your works, with an exception for fair use that allows people to copy content for educational purposes or parody.

Computer code is complicated is *technically* written language, so it's technically bound by copyright law. Copyright is implicit (i.e., you don't have to opt into it), but it's an [arcane mess](legal-ip.md), especially with the complexities of how software code is legally interpreted.

There are several non-copyright ways to release non-code text (including [technical documentation](language-writing-documentation.md)) with a more free license:

- [Creative Commons](https://creativecommons.org/) is the standard license that most non-computer people may be familiar with, with [Creative Commons' CC0](https://creativecommons.org/share-your-work/public-domain/cc0/) being the most liberal way to release it to the public domain and keep it there.
- Alongside CC, the [GNU Free Documentation License](https://www.gnu.org/licenses/fdl-1.3.html) (FDL) is also a safe way to publicly release documentation.

But, unlike human minds that read ideas and interpret an approximate concept, software works *very* precisely. Under copyright, you may not be able to legally create the same *code*, but the scope of what you're typically permitted to legally build will easily include the same *[logic](logic-cs.md)* that holds a program together. Even without copying code, enough patience and dedication means anyone can re-engineer and distribute software under copyright.

To that end, software licensing is *much* more constricting and specific than copyright.

But, don't simply release your software to the public domain without a sufficient license, or someone else could license it (or something like it) and then sue *you*. This is [more frequent than you'd realize](faang.md).

## Free Use

One of the major pioneers of the free software movement was Richard Stallman. He presented an extreme viewpoint of *completely* free software, embodied in the GPL (see below). There have been many personal criticisms leveled against him (mostly about his demeanor or hygiene), but most of that (along with his extreme views) can be simply explained by his [high-functioning autism](autism.md).

A software's "source code" is either open or closed based on how accessible the "code base" is to the public:

- Closed-source software is free for people to freely download, but the source code is at least somewhat private.
  - By contrast, open-source software is at least *somewhat* free to download, distribute, and modify.
- Only [authorized people](computers-cysec-authentication.md) can see the inner workings of the closed-source code, which makes [fixing bugs](computers-software-redesign.md) the sole responsibility of the developer, and [exploits](hacking.md) are more likely.
- In open-source software, anyone can see the code that creates the output (even while any [databases](database.md) and personal information are off-limits).

The legal and technical freedom to use the software needs more specificity than simply "freedom":

1. Freedom to run the program as you wish, for any purpose.
2. Freedom to study the program to see how it works, and change it to do your computing as you wish. To accomplish this, you must be able to access the source code.
3. Freedom to redistribute copies to help others.
4. Freedom to distribute copies of *your* modified versions to others. This gives the whole community a chance to benefit from the changes.

However, there are *other* freedoms that users can do, which may or may not infringe on everyone else's freedoms:

1. Freedom for *everyone else* to have those same freedoms (aka "copyleft", hereditary, viral).
2. Freedom to distribute software as their own, for-profit (aka, non-copyleft or "permissive").
3. Freedom to impose constraints, such as required packaging/distribution, [legal considerations](legal-safety.md), inter-regional export regulations, and [contract-based](contracts.md) licensing.

In summary, "freedom" has a few possible meanings:

- Free-as-in-freedom means others can use it at liberty for their purposes, which includes making money off it, and could possibly include [illegal things](legal-safety.md).
- Free-as-in-beer means others can use it freely, but there are restrictions to using it.

## Free Code

How freely you release your code should be driven by your motivations of what you want *other* people to do with the code:

- If you deeply care solely about making money, releasing code to the public is a bad idea.
- If you're trying to learn and want feedback, open-source allows others to draw attention to your failures, as well as fix them.
- To be influential among [programmers](programming-basics.md), public code is an excellent way to create meaningful impact and influence, since others can adapt it to their needs.
- To [educate others](pedagogy.md), open-source is the most hands-on way to do it.
- Sometimes, the software resolves a *major* problem you have, and mass-adoption of that software would make *your* life easier.

Copyright is very constricting for others' freedom relative to [the involvement many developers want to see](computers-software-versionctrl.md), and there are other options:

- Public domain forbids absolutely nothing.
- Permissive licenses forbid very little, but typically revolve around attribution.
- Copyleft licenses leans against people profiting off the work and, thus, keeping it and its permutations completely free.
- Noncommercial use is closely connected to copyleft, but with some variations.

## Licensing

To prevent the [lawsuits](legal-safety.md) and [implicit contracts](contracts.md) that would derive from a natural agreement to use a software product, the software released under open-source licenses are always "as is". There is *no* promise of future performance, and the terms of use aren't certain or complete.

- It means that it's the *users'* responsibility regarding use of the software, and the consequences that may come from it.
- The same software used for completely ethical [PenTesting](computers-cysec-pentest.md) can be used for [hacking](hacking.md), and [archiving data for security reasons](computers-cysec.md) will use the same software as [internet piracy](computers-distsys-torrent.md), with no legal consequences for the developer who made the software.

For users who consume the product, most software licenses reside within the broader "end user license [agreement](contracts.md)", or EULA, often bundled with the software itself.

There are many [licensing options](contracts.md) specifically for publishing open-source software:

- The GNU "General Public License" ([GPL](https://www.gnu.org/licenses/)) is a very permissive license, and the source for all the other GNU licenses.
  - It's completely copyleft/hereditary/viral.
  - You can make money off your code, but others can modify it and profit off it as well.
  - The only clarification is that it's not the original author's fault for defects that someone introduces later on.
  - There are several versions of it (GPLv2, GPLv3).
  - The GPL also grants certain [patent](legal-ip.md) grants as well.
  - GNU has [a whole guide for the best way to have a GPL-based licensing](https://www.gnu.org/licenses/license-recommendations.html), and its permissiveness sets the standard on whether software code is *completely* free.
  - One of the strange, and extreme, consequences of GPL is that code distributed with GPL code inside it *also* becomes GPL, meaning the code is *always* free for anyone to use, profit, or modify.
- The GNU Lesser General Public License (LGPL) is mostly the same as the GPL, but allows proprietary vendors to link free code to non-free modules.
  - The LGPL is only better if the code will reach more vendors who were otherwise unwilling to release *their* code.
  - LGPL versions run parallel to GPL.
- The GNU Affero General Public License (AGPL) is almost the same as the GPL, but clarifies that licensed software running over a network will share its source code.
- The GNU All-Permissive License is useful for small supporting files and [README files](/documentation/) contained inside software.
- The Perl Foundation's [Artistic License 2.0](https://www.perlfoundation.org/artistic-license-20.html) is completely GPL-compatible.
- The [Apache License, version 2.0](https://www.apache.org/licenses/LICENSE-2.0) is almost the same as the GPL, but its relationship is complicated.
  - Apache-licensed software is compatible with GPLv3, but GPLv3 software does *not* work with Apachev2, mostly because Apache gives more legal constraint on warranties and indemnity.
  - Apachev2 is better for [large-scale projects](computers-distsys-enterprise.md).
- The Berkeley Software Distribution (BSD, a now-obsolete [Unix-like OS](computers-os-unix.md) that has been overtaken by FreeBSD) has a GPL-compatible license.
  - It comes in a [2-clause](https://opensource.org/licenses/BSD-2-Clause/) or [3-clause](https://opensource.org/licenses/BSD-3-Clause) version, and that 3rd clause distinguishes whether the user must request for permission to attribute anything to the original creator.
- [The Unlicense](https://opensource.org/license/unlicense/) and [The MIT License](https://opensource.org/licenses/MIT) are attempts to simplify GPL.
  - The standard MIT license requires another developer to require attribution to the original creator and the fact that it's MIT licensed.
  - The [MIT No Attribution License (MIT-0)](https://opensource.org/license/mit-0/) removes the need for attribution to the original creator, making it practically the same as GPL, but with more permissiveness for commercial use.
- The [Mozilla Public License (MPL)](https://www.mozilla.org/en-US/MPL/) is the LGPL, but with the freedom for modifications to link to the original library (rather than the LGPL requiring an entirely different reference).
  - The major difference is that MPL gives more freedom for developers to link to proprietary packages, while LGPL makes it more cumbersome for those proprietary packages to exist without the freedom to swap it out with an alternative.
  - It's a weak copyleft license, in-between the GPL and BSD/MIT permissive licenses.
- The [Community Research and Academic Programming License (CRAPL)](https://matt.might.net/articles/crapl/) is designed for academics and researchers, and adds 2 conditions beyond most open-source:
  1. Any source/modifications to validate scientific claims be released with those claims.
  2. Absolve the authors of any shame, embarrassment, or ridicule for ugly code.
- Many, *many* other licenses apply to specific things:
  - One-off licenses for specific projects.
  - Some are for educational institutions or specific software libraries.
  - Large organizations will frequently make a new license that is 95% the same wording of one of the above, but with a few key differences.
- Other licenses are *not* GPL-compliant, but worth noting:
  - [Eclipse Public License (EPL)](https://opensource.org/license/epl-2-0/), a replacement for the Common Public License (CPL)
  - Sun Community Source License (SCSL)
  - Java Research License (JRL)
  - Aladdin Free Public License (AFPL)
  - The [Common Development and Distribution License (CDDL)](https://opensource.org/license/cddl-1-0/), created by Sun Microsystems, was based on the MPL, and was created to overcome the shortcomings of the MPL to allow more commercial business cases.
  - The [WTFPL](http://www.wtfpl.net/) is intentionally simple, and intentionally non-invasive, but probably not appropriate or granular enough for *many* contexts.
  - The [Anti-Capitalist Software License (ACSL)](https://anticapitalist.software/) has a [leftist](leftism.md) streak to its licensing approach.

Without any of those licenses in place, a software developer must ask permission first before modifying, distributing, or selling any derivative work. Historically, many developers did *not* do that, but it was certainly illegal.

The freedom that comes with open-source does *not* mean inherent altruism. Developers and corporations often use open-source to gain more attention to themselves, then sell closed-source software as an entirely different package, often with their open-source code inside the *closed-source* software.

In general, to summarize:

- These licenses are constantly being reworked and updated to conform to ever-changing legal environments, so there may soon be new licenses beyond the above-stated.
- If you want complete freedom for everyone, but don't want anyone to make money off the code directly, use the GPL or MIT License.
- If you want complete freedom for developers to use your code beyond the "free" space, use the LGPL.
- If you want complete freedom for anyone to use it in any way they please, use the BSD License.
- If it's a [large-scale project](computers-distsys-enterprise.md), use the Apache license.

## Pay Models

Open-source is *not* a business model, and is strictly about the release of the source code. The means to make money from it is another matter entirely. However, open-source isn't an *entirely* separate concept, since it still works within the domain of free software.

Selling software without any free options creates more work for [marketing](marketing.md), since users won't know if the product will serve their desires. Since software is nearly free to distribute, the only financial downside is giving paid-version software for free to a customer who would *otherwise* have paid for it.

The nature of software gives *many* ways to market and expose people to a free product:

- Release "bundleware" with added software included during the software's installation (most notably in [Windows-based](computers-os-windows.md) software).
  - The free software will often include unwanted junk like [browser toolbars](computers-webdev.md), [antivirus software](computers-cysec-malware.md), and [adware](computers-cysec-malware.md).
  - Generally, this requires [dark patterns](design-uxui.md) to provoke unknowing users to download the extra software.
- Load the product interface with paid advertisements from vendors.
  - This is largely becoming unpopular ever since the [online ad market started shifting](marketing.md).
  - Often, extra tracking data can be included in the product, which can also create [privacy concerns](faang.md).
- Release the product as "shareware", where it's free-to-copy, but features are cut out without a specific license key.
  - Shareware is a largely obsolete method, but some software still uses it, and [web app](computers-webdev.md) software products for [larger-scale use](computers-distsys-enterprise.md) sometimes employ the method.
  - They were notoriously annoying because they often came with 30-day free trials and were often vastly overpriced for the value they added.
- Create free products and tools with the company/brand name on them.
  - The purpose of the software is to effectively serve as an advertisement for people to become brand-aware of other paid software.
- Give away older iterations of the product for free or sell them at absurdly low discounts.
  - [Game developers](computers-software-gamedev.md) often do this about a month or two before they release another installment in their franchise.
- Release a "freemium" version of the product, with an upgraded version available with more features.
  - The most popular method is to break the product into 3 tiers, such as Basic, Plus, and Professional.
  - Typically, a vast majority of the users will use the free version, while the rest (typically under 10%) will pay for the product.
- Release the software for free as "beggarware".
  - Essentially, have a Donate button on the interface to help you continue making free software.
  - It won't make much money, but it will gain widespread attention.
- Give it away for free to certain groups (e.g., students, 1-user clients).

Contrary to most non-technical intuition, completely closed-source software can often sabotage long-term profits:

- The majority of highly intelligent people who *could* improve the software [from their particular specialization](jobs-specialization.md) won't see how the software is designed, and software [bugs](computers-software-redesign.md) will eventually lag over any open-source alternative. Thus, most intelligent people viewing the code will reverse-engineer or [pentest](computers-cysec-pentest.md) it.
- The [forbidden fruit effect](lawsaxioms.md) means that software developers are more likely to [reverse-engineer](hacking.md) it, which means they'll easily "clone" the software. The intelligence requirements of doing this means they'll likely create a better version of it.
- Software intellectual property is *very* difficult to enforce, and requires extra legal expenses to maintain it, as well as the chances of a [legal precedent](legal-doctrines.md) of *not* enforcing that intellectual property concluding in a lost suit.
- While intellectual property can protect ideas, it's only partially effective. If anything is legitimately groundbreaking, the original creator only has a few years of innovation before the idea is blatantly copied.
- Long-term unawareness of bugs and defects can carry over into future projects, meaning software developers will frequently repeat mistakes they weren't aware they were making.
- The long-term goodwill or bad faith of the public has more [reputational](legacy.md) benefit than the short-term financial gains or losses from creating software, and a sufficiently qualified open-source developer [will always find plenty of well-paid work](jobs-4_hunt-cs.md).

While open-source software may be freely licensed, the *distribution* for it may not be. It's not uncommon to see open-source software sold on app stores, printed on media, or mailed, with the cost coming strictly from distributing it. Anyone is still free to copy, share, and modify the code.

Tech companies that create [computer hardware](computers-hardware.md) will often release their code as open-source:

- Their [business model](entrepreneur-1_why-cs.md) will typically depend on selling the hardware itself, meaning there's zero risk of *any* lost profits from releasing the code for it.
- Hobbyists will be more likely to adopt open-source code, and will be able to [fix bugs](computers-software-redesign.md) or add [software features](computers-software-maintenance.md).
- The software will sometimes also gain attention as the tool for a [clever hack](hacking.md).
- Typically, if the organization fosters the hobbyist community through further hardware development, they'll have a thriving community-business relationship that will naturally maintain or increase their hardware sales.

## Open-Source Projects

Building a personal or closed-source company project into an open-source one doesn't take *too* much [documentation](language-writing-documentation-cs.md):

1. Scan the entire codebase for any "[secrets](computers-cysec-authentication.md)".
2. If a company, replace internal names and emails with public ones.
3. Write the contribution guidelines (in CONTRIBUTING.md).
4. Write templates for [bug reports](computers-software-redesign.md) and [pull requests](computers-software-versionctrl.md).
5. Choose and insert the license (LICENSE.md).
6. Write the [security](safety-security.md) policy (SECURITY.md).
7. Write the project's introduction (README.md).

Human nature mixed with freely distributed software means it's constantly tweaked and rebuilt, which creates a few inevitable realities in comparison to closed-source software:

1. The entire project is defined heavily by how well both paid and volunteer developers respond to the community.
   - If there isn't much feedback, the project will have *more* [bugs](/software-redesign/) than a proprietary version with a [team of developers](mgmt-2_projects-cs.md).
2. There's no indefinite Definitive Edition of a particular software.
   - If you're even *moderately* successful, other people will adapt your software, and [alternative versions](computers-software-versionctrl.md) will arise from your original work.
   - Even when a developer's project gains widespread acceptance, there's always an "edge case" where someone will make a variant.
   - Sometimes, that variant becomes more reliable or feature-rich than the original, and can sometimes compete with the original version or become the new Definitive [Version](computers-software-versionctrl.md).
3. There's rarely a final, polished look to open-source.
   - As a general rule, [geeks aren't specialized in the same domain](https://trendless.tech/understanding/), so great back-end design often uses a boring interface.
   - While [good UX design](design-uxui.md) is important, it doesn't mean it has to have much aesthetic.
   - Lousy UX can sometimes turn off average users who are accustomed to high-grade [marketing](marketing.md) built into the software, but the open-source subculture (such as [GNU/Linux](computers-os-unix.md) fans) often won't care if the software does their work better.
4. Some of the most talented software developers in the world build open-source.
   - While [finding a bug](fix-computers.md) is often easy, open-source software allows a qualified developer to localize the code that creates the bug, then create code that [submits a pull request](computers-software-versionctrl.md) to fix it.
   - Since *everyone* is looking at the codebase, it allows more accountability, which can dramatically improve how [safe](computers-cysec.md) the software is from bad actors.

While a [hacker](hacking.md) *could* insert [malicious code](computers-cysec-malware.md) into open-source software, they'd have to submit a pull request that had to get approved. A developer who worked very hard to build software will *not* approve something that turns it into malware or bricks it. However, a bad actor has the full capacity to fork and release a different version, though it may be difficult for the tech community to trust its legitimacy (i.e., "What makes *that* software better than what we know about already?").

Often, code might *not* be open-source within a company. If that's the case, a developer who worked at that company may not be free to publish it legally. It doesn't stop many of them, however, from [*illegally* publishing it](computers-cysec-pentest.md) (usually anonymously). Most software developers avoid this conundrum by establishing one of the above-stated open-source licenses before writing any code, even if they don't publish until after they leave the company.

## Scaling

When all things are equal, open-source [scales better](computers-distsys.md) for end-users.

- You don't need to purchase a license for each device.
- The support is more scattered, but a sufficiently talented software developer can fix an open-source software themselves, without waiting for the company to get to it. This is *desperately* important when time is critical, such as in a [startup](entrepreneur-1_why-cs.md).

The extra complexity of larger projects means developers can mix-and-match licensing:

- "Multi-licensing" involves issuing differing licenses for the same software, typically divided by usage (e.g., one license for commercial use, another for non-commercial use).

Getting funding to be an open-source developer is *not* easy.

- They typically are paid *far* less than standard [Big Tech workers](https://trendless.tech/your-job-sucks/), with some of them even at risk of [homelessness](hardship-homeless.md).
- Most of them must either [work an unrelated job](jobs-2_goals-cs.md) or use [clever](mind-creativity.md) financing solutions (such as charging to [operate servers](computers-distsys.md) with their software) to pay the bills.
- Eventually, if the project continues to grow, they *will* need a more direct source of funding, and should consider ways to either turn their project into an [entrepreneurial product](entrepreneur-1_why-cs.md) or give it up for others to maintain.

If the developer's work was relatively easy, but depends on *other* work, then they may simply deflect all donations to those developers' efforts instead.

[Large-scale](computers-distsys-enterprise.md) open-source projects require tons of resources, so developers at some point of growth *must* get funding for the project to stay continuously up-to-date:

- The developer receives contributions from other people to keep supporting his work (e.g., donation button on their website, crowdsourcing).
- The developer or organization has to convert the product to something people pay for (see above).
- Open-source-supporting [not-for-profit organizations](mgmt-npo.md) provide grants to keep the developers paid (e.g., [Free Software Foundation](https://www.fsf.org/), [Mozilla Foundation](https://foundation.mozilla.org/en/), [Linux Foundation](https://www.linuxfoundation.org/), [NLnet](https://nlnet.nl/)).
- Corporations who benefit from the product contribute, often *through* the above-stated NPOs to make it [tax-deductible](accounting.md).

When [larger companies](mgmt-5_communication-cs.md) use open-source from an outside developer, they *must* be aware of the risks, and it's their responsibility to take action:

- They're consenting to a weak [implicit contract](contracts.md), with little to no promises on either side.
- They are adopting a copy of the software as-is, which may mean they're potentially trusting the [security](computers-cysec.md) and [reliability](computers-cysec-compliance.md) of their company's infrastructure to an overworked parent or college student.
- The only way the relationship will become more mutually advantageous requires equipping the open-source developer. This may include moral support, publicity, and *always* requires funding.
- When it works well, the users support the maintainers, and the maintainers support the users, and everyone wins.
- When it doesn't, the developers often experience [severe hardship](hardship.md) and the project falls apart. This can be an especially tragic story because the developer will frequently toil selflessly for *years* without recognition or assistance before giving up. Other times, they're a victim of an unfortunate situation where more money to pay legal fees or medical bills could have resolved or assisted them.
- Occasionally, a developer may completely snap and intentionally destroy their project, such as delivering an update that bricks their system, sending [malware](computers-cysec-malware.md) through their software, or deleting their codebase. This only occurs through severe mental illness, which is often (but not always) from the stress caused by a lack of [personal human support](people-4_friends.md).

## Back-End vs. Front-End

Generally, back-end programming is designed to feed information into other software (e.g., "middleware").

Most people outside the tech industry don't realize it, but *how* a back-end developer licenses their software has a severe impact on the industry. In particular, GPL code leans everything toward completely public code, but can become *very* difficult to clarify where any particular code (or its derivatives) begin or end being "free".

While it doesn't draw all the attention of front-end software, back-end software has more power. A closed-source back-end is essentially [how Big Tech maintains its control](faang.md), and is the basis for most political bluster.

But, this back-end/front-end dichotomy [travels backward several degrees](https://trendless.tech/understanding/), and one of the most significant ways this shows itself is through the implementation of open [protocols](standards-computers.md).

- Even when there are plenty of closed-source frameworks or front-end software, protocols are the farthest possible upstream system before getting to [computer hardware](computers-hardware.md).
- The presence of an open protocol allows ambitious developers to circumvent any frameworks which may be closed off to them.
- Many technology standards are *not* open (e.g., ISO standards), which adds a heavy financial burden that prevents innovation and reduces transparency.
- If a hardware designer is particularly confident in what they're building, they'll make their own *hardware* standards open. Over time, this can create a tremendously loyal community, and [adoption](trends.md) can make it industry-standard.

Beyond open software and data, one of the most popular open-source developments in [CPU design](computers-cpu.md) comes through a completely open software architecture called [RISC-V](https://riscv.org/), which superseded the open-architecture movement OpenRISC held for a while.

- You can even make it at home yourself, and it's a very appealing approach for many hardware [startups](entrepreneur-1_why-cs.md).
- However, there are *many* other open standards that have not been created that RISC-V must rely on, such as [memory](computers-memory.md) controllers and interfaces, USB, and [PCI](computers-motherboard.md).

Even when *everything* is open, distributors must stay aware of whether software or operating systems are presently compatible with their hardware. Failure to do so will result in the users being adversely affected and general dissatisfaction with the product. When it comes time to [blame someone](image-distortion.md), distributors [have historically been labeled at-fault for the failure](https://dont-ship.it/).

## Inter-Community Conflicts

If it's public-facing, open-source software developers will get plenty of unwarranted hate for what they do, especially if their software becomes popular. Some developers [enjoy some levity with it](https://notepad-plus-plus.org/news/v843-unhappy-users-edition/), but there are often many toxic people who send unpleasant messages.

While the codebase is completely public and open, open-source [version control](politics-systems.md) forms into several competing views:

1. Anyone is free to contribute or fork whatever they want, and the original code owners will support all the variants.
   - It's a type of [communism](politics-systems.md), which creates an organic and varied form of growth, but is wildly unpredictable.
   - In terms of quality, it's often *very* difficult for fully open software to compete with proprietary software.
2. Anyone is free to contribute or fork whatever they want, but the original code owners possess a "[benevolent dictatorship](politics-systems.md)" through the approval/denial of [pull requests](computers-software-versionctrl.md).
   - This is a much more hands-on form of [management](groupslarge.md) (and can sometimes become highly controversial).
   - Centralized control by a few developers guarantees a more effective software, and the software is often *better* than any proprietary software could be.
   - However, there's a *much* higher likelihood of the code forking off due to a petty dispute over a mostly irrelevant feature.
3. An "open-core" concept, with all the features coming as plugins or extensions.
   - The final software is effectively a proprietary system, with most of the work maintaining the code performed by the organization's members.
   - This has been proven as a successful [business model](entrepreneur-2_idea-cs.md) (e.g., Google's Android OS, most Apache software) that allows complete freedom while also giving control to the original developers.
   - It's not uncommon for forks without that [organization's](groupslarge.md) involvement, which may mean competition or dramatic permutations from the original software.
4. People are *not* free to contribute or fork whatever they want (closed-contribution), though the software is still open-source.
   - This is basically #2, but with more constraints, since too many pull requests can cause burnout for developers.
   - [Features](computers-software-maintenance.md) require extra work to implement, and then require more work to maintain.
   - Usually, the pull requests are constrained to *only* [bug fixes](computers-software-redesign.md).

Open-source projects are *not* exempt from politics and [social decay](mgmt-badsystems.md).

- Many open-source developers feel entitled:
  - They may feel their contributions deserve [recognition](image.md), they deserve payment, or their pull requests should be automatically approved from [what they've done in the past](power-influence.md).
- The scope of authority in an open-source project comes through how much contribution someone invests into it, and an open-source community has the same [group hierarchy](groupssmall.md) as any other organization.
  - They often must invest time to follow the project's mailing list or pull requests, and typically must follow the group's [social norms](people-rules.md).
- Every open-source project goes through the same predictable [trend](trends.md) of growth, stagnation, then decay, which will eventually spawn a [defective culture](mgmt-badsystems.md) around it.
  - Sometimes, a long-standing and popular open software may be significantly inferior to another open-source product, but can screw up the [reputation](image.md) of the *entire* open-source community by dominating everyone's attention. This entire situation can make proprietary choices prevail for longer.
- It's not uncommon for large organizations running on open-source software to *not* credit specific developers who [find bugs](computers-software-redesign.md) in the code, often with them responding rudely to the developer before publicizing they fixed the bug.
- [Technical idiots](https://gainedin.site/idiot/) who are *not* aware of how open-source works may demand answers or fixes from open-source developers.
  - Ironically, if they *do* perform without compensation, this can [set a precedent](contracts.md) that frames a type of business contract, though it's not typically enforced (since it's [too unethical](morality.md) for any reasonable judge to rule in the favor of the requestor).
  - Some of the more [contract-savvy](contracts.md) developers will ask them to arrange a business arrangement first before acting more promptly.
  - Every software developer must learn [healthy boundaries](boundaries.md) to avoid the exploit and abuse from ignorant [managers](mgmt-1_why.md).
- If a company offers both a proprietary and open-source version, and the proprietary version makes more money, they may completely disregard the open-source version.
- If a developer significant to a project ever starts committing implementations of their current [political views](politics-conservativeliberal.md) into the project, political fashions can overtake projects and corrupt them away from their simple purpose.
- Since the developers have to [pay their bills](money-3_budget.md), they need *some* sort of funding. This may connect to the software itself (see above), or the project may have to run like a [not-for-profit](mgmt-npo.md).

However, the beauty of *any* open-source project is that absolutely anyone can fork the original code and create something new with it, thereby building their own software inspired by the original software.

Sometimes, irrespective of the relationship with the original creator, it may be wise to fork the software.

- To expand on an open-source project with very few recent updates, fork the project and start your own, or find other people who have made a more recent project that does effectively the same thing.
- If the software is used for anything sensitive, it needs attention on it to maintain [security patches](computers-cysec-compliance.md).
- The licensing may bind you into constraints you may not want (e.g., can't sell the software without also releasing the code), and a fork may provide opportunities to change that.
- If the software is used for particularly high-attention things (e.g., [illegal activities](computers-distsys-torrent.md)), it may make sense to clone a copy of the software to prevent complete removal of the software for the public to use.

## Legal Conflicts

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
- GPL code has effectively been labeled as a [contract-based matter](contracts.md), *not* over [intellectual property](legal-ip.md). It doesn't make much intuitive sense, but it [gives lawyers more work](legal-doctrines.md) and means the payment for damages is generally higher (i.e., [California district court](https://web.archive.org/web/20200719095524/https://www.theregister.com/2017/05/13/gnu_gpl_enforceable_contract/)).
- There are also movements that imply that *any* [decompilation](computers-compilers.md) of software might be legal, if only for the intention of [fixing a bug](computers-software-redesign.md). Nothing says the [core logic](computers-alu.md) can't be reproduced, either, even if the software isn't outright copied (i.e., [EU court ruling](https://curia.europa.eu/juris/document/document.jsf?text=&docid=247056&pageIndex=0&doclang=en&mode=req&dir=&occ=first&part=1)).
- Copying your software's [API outputs](programming-basics.md) to make it interoperable with another, more popular software *might* be legal, but will be somewhat of an uphill battle to wrestle over the dispute (i.e., [Google vs. Oracle's Java ruling](https://www.supremecourt.gov/opinions/20pdf/18-956_d18f.pdf)).
- Calling software open-source when it's *not* open-source is considered false advertising.

The reality about software developers is many of them (especially anyone who wants to work on an open-source project) does *not* care as much about money as they do about their [specialization](jobs-specialization.md) inside computers.

- Legal battles are unpleasant, and it's very difficult to visualize anyone who [engages in lawfare](legal-safety.md) against software developers that make software free to the public as anything *but* an [antagonistic](stories.md) or [evil](morality-evil.md) entity.
- The [win/win solution](people-conflicts.md) is to give substantial wealth to those developers: if a tool generated a few hundred million dollars for a company, give a few million to that developer.
- However, barring that, some software-based lawyers [near the end of their life](legacy.md) would be *thrilled* to lend their time to winning legal battles that promote free software.

## FLOSS Trends

Anytime a popular closed-source version of a software becomes popular, *someone* will want to recreate an open-source version of it:

- The [GNU/Linux operating system](computers-os-unix.md), as well as FreeBSD, are derived from the technically-closed-source Unix.
- Just about every software application, including calculators and word processing, now has an open-source alternative.
- Most [games](computers-software-gamedev.md) have been modded with open-source plugins that improve or fix the game, and the entire *codebase* of some popular games have been entirely rebuilt as open-source (e.g., Elder Scrolls games, Command & Conquer).
- Even many [enterprise-grade software](computers-distsys-enterprise.md) have been successfully reproduced as open-source.

Often, when the tech-related economy starts dipping (often because [a tech trend](trends.md) failed spectacularly), open-source becomes less common. Gigantic open-source corporations may release projects as entirely closed-source, or create closed-source modules.

At the same time, open-source becomes the dumping ground for anything Big Tech has to shed due to [antitrust lawsuits](politics-monopolies.md) or [company downsizing](mgmt-7_changes.md) (e.g., the history of [Linux](computers-os-unix.md)). As every large tech company [invariably fails](mgmt-badsystems.md), *something* has to maintain what it held up, and that role eventually becomes open-source if it was popular enough.

## Future FLOSS Trends

A few decades ago, most operating systems and software were closed-source, but most software is at least *partially* open-source. In fact, for almost any technology older than a few years, there's an open-source alternative.

This set of facts leads open-source advocates to conclude that the open-source [trend](trends.md) will *completely* take over software licensing, but they're forgetting a few additional facts:

- The required amount of research to create brand-new software can often be costly, so most companies concerned with profits tend to create closed-source software for new things.
- By contrast, the motive for open-source development over closed-source is never directly for financial profit.
- Thus, open-source development is always a trend that follows closely *after* a closed-source option became [a trend of its own](trends.md).

In one sense, open-source has *already* taken over the tech industry, but [in name only](image.md) as mistaken [marketing jargon](marketing.md) for *free*.

Any software or hardware industry only becomes open-source when several conditions are fulfilled:

1. There haven't been any new developments that change the core function of the object or its implementation.
2. It's [widely adopted](trends.md), in its standardized form.
3. Some open-source variants are significantly superior to their closed-source competitors.

In other words, all tech become open-source when they become commodities and software developers can imitate them. All it needs is the software to be good-enough, then the users will trust the open-source solution more.

But, the influence of open-source goes farther than its actual basis, and the concept has transcended software licensing:

- Open-source advocates have expanded the idea into open-source billing, which is nothing more than charging for the *precise* components and features a user has selected for use.
- The idea expands (at least partly) into other domains:
  - [Seeds](https://worldsensorium.com/open-source-seeds-loosen-big-ags-grip-on-farmers/)
  - [Contracts](https://standard.open-contracting.org/)
  - [Academic research papers](https://www.researchprofessionalnews.com/rr-news-europe-infrastructure-2023-5-eu-ready-to-back-immediate-open-access-without-author-fees/)
  - [Economic models](https://github.com/DREAM-DK/MAKRO)
  - [Microscope designs](https://ibm-research.medium.com/ibm-open-sources-300-fully-functional-lego-microscope-design-248a6cdc81bf)

There need to always be freedom advocates willing to obsess about everyone's freedom.

- Literally, every new proprietary technology needs open-source advocates to defend public use of it (e.g., [robotics](computers-robotics.md), [quantum computers](computers-quantum.md), [DNA programming](computers-biological.md)).
- The [degradation into a defective society](mgmt-badsystems.md) that violates [individual liberties](boundaries.md) comes through nobody taking action against those risks when they arise.
- [Far too often](humanity-universals.md), people tend to react to the crisis *after* it has become severe, instead of facing the issues when they can be easily resolved.

## Additional Reading

[What is Free Software?](https://www.gnu.org/philosophy/free-sw.html)

[The MIT License, Line by Line](https://writing.kemitchell.com/2016/09/21/MIT-License-Line-by-Line.html)

[How to safely open-source internal software](https://blog.gitguardian.com/safely-open-source-software-best-practices/)
