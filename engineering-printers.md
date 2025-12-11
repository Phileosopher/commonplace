
# What printers and 3D printers are

The printer is a much older output than the [computer screen](engineering-screen.md), and was once much cheaper. Now, since screens can display a wide variety of information (and do it indefinitely), they're *far* cheaper to maintain than printers.

Printer output uses nearly the same internal framework as screen output:

1. The CPU sends information stored in memory through an "interpreter" to a "print spooler" process.
2. The print spooler breaks down the print instructions, line by line, and runs it through the [printer device driver](computers-os.md).
3. The printer itself receives the driver-translated information and carries out its ink/toner output.

It's worth noting that "print" is still the term for a [console output](computers-cli.md), and from the software's perspective the two are effectively the same, since they both travel out to a device driver that handles what happens next.

## Hardware

Many printers use ink, but quite a few office printers use toner, which is mostly a type of plastic ground into extremely fine dust.

Ink is directly injected onto the paper, but toner printers use a few extra steps:

1. Spray the toner dust evenly on the entire page.
2. Use a heating element (like a laser or LED) to melt the toner into letters and images, line-by-line. Laser printers, in particular, heat a drum that rolls onto the paper.
3. Blow off the dust and gather it for reuse, which also cools the page at the same time to prevent it from catching fire.

Most daily-use printers for receipts use a special heat-sensitive paper, with the printer applying a heating element in a pattern. Exposing it to heat or direct sunlight will turn it black, which makes it terrible for archiving documents.

Beyond imposing a black substance onto a paper medium, there are various other printer features:

- Color printing allows color-based cartridges alongside black. Unlike the [screen](engineering-screen.md), printers use reflected light instead of visible light. So, instead of combining emitted wavelengths with additive colors (red/blue/green), printers use subtractive primary colors instead to *reflect* wavelengths (cyan/magenta/yellow).
- "Duplex printing" will print a page on both sides. This isn't *strictly* necessary, but can be a severe logistical headache if you're trying to print out a lot of content (e.g., print odd-numbered pages, then load up the pages again and print even-numbered pages).
- [Network](networks-cs.md) printing allows a printer to connect with other computers on a network, and typically implies it's a wireless connection.
- Secure printing allows a [password-protected](computers-cysec-authentication.md) print job, which may be important in a large office.
- For larger printers, including a decent-enough [scanner](computers-ocr.md).
- If it comes with the functionality of a scanner, it technically has a copier feature as well. However, it's simply printing a scanned (and spooled) copy instead of how copier technology directly imposes a scanned image.
- While it's not as popular anymore, including a [fax machine](networks-cs.md).
- Multiple trays to allow printing different paper sizes or types, which can also include a multipurpose tray.
- Toner/ink page counter, which can *also* serve to cost more money long-term in wasted toner/ink (see below).

But, most of the features are simply extra padding for the quality of a printer. Instead, watch for legitimate performance metrics to determine the printer's quality:

- Duty cycle - the number of pages (typically thousands or tens of thousands) before it needs routine servicing.
- Memory - how much on-board [memory](computers-memory.md) it has, which determines how many print jobs it can store in its queue.
- Speed - raw printing speed, which can also include the time for it to warm up.
- Reliability - the number of paper jams relative to the number of pages it prints.

## Unreliable

The workings inside a printer are vastly complicated, which is why printers are notoriously unreliable:

- Toner has a tendency to gum up over time and halt the printer or make it print at an odd angle.
- The mechanical rollers of a printer aren't always great quality, and pages can print askew or jam.
- When starting, the printer's heating element often has to engage, which slows down the time it takes for it to start.
- The entire process of heating toner and blowing off excess is an orchestra of moving parts.
- Large-scale printers must feed the paper through an elaborate pathway to accommodate a waist-high entry and exit point.

Updating printers is difficult, since it requires the physical constraints of hardware design, unlike [software](computers-software.md). And unlike software, updates and feedback only roll out at the speed of people buying the new version, so there's no chance to [publicly test](computers-software-redesign.md) printers before a new printer design is thoroughly approved. The extra complexities of printer hardware compared to a [mouse](computers-mouse.md) or [keyboard](computers-keyboard.md) mean they're always behind the reliability of most other I/O devices.

