
# FLOSS licensing

To prevent the [lawsuits](legal-safety.md) and [implicit contracts](people-contracts.md) that would derive from a natural agreement to use a software product, the software released under open-source licenses are always "as is". There is *no* promise of future performance, and the terms of use aren't certain or complete.

- It means that it's the *users'* responsibility regarding use of the software, and the consequences that may come from it.
- The same software used for completely ethical [PenTesting](computers-cysec-pentest.md) can be used for [hacking](hacking.md), and [archiving data for security reasons](computers-cysec.md) will use the same software as [internet piracy](computers-distsys-torrent.md), with no legal consequences for the developer who made the software.

For users who consume the product, most software licenses reside within the broader "end user license [agreement](people-contracts.md)", or EULA, often bundled with the software itself.

There are many [licensing options](people-contracts.md) specifically for publishing open-source software:

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
- The GNU All-Permissive License is useful for small supporting files and [README files](language-writing-documentation.md) contained inside software.
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
  - The [Anti-Capitalist Software License (ACSL)](https://anticapitalist.software/) has a [leftist](politics-leftism.md) streak to its licensing approach.

Without any of those licenses in place, a software developer must ask permission first before modifying, distributing, or selling any derivative work. Historically, many developers did *not* do that, but it was certainly illegal.

The freedom that comes with open-source does *not* mean inherent altruism. Developers and corporations often use open-source to gain more attention to themselves, then sell closed-source software as an entirely different package, often with their open-source code inside the *closed-source* software.

In general, to summarize:

- These licenses are constantly being reworked and updated to conform to ever-changing legal environments, so there may soon be new licenses beyond the above-stated.
- If you want complete freedom for everyone, but don't want anyone to make money off the code directly, use the GPL or MIT License.
- If you want complete freedom for developers to use your code beyond the "free" space, use the LGPL.
- If you want complete freedom for anyone to use it in any way they please, use the BSD License.
- If it's a [large-scale project](computers-distsys-enterprise.md), use the Apache license.
