
# FLOSS licensing explained

While [intellectual property](legal-ip.md) *generally* sits on a spectrum of usage (e.g., free to consume but not distribute, free to distribute if it's also free), software has its complexities regarding free use of code.

The broad term for the entire domain was FOSS (Free and Open-Source Software), but has more particularly used the acronym FLOSS (Free/Libre Open-Source Software).

In many ways, developers are passively taking a type of [political stance](power-types.md) based on their adoption of open-source licensing, and users are passively endorsing those politics by [consenting](people-contracts.md) to use that software.

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
3. Freedom to impose constraints, such as required packaging/distribution, [legal considerations](legal-safety.md), inter-regional export regulations, and [contract-based](people-contracts.md) licensing.

In summary, "freedom" has a few possible meanings:

- Free-as-in-freedom means others can use it at liberty for their purposes, which includes making money off it, and could possibly include [illegal things](legal-safety.md).
- Free-as-in-beer means others can use it freely, but there are restrictions to using it.

## Free Code

How freely you release your code should be driven by your motivations of what you want *other* people to do with the code:

- If you deeply care solely about making money, releasing code to the public is a bad idea.
- If you're trying to learn and want feedback, open-source allows others to draw attention to your failures, as well as fix them.
- To be influential among [programmers](computers-programming.md), public code is an excellent way to create meaningful impact and influence, since others can adapt it to their needs.
- To [educate others](education.md), open-source is the most hands-on way to do it.
- Sometimes, the software resolves a *major* problem you have, and mass-adoption of that software would make *your* life easier.

Copyright is very constricting for others' freedom relative to [the involvement many developers want to see](computers-software-versionctrl.md), and there are other options:

- Public domain forbids absolutely nothing.
- Permissive licenses forbid very little, but typically revolve around attribution.
- Copyleft licenses leans against people profiting off the work and, thus, keeping it and its permutations completely free.
- Noncommercial use is closely connected to copyleft, but with some variations.

However, the [licensing can get complicated](legal-ip-floss-licenses.md) to make this happen, and [the business models](legal-ip-floss-business.md) aren't always so straightforward.

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
- Corporations who benefit from the product contribute, often *through* the above-stated NPOs to make it [tax-deductible](money-accounting.md).

When [larger companies](mgmt-5_communication-cs.md) use open-source from an outside developer, they *must* be aware of the risks, and it's their responsibility to take action:

- They're consenting to a weak [implicit contract](people-contracts.md), with little to no promises on either side.
- They are adopting a copy of the software as-is, which may mean they're potentially trusting the [security](computers-cysec.md) and [reliability](computers-cysec-compliance.md) of their company's infrastructure to an overworked parent or college student.
- The only way the relationship will become more mutually advantageous requires equipping the open-source developer. This may include moral support, publicity, and *always* requires funding.
- When it works well, the users support the maintainers, and the maintainers support the users, and everyone wins.
- When it doesn't, the developers often experience [severe hardship](hardship.md) and the project falls apart. This can be an especially tragic story because the developer will frequently toil selflessly for *years* without recognition or assistance before giving up. Other times, they're a victim of an unfortunate situation where more money to pay legal fees or medical bills could have resolved or assisted them.
- Occasionally, a developer may completely snap and intentionally destroy their project, such as delivering an update that bricks their system, sending [malware](computers-cysec-malware.md) through their software, or deleting their codebase. This only occurs through severe mental illness, which is often (but not always) from the stress caused by a lack of [personal human support](people-friends.md).

With all the risks associated, it's not really much of a surprise that [FLOSS creates conflicts](legal-ip-floss-conflicts.md).

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

Even when *everything* is open, distributors must stay aware of whether software or operating systems are presently compatible with their hardware. Failure to do so will result in the users being adversely affected and general dissatisfaction with the product. When it comes time to [blame someone](people-image-distortion.md), distributors [have historically been labeled at-fault for the failure](https://dont-ship.it/).

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

In one sense, open-source has *already* taken over the tech industry, but [in name only](people-image-why.md) as mistaken [marketing jargon](marketing.md) for *free*.

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
- The [degradation into a defective society](mgmt-badsystems.md) that violates [individual liberties](people-boundaries-why.md) comes through nobody taking action against those risks when they arise.
- [Far too often](humanity-universals.md), people tend to react to the crisis *after* it has become severe, instead of facing the issues when they can be easily resolved.

## Additional Reading

[What is Free Software?](https://www.gnu.org/philosophy/free-sw.html)

[The MIT License, Line by Line](https://writing.kemitchell.com/2016/09/21/MIT-License-Line-by-Line.html)

[How to safely open-source internal software](https://blog.gitguardian.com/safely-open-source-software-best-practices/)
