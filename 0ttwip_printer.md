
The printer is a much older output than the [computer screen](/screen/), and was once much cheaper. Now, since screens can display a wide variety of information (and do it indefinitely), they're *far* cheaper to maintain than printers.

Printer output uses nearly the same internal framework as screen output:

1. The CPU sends information stored in memory through an "interpreter" to a "print spooler" process.
2. The print spooler breaks down the print instructions, line by line, and runs it through the [printer device driver](/os/).
3. The printer itself receives the driver-translated information and carries out its ink/toner output.

It's worth noting that "print" is still the term for a [console output](/consoles/), and from the software's perspective the two are effectively the same, since they both travel out to a device driver that handles what happens next.

## Hardware

Many printers use ink, but quite a few office printers use toner, which is mostly a type of plastic ground into extremely fine dust.

Ink is directly injected onto the paper, but toner printers use a few extra steps:

1. Spray the toner dust evenly on the entire page.
2. Use a heating element (like a laser or LED) to melt the toner into letters and images, line-by-line. Laser printers, in particular, heat a drum that rolls onto the paper.
3. Blow off the dust and gather it for reuse, which also cools the page at the same time to prevent it from catching fire.

Most daily-use printers for receipts use a special heat-sensitive paper, with the printer applying a heating element in a pattern. Exposing it to heat or direct sunlight will turn it black, which makes it terrible for archiving documents.

Beyond imposing a black substance onto a paper medium, there are various other printer features:

- Color printing allows color-based cartridges alongside black. Unlike the [screen](/screen/), printers use reflected light instead of visible light. So, instead of combining emitted wavelengths with additive colors (red/blue/green), printers use subtractive primary colors instead to *reflect* wavelengths (cyan/magenta/yellow).
- "Duplex printing" will print a page on both sides. This isn't *strictly* necessary, but can be a severe logistical headache if you're trying to print out a lot of content (e.g., print odd-numbered pages, then load up the pages again and print even-numbered pages).
- [Network](/networks/) printing allows a printer to connect with other computers on a network, and typically implies it's a wireless connection.
- Secure printing allows a [password-protected](/authentication/) print job, which may be important in a large office.
- For larger printers, including a decent-enough [scanner](/handwriting-ocr/).
- If it comes with the functionality of a scanner, it technically has a copier feature as well. However, it's simply printing a scanned (and spooled) copy instead of how copier technology directly imposes a scanned image.
- While it's not as popular anymore, including a [fax machine](/networks/).
- Multiple trays to allow printing different paper sizes or types, which can also include a multipurpose tray.
- Toner/ink page counter, which can *also* serve to cost more money long-term in wasted toner/ink (see below).

But, most of the features are simply extra padding for the quality of a printer. Instead, watch for legitimate performance metrics to determine the printer's quality:

- Duty cycle - the number of pages (typically thousands or tens of thousands) before it needs routine servicing.
- Memory - how much on-board [memory](/memory/) it has, which determines how many print jobs it can store in its queue.
- Speed - raw printing speed, which can also include the time for it to warm up.
- Reliability - the number of paper jams relative to the number of pages it prints.

## Unreliable

The workings inside a printer are vastly complicated, which is why printers are notoriously unreliable:

- Toner has a tendency to gum up over time and halt the printer or make it print at an odd angle.
- The mechanical rollers of a printer aren't always great quality, and pages can print askew or jam.
- When starting, the printer's heating element often has to engage, which slows down the time it takes for it to start.
- The entire process of heating toner and blowing off excess is an orchestra of moving parts.
- Large-scale printers must feed the paper through an elaborate pathway to accommodate a waist-high entry and exit point.

Updating printers is difficult, since it requires the physical constraints of hardware design, unlike [software](/software-design/). And unlike software, updates and feedback only roll out at the speed of people buying the new version, so there's no chance to [publicly test](/software-redesign/) printers before a new printer design is thoroughly approved. The extra complexities of printer hardware compared to a [mouse](/mouse/) or [keyboard](/keyboard/) mean they're always behind the reliability of most other I/O devices.

If the printer is connected to a central network (and *especially* if that network is connected to [the internet](/web-dev/)), lagging [security updates](/security/) can be a severe problem. Even when a printer doesn't hold on to personal information, it can still have malware installed directly onto its firmware.

However, a long time ago, printers were *far* more flammable. This came from a combination of paper dust, the older dot-matrix printer ribbons, and the fact that some printer cleaning solutions were combustible. A simple spark or enough heat from a heavy printer workload was enough to ignite the device.

Printers becoming more efficient is also not very cost-beneficial to corporations that sell printers. Toner is more expensive per-ounce than blood or silver, and is the profitable aspect of most printers, so creating [exclusionary right-to-repair-violating design](/faang/) and generally inefficient toner use is the best way to make more money.

In many ways, printers *can* become more reliable, but there's no financial incentive to do so, especially now that society has trended more toward *paperless* information transfer. Most printers tend to be awfully designed, but try to compensate with as many built-in features as a [marketing trick](https://notageni.us/marketing/) to imply additional value.
