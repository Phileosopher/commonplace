
3D printing, or "additive manufacturing" (AM), is one of the newest technologies in the [printing](computers-printers.md) industry, though it's technically been available since the 1970s.

## History

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

## General implementation

The process is a relatively straightforward approach:

1. Use CAD software to create a desired output form, which is often using the same or similar CAD software as most [graphics technology](graphics.md).
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

Like [a standard printer](computers-printers.md), the printer's resolution is represented as dots per inch (dpi), but can also represent as micrometers (μm). A typical layer's thickness is ~100 μm (or 250 dpi) though some machines can print as small as 16 μm (or 1,600 dpi).

Contrary to plastic, metal 3D printing works with aluminum or stainless-steel powder and a weak binding agent to create a hollowed-out form, then covering the form with aluminum oxide and pouring in bronze. The technique is much faster and affordable than conventional methods.

Beyond that, the details are very specific to the method. Many approaches are simply additive, but additive/subtractive hybrid manufacturing (ASHM) involves *both* adding and removing.

## Power

The ability for *anyone* with [design](graphics.md) skills to make what they [imagine](imagination.md) has tremendous implications:

1. Engineers can effectively prototype and test their creations within a matter of days, not weeks or months.
2. The opportunity to create anything can include protected [intellectual property](legal-ip.md) and [illegal](rules.md) objects (e.g., guns).

Currently, as of 2023, an affordable and decent 3D printer for small uses can be $200, and [that price will only go down over time](economics.md) without government intervention. This situation will only magnify as the technology improves.

Naturally, this extra power provides tremendous independence. Someone can, in theory, print the components necessary for the object they're working with. Even if it's sub-par, it gives the ability to only need copious amounts of filament to make anything the CAD can design.

## Opportunity

The technology continues to improve as well. While polymer plastics are the best and most affordable option, there are new technologies arriving soon:

1. Printing with metals and ceramics are starting to arise as viable AM techniques, as well as other domains such as [Wagyu beef](https://newatlas.com/science/world-first-lab-grown-wagyu-beef-japan).
2. With metals and ceramics, multi-material printing with different material types is also on the horizon.
3. 4D printing involves forming an object based on its desired future form (i.e., changing shape over time with temperature or some other stimulation like pressure).
4. As printers become more effective, they'll soon be able to create large structures like bridge components and houses, which will *radically* define [logistics](logistics.md): simply send over raw materials and the printer to a hard-to-navigate site.
5. Printers can print increasingly smaller sizes ([at 25 nanometers long right now](https://interestingengineering.com/science/scientists-can-now-print-metal-objects-that-are-only-25-nanometers-long)), meaning it may *radically* redefine the manufacture of electronic components, such as [processors](computers-cpu.md) or [memory](computers-memory.md), in the not-too-distant future.

Within a century, it won't be uncommon to see [startups](entrepreneur-1_why.md) building many materials with a 3D printer, and it may happen as early as 2040.

## DIY

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
6. Bypass the power switch detection by connecting a ground pin to PS-ON with a small bit of wire (which effectively overrides the power-on switch).
   - ![](https://trendless.tech/wp-content/uploads/2023/10/power-supply.jpg)
7. Attach the power supply to the Arduino and motors.
8. Pull apart the 3D printing pen and configure the engage button to work off a transistor, with a resistor to limit the power from the Arduino, then attach to the power supply and Arduino.
9. Install grbl to the Arduinos, then use grbl software for sending the code to the printer.
10. Code the software to calibrate the printer, which should look close to the following:
    - ![](https://trendless.tech/wp-content/uploads/2023/10/3dprintercode.jpg)