If the printer is connected to a central network (and *especially* if that network is connected to [the internet](computers-sofware-webdev.md)), lagging [security updates](computers-cysec.md) can be a severe problem. Even when a printer doesn't hold on to personal information, it can still have malware installed directly onto its firmware.

However, a long time ago, printers were *far* more flammable. This came from a combination of paper dust, the older dot-matrix printer ribbons, and the fact that some printer cleaning solutions were combustible. A simple spark or enough heat from a heavy printer workload was enough to ignite the device.

Printers becoming more efficient is also not very cost-beneficial to corporations that sell printers. Toner is more expensive per-ounce than blood or silver, and is the profitable aspect of most printers, so creating [exclusionary right-to-repair-violating design](faang.md) and generally inefficient toner use is the best way to make more money.

In many ways, printers *can* become more reliable, but there's no financial incentive to do so, especially now that society has trended more toward *paperless* information transfer. Most printers tend to be awfully designed, but try to compensate with as many built-in features as a [marketing trick](marketing.md) to imply additional value.

## 3D printing

3D printing, or "additive manufacturing" (AM), is one of the newest technologies in the [printing](engineering-printers.md) industry, though it's technically been available since the 1970s.

### History

The first clear idea of AM arose in a few short stories in 1945 and 1950, but the first patent for the technology was in 1971 by Johannes Gottwald. It was called the Liquid Metal Recorder and permitted on-demand melting away metal according to an on-demand pattern.

The first 3D printers used metal, but the 1980s saw tremendous leaps in plastic-based implementations and a layered approach:

- A 1981 research paper that invented two additive methods to fabricate plastic models with photo-hardened thermoset polymer.
- A 1982 patent that used hundreds or thousands of layers of powdered metal, with a laser energy source.
- A 1984 USA patent for a computer automated manufacturing process and system.
- A 1984 French patent for "stereo lithography", which involved adding material to an object until it reached a desired form.
- A 1984 USA patent was also filed for an improved stereo lithography format.
- In 1988, Scott Crump designed FDM (fused deposition modeling), which has been the standard for most 3D printers since its inception.

It wasn't commercially successful. In the 1980s, a 3D printer cost about $300,000, and the cost meant it wasn't very useful relative to manufacturing objects for a specific purpose (e.g., factory equipment).

The term 3D printing has gone through some permutations. At one time, it referred to [metal sintering](engineering.md), but changed as plastic started becoming the standard for AM in the 2010s.

### General implementation

The process is a relatively straightforward approach:

1. Use CAD software to create a desired output form, which is often using the same or similar CAD software as most [graphics technology](engineering-graphics.md).
2. Output the CAD software's information into an STL [file](computers-files.md) (for stereo lithography), which will store data of the CAD model's surfaces.
3. That CAD STL file will frequently have errors, and there are a *lot* of error-correcting procedures to fix the *many* possible failures (e.g., warping, curling, holes, lines, vibrations), as well as structural risks (bridging failure, walls caving in, etc.). This often includes building other supports around the object:
   - Rafts are entire layers that sit below the build.
   - Brims are preferable to rafts, and simply extend from the edge of the build to enable the build to stick to the bed.
   - Skirts are created around the object, but not directly touching it, to prepare the extruder for the first layer and slow down the cooling of the lowest layers.
