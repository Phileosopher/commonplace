
# Business models and FLOSS

## Pay Models

Open-source is *not* a business model, and is strictly about the release of the source code. The means to make money from it is another matter entirely. However, open-source isn't an *entirely* separate concept, since it still works within the domain of free software.

Selling software without any free options creates more work for [marketing](marketing.md), since users won't know if the product will serve their desires. Since software is nearly free to distribute, the only financial downside is giving paid-version software for free to a customer who would *otherwise* have paid for it.

The nature of software gives *many* ways to market and expose people to a free product:

- Release "bundleware" with added software included during the software's installation (most notably in [Windows-based](computers-os-windows.md) software).
  - The free software will often include unwanted junk like [browser toolbars](computers-sofware-webdev.md), [antivirus software](computers-cysec-malware.md), and [adware](computers-cysec-malware.md).
  - Generally, this requires [dark patterns](engineering-design.md) to provoke unknowing users to download the extra software.
- Load the product interface with paid advertisements from vendors.
  - This is largely becoming unpopular ever since the [online ad market started shifting](marketing.md).
  - Often, extra tracking data can be included in the product, which can also create [privacy concerns](faang.md).
- Release the product as "shareware", where it's free-to-copy, but features are cut out without a specific license key.
  - Shareware is a largely obsolete method, but some software still uses it, and [web app](computers-sofware-webdev.md) software products for [larger-scale use](computers-distsys-enterprise.md) sometimes employ the method.
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
- Software intellectual property is *very* difficult to enforce, and requires extra legal expenses to maintain it, as well as the chances of a [legal precedent](lawsaxioms-legal.md) of *not* enforcing that intellectual property concluding in a lost suit.
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
   - If there isn't much feedback, the project will have *more* [bugs](computers-software-redesign.md) than a proprietary version with a [team of developers](mgmt-2_projects-cs.md).
2. There's no indefinite Definitive Edition of a particular software.
   - If you're even *moderately* successful, other people will adapt your software, and [alternative versions](computers-software-versionctrl.md) will arise from your original work.
   - Even when a developer's project gains widespread acceptance, there's always an "edge case" where someone will make a variant.
   - Sometimes, that variant becomes more reliable or feature-rich than the original, and can sometimes compete with the original version or become the new Definitive [Version](computers-software-versionctrl.md).
3. There's rarely a final, polished look to open-source.
   - As a general rule, [geeks aren't specialized in the same domain](https://trendless.tech/understanding/), so great back-end design often uses a boring interface.
   - While [good UX design](engineering-design.md) is important, it doesn't mean it has to have much aesthetic.
   - Lousy UX can sometimes turn off average users who are accustomed to high-grade [marketing](marketing.md) built into the software, but the open-source subculture (such as [GNU/Linux](computers-os-unix.md) fans) often won't care if the software does their work better.
4. Some of the most talented software developers in the world build open-source.
   - While [finding a bug](fix-cs.md) is often easy, open-source software allows a qualified developer to localize the code that creates the bug, then create code that [submits a pull request](computers-software-versionctrl.md) to fix it.
   - Since *everyone* is looking at the codebase, it allows more accountability, which can dramatically improve how [safe](computers-cysec.md) the software is from bad actors.

While a [hacker](hacking.md) *could* insert [malicious code](computers-cysec-malware.md) into open-source software, they'd have to submit a pull request that had to get approved. A developer who worked very hard to build software will *not* approve something that turns it into malware or bricks it. However, a bad actor has the full capacity to fork and release a different version, though it may be difficult for the tech community to trust its legitimacy (i.e., "What makes *that* software better than what we know about already?").

Often, code might *not* be open-source within a company. If that's the case, a developer who worked at that company may not be free to publish it legally. It doesn't stop many of them, however, from [*illegally* publishing it](computers-cysec-pentest.md) (usually anonymously). Most software developers avoid this conundrum by establishing one of the above-stated open-source licenses before writing any code, even if they don't publish until after they leave the company.