4. The CAD file converts to G-code, a [programming language](computers-languages.md) that instructs where the printer should move in physical space with [Cartesian coordinates](math-algebra.md), layer-by-layer.
5. Convert that CAD file into instructions for the printer using proprietary code that corresponds with the printer.
6. The printer creates the form, one step at a time (typically layer-by-layer), typically by extruding a polymer "filament" and using UV light to harden and congeal it.
7. Post-process to fix more errors (e.g., clumping, elephant's foot, lines on the side).

STL files aren't exactly straightforward. Their data is stored as [triangulation](math-geotrig.md), and AMF files (AM file format) try to remedy some of those by including curved triangulation.

Like [a standard printer](engineering-printers.md), the printer's resolution is represented as dots per inch (dpi), but can also represent as micrometers (μm). A typical layer's thickness is ~100 μm (or 250 dpi) though some machines can print as small as 16 μm (or 1,600 dpi).

Contrary to plastic, metal 3D printing works with aluminum or stainless-steel powder and a weak binding agent to create a hollowed-out form, then covering the form with aluminum oxide and pouring in bronze. The technique is much faster and affordable than conventional methods.

Beyond that, the details are very specific to the method. Many approaches are simply additive, but additive/subtractive hybrid manufacturing (ASHM) involves *both* adding and removing.

### Power

The ability for *anyone* with [design](engineering-graphics.md) skills to make what they [imagine](imagination.md) has tremendous implications:

1. Engineers can effectively prototype and test their creations within a matter of days, not weeks or months.
2. The opportunity to create anything can include protected [intellectual property](legal-ip.md) and [illegal](people-rules.md) objects (e.g., guns).

Currently, as of 2023, an affordable and decent 3D printer for small uses can be $200, and [that price will only go down over time](money-economics.md) without government intervention. This situation will only magnify as the technology improves.

Naturally, this extra power provides tremendous independence. Someone can, in theory, print the components necessary for the object they're working with. Even if it's sub-par, it gives the ability to only need copious amounts of filament to make anything the CAD can design.

### Opportunity

The technology continues to improve as well. While polymer plastics are the best and most affordable option, there are new technologies arriving soon:

1. Printing with metals and ceramics are starting to arise as viable AM techniques, as well as other domains such as [Wagyu beef](https://newatlas.com/science/world-first-lab-grown-wagyu-beef-japan).
2. With metals and ceramics, multi-material printing with different material types is also on the horizon.
3. 4D printing involves forming an object based on its desired future form (i.e., changing shape over time with temperature or some other stimulation like pressure).
4. As printers become more effective, they'll soon be able to create large structures like bridge components and houses, which will *radically* define [logistics](logistics.md): simply send over raw materials and the printer to a hard-to-navigate site.
5. Printers can print increasingly smaller sizes ([at 25 nanometers long right now](https://interestingengineering.com/science/scientists-can-now-print-metal-objects-that-are-only-25-nanometers-long)), meaning it may *radically* redefine the manufacture of electronic components, such as [processors](computers-cpu.md) or [memory](computers-memory.md), in the not-too-distant future.

Within a century, it won't be uncommon to see [startups](entrepreneur-1_why.md) building many materials with a 3D printer, and it may happen as early as 2040.

### DIY

You can even [build your own computer numerical control (CNC) 3D printer](https://github.com/maxvfischer/DIY-CNC-machine).

Or, if you want something *far* less sophisticated, you can build a 3D printer out of old parts:

1. Acquire everything you need:
   - 3 CD/DVD drives, which are often perfectly intact in older computers
   - An old computer's power supply
   - 3 Arduino controllers
   - A cheap 3D printing pen that extrudes a filament
2. Remove the spiral stepper motor from all 3 drives, which will serve as the X, Y, and Z coordinate axes.
3. Mount the motors to the CD cases, then all 3 motor housings to each other for all 3 axes.
4. Add a flat metal plate to the Y axis, to give something to hold the object being printed.
5. Attach each of the controllers for the 3 motors to the Arduino controllers.
6. Bypass the power switch detection by [connecting a ground pin to PS-ON](engineering-printers-1.jpg) with a small bit of wire (which effectively overrides the power-on switch).
7. Attach the power supply to the Arduino and motors.
8. Pull apart the 3D printing pen and configure the engage button to work off a transistor, with a resistor to limit the power from the Arduino, then attach to the power supply and Arduino.
9. Install grbl to the Arduinos, then use grbl software for sending the code to the printer.
10. Code the software to calibrate the printer, [which should look close to the following](engineering-printers-2.jpg).
